# InternationalMessagingOtherApi

All URIs are relative to *https://rest.clicksend.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**agreeToRulesAndRegulation**](InternationalMessagingOtherApi.md#agreeToRulesAndRegulation) | **POST** /v3/user-countries/agree | Agree to rules and regulation |
| [**getCountriesForGlobalSending**](InternationalMessagingOtherApi.md#getCountriesForGlobalSending) | **GET** /v3/user-countries | Get Countries for Global Sending |
| [**listCountries**](InternationalMessagingOtherApi.md#listCountries) | **GET** /v3/country-list | International Messaging |
| [**selectCountriesForGlobalSending**](InternationalMessagingOtherApi.md#selectCountriesForGlobalSending) | **POST** /v3/user-countries | Select Countries for Global Sending |
| [**timezones**](InternationalMessagingOtherApi.md#timezones) | **GET** /v3/timezones | Timezones |
| [**viewCountries**](InternationalMessagingOtherApi.md#viewCountries) | **GET** /v3/countries | View Countries |


<a id="agreeToRulesAndRegulation"></a>
# **agreeToRulesAndRegulation**
> AgreeToRulesAndRegulation agreeToRulesAndRegulation()

Agree to rules and regulation

_Update Country Rule_  To agree on rules and regulations of selected countries and confirm selection.  ### Properties  | Name | Type | Required | Restrictions | Description | | --- | --- | --- | --- | --- | | country_list_ids | number | true | none | Country list ID&#39;s |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.InternationalMessagingOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    InternationalMessagingOtherApi apiInstance = new InternationalMessagingOtherApi(defaultClient);
    try {
      AgreeToRulesAndRegulation result = apiInstance.agreeToRulesAndRegulation();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling InternationalMessagingOtherApi#agreeToRulesAndRegulation");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**AgreeToRulesAndRegulation**](AgreeToRulesAndRegulation.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="getCountriesForGlobalSending"></a>
# **getCountriesForGlobalSending**
> GetCountriesForGlobalSending getCountriesForGlobalSending()

Get Countries for Global Sending

_Get Countries for global sending_  Get the list of selected countries.  Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.  &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.InternationalMessagingOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    InternationalMessagingOtherApi apiInstance = new InternationalMessagingOtherApi(defaultClient);
    try {
      GetCountriesForGlobalSending result = apiInstance.getCountriesForGlobalSending();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling InternationalMessagingOtherApi#getCountriesForGlobalSending");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**GetCountriesForGlobalSending**](GetCountriesForGlobalSending.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="listCountries"></a>
# **listCountries**
> ListCountries listCountries()

International Messaging

_List of countries_  List of countries with IDs that can be used in selecting countries for Global sending.  Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.  &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.InternationalMessagingOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    InternationalMessagingOtherApi apiInstance = new InternationalMessagingOtherApi(defaultClient);
    try {
      ListCountries result = apiInstance.listCountries();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling InternationalMessagingOtherApi#listCountries");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**ListCountries**](ListCountries.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="selectCountriesForGlobalSending"></a>
# **selectCountriesForGlobalSending**
> SelectCountriesForGlobalSending selectCountriesForGlobalSending(selectCountriesForGlobalSendingRequest)

Select Countries for Global Sending

_Select Countries_  Use this endpoint to select countries that you intend to send sms / mms to. To remove / unselect a country, just remove the country id from the array in the payload.  ### Properties  | Name | Type | Required | Restrictions | Description | | --- | --- | --- | --- | --- | | country_list_ids | number | true | none | Country list ID&#39;s |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.InternationalMessagingOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    InternationalMessagingOtherApi apiInstance = new InternationalMessagingOtherApi(defaultClient);
    SelectCountriesForGlobalSendingRequest selectCountriesForGlobalSendingRequest = new SelectCountriesForGlobalSendingRequest(); // SelectCountriesForGlobalSendingRequest | 
    try {
      SelectCountriesForGlobalSending result = apiInstance.selectCountriesForGlobalSending(selectCountriesForGlobalSendingRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling InternationalMessagingOtherApi#selectCountriesForGlobalSending");
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
| **selectCountriesForGlobalSendingRequest** | [**SelectCountriesForGlobalSendingRequest**](SelectCountriesForGlobalSendingRequest.md)|  | [optional] |

### Return type

[**SelectCountriesForGlobalSending**](SelectCountriesForGlobalSending.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="timezones"></a>
# **timezones**
> Timezones timezones(contentType)

Timezones

_Get supported list of timezones._  Get supported list of timezones.  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | page | query | integer(int32) | false | Page number | | limit | query | integer(int32) | false | Number of records per page |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.InternationalMessagingOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    InternationalMessagingOtherApi apiInstance = new InternationalMessagingOtherApi(defaultClient);
    String contentType = "application/json"; // String | 
    try {
      Timezones result = apiInstance.timezones(contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling InternationalMessagingOtherApi#timezones");
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

[**Timezones**](Timezones.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewCountries"></a>
# **viewCountries**
> ViewCountries viewCountries()

View Countries

_Get all country codes_  Get all countries   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #6BBD5B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint does not require authentication&lt;/span&gt;  &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.models.*;
import ClickSend.Api.InternationalMessagingOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");

    InternationalMessagingOtherApi apiInstance = new InternationalMessagingOtherApi(defaultClient);
    try {
      ViewCountries result = apiInstance.viewCountries();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling InternationalMessagingOtherApi#viewCountries");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**ViewCountries**](ViewCountries.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

