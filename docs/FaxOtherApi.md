# FaxOtherApi

All URIs are relative to *https://rest.clicksend.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**calculateFaxPrice**](FaxOtherApi.md#calculateFaxPrice) | **POST** /v3/fax/price | Calculate Fax Price |
| [**createFaxDeliveryReceiptRule**](FaxOtherApi.md#createFaxDeliveryReceiptRule) | **POST** /v3/automations/fax/receipts | Create FAX Delivery Receipt Rule |
| [**createFaxInboundRule**](FaxOtherApi.md#createFaxInboundRule) | **POST** /v3/automations/fax/inbound | Create Fax Inbound Rule |
| [**deleteFaxDeliveryReceiptRule**](FaxOtherApi.md#deleteFaxDeliveryReceiptRule) | **DELETE** /v3/automations/fax/receipts/{receipt_rule_id} | Delete FAX Delivery Receipt Rule |
| [**deleteFaxInboundRule**](FaxOtherApi.md#deleteFaxInboundRule) | **DELETE** /v3/automations/fax/inbound/{inbound_rule_id} | Delete Fax Inbound Rule |
| [**sendFax**](FaxOtherApi.md#sendFax) | **POST** /v3/fax/send | Send Fax |
| [**updateFaxDeliveryReceiptRule**](FaxOtherApi.md#updateFaxDeliveryReceiptRule) | **PUT** /v3/automations/fax/receipts/{receipt_rule_id} | Update FAX Delivery Receipt Rule |
| [**updateFaxInboundRule**](FaxOtherApi.md#updateFaxInboundRule) | **PUT** /v3/automations/fax/inbound/{inbound_rule_id} | Update Fax Inbound Rule |
| [**viewFaxDeliveryReceiptRule**](FaxOtherApi.md#viewFaxDeliveryReceiptRule) | **GET** /v3/automations/fax/receipts/{receipt_rule_id} | View FAX Delivery Receipt Rule |
| [**viewFaxDeliveryReceiptRules**](FaxOtherApi.md#viewFaxDeliveryReceiptRules) | **GET** /v3/automations/fax/receipts | View FAX Delivery Receipt Rules |
| [**viewFaxHistory**](FaxOtherApi.md#viewFaxHistory) | **GET** /v3/fax/history | View Fax History |
| [**viewFaxInboundRule**](FaxOtherApi.md#viewFaxInboundRule) | **GET** /v3/automations/fax/inbound/{inbound_rule_id} | View Fax Inbound Rule |
| [**viewFaxInboundRules**](FaxOtherApi.md#viewFaxInboundRules) | **GET** /v3/automations/fax/inbound | View Fax Inbound Rules |
| [**viewFaxReceipts**](FaxOtherApi.md#viewFaxReceipts) | **GET** /v3/fax/receipts | View Fax Receipts |
| [**viewSpecificFaxReceipt**](FaxOtherApi.md#viewSpecificFaxReceipt) | **GET** /v3/fax/receipts/{message_id} | View Specific Fax Receipt |


<a id="calculateFaxPrice"></a>
# **calculateFaxPrice**
> CalculateFaxPrice calculateFaxPrice(contentType, calculateFaxPriceRequest)

Calculate Fax Price

_Calculate Total Price for Fax Messages sent_  ### Properties  | Name | Type | Required | Restrictions | Description | | --- | --- | --- | --- | --- | | file_url | string | true | none | URL of file to send | | source | string | true | none | Your method of sending e.g. &#39;wordpress&#39;, &#39;php&#39;, &#39;c#&#39;. | | to | string | true | none | Recipient fax number in [E.164](https://en.wikipedia.org/wiki/E.164) format. | | list_id | integer(int32) | false | none | Your list ID if sending to a whole list. Can be used instead of &#39;to&#39;. | | from | string | true | [yes](http://help.clicksend.com/SMS/what-is-a-sender-id-or-sender-number) | Your sender id. Must be a valid fax number. | | schedule | integer(int32) | false | none | Leave blank for immediate delivery. Your schedule time in unix format [http://help.clicksend.com/what-is-a-unix-timestamp](http://help.clicksend.com/what-is-a-unix-timestamp) | | custom_string | string | false | none | Your reference. Will be passed back with all replies and delivery reports. | | country | string | false | none | ISO alpha-2 character country code e.g. &#39;US&#39;, we use this to format the recipient number if it&#39;s not in international format. | | from_email | string | false | none | An email address where the reply should be emailed to. |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.FaxOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    FaxOtherApi apiInstance = new FaxOtherApi(defaultClient);
    String contentType = "application/json"; // String | 
    CalculateFaxPriceRequest calculateFaxPriceRequest = new CalculateFaxPriceRequest(); // CalculateFaxPriceRequest | 
    try {
      CalculateFaxPrice result = apiInstance.calculateFaxPrice(contentType, calculateFaxPriceRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling FaxOtherApi#calculateFaxPrice");
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
| **calculateFaxPriceRequest** | [**CalculateFaxPriceRequest**](CalculateFaxPriceRequest.md)|  | [optional] |

### Return type

[**CalculateFaxPrice**](CalculateFaxPrice.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="createFaxDeliveryReceiptRule"></a>
# **createFaxDeliveryReceiptRule**
> CreateFaxDeliveryReceiptRule createFaxDeliveryReceiptRule(contentType, createFaxDeliveryReceiptRuleRequest)

Create FAX Delivery Receipt Rule

_Create fax delivery receipt automations_  Create fax delivery receipt automations  ### Properties  | Name | Type | Required | Restrictions | Description | | --- | --- | --- | --- | --- | | rule_name | string | true | none | Rule Name. | | match_type | number | true | none | Match Type. 0&#x3D;All reports. | | action | string | true | none | Action to be taken (AUTO_REPLY, EMAIL_USER, EMAIL_FIXED, URL, SMS, POLL, GROUP_SMS, MOVE_CONTACT, CREATE_CONTACT, CREATE_CONTACT_PLUS_EMAIL, CREATE_CONTACT_PLUS_NAME_EMAIL CREATE_CONTACT_PLUS_NAME, SMPP, NONE). | | action_address | string | true | none | Action address. | | enabled | number | true | none | Enabled: Disabled&#x3D;0 or Enabled&#x3D;1. |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.FaxOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    FaxOtherApi apiInstance = new FaxOtherApi(defaultClient);
    String contentType = "application/json"; // String | 
    CreateFaxDeliveryReceiptRuleRequest createFaxDeliveryReceiptRuleRequest = new CreateFaxDeliveryReceiptRuleRequest(); // CreateFaxDeliveryReceiptRuleRequest | 
    try {
      CreateFaxDeliveryReceiptRule result = apiInstance.createFaxDeliveryReceiptRule(contentType, createFaxDeliveryReceiptRuleRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling FaxOtherApi#createFaxDeliveryReceiptRule");
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
| **createFaxDeliveryReceiptRuleRequest** | [**CreateFaxDeliveryReceiptRuleRequest**](CreateFaxDeliveryReceiptRuleRequest.md)|  | [optional] |

### Return type

[**CreateFaxDeliveryReceiptRule**](CreateFaxDeliveryReceiptRule.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="createFaxInboundRule"></a>
# **createFaxInboundRule**
> CreateFaxInboundRule createFaxInboundRule(contentType, createFaxInboundRuleRequest)

Create Fax Inbound Rule

_Create new inbound fax automation_  Create new inbound fax automation  ### Properties  | Name | Type | Required | Restrictions | Description | | --- | --- | --- | --- | --- | | dedicated_number | string | true | none | Dedicated Number. Can be &#39;\\*&#39; to apply to all numbers. | | rule_name | string | true | none | Rule Name. | | action | string | true | none | Action to be taken (AUTO_REPLY, EMAIL_USER, EMAIL_FIXED, URL, SMS, POLL, GROUP_SMS, MOVE_CONTACT, CREATE_CONTACT, CREATE_CONTACT_PLUS_EMAIL, CREATE_CONTACT_PLUS_NAME_EMAIL CREATE_CONTACT_PLUS_NAME, SMPP, NONE). | | action_address | string | true | none | Action address. | | enabled | number | true | none | Enabled: Disabled&#x3D;0 or Enabled&#x3D;1. |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.FaxOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    FaxOtherApi apiInstance = new FaxOtherApi(defaultClient);
    String contentType = "application/json"; // String | 
    CreateFaxInboundRuleRequest createFaxInboundRuleRequest = new CreateFaxInboundRuleRequest(); // CreateFaxInboundRuleRequest | 
    try {
      CreateFaxInboundRule result = apiInstance.createFaxInboundRule(contentType, createFaxInboundRuleRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling FaxOtherApi#createFaxInboundRule");
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
| **createFaxInboundRuleRequest** | [**CreateFaxInboundRuleRequest**](CreateFaxInboundRuleRequest.md)|  | [optional] |

### Return type

[**CreateFaxInboundRule**](CreateFaxInboundRule.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="deleteFaxDeliveryReceiptRule"></a>
# **deleteFaxDeliveryReceiptRule**
> DeleteFaxDeliveryReceiptRule deleteFaxDeliveryReceiptRule(receiptRuleId, contentType)

Delete FAX Delivery Receipt Rule

_Delete fax delivery receipt automation_  Delete fax delivery receipt automation  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | receipt_rule_id | path | integer(int32) | true | Receipt rule id |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.FaxOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    FaxOtherApi apiInstance = new FaxOtherApi(defaultClient);
    String receiptRuleId = "receiptRuleId_example"; // String | 
    String contentType = "application/json"; // String | 
    try {
      DeleteFaxDeliveryReceiptRule result = apiInstance.deleteFaxDeliveryReceiptRule(receiptRuleId, contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling FaxOtherApi#deleteFaxDeliveryReceiptRule");
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

[**DeleteFaxDeliveryReceiptRule**](DeleteFaxDeliveryReceiptRule.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="deleteFaxInboundRule"></a>
# **deleteFaxInboundRule**
> DeleteFaxInboundRule deleteFaxInboundRule(inboundRuleId, contentType)

Delete Fax Inbound Rule

_Delete inbound fax automation_  Delete inbound fax automation  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | inbound_rule_id | path | integer(int32) | true | Inbound rule id |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.FaxOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    FaxOtherApi apiInstance = new FaxOtherApi(defaultClient);
    String inboundRuleId = "inboundRuleId_example"; // String | 
    String contentType = "application/json"; // String | 
    try {
      DeleteFaxInboundRule result = apiInstance.deleteFaxInboundRule(inboundRuleId, contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling FaxOtherApi#deleteFaxInboundRule");
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

[**DeleteFaxInboundRule**](DeleteFaxInboundRule.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="sendFax"></a>
# **sendFax**
> SendFax sendFax(contentType, sendFaxRequest)

Send Fax

### **Supported File Types**  - Supported file types are listed below. If you need to convert a file to a supported format, it can be first passed to our uploads endpoint: &#x60;/uploads?convert&#x3D;fax&#x60; - This will return a URL to the converted pdf file that can be used in the /fax/send endpoint. - Contact us to add support for any other file type.       ### Documents  | File type | Required to be passed to uploads endpoint first? | | --- | --- | | pdf | No | | docx | Yes | | doc | Yes | | rtf | Yes |  _Send a fax using supplied supported file-types._  ### **Letter File Options**  ### Use existing URL  With this option, you can use an existing URL to a &#x60;pdf&#x60; document. For example, you might generate the &#x60;pdf&#x60; on your server.  When using an existing url make sure that it is publicly accessible as it will not work if it is private.  ### Upload File to Our Server  With this option, you can use the [/uploads](/#upload-media-file) endpoint to upload the document. The &#x60;/uploads&#x60; endpoint returns a URL that can be used in the &#x60;/fax/send&#x60; endpoint.  ### Properties  | Name | Type | Required | Restrictions | Description | | --- | --- | --- | --- | --- | | file_url | string | true | none | URL of file to send | | source | string | true | none | Your method of sending e.g. &#39;wordpress&#39;, &#39;php&#39;, &#39;c#&#39;. | | to | string | true | none | Recipient fax number in [E.164](https://en.wikipedia.org/wiki/E.164) format. | | list_id | integer(int32) | false | none | Your list ID if sending to a whole list. Can be used instead of &#39;to&#39;. | | from | string | true | [yes](http://help.clicksend.com/SMS/what-is-a-sender-id-or-sender-number) | Your sender id. Must be a valid fax number. | | schedule | integer(int32) | false | none | Leave blank for immediate delivery. Your schedule time in unix format [http://help.clicksend.com/what-is-a-unix-timestamp](http://help.clicksend.com/what-is-a-unix-timestamp) | | custom_string | string | false | none | Your reference. Will be passed back with all replies and delivery reports. | | country | string | false | none | ISO alpha-2 character country code e.g. &#39;US&#39;, we use this to format the recipient number if it&#39;s not in international format. | | from_email | string | false | none | An email address where the reply should be emailed to. |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.FaxOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    FaxOtherApi apiInstance = new FaxOtherApi(defaultClient);
    String contentType = "application/json"; // String | 
    SendFaxRequest sendFaxRequest = new SendFaxRequest(); // SendFaxRequest | 
    try {
      SendFax result = apiInstance.sendFax(contentType, sendFaxRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling FaxOtherApi#sendFax");
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
| **sendFaxRequest** | [**SendFaxRequest**](SendFaxRequest.md)|  | [optional] |

### Return type

[**SendFax**](SendFax.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="updateFaxDeliveryReceiptRule"></a>
# **updateFaxDeliveryReceiptRule**
> UpdateFaxDeliveryReceiptRule updateFaxDeliveryReceiptRule(receiptRuleId, contentType, updateFaxDeliveryReceiptRuleRequest)

Update FAX Delivery Receipt Rule

_Update fax delivery receipt automation_  Update fax delivery receipt automation  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | receipt_rule_id | path | integer(int32) | true | Receipt rule id |  ### Properties  | Name | Type | Required | Restrictions | Description | | --- | --- | --- | --- | --- | | rule_name | string | true | none | Rule Name. | | match_type | number | true | none | Match Type. 0&#x3D;All reports. | | action | string | true | none | Action to be taken (AUTO_REPLY, EMAIL_USER, EMAIL_FIXED, URL, SMS, POLL, GROUP_SMS, MOVE_CONTACT, CREATE_CONTACT, CREATE_CONTACT_PLUS_EMAIL, CREATE_CONTACT_PLUS_NAME_EMAIL CREATE_CONTACT_PLUS_NAME, SMPP, NONE). | | action_address | string | true | none | Action address. | | enabled | number | true | none | Enabled: Disabled&#x3D;0 or Enabled&#x3D;1. |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.FaxOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    FaxOtherApi apiInstance = new FaxOtherApi(defaultClient);
    String receiptRuleId = "receiptRuleId_example"; // String | 
    String contentType = "application/json"; // String | 
    UpdateFaxDeliveryReceiptRuleRequest updateFaxDeliveryReceiptRuleRequest = new UpdateFaxDeliveryReceiptRuleRequest(); // UpdateFaxDeliveryReceiptRuleRequest | 
    try {
      UpdateFaxDeliveryReceiptRule result = apiInstance.updateFaxDeliveryReceiptRule(receiptRuleId, contentType, updateFaxDeliveryReceiptRuleRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling FaxOtherApi#updateFaxDeliveryReceiptRule");
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
| **updateFaxDeliveryReceiptRuleRequest** | [**UpdateFaxDeliveryReceiptRuleRequest**](UpdateFaxDeliveryReceiptRuleRequest.md)|  | [optional] |

### Return type

[**UpdateFaxDeliveryReceiptRule**](UpdateFaxDeliveryReceiptRule.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="updateFaxInboundRule"></a>
# **updateFaxInboundRule**
> UpdateFaxInboundRule updateFaxInboundRule(inboundRuleId, contentType, createFaxInboundRuleRequest)

Update Fax Inbound Rule

_Update inbound fax automation_  Update inbound fax automation  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | inbound_rule_id | path | integer(int32) | true | Inbound rule id |  ### Properties  | Name | Type | Required | Restrictions | Description | | --- | --- | --- | --- | --- | | dedicated_number | string | true | none | Dedicated Number. Can be &#39;\\*&#39; to apply to all numbers. | | rule_name | string | true | none | Rule Name. | | action | string | true | none | Action to be taken (AUTO_REPLY, EMAIL_USER, EMAIL_FIXED, URL, SMS, POLL, GROUP_SMS, MOVE_CONTACT, CREATE_CONTACT, CREATE_CONTACT_PLUS_EMAIL, CREATE_CONTACT_PLUS_NAME_EMAIL CREATE_CONTACT_PLUS_NAME, SMPP, NONE). | | action_address | string | true | none | Action address. | | enabled | number | true | none | Enabled: Disabled&#x3D;0 or Enabled&#x3D;1. |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.FaxOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    FaxOtherApi apiInstance = new FaxOtherApi(defaultClient);
    String inboundRuleId = "inboundRuleId_example"; // String | 
    String contentType = "application/json"; // String | 
    CreateFaxInboundRuleRequest createFaxInboundRuleRequest = new CreateFaxInboundRuleRequest(); // CreateFaxInboundRuleRequest | 
    try {
      UpdateFaxInboundRule result = apiInstance.updateFaxInboundRule(inboundRuleId, contentType, createFaxInboundRuleRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling FaxOtherApi#updateFaxInboundRule");
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
| **createFaxInboundRuleRequest** | [**CreateFaxInboundRuleRequest**](CreateFaxInboundRuleRequest.md)|  | [optional] |

### Return type

[**UpdateFaxInboundRule**](UpdateFaxInboundRule.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewFaxDeliveryReceiptRule"></a>
# **viewFaxDeliveryReceiptRule**
> ViewFaxDeliveryReceiptRule viewFaxDeliveryReceiptRule(receiptRuleId, contentType)

View FAX Delivery Receipt Rule

_Get specific fax delivery receipt automation_  Get specific fax delivery receipt automation  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | receipt_rule_id | path | integer(int32) | true | Receipt rule id |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.FaxOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    FaxOtherApi apiInstance = new FaxOtherApi(defaultClient);
    String receiptRuleId = "receiptRuleId_example"; // String | 
    String contentType = "application/json"; // String | 
    try {
      ViewFaxDeliveryReceiptRule result = apiInstance.viewFaxDeliveryReceiptRule(receiptRuleId, contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling FaxOtherApi#viewFaxDeliveryReceiptRule");
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

[**ViewFaxDeliveryReceiptRule**](ViewFaxDeliveryReceiptRule.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewFaxDeliveryReceiptRules"></a>
# **viewFaxDeliveryReceiptRules**
> ViewFaxDeliveryReceiptRules viewFaxDeliveryReceiptRules(contentType)

View FAX Delivery Receipt Rules

_Get all fax delivery receipt automations_  Get all fax delivery receipt automations  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | page | query | integer(int32) | false | Page number | | limit | query | integer(int32) | false | Number of records per page |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.FaxOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    FaxOtherApi apiInstance = new FaxOtherApi(defaultClient);
    String contentType = "application/json"; // String | 
    try {
      ViewFaxDeliveryReceiptRules result = apiInstance.viewFaxDeliveryReceiptRules(contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling FaxOtherApi#viewFaxDeliveryReceiptRules");
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

[**ViewFaxDeliveryReceiptRules**](ViewFaxDeliveryReceiptRules.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewFaxHistory"></a>
# **viewFaxHistory**
> ViewFaxHistory viewFaxHistory(contentType)

View Fax History

_Get a list of Fax History._  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | date_from | query | integer(int32) | false | Start date (Unix Timestamp e.g. 1436849372) | | date_to | query | integer(int32) | false | End date (Unix Timestamp e.g. 1436879372) | | q | query | string | false | Custom query Example: status:Sent,status_code:201. | | order | query | string | false | Order result by Example: date_added:desc,list_id:desc. | | page | query | integer(int32) | false | [Page number](/#pagination) | | limit | query | integer(int32) | false | [Number of records per page](/#pagination) |  Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.  This endpoint requires authentication, [more info...](/#authentication)   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.FaxOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    FaxOtherApi apiInstance = new FaxOtherApi(defaultClient);
    String contentType = "application/json"; // String | 
    try {
      ViewFaxHistory result = apiInstance.viewFaxHistory(contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling FaxOtherApi#viewFaxHistory");
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

[**ViewFaxHistory**](ViewFaxHistory.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewFaxInboundRule"></a>
# **viewFaxInboundRule**
> ViewFaxInboundRule viewFaxInboundRule(inboundRuleId, contentType)

View Fax Inbound Rule

_Get specific inbound fax automation_  Get specific inbound fax automation  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | inbound_rule_id | path | integer(int32) | true | Inbound rule id |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.FaxOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    FaxOtherApi apiInstance = new FaxOtherApi(defaultClient);
    String inboundRuleId = "inboundRuleId_example"; // String | 
    String contentType = "application/json"; // String | 
    try {
      ViewFaxInboundRule result = apiInstance.viewFaxInboundRule(inboundRuleId, contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling FaxOtherApi#viewFaxInboundRule");
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

[**ViewFaxInboundRule**](ViewFaxInboundRule.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewFaxInboundRules"></a>
# **viewFaxInboundRules**
> ViewFaxInboundRules viewFaxInboundRules(contentType)

View Fax Inbound Rules

_Get all inbound fax automations_  Get all inbound fax automations  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | page | query | integer(int32) | false | Page number | | limit | query | integer(int32) | false | Number of records per page |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.FaxOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    FaxOtherApi apiInstance = new FaxOtherApi(defaultClient);
    String contentType = "application/json"; // String | 
    try {
      ViewFaxInboundRules result = apiInstance.viewFaxInboundRules(contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling FaxOtherApi#viewFaxInboundRules");
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

[**ViewFaxInboundRules**](ViewFaxInboundRules.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewFaxReceipts"></a>
# **viewFaxReceipts**
> ViewFaxReceipts viewFaxReceipts(contentType)

View Fax Receipts

_Get List of Fax Receipts_  **Push Delivery Receipts**  If you prefer, we can push message replies to your server as they arrive with us.  1. Log into your account. 2. Click on your profile on the top right. 3. Then click on the Messaging Settings option. 4. Click on Fax then Delivery Reports. 5. Click the &#39;Add New Rule&#39; button. 6. Select the &#39;URL&#39; action. 7. Enter the URL and click &#39;Save&#39;.       The following variables will be posted to the URL specified:  | Variable | Description | | --- | --- | | &#x60;timestamp_send&#x60; | Timestamp of the original send request in UNIX format. e.g 1439173980 | | &#x60;timestamp&#x60; | Timestamp of delivery report in UNIX format. e.g 1439173981 | | &#x60;message_id&#x60; | Message ID, returned when originally sending the message. | | &#x60;status&#x60; | Delivered or Undelivered | | &#x60;status_code&#x60; | Status code. Refer to &#39;Fax Delivery Status Codes&#39; in docs. | | &#x60;status_text&#x60; | Status text. | | &#x60;error_code&#x60; | Error code. | | &#x60;error_text&#x60; | Error text. | | &#x60;custom_string&#x60; | A custom string used when sending the original message. | | &#x60;user_id&#x60; | The user ID of the user who sent the message. | | &#x60;subaccount_id&#x60; | The subaccount ID of the user who sent the message. | | &#x60;message_type&#x60; | &#39;fax&#39; (constant). |  **Pull Delivery Receipts**  Receive delivery reports by polling. You can poll our server and retrieve delivery reports at a time that suits you.  1. Log into your account. 2. Click on your profile on the top right. 3. Then click on the Messaging Settings option. 4. Click on Fax then Delivery Rules. 5. Click the &#39;Add New Rule&#39; button. 6. Select the &#39;Poll&#39; action. 7. Then click &#39;Save&#39;.       Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.FaxOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    FaxOtherApi apiInstance = new FaxOtherApi(defaultClient);
    String contentType = "application/json"; // String | 
    try {
      ViewFaxReceipts result = apiInstance.viewFaxReceipts(contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling FaxOtherApi#viewFaxReceipts");
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

[**ViewFaxReceipts**](ViewFaxReceipts.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewSpecificFaxReceipt"></a>
# **viewSpecificFaxReceipt**
> ViewSpecificFaxReceipt viewSpecificFaxReceipt(messageId, contentType)

View Specific Fax Receipt

_Get a single fax receipt based on message id._  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | message_id | path | string | true | ID of the message receipt to retrieve |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.FaxOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    FaxOtherApi apiInstance = new FaxOtherApi(defaultClient);
    String messageId = "messageId_example"; // String | 
    String contentType = "application/json"; // String | 
    try {
      ViewSpecificFaxReceipt result = apiInstance.viewSpecificFaxReceipt(messageId, contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling FaxOtherApi#viewSpecificFaxReceipt");
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
| **messageId** | **String**|  | |
| **contentType** | **String**|  | [optional] |

### Return type

[**ViewSpecificFaxReceipt**](ViewSpecificFaxReceipt.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

