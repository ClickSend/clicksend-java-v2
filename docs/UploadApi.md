# UploadApi

All URIs are relative to *https://rest.clicksend.com/v3*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**uploadsPost**](UploadApi.md#uploadsPost) | **POST** /uploads | Upload File |


<a id="uploadsPost"></a>
# **uploadsPost**
> String uploadsPost(convert, uploadFile)

Upload File

Upload File

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.UploadApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com/v3");
    
    // Configure HTTP basic authorization: BasicAuth
    HttpBasicAuth BasicAuth = (HttpBasicAuth) defaultClient.getAuthentication("BasicAuth");
    BasicAuth.setUsername("YOUR USERNAME");
    BasicAuth.setPassword("YOUR PASSWORD");

    UploadApi apiInstance = new UploadApi(defaultClient);
    String convert = "convert_example"; // String | 
    UploadFile uploadFile = new UploadFile(); // UploadFile | Your file to be uploaded
    try {
      String result = apiInstance.uploadsPost(convert, uploadFile);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling UploadApi#uploadsPost");
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
| **convert** | **String**|  | |
| **uploadFile** | [**UploadFile**](UploadFile.md)| Your file to be uploaded | |

### Return type

**String**

### Authorization

[BasicAuth](../README.md#BasicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | SUCCESS |  -  |
| **400** | BAD_REQUEST |  -  |
| **401** | UNAUTHORIZED |  -  |
| **403** | FORBIDDEN |  -  |
| **404** | NOT_FOUND |  -  |
| **405** | METHOD_NOT_FOUND |  -  |
| **429** | TOO_MANY_REQUESTS |  -  |
| **0** | INTERNAL_SERVER_ERROR |  -  |

