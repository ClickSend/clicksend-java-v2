# ResellerOtherApi

All URIs are relative to *https://rest.clicksend.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createResellerAccount**](ResellerOtherApi.md#createResellerAccount) | **POST** /v3/reseller/accounts | Create Reseller Account |
| [**resellerTransferCredit**](ResellerOtherApi.md#resellerTransferCredit) | **PUT** /v3/reseller/transfer-credit | Reseller Transfer Credit |
| [**updateClientAccount**](ResellerOtherApi.md#updateClientAccount) | **PUT** /v3/reseller/accounts/{client_user_id} | Update Client Account |
| [**viewClientAccounts**](ResellerOtherApi.md#viewClientAccounts) | **GET** /v3/reseller/accounts | View Client Accounts |
| [**viewSpecificClientAccount**](ResellerOtherApi.md#viewSpecificClientAccount) | **GET** /v3/reseller/accounts/{client_user_id} | View Specific Client Account |


<a id="createResellerAccount"></a>
# **createResellerAccount**
> CreateResellerAccount createResellerAccount(contentType, createResellerAccountRequest)

Create Reseller Account

_Create reseller account_  ### Properties  | Name | Type | Required | Restrictions | Description | | --- | --- | --- | --- | --- | | username | string | true | none | Account username | | password | string | true | none | Account password (unhashed) | | user_email | string | true | none | Account email | | user_phone | string | true | none | Account phone number | | user_first_name | string | true | none | Account owner first name | | user_last_name | string | true | none | Account owner last name | | account_name | string | true | none | Account name (usually company name) | | country | string | true | none | Country of account holder |  Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.ResellerOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    ResellerOtherApi apiInstance = new ResellerOtherApi(defaultClient);
    String contentType = "application/json"; // String | 
    CreateResellerAccountRequest createResellerAccountRequest = new CreateResellerAccountRequest(); // CreateResellerAccountRequest | 
    try {
      CreateResellerAccount result = apiInstance.createResellerAccount(contentType, createResellerAccountRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ResellerOtherApi#createResellerAccount");
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
| **createResellerAccountRequest** | [**CreateResellerAccountRequest**](CreateResellerAccountRequest.md)|  | [optional] |

### Return type

[**CreateResellerAccount**](CreateResellerAccount.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="resellerTransferCredit"></a>
# **resellerTransferCredit**
> ResellerTransferCredit resellerTransferCredit(contentType, updatePaymentInfoRequest)

Reseller Transfer Credit

_Transfer Credit_  ### Properties  | Name | Type | Required | Restrictions | Description | | --- | --- | --- | --- | --- | | client_user_id | integer(int32) | true | none | User ID of client | | balance | integer(int32) | true | none | Balance to transfer | | currency | string | true | none | Currency of balance to transfer |  Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.  &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.ResellerOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    ResellerOtherApi apiInstance = new ResellerOtherApi(defaultClient);
    String contentType = "application/x-www-form-urlencoded"; // String | 
    UpdatePaymentInfoRequest updatePaymentInfoRequest = new UpdatePaymentInfoRequest(); // UpdatePaymentInfoRequest | 
    try {
      ResellerTransferCredit result = apiInstance.resellerTransferCredit(contentType, updatePaymentInfoRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ResellerOtherApi#resellerTransferCredit");
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
| **updatePaymentInfoRequest** | [**UpdatePaymentInfoRequest**](UpdatePaymentInfoRequest.md)|  | [optional] |

### Return type

[**ResellerTransferCredit**](ResellerTransferCredit.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="updateClientAccount"></a>
# **updateClientAccount**
> UpdateClientAccount updateClientAccount(clientUserId, contentType, updatePaymentInfoRequest)

Update Client Account

_Update Reseller clients Account_  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | client_user_id | path | integer(int32) | true | User ID of client |  ### Properties  | Name | Type | Required | Restrictions | Description | | --- | --- | --- | --- | --- | | username | string | true | none | Account username | | password | string | true | none | Account password (unhashed) | | user_email | string | true | none | Account email | | user_phone | string | true | none | Account phone number | | user_first_name | string | true | none | Account owner first name | | user_last_name | string | true | none | Account owner last name | | account_name | string | true | none | Account name (usually company name) | | country | string | true | none | Country of account holder |  Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.  &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.ResellerOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    ResellerOtherApi apiInstance = new ResellerOtherApi(defaultClient);
    String clientUserId = "clientUserId_example"; // String | 
    String contentType = "application/x-www-form-urlencoded"; // String | 
    UpdatePaymentInfoRequest updatePaymentInfoRequest = new UpdatePaymentInfoRequest(); // UpdatePaymentInfoRequest | 
    try {
      UpdateClientAccount result = apiInstance.updateClientAccount(clientUserId, contentType, updatePaymentInfoRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ResellerOtherApi#updateClientAccount");
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
| **clientUserId** | **String**|  | |
| **contentType** | **String**|  | [optional] |
| **updatePaymentInfoRequest** | [**UpdatePaymentInfoRequest**](UpdatePaymentInfoRequest.md)|  | [optional] |

### Return type

[**UpdateClientAccount**](UpdateClientAccount.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewClientAccounts"></a>
# **viewClientAccounts**
> ViewClientAccounts viewClientAccounts(contentType)

View Client Accounts

_Get list of reseller accounts_  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | page | query | integer(int32) | false | [Page number](/#pagination) | | limit | query | integer(int32) | false | [Number of records per page](/#pagination) |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.ResellerOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    ResellerOtherApi apiInstance = new ResellerOtherApi(defaultClient);
    String contentType = "application/json"; // String | 
    try {
      ViewClientAccounts result = apiInstance.viewClientAccounts(contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ResellerOtherApi#viewClientAccounts");
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

[**ViewClientAccounts**](ViewClientAccounts.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewSpecificClientAccount"></a>
# **viewSpecificClientAccount**
> ViewSpecificClientAccount viewSpecificClientAccount(clientUserId, contentType)

View Specific Client Account

_Get Reseller clients Account_  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | client_user_id | path | integer(int32) | true | User ID of client |  Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.  &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.ResellerOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    ResellerOtherApi apiInstance = new ResellerOtherApi(defaultClient);
    String clientUserId = "clientUserId_example"; // String | 
    String contentType = "application/json"; // String | 
    try {
      ViewSpecificClientAccount result = apiInstance.viewSpecificClientAccount(clientUserId, contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ResellerOtherApi#viewSpecificClientAccount");
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
| **clientUserId** | **String**|  | |
| **contentType** | **String**|  | [optional] |

### Return type

[**ViewSpecificClientAccount**](ViewSpecificClientAccount.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

