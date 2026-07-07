# OwnNumbersOtherApi

All URIs are relative to *https://rest.clicksend.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**deleteOwnNumber**](OwnNumbersOtherApi.md#deleteOwnNumber) | **DELETE** /v3/own-numbers/{own_number_id} | Delete Own Number |
| [**getOwnNumberDetail**](OwnNumbersOtherApi.md#getOwnNumberDetail) | **GET** /v3/own-numbers/{own_number_id} | Get Own Number Detail |
| [**listOwnNumbers**](OwnNumbersOtherApi.md#listOwnNumbers) | **GET** /v3/own-numbers | List Own Numbers |
| [**requestOwnNumberVerificationOtp**](OwnNumbersOtherApi.md#requestOwnNumberVerificationOtp) | **POST** /v3/own-numbers/verifications | Request Own Number Verification OTP |
| [**updateOwnNumber**](OwnNumbersOtherApi.md#updateOwnNumber) | **PATCH** /v3/own-numbers/{own_number_id} | Update Own Number |
| [**verifyOwnNumberOtp**](OwnNumbersOtherApi.md#verifyOwnNumberOtp) | **POST** /v3/own-numbers/verifications/{verification_id}/verify | Verify Own Number OTP |


<a id="deleteOwnNumber"></a>
# **deleteOwnNumber**
> OwnNumber deleteOwnNumber(ownNumberId, contentType)

Delete Own Number

_Delete a specific own numbers._  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | own_number_id | path | uuid | true | ID of the own number |  Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.  This endpoint requires authentication, [more info...](/#authentication)

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.OwnNumbersOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    OwnNumbersOtherApi apiInstance = new OwnNumbersOtherApi(defaultClient);
    String ownNumberId = "ownNumberId_example"; // String | 
    String contentType = "application/json"; // String | 
    try {
      OwnNumber result = apiInstance.deleteOwnNumber(ownNumberId, contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling OwnNumbersOtherApi#deleteOwnNumber");
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
| **ownNumberId** | **String**|  | |
| **contentType** | **String**|  | [optional] |

### Return type

[**OwnNumber**](OwnNumber.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="getOwnNumberDetail"></a>
# **getOwnNumberDetail**
> OwnNumber getOwnNumberDetail(ownNumberId, contentType)

Get Own Number Detail

_Get a specific own numbers._  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | own_number_id | path | uuid | true | ID of the own number |  Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.  This endpoint requires authentication, [more info...](/#authentication)

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.OwnNumbersOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    OwnNumbersOtherApi apiInstance = new OwnNumbersOtherApi(defaultClient);
    String ownNumberId = "ownNumberId_example"; // String | 
    String contentType = "application/json"; // String | 
    try {
      OwnNumber result = apiInstance.getOwnNumberDetail(ownNumberId, contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling OwnNumbersOtherApi#getOwnNumberDetail");
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
| **ownNumberId** | **String**|  | |
| **contentType** | **String**|  | [optional] |

### Return type

[**OwnNumber**](OwnNumber.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="listOwnNumbers"></a>
# **listOwnNumbers**
> ListOwnNumbers listOwnNumbers(contentType)

List Own Numbers

_List own numbers._  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | offset | query | uuid | false | Page(offset) to be used for pagination. Example: &#x60;offset&#x3D;f99872cc-11a6-48ba-a9f2-bcfb6dd1e3d4#8fa5ebc2-777b-45db-a448-ec76a40d4384&#x60; | | page_size | query | integer | false | Number of records per page. Default: 10. Range \\[1..500\\] | | filter\\[status\\]\\[\\] | query | string | false | Filter by statuses. Value must be in enum \\[&#x60;PENDING&#x60;, &#x60;APPROVED&#x60;, &#x60;REJECTED&#x60;\\]. For example: &#x60;filter[status][0]&#x3D;PENDING&amp;filter[status][1]&#x3D;APPROVED&#x60; . | | sort_by | query | string | false | Sort by parameter. Default: &#x60;created_timestamp&#x60; | | sort_direction | query | string | false | Direction of sorting. Default: &#x60;asc&#x60;. Value must be in enum \\[&#x60;asc&#x60;, &#x60;desc&#x60;\\]. |  Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   This endpoint requires authentication, [more info...](/#authentication)

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.OwnNumbersOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    OwnNumbersOtherApi apiInstance = new OwnNumbersOtherApi(defaultClient);
    String contentType = "application/json"; // String | 
    try {
      ListOwnNumbers result = apiInstance.listOwnNumbers(contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling OwnNumbersOtherApi#listOwnNumbers");
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

[**ListOwnNumbers**](ListOwnNumbers.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="requestOwnNumberVerificationOtp"></a>
# **requestOwnNumberVerificationOtp**
> RequestOwnNumberVerificationOtp requestOwnNumberVerificationOtp(contentType, requestOwnNumberVerificationOtpRequest)

Request Own Number Verification OTP

_Request to generate own number verification OTP_  ### Properties  | Name | Type | Required | Restrictions | Description | | --- | --- | --- | --- | --- | | label | string | false | none | Custom label for phone number. Length must be between 1 - 200 characters. | | phone_number | string | true | none | Phone number. | | country | string | false | none | Country code. |  Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.  This endpoint requires authentication, [more info...](/#authentication)

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.OwnNumbersOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    OwnNumbersOtherApi apiInstance = new OwnNumbersOtherApi(defaultClient);
    String contentType = "application/json"; // String | 
    RequestOwnNumberVerificationOtpRequest requestOwnNumberVerificationOtpRequest = new RequestOwnNumberVerificationOtpRequest(); // RequestOwnNumberVerificationOtpRequest | 
    try {
      RequestOwnNumberVerificationOtp result = apiInstance.requestOwnNumberVerificationOtp(contentType, requestOwnNumberVerificationOtpRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling OwnNumbersOtherApi#requestOwnNumberVerificationOtp");
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
| **requestOwnNumberVerificationOtpRequest** | [**RequestOwnNumberVerificationOtpRequest**](RequestOwnNumberVerificationOtpRequest.md)|  | [optional] |

### Return type

[**RequestOwnNumberVerificationOtp**](RequestOwnNumberVerificationOtp.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="updateOwnNumber"></a>
# **updateOwnNumber**
> OwnNumber updateOwnNumber(ownNumberId)

Update Own Number

_Update details of a specific own numbers._  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | own_number_id | path | uuid | true | ID of the own number |  ### Properties  | Name | Type | Required | Restrictions | Description | | --- | --- | --- | --- | --- | | label | string | false | none | Custom label for phone number. Length must be between 1 - 200 characters. |  Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.  This endpoint requires authentication, [more info...](/#authentication)

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.models.*;
import org.openapitools.client.api.OwnNumbersOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");

    OwnNumbersOtherApi apiInstance = new OwnNumbersOtherApi(defaultClient);
    String ownNumberId = "ownNumberId_example"; // String | 
    try {
      OwnNumber result = apiInstance.updateOwnNumber(ownNumberId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling OwnNumbersOtherApi#updateOwnNumber");
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
| **ownNumberId** | **String**|  | |

### Return type

[**OwnNumber**](OwnNumber.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="verifyOwnNumberOtp"></a>
# **verifyOwnNumberOtp**
> VerifyOwnNumberOtp verifyOwnNumberOtp(verificationId, contentType, verifyOwnNumberOtpRequest)

Verify Own Number OTP

_Request to verify an OTP for Own Number verification_  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | verification_id | path | uuid | true | ID of the Own Number verification |  ### Properties  | Name | Type | Required | Restrictions | Description | | --- | --- | --- | --- | --- | | code | string | true | none | OTP code. Length must be 6 characters | | phone_number | string | true | none | Phone number. | | country | string | false | none | Country code. |  Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.  This endpoint requires authentication, [more info...](/#authentication)

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.OwnNumbersOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    OwnNumbersOtherApi apiInstance = new OwnNumbersOtherApi(defaultClient);
    String verificationId = "verificationId_example"; // String | 
    String contentType = "application/json"; // String | 
    VerifyOwnNumberOtpRequest verifyOwnNumberOtpRequest = new VerifyOwnNumberOtpRequest(); // VerifyOwnNumberOtpRequest | 
    try {
      VerifyOwnNumberOtp result = apiInstance.verifyOwnNumberOtp(verificationId, contentType, verifyOwnNumberOtpRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling OwnNumbersOtherApi#verifyOwnNumberOtp");
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
| **verificationId** | **String**|  | |
| **contentType** | **String**|  | [optional] |
| **verifyOwnNumberOtpRequest** | [**VerifyOwnNumberOtpRequest**](VerifyOwnNumberOtpRequest.md)|  | [optional] |

### Return type

[**VerifyOwnNumberOtp**](VerifyOwnNumberOtp.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

