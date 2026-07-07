# SmsOtherApi

All URIs are relative to *https://rest.clicksend.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**calculateSmsPrice**](SmsOtherApi.md#calculateSmsPrice) | **POST** /v3/sms/price | Calculate SMS Price |
| [**cancelAllSms**](SmsOtherApi.md#cancelAllSms) | **PUT** /v3/sms/cancel-all | Cancel All SMS |
| [**cancelSms**](SmsOtherApi.md#cancelSms) | **PUT** /v3/sms/{message_id}/cancel | Cancel SMS |
| [**createSmsDeliveryReceiptRule**](SmsOtherApi.md#createSmsDeliveryReceiptRule) | **POST** /v3/automations/sms/receipts | Create SMS Delivery Receipt Rule |
| [**createSmsInboundAutomation**](SmsOtherApi.md#createSmsInboundAutomation) | **POST** /v3/automations/sms/inbound | Create SMS Inbound Automation |
| [**createSmsTemplate**](SmsOtherApi.md#createSmsTemplate) | **POST** /v3/sms/templates | Create SMS Template |
| [**createTestInboundSms**](SmsOtherApi.md#createTestInboundSms) | **POST** /v3/sms/inbound | Create Test Inbound SMS |
| [**createTestSmsReceipt**](SmsOtherApi.md#createTestSmsReceipt) | **POST** /v3/sms/receipts | Create Test SMS Receipt |
| [**deleteSmsDeliveryReceiptRule**](SmsOtherApi.md#deleteSmsDeliveryReceiptRule) | **DELETE** /v3/automations/sms/receipts/{receipt_rule_id} | Delete SMS Delivery Receipt Rule |
| [**deleteSmsInboundAutomation**](SmsOtherApi.md#deleteSmsInboundAutomation) | **DELETE** /v3/automations/sms/inbound/{inbound_rule_id} | Delete SMS Inbound Automation |
| [**deleteSmsTemplate**](SmsOtherApi.md#deleteSmsTemplate) | **DELETE** /v3/sms/templates/{template_id} | Delete SMS Template |
| [**exportSmsHistory**](SmsOtherApi.md#exportSmsHistory) | **GET** /v3/sms/history/export | Export SMS History |
| [**markInboundSmsAsRead**](SmsOtherApi.md#markInboundSmsAsRead) | **PUT** /v3/sms/inbound-read | Mark Inbound SMS as Read |
| [**markSmsReceiptAsRead**](SmsOtherApi.md#markSmsReceiptAsRead) | **PUT** /v3/sms/receipts-read | Mark SMS Receipt As Read |
| [**markSpecificInboundSmsMessageAsRead**](SmsOtherApi.md#markSpecificInboundSmsMessageAsRead) | **PUT** /v3/sms/inbound-read/{message_id} | Mark Specific Inbound SMS Message As Read |
| [**sendSms**](SmsOtherApi.md#sendSms) | **POST** /v3/sms/send | Send SMS |
| [**updateSmsDeliveryReceiptRule**](SmsOtherApi.md#updateSmsDeliveryReceiptRule) | **PUT** /v3/automations/sms/receipts/{receipt_rule_id} | Update SMS Delivery Receipt Rule |
| [**updateSmsInboundAutomation**](SmsOtherApi.md#updateSmsInboundAutomation) | **PUT** /v3/automations/sms/inbound/{inbound_rule_id} | Update SMS Inbound Automation |
| [**updateSmsTemplate**](SmsOtherApi.md#updateSmsTemplate) | **PUT** /v3/sms/templates/{template_id} | Update SMS Template |
| [**viewASpecificInboundSmsMessage**](SmsOtherApi.md#viewASpecificInboundSmsMessage) | **GET** /v3/sms/inbound/{original_message_id} | View a specific inbound SMS message |
| [**viewASpecificSmsTemplate**](SmsOtherApi.md#viewASpecificSmsTemplate) | **GET** /v3/sms/templates/{template_id} | View a Specific SMS Template |
| [**viewInboundSms**](SmsOtherApi.md#viewInboundSms) | **GET** /v3/sms/inbound | View Inbound SMS |
| [**viewSmsDeliveryReceiptRule**](SmsOtherApi.md#viewSmsDeliveryReceiptRule) | **GET** /v3/automations/sms/receipts/{receipt_rule_id} | View SMS Delivery Receipt Rule |
| [**viewSmsDeliveryReceiptRules**](SmsOtherApi.md#viewSmsDeliveryReceiptRules) | **GET** /v3/automations/sms/receipts | View SMS Delivery Receipt Rules |
| [**viewSmsHistory**](SmsOtherApi.md#viewSmsHistory) | **GET** /v3/sms/history | View SMS History |
| [**viewSmsInboundAutomation**](SmsOtherApi.md#viewSmsInboundAutomation) | **GET** /v3/automations/sms/inbound/{inbound_rule_id} | View SMS Inbound Automation |
| [**viewSmsInboundAutomations**](SmsOtherApi.md#viewSmsInboundAutomations) | **GET** /v3/automations/sms/inbound | View SMS Inbound Automations |
| [**viewSmsReceipts**](SmsOtherApi.md#viewSmsReceipts) | **GET** /v3/sms/receipts | View SMS Receipts |
| [**viewSmsTemplates**](SmsOtherApi.md#viewSmsTemplates) | **GET** /v3/sms/templates | View SMS Templates |
| [**viewSpecificSmsReceipt**](SmsOtherApi.md#viewSpecificSmsReceipt) | **GET** /v3/sms/receipts/{message_id} | View Specific SMS Receipt |


<a id="calculateSmsPrice"></a>
# **calculateSmsPrice**
> CalculateSmsPrice calculateSmsPrice(contentType, calculateSmsPriceRequest)

Calculate SMS Price

Use this endpoint to calculate the price of sending messages. The cost of sending messages varies based on the &lt;a href&#x3D;\&quot;https://help.clicksend.com/article/h474eseq3a-how-many-characters-can-i-send-in-an-sms\&quot; target&#x3D;\&quot;_blank\&quot;&gt;type&lt;/a&gt; and length of the message.

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.SmsOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    SmsOtherApi apiInstance = new SmsOtherApi(defaultClient);
    String contentType = "application/json"; // String | 
    CalculateSmsPriceRequest calculateSmsPriceRequest = new CalculateSmsPriceRequest(); // CalculateSmsPriceRequest | 
    try {
      CalculateSmsPrice result = apiInstance.calculateSmsPrice(contentType, calculateSmsPriceRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SmsOtherApi#calculateSmsPrice");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **contentType** | **String**|  | [optional] |
| **calculateSmsPriceRequest** | [**CalculateSmsPriceRequest**](CalculateSmsPriceRequest.md)|  | [optional] |

### Return type

[**CalculateSmsPrice**](CalculateSmsPrice.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="cancelAllSms"></a>
# **cancelAllSms**
> CancelAllSms cancelAllSms(contentType, cancelAllSmsRequest)

Cancel All SMS

Use this endpoint to cancel all scheduled SMS. To cancel only one scheduled SMS, use the **Cancel SMS** endpoint.

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.SmsOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    SmsOtherApi apiInstance = new SmsOtherApi(defaultClient);
    String contentType = "application/json"; // String | 
    CancelAllSmsRequest cancelAllSmsRequest = new CancelAllSmsRequest(); // CancelAllSmsRequest | 
    try {
      CancelAllSms result = apiInstance.cancelAllSms(contentType, cancelAllSmsRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SmsOtherApi#cancelAllSms");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **contentType** | **String**|  | [optional] |
| **cancelAllSmsRequest** | [**CancelAllSmsRequest**](CancelAllSmsRequest.md)|  | [optional] |

### Return type

[**CancelAllSms**](CancelAllSms.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="cancelSms"></a>
# **cancelSms**
> CancelSms cancelSms(messageId, contentType)

Cancel SMS

Use this endpoint to cancel a specific scheduled SMS. Unlike the **Cancel All SMS** endpoint, which cancels all scheduled SMS, this endpoint only cancels one specified scheduled SMS.  Specify the scheduled SMS to cancel by providing its _message_id_.

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.SmsOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    SmsOtherApi apiInstance = new SmsOtherApi(defaultClient);
    String messageId = "messageId_example"; // String | The _message_id_ of the scheduled SMS to cancel.
    String contentType = "application/json"; // String | 
    try {
      CancelSms result = apiInstance.cancelSms(messageId, contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SmsOtherApi#cancelSms");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **messageId** | **String**| The _message_id_ of the scheduled SMS to cancel. | |
| **contentType** | **String**|  | [optional] |

### Return type

[**CancelSms**](CancelSms.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="createSmsDeliveryReceiptRule"></a>
# **createSmsDeliveryReceiptRule**
> CreateSmsDeliveryReceiptRule createSmsDeliveryReceiptRule(contentType, createSmsDeliveryReceiptRuleRequest)

Create SMS Delivery Receipt Rule

_Create sms delivery receipt automations_  Create sms delivery receipt automations  ### Properties  | Name | Type | Required | Restrictions | Description | | --- | --- | --- | --- | --- | | rule_name | string | true | none | Rule Name. | | match_type | number | true | none | Match Type. 0&#x3D;All reports. | | action | string | true | none | Action to be taken (AUTO_REPLY, EMAIL_USER, EMAIL_FIXED, URL, SMS, POLL, GROUP_SMS, MOVE_CONTACT, CREATE_CONTACT, CREATE_CONTACT_PLUS_EMAIL, CREATE_CONTACT_PLUS_NAME_EMAIL CREATE_CONTACT_PLUS_NAME, SMPP, NONE). | | action_address | string | true | none | Action address. | | enabled | number | true | none | Enabled: Disabled&#x3D;0 or Enabled&#x3D;1. |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.SmsOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    SmsOtherApi apiInstance = new SmsOtherApi(defaultClient);
    String contentType = "application/json"; // String | 
    CreateSmsDeliveryReceiptRuleRequest createSmsDeliveryReceiptRuleRequest = new CreateSmsDeliveryReceiptRuleRequest(); // CreateSmsDeliveryReceiptRuleRequest | 
    try {
      CreateSmsDeliveryReceiptRule result = apiInstance.createSmsDeliveryReceiptRule(contentType, createSmsDeliveryReceiptRuleRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SmsOtherApi#createSmsDeliveryReceiptRule");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **contentType** | **String**|  | [optional] |
| **createSmsDeliveryReceiptRuleRequest** | [**CreateSmsDeliveryReceiptRuleRequest**](CreateSmsDeliveryReceiptRuleRequest.md)|  | [optional] |

### Return type

[**CreateSmsDeliveryReceiptRule**](CreateSmsDeliveryReceiptRule.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="createSmsInboundAutomation"></a>
# **createSmsInboundAutomation**
> CreateSmsInboundAutomation createSmsInboundAutomation(contentType, createSmsInboundAutomationRequest)

Create SMS Inbound Automation

_Create new inbound sms automation_  Create new inbound sms automation  | Name | Type | Required | Restrictions | Description | | --- | --- | --- | --- | --- | | dedicated_number | string | true | none | Decicated Number. Can be &#39;\\*&#39; to apply to all numbers. | | rule_name | string | true | none | Rule Name. | | message_search_type | number | true | none | Message Search Type: 0&#x3D;Any message, 1&#x3D;starts with, 2&#x3D;contains, 3&#x3D;does not contain. | | message_search_term | string | true | none | Message search term. | | action | string | true | none | Action to be taken (AUTO_REPLY, EMAIL_USER, EMAIL_FIXED, URL, SMS, POLL, GROUP_SMS, MOVE_CONTACT, CREATE_CONTACT, CREATE_CONTACT_PLUS_EMAIL, CREATE_CONTACT_PLUS_NAME_EMAIL CREATE_CONTACT_PLUS_NAME, SMPP, NONE). | | action_address | string | true | none | Action address. | | enabled | number | true | none | Enabled: Disabled&#x3D;0 or Enabled&#x3D;1. | | webhook_type | string | false | Required when action &#x3D; URL only | Set as post, get, or json to change the format of the request sent. |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.SmsOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    SmsOtherApi apiInstance = new SmsOtherApi(defaultClient);
    String contentType = "application/json"; // String | 
    CreateSmsInboundAutomationRequest createSmsInboundAutomationRequest = new CreateSmsInboundAutomationRequest(); // CreateSmsInboundAutomationRequest | 
    try {
      CreateSmsInboundAutomation result = apiInstance.createSmsInboundAutomation(contentType, createSmsInboundAutomationRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SmsOtherApi#createSmsInboundAutomation");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **contentType** | **String**|  | [optional] |
| **createSmsInboundAutomationRequest** | [**CreateSmsInboundAutomationRequest**](CreateSmsInboundAutomationRequest.md)|  | [optional] |

### Return type

[**CreateSmsInboundAutomation**](CreateSmsInboundAutomation.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="createSmsTemplate"></a>
# **createSmsTemplate**
> CreateSmsTemplate createSmsTemplate(contentType, createSmsTemplateRequest)

Create SMS Template

Use this endpoint to create a SMS template that you can use for sending SMS.

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.SmsOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    SmsOtherApi apiInstance = new SmsOtherApi(defaultClient);
    String contentType = "application/json"; // String | 
    CreateSmsTemplateRequest createSmsTemplateRequest = new CreateSmsTemplateRequest(); // CreateSmsTemplateRequest | 
    try {
      CreateSmsTemplate result = apiInstance.createSmsTemplate(contentType, createSmsTemplateRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SmsOtherApi#createSmsTemplate");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **contentType** | **String**|  | [optional] |
| **createSmsTemplateRequest** | [**CreateSmsTemplateRequest**](CreateSmsTemplateRequest.md)|  | [optional] |

### Return type

[**CreateSmsTemplate**](CreateSmsTemplate.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="createTestInboundSms"></a>
# **createTestInboundSms**
> CreateTestInboundSms createTestInboundSms(contentType, createTestInboundSmsRequest)

Create Test Inbound SMS

Use this endpoint to generate and send a test &lt;a href&#x3D;\&quot;https://help.clicksend.com/article/ik4hw5xu35-can-i-receive-inbound-sms-to-my-url\&quot; target&#x3D;\&quot;_blank\&quot;&gt;inbound SMS&lt;/a&gt; to your webhook URL. Inbound SMS are messages sent by your recipient to you.  This test endpoint allows you to verify that the inbound SMS is correctly sent to your webhook URL.

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.SmsOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    SmsOtherApi apiInstance = new SmsOtherApi(defaultClient);
    String contentType = "application/json"; // String | 
    CreateTestInboundSmsRequest createTestInboundSmsRequest = new CreateTestInboundSmsRequest(); // CreateTestInboundSmsRequest | 
    try {
      CreateTestInboundSms result = apiInstance.createTestInboundSms(contentType, createTestInboundSmsRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SmsOtherApi#createTestInboundSms");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **contentType** | **String**|  | [optional] |
| **createTestInboundSmsRequest** | [**CreateTestInboundSmsRequest**](CreateTestInboundSmsRequest.md)|  | [optional] |

### Return type

[**CreateTestInboundSms**](CreateTestInboundSms.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="createTestSmsReceipt"></a>
# **createTestSmsReceipt**
> CreateTestSmsReceipt createTestSmsReceipt(contentType, createTestSmsReceiptRequest)

Create Test SMS Receipt

Use this endpoint to generate and send a test &lt;a href&#x3D;\&quot;https://help.clicksend.com/article/49eq1qdcui-how-do-i-receive-sms-delivery-receipts-delivery-status-updates\&quot; target&#x3D;\&quot;_blank\&quot;&gt;SMS delivery receipt&lt;/a&gt; to your webhook URL. When you send an SMS, a delivery receipt is generated and can be received at your webhook URL. This test endpoint allows you to verify that the receipt is correctly sent to your webhook URL.  Additionally, you can obtain SMS receipts by setting the webhook URL to **poll** and periodically calling the **View SMS Receipt** endpoint to check for new receipts. This process is known as _polling_.

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.SmsOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    SmsOtherApi apiInstance = new SmsOtherApi(defaultClient);
    String contentType = "application/json"; // String | 
    CreateTestSmsReceiptRequest createTestSmsReceiptRequest = new CreateTestSmsReceiptRequest(); // CreateTestSmsReceiptRequest | 
    try {
      CreateTestSmsReceipt result = apiInstance.createTestSmsReceipt(contentType, createTestSmsReceiptRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SmsOtherApi#createTestSmsReceipt");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **contentType** | **String**|  | [optional] |
| **createTestSmsReceiptRequest** | [**CreateTestSmsReceiptRequest**](CreateTestSmsReceiptRequest.md)|  | [optional] |

### Return type

[**CreateTestSmsReceipt**](CreateTestSmsReceipt.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="deleteSmsDeliveryReceiptRule"></a>
# **deleteSmsDeliveryReceiptRule**
> DeleteSmsDeliveryReceiptRule deleteSmsDeliveryReceiptRule(receiptRuleId, contentType)

Delete SMS Delivery Receipt Rule

_Delete sms delivery receipt automation_  Delete sms delivery receipt automation  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | receipt_rule_id | path | integer(int32) | true | Receipt rule id |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.SmsOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    SmsOtherApi apiInstance = new SmsOtherApi(defaultClient);
    String receiptRuleId = "receiptRuleId_example"; // String | 
    String contentType = "application/json"; // String | 
    try {
      DeleteSmsDeliveryReceiptRule result = apiInstance.deleteSmsDeliveryReceiptRule(receiptRuleId, contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SmsOtherApi#deleteSmsDeliveryReceiptRule");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **receiptRuleId** | **String**|  | |
| **contentType** | **String**|  | [optional] |

### Return type

[**DeleteSmsDeliveryReceiptRule**](DeleteSmsDeliveryReceiptRule.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="deleteSmsInboundAutomation"></a>
# **deleteSmsInboundAutomation**
> DeleteSmsInboundAutomation deleteSmsInboundAutomation(inboundRuleId, contentType)

Delete SMS Inbound Automation

_Delete inbound sms automation_  Delete inbound sms automation  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | inbound_rule_id | path | integer(int32) | true | Inbound rule id |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.SmsOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    SmsOtherApi apiInstance = new SmsOtherApi(defaultClient);
    String inboundRuleId = "inboundRuleId_example"; // String | 
    String contentType = "application/json"; // String | 
    try {
      DeleteSmsInboundAutomation result = apiInstance.deleteSmsInboundAutomation(inboundRuleId, contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SmsOtherApi#deleteSmsInboundAutomation");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **inboundRuleId** | **String**|  | |
| **contentType** | **String**|  | [optional] |

### Return type

[**DeleteSmsInboundAutomation**](DeleteSmsInboundAutomation.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="deleteSmsTemplate"></a>
# **deleteSmsTemplate**
> DeleteSmsTemplate deleteSmsTemplate(templateId, contentType)

Delete SMS Template

Use this endpoint to delete a &lt;a href&#x3D;\&quot;https://help.clicksend.com/article/9z9uloaz8y-sms-templates-for-different-industries\&quot; target&#x3D;\&quot;_blank\&quot;&gt;SMS template&lt;/a&gt;. Specify the SMS template to delete by providing its _template_id_.

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.SmsOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    SmsOtherApi apiInstance = new SmsOtherApi(defaultClient);
    String templateId = "templateId_example"; // String | The ID of the template to delete.
    String contentType = "application/json"; // String | 
    try {
      DeleteSmsTemplate result = apiInstance.deleteSmsTemplate(templateId, contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SmsOtherApi#deleteSmsTemplate");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **templateId** | **String**| The ID of the template to delete. | |
| **contentType** | **String**|  | [optional] |

### Return type

[**DeleteSmsTemplate**](DeleteSmsTemplate.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="exportSmsHistory"></a>
# **exportSmsHistory**
> ExportSmsHistory exportSmsHistory(contentType, filename, page, limit, q, orderBy, dateFrom, dateTo)

Export SMS History

Use this endpoint to create a download link of your SMS history. You can filter the SMS history result using the query parameters.

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.SmsOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    SmsOtherApi apiInstance = new SmsOtherApi(defaultClient);
    String contentType = "application/json"; // String | 
    String filename = "export.csv"; // String | The filename of the result. It should be in the .csv format.
    Integer page = 1; // Integer | The page number to retrieve. Use this parameter to navigate through the [pagination](/#pagination) results. The default value is 1.
    Integer limit = 15; // Integer | The number of items to return per page. This parameter controls the size of each page of results. The default value is 15.
    String q = "field_name"; // String | Allows filtering of results based on your search criteria. The query should be in the format `field_name:value`.  1. **Field Name**: The field within the SMS history you want to filter by. You can use the following fields:          - _Status_: The status of the SMS. Available values for status are: Queued, Completed, Scheduled, WaitApproval, Failed, Cancelled, CancelledAfterReview, Received, Sent.              - _To_: The recipient of the SMS.              - _from_: The sender of the SMS.              - _subaccount_id_: The sub-account identifier.              - _message_id_: The ID of your SMS.          2. **Value**: The text or keyword you're searching for within the specified field. If left empty after the colon, the filter will look for all templates with any value in the **Field Name**.             For example, if you are searching for a SMS with the status of _Scheduled_, the final query would look like this:    `q=status:Scheduled`  <div class=\"info-box\">   <h4><i class=\"fas fa-info-circle\"></i> Note:</h4>   <div>   <p>Some characters have to be encoded. For example, if you are searching for SMS sent from the phone number +61437085284, your search query q would be:<br/></p>     <ul>       <li>q=from:%2B61437085284</li>     </ul>     <p>You can use the <a href=\"https://www.urlencoder.org/\" target=\"_blank\">URL encoder</a> to encode the text. If a character is not an alphanumeric character (A-Z, a-z, 0-9), it is typically either reserved or unsafe and should be encoded.</p>   </div> </div>
    String orderBy = "date:asc"; // String | Specifies the field and order to sort the results by. The value is composed of the field name followed by a colon and the sort direction (asc for ascending or desc for descending).  The default sort order is by date in ascending order. You can use the following fields:    - _date_    - _username_   - _from_    - _to_   - _status_    - _body_  For example, if you want to order by the most recently sent SMS, you should sort by date in descending order. The query would look like this:    `order_by=date:desc`
    Integer dateFrom = 56; // Integer | Start date to filter results. It should be in <a href=\"http://help.clicksend.com/what-is-a-unix-timestamp\" target=\"_blank\">Unix format</a>.
    Integer dateTo = 56; // Integer | End date to filter results. It should be in <a href=\"http://help.clicksend.com/what-is-a-unix-timestamp\" target=\"_blank\">Unix format</a>.
    try {
      ExportSmsHistory result = apiInstance.exportSmsHistory(contentType, filename, page, limit, q, orderBy, dateFrom, dateTo);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SmsOtherApi#exportSmsHistory");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **contentType** | **String**|  | [optional] |
| **filename** | **String**| The filename of the result. It should be in the .csv format. | [optional] [default to export.csv] |
| **page** | **Integer**| The page number to retrieve. Use this parameter to navigate through the [pagination](/#pagination) results. The default value is 1. | [optional] [default to 1] |
| **limit** | **Integer**| The number of items to return per page. This parameter controls the size of each page of results. The default value is 15. | [optional] [default to 15] |
| **q** | **String**| Allows filtering of results based on your search criteria. The query should be in the format &#x60;field_name:value&#x60;.  1. **Field Name**: The field within the SMS history you want to filter by. You can use the following fields:          - _Status_: The status of the SMS. Available values for status are: Queued, Completed, Scheduled, WaitApproval, Failed, Cancelled, CancelledAfterReview, Received, Sent.              - _To_: The recipient of the SMS.              - _from_: The sender of the SMS.              - _subaccount_id_: The sub-account identifier.              - _message_id_: The ID of your SMS.          2. **Value**: The text or keyword you&#39;re searching for within the specified field. If left empty after the colon, the filter will look for all templates with any value in the **Field Name**.             For example, if you are searching for a SMS with the status of _Scheduled_, the final query would look like this:    &#x60;q&#x3D;status:Scheduled&#x60;  &lt;div class&#x3D;\&quot;info-box\&quot;&gt;   &lt;h4&gt;&lt;i class&#x3D;\&quot;fas fa-info-circle\&quot;&gt;&lt;/i&gt; Note:&lt;/h4&gt;   &lt;div&gt;   &lt;p&gt;Some characters have to be encoded. For example, if you are searching for SMS sent from the phone number +61437085284, your search query q would be:&lt;br/&gt;&lt;/p&gt;     &lt;ul&gt;       &lt;li&gt;q&#x3D;from:%2B61437085284&lt;/li&gt;     &lt;/ul&gt;     &lt;p&gt;You can use the &lt;a href&#x3D;\&quot;https://www.urlencoder.org/\&quot; target&#x3D;\&quot;_blank\&quot;&gt;URL encoder&lt;/a&gt; to encode the text. If a character is not an alphanumeric character (A-Z, a-z, 0-9), it is typically either reserved or unsafe and should be encoded.&lt;/p&gt;   &lt;/div&gt; &lt;/div&gt; | [optional] [default to field_name] |
| **orderBy** | **String**| Specifies the field and order to sort the results by. The value is composed of the field name followed by a colon and the sort direction (asc for ascending or desc for descending).  The default sort order is by date in ascending order. You can use the following fields:    - _date_    - _username_   - _from_    - _to_   - _status_    - _body_  For example, if you want to order by the most recently sent SMS, you should sort by date in descending order. The query would look like this:    &#x60;order_by&#x3D;date:desc&#x60; | [optional] [default to date:asc] |
| **dateFrom** | **Integer**| Start date to filter results. It should be in &lt;a href&#x3D;\&quot;http://help.clicksend.com/what-is-a-unix-timestamp\&quot; target&#x3D;\&quot;_blank\&quot;&gt;Unix format&lt;/a&gt;. | [optional] |
| **dateTo** | **Integer**| End date to filter results. It should be in &lt;a href&#x3D;\&quot;http://help.clicksend.com/what-is-a-unix-timestamp\&quot; target&#x3D;\&quot;_blank\&quot;&gt;Unix format&lt;/a&gt;. | [optional] |

### Return type

[**ExportSmsHistory**](ExportSmsHistory.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="markInboundSmsAsRead"></a>
# **markInboundSmsAsRead**
> MarkInboundSmsAsRead markInboundSmsAsRead(contentType, markSmsReceiptAsReadRequest)

Mark Inbound SMS as Read

Use this endpoint to mark all &lt;a href&#x3D;\&quot;https://help.clicksend.com/article/ik4hw5xu35-can-i-receive-inbound-sms-to-my-url\&quot; target&#x3D;\&quot;_blank\&quot;&gt;inbound SMS&lt;/a&gt; as read. Inbound SMS that has been marked as read won’t be shown in the **View Inbound SMS** endpoint. You can still use the **View Specific Inbound SMS** endpoint to view inbound SMS marked as read.  In the request, you can optionally add a _date_before_ parameter to only mark inbound SMS sent before that date as read.

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.SmsOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    SmsOtherApi apiInstance = new SmsOtherApi(defaultClient);
    String contentType = "application/json"; // String | 
    MarkSmsReceiptAsReadRequest markSmsReceiptAsReadRequest = new MarkSmsReceiptAsReadRequest(); // MarkSmsReceiptAsReadRequest | 
    try {
      MarkInboundSmsAsRead result = apiInstance.markInboundSmsAsRead(contentType, markSmsReceiptAsReadRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SmsOtherApi#markInboundSmsAsRead");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **contentType** | **String**|  | [optional] |
| **markSmsReceiptAsReadRequest** | [**MarkSmsReceiptAsReadRequest**](MarkSmsReceiptAsReadRequest.md)|  | [optional] |

### Return type

[**MarkInboundSmsAsRead**](MarkInboundSmsAsRead.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="markSmsReceiptAsRead"></a>
# **markSmsReceiptAsRead**
> MarkSmsReceiptAsRead markSmsReceiptAsRead(contentType, markSmsReceiptAsReadRequest)

Mark SMS Receipt As Read

Use this endpoint to mark all &lt;a target&#x3D;\&quot;_blank\&quot; href&#x3D;\&quot;https://help.clicksend.com/article/49eq1qdcui-how-do-i-receive-sms-delivery-receipts-delivery-status-updates\&quot;&gt;SMS delivery receipts&lt;/a&gt; as read. Delivery receipts that have been marked as read won’t be shown in the **View SMS Receipts** endpoint.  You can still use the **View Specific SMS Receipt** endpoint to view delivery receipts marked as read. In the request, you can optionally add a _date_before_ parameter to only mark receipts sent before that date as read

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.SmsOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    SmsOtherApi apiInstance = new SmsOtherApi(defaultClient);
    String contentType = "application/json"; // String | 
    MarkSmsReceiptAsReadRequest markSmsReceiptAsReadRequest = new MarkSmsReceiptAsReadRequest(); // MarkSmsReceiptAsReadRequest | 
    try {
      MarkSmsReceiptAsRead result = apiInstance.markSmsReceiptAsRead(contentType, markSmsReceiptAsReadRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SmsOtherApi#markSmsReceiptAsRead");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **contentType** | **String**|  | [optional] |
| **markSmsReceiptAsReadRequest** | [**MarkSmsReceiptAsReadRequest**](MarkSmsReceiptAsReadRequest.md)|  | [optional] |

### Return type

[**MarkSmsReceiptAsRead**](MarkSmsReceiptAsRead.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="markSpecificInboundSmsMessageAsRead"></a>
# **markSpecificInboundSmsMessageAsRead**
> MarkSpecificInboundSmsMessageAsRead markSpecificInboundSmsMessageAsRead(messageId, contentType)

Mark Specific Inbound SMS Message As Read

Use this endpoint to mark a specific &lt;a href&#x3D;\&quot;https://help.clicksend.com/article/ik4hw5xu35-can-i-receive-inbound-sms-to-my-url\&quot; target&#x3D;\&quot;_blank\&quot;&gt;inbound SMS&lt;/a&gt; as read. Unlike the **View Inbound SMS** endpoint, which marks all inbound SMS as read,  this endpoint only marks one specified inbound SMS. Specify the SMS to be marked as read by providing its _message_id_.

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.SmsOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    SmsOtherApi apiInstance = new SmsOtherApi(defaultClient);
    String messageId = "messageId_example"; // String | The message_id of the inbound SMS to mark as read.  <div class=\"info-box\">   <h4><i class=\"fas fa-info-circle\"></i> Note:</h4>   <p>     When you receive an inbound message, you will get two parameters: <em>original_message_id</em> and <em>message_id</em>:   </p>   <ul>     <li><em>original_message_id</em>: This is the ID of the outbound message sent to the recipient</li>     <li><em>message_id</em>: This is the ID of the inbound message sent by the recipient.</li>   </ul> </div>
    String contentType = "application/json"; // String | 
    try {
      MarkSpecificInboundSmsMessageAsRead result = apiInstance.markSpecificInboundSmsMessageAsRead(messageId, contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SmsOtherApi#markSpecificInboundSmsMessageAsRead");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **messageId** | **String**| The message_id of the inbound SMS to mark as read.  &lt;div class&#x3D;\&quot;info-box\&quot;&gt;   &lt;h4&gt;&lt;i class&#x3D;\&quot;fas fa-info-circle\&quot;&gt;&lt;/i&gt; Note:&lt;/h4&gt;   &lt;p&gt;     When you receive an inbound message, you will get two parameters: &lt;em&gt;original_message_id&lt;/em&gt; and &lt;em&gt;message_id&lt;/em&gt;:   &lt;/p&gt;   &lt;ul&gt;     &lt;li&gt;&lt;em&gt;original_message_id&lt;/em&gt;: This is the ID of the outbound message sent to the recipient&lt;/li&gt;     &lt;li&gt;&lt;em&gt;message_id&lt;/em&gt;: This is the ID of the inbound message sent by the recipient.&lt;/li&gt;   &lt;/ul&gt; &lt;/div&gt; | |
| **contentType** | **String**|  | [optional] |

### Return type

[**MarkSpecificInboundSmsMessageAsRead**](MarkSpecificInboundSmsMessageAsRead.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="sendSms"></a>
# **sendSms**
> SendSms sendSms(contentType, sendSmsRequest)

Send SMS

Use this endpoint to send messages to your recipients, either as phone numbers or contacts from your contact list.  The sender of the message (&lt;a href&#x3D;\&quot;https://help.clicksend.com/article/4kgj7krx00-what-is-a-sender-id-or-sender-number\&quot; target&#x3D;\&quot;_blank\&quot;&gt;&lt;strong&gt;Sender ID&lt;/strong&gt;&lt;/a&gt;) can be a shared number, a dedicated number, alpha tag (business name), or your own number.  You can send messages both locally and globally, subject to the country restrictions. The cost of sending messages varies based on the &lt;a href&#x3D;\&quot;https://help.clicksend.com/article/h474eseq3a-how-many-characters-can-i-send-in-an-sms\&quot; target&#x3D;\&quot;_blank\&quot;&gt;type&lt;/a&gt; and length of the message.

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.SmsOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    SmsOtherApi apiInstance = new SmsOtherApi(defaultClient);
    String contentType = "application/json"; // String | 
    SendSmsRequest sendSmsRequest = new SendSmsRequest(); // SendSmsRequest | 
    try {
      SendSms result = apiInstance.sendSms(contentType, sendSmsRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SmsOtherApi#sendSms");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **contentType** | **String**|  | [optional] |
| **sendSmsRequest** | [**SendSmsRequest**](SendSmsRequest.md)|  | [optional] |

### Return type

[**SendSms**](SendSms.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="updateSmsDeliveryReceiptRule"></a>
# **updateSmsDeliveryReceiptRule**
> UpdateSmsDeliveryReceiptRule updateSmsDeliveryReceiptRule(receiptRuleId, contentType, createSmsDeliveryReceiptRuleRequest)

Update SMS Delivery Receipt Rule

_Update sms delivery receipt automation_  Update sms delivery receipt automation  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | receipt_rule_id | path | integer(int32) | true | Receipt rule id |  ### Properties  | Name | Type | Required | Restrictions | Description | | --- | --- | --- | --- | --- | | rule_name | string | true | none | Rule Name. | | match_type | number | true | none | Match Type. 0&#x3D;All reports. | | action | string | true | none | Action to be taken (AUTO_REPLY, EMAIL_USER, EMAIL_FIXED, URL, SMS, POLL, GROUP_SMS, MOVE_CONTACT, CREATE_CONTACT, CREATE_CONTACT_PLUS_EMAIL, CREATE_CONTACT_PLUS_NAME_EMAIL CREATE_CONTACT_PLUS_NAME, SMPP, NONE). | | action_address | string | true | none | Action address. | | enabled | number | true | none | Enabled: Disabled&#x3D;0 or Enabled&#x3D;1. |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.SmsOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    SmsOtherApi apiInstance = new SmsOtherApi(defaultClient);
    String receiptRuleId = "receiptRuleId_example"; // String | 
    String contentType = "application/json"; // String | 
    CreateSmsDeliveryReceiptRuleRequest createSmsDeliveryReceiptRuleRequest = new CreateSmsDeliveryReceiptRuleRequest(); // CreateSmsDeliveryReceiptRuleRequest | 
    try {
      UpdateSmsDeliveryReceiptRule result = apiInstance.updateSmsDeliveryReceiptRule(receiptRuleId, contentType, createSmsDeliveryReceiptRuleRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SmsOtherApi#updateSmsDeliveryReceiptRule");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **receiptRuleId** | **String**|  | |
| **contentType** | **String**|  | [optional] |
| **createSmsDeliveryReceiptRuleRequest** | [**CreateSmsDeliveryReceiptRuleRequest**](CreateSmsDeliveryReceiptRuleRequest.md)|  | [optional] |

### Return type

[**UpdateSmsDeliveryReceiptRule**](UpdateSmsDeliveryReceiptRule.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="updateSmsInboundAutomation"></a>
# **updateSmsInboundAutomation**
> UpdateSmsInboundAutomation updateSmsInboundAutomation(inboundRuleId, contentType, updateSmsInboundAutomationRequest)

Update SMS Inbound Automation

_Update inbound sms automation_  Update inbound sms automation  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | inbound_rule_id | path | integer(int32) | true | Inbound rule id |  ### Properties  | Name | Type | Required | Restrictions | Description | | --- | --- | --- | --- | --- | | dedicated_number | string | true | none | Dedicated Number. Can be &#39;\\*&#39; to apply to all numbers. | | rule_name | string | true | none | Rule Name. | | message_search_type | number | true | none | Message Search Type: 0&#x3D;Any message, 1&#x3D;starts with, 2&#x3D;contains, 3&#x3D;does not contain. | | message_search_term | string | true | none | Message search term. | | action | string | true | none | Action to be taken (AUTO_REPLY, EMAIL_USER, EMAIL_FIXED, URL, SMS, POLL, GROUP_SMS, MOVE_CONTACT, CREATE_CONTACT, CREATE_CONTACT_PLUS_EMAIL, CREATE_CONTACT_PLUS_NAME_EMAIL CREATE_CONTACT_PLUS_NAME, SMPP, NONE). | | action_address | string | true | none | Action address. | | enabled | number | true | none | Enabled: Disabled&#x3D;0 or Enabled&#x3D;1. | | webhook_type | string | false | Required when action &#x3D; URL only | Set as post, get, or json to change the format of the request sent. |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.SmsOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    SmsOtherApi apiInstance = new SmsOtherApi(defaultClient);
    String inboundRuleId = "inboundRuleId_example"; // String | 
    String contentType = "application/json"; // String | 
    UpdateSmsInboundAutomationRequest updateSmsInboundAutomationRequest = new UpdateSmsInboundAutomationRequest(); // UpdateSmsInboundAutomationRequest | 
    try {
      UpdateSmsInboundAutomation result = apiInstance.updateSmsInboundAutomation(inboundRuleId, contentType, updateSmsInboundAutomationRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SmsOtherApi#updateSmsInboundAutomation");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **inboundRuleId** | **String**|  | |
| **contentType** | **String**|  | [optional] |
| **updateSmsInboundAutomationRequest** | [**UpdateSmsInboundAutomationRequest**](UpdateSmsInboundAutomationRequest.md)|  | [optional] |

### Return type

[**UpdateSmsInboundAutomation**](UpdateSmsInboundAutomation.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="updateSmsTemplate"></a>
# **updateSmsTemplate**
> UpdateSmsTemplate updateSmsTemplate(templateId, contentType, createSmsTemplateRequest)

Update SMS Template

Use this endpoint to update a &lt;a href&#x3D;\&quot;https://help.clicksend.com/article/9z9uloaz8y-sms-templates-for-different-industries\&quot; target&#x3D;\&quot;_blank\&quot;&gt;SMS template&lt;/a&gt;.

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.SmsOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    SmsOtherApi apiInstance = new SmsOtherApi(defaultClient);
    String templateId = "templateId_example"; // String | The ID of the template to update.
    String contentType = "application/json"; // String | 
    CreateSmsTemplateRequest createSmsTemplateRequest = new CreateSmsTemplateRequest(); // CreateSmsTemplateRequest | 
    try {
      UpdateSmsTemplate result = apiInstance.updateSmsTemplate(templateId, contentType, createSmsTemplateRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SmsOtherApi#updateSmsTemplate");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **templateId** | **String**| The ID of the template to update. | |
| **contentType** | **String**|  | [optional] |
| **createSmsTemplateRequest** | [**CreateSmsTemplateRequest**](CreateSmsTemplateRequest.md)|  | [optional] |

### Return type

[**UpdateSmsTemplate**](UpdateSmsTemplate.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewASpecificInboundSmsMessage"></a>
# **viewASpecificInboundSmsMessage**
> ViewASpecificInboundSmsMessage viewASpecificInboundSmsMessage(originalMessageId, contentType)

View a specific inbound SMS message

Use this endpoint to retrieve a specific inbound SMS, including those that have been marked as read.  Inbound SMS are messages sent by your recipient to you. This endpoint enables you to retrieve those inbound SMS.

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.SmsOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    SmsOtherApi apiInstance = new SmsOtherApi(defaultClient);
    String originalMessageId = "originalMessageId_example"; // String | The _original_message_id_ of the inbound SMS to view. If the recipient replied with multiple messages, this endpoint returns the first inbound SMS received.  <div class=\"info-box\">   <h4><i class=\"fas fa-info-circle\"></i> Note:</h4>   <p>     When you receive an inbound message, you will get two parameters: <em>original_message_id</em> and <em>message_id</em>:   </p>   <ul>     <li><em>original_message_id</em>: This is the ID of the outbound message sent to the recipient</li>     <li><em>message_id</em>: This is the ID of the inbound message sent by the recipient.</li>   </ul> </div>
    String contentType = "application/json"; // String | 
    try {
      ViewASpecificInboundSmsMessage result = apiInstance.viewASpecificInboundSmsMessage(originalMessageId, contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SmsOtherApi#viewASpecificInboundSmsMessage");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **originalMessageId** | **String**| The _original_message_id_ of the inbound SMS to view. If the recipient replied with multiple messages, this endpoint returns the first inbound SMS received.  &lt;div class&#x3D;\&quot;info-box\&quot;&gt;   &lt;h4&gt;&lt;i class&#x3D;\&quot;fas fa-info-circle\&quot;&gt;&lt;/i&gt; Note:&lt;/h4&gt;   &lt;p&gt;     When you receive an inbound message, you will get two parameters: &lt;em&gt;original_message_id&lt;/em&gt; and &lt;em&gt;message_id&lt;/em&gt;:   &lt;/p&gt;   &lt;ul&gt;     &lt;li&gt;&lt;em&gt;original_message_id&lt;/em&gt;: This is the ID of the outbound message sent to the recipient&lt;/li&gt;     &lt;li&gt;&lt;em&gt;message_id&lt;/em&gt;: This is the ID of the inbound message sent by the recipient.&lt;/li&gt;   &lt;/ul&gt; &lt;/div&gt; | |
| **contentType** | **String**|  | [optional] |

### Return type

[**ViewASpecificInboundSmsMessage**](ViewASpecificInboundSmsMessage.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewASpecificSmsTemplate"></a>
# **viewASpecificSmsTemplate**
> ViewASpecificSmsTemplate viewASpecificSmsTemplate(templateId, contentType)

View a Specific SMS Template

Use this endpoint to retrieve a &lt;a href&#x3D;\&quot;https://help.clicksend.com/article/9z9uloaz8y-sms-templates-for-different-industries\&quot; target&#x3D;\&quot;_blank\&quot;&gt;SMS template&lt;/a&gt;. Specify which template to retrieve using the template ID.

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.SmsOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    SmsOtherApi apiInstance = new SmsOtherApi(defaultClient);
    String templateId = "templateId_example"; // String | The ID of the template to retrieve
    String contentType = "application/json"; // String | 
    try {
      ViewASpecificSmsTemplate result = apiInstance.viewASpecificSmsTemplate(templateId, contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SmsOtherApi#viewASpecificSmsTemplate");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **templateId** | **String**| The ID of the template to retrieve | |
| **contentType** | **String**|  | [optional] |

### Return type

[**ViewASpecificSmsTemplate**](ViewASpecificSmsTemplate.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewInboundSms"></a>
# **viewInboundSms**
> ViewInboundSms viewInboundSms(contentType, page, limit)

View Inbound SMS

Use this endpoint to retrieve &lt;a href&#x3D;\&quot;https://help.clicksend.com/article/49eq1qdcui-how-do-i-receive-sms-delivery-receipts-delivery-status-updates\&quot; target&#x3D;\&quot;_blank\&quot;&gt;SMS delivery receipts&lt;/a&gt; sent by your recipient.  To be able to view receipts, add a &lt;a href&#x3D;\&quot;https://help.clicksend.com/article/ut4ttdrrai-incoming-reply-sms-options\&quot;&gt;inbound rule&lt;/a&gt; with the Action set to **POLL** in the Dashboard, or use the [**Create SMS Inbound Automation**](/automations/sms/other/create-sms-inbound-automation) endpoint.  Control [pagination](/#pagination) with the _page_ and _limit_ query parameters to specify the page of results and the number of items returned.  &lt;div class&#x3D;\&quot;info-box\&quot;&gt;   &lt;h4&gt;&lt;i class&#x3D;\&quot;fas fa-info-circle\&quot;&gt;&lt;/i&gt; Note:&lt;/h4&gt;   &lt;p&gt;If you have multiple inbound rules set to &lt;strong&gt;POLL&lt;/strong&gt;, you will receive the inbound message multiple times.&lt;/p&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.SmsOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    SmsOtherApi apiInstance = new SmsOtherApi(defaultClient);
    String contentType = "application/json"; // String | 
    Integer page = 1; // Integer | The page number to retrieve. Use this parameter to navigate through the [pagination](/#pagination) results. The default value is 1.
    Integer limit = 15; // Integer | The number of items to return per page. This parameter controls the size of each page of results. The default value is 15.
    try {
      ViewInboundSms result = apiInstance.viewInboundSms(contentType, page, limit);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SmsOtherApi#viewInboundSms");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **contentType** | **String**|  | [optional] |
| **page** | **Integer**| The page number to retrieve. Use this parameter to navigate through the [pagination](/#pagination) results. The default value is 1. | [optional] [default to 1] |
| **limit** | **Integer**| The number of items to return per page. This parameter controls the size of each page of results. The default value is 15. | [optional] [default to 15] |

### Return type

[**ViewInboundSms**](ViewInboundSms.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewSmsDeliveryReceiptRule"></a>
# **viewSmsDeliveryReceiptRule**
> ViewSmsDeliveryReceiptRule viewSmsDeliveryReceiptRule(receiptRuleId, contentType)

View SMS Delivery Receipt Rule

_Get specific sms delivery receipt automation_  Get specific sms delivery receipt automation  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | receipt_rule_id | path | integer(int32) | true | Receipt rule id |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.SmsOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    SmsOtherApi apiInstance = new SmsOtherApi(defaultClient);
    String receiptRuleId = "receiptRuleId_example"; // String | 
    String contentType = "application/json"; // String | 
    try {
      ViewSmsDeliveryReceiptRule result = apiInstance.viewSmsDeliveryReceiptRule(receiptRuleId, contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SmsOtherApi#viewSmsDeliveryReceiptRule");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **receiptRuleId** | **String**|  | |
| **contentType** | **String**|  | [optional] |

### Return type

[**ViewSmsDeliveryReceiptRule**](ViewSmsDeliveryReceiptRule.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewSmsDeliveryReceiptRules"></a>
# **viewSmsDeliveryReceiptRules**
> ViewSmsDeliveryReceiptRules viewSmsDeliveryReceiptRules(contentType)

View SMS Delivery Receipt Rules

_Get all sms delivery receipt automations_  Get all sms delivery receipt automations  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | page | query | integer(int32) | false | Page number | | limit | query | integer(int32) | false | Number of records per page |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.SmsOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    SmsOtherApi apiInstance = new SmsOtherApi(defaultClient);
    String contentType = "application/json"; // String | 
    try {
      ViewSmsDeliveryReceiptRules result = apiInstance.viewSmsDeliveryReceiptRules(contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SmsOtherApi#viewSmsDeliveryReceiptRules");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **contentType** | **String**|  | [optional] |

### Return type

[**ViewSmsDeliveryReceiptRules**](ViewSmsDeliveryReceiptRules.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewSmsHistory"></a>
# **viewSmsHistory**
> ViewSmsHistory viewSmsHistory(contentType, page, limit, q, orderBy, dateFrom, dateTo)

View SMS History

Use this endpoint to view previously sent SMS. You can filter the SMS history result using the query parameters.

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.SmsOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    SmsOtherApi apiInstance = new SmsOtherApi(defaultClient);
    String contentType = "application/json"; // String | 
    Integer page = 1; // Integer | The page number to retrieve. Use this parameter to navigate through the [pagination](/#pagination) results. The default value is 1.
    Integer limit = 15; // Integer | The number of items to return per page. This parameter controls the size of each page of results. The default value is 15.
    String q = "field_name"; // String | Allows filtering of results based on your search criteria. The query should be in the format `field_name:value`.  1. **Field Name**: The field within the SMS history you want to filter by. You can use the following fields:          - _Status_: The status of the SMS. Available values for status are: Queued, Completed, Scheduled, WaitApproval, Failed, Cancelled, CancelledAfterReview, Received, Sent.              - _To_: The recipient of the SMS.              - _from_: The sender of the SMS.              - _subaccount_id_: The sub-account identifier.              - _message_id_: The ID of your SMS.          2. **Value**: The text or keyword you're searching for within the specified field. If left empty after the colon, the filter will look for all templates with any value in the **Field Name**.             For example, if you are searching for a SMS with the status of Scheduled, the final query would look like this:    `q=status:Scheduled`  <div class=\"info-box\">   <h4><i class=\"fas fa-info-circle\"></i> Note:</h4>   <div>    <p>Some characters have to be encoded. For example, if you are searching for SMS sent from the phone number +61437085284, your search query q would be:<br/></p>     <ul>       <li>q=from:%2B61437085284</li>     </ul>     <p>You can use the <a href=\"https://www.urlencoder.org/\" target=\"_blank\">URL encoder</a> to encode the text. If a character is not an alphanumeric character (A-Z, a-z, 0-9), it is typically either reserved or unsafe and should be encoded.</p>   </div> </div>
    String orderBy = "date:asc"; // String | Specifies the field and order to sort the results by. The value is composed of the field name followed by a colon and the sort direction (_asc_ for ascending or _desc_ for descending).  The default sort order is by _date_ in ascending order. You can use the following fields:    - _date_   - _username_   - _from_    - _to_   - _status_   - _body_  For example, if you want to order by the most recently sent SMS, you should sort by date in descending order. The query would look like this:    `order_by=date:desc`
    Integer dateFrom = 56; // Integer | Start date to filter results. It should be in <a href=\"http://help.clicksend.com/what-is-a-unix-timestamp\" target=\"_blank\">Unix format</a>.
    Integer dateTo = 56; // Integer | End date to filter results. It should be in <a href=\"http://help.clicksend.com/what-is-a-unix-timestamp\" target=\"_blank\">Unix format</a>.
    try {
      ViewSmsHistory result = apiInstance.viewSmsHistory(contentType, page, limit, q, orderBy, dateFrom, dateTo);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SmsOtherApi#viewSmsHistory");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **contentType** | **String**|  | [optional] |
| **page** | **Integer**| The page number to retrieve. Use this parameter to navigate through the [pagination](/#pagination) results. The default value is 1. | [optional] [default to 1] |
| **limit** | **Integer**| The number of items to return per page. This parameter controls the size of each page of results. The default value is 15. | [optional] [default to 15] |
| **q** | **String**| Allows filtering of results based on your search criteria. The query should be in the format &#x60;field_name:value&#x60;.  1. **Field Name**: The field within the SMS history you want to filter by. You can use the following fields:          - _Status_: The status of the SMS. Available values for status are: Queued, Completed, Scheduled, WaitApproval, Failed, Cancelled, CancelledAfterReview, Received, Sent.              - _To_: The recipient of the SMS.              - _from_: The sender of the SMS.              - _subaccount_id_: The sub-account identifier.              - _message_id_: The ID of your SMS.          2. **Value**: The text or keyword you&#39;re searching for within the specified field. If left empty after the colon, the filter will look for all templates with any value in the **Field Name**.             For example, if you are searching for a SMS with the status of Scheduled, the final query would look like this:    &#x60;q&#x3D;status:Scheduled&#x60;  &lt;div class&#x3D;\&quot;info-box\&quot;&gt;   &lt;h4&gt;&lt;i class&#x3D;\&quot;fas fa-info-circle\&quot;&gt;&lt;/i&gt; Note:&lt;/h4&gt;   &lt;div&gt;    &lt;p&gt;Some characters have to be encoded. For example, if you are searching for SMS sent from the phone number +61437085284, your search query q would be:&lt;br/&gt;&lt;/p&gt;     &lt;ul&gt;       &lt;li&gt;q&#x3D;from:%2B61437085284&lt;/li&gt;     &lt;/ul&gt;     &lt;p&gt;You can use the &lt;a href&#x3D;\&quot;https://www.urlencoder.org/\&quot; target&#x3D;\&quot;_blank\&quot;&gt;URL encoder&lt;/a&gt; to encode the text. If a character is not an alphanumeric character (A-Z, a-z, 0-9), it is typically either reserved or unsafe and should be encoded.&lt;/p&gt;   &lt;/div&gt; &lt;/div&gt; | [optional] [default to field_name] |
| **orderBy** | **String**| Specifies the field and order to sort the results by. The value is composed of the field name followed by a colon and the sort direction (_asc_ for ascending or _desc_ for descending).  The default sort order is by _date_ in ascending order. You can use the following fields:    - _date_   - _username_   - _from_    - _to_   - _status_   - _body_  For example, if you want to order by the most recently sent SMS, you should sort by date in descending order. The query would look like this:    &#x60;order_by&#x3D;date:desc&#x60; | [optional] [default to date:asc] |
| **dateFrom** | **Integer**| Start date to filter results. It should be in &lt;a href&#x3D;\&quot;http://help.clicksend.com/what-is-a-unix-timestamp\&quot; target&#x3D;\&quot;_blank\&quot;&gt;Unix format&lt;/a&gt;. | [optional] |
| **dateTo** | **Integer**| End date to filter results. It should be in &lt;a href&#x3D;\&quot;http://help.clicksend.com/what-is-a-unix-timestamp\&quot; target&#x3D;\&quot;_blank\&quot;&gt;Unix format&lt;/a&gt;. | [optional] |

### Return type

[**ViewSmsHistory**](ViewSmsHistory.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewSmsInboundAutomation"></a>
# **viewSmsInboundAutomation**
> ViewSmsInboundAutomation viewSmsInboundAutomation(inboundRuleId, contentType)

View SMS Inbound Automation

_Get specific inbound sms automation_  Get specific inbound sms automation  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | inbound_rule_id | path | integer(int32) | true | Inbound rule id |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.SmsOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    SmsOtherApi apiInstance = new SmsOtherApi(defaultClient);
    String inboundRuleId = "inboundRuleId_example"; // String | 
    String contentType = "application/json"; // String | 
    try {
      ViewSmsInboundAutomation result = apiInstance.viewSmsInboundAutomation(inboundRuleId, contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SmsOtherApi#viewSmsInboundAutomation");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **inboundRuleId** | **String**|  | |
| **contentType** | **String**|  | [optional] |

### Return type

[**ViewSmsInboundAutomation**](ViewSmsInboundAutomation.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewSmsInboundAutomations"></a>
# **viewSmsInboundAutomations**
> ViewSmsInboundAutomations viewSmsInboundAutomations(contentType)

View SMS Inbound Automations

_Get all inbound sms automations_  Get all inbound sms automations  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | page | query | integer(int32) | false | Page number | | limit | query | integer(int32) | false | Number of records per page |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.SmsOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    SmsOtherApi apiInstance = new SmsOtherApi(defaultClient);
    String contentType = "application/json"; // String | 
    try {
      ViewSmsInboundAutomations result = apiInstance.viewSmsInboundAutomations(contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SmsOtherApi#viewSmsInboundAutomations");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **contentType** | **String**|  | [optional] |

### Return type

[**ViewSmsInboundAutomations**](ViewSmsInboundAutomations.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewSmsReceipts"></a>
# **viewSmsReceipts**
> ViewSmsReceipts viewSmsReceipts(contentType, page, limit)

View SMS Receipts

Use this endpoint to retrieve &lt;a href&#x3D;\&quot;https://help.clicksend.com/article/49eq1qdcui-how-do-i-receive-sms-delivery-receipts-delivery-status-updates\&quot; target&#x3D;\&quot;_blank\&quot;&gt;SMS delivery receipts&lt;/a&gt; sent by your recipient.  To be able to view receipts, add a &lt;a href&#x3D;\&quot;https://help.clicksend.com/en/articles/42317-delivery-notifications-reports\&quot; target&#x3D;\&quot;_blank\&quot;&gt;delivery report&lt;/a&gt; rule with the Action set to **POLL** in the Dashboard, or use the [**Create SMS Delivery Receipt Rule**](/automations/sms/other/create-sms-delivery-receipt-rule) endpoint.  Control [pagination](/#pagination) with the _page_ and _limit_ query parameters to specify the page of results and the number of items returned.

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.SmsOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    SmsOtherApi apiInstance = new SmsOtherApi(defaultClient);
    String contentType = "application/json"; // String | 
    Integer page = 1; // Integer | The page number to retrieve. Use this parameter to navigate through the [pagination](/#pagination) results. The default value is 1.
    Integer limit = 15; // Integer | The number of items to return per page. This parameter controls the size of each page of results. The default value is 15.
    try {
      ViewSmsReceipts result = apiInstance.viewSmsReceipts(contentType, page, limit);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SmsOtherApi#viewSmsReceipts");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **contentType** | **String**|  | [optional] |
| **page** | **Integer**| The page number to retrieve. Use this parameter to navigate through the [pagination](/#pagination) results. The default value is 1. | [optional] [default to 1] |
| **limit** | **Integer**| The number of items to return per page. This parameter controls the size of each page of results. The default value is 15. | [optional] [default to 15] |

### Return type

[**ViewSmsReceipts**](ViewSmsReceipts.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewSmsTemplates"></a>
# **viewSmsTemplates**
> ViewSmsTemplates viewSmsTemplates(contentType, page, limit, q, orderBy)

View SMS Templates

Use this endpoint to retrieve &lt;a href&#x3D;\&quot;https://help.clicksend.com/article/9z9uloaz8y-sms-templates-for-different-industries\&quot; target&#x3D;\&quot;_blank\&quot;&gt;SMS templates&lt;/a&gt;. You can filter the SMS templates result using the query parameters.

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.SmsOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    SmsOtherApi apiInstance = new SmsOtherApi(defaultClient);
    String contentType = "application/json"; // String | 
    Integer page = 1; // Integer | The page number to retrieve. Use this parameter to navigate through the [pagination](/#pagination) results. The default value is 1.
    Integer limit = 15; // Integer | The number of items to return per page. This parameter controls the size of each page of results. The default value is 15.
    String q = "field_name"; // String | Allows filtering of results based on your search criteria. The query should be in the format `field_name:value`.  1. **Field Name**: The field within the SMS history you want to filter by. You can use the following fields:    - _template_id_ : The ID of the template   - _template_name_ : The name of the template   - _body_ : The body content of the template.          2. **Value**: The text or keyword you're searching for within the specified field. If left empty after the colon, the filter will look for all templates with any value in the **Field Name**.      For example, if you are searching for the template with the name of _sample_name_, the final query would look like this:     `q=template_name:sample_name`  <div class=\"info-box\">   <h4><i class=\"fas fa-info-circle\"></i> Note:</h4>   <div>    <p>Some characters have to be encoded. For example, if you are searching for SMS sent from the phone number +61437085284, your search query q would be:<br/></p>     <ul>       <li>q=from:%2B61437085284</li>     </ul>     <p>You can use the <a href=\"https://www.urlencoder.org/\" target=\"_blank\">URL encoder</a> to encode the text. If a character is not an alphanumeric character (A-Z, a-z, 0-9), it is typically either reserved or unsafe and should be encoded.</p>   </div> </div>
    String orderBy = "template_id:asc"; // String | Specifies the field and order to sort the results by.  The value is composed of the field name followed by a colon and the sort direction (_asc_ for ascending or _desc_ for descending).  The default sort order is by _template_id_ in ascending order. You can use the following fields:      - _template_id_ : The ID of the Template - _template_name_ : The name of the Template - _body_ : The body content of the Template  For example, if you want to order by the _template_id_ in descending order, the query would look like this:    `order_by=template_id:desc`
    try {
      ViewSmsTemplates result = apiInstance.viewSmsTemplates(contentType, page, limit, q, orderBy);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SmsOtherApi#viewSmsTemplates");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **contentType** | **String**|  | [optional] |
| **page** | **Integer**| The page number to retrieve. Use this parameter to navigate through the [pagination](/#pagination) results. The default value is 1. | [optional] [default to 1] |
| **limit** | **Integer**| The number of items to return per page. This parameter controls the size of each page of results. The default value is 15. | [optional] [default to 15] |
| **q** | **String**| Allows filtering of results based on your search criteria. The query should be in the format &#x60;field_name:value&#x60;.  1. **Field Name**: The field within the SMS history you want to filter by. You can use the following fields:    - _template_id_ : The ID of the template   - _template_name_ : The name of the template   - _body_ : The body content of the template.          2. **Value**: The text or keyword you&#39;re searching for within the specified field. If left empty after the colon, the filter will look for all templates with any value in the **Field Name**.      For example, if you are searching for the template with the name of _sample_name_, the final query would look like this:     &#x60;q&#x3D;template_name:sample_name&#x60;  &lt;div class&#x3D;\&quot;info-box\&quot;&gt;   &lt;h4&gt;&lt;i class&#x3D;\&quot;fas fa-info-circle\&quot;&gt;&lt;/i&gt; Note:&lt;/h4&gt;   &lt;div&gt;    &lt;p&gt;Some characters have to be encoded. For example, if you are searching for SMS sent from the phone number +61437085284, your search query q would be:&lt;br/&gt;&lt;/p&gt;     &lt;ul&gt;       &lt;li&gt;q&#x3D;from:%2B61437085284&lt;/li&gt;     &lt;/ul&gt;     &lt;p&gt;You can use the &lt;a href&#x3D;\&quot;https://www.urlencoder.org/\&quot; target&#x3D;\&quot;_blank\&quot;&gt;URL encoder&lt;/a&gt; to encode the text. If a character is not an alphanumeric character (A-Z, a-z, 0-9), it is typically either reserved or unsafe and should be encoded.&lt;/p&gt;   &lt;/div&gt; &lt;/div&gt; | [optional] [default to field_name] |
| **orderBy** | **String**| Specifies the field and order to sort the results by.  The value is composed of the field name followed by a colon and the sort direction (_asc_ for ascending or _desc_ for descending).  The default sort order is by _template_id_ in ascending order. You can use the following fields:      - _template_id_ : The ID of the Template - _template_name_ : The name of the Template - _body_ : The body content of the Template  For example, if you want to order by the _template_id_ in descending order, the query would look like this:    &#x60;order_by&#x3D;template_id:desc&#x60; | [optional] [default to template_id:asc] |

### Return type

[**ViewSmsTemplates**](ViewSmsTemplates.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewSpecificSmsReceipt"></a>
# **viewSpecificSmsReceipt**
> ViewSpecificSmsReceipt viewSpecificSmsReceipt(messageId, contentType)

View Specific SMS Receipt

Use this endpoint to retrieve a specific &lt;a href&#x3D;\&quot;https://help.clicksend.com/article/49eq1qdcui-how-do-i-receive-sms-delivery-receipts-delivery-status-updates\&quot; target&#x3D;\&quot;_blank\&quot;&gt;SMS delivery receipt&lt;/a&gt;, including those that have been marked as read. When you send an SMS, a delivery receipt is generated and can be received.  This endpoint enables you to retrieve those receipts.

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.SmsOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    SmsOtherApi apiInstance = new SmsOtherApi(defaultClient);
    String messageId = "messageId_example"; // String | The _message_id_ of the SMS delivery receipt to retrieve
    String contentType = "application/json"; // String | 
    try {
      ViewSpecificSmsReceipt result = apiInstance.viewSpecificSmsReceipt(messageId, contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SmsOtherApi#viewSpecificSmsReceipt");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **messageId** | **String**| The _message_id_ of the SMS delivery receipt to retrieve | |
| **contentType** | **String**|  | [optional] |

### Return type

[**ViewSpecificSmsReceipt**](ViewSpecificSmsReceipt.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

