# AddressesOtherApi

All URIs are relative to *https://rest.clicksend.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createReturnAddress**](AddressesOtherApi.md#createReturnAddress) | **POST** /v3/post/return-addresses | Create Return Address |
| [**deleteReturnAddress**](AddressesOtherApi.md#deleteReturnAddress) | **DELETE** /v3/post/return-addresses/{return_address_id} | Delete Return Address |
| [**updateReturnAddress**](AddressesOtherApi.md#updateReturnAddress) | **PUT** /v3/post/return-addresses/{return_address_id} | Update Return Address |
| [**viewSpecificReturnAddress**](AddressesOtherApi.md#viewSpecificReturnAddress) | **GET** /v3/post/return-addresses/{return_address_id} | View Specific Return Address |
| [**viewYourReturnAddresses**](AddressesOtherApi.md#viewYourReturnAddresses) | **GET** /v3/post/return-addresses | View Your Return Addresses |


<a id="createReturnAddress"></a>
# **createReturnAddress**
> CreateReturnAddress createReturnAddress(contentType, createReturnAddressRequest)

Create Return Address

_Create post return address_  ### Properties  | Name | Type | Required | Restrictions | Description | | --- | --- | --- | --- | --- | | address_name | string | true | none | Your address name. | | address_line_1 | string | true | none | Your address line 1 | | address_city | string | true | none | Your city | | address_postal_code | string | true | none | Your postal code | | address_country | string | true | none | Your country | | address_line_2 | string | false | none | Your address line 2 | | address_state | string | false | none | Your state |    Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.    &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.AddressesOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    AddressesOtherApi apiInstance = new AddressesOtherApi(defaultClient);
    String contentType = "application/json"; // String | 
    CreateReturnAddressRequest createReturnAddressRequest = new CreateReturnAddressRequest(); // CreateReturnAddressRequest | 
    try {
      CreateReturnAddress result = apiInstance.createReturnAddress(contentType, createReturnAddressRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AddressesOtherApi#createReturnAddress");
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
| **createReturnAddressRequest** | [**CreateReturnAddressRequest**](CreateReturnAddressRequest.md)|  | [optional] |

### Return type

[**CreateReturnAddress**](CreateReturnAddress.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="deleteReturnAddress"></a>
# **deleteReturnAddress**
> DeleteReturnAddress deleteReturnAddress(returnAddressId, contentType)

Delete Return Address

_Delete specific post return address_  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | return_address_id | path | integer(int32) | true | Return address ID |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.AddressesOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    AddressesOtherApi apiInstance = new AddressesOtherApi(defaultClient);
    String returnAddressId = "returnAddressId_example"; // String | 
    String contentType = "application/json"; // String | 
    try {
      DeleteReturnAddress result = apiInstance.deleteReturnAddress(returnAddressId, contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AddressesOtherApi#deleteReturnAddress");
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
| **returnAddressId** | **String**|  | |
| **contentType** | **String**|  | [optional] |

### Return type

[**DeleteReturnAddress**](DeleteReturnAddress.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="updateReturnAddress"></a>
# **updateReturnAddress**
> UpdateReturnAddress updateReturnAddress(returnAddressId, contentType, updateReturnAddressRequest)

Update Return Address

_Update post return address_  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | return_address_id | path | integer(int32) | true | Return address ID |  ### Properties  | Name | Type | Required | Restrictions | Description | | --- | --- | --- | --- | --- | | address_name | string | true | none | Your address name. | | address_line_1 | string | true | none | Your address line 1 | | address_city | string | true | none | Your city | | address_postal_code | string | true | none | Your postal code | | address_country | string | true | none | Your country | | address_line_2 | string | false | none | Your address line 2 | | address_state | string | false | none | Your state |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.AddressesOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    AddressesOtherApi apiInstance = new AddressesOtherApi(defaultClient);
    String returnAddressId = "returnAddressId_example"; // String | 
    String contentType = "application/json"; // String | 
    UpdateReturnAddressRequest updateReturnAddressRequest = new UpdateReturnAddressRequest(); // UpdateReturnAddressRequest | 
    try {
      UpdateReturnAddress result = apiInstance.updateReturnAddress(returnAddressId, contentType, updateReturnAddressRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AddressesOtherApi#updateReturnAddress");
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
| **returnAddressId** | **String**|  | |
| **contentType** | **String**|  | [optional] |
| **updateReturnAddressRequest** | [**UpdateReturnAddressRequest**](UpdateReturnAddressRequest.md)|  | [optional] |

### Return type

[**UpdateReturnAddress**](UpdateReturnAddress.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewSpecificReturnAddress"></a>
# **viewSpecificReturnAddress**
> ViewSpecificReturnAddress viewSpecificReturnAddress(returnAddressId, contentType)

View Specific Return Address

_Get specific post return address_  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | return_address_id | path | integer(int32) | true | Return address ID |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.AddressesOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    AddressesOtherApi apiInstance = new AddressesOtherApi(defaultClient);
    String returnAddressId = "returnAddressId_example"; // String | 
    String contentType = "application/json"; // String | 
    try {
      ViewSpecificReturnAddress result = apiInstance.viewSpecificReturnAddress(returnAddressId, contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AddressesOtherApi#viewSpecificReturnAddress");
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
| **returnAddressId** | **String**|  | |
| **contentType** | **String**|  | [optional] |

### Return type

[**ViewSpecificReturnAddress**](ViewSpecificReturnAddress.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewYourReturnAddresses"></a>
# **viewYourReturnAddresses**
> ViewYourReturnAddresses viewYourReturnAddresses(contentType)

View Your Return Addresses

_Get list of post return addresses_  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | page | query | integer(int32) | false | [Page number](/#pagination) | | limit | query | integer(int32) | false | [Number of records per page](/#pagination) |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.AddressesOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    AddressesOtherApi apiInstance = new AddressesOtherApi(defaultClient);
    String contentType = "application/json"; // String | 
    try {
      ViewYourReturnAddresses result = apiInstance.viewYourReturnAddresses(contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AddressesOtherApi#viewYourReturnAddresses");
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

[**ViewYourReturnAddresses**](ViewYourReturnAddresses.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

