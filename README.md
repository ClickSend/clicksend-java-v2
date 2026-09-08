# ClickSend Java SDK

[![Maven Central](https://img.shields.io/maven-central/v/com.clicksend/clicksend-java.svg)](https://central.sonatype.com/artifact/com.clicksend/clicksend-java)
[![License: MIT](https://img.shields.io/badge/license-MIT-blue.svg)](https://opensource.org/licenses/MIT)
[![API: v3](https://img.shields.io/badge/ClickSend%20API-v3-brightgreen.svg)](https://developers.clicksend.com/docs/rest/v3/)

Official Java client for the [ClickSend API](https://developers.clicksend.com/) — send SMS, MMS, voice and email messages, run SMS and MMS campaigns, manage numbers, contacts and subaccounts, and pull delivery receipts and reporting through a single authenticated HTTPS client.

This library is generated from ClickSend's official OpenAPI v3 specification and is maintained by ClickSend. It covers every endpoint of the [ClickSend REST API](https://developers.clicksend.com/docs/rest/v3/).

- 📚 **API reference:** https://developers.clicksend.com/docs/rest/v3/
- 🔑 **Dashboard & API credentials:** https://dashboard.clicksend.com
- 🗂 **Source & issues:** https://github.com/ClickSend/clicksend-java-v2
- 💬 **Support:** https://help.clicksend.com

## Features

- **Messaging** — SMS, MMS, voice / text-to-speech, transactional email, email-to-SMS
- **Campaigns** — SMS and MMS campaigns
- **Numbers & sender IDs** — dedicated numbers, own numbers, alpha tags, default senders
- **Contacts** — contact lists, contacts and the address book
- **Account & billing** — account details, transactions, subaccounts, referrals, reseller accounts
- **Delivery & reporting** — delivery receipts, inbound messages, statistics
- **Extras** — URL shortening, file uploads, number verification, international messaging
- **Typed models** for every request and response
- **HTTP Basic auth** with your ClickSend username and API key
- **Identifiable traffic** — requests are sent with a `ClickSend-SDK/<version>/java` `User-Agent` by default
- MIT licensed

## Requirements

- Java 1.8 or newer
- Maven (3.8.3+) or Gradle (7.2+)

## Installation

### Maven

```xml
<dependency>
  <groupId>com.clicksend</groupId>
  <artifactId>clicksend-java</artifactId>
  <version>6.0.1</version>
</dependency>
```

### Gradle

```groovy
implementation "com.clicksend:clicksend-java:6.0.1"
```

## Authentication

Every API class authenticates with HTTP Basic auth using your ClickSend **username** and **API key**, both available from the [ClickSend Dashboard](https://dashboard.clicksend.com/#/account/subaccount). Supply them through environment variables rather than hard-coding them:

```sh
export CLICKSEND_USERNAME="your-username"
export CLICKSEND_API_KEY="your-api-key"
```

## Quickstart

```java
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.Api.SmsApi;
import ClickSend.Model.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();

        HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
        basicAuth.setUsername(System.getenv("CLICKSEND_USERNAME"));
        basicAuth.setPassword(System.getenv("CLICKSEND_API_KEY"));

        SmsApi apiInstance = new SmsApi(defaultClient);
        SendSmsRequest sendSmsRequest = new SendSmsRequest()
            .addMessagesItem(new SendSmsRequestMessagesInner()
                .body("Hello from ClickSend!")
                .to("+61411111111")
                .source("sdk"));

        try {
            // The first argument is the optional `contentType` header — pass `null` to use the default.
            // The request body is the second argument.
            SendSms result = apiInstance.sendSms(null, sendSmsRequest);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling SmsApi#sendSms: " + e.getMessage());
        }
    }
}
```

## More Examples

### View account details

```java
import ClickSend.Api.ManagementApi;
import ClickSend.Model.ViewAccountDetails;

ManagementApi managementApi = new ManagementApi(defaultClient);

try {
    ViewAccountDetails account = managementApi.viewAccountDetails(null);
    System.out.println(account);
} catch (ApiException e) {
    System.err.println("Exception when calling ManagementApi#viewAccountDetails: " + e.getMessage());
}
```

### Send an MMS

```java
import ClickSend.Api.MmsApi;
import ClickSend.Model.SendMms;
import ClickSend.Model.SendMmsRequest;
import ClickSend.Model.SendMmsRequestMessagesInner;

MmsApi mmsApi = new MmsApi(defaultClient);
SendMmsRequest sendMmsRequest = new SendMmsRequest()
    .mediaFile("https://clicksend.com/logo.png")
    .addMessagesItem(new SendMmsRequestMessagesInner()
        .to("+61411111111")
        .from("sdk")
        .subject("Hello")
        .body("Hello from ClickSend!")
        .source("sdk"));

try {
    // As with sendSms, the first argument is the optional `contentType` header — pass `null`.
    SendMms result = mmsApi.sendMms(null, sendMmsRequest);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling MmsApi#sendMms: " + e.getMessage());
}
```

## Configuration

```java
ApiClient defaultClient = Configuration.getDefaultApiClient();

// Override the API base URL (default: https://rest.clicksend.com).
defaultClient.setBasePath("https://rest.clicksend.com");

// Connect / read timeouts, in milliseconds.
defaultClient.setConnectTimeout(10_000);
defaultClient.setReadTimeout(30_000);
```

## Error Handling

Non-2xx responses throw `ClickSend.ApiException`:

```java
try {
    SendSms result = apiInstance.sendSms(null, sendSmsRequest);
} catch (ApiException e) {
    e.getCode();            // HTTP status code
    e.getResponseBody();    // raw error payload from the API
    e.getResponseHeaders(); // response headers
}
```

## Documentation

- Full REST API reference: https://developers.clicksend.com/docs/rest/v3/
- Per-endpoint SDK docs: the [`docs/`](docs) directory in this repository
- Source code: https://github.com/ClickSend/clicksend-java-v2

## Versioning

This package follows [semantic versioning](https://semver.org/). Breaking changes are released as major versions.

## Support

- Help Centre: https://help.clicksend.com
- Contact support: https://clicksend.com/contact
- SDK bugs and feature requests: https://github.com/ClickSend/clicksend-java-v2/issues

## License

Released under the [MIT License](https://opensource.org/licenses/MIT).

---

**Keywords:** clicksend, sms, sms api, send sms, bulk sms, text message, texting, mms, mms api, voice, voice call, text to speech, tts, ivr, email to sms, sms campaign, mms campaign, url shortening, number verification, messaging, notifications, otp, 2fa, two factor authentication, transactional sms, marketing sms, appointment reminders, alerts, java, jvm, rest api, clicksend sdk
