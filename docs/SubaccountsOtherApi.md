# SubaccountsOtherApi

All URIs are relative to *https://rest.clicksend.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createSubaccount**](SubaccountsOtherApi.md#createSubaccount) | **POST** /v3/subaccounts | Create Subaccount |
| [**deleteSubaccount**](SubaccountsOtherApi.md#deleteSubaccount) | **DELETE** /v3/subaccounts/{subaccount_id} | Delete Subaccount |
| [**generateNewApiKey**](SubaccountsOtherApi.md#generateNewApiKey) | **PUT** /v3/subaccounts/{subaccount_id}/regen-api-key | Generate New API Key |
| [**updateSubaccount**](SubaccountsOtherApi.md#updateSubaccount) | **PUT** /v3/subaccounts/{subaccount_id} | Update Subaccount |
| [**viewSpecificSubaccount**](SubaccountsOtherApi.md#viewSpecificSubaccount) | **GET** /v3/subaccounts/{subaccount_id} | View Specific Subaccount |
| [**viewSubaccounts**](SubaccountsOtherApi.md#viewSubaccounts) | **GET** /v3/subaccounts | View Subaccounts |


<a id="createSubaccount"></a>
# **createSubaccount**
> CreateSubaccount createSubaccount(contentType, createSubaccountRequest)

Create Subaccount

_Create new subaccount_  ### Properties  | Name | Type | Required | Restrictions | Description | | --- | --- | --- | --- | --- | | api_username | string | true | none | Your new api username. | | password | string | true | none | Your new password | | email | string | true | none | Your new email. | | phone_number | string | true | none | Your phone number in [E.164](https://en.wikipedia.org/wiki/E.164) format. | | first_name | string | true | none | Your firstname | | last_name | string | true | none | Your lastname | | access_users | integer(int1) | false | none | Flag value must be 1 for yes or 0 for no. | | access_billing | integer(int1) | false | none | Flag value must be 1 for yes or 0 for no. | | access_reporting | integer(int1) | false | none | Flag value must be 1 for yes or 0 for no. | | access_contacts | integer(int1) | false | none | Flag value must be 1 for yes or 0 for no. | | access_settings | integer(int1) | false | none | Flag value must be 1 for yes or 0 for no. |  Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.  &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.SubaccountsOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    SubaccountsOtherApi apiInstance = new SubaccountsOtherApi(defaultClient);
    String contentType = "application/json"; // String | 
    CreateSubaccountRequest createSubaccountRequest = new CreateSubaccountRequest(); // CreateSubaccountRequest | 
    try {
      CreateSubaccount result = apiInstance.createSubaccount(contentType, createSubaccountRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SubaccountsOtherApi#createSubaccount");
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
| **createSubaccountRequest** | [**CreateSubaccountRequest**](CreateSubaccountRequest.md)|  | [optional] |

### Return type

[**CreateSubaccount**](CreateSubaccount.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="deleteSubaccount"></a>
# **deleteSubaccount**
> DeleteSubaccount deleteSubaccount(subaccountId, contentType)

Delete Subaccount

_Delete a subaccount_  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | subaccount_id | path | integer(int32) | true | ID of subaccount to delete |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.SubaccountsOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    SubaccountsOtherApi apiInstance = new SubaccountsOtherApi(defaultClient);
    String subaccountId = "subaccountId_example"; // String | 
    String contentType = "application/json"; // String | 
    try {
      DeleteSubaccount result = apiInstance.deleteSubaccount(subaccountId, contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SubaccountsOtherApi#deleteSubaccount");
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
| **subaccountId** | **String**|  | |
| **contentType** | **String**|  | [optional] |

### Return type

[**DeleteSubaccount**](DeleteSubaccount.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="generateNewApiKey"></a>
# **generateNewApiKey**
> GenerateNewApiKey generateNewApiKey(subaccountId, contentType, generateNewApiKeyRequest)

Generate New API Key

_Regenerate an API Key_  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | subaccount_id | path | integer(int32) | true | ID of subaccount to regenerate API key for |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.SubaccountsOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    SubaccountsOtherApi apiInstance = new SubaccountsOtherApi(defaultClient);
    String subaccountId = "subaccountId_example"; // String | 
    String contentType = "application/json"; // String | 
    GenerateNewApiKeyRequest generateNewApiKeyRequest = new GenerateNewApiKeyRequest(); // GenerateNewApiKeyRequest | 
    try {
      GenerateNewApiKey result = apiInstance.generateNewApiKey(subaccountId, contentType, generateNewApiKeyRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SubaccountsOtherApi#generateNewApiKey");
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
| **subaccountId** | **String**|  | |
| **contentType** | **String**|  | [optional] |
| **generateNewApiKeyRequest** | [**GenerateNewApiKeyRequest**](GenerateNewApiKeyRequest.md)|  | [optional] |

### Return type

[**GenerateNewApiKey**](GenerateNewApiKey.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="updateSubaccount"></a>
# **updateSubaccount**
> UpdateSubaccount updateSubaccount(subaccountId, contentType, updateSubaccountRequest)

Update Subaccount

_Update subaccount_  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | subaccount_id | path | integer(int32) | true | ID of subaccount to update |  ### Properties  | Name | Type | Required | Restrictions | Description | | --- | --- | --- | --- | --- | | api_username | string | true | none | Your new api username. | | password | string | true | none | Your new password | | email | string | true | none | Your new email. | | phone_number | string | true | none | Your phone number in [E.164](https://en.wikipedia.org/wiki/E.164) format. | | first_name | string | true | none | Your firstname | | last_name | string | true | none | Your lastname | | access_users | integer(int1) | false | none | Flag value must be 1 for yes or 0 for no. | | access_billing | integer(int1) | false | none | Flag value must be 1 for yes or 0 for no. | | access_reporting | integer(int1) | false | none | Flag value must be 1 for yes or 0 for no. | | access_contacts | integer(int1) | false | none | Flag value must be 1 for yes or 0 for no. | | access_settings | integer(int1) | false | none | Flag value must be 1 for yes or 0 for no. |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.SubaccountsOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    SubaccountsOtherApi apiInstance = new SubaccountsOtherApi(defaultClient);
    String subaccountId = "subaccountId_example"; // String | 
    String contentType = "application/json"; // String | 
    UpdateSubaccountRequest updateSubaccountRequest = new UpdateSubaccountRequest(); // UpdateSubaccountRequest | 
    try {
      UpdateSubaccount result = apiInstance.updateSubaccount(subaccountId, contentType, updateSubaccountRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SubaccountsOtherApi#updateSubaccount");
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
| **subaccountId** | **String**|  | |
| **contentType** | **String**|  | [optional] |
| **updateSubaccountRequest** | [**UpdateSubaccountRequest**](UpdateSubaccountRequest.md)|  | [optional] |

### Return type

[**UpdateSubaccount**](UpdateSubaccount.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewSpecificSubaccount"></a>
# **viewSpecificSubaccount**
> ViewSpecificSubaccount viewSpecificSubaccount(subaccountId, contentType)

View Specific Subaccount

_Get specific subaccount_  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | subaccount_id | path | integer(int32) | true | ID of subaccount to get |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.SubaccountsOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    SubaccountsOtherApi apiInstance = new SubaccountsOtherApi(defaultClient);
    String subaccountId = "subaccountId_example"; // String | 
    String contentType = "application/json"; // String | 
    try {
      ViewSpecificSubaccount result = apiInstance.viewSpecificSubaccount(subaccountId, contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SubaccountsOtherApi#viewSpecificSubaccount");
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
| **subaccountId** | **String**|  | |
| **contentType** | **String**|  | [optional] |

### Return type

[**ViewSpecificSubaccount**](ViewSpecificSubaccount.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewSubaccounts"></a>
# **viewSubaccounts**
> ViewSubaccounts viewSubaccounts(contentType)

View Subaccounts

_Get all subaccounts_  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | page | query | integer(int32) | false | [Page number](/#pagination) | | limit | query | integer(int32) | false | [Number of records per page](/#pagination) |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.SubaccountsOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    SubaccountsOtherApi apiInstance = new SubaccountsOtherApi(defaultClient);
    String contentType = "application/json"; // String | 
    try {
      ViewSubaccounts result = apiInstance.viewSubaccounts(contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SubaccountsOtherApi#viewSubaccounts");
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

[**ViewSubaccounts**](ViewSubaccounts.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

