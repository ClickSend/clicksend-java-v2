# UploadsOtherApi

All URIs are relative to *https://rest.clicksend.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**uploadAMediaFile**](UploadsOtherApi.md#uploadAMediaFile) | **POST** /v3/uploads | Upload Media File |


<a id="uploadAMediaFile"></a>
# **uploadAMediaFile**
> uploadAMediaFile(contentType, body)

Upload Media File

The &#x60;upload&#x60; endpoint provides a method for converting files from an unsupported format to a format that one of our endpoints can handle.  Files can be submitted two ways: 1. Using &#x60;base64&#x60; encoding in an &#x60;application/json&#x60; request. In this case, submit the &#x60;base64&#x60;\\-encoded file contents in the &#x60;content&#x60; field of the request body, and &#x60;convert&#x60; can be specified either also in the body or as part of the query string. 2. Using &#x60;multipart/form-data&#x60; encoding, in the same way it would be submitted using a HTML form. You may find cURL useful for this. For an example of how to do this, see one of our [SDKs](https://dashboard.clicksend.com/#/libraries-sdk/main). In this case, specify &#x60;convert&#x60; in the query string.  Note that &#x60;convert&#x60; specifies the conversion to take place. That is, what the result should be compatible with and can be any of the following:  - &#x60;fax&#x60; - &#x60;mms&#x60; - &#x60;csv&#x60; - &#x60;post&#x60; - &#x60;postcard&#x60;       All files will expire 10 minutes after being uploaded.  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | convert | query | string | true | none | | content | body | string | true | Base64-encoded file contents |  Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.  This endpoint requires authentication, [more info...](/#authentication)

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.UploadsOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    UploadsOtherApi apiInstance = new UploadsOtherApi(defaultClient);
    String contentType = "application/json"; // String | 
    Object body = null; // Object | 
    try {
      apiInstance.uploadAMediaFile(contentType, body);
    } catch (ApiException e) {
      System.err.println("Exception when calling UploadsOtherApi#uploadAMediaFile");
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

null (empty response body)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

