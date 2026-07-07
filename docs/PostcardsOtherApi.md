# PostcardsOtherApi

All URIs are relative to *https://rest.clicksend.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**calculatePostcardPrice**](PostcardsOtherApi.md#calculatePostcardPrice) | **POST** /v3/post/postcards/price | Calculate Postcard Price |
| [**cancelScheduledPostcard**](PostcardsOtherApi.md#cancelScheduledPostcard) | **PUT** /v3/post/postcards/{message_id}/cancel | Cancel Scheduled Postcard |
| [**exportPostcardHistory**](PostcardsOtherApi.md#exportPostcardHistory) | **GET** /v3/post/postcards/history/export | Export Postcard History |
| [**sendPostcard**](PostcardsOtherApi.md#sendPostcard) | **POST** /v3/post/postcards/send | Send Postcard |
| [**viewPostcardHistory**](PostcardsOtherApi.md#viewPostcardHistory) | **GET** /v3/post/postcards/history | View Postcard History |


<a id="calculatePostcardPrice"></a>
# **calculatePostcardPrice**
> CalculatePostcardPrice calculatePostcardPrice(contentType, sendPostcardRequest)

Calculate Postcard Price

_Calculate price for sending one or more postcards_  For &#x60;file_urls&#x60; field. You can attach at least 1 and max of 2 PDF file urls.  - Supply a single pdf with 2 pages (front and back) - Supply 2 urls to seperate PDFs       ### Properties  | Name | Type | Required | Restrictions | Description | | --- | --- | --- | --- | --- | | file_urls | \\[string\\] | true | none | Postcard file URLs | | address_name | string | true | none | Name of address | | address_line_1 | string | true | none | First line of address | | address_line_2 | string | true | none | Second line of address | | address_city | string | true | none | City | | address_state | string | true | none | State | | address_postal_code | string | true | none | Postal code | | address_country | string | true | none | Country | | return_address_id | integer(int32) | true | none | ID of return address to use | | schedule | integer(int32) | false | none | When to send letter (0/null&#x3D;now) |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.PostcardsOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    PostcardsOtherApi apiInstance = new PostcardsOtherApi(defaultClient);
    String contentType = "application/json"; // String | 
    SendPostcardRequest sendPostcardRequest = new SendPostcardRequest(); // SendPostcardRequest | 
    try {
      CalculatePostcardPrice result = apiInstance.calculatePostcardPrice(contentType, sendPostcardRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PostcardsOtherApi#calculatePostcardPrice");
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
| **sendPostcardRequest** | [**SendPostcardRequest**](SendPostcardRequest.md)|  | [optional] |

### Return type

[**CalculatePostcardPrice**](CalculatePostcardPrice.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="cancelScheduledPostcard"></a>
# **cancelScheduledPostcard**
> CancelScheduledPostcard cancelScheduledPostcard(messageId)

Cancel Scheduled Postcard

_Cancel scheduled postcard_  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | message_id | query | string | true | Message ID of the scheduled postcard that is to be cancelled. |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.models.*;
import ClickSend.Api.PostcardsOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");

    PostcardsOtherApi apiInstance = new PostcardsOtherApi(defaultClient);
    String messageId = "messageId_example"; // String | 
    try {
      CancelScheduledPostcard result = apiInstance.cancelScheduledPostcard(messageId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PostcardsOtherApi#cancelScheduledPostcard");
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

### Return type

[**CancelScheduledPostcard**](CancelScheduledPostcard.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="exportPostcardHistory"></a>
# **exportPostcardHistory**
> ExportPostcardHistory exportPostcardHistory(contentType)

Export Postcard History

_Export postcard history to a CSV file_  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | filename | query | string | true | Filename to export to |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.PostcardsOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    PostcardsOtherApi apiInstance = new PostcardsOtherApi(defaultClient);
    String contentType = "application/json"; // String | 
    try {
      ExportPostcardHistory result = apiInstance.exportPostcardHistory(contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PostcardsOtherApi#exportPostcardHistory");
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

[**ExportPostcardHistory**](ExportPostcardHistory.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="sendPostcard"></a>
# **sendPostcard**
> SendPostcard sendPostcard(contentType, sendPostcardRequest)

Send Postcard

_Send one or more postcards_  ### **Supported File Types**  We support PDF, docx, doc, jpg, gif, png, and bmp. Contact us to add support for any other file type. If you&#39;re using docx, doc, jpg, gif, png, or bmp files, you&#39;ll need to convert the file first using our uploads endpoint with the querystring parameter ?convert&#x3D;postcard. e.g. POST /uploads?convert&#x3D;postcard. This will return a URL to the converted pdf file that can be used in the /post/postcards/send endpoint.  ### **Postcard Specification Guide**  Follow our [Postcard specification guide](https://help.clicksend.com/article/ysyql7bsr1-postcard-template) to ensure correct sending and postcard template information.  ### **Postcard File Options**  ### Use existing URL  With this option, you can use an existing URL to a &#x60;pdf&#x60; document. For example, you might generate the &#x60;pdf&#x60; on your server.  When using an existing url make sure that it is publicly accessible as it will not work if it is private.  For &#x60;file_urls&#x60; field. You can attach at least 1 and max of 2 PDF file urls.  - Supply a single pdf with 2 pages (front and back) - Supply 2 urls to seperate PDFs       ### Upload File to Our Server  With this option, you can use the [/uploads](/#upload-media-file) endpoint to upload the document. The &#x60;/uploads&#x60; endpoint returns a URL that can be used in the &#x60;/post/postcards/send&#x60; endpoint.  ### Properties  | Name | Type | Required | Restrictions | Description | | --- | --- | --- | --- | --- | | file_urls | \\[string\\] | true | none | Postcard file URLs | | address_name | string | true | none | Name of address | | address_line_1 | string | true | none | First line of address | | address_line_2 | string | true | none | Second line of address | | address_city | string | true | none | City | | address_state | string | true | none | State | | address_postal_code | string | true | none | Postal code | | address_country | string | true | none | Country | | return_address_id | integer(int32) | true | none | ID of return address to use | | schedule | integer(int32) | false | none | When to send letter (0/null&#x3D;now) |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.PostcardsOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    PostcardsOtherApi apiInstance = new PostcardsOtherApi(defaultClient);
    String contentType = "application/json"; // String | 
    SendPostcardRequest sendPostcardRequest = new SendPostcardRequest(); // SendPostcardRequest | 
    try {
      SendPostcard result = apiInstance.sendPostcard(contentType, sendPostcardRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PostcardsOtherApi#sendPostcard");
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
| **sendPostcardRequest** | [**SendPostcardRequest**](SendPostcardRequest.md)|  | [optional] |

### Return type

[**SendPostcard**](SendPostcard.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewPostcardHistory"></a>
# **viewPostcardHistory**
> ViewPostcardHistory viewPostcardHistory(contentType)

View Postcard History

_Retrieve the history of postcards sent or scheduled_  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | page | query | integer(int32) | false | [Page number](/#pagination) | | limit | query | integer(int32) | false | [Number of records per page](/#pagination) |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.PostcardsOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    PostcardsOtherApi apiInstance = new PostcardsOtherApi(defaultClient);
    String contentType = "application/json"; // String | 
    try {
      ViewPostcardHistory result = apiInstance.viewPostcardHistory(contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PostcardsOtherApi#viewPostcardHistory");
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

[**ViewPostcardHistory**](ViewPostcardHistory.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

