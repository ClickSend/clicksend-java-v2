# LettersOtherApi

All URIs are relative to *https://rest.clicksend.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**calculateLetterPrice**](LettersOtherApi.md#calculateLetterPrice) | **POST** /v3/post/letters/price | Calculate Letter Price |
| [**cancelScheduledLetter**](LettersOtherApi.md#cancelScheduledLetter) | **PUT** /v3/post/letters/{message_id}/cancel | Cancel Scheduled Letter |
| [**detectAddress**](LettersOtherApi.md#detectAddress) | **POST** /v3/post/letters/detect-address | Detect Address |
| [**exportLetterHistory**](LettersOtherApi.md#exportLetterHistory) | **GET** /v3/post/letters/history/export | Export Letter History |
| [**sendLetter**](LettersOtherApi.md#sendLetter) | **POST** /v3/post/letters/send | Send Letter |
| [**viewLetterHistory**](LettersOtherApi.md#viewLetterHistory) | **GET** /v3/post/letters/history | View Letter History |


<a id="calculateLetterPrice"></a>
# **calculateLetterPrice**
> CalculateLetterPrice calculateLetterPrice(contentType, calculateLetterPriceRequest)

Calculate Letter Price

_Calculate letter price_  ### Properties  | Name | Type | Required | Restrictions | Description | | --- | --- | --- | --- | --- | | file_url | string | true | none | URL of file to send | | address_name | string | true | none | Name of address | | address_line_1 | string | true | none | First line of address | | address_line_2 | string | true | none | Second line of address | | address_city | string | true | none | City | | address_state | string | true | none | State | | address_postal_code | string | true | none | Postal code | | address_country | string | true | none | Country | | return_address_id | integer(int32) | true | none | ID of return address to use | | schedule | integer(int32) | false | none | When to send letter (0/null&#x3D;now) | | template_used | integer(int1) | false | none | Whether using our letter template. Flag value must be 1 for yes or 0 for no. | | duplex | integer(int1) | false | none | Whether letter is duplex. Flag value must be 1 for yes or 0 for no. | | colour | integer(int1) | false | none | Whether letter is in colour. Flag value must be 1 for yes or 0 for no. | | priority_post | integer(int1) | false | none | Whether letter is priority. Flag value must be 1 for yes or 0 for no. | | source | string | false | none | Source being sent from |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.LettersOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    LettersOtherApi apiInstance = new LettersOtherApi(defaultClient);
    String contentType = "application/json"; // String | 
    CalculateLetterPriceRequest calculateLetterPriceRequest = new CalculateLetterPriceRequest(); // CalculateLetterPriceRequest | 
    try {
      CalculateLetterPrice result = apiInstance.calculateLetterPrice(contentType, calculateLetterPriceRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling LettersOtherApi#calculateLetterPrice");
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
| **calculateLetterPriceRequest** | [**CalculateLetterPriceRequest**](CalculateLetterPriceRequest.md)|  | [optional] |

### Return type

[**CalculateLetterPrice**](CalculateLetterPrice.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="cancelScheduledLetter"></a>
# **cancelScheduledLetter**
> CancelScheduledLetter cancelScheduledLetter(messageId)

Cancel Scheduled Letter

_Cancel scheduled letter_  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | message_id | query | string | true | Message ID of the scheduled letter that is to be cancelled. |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.models.*;
import org.openapitools.client.api.LettersOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");

    LettersOtherApi apiInstance = new LettersOtherApi(defaultClient);
    String messageId = "messageId_example"; // String | 
    try {
      CancelScheduledLetter result = apiInstance.cancelScheduledLetter(messageId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling LettersOtherApi#cancelScheduledLetter");
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

[**CancelScheduledLetter**](CancelScheduledLetter.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="detectAddress"></a>
# **detectAddress**
> DetectAddress detectAddress(contentType, body)

Detect Address

_Detects address in uploaded file._  The &#x60;detect-address&#x60; endpoint accepts either a letter in PDF format or an address string and attempts to convert it to a standard address format. Note that the PDF should be in standard address format, having the recipient&#39;s name and address listed at the top.  The endpoint accepts two types of data: 1. A PDF file in &#x60;base64&#x60; encoding. In this case, submit the &#x60;base64&#x60;\\-encoded PDF file contents in the &#x60;content&#x60; field of the request body. 2. An address string. In this case, submit the address in a string using the &#x60;address&#x60; field of the request body.  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | convert | query | string | true | none | | content | body | string | true | Base64-encoded file contents |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.LettersOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    LettersOtherApi apiInstance = new LettersOtherApi(defaultClient);
    String contentType = "application/json"; // String | 
    Object body = null; // Object | 
    try {
      DetectAddress result = apiInstance.detectAddress(contentType, body);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling LettersOtherApi#detectAddress");
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
| **body** | **Object**|  | [optional] |

### Return type

[**DetectAddress**](DetectAddress.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="exportLetterHistory"></a>
# **exportLetterHistory**
> ExportLetterHistory exportLetterHistory(contentType, filename, q, orderBy, dateFrom, dateTo, limit)

Export Letter History

_export letter history_  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | filename | query | string | true | Filename to export to |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.LettersOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    LettersOtherApi apiInstance = new LettersOtherApi(defaultClient);
    String contentType = "application/json"; // String | 
    String filename = "Post_history.csv"; // String | 
    String q = "q_example"; // String | 
    String orderBy = "date_added:desc"; // String | 
    String dateFrom = "dateFrom_example"; // String | 
    String dateTo = "dateTo_example"; // String | 
    Integer limit = 50000; // Integer | 
    try {
      ExportLetterHistory result = apiInstance.exportLetterHistory(contentType, filename, q, orderBy, dateFrom, dateTo, limit);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling LettersOtherApi#exportLetterHistory");
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
| **filename** | **String**|  | [optional] |
| **q** | **String**|  | [optional] |
| **orderBy** | **String**|  | [optional] |
| **dateFrom** | **String**|  | [optional] |
| **dateTo** | **String**|  | [optional] |
| **limit** | **Integer**|  | [optional] |

### Return type

[**ExportLetterHistory**](ExportLetterHistory.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="sendLetter"></a>
# **sendLetter**
> SendLetter sendLetter(contentType, sendLetterRequest)

Send Letter

### Send letter  ### **Supported File Types**  We support &#x60;pdf&#x60;, &#x60;docx&#x60; and &#x60;doc&#x60; files. Contact us to add support for any other file type. If you&#39;re using &#x60;docx&#x60; or &#x60;doc&#x60; files, you&#39;ll need to convert the file first using our uploads endpoint with the querystring parameter &#x60;convert&#x3D;post&#x60; e.g. &#x60;POST https://rest.clicksend.com/v3/uploads?convert&#x3D;post&#x60;. This will return a URL to the converted pdf file that can be used in the &#x60;/post/letters/send&#x60; endpoint.  ### **Letter Specification Guide**  Follow our [Letter specification guide](https://help.clicksend.com/article/wcpkkoou6c-post-letter-template) to ensure correct sending and letter template information.  ### **Letter File Options**  ### Use existing URL  With this option, you can use an existing URL to a &#x60;pdf&#x60; document. For example, you might generate the &#x60;pdf&#x60; on your server.  When using an existing url make sure that it is publicly accessible as it will not work if it is private.  ### Upload File to Our Server  With this option, you can use the [/uploads](/#upload-media-file) endpoint to upload the document. The &#x60;/uploads&#x60; endpoint returns a URL that can be used in the &#x60;/post/letters/send&#x60; endpoint.  ### Properties  | Name | Type | Required | Restrictions | Description | | --- | --- | --- | --- | --- | | file_url | string | true | none | URL of file to send | | address_name | string | true | none | Name of address | | address_line_1 | string | true | none | First line of address | | address_line_2 | string | true | none | Second line of address | | address_city | string | true | none | City | | address_state | string | true | none | State | | address_postal_code | string | true | none | Postal code | | address_country | string | true | none | Country | | return_address_id | integer(int32) | true | none | ID of return address to use | | schedule | integer(int32) | false | none | When to send letter (0/null&#x3D;now) | | template_used | integer(int1) | false | none | Whether using our letter template. Flag value must be 1 for yes or 0 for no. | | duplex | integer(int1) | false | none | Whether letter is duplex. Flag value must be 1 for yes or 0 for no. | | colour | integer(int1) | false | none | Whether letter is in colour. Flag value must be 1 for yes or 0 for no. | | priority_post | integer(int1) | false | none | Whether letter is priority, Flag value must be 1 for yes or 0 for no. | | source | string | false | none | Source being sent from |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.LettersOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    LettersOtherApi apiInstance = new LettersOtherApi(defaultClient);
    String contentType = "application/json"; // String | 
    SendLetterRequest sendLetterRequest = new SendLetterRequest(); // SendLetterRequest | 
    try {
      SendLetter result = apiInstance.sendLetter(contentType, sendLetterRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling LettersOtherApi#sendLetter");
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
| **sendLetterRequest** | [**SendLetterRequest**](SendLetterRequest.md)|  | [optional] |

### Return type

[**SendLetter**](SendLetter.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewLetterHistory"></a>
# **viewLetterHistory**
> ViewLetterHistory viewLetterHistory(contentType)

View Letter History

_Get all letter history_  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | page | query | integer(int32) | false | [Page number](/#pagination) | | limit | query | integer(int32) | false | [Number of records per page](/#pagination) |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.LettersOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    LettersOtherApi apiInstance = new LettersOtherApi(defaultClient);
    String contentType = "application/json"; // String | 
    try {
      ViewLetterHistory result = apiInstance.viewLetterHistory(contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling LettersOtherApi#viewLetterHistory");
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

[**ViewLetterHistory**](ViewLetterHistory.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

