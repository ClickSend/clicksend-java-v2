# ManagementOtherApi

All URIs are relative to *https://rest.clicksend.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**viewAccountDetails**](ManagementOtherApi.md#viewAccountDetails) | **GET** /v3/account | View Account Details |
| [**viewAccountUsage**](ManagementOtherApi.md#viewAccountUsage) | **GET** /v3/account/usage/{year}/{month}/subaccount | View Account Usage |


<a id="viewAccountDetails"></a>
# **viewAccountDetails**
> ViewAccountDetails viewAccountDetails(contentType)

View Account Details

_Get account information_  Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.  &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/#pagination\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.ManagementOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    ManagementOtherApi apiInstance = new ManagementOtherApi(defaultClient);
    String contentType = "application/json"; // String | 
    try {
      ViewAccountDetails result = apiInstance.viewAccountDetails(contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ManagementOtherApi#viewAccountDetails");
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

[**ViewAccountDetails**](ViewAccountDetails.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewAccountUsage"></a>
# **viewAccountUsage**
> ViewAccountUsage viewAccountUsage(year, month, contentType)

View Account Usage

_Get account usage_  | **Name** | **Type** | **Required** | **Restrictions** | **Description** | | --- | --- | --- | --- | --- | | year | string | true | none | Your account usage year. Example: 2019 | | month | string | true | none | Your account usage month. Example: 4 |  Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.  &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/#pagination\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.ManagementOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    ManagementOtherApi apiInstance = new ManagementOtherApi(defaultClient);
    String year = "year_example"; // String | 
    String month = "month_example"; // String | 
    String contentType = "application/json"; // String | 
    try {
      ViewAccountUsage result = apiInstance.viewAccountUsage(year, month, contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ManagementOtherApi#viewAccountUsage");
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
| **year** | **String**|  | |
| **month** | **String**|  | |
| **contentType** | **String**|  | [optional] |

### Return type

[**ViewAccountUsage**](ViewAccountUsage.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

