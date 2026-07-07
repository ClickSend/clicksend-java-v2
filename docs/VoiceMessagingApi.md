# VoiceMessagingApi

All URIs are relative to *https://rest.clicksend.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**calculateVoicePrice**](VoiceMessagingApi.md#calculateVoicePrice) | **POST** /v3/voice/price | Calculate Voice Price |
| [**cancelAllVoiceMessages**](VoiceMessagingApi.md#cancelAllVoiceMessages) | **PUT** /v3/voice/cancel-all | Cancel All Voice Messages |
| [**cancelVoiceMessage**](VoiceMessagingApi.md#cancelVoiceMessage) | **PUT** /v3/voice/{message_id}/cancel | Cancel Voice Message |
| [**exportVoiceHistory**](VoiceMessagingApi.md#exportVoiceHistory) | **GET** /v3/voice/history/export | Export Voice History |
| [**getVoiceHistory**](VoiceMessagingApi.md#getVoiceHistory) | **GET** /v3/voice/history | Get Voice History |
| [**sendVoiceMessage**](VoiceMessagingApi.md#sendVoiceMessage) | **POST** /v3/voice/send | Send Voice Message |
| [**viewVoiceLanguages**](VoiceMessagingApi.md#viewVoiceLanguages) | **GET** /v3/voice/lang | View Voice Languages |
| [**viewVoiceReceipts**](VoiceMessagingApi.md#viewVoiceReceipts) | **GET** /v3/voice/receipts | View Voice Receipts |


<a id="calculateVoicePrice"></a>
# **calculateVoicePrice**
> CalculateVoicePrice calculateVoicePrice(contentType, calculateVoicePriceRequest)

Calculate Voice Price

_Calculate voice price_  ### Properties  | Name | Type | Required | Restrictions | Description | | --- | --- | --- | --- | --- | | to | string | true | none | Your phone number in [E.164](https://en.wikipedia.org/wiki/E.164) format. | | body | string | true | none | Biscuit uv3nlCOjRk croissant chocolate lollipop chocolate muffin. | | voice | string | true | none | Either &#39;female&#39; or &#39;male&#39;. | | custom_string | string | true | none | Your reference. Will be passed back with all replies and delivery reports. | | country | string | true | none | The country of the recipient. | | source | string | false | none | Your method of sending e.g. &#39;wordpress&#39;, &#39;php&#39;, &#39;c#&#39;. | | list_id | integer(int32) | false | none | Your list ID if sending to a whole list. Can be used instead of &#39;to&#39;. | | lang | string | false | none | au (string, required) - See section on available languages. | | schedule | integer(int32) | false | none | Leave blank for immediate delivery. Your schedule time in unix format [http://help.clicksend.com/what-is-a-unix-timestamp](http://help.clicksend.com/what-is-a-unix-timestamp) | | require_input | integer(int1) | false | none | Recieve a keypress from the recipient. Flag value must be 1 for yes or 0 for no. | | machine_detection | integer(int1) | false | none | Detect answering machine or voicemail and leave a message. Flag value must be 1 for yes or 0 for no. |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.VoiceMessagingApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    VoiceMessagingApi apiInstance = new VoiceMessagingApi(defaultClient);
    String contentType = "application/json"; // String | 
    CalculateVoicePriceRequest calculateVoicePriceRequest = new CalculateVoicePriceRequest(); // CalculateVoicePriceRequest | 
    try {
      CalculateVoicePrice result = apiInstance.calculateVoicePrice(contentType, calculateVoicePriceRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling VoiceMessagingApi#calculateVoicePrice");
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
| **calculateVoicePriceRequest** | [**CalculateVoicePriceRequest**](CalculateVoicePriceRequest.md)|  | [optional] |

### Return type

[**CalculateVoicePrice**](CalculateVoicePrice.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="cancelAllVoiceMessages"></a>
# **cancelAllVoiceMessages**
> CancelAllVoiceMessages cancelAllVoiceMessages(contentType, body)

Cancel All Voice Messages

_Update all voice messages as cancelled_  Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.  &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.VoiceMessagingApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    VoiceMessagingApi apiInstance = new VoiceMessagingApi(defaultClient);
    String contentType = "application/x-www-form-urlencoded"; // String | 
    Object body = null; // Object | 
    try {
      CancelAllVoiceMessages result = apiInstance.cancelAllVoiceMessages(contentType, body);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling VoiceMessagingApi#cancelAllVoiceMessages");
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

[**CancelAllVoiceMessages**](CancelAllVoiceMessages.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="cancelVoiceMessage"></a>
# **cancelVoiceMessage**
> CancelVoiceMessage cancelVoiceMessage(messageId, contentType, body)

Cancel Voice Message

_Update voice message status as cancelled_  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | message_id | path | string | true | Your voice message id |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.VoiceMessagingApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    VoiceMessagingApi apiInstance = new VoiceMessagingApi(defaultClient);
    String messageId = "messageId_example"; // String | 
    String contentType = "application/x-www-form-urlencoded"; // String | 
    Object body = null; // Object | 
    try {
      CancelVoiceMessage result = apiInstance.cancelVoiceMessage(messageId, contentType, body);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling VoiceMessagingApi#cancelVoiceMessage");
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
| **body** | **Object**|  | [optional] |

### Return type

[**CancelVoiceMessage**](CancelVoiceMessage.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="exportVoiceHistory"></a>
# **exportVoiceHistory**
> ExportVoiceHistory exportVoiceHistory(contentType, filename, q, orderBy, dateFrom, dateTo, limit)

Export Voice History

_Export voice history_  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | filename | query | string | true | Filename to export to |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.VoiceMessagingApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    VoiceMessagingApi apiInstance = new VoiceMessagingApi(defaultClient);
    String contentType = "application/json"; // String | 
    String filename = "Voice_history.csv"; // String | 
    String q = "q_example"; // String | 
    String orderBy = "date_added:desc"; // String | 
    String dateFrom = "dateFrom_example"; // String | 
    String dateTo = "dateTo_example"; // String | 
    Integer limit = 50000; // Integer | 
    try {
      ExportVoiceHistory result = apiInstance.exportVoiceHistory(contentType, filename, q, orderBy, dateFrom, dateTo, limit);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling VoiceMessagingApi#exportVoiceHistory");
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

[**ExportVoiceHistory**](ExportVoiceHistory.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="getVoiceHistory"></a>
# **getVoiceHistory**
> GetVoiceHistory getVoiceHistory(contentType, dateTo, limit, operator, orderBy, page)

Get Voice History

_Get all voice history_  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | date_from | query | integer(int32) | false | Start date (Unix Timestamp e.g. 1436849372) | | date_to | query | integer(int32) | false | End date (Unix Timestamp e.g. 1436879372) | | page | query | integer(int32) | false | [Page number](/#pagination) | | limit | query | integer(int32) | false | [Number of records per page](/#pagination) |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.VoiceMessagingApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    VoiceMessagingApi apiInstance = new VoiceMessagingApi(defaultClient);
    String contentType = "application/json"; // String | 
    String dateTo = "dateTo_example"; // String | 
    Integer limit = 20; // Integer | 
    String operator = "AND"; // String | 
    String orderBy = "date_added:desc"; // String | 
    Integer page = 1; // Integer | 
    try {
      GetVoiceHistory result = apiInstance.getVoiceHistory(contentType, dateTo, limit, operator, orderBy, page);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling VoiceMessagingApi#getVoiceHistory");
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
| **dateTo** | **String**|  | [optional] |
| **limit** | **Integer**|  | [optional] |
| **operator** | **String**|  | [optional] |
| **orderBy** | **String**|  | [optional] |
| **page** | **Integer**|  | [optional] |

### Return type

[**GetVoiceHistory**](GetVoiceHistory.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="sendVoiceMessage"></a>
# **sendVoiceMessage**
> SendVoiceMessage sendVoiceMessage(contentType, sendVoiceMessageRequest)

Send Voice Message

_Send voice message(s)_  Send TTS (Text-to-speech) voice calls  ### How many messages can I send?  You can post **up to 1000 messages** with each API call. You can send to a mix of contacts and contact lists, as long as the total number of recipients is up to 1000. The response contains a status and details for each recipient.  ### How many characters can I send in a message?  If a message is longer than 4 message parts, it will be truncated (see below). If a message contains any characters that aren&#39;t in the GSM 03.38 character set, the message type will be treated as unicode. (&#x60;https://en.wikipedia.org/wiki/GSM_03.38&#x60;)  ### _Standard English Characters:_  | Number of Characters | Message Credits | | --- | --- | | 1 - 300 | 1 | | 301 - 600 | 2 | | 601 - 900 | 3 | | 901 - 1200 | 4 |  ### _Non-GSM (Unicode) characters:_  | Number of Characters | Message Credits | | --- | --- | | 1 - 150 | 1 | | 151 - 300 | 2 | | 301 - 450 | 3 | | 451 - 600 | 4 |  ### _Allowed Languages_  | Language, Locale | lang | voice | | --- | --- | --- | | &#x60;English&#x60;, US | en-us | female (default) / male | | &#x60;English&#x60;, Australia | en-au | female (default) / male | | &#x60;English&#x60;, UK | en-gb | female (default) / male | | &#x60;English&#x60;, India | en-in | female | | &#x60;English&#x60;, Wales | en-gb-wls | female (default) / male | | &#x60;Celtic&#x60;, Wales | cy-gb-wls | female (default) / male | | &#x60;German&#x60;, Germany | de-de | female (default) / male | | &#x60;Spanish&#x60;, Spain | es-es | female (default) / male | | &#x60;Spanish&#x60;, US | es-us | female (default) / male | | &#x60;French&#x60;, Canada | fr-ca | female | | &#x60;French&#x60;, France | fr-fr | female (default) / male | | &#x60;Icelandic&#x60;, Iceland | is-is | female (default) / male | | &#x60;Italian&#x60;, Italy | it-it | female (default) / male | | &#x60;Danish&#x60;, Denmark | da-dk | female (default) / male | | &#x60;Dutch&#x60;, Netherlands | nl-nl | female (default) / male | | &#x60;Norwegian&#x60;, Norway | nb-no | female | | &#x60;Polish&#x60;, Poland | pl-pl | female (default) / male | | &#x60;Portuguese&#x60;, Portugal | pt-pt | male | | &#x60;Portuguese&#x60;, Brazil | pt-br | female (default) / male | | &#x60;Romanian&#x60;, Romania | ro-ro | female | | &#x60;Russian&#x60;, Russia | ru-ru | female (default) / male | | &#x60;Swedish&#x60;, Sweden | sv-se | female | | &#x60;Turkish&#x60;, Turkey | tr-tr | female |  _Tips_  To introduce a small delay between words or digits you can use a comma (,).  For example: &#x60;Please enter your activation code 9, 0, 9, 0, in the next 20 minutes.&#x60;  We support some SSML tags allowing custom breaks or pauses to be entered, and the readout rate to be altered.  [More info...](https://help.clicksend.com/en/articles/42982-customising-text-to-voice-output)  ### Properties  | Name | Type | Required | Restrictions | Description | | --- | --- | --- | --- | --- | | to | string | true | none | Your phone number in [E.164](https://en.wikipedia.org/wiki/E.164) format. | | body | string | true | none | Biscuit uv3nlCOjRk croissant chocolate lollipop chocolate muffin. | | voice | string | true | none | Either &#39;female&#39; or &#39;male&#39;. | | custom_string | string | true | none | Your reference. Will be passed back with all replies and delivery reports. | | country | string | true | none | The country of the recipient. | | source | string | false | none | Your method of sending e.g. &#39;wordpress&#39;, &#39;php&#39;, &#39;c#&#39;. | | list_id | integer(int32) | false | none | Your list ID if sending to a whole list. Can be used instead of &#39;to&#39;. | | lang | string | false | none | au (string, required) - See section on available languages. | | schedule | integer(int32) | false | none | Leave blank for immediate delivery. Your schedule time in unix format [http://help.clicksend.com/what-is-a-unix-timestamp](http://help.clicksend.com/what-is-a-unix-timestamp) | | require_input | integer(int1) | false | none | Recieve a keypress from the recipient. Flag value must be 1 for yes or 0 for no. | | machine_detection | integer(int1) | false | none | Detect answering machine or voicemail and leave a message. Flag value must be 1 for yes or 0 for no. |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.VoiceMessagingApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    VoiceMessagingApi apiInstance = new VoiceMessagingApi(defaultClient);
    String contentType = "application/json"; // String | 
    SendVoiceMessageRequest sendVoiceMessageRequest = new SendVoiceMessageRequest(); // SendVoiceMessageRequest | 
    try {
      SendVoiceMessage result = apiInstance.sendVoiceMessage(contentType, sendVoiceMessageRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling VoiceMessagingApi#sendVoiceMessage");
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
| **sendVoiceMessageRequest** | [**SendVoiceMessageRequest**](SendVoiceMessageRequest.md)|  | [optional] |

### Return type

[**SendVoiceMessage**](SendVoiceMessage.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewVoiceLanguages"></a>
# **viewVoiceLanguages**
> ViewVoiceLanguages viewVoiceLanguages(contentType)

View Voice Languages

_Get all voice languages_   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.VoiceMessagingApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    VoiceMessagingApi apiInstance = new VoiceMessagingApi(defaultClient);
    String contentType = "application/json"; // String | 
    try {
      ViewVoiceLanguages result = apiInstance.viewVoiceLanguages(contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling VoiceMessagingApi#viewVoiceLanguages");
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

[**ViewVoiceLanguages**](ViewVoiceLanguages.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewVoiceReceipts"></a>
# **viewVoiceReceipts**
> ViewVoiceReceipts viewVoiceReceipts(contentType)

View Voice Receipts

_Get all voice receipts_  **Push Delivery Receipts**  If you prefer, we can push message replies to your server as they arrive with us.  1. Log into your account. 2. Click on your profile on the top right. 3. Then click on the Messaging Settings option. 4. Click on Voice then Delivery Report Rules. 5. Click the &#39;Add New Rule&#39; button. 6. Select the &#39;URL&#39; action. 7. Enter the URL and click &#39;Save&#39;.       The following variables will be posted to the URL specified:  | Variable | Description | | --- | --- | | &#x60;timestamp_send&#x60; | Timestamp of the original send request in UNIX format. e.g 1439173980 | | &#x60;timestamp&#x60; | Timestamp of delivery report in UNIX format. e.g 1439173981 | | &#x60;message_id&#x60; | Message ID, returned when originally sending the message. | | &#x60;status&#x60; | Delivered or Undelivered | | &#x60;status_code&#x60; | Status code. Refer to &#39;Voice Delivery Status Codes&#39; in docs. | | &#x60;status_text&#x60; | Status text. | | &#x60;error_code&#x60; | Error code. | | &#x60;error_text&#x60; | Error text. | | &#x60;custom_string&#x60; | A custom string used when sending the original message. | | &#x60;user_id&#x60; | The user ID of the user who sent the message. | | &#x60;subaccount_id&#x60; | The subaccount ID of the user who sent the message. | | &#x60;message_type&#x60; | &#39;voice&#39; (constant). | | &#x60;digits&#x60; | Numbers the recipient pressed on their keypad during the call. A blank string will be used if they didn&#39;t provide any input. |  **Pull Delivery Receipts**  Receive delivery reports by polling. You can poll our server and retrieve delivery reports at a time that suits you.  1. Log into your account. 2. Click on your profile on the top right. 3. Then click on the Messaging Settings option. 4. Click on Voice then Delivery Report Rules. 5. Click the &#39;Add New Rule&#39; button. 6. Select the &#39;Poll&#39; action. 7. Then click &#39;Save&#39;.       ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | page | query | integer(int32) | false | [Page number](/#pagination) | | limit | query | integer(int32) | false | [Number of records per page](/#pagination) |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.VoiceMessagingApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    VoiceMessagingApi apiInstance = new VoiceMessagingApi(defaultClient);
    String contentType = "application/json"; // String | 
    try {
      ViewVoiceReceipts result = apiInstance.viewVoiceReceipts(contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling VoiceMessagingApi#viewVoiceReceipts");
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

[**ViewVoiceReceipts**](ViewVoiceReceipts.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

