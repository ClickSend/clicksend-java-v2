# VoiceOtherApi

All URIs are relative to *https://rest.clicksend.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createVoiceDeliveryReceiptRule**](VoiceOtherApi.md#createVoiceDeliveryReceiptRule) | **POST** /v3/automations/voice/receipts | Create Voice Delivery Receipt Rule |
| [**deleteVoiceDeliveryReceiptRule**](VoiceOtherApi.md#deleteVoiceDeliveryReceiptRule) | **DELETE** /v3/automations/voice/receipts/{receipt_rule_id} | Delete Voice Delivery Receipt Rule |
| [**updateVoiceDeliveryReceiptRule**](VoiceOtherApi.md#updateVoiceDeliveryReceiptRule) | **PUT** /v3/automations/voice/receipts/{receipt_rule_id} | Update Voice Delivery Receipt Rule |
| [**viewVoiceDeliveryReceiptRule**](VoiceOtherApi.md#viewVoiceDeliveryReceiptRule) | **GET** /v3/automations/voice/receipts/{receipt_rule_id} | View Voice Delivery Receipt Rule |
| [**viewVoiceDeliveryReceiptRules**](VoiceOtherApi.md#viewVoiceDeliveryReceiptRules) | **GET** /v3/automations/voice/receipts | View Voice Delivery Receipt Rules |


<a id="createVoiceDeliveryReceiptRule"></a>
# **createVoiceDeliveryReceiptRule**
> CreateVoiceDeliveryReceiptRule createVoiceDeliveryReceiptRule(contentType, createSmsDeliveryReceiptRuleRequest)

Create Voice Delivery Receipt Rule

_Create voice delivery receipt automations_  Create voice delivery receipt automations  ### Properties  | Name | Type | Required | Restrictions | Description | | --- | --- | --- | --- | --- | | rule_name | string | true | none | Rule Name. | | match_type | number | true | none | Match Type. 0&#x3D;All reports. | | action | string | true | none | Action to be taken (AUTO_REPLY, EMAIL_USER, EMAIL_FIXED, URL, SMS, POLL, GROUP_SMS, MOVE_CONTACT, CREATE_CONTACT, CREATE_CONTACT_PLUS_EMAIL, CREATE_CONTACT_PLUS_NAME_EMAIL CREATE_CONTACT_PLUS_NAME, SMPP, NONE). | | action_address | string | true | none | Action address. | | enabled | number | true | none | Enabled: Disabled&#x3D;0 or Enabled&#x3D;1. |  Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.  &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.VoiceOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    VoiceOtherApi apiInstance = new VoiceOtherApi(defaultClient);
    String contentType = "application/json"; // String | 
    CreateSmsDeliveryReceiptRuleRequest createSmsDeliveryReceiptRuleRequest = new CreateSmsDeliveryReceiptRuleRequest(); // CreateSmsDeliveryReceiptRuleRequest | 
    try {
      CreateVoiceDeliveryReceiptRule result = apiInstance.createVoiceDeliveryReceiptRule(contentType, createSmsDeliveryReceiptRuleRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling VoiceOtherApi#createVoiceDeliveryReceiptRule");
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

[**CreateVoiceDeliveryReceiptRule**](CreateVoiceDeliveryReceiptRule.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="deleteVoiceDeliveryReceiptRule"></a>
# **deleteVoiceDeliveryReceiptRule**
> DeleteVoiceDeliveryReceiptRule deleteVoiceDeliveryReceiptRule(receiptRuleId, contentType)

Delete Voice Delivery Receipt Rule

_Delete voice delivery receipt automation_  Delete voice delivery receipt automation  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | receipt_rule_id | path | integer(int32) | true | Receipt rule id |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.VoiceOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    VoiceOtherApi apiInstance = new VoiceOtherApi(defaultClient);
    String receiptRuleId = "receiptRuleId_example"; // String | 
    String contentType = "application/json"; // String | 
    try {
      DeleteVoiceDeliveryReceiptRule result = apiInstance.deleteVoiceDeliveryReceiptRule(receiptRuleId, contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling VoiceOtherApi#deleteVoiceDeliveryReceiptRule");
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

[**DeleteVoiceDeliveryReceiptRule**](DeleteVoiceDeliveryReceiptRule.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="updateVoiceDeliveryReceiptRule"></a>
# **updateVoiceDeliveryReceiptRule**
> UpdateVoiceDeliveryReceiptRule updateVoiceDeliveryReceiptRule(receiptRuleId, contentType, createSmsDeliveryReceiptRuleRequest)

Update Voice Delivery Receipt Rule

_Update voice delivery receipt automation_  Update voice delivery receipt automation  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | receipt_rule_id | path | integer(int32) | true | Receipt rule id |  ### Properties  | Name | Type | Required | Restrictions | Description | | --- | --- | --- | --- | --- | | rule_name | string | true | none | Rule Name. | | match_type | number | true | none | Match Type. 0&#x3D;All reports. | | action | string | true | none | Action to be taken (AUTO_REPLY, EMAIL_USER, EMAIL_FIXED, URL, SMS, POLL, GROUP_SMS, MOVE_CONTACT, CREATE_CONTACT, CREATE_CONTACT_PLUS_EMAIL, CREATE_CONTACT_PLUS_NAME_EMAIL CREATE_CONTACT_PLUS_NAME, SMPP, NONE). | | action_address | string | true | none | Action address. | | enabled | number | true | none | Enabled: Disabled&#x3D;0 or Enabled&#x3D;1. |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.VoiceOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    VoiceOtherApi apiInstance = new VoiceOtherApi(defaultClient);
    String receiptRuleId = "receiptRuleId_example"; // String | 
    String contentType = "application/json"; // String | 
    CreateSmsDeliveryReceiptRuleRequest createSmsDeliveryReceiptRuleRequest = new CreateSmsDeliveryReceiptRuleRequest(); // CreateSmsDeliveryReceiptRuleRequest | 
    try {
      UpdateVoiceDeliveryReceiptRule result = apiInstance.updateVoiceDeliveryReceiptRule(receiptRuleId, contentType, createSmsDeliveryReceiptRuleRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling VoiceOtherApi#updateVoiceDeliveryReceiptRule");
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

[**UpdateVoiceDeliveryReceiptRule**](UpdateVoiceDeliveryReceiptRule.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewVoiceDeliveryReceiptRule"></a>
# **viewVoiceDeliveryReceiptRule**
> ViewVoiceDeliveryReceiptRule viewVoiceDeliveryReceiptRule(receiptRuleId, contentType)

View Voice Delivery Receipt Rule

_Get specific voice delivery receipt automation_  Get specific voice delivery receipt automation  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | receipt_rule_id | path | integer(int32) | true | Receipt rule id |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.VoiceOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    VoiceOtherApi apiInstance = new VoiceOtherApi(defaultClient);
    String receiptRuleId = "receiptRuleId_example"; // String | 
    String contentType = "application/json"; // String | 
    try {
      ViewVoiceDeliveryReceiptRule result = apiInstance.viewVoiceDeliveryReceiptRule(receiptRuleId, contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling VoiceOtherApi#viewVoiceDeliveryReceiptRule");
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

[**ViewVoiceDeliveryReceiptRule**](ViewVoiceDeliveryReceiptRule.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewVoiceDeliveryReceiptRules"></a>
# **viewVoiceDeliveryReceiptRules**
> ViewVoiceDeliveryReceiptRules viewVoiceDeliveryReceiptRules(contentType)

View Voice Delivery Receipt Rules

_Get all voice delivery receipt automations_  Get all voice delivery receipt automations  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | page | query | integer(int32) | false | Page number | | limit | query | integer(int32) | false | Number of records per page |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.VoiceOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    VoiceOtherApi apiInstance = new VoiceOtherApi(defaultClient);
    String contentType = "application/json"; // String | 
    try {
      ViewVoiceDeliveryReceiptRules result = apiInstance.viewVoiceDeliveryReceiptRules(contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling VoiceOtherApi#viewVoiceDeliveryReceiptRules");
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

[**ViewVoiceDeliveryReceiptRules**](ViewVoiceDeliveryReceiptRules.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

