# ClickSend Java SDK

Official Java client for the [ClickSend API](https://developers.clicksend.com/) — send and manage SMS, MMS, email, voice, fax, letters, postcards, and more.

## Requirements

- Java 1.8+
- Maven (3.8.3+) / Gradle (7.2+)

## Installation

### Maven

```xml
<dependency>
  <groupId>com.clicksend</groupId>
  <artifactId>clicksend-java</artifactId>
  <version>1.0.0</version>
</dependency>
```

### Gradle

```groovy
implementation "com.clicksend:clicksend-java:1.0.0"
```

## Getting Started

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
        SmsMessageCollection smsMessageCollection = new SmsMessageCollection();

        try {
            SmsMessageResponse result = apiInstance.smsSendPost(smsMessageCollection);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling SmsApi#smsSendPost: " + e.getMessage());
        }
    }
}
```

## Authentication

The API uses HTTP Basic authentication — your ClickSend **username** and **API key** (available from the [ClickSend Dashboard](https://dashboard.clicksend.com/#/account/subaccount)).

## Documentation

Full API reference: https://developers.clicksend.com/docs/rest/v3/

## Support

Need help? Contact [ClickSend Support](https://clicksend.com/contact) or visit the [Help Centre](https://help.clicksend.com/).