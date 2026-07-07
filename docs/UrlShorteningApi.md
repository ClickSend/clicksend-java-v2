# UrlShorteningApi

All URIs are relative to *https://rest.clicksend.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**shortUrlGetStatistics**](UrlShorteningApi.md#shortUrlGetStatistics) | **GET** /v3/short-url/statistics/{source}/{source_id} | Get Statistics |
| [**shortUrlGetTracking**](UrlShorteningApi.md#shortUrlGetTracking) | **GET** /v3/short-url/tracking/{long_url_id} | Get Tracking |


<a id="shortUrlGetStatistics"></a>
# **shortUrlGetStatistics**
> GetStatistics shortUrlGetStatistics(source, sourceId, contentType)

Get Statistics

Use this endpoint to get the aggregated statistics for a shortened URL. This allows you to track the total number of clicks on the link. You can gather details such as the device type and where it was opened from as well.

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.UrlShorteningApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    UrlShorteningApi apiInstance = new UrlShorteningApi(defaultClient);
    String source = "quick_sms"; // String | Source of the request.
    String sourceId = "sourceId_example"; // String | ID of the source (e.g. message ID).
    String contentType = "application/json"; // String | 
    try {
      GetStatistics result = apiInstance.shortUrlGetStatistics(source, sourceId, contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling UrlShorteningApi#shortUrlGetStatistics");
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
| **source** | **String**| Source of the request. | [enum: quick_sms] |
| **sourceId** | **String**| ID of the source (e.g. message ID). | |
| **contentType** | **String**|  | [optional] |

### Return type

[**GetStatistics**](GetStatistics.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="shortUrlGetTracking"></a>
# **shortUrlGetTracking**
> GetTracking shortUrlGetTracking(longUrlId, contentType)

Get Tracking

Use this endpoint to track how individual recipients interact with the link.  It returns data from the most recent click, including statistics such as how many times they’ve visited the link and when it was last opened. To use this endpoint, reference the _long_url_id_ provided in the [GET /short-url/statistics](/messaging/url-shortening/other/short-url-get-statistics) endpoint.

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.UrlShorteningApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    UrlShorteningApi apiInstance = new UrlShorteningApi(defaultClient);
    String longUrlId = "longUrlId_example"; // String | ID of the long URL (uniquely defined by the source, source ID, and long URL). Obtained from the GET statistics endpoint.
    String contentType = "application/json"; // String | 
    try {
      GetTracking result = apiInstance.shortUrlGetTracking(longUrlId, contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling UrlShorteningApi#shortUrlGetTracking");
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
| **longUrlId** | **String**| ID of the long URL (uniquely defined by the source, source ID, and long URL). Obtained from the GET statistics endpoint. | |
| **contentType** | **String**|  | [optional] |

### Return type

[**GetTracking**](GetTracking.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

