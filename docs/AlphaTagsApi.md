# AlphaTagsApi

All URIs are relative to *https://rest.clicksend.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**deleteAlphaTag**](AlphaTagsApi.md#deleteAlphaTag) | **DELETE** /v3/alpha-tags/{alpha_tag_id} | Delete Alpha Tag |
| [**getAlphaTag**](AlphaTagsApi.md#getAlphaTag) | **GET** /v3/alpha-tags/{alpha_tag_id} | Get Alpha Tag |
| [**listAlphaTags**](AlphaTagsApi.md#listAlphaTags) | **GET** /v3/alpha-tags | List Alpha Tags |
| [**requestAlphaTag**](AlphaTagsApi.md#requestAlphaTag) | **POST** /v3/alpha-tags | Request Alpha Tag |


<a id="deleteAlphaTag"></a>
# **deleteAlphaTag**
> deleteAlphaTag(alphaTagId, contentType)

Delete Alpha Tag

_Delete a specific alpha tag._  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | alpha_tag_id | path | uuid | true | ID of the alpha tag |  Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.  This endpoint requires authentication, [more info...](/#authentication)

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.AlphaTagsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    AlphaTagsApi apiInstance = new AlphaTagsApi(defaultClient);
    String alphaTagId = "alphaTagId_example"; // String | 
    String contentType = "application/json"; // String | 
    try {
      apiInstance.deleteAlphaTag(alphaTagId, contentType);
    } catch (ApiException e) {
      System.err.println("Exception when calling AlphaTagsApi#deleteAlphaTag");
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
| **alphaTagId** | **String**|  | |
| **contentType** | **String**|  | [optional] |

### Return type

null (empty response body)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="getAlphaTag"></a>
# **getAlphaTag**
> AlphaTag getAlphaTag(alphaTagId, contentType)

Get Alpha Tag

_Get a specific alpha tag._  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | alpha_tag_id | path | uuid | true | ID of the alpha tag |  Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   This endpoint requires authentication, [more info...](/#authentication)

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.AlphaTagsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    AlphaTagsApi apiInstance = new AlphaTagsApi(defaultClient);
    String alphaTagId = "alphaTagId_example"; // String | 
    String contentType = "application/json"; // String | 
    try {
      AlphaTag result = apiInstance.getAlphaTag(alphaTagId, contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AlphaTagsApi#getAlphaTag");
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
| **alphaTagId** | **String**|  | |
| **contentType** | **String**|  | [optional] |

### Return type

[**AlphaTag**](AlphaTag.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="listAlphaTags"></a>
# **listAlphaTags**
> ListAlphaTags listAlphaTags(sortDirection, pageSize)

List Alpha Tags



### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.AlphaTagsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    AlphaTagsApi apiInstance = new AlphaTagsApi(defaultClient);
    String sortDirection = "asc"; // String | The sort direction for the results. The default value is asc.
    Integer pageSize = 10; // Integer | The number of items to return per page. This parameter controls the size of each page of results. The default value is 10.
    try {
      ListAlphaTags result = apiInstance.listAlphaTags(sortDirection, pageSize);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AlphaTagsApi#listAlphaTags");
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
| **sortDirection** | **String**| The sort direction for the results. The default value is asc. | [optional] [default to asc] [enum: asc, desc] |
| **pageSize** | **Integer**| The number of items to return per page. This parameter controls the size of each page of results. The default value is 10. | [optional] [default to 10] |

### Return type

[**ListAlphaTags**](ListAlphaTags.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="requestAlphaTag"></a>
# **requestAlphaTag**
> AlphaTag requestAlphaTag(contentType, requestAlphaTagRequest)

Request Alpha Tag

_Request to register an alpha tag. After requested, the alpha tag will be reviewed by ClickSend and either approved or rejected. Some countries (e.g Australia) require you to submit additional fields due to government mandated compliance checks._  ### Properties  | Name | Type | Required | Restrictions | Description | | --- | --- | --- | --- | --- | | alpha_tag | string | true | [yes](https://help.clicksend.com/article/1qxfxkcwm2-global-generic-alpha-tags) | The alpha tag name. Length must be between 3 - 11 characters, can only contain a-z A-Z 0-9 + and must contain at least one non numeric. | | reason | string | false | none | Must be one of the following: &#x60;Sole Trader Name&#x60;, &#x60;Company Name&#x60;, &#x60;Partnership Name&#x60;, &#x60;Registered Trust Name&#x60;, &#x60;Co-Operative Name&#x60;, &#x60;Indigenous Corporation Name&#x60;, &#x60;Registered Organisation Name&#x60;, &#x60;Personal Name&#x60;, &#x60;Trademark&#x60;, &#x60;Government Agency or Entity&#x60;, &#x60;Product or Service Name&#x60;, &#x60;Acronym/Initialism&#x60;, &#x60;Contraction of Name&#x60;, &#x60;Third Party&#x60;. In case of &#x60;Third Party&#x60;, we will contact you to collect the relevant information. | | countries | array of strings | false | none | List of country codes (e.g., \&quot;AU\&quot;, \&quot;US\&quot;) where the alpha tag is requested. Only supported and required for AU. | | businesses | array of objects | false | none | List of business details required for alpha tag registration. Each object contains country, business information, ... Required if &#x60;countries&#x60; is provided. When &#x60;business_relationship&#x60; is &#x60;ENTITY_ASSOCIATE&#x60;, the following partner fields are also **required**: &#x60;partner_business_name&#x60;, &#x60;partner_abn&#x60;, &#x60;partner_business_info&#x60;, &#x60;partner_business_address&#x60;, &#x60;partner_representative&#x60;. These fields are **forbidden** for any other &#x60;business_relationship&#x60; value. |  Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.  _This endpoint requires authentication,_ [more info...](/#authentication) 

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.AlphaTagsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    AlphaTagsApi apiInstance = new AlphaTagsApi(defaultClient);
    String contentType = "application/json"; // String | 
    RequestAlphaTagRequest requestAlphaTagRequest = new RequestAlphaTagRequest(); // RequestAlphaTagRequest | 
    try {
      AlphaTag result = apiInstance.requestAlphaTag(contentType, requestAlphaTagRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AlphaTagsApi#requestAlphaTag");
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
| **requestAlphaTagRequest** | [**RequestAlphaTagRequest**](RequestAlphaTagRequest.md)|  | [optional] |

### Return type

[**AlphaTag**](AlphaTag.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

