# MmsOtherApi

All URIs are relative to *https://rest.clicksend.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**calculateMmsPrice**](MmsOtherApi.md#calculateMmsPrice) | **POST** /v3/mms/price | Calculate MMS Price |
| [**exportMmsHistory**](MmsOtherApi.md#exportMmsHistory) | **GET** /v3/mms/history/export | Export MMS History |
| [**sendMms**](MmsOtherApi.md#sendMms) | **POST** /v3/mms/send | Send MMS |
| [**viewMmsHistory**](MmsOtherApi.md#viewMmsHistory) | **GET** /v3/mms/history | View MMS History |


<a id="calculateMmsPrice"></a>
# **calculateMmsPrice**
> CalculateMmsPrice calculateMmsPrice(contentType, calculateMmsPriceRequest)

Calculate MMS Price

_Get Price for MMS sent_  ### Properties  | Name | Type | Required | Restrictions | Description | | --- | --- | --- | --- | --- | | media_file | string | true | none | Media file you want to send | | to | string | true | none | Recipient phone number in [E.164](https://en.wikipedia.org/wiki/E.164) format | | body | string | true | none | Your message | | subject | string | true | none | Subject line (max 20 characters) | | from | string | true | [yes](http://help.clicksend.com/SMS/what-is-a-sender-id-or-sender-number) | Your sender id |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.MmsOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    MmsOtherApi apiInstance = new MmsOtherApi(defaultClient);
    String contentType = "application/json"; // String | 
    CalculateMmsPriceRequest calculateMmsPriceRequest = new CalculateMmsPriceRequest(); // CalculateMmsPriceRequest | 
    try {
      CalculateMmsPrice result = apiInstance.calculateMmsPrice(contentType, calculateMmsPriceRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling MmsOtherApi#calculateMmsPrice");
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
| **calculateMmsPriceRequest** | [**CalculateMmsPriceRequest**](CalculateMmsPriceRequest.md)|  | [optional] |

### Return type

[**CalculateMmsPrice**](CalculateMmsPrice.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="exportMmsHistory"></a>
# **exportMmsHistory**
> ExportMmsHistory exportMmsHistory(contentType, filename, q, orderBy, dateFrom, dateTo, limit)

Export MMS History

_Export all mms history_  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | filename | query | string | true | Filename to download history as |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.MmsOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    MmsOtherApi apiInstance = new MmsOtherApi(defaultClient);
    String contentType = "application/json"; // String | 
    String filename = "MMS_history.csv"; // String | 
    String q = "q_example"; // String | 
    String orderBy = "date_added:desc"; // String | 
    String dateFrom = "dateFrom_example"; // String | 
    String dateTo = "dateTo_example"; // String | 
    Integer limit = 50000; // Integer | 
    try {
      ExportMmsHistory result = apiInstance.exportMmsHistory(contentType, filename, q, orderBy, dateFrom, dateTo, limit);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling MmsOtherApi#exportMmsHistory");
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

[**ExportMmsHistory**](ExportMmsHistory.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="sendMms"></a>
# **sendMms**
> SendMms sendMms(contentType, sendMmsRequest)

Send MMS

_Send MMS_  You can post **up to 1000 messages** with each API call. You can send to a mix of contacts and contact lists, as long as the total number of recipients is up to 1000. The response contains a status and details for each recipient.  Refer to [&lt;b&gt;Application Status Codes&lt;/b&gt;](/#application-status-codes) for the possible response message status strings.  ### **How many characters can I send in a message?**  ### Standard MMS Message  1500 characters  ### Unicode MMS Message  500 characters  If a message is longer the allowed number of characters it will be truncated. If a message contains any characters that aren&#39;t in the GSM 03.38 character set, the message type will be treated as unicode. ([https://en.wikipedia.org/wiki/GSM_03.38](https://en.wikipedia.org/wiki/GSM_03.38))  ### Maximum File Size  You can send a single attachment with a size of up to 250 kB. Some older devices can only accept attachments with up to 30 kB.  ### Supported File Types  - Supported file types are listed below. If you need to convert a file to a supported format, it can be first passed to our uploads endpoint: &#x60;/uploads?convert&#x3D;mms&#x60; - This will return a URL to the converted image file that can be used in the /mms/send endpoint. - Contact us to add support for any other file type.       ### Images  | File type | Required to be passed to uploads endpoint first? | | --- | --- | | &#x60;jpg&#x60; | No | | &#x60;gif&#x60; | No | | &#x60;jpeg&#x60; | Yes | | &#x60;png&#x60; | Yes | | &#x60;bmp&#x60; | Yes |  ### Properties  | Name | Type | Required | Restrictions | Description | | --- | --- | --- | --- | --- | | media_file | string | true | none | Media file you want to send | | to | string | true | none | Recipient phone number in [E.164](https://en.wikipedia.org/wiki/E.164) format | | body | string | true | none | Your message | | subject | string | true | none | Subject line (max 20 characters) | | from | string | true | [yes](http://help.clicksend.com/SMS/what-is-a-sender-id-or-sender-number) | Your sender id |  Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.  &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.MmsOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    MmsOtherApi apiInstance = new MmsOtherApi(defaultClient);
    String contentType = "application/json"; // String | 
    SendMmsRequest sendMmsRequest = new SendMmsRequest(); // SendMmsRequest | 
    try {
      SendMms result = apiInstance.sendMms(contentType, sendMmsRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling MmsOtherApi#sendMms");
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
| **sendMmsRequest** | [**SendMmsRequest**](SendMmsRequest.md)|  | [optional] |

### Return type

[**SendMms**](SendMms.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewMmsHistory"></a>
# **viewMmsHistory**
> ViewMmsHistory viewMmsHistory(contentType, limit)

View MMS History

_Get all mms history_  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | date_from | query | integer(int32) | false | Start date (Unix Timestamp e.g. 1436849372) | | date_to | query | integer(int32) | false | End date (Unix Timestamp e.g. 1436879372) | | page | query | integer(int32) | false | [Page number](/#pagination) | | limit | query | integer(int32) | false | [Number of records per page](/#pagination) |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.MmsOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    MmsOtherApi apiInstance = new MmsOtherApi(defaultClient);
    String contentType = "application/json"; // String | 
    Integer limit = 100; // Integer | 
    try {
      ViewMmsHistory result = apiInstance.viewMmsHistory(contentType, limit);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling MmsOtherApi#viewMmsHistory");
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
| **limit** | **Integer**|  | [optional] |

### Return type

[**ViewMmsHistory**](ViewMmsHistory.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

