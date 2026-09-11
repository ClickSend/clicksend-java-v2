# Migration Guide: clicksend-java-client (legacy) → clicksend-java (v2)

This guide helps you migrate from the legacy ClickSend Java SDK (`com.clicksend:clicksend-java-client`, package `ClickSend.*`) to the current v2 SDK (`com.clicksend:clicksend-java`, package `ClickSend.*` — unchanged). The two SDKs are **not drop-in compatible** — the Maven coordinates, method names, request/response shapes, and a few internals have all changed. Read this guide fully before upgrading, then use the class/method mapping tables to update your code.

## Contents

1. [Why this migration isn't a drop-in replacement](#1-why-this-migration-isnt-a-drop-in-replacement)
2. [Installation & imports](#2-installation--imports)
3. [Authentication & client setup](#3-authentication--client-setup)
4. [Base path / URL changes](#4-base-path--url-changes)
5. [Method naming convention change](#5-method-naming-convention-change)
6. [Request payloads: `*Request` models replace reusable domain models](#6-request-payloads-request-models-replace-reusable-domain-models)
7. [Response payloads are now properly typed](#7-response-payloads-are-now-properly-typed)
8. [Error handling changes](#8-error-handling-changes)
9. [`ApiCallback` async calls are preserved — only the type parameter changes](#9-apicallback-async-calls-are-preserved--only-the-type-parameter-changes)
10. [Class-by-class mapping (all 37 legacy classes)](#10-class-by-class-mapping-all-37-legacy-classes)
11. [Side-by-side examples for common operations](#11-side-by-side-examples-for-common-operations)
12. [The Voice naming trap (read this before touching voice code)](#12-the-voice-naming-trap-read-this-before-touching-voice-code)
13. [Endpoints/methods removed in v2](#13-endpointsmethods-removed-in-v2)
14. [Brand-new resources and methods in v2](#14-brand-new-resources-and-methods-in-v2)
15. [Step-by-step migration checklist](#15-step-by-step-migration-checklist)

## 1. Why this migration isn't a drop-in replacement

The legacy SDK grew organically against ClickSend's v3 API: one API class per rough "concept" split further into separate "delivery receipt rules" / "inbound rules" classes (e.g. `SmsApi`, `SmsDeliveryReceiptRulesApi`, and `InboundSmsRulesApi` were three *separate* classes for what is now one `SmsApi`), method names followed a `resourcePathHttpVerb` pattern (`smsSendPost`, `smsHistoryGet`), request bodies were broad reusable domain models (`SmsMessage`, `SmsMessageCollection`), and **every method returned a raw, unparsed `String`** — callers had to deserialize the JSON themselves.

The v2 SDK is generated fresh from ClickSend's current OpenAPI v3 specification for Java, which:

- Groups methods into **one class per resource/tag** (26 classes instead of 37 — several legacy classes were merged, one was split, and the Fax, Post Letters, and Post Postcards classes were dropped entirely — see [§13](#13-endpointsmethods-removed-in-v2)).
- Names methods after the endpoint's **operationId** (camelCase, e.g. `sendSms`, `viewSmsHistory`, `exportSmsHistory`) instead of `resourcePath` + HTTP verb.
- Wraps every request body in a dedicated, single-purpose `*Request` model (e.g. `SendSmsRequest`) instead of reusing broad domain models (e.g. `SmsMessageCollection`), and gives nested list items their own `*Inner`-suffixed model (`SendSmsRequestMessagesInner`) instead of a standalone class (`SmsMessage`).
- **Deserializes every response into a specific, strongly-typed model class** (e.g. `SendSms`) instead of returning a raw `String`.
- Keeps `ApiException` in the same package with the same core methods, and adds `getMessage()`.
- Bumps the Maven `artifactId` from `clicksend-java-client` to `clicksend-java` (the `groupId`, `com.clicksend`, is unchanged — see [§2](#2-installation--imports)).
- Actually **lowers** the minimum Java version needed to compile from the bytecode target the legacy SDK ships (11) to 1.8 — see [§2](#2-installation--imports) for the important caveat about the legacy README's stated requirement.
- **Keeps the synchronous/`ApiCallback`-async dual API surface** — unlike some other ClickSend SDKs' v2 migrations, Java does **not** drop async calling; only the callback's generic type parameter changes (see [§9](#9-apicallback-async-calls-are-preserved--only-the-type-parameter-changes)).

None of this changes the underlying REST API — it's the same ClickSend v3 API — but it does change **every call site** in your existing integration.

## 2. Installation & imports

### Maven

```xml
<!-- Legacy -->
<dependency>
  <groupId>com.clicksend</groupId>
  <artifactId>clicksend-java-client</artifactId>
  <version>1.0.0</version>
</dependency>
```

```xml
<!-- v2 -->
<dependency>
  <groupId>com.clicksend</groupId>
  <artifactId>clicksend-java</artifactId>
  <version>6.0.2</version>
</dependency>
```

**The `groupId` is unchanged (`com.clicksend`) — only the `artifactId` changes**, from `clicksend-java-client` to `clicksend-java`. This is still a new dependency coordinate (Maven treats a different `artifactId` as a different artifact), so remove the old dependency rather than just bumping its version — but note this is *not* a `groupId` rename, despite that being a common pattern in other ClickSend SDK migrations.

### Gradle

```groovy
// Legacy
implementation "com.clicksend:clicksend-java-client:1.0.0"
```

```groovy
// v2
implementation "com.clicksend:clicksend-java:6.0.2"
```

### Java / build-tool requirements — read this carefully

| | Legacy | v2 |
|---|---|---|
| README-stated Java requirement | "Java 1.7+" | "Java 1.8 or newer" |
| **Actual `pom.xml` compiler target** (`maven.compiler.source`/`target`) | **`11`** | **`1.8`** |
| README-stated build tool | "Maven/Gradle" (no version stated) | Maven 3.8.3+ or Gradle 7.2+ |
| `maven-enforcer-plugin` `requireMavenVersion` (actually enforced) | `2.2.0` | `2.2.0` (same rule; the README's 3.8.3+ is a documentation recommendation, not an enforced minimum) |

**The legacy SDK's own README understates its Java requirement.** Its `pom.xml` sets `<java.version>11</java.version>` (and `maven.compiler.source`/`target` both derive from it), so the legacy JAR is actually compiled for **Java 11 bytecode** despite the README claiming "Java 1.7+". The v2 SDK's `pom.xml` sets `<java.version>1.8</java.version>`, matching its README. **Net effect: v2 has a *lower* minimum Java version than the legacy SDK actually requires**, which is the opposite of what you'd naively expect from a major-version bump — verify against your own runtime before assuming you need a newer JDK to upgrade.

### Transitive dependencies

If your build explicitly pins or excludes any of the SDK's transitive libraries, note these changes:

| Library | Legacy | v2 |
|---|---|---|
| `io.swagger:swagger-annotations` | `1.6.14` | removed |
| `org.threeten:threetenbp` | `1.6.8` | removed |
| `com.google.code.gson:gson` | `2.10.1` | `2.10.1` (unchanged) |
| `io.gsonfire:gson-fire` | `1.8.5` | `1.9.0` |
| `com.squareup.okhttp3:okhttp` / `logging-interceptor` | `4.12.0` | `4.12.0` (unchanged) |
| `com.google.code.findbugs:jsr305` | — | `3.0.2` (new) |
| `jakarta.annotation:jakarta.annotation-api` | — | `1.3.5` (new, `provided` scope) |
| `jakarta.ws.rs:jakarta.ws.rs-api` | — | new (new) |
| `org.openapitools:jackson-databind-nullable` | — | `0.2.10` (new) |
| `org.apache.commons:commons-lang3` | — | `3.18.0` (new) |
| Test framework | JUnit `4.13.2` | JUnit Jupiter `5.10.3` + `junit-platform-runner` `1.10.0` (no Mockito) |

Package structure is unchanged: both SDKs use `ClickSend.Api`, `ClickSend.Model`, and `ClickSend.auth` as the top-level packages. `import ClickSend.Api.SmsApi;`, `import ClickSend.Model.*;`, and `import ClickSend.auth.*;` still work verbatim in v2 — only *which* classes exist inside `ClickSend.Api`/`ClickSend.Model` changes (see [§10](#10-class-by-class-mapping-all-37-legacy-classes)).

> Model classes went from **47** (shared/reused across endpoints) to **384** (overwhelmingly one request/response model per endpoint, e.g. `SendSmsRequest`, `SendSmsRequestMessagesInner`, `SendSms`).

## 3. Authentication & client setup

The mechanism (HTTP Basic Auth using your ClickSend **username** and **API key** as the password) and the object graph (`Configuration` → `ApiClient` → `*Api`) are unchanged. The only functional difference is the **case of the auth-scheme name** used to look it up:

```java
// Legacy
import ClickSend.ApiClient;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.Api.SmsApi;

ApiClient defaultClient = Configuration.getDefaultApiClient();
HttpBasicAuth BasicAuth = (HttpBasicAuth) defaultClient.getAuthentication("BasicAuth");
BasicAuth.setUsername("YOUR USERNAME");
BasicAuth.setPassword("YOUR API KEY");

SmsApi apiInstance = new SmsApi();
```

```java
// v2
import ClickSend.ApiClient;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.Api.SmsApi;

ApiClient defaultClient = Configuration.getDefaultApiClient();
HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
basicAuth.setUsername(System.getenv("CLICKSEND_USERNAME"));
basicAuth.setPassword(System.getenv("CLICKSEND_API_KEY"));

SmsApi apiInstance = new SmsApi(defaultClient);
```

| | Legacy | v2 |
|---|---|---|
| `Configuration.getDefaultApiClient()` | plain static holder | same idea, now backed by an `AtomicReference` for thread safety; adds `Configuration.setApiClientFactory(...)` |
| Auth-scheme key in `getAuthentication(...)` | `"BasicAuth"` (capital B) | `"basicAuth"` (lowercase b) |
| `*Api` no-arg constructor | uses `Configuration.getDefaultApiClient()` internally — still works in both | still works in both, but prefer `new SmsApi(defaultClient)` once you have more than one `ApiClient` |
| Default `User-Agent` | `ClickSend-Codegen/1.0.0/java` | `ClickSend-SDK/6.0.2/java`, changeable via `apiClient.setUserAgent("...")` |
| `HttpBearerAuth` | not present | added to `ClickSend.auth` (unused by ClickSend's own Basic-Auth endpoints; informational) |

`defaultClient.getAuthentication("BasicAuth")` (old casing) returns `null` against the v2 client — update the string literal to `"basicAuth"`. If you only ever call `.setUsername(...)`/`.setPassword(...)` on the object you already looked up, the fix is a single-line string change.

## 4. Base path / URL changes

| | Legacy | v2 |
|---|---|---|
| Default `basePath` (`ApiClient.java`) | `https://rest.clicksend.com/v3` | `https://rest.clicksend.com` |
| Per-method path | `/sms/send` (no version prefix — baked into the host) | `/v3/sms/send` (the `/v3` prefix is part of each method's path) |
| Override method | `apiClient.setBasePath(...)` | `apiClient.setBasePath(...)` (same name) |

The final resolved URL is identical in both cases (`https://rest.clicksend.com/v3/sms/send`). This only matters if you:

- Called `getBasePath()` and manually appended `/v3` or a resource path yourself.
- Pointed `setBasePath(...)` at a proxy/mock server whose paths assume no `/v3` prefix — remove any hardcoded `/v3` suffix from your custom host when you switch to v2, otherwise you'll request `.../v3/v3/sms/send`.
- Read the new `ServerConfiguration`/`ServerVariable` classes — these are new additions to `ApiClient`'s public surface for multi-server OpenAPI support; they aren't used by the ClickSend spec today.

## 5. Method naming convention change

Every method on every API class has been renamed. There is no shared prefix/suffix rule you can find-and-replace — the new names follow each endpoint's `operationId` (camelCased), which reads like an English phrase, while the old ones followed `resourcePath` + HTTP verb.

| Legacy | v2 |
|---|---|
| `smsSendPost` | `sendSms` |
| `smsHistoryGet` | `viewSmsHistory` |
| `smsHistoryExportGet` | `exportSmsHistory` |
| `smsTemplatesByTemplateIdDelete` | `deleteSmsTemplate` |
| `listsContactsByListIdPost` | `createNewContact` |
| `subaccountsPost` | `createSubaccount` |
| `voiceLangGet` | `viewVoiceLanguages` |
| `numbersSearchByCountryGet` | `viewAvailableNumbers` |

**You cannot mechanically derive the new name from the old one.** Use the mapping tables in [§10](#10-class-by-class-mapping-all-37-legacy-classes)–[§11](#11-side-by-side-examples-for-common-operations), or import the relevant `*Api` class and let your IDE's autocomplete suggest candidates — the new names are descriptive enough that the right method is usually the first sensible match.

## 6. Request payloads: `*Request` models replace reusable domain models

Legacy methods took a broad, reusable domain model directly as the payload, and returned an unparsed `String`:

```java
// Legacy
import ClickSend.Model.SmsMessage;
import ClickSend.Model.SmsMessageCollection;
import ClickSend.Api.SmsApi;

SmsMessage message = new SmsMessage();
message.setTo("+61411111111");
message.setBody("Hello from ClickSend!");

SmsMessageCollection smsMessages = new SmsMessageCollection();
smsMessages.setMessages(Arrays.asList(message));

String result = apiInstance.smsSendPost(smsMessages); // raw JSON string
```

v2 introduces **one dedicated `*Request` model per operation**, and nearly every method also takes a leading, nullable `String contentType` parameter for the `Content-Type` header:

```java
// v2
import ClickSend.Model.SendSmsRequest;
import ClickSend.Model.SendSmsRequestMessagesInner;
import ClickSend.Model.SendSms;
import ClickSend.Api.SmsApi;

SendSmsRequestMessagesInner message = new SendSmsRequestMessagesInner();
message.setTo("+61411111111");
message.setBody("Hello from ClickSend!");
message.setSource("sdk"); // omit to fall back to the built-in default — see below

SendSmsRequest sendSmsRequest = new SendSmsRequest();
sendSmsRequest.setMessages(Arrays.asList(message));

SendSms result = apiInstance.sendSms(null, sendSmsRequest); // contentType, then request body
```

Practical implications:

- **The old domain-model class names mostly don't exist in v2.** `SmsMessage`, `SmsMessageCollection`, `Contact`, `ContactList`, `Subaccount`, etc. are gone. The `Model/` package went from 47 files to 384, almost all named after a specific operation (`SendSmsRequest.java`, `CreateNewContactRequest.java`, `CreateSubaccountRequest.java`, …) rather than a domain noun. Nested list items get their own generated `*Inner` models too (e.g. `SendSmsRequestMessagesInner`, `SendersInner`).
- **Because Java is statically typed, you cannot silently misplace the payload the way you could in a dynamically-typed SDK.** The `contentType` parameter comes *before* the request-body parameter in every method signature (`sendSms(String contentType, SendSmsRequest sendSmsRequest)`), but swapping the argument order fails to *compile* rather than silently sending an empty body — the compiler will reject a `SendSmsRequest` where a `String` is expected. Passing `null` for `contentType` is fine and is what the SDK's own README example does.
- **The sender field is a plain `from` — Java has no `_from`/`var_from`-style rename.** `SendSmsRequestMessagesInner.getFrom()`/`.setFrom(String)` map straight to JSON `"from"`, same shape as the legacy `SmsMessage.getFrom()`/`.setFrom(String)`.
- **`source` now defaults to `"sdk-java"`** on `SendSmsRequestMessagesInner` (and the analogous MMS/voice message-item models) if you don't set it explicitly — confirmed by the field initializer `private String source = "sdk-java";` in the generated model. Legacy had no default.
- **Field types changed on some carried-over field names**, not just class names — these fail loudly at compile time rather than misbehaving at runtime, but still require code changes. Example, sending to a contact list:

  | Field | Legacy type (`SmsMessage`) | v2 type (`SendSmsRequestMessagesInner`) |
  |---|---|---|
  | `listId` | `Integer` | `String` |
  | `contactId` | *(not present)* | `Integer` *(new; marked "no longer in use" in the current API docs)* |
  | `excludeNoSenderIdRecipients` | *(not present)* | `Boolean` *(new)* |

  The `SendSmsRequest` wrapper itself also gained two top-level fields with no legacy equivalent: `senders` (`List<SendersInner>`, per-country sender-ID overrides) and `shortenUrls` (`Boolean`).
- **Not every "update" method gets its own dedicated request model.** Most do (e.g. `EmailApi.updateEmailCampaign` takes `UpdateEmailCampaignRequest`), but `ListsApi.updateList` reuses `CreateListRequest` rather than a separate `UpdateListRequest` — don't assume a `*Request` class name always matches the method name; check the actual method signature.
- Treat every model as new — even where the class name is unchanged (e.g. `EmailAddress` exists in both SDKs) — double-check field names/types against the current `docs/<Model>.md` in this repo rather than assuming parity with the legacy docs.

## 7. Response payloads are now properly typed

Legacy responses were **always typed `String`** and never deserialized — you parsed the JSON yourself (Gson, Jackson, manual parsing), knowing the shape out-of-band from the API docs.

```java
// Legacy — return value is a raw JSON string
String result = apiInstance.smsSendPost(smsMessages);
// caller must parse `result` themselves
```

v2 deserializes every response into a specific per-operation model class (e.g. `SendSms`, `ViewSmsHistory`, `CalculateSmsPrice`), so the return value is typed and IDE-autocomplete-friendly:

```java
// v2 — return value is a SendSms instance
SendSms result = apiInstance.sendSms(null, sendSmsRequest);
System.out.println(result.getData().getMessages());
System.out.println(result.getData().getTotalPrice());
```

**Migration action:** find every place your code parses the `String` result from a legacy call (Gson/Jackson deserialization, manual field digging, etc.) and replace it with direct getter access on the typed model v2 returns. To get the status code and headers alongside the body, use the `*WithHttpInfo` variant of any method (returns an `ApiResponse<T>` with `.getData()`, `.getStatusCode()`, `.getHeaders()`) — both SDKs have always had this variant.

## 8. Error handling changes

`ApiException` stays in the same package (`ClickSend.ApiException`) with the same core methods — `getCode()`, `getResponseBody()`, `getResponseHeaders()` are unchanged in name and semantics. v2 adds one method:

```java
// Works unchanged against both SDKs, plus the new getMessage() in v2
try {
    SendSms result = apiInstance.sendSms(null, sendSmsRequest);
} catch (ApiException e) {
    System.err.println("Status code: " + e.getCode());
    System.err.println("Reason: " + e.getResponseBody());
    System.err.println("Response headers: " + e.getResponseHeaders());
    System.err.println("Message: " + e.getMessage()); // new in v2 — not present on the legacy ApiException
    e.printStackTrace();
}
```

**No changes are required to existing `catch (ApiException e)` blocks** — this is one of the few places the migration is a true drop-in. Unlike some other ClickSend SDKs' v2 rewrites, the Java v2 SDK does **not** add status-specific exception subclasses (no `BadRequestException`/`UnauthorizedException`/etc.) — `ApiException` remains the single exception type for all non-2xx responses in both versions.

## 9. `ApiCallback` async calls are preserved — only the type parameter changes

**Not removed.** Unlike SDKs that dropped their thread-pool-based async mode entirely in v2, the Java SDK's `okhttp3`-backed asynchronous calling convention survives unchanged in both versions: every method has a synchronous form, an internal `*Call(...)` builder, and an async `*Async(...)` form that takes an `ApiCallback<T>` and returns an `okhttp3.Call` you can `.cancel()`.

```java
// Legacy — ApiCallback<String> because every response was a raw string
apiInstance.smsSendPostAsync(smsMessages, new ApiCallback<String>() {
    @Override
    public void onSuccess(String result, int statusCode, Map<String, List<String>> responseHeaders) {
        System.out.println(result); // raw JSON string
    }
    @Override
    public void onFailure(ApiException e, int statusCode, Map<String, List<String>> responseHeaders) {
        e.printStackTrace();
    }
    @Override
    public void onUploadProgress(long bytesWritten, long contentLength, boolean done) {}
    @Override
    public void onDownloadProgress(long bytesRead, long contentLength, boolean done) {}
});
```

```java
// v2 — ApiCallback<SendSms> because the response is now typed; contentType is now a leading param
apiInstance.sendSmsAsync(null, sendSmsRequest, new ApiCallback<SendSms>() {
    @Override
    public void onSuccess(SendSms result, int statusCode, Map<String, List<String>> responseHeaders) {
        System.out.println(result.getData().getTotalPrice()); // typed
    }
    @Override
    public void onFailure(ApiException e, int statusCode, Map<String, List<String>> responseHeaders) {
        e.printStackTrace();
    }
    @Override
    public void onUploadProgress(long bytesWritten, long contentLength, boolean done) {}
    @Override
    public void onDownloadProgress(long bytesRead, long contentLength, boolean done) {}
});
```

**The only change is the generic type parameter** (`ApiCallback<String>` → `ApiCallback<SendSms>`, matching whatever model that operation returns) and the extra leading `contentType` argument — the same signature change described in [§6](#6-request-payloads-request-models-replace-reusable-domain-models). If you use `*Async` calls anywhere, update the callback's declared type to match the new return model and thread the `contentType` argument through, but **no architectural change is needed** — you do not need to introduce your own thread pool or executor to keep async behavior working, unlike SDKs where async support was dropped.

## 10. Class-by-class mapping (all 37 legacy classes)

26 v2 classes now cover what used to be 37 legacy classes. Some legacy classes merged (five email classes → one `EmailApi`); the Fax, Post Letters, and Post Postcards classes were **dropped entirely** (see [§13](#13-endpointsmethods-removed-in-v2)); and — critically — the two Voice classes **swapped roles** in v2 naming (see [§12](#12-the-voice-naming-trap-read-this-before-touching-voice-code)).

| Legacy class | → | New class(es) | Notes |
|---|---|---|---|
| `AccountApi` | → | `ManagementApi`, `VerificationApi` | Split: `accountGet`/`accountUseageBySubaccountGet` → `ManagementApi`; `forgotPasswordPut`/`forgotUsernamePut` → `VerificationApi`. Four methods have no v2 equivalent — see [§13](#13-endpointsmethods-removed-in-v2). |
| `AccountRechargeApi` | → | `TransactionsApi` | Renamed 1:1 (6 methods). |
| `ContactApi` | → | `ContactsApi`, `ListsApi` | Split: single-contact-by-id CRUD → `ContactsApi` (3 methods); list-scoped contact ops (create/list/copy/transfer/remove-opted-out) → `ListsApi`. |
| `ContactListApi` | → | `ListsApi` | Merged into `ListsApi`. |
| `CountriesApi` | → | `InternationalMessagingApi` | `countriesGet` → `viewCountries`. |
| `DeliveryIssuesApi` | → | `MessageDeliveryApi` | Renamed. Unrelated to the delivery-*receipt-rule* classes despite the similar name. |
| `DetectAddressApi` | → | _(removed)_ | Address detection/parsing has no v2 equivalent — see [§13](#13-endpointsmethods-removed-in-v2). |
| `EmailDeliveryReceiptRulesApi` | → | `EmailApi` | Folded into the unified `EmailApi`. |
| `EmailMarketingApi` | → | `EmailApi` | Folded into the unified `EmailApi`. |
| `EmailToSmsApi` | → | `EmailToSmsApi` | Same class name, all 7 methods renamed. |
| `FaxApi` | → | _(removed)_ | Fax is not part of the v2 SDK — see [§13](#13-endpointsmethods-removed-in-v2). |
| `FaxDeliveryReceiptRulesApi` | → | _(removed)_ | Fax is not part of the v2 SDK — see [§13](#13-endpointsmethods-removed-in-v2). |
| `GlobalSendingApi` | → | `InternationalMessagingApi` | Folded in (`userCountries*` → `viewCountries`/`selectCountriesForGlobalSending`/`agreeToRulesAndRegulation`; `listCountriesGet` → `getCountriesForGlobalSending`). |
| `InboundFaxRulesApi` | → | _(removed)_ | Fax is not part of the v2 SDK — see [§13](#13-endpointsmethods-removed-in-v2). |
| `InboundSmsRulesApi` | → | `SmsApi` | Folded in as `*SmsInboundAutomation(s)`. |
| `MasterEmailTemplatesApi` | → | `EmailApi` | Folded into the unified `EmailApi`. |
| `MmsApi` | → | `MmsApi` | Same class name; renamed 1:1 for 4 methods, 2 dropped — see [§13](#13-endpointsmethods-removed-in-v2). |
| `MmsCampaignApi` | → | `MmsCampaignsApi` | Renamed 1:1 (6 methods). |
| `NumberApi` | → | `NumbersApi` | Renamed 1:1 (3 methods), plus a brand-new `registerNumbers` — see [§14](#14-brand-new-resources-and-methods-in-v2). |
| `PostLetterApi` | → | _(removed)_ | Post Letters is not part of the v2 SDK — see [§13](#13-endpointsmethods-removed-in-v2). |
| `PostPostcardApi` | → | _(removed)_ | Post Postcards is not part of the v2 SDK — see [§13](#13-endpointsmethods-removed-in-v2). |
| `PostReturnAddressApi` | → | `AddressesApi` | Renamed (5 methods): `postReturnAddresses*` → `*ReturnAddress(es)`. |
| `ReferralAccountApi` | → | `ReferralsApi` | `referralAccountsGet` → `viewReferralAccounts`. |
| `ResellerAccountApi` | → | `ResellerApi` | Merged with `TransferCreditApi`. |
| `SearchApi` | → | `ListsApi` | `searchContactsListsGet` → `viewContactLists`. |
| `SmsApi` | → | `SmsApi` | Same class name; renamed 1:1 for all core methods. |
| `SmsCampaignApi` | → | `SmsCampaignsApi` | Renamed 1:1 (6 methods). |
| `SmsDeliveryReceiptRulesApi` | → | `SmsApi` | Folded in as `*SmsDeliveryReceiptRule(s)`. |
| `StatisticsApi` | → | `StatisticsApi` | Same class name: `statisticsSmsGet` → `viewSmsStatistics`, `statisticsVoiceGet` → `viewVoiceStatistics`. |
| `SubaccountApi` | → | `SubaccountsApi` | Renamed 1:1 (6 methods). |
| `TimezonesApi` | → | `InternationalMessagingApi` | `timezonesGet` → `timezones`. |
| `TransactionalEmailApi` | → | `EmailApi` | Folded into the unified `EmailApi`. |
| `TransferCreditApi` | → | `ResellerApi` | Merged with `ResellerAccountApi`; `resellerTransferCreditPut` → `resellerTransferCredit`. |
| `UploadApi` | → | `UploadsApi` | `uploadsPost` → `uploadAMediaFile`. |
| `UserEmailTemplatesApi` | → | `EmailApi` | Folded into the unified `EmailApi`. |
| `VoiceApi` (send/history/price/lang) | → | **`VoiceMessagingApi`** | ⚠️ See [§12](#12-the-voice-naming-trap-read-this-before-touching-voice-code) — this is *not* the new `VoiceApi`. |
| `VoiceDeliveryReceiptRulesApi` | → | **`VoiceApi`** | ⚠️ See [§12](#12-the-voice-naming-trap-read-this-before-touching-voice-code) — the new `VoiceApi` only has delivery-receipt-rule methods. |

`AlphaTagsApi`, `DefaultSendersApi`, `OwnNumbersApi`, and `UrlShorteningApi` in v2 have **no legacy predecessor at all** — see [§14](#14-brand-new-resources-and-methods-in-v2).

### Email: five legacy classes → `EmailApi`

| Legacy | v2 (`EmailApi`) |
|---|---|
| `TransactionalEmailApi.emailSendPost` | `sendEmail` |
| `TransactionalEmailApi.emailHistoryGet` | `viewEmailHistory` |
| `TransactionalEmailApi.emailHistoryExportGet` | `exportEmailHistory` |
| `TransactionalEmailApi.emailPricePost` | `calculateEmailPrice` |
| `EmailMarketingApi.emailCampaignPost` | `sendEmailCampaign` |
| `EmailMarketingApi.emailCampaignsGet` | `viewAllEmailCampaigns` |
| `EmailMarketingApi.emailCampaignGet` | `viewEmailCampaign` |
| `EmailMarketingApi.emailCampaignPut` | `updateEmailCampaign` |
| `EmailMarketingApi.cancelEmailCampaignPut` | `cancelEmailCampaign` |
| `EmailMarketingApi.emailCampaignPricePost` | `calculateEmailCampaignPrice` |
| `EmailMarketingApi.emailCampaignHistoryGet` | `viewEmailCampaignHistory` |
| `EmailMarketingApi.emailCampaignHistoryExportGet` | `exportEmailCampaignHistory` |
| `EmailMarketingApi.allowedEmailAddressGet` | `viewAllowedEmailAddresses` |
| `EmailMarketingApi.allowedEmailAddressPost` | `createAllowedEmailAddress` |
| `EmailMarketingApi.specificAllowedEmailAddressGet` | `viewAllowedEmailAddress` |
| `EmailMarketingApi.specificAllowedEmailAddressDelete` | `deleteAllowedEmailAddress` |
| `EmailMarketingApi.verifyAllowedEmailAddressGet` | `verifyAllowedEmailAddress` |
| `EmailMarketingApi.sendVerificationTokenGet` | `sendEmailVerificationToken` |
| `UserEmailTemplatesApi.emailTemplatesGet` | `viewEmailTemplates` |
| `UserEmailTemplatesApi.emailTemplateGet` | `viewEmailTemplate` |
| `UserEmailTemplatesApi.emailTemplatePost` | `createEmailTemplate` |
| `UserEmailTemplatesApi.emailTemplatePut` | `updateEmailTemplate` |
| `UserEmailTemplatesApi.emailTemplateDelete` | `deleteEmailTemplate` |
| `MasterEmailTemplatesApi.masterEmailTemplatesGet` | `viewMasterEmailTemplates` |
| `MasterEmailTemplatesApi.masterEmailTemplateGet` | `viewMasterEmailTemplate` |
| `MasterEmailTemplatesApi.masterEmailTemplateCategoriesGet` | `viewTemplateCategories` |
| `MasterEmailTemplatesApi.masterEmailTemplateCategoryGet` | `viewTemplateCategory` |
| `MasterEmailTemplatesApi.masterEmailTemplatesInCategoryGet` | `viewTemplatesInCategory` |
| `EmailDeliveryReceiptRulesApi.emailDeliveryReceiptAutomationsGet` | `viewEmailDeliveryReceiptRules` |
| `EmailDeliveryReceiptRulesApi.emailDeliveryReceiptAutomationGet` | `viewEmailDeliveryReceiptRule` |
| `EmailDeliveryReceiptRulesApi.emailDeliveryReceiptAutomationPost` | `createEmailDeliveryReceiptRule` |
| `EmailDeliveryReceiptRulesApi.emailDeliveryReceiptAutomationPut` | `updateEmailDeliveryReceiptRule` |
| `EmailDeliveryReceiptRulesApi.emailDeliveryReceiptAutomationDelete` | `deleteEmailDeliveryReceiptRule` |

> `EmailMarketingApi.emailCampaignPut` in the legacy SDK took an `EmailCampaign` domain model; v2's `updateEmailCampaign` takes a dedicated `UpdateEmailCampaignRequest`. Same story for every other method above — check the current per-method Javadoc for the exact request model name.

### SMS: `SmsApi` + `InboundSmsRulesApi` + `SmsDeliveryReceiptRulesApi` → `SmsApi`

| Legacy | v2 (`SmsApi`) |
|---|---|
| `SmsApi.smsSendPost` | `sendSms` |
| `SmsApi.smsHistoryGet` | `viewSmsHistory` |
| `SmsApi.smsHistoryExportGet` | `exportSmsHistory` |
| `SmsApi.smsPricePost` | `calculateSmsPrice` |
| `SmsApi.smsCancelAllPut` | `cancelAllSms` |
| `SmsApi.smsCancelByMessageIdPut` | `cancelSms` |
| `SmsApi.smsInboundGet` | `viewInboundSms` |
| `SmsApi.smsInboundPost` | `createTestInboundSms` |
| `SmsApi.smsInboundReadPut` | `markInboundSmsAsRead` |
| `SmsApi.smsInboundReadByMessageIdPut` | `markSpecificInboundSmsMessageAsRead` |
| `SmsApi.smsReceiptsGet` | `viewSmsReceipts` |
| `SmsApi.smsReceiptsByMessageIdGet` | `viewSpecificSmsReceipt` |
| `SmsApi.smsReceiptsPost` | `createTestSmsReceipt` |
| `SmsApi.smsReceiptsReadPut` | `markSmsReceiptAsRead` |
| `SmsApi.smsTemplatesGet` | `viewSmsTemplates` |
| `SmsApi.smsTemplatesPost` | `createSmsTemplate` |
| `SmsApi.smsTemplatesByTemplateIdPut` | `updateSmsTemplate` |
| `SmsApi.smsTemplatesByTemplateIdDelete` | `deleteSmsTemplate` |
| `InboundSmsRulesApi.smsInboundAutomationsGet` | `viewSmsInboundAutomations` |
| `InboundSmsRulesApi.smsInboundAutomationGet` | `viewSmsInboundAutomation` |
| `InboundSmsRulesApi.smsInboundAutomationPost` | `createSmsInboundAutomation` |
| `InboundSmsRulesApi.smsInboundAutomationPut` | `updateSmsInboundAutomation` |
| `InboundSmsRulesApi.smsInboundAutomationDelete` | `deleteSmsInboundAutomation` |
| `SmsDeliveryReceiptRulesApi.smsDeliveryReceiptAutomationsGet` | `viewSmsDeliveryReceiptRules` |
| `SmsDeliveryReceiptRulesApi.smsDeliveryReceiptAutomationGet` | `viewSmsDeliveryReceiptRule` |
| `SmsDeliveryReceiptRulesApi.smsDeliveryReceiptAutomationPost` | `createSmsDeliveryReceiptRule` |
| `SmsDeliveryReceiptRulesApi.smsDeliveryReceiptAutomationPut` | `updateSmsDeliveryReceiptRule` |
| `SmsDeliveryReceiptRulesApi.smsDeliveryReceiptAutomationDelete` | `deleteSmsDeliveryReceiptRule` |
| — | `viewASpecificSmsTemplate` *(new — see [§14](#14-brand-new-resources-and-methods-in-v2))* |
| — | `viewASpecificInboundSmsMessage` *(new — see [§14](#14-brand-new-resources-and-methods-in-v2))* |

### Contacts & lists: `ContactApi` + `ContactListApi` + `SearchApi` → `ContactsApi` + `ListsApi`

| Legacy | v2 |
|---|---|
| `ContactApi.listsContactsByListIdAndContactIdGet` | `ContactsApi.getSpecificContact` |
| `ContactApi.listsContactsByListIdAndContactIdPut` | `ContactsApi.updateContact` |
| `ContactApi.listsContactsByListIdAndContactIdDelete` | `ContactsApi.deleteContact` |
| `ContactApi.listsContactsByListIdPost` | `ListsApi.createNewContact` |
| `ContactApi.listsContactsByListIdGet` | `ListsApi.viewListContacts` |
| `ContactApi.listsCopyContactPut` | `ListsApi.copyContactToList` |
| `ContactApi.listsTransferContactPut` | `ListsApi.transferContactToList` |
| `ContactApi.listsRemoveOptedOutContactsByListIdAndOptOutListIdPut` | `ListsApi.removeOptedOutContacts` |
| `ContactListApi.listsGet` | `ListsApi.viewLists` |
| `ContactListApi.listsPost` | `ListsApi.createList` |
| `ContactListApi.listsByListIdGet` | `ListsApi.viewSpecificList` |
| `ContactListApi.listsByListIdPut` | `ListsApi.updateList` |
| `ContactListApi.listsByListIdDelete` | `ListsApi.deleteList` |
| `ContactListApi.listsImportByListIdPost` | `ListsApi.importContacts` |
| `ContactListApi.listsRemoveDuplicatesByListIdPut` | `ListsApi.removeDuplicateContacts` |
| `SearchApi.searchContactsListsGet` | `ListsApi.viewContactLists` |

> **`listId` changed type from `Integer` to `String`** on every one of these methods and on the corresponding model fields (e.g. `SmsMessage.listId` → `SendSmsRequestMessagesInner.listId`). This fails to compile if you pass an `int`/`Integer` literal where a `String` is now expected — a clear, compiler-enforced signal, not a silent runtime bug.
>
> **`ListsApi.updateList` reuses `CreateListRequest`** rather than a dedicated `UpdateListRequest` — don't assume every v2 method gets a same-named `*Request` model.
>
> **`ListsApi.viewContactLists` returns `void`** in the generated client (it has a `viewContactListsWithHttpInfo` returning `ApiResponse<Void>`) — unlike almost every other v2 method, there is no typed response body to read; consume the HTTP response directly if you need the payload.

### Account & billing

| Legacy | v2 |
|---|---|
| `AccountApi.accountGet` | `ManagementApi.viewAccountDetails` |
| `AccountApi.accountUseageBySubaccountGet` | `ManagementApi.viewAccountUsage` |
| `AccountApi.forgotPasswordPut` | `VerificationApi.forgotPassword` |
| `AccountApi.forgotUsernamePut` | `VerificationApi.forgotUsername` |
| `AccountRechargeApi.rechargeCreditCardGet` | `TransactionsApi.currentPaymentInfo` |
| `AccountRechargeApi.rechargeCreditCardPut` | `TransactionsApi.updatePaymentInfo` |
| `AccountRechargeApi.rechargePackagesGet` | `TransactionsApi.viewRechargePackages` |
| `AccountRechargeApi.rechargePurchaseByPackageIdPut` | `TransactionsApi.purchaseRechargePackage` |
| `AccountRechargeApi.rechargeTransactionsGet` | `TransactionsApi.viewAllTransactions` |
| `AccountRechargeApi.rechargeTransactionsByTransactionIdGet` | `TransactionsApi.viewSpecificTransaction` |
| `ResellerAccountApi.resellerAccountsGet` | `ResellerApi.viewClientAccounts` |
| `ResellerAccountApi.resellerAccountsPost` | `ResellerApi.createResellerAccount` |
| `ResellerAccountApi.resellerAccountsByClientUserIdGet` | `ResellerApi.viewSpecificClientAccount` |
| `ResellerAccountApi.resellerAccountsByClientUserIdPut` | `ResellerApi.updateClientAccount` |
| `TransferCreditApi.resellerTransferCreditPut` | `ResellerApi.resellerTransferCredit` |
| `SubaccountApi.subaccountsGet` | `SubaccountsApi.viewSubaccounts` |
| `SubaccountApi.subaccountsPost` | `SubaccountsApi.createSubaccount` |
| `SubaccountApi.subaccountsBySubaccountIdGet` | `SubaccountsApi.viewSpecificSubaccount` |
| `SubaccountApi.subaccountsBySubaccountIdPut` | `SubaccountsApi.updateSubaccount` |
| `SubaccountApi.subaccountsBySubaccountIdDelete` | `SubaccountsApi.deleteSubaccount` |
| `SubaccountApi.subaccountsRegenApiKeyBySubaccountIdPut` | `SubaccountsApi.generateNewApiKey` |
| `ReferralAccountApi.referralAccountsGet` | `ReferralsApi.viewReferralAccounts` |

### Numbers, addresses, uploads, international, delivery issues

| Legacy | v2 |
|---|---|
| `NumberApi.numbersGet` | `NumbersApi.viewYourNumbers` |
| `NumberApi.numbersSearchByCountryGet` | `NumbersApi.viewAvailableNumbers` |
| `NumberApi.numbersBuyByDedicatedNumberPost` | `NumbersApi.purchaseDedicatedNumber` |
| `PostReturnAddressApi.postReturnAddressesGet` | `AddressesApi.viewYourReturnAddresses` |
| `PostReturnAddressApi.postReturnAddressesPost` | `AddressesApi.createReturnAddress` |
| `PostReturnAddressApi.postReturnAddressesByReturnAddressIdGet` | `AddressesApi.viewSpecificReturnAddress` |
| `PostReturnAddressApi.postReturnAddressesByReturnAddressIdPut` | `AddressesApi.updateReturnAddress` |
| `PostReturnAddressApi.postReturnAddressesByReturnAddressIdDelete` | `AddressesApi.deleteReturnAddress` |
| `UploadApi.uploadsPost` | `UploadsApi.uploadAMediaFile` |
| `CountriesApi.countriesGet` | `InternationalMessagingApi.viewCountries` |
| `TimezonesApi.timezonesGet` | `InternationalMessagingApi.timezones` |
| `GlobalSendingApi.listCountriesGet` | `InternationalMessagingApi.listCountries` |
| `GlobalSendingApi.userCountriesGet` | `InternationalMessagingApi.getCountriesForGlobalSending` |
| `GlobalSendingApi.userCountriesPost` | `InternationalMessagingApi.selectCountriesForGlobalSending` |
| `GlobalSendingApi.userCountriesAgreePost` | `InternationalMessagingApi.agreeToRulesAndRegulation` |
| `DeliveryIssuesApi.deliveryIssuesGet` | `MessageDeliveryApi.getAllDeliveryIssues` |
| `DeliveryIssuesApi.deliveryIssuesPost` | `MessageDeliveryApi.createDeliveryIssue` |

> Note the `InternationalMessagingApi` method names above don't quite mirror the legacy `GlobalSendingApi`/`CountriesApi` names one-to-one — cross-check with your IDE's autocomplete on `InternationalMessagingApi` if a name below looks off, since ClickSend's build tooling regenerates operationIds and they can shift slightly release to release.

### MMS, campaigns, voice, statistics

| Legacy | v2 |
|---|---|
| `MmsApi.mmsSendPost` | `MmsApi.sendMms` |
| `MmsApi.mmsHistoryGet` | `MmsApi.viewMmsHistory` |
| `MmsApi.mmsHistoryExportGet` | `MmsApi.exportMmsHistory` |
| `MmsApi.mmsPricePost` | `MmsApi.calculateMmsPrice` |
| `MmsCampaignApi.mmsCampaignsSendPost` | `MmsCampaignsApi.sendMmsCampaign` |
| `MmsCampaignApi.mmsCampaignsGet` | `MmsCampaignsApi.viewAllMmsCampaigns` |
| `MmsCampaignApi.mmsCampaignByMmsCampaignIdGet` | `MmsCampaignsApi.viewMmsCampaign` |
| `MmsCampaignApi.mmsCampaignsByMmsCampaignIdPut` | `MmsCampaignsApi.updateMmsCampaign` |
| `MmsCampaignApi.mmsCampaignsCancelByMmsCampaignIdPut` | `MmsCampaignsApi.cancelMmsCampaign` |
| `MmsCampaignApi.mmsCampaignsPricePost` | `MmsCampaignsApi.calculateMmsCampaignPrice` |
| `SmsCampaignApi.smsCampaignsSendPost` | `SmsCampaignsApi.sendSmsCampaign` |
| `SmsCampaignApi.smsCampaignsGet` | `SmsCampaignsApi.viewSmsCampaigns` |
| `SmsCampaignApi.smsCampaignBySmsCampaignIdGet` | `SmsCampaignsApi.viewSpecificSmsCampaign` |
| `SmsCampaignApi.smsCampaignsBySmsCampaignIdPut` | `SmsCampaignsApi.updateSmsCampaign` |
| `SmsCampaignApi.smsCampaignsCancelBySmsCampaignIdPut` | `SmsCampaignsApi.cancelSmsCampaign` |
| `SmsCampaignApi.smsCampaignsPricePost` | `SmsCampaignsApi.calculateSmsCampaignPrice` |
| `VoiceApi.voiceSendPost` | `VoiceMessagingApi.sendVoiceMessage` ⚠️ [§12](#12-the-voice-naming-trap-read-this-before-touching-voice-code) |
| `VoiceApi.voiceHistoryGet` | `VoiceMessagingApi.getVoiceHistory` |
| `VoiceApi.voiceHistoryExportGet` | `VoiceMessagingApi.exportVoiceHistory` |
| `VoiceApi.voicePricePost` | `VoiceMessagingApi.calculateVoicePrice` |
| `VoiceApi.voiceLangGet` | `VoiceMessagingApi.viewVoiceLanguages` |
| `VoiceApi.voiceCancelAllPut` | `VoiceMessagingApi.cancelAllVoiceMessages` |
| `VoiceApi.voiceCancelByMessageIdPut` | `VoiceMessagingApi.cancelVoiceMessage` |
| `VoiceApi.voiceReceiptsGet` | `VoiceMessagingApi.viewVoiceReceipts` |
| `VoiceDeliveryReceiptRulesApi.voiceDeliveryReceiptAutomationsGet` | `VoiceApi.viewVoiceDeliveryReceiptRules` ⚠️ [§12](#12-the-voice-naming-trap-read-this-before-touching-voice-code) |
| `VoiceDeliveryReceiptRulesApi.voiceDeliveryReceiptAutomationGet` | `VoiceApi.viewVoiceDeliveryReceiptRule` |
| `VoiceDeliveryReceiptRulesApi.voiceDeliveryReceiptAutomationPost` | `VoiceApi.createVoiceDeliveryReceiptRule` |
| `VoiceDeliveryReceiptRulesApi.voiceDeliveryReceiptAutomationPut` | `VoiceApi.updateVoiceDeliveryReceiptRule` |
| `VoiceDeliveryReceiptRulesApi.voiceDeliveryReceiptAutomationDelete` | `VoiceApi.deleteVoiceDeliveryReceiptRule` |
| `StatisticsApi.statisticsSmsGet` | `StatisticsApi.viewSmsStatistics` |
| `StatisticsApi.statisticsVoiceGet` | `StatisticsApi.viewVoiceStatistics` |

> `VoiceApi.createVoiceDeliveryReceiptRule`/`updateVoiceDeliveryReceiptRule` take a `CreateSmsDeliveryReceiptRuleRequest` as their request model, not a "voice"-named request class — the generator reused the SMS delivery-receipt-rule request shape since the schema is identical. This is intentional, not a documentation error; double-check against the actual method signature rather than guessing a `CreateVoiceDeliveryReceiptRuleRequest` class exists.

### Email-to-SMS: `EmailToSmsApi` → `EmailToSmsApi`

| Legacy | v2 |
|---|---|
| `smsEmailSmsGet` | `viewAllowedEmails` |
| `smsEmailSmsPost` | `addAllowedEmail` |
| `smsEmailSmsStrippedStringPost` | `createStrippedStringRule` |
| `smsEmailSmsStrippedStringGet` | `viewStrippedStringRule` |
| `smsEmailSmsStrippedStringsGet` | `viewStrippedStringRules` |
| `smsEmailSmsStrippedStringPut` | `updateStrippedStringRule` |
| `smsEmailSmsStrippedStringDelete` | `deleteStrippedStringRule` |

## 11. Side-by-side examples for common operations

### Send an SMS

```java
// Legacy
import ClickSend.Model.SmsMessage;
import ClickSend.Model.SmsMessageCollection;
import ClickSend.Api.SmsApi;
import ClickSend.ApiException;

SmsMessage msg = new SmsMessage();
msg.setTo("+61411111111");
msg.setBody("Hello from ClickSend!");
msg.setSource("php");

SmsMessageCollection collection = new SmsMessageCollection();
collection.setMessages(Arrays.asList(msg));

try {
    String result = apiInstance.smsSendPost(collection); // raw JSON string
    System.out.println(result);
} catch (ApiException e) {
    System.err.println(e.getCode() + " " + e.getResponseBody());
}

// v2
import ClickSend.Model.SendSmsRequest;
import ClickSend.Model.SendSmsRequestMessagesInner;
import ClickSend.Model.SendSms;
import ClickSend.Api.SmsApi;
import ClickSend.ApiException;

SendSmsRequestMessagesInner message = new SendSmsRequestMessagesInner()
    .to("+61411111111")
    .body("Hello from ClickSend!")
    .source("sdk");

SendSmsRequest request = new SendSmsRequest().addMessagesItem(message);

try {
    SendSms result = apiInstance.sendSms(null, request); // typed SendSms instance
    System.out.println(result.getData());
} catch (ApiException e) {
    System.err.println(e.getCode() + " " + e.getResponseBody());
}
```

### View SMS history

```java
// Legacy — positional params, no order_by
apiInstance.smsHistoryGet(q, dateFrom, dateTo, page, limit);

// v2 — dedicated setter-style builder; contentType leads, plus a new orderBy
apiInstance.viewSmsHistory(null, q, "date:desc", dateFrom, dateTo, page, limit);
```

> Always check the current method signature — parameter sets changed (this one gained `orderBy`); consult `docs/SmsApi.md#viewSmsHistory` in this repo for the authoritative order.

### Send an MMS / Email / Voice message

Same pattern on every channel — build a `Send<Channel>Request`, call `send<Channel>(...)`:

| Channel | Legacy call | v2 call |
|---|---|---|
| MMS | `mmsApi.mmsSendPost(mmsMessageCollection)` | `mmsApi.sendMms(null, sendMmsRequest)` |
| Email | `emailApi.emailSendPost(email)` | `emailApi.sendEmail(null, sendEmailRequest)` |
| Voice | `voiceApi.voiceSendPost(voiceCollection)` (legacy `VoiceApi`) | `voiceMessagingApi.sendVoiceMessage(null, sendVoiceMessageRequest)` (⚠️ new `VoiceMessagingApi`, see [§12](#12-the-voice-naming-trap-read-this-before-touching-voice-code)) |

> **Fax, Post Letters, and Post Postcards are not part of the v2 SDK** — there is no `sendFax`/`sendPostLetter`/`sendPostcard` equivalent. See [§13](#13-endpointsmethods-removed-in-v2).

### Create a contact in a list

```java
// Legacy — list_id is Integer, contact model second
apiInstance.listsContactsByListIdPost(listId, contact); // listId: Integer

// v2 — list_id is now a String and comes first; payload is a dedicated request model
apiInstance.createNewContact(String.valueOf(listId), null, createNewContactRequest);
```

### Create a subaccount

```java
// Legacy
apiInstance.subaccountsPost(subaccount);

// v2
apiInstance.createSubaccount(null, createSubaccountRequest);
```

## 12. The Voice naming trap (read this before touching voice code)

This is the single most confusing rename in the whole migration, and a naive search-and-replace of `VoiceApi` will silently point your code at the wrong class — and it's identical across every ClickSend SDK, Java included:

- Legacy **`VoiceApi`** (send a voice message, view/export history, calculate price, list voice languages, cancel, view receipts) → renamed to new **`VoiceMessagingApi`**.
- Legacy **`VoiceDeliveryReceiptRulesApi`** (create/update/delete/view delivery-receipt rules) → renamed to new **`VoiceApi`**.

The new `VoiceApi` has **nothing to do with sending voice calls** — it is purely the old delivery-receipt-rules class under a new name. To migrate voice-sending code, import `VoiceMessagingApi`:

```java
// Wrong — this compiles, but VoiceApi in v2 only has delivery-receipt-rule methods
import ClickSend.Api.VoiceApi;
VoiceApi voiceApi = new VoiceApi(defaultClient);
voiceApi.sendVoiceMessage(...);          // compile error — no such method on the new VoiceApi

// Correct
import ClickSend.Api.VoiceMessagingApi;
VoiceMessagingApi voiceMessagingApi = new VoiceMessagingApi(defaultClient);
voiceMessagingApi.sendVoiceMessage(null, sendVoiceMessageRequest);
```

Because Java is statically typed, calling `sendVoiceMessage` on the wrong `VoiceApi` is a **compile-time** error, not a runtime `AttributeError` as in dynamically-typed SDKs — but the class name itself is what will mislead you (and your IDE's autocomplete on `VoiceApi` will offer only delivery-receipt-rule methods, which is your first clue something is off).

## 13. Endpoints/methods removed in v2

### Entire products dropped

The **Fax**, **Post Letters**, and **Post Postcards** products have **no presence at all** in the v2 SDK — no API class, no models. If your integration sends faxes, letters, or postcards, there is currently no v2 SDK path for it; call the REST API directly or stay on the legacy SDK for those channels.

| Legacy class(es) | Covered (legacy) | v2 |
|---|---|---|
| `FaxApi`, `FaxDeliveryReceiptRulesApi`, `InboundFaxRulesApi` | send fax, fax history/price, fax receipts (get/create/read), fax delivery-receipt rules, inbound fax rules | _none_ |
| `PostLetterApi` | send letter, letter history/export, letter price | _none_ |
| `PostPostcardApi` | send postcard, postcard history/export, postcard price | _none_ |
| `DetectAddressApi` | address detection/parsing (`detectAddressPost`) | _none_ |

### Individual methods dropped (class otherwise survived)

The following legacy operations have **no equivalent anywhere in the v2 SDK**. If your integration depends on any of these, check the current ClickSend API reference before upgrading — the underlying endpoint may have been retired, moved, or simply not covered by the new spec at build time:

- `AccountApi.accountPost` — create a new account
- `AccountApi.accountVerifySendPut` — send account activation token
- `AccountApi.accountVerifyVerifyByActivationTokenPut` — verify a new account
- `AccountApi.forgotPasswordVerifyPut` — verify a forgotten-password token
- `MmsApi.mmsReceiptsGet` — view MMS delivery receipts
- `MmsApi.mmsReceiptsReadPut` — mark MMS receipts as read
- `VoiceApi.voiceReceiptsPost` (legacy class) — create a test voice receipt
- `VoiceApi.voiceReceiptsReadPut` (legacy class) — mark voice receipts as read

Self-service account creation/verification (the first four rows) appears to have been removed from the SDK surface entirely — account provisioning is presumably dashboard/support-only now. For MMS/Voice, "add"/"mark as read" of delivery receipts is gone, but **reading** receipts remains available (`VoiceMessagingApi.viewVoiceReceipts`) — only MMS lost receipt visibility entirely. Delivery-receipt **automation rules** (webhooks) for the surviving channels are unaffected — those are the separate `automations/*/receipts` endpoints covered in [§10](#10-class-by-class-mapping-all-37-legacy-classes).

Counting it out: legacy has **188 methods** across 37 classes; **34** have no v2 equivalent (26 belong to the three dropped products, 8 are the individual methods above); the remaining **154** all have a direct v2 equivalent, plus **20** genuinely new v2-only methods (see [§14](#14-brand-new-resources-and-methods-in-v2)) bring the v2 total to **174** methods across 26 classes.

## 14. Brand-new resources and methods in v2

No legacy counterpart at all — nothing to migrate, but worth knowing they exist:

- **`AlphaTagsApi`** — `listAlphaTags`, `getAlphaTag`, `requestAlphaTag`, `deleteAlphaTag`
- **`DefaultSendersApi`** — `getDefaultSendersList`, `getDefaultSenderDetails`, `createDefaultSender`, `updateDefaultSender`, `deleteDefaultSender`, `listCompliantSenderTypes`
- **`OwnNumbersApi`** (Bring Your Own Number) — `listOwnNumbers`, `getOwnNumberDetail`, `updateOwnNumber`, `deleteOwnNumber`, `requestOwnNumberVerificationOtp`, `verifyOwnNumberOtp`
- **`UrlShorteningApi`** — `shortUrlGetStatistics`, `shortUrlGetTracking`
- **`NumbersApi.registerNumbers`** — number registration (alongside the renamed `NumberApi` methods)
- **`SmsApi.viewASpecificInboundSmsMessage`** and **`SmsApi.viewASpecificSmsTemplate`** — fetch a single inbound message / template by ID (legacy only exposed the list endpoints)

## 15. Step-by-step migration checklist

1. **Update your Maven/Gradle coordinates**: `groupId` stays `com.clicksend`; change `artifactId` from `clicksend-java-client` to `clicksend-java` and bump the version to `6.0.2` ([§2](#2-installation--imports)). Remove the old dependency rather than just editing its version — the `artifactId` changed.
2. **Confirm your runtime JDK.** The v2 SDK only needs Java 1.8+; don't assume you need a newer JDK than before — the legacy SDK's own `pom.xml` actually targets Java 11 despite its README claiming 1.7+ ([§2](#2-installation--imports)).
3. **Update the authentication scheme key** from `"BasicAuth"` to `"basicAuth"` in every `getAuthentication(...)` call ([§3](#3-authentication--client-setup)).
4. **Rename every API class per the mapping table** ([§10](#10-class-by-class-mapping-all-37-legacy-classes)) — most are a straightforward rename (`ContactListApi` → `ListsApi`), but a few legacy classes split across two new classes (`ContactApi` → `ContactsApi` + `ListsApi`, `AccountApi` → `ManagementApi` + `VerificationApi`). **Pay special attention to `VoiceApi` → `VoiceMessagingApi`** ([§12](#12-the-voice-naming-trap-read-this-before-touching-voice-code)).
5. **Rebuild every request payload** with the matching `*Request` model instead of the old domain model, and thread the new leading `contentType` parameter (pass `null` unless you need something other than `application/json`) ([§6](#6-request-payloads-request-models-replace-reusable-domain-models)). Watch for type changes on carried-over fields (`listId` `Integer` → `String` is the most common).
6. **Rename every method call** using the [§10](#10-class-by-class-mapping-all-37-legacy-classes)/[§11](#11-side-by-side-examples-for-common-operations) tables or your IDE's autocomplete on the new `*Api` class.
7. **Update response handling** — the return value is now a typed model, not a raw `String`. Delete manual Gson/Jackson parsing and switch to direct getters. Use `*WithHttpInfo` when you need the status code or headers ([§7](#7-response-payloads-are-now-properly-typed)).
8. **`ApiException` catch blocks need no changes** beyond confirming the import still resolves (same package, same class) — optionally start using the new `getMessage()` ([§8](#8-error-handling-changes)).
9. **If you use `*Async(...)`/`ApiCallback`**, update the callback's generic type parameter to the new typed response model and add the leading `contentType` argument — the async mechanism itself is unchanged and does not need to be re-architected ([§9](#9-apicallback-async-calls-are-preserved--only-the-type-parameter-changes)).
10. **Check for removed endpoints and dropped products** ([§13](#13-endpointsmethods-removed-in-v2)) — the entire Fax, Post Letters, and Post Postcards products are gone — and confirm a replacement exists in the current API before shipping.
11. **Re-run your test suite.** If you have unit tests that mock SDK responses as raw JSON strings, they'll need to be rewritten to construct/mock the new typed model objects instead.
12. **Build and smoke-test against a sandbox/test ClickSend account** before deploying — Java's compiler will catch renamed methods and type mismatches, but it cannot catch field-name/shape drift inside a request you build from untrusted input or catch the exact runtime JSON shape v2 returns for endpoints you haven't yet exercised.
