# MessageDeliveryApi

All URIs are relative to *https://rest.clicksend.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createDeliveryIssue**](MessageDeliveryApi.md#createDeliveryIssue) | **POST** /v3/delivery-issues | Create Delivery Issues |
| [**getAllDeliveryIssues**](MessageDeliveryApi.md#getAllDeliveryIssues) | **GET** /v3/delivery-issues | Get All Delivery Issues |


<a id="createDeliveryIssue"></a>
# **createDeliveryIssue**
> CreateDeliveryIssue createDeliveryIssue(contentType, createDeliveryIssueRequest)

Create Delivery Issues

_Create delivery Issue_  Create delivery Issue  ### Properties  | Name | Type | Required | Restrictions | Description | | --- | --- | --- | --- | --- | | message_id | string | false | none | The message id of the message. | | type | string | true | none | The type of message, must be one of the following values SMS, MMS, VOICE, EMAIL_MARKETING, EMAIL_TRANSACTIONAL, FAX, POST. | | description | string | true | none | The description of the message. | | client_comments | string | false | none | The user&#39;s comments. | | email-address | string | true | none | The user&#39;s email address. |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.MessageDeliveryApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    MessageDeliveryApi apiInstance = new MessageDeliveryApi(defaultClient);
    String contentType = "application/json"; // String | 
    CreateDeliveryIssueRequest createDeliveryIssueRequest = new CreateDeliveryIssueRequest(); // CreateDeliveryIssueRequest | 
    try {
      CreateDeliveryIssue result = apiInstance.createDeliveryIssue(contentType, createDeliveryIssueRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling MessageDeliveryApi#createDeliveryIssue");
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
| **createDeliveryIssueRequest** | [**CreateDeliveryIssueRequest**](CreateDeliveryIssueRequest.md)|  | [optional] |

### Return type

[**CreateDeliveryIssue**](CreateDeliveryIssue.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="getAllDeliveryIssues"></a>
# **getAllDeliveryIssues**
> GetAllDeliveryIssues getAllDeliveryIssues(contentType)

Get All Delivery Issues

_Get all delivery issues_  Get all delivery issues  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | page | query | integer(int32) | false | Page number | | limit | query | integer(int32) | false | Number of records per page |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.MessageDeliveryApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    MessageDeliveryApi apiInstance = new MessageDeliveryApi(defaultClient);
    String contentType = "application/json"; // String | 
    try {
      GetAllDeliveryIssues result = apiInstance.getAllDeliveryIssues(contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling MessageDeliveryApi#getAllDeliveryIssues");
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

[**GetAllDeliveryIssues**](GetAllDeliveryIssues.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

