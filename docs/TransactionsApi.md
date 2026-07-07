# TransactionsApi

All URIs are relative to *https://rest.clicksend.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**currentPaymentInfo**](TransactionsApi.md#currentPaymentInfo) | **GET** /v3/recharge/credit-card | Current Payment Info |
| [**purchaseRechargePackage**](TransactionsApi.md#purchaseRechargePackage) | **PUT** /v3/recharge/purchase/{package_id} | Purchase Recharge Package |
| [**updatePaymentInfo**](TransactionsApi.md#updatePaymentInfo) | **PUT** /v3/recharge/credit-card | Update Payment Info |
| [**viewAllTransactions**](TransactionsApi.md#viewAllTransactions) | **GET** /v3/recharge/transactions | View All Transactions |
| [**viewRechargePackages**](TransactionsApi.md#viewRechargePackages) | **GET** /v3/recharge/packages | View Recharge Packages |
| [**viewSpecificTransaction**](TransactionsApi.md#viewSpecificTransaction) | **GET** /v3/recharge/transactions/{transaction_id} | View Specific Transaction |


<a id="currentPaymentInfo"></a>
# **currentPaymentInfo**
> CurrentPaymentInfo currentPaymentInfo(contentType)

Current Payment Info

_Get current payment info_  This endpoint returns your current payment info, we do not store credit card numbers, only a card token for security reasons.  Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.TransactionsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    TransactionsApi apiInstance = new TransactionsApi(defaultClient);
    String contentType = "application/json"; // String | 
    try {
      CurrentPaymentInfo result = apiInstance.currentPaymentInfo(contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TransactionsApi#currentPaymentInfo");
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

[**CurrentPaymentInfo**](CurrentPaymentInfo.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="purchaseRechargePackage"></a>
# **purchaseRechargePackage**
> PurchaseRechargePackage purchaseRechargePackage(packageId, contentType)

Purchase Recharge Package

_Purchase a package_  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | package_id | path | integer(int32) | true | ID of package to purchase |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.TransactionsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    TransactionsApi apiInstance = new TransactionsApi(defaultClient);
    String packageId = "packageId_example"; // String | 
    String contentType = "application/x-www-form-urlencoded"; // String | 
    try {
      PurchaseRechargePackage result = apiInstance.purchaseRechargePackage(packageId, contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TransactionsApi#purchaseRechargePackage");
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
| **packageId** | **String**|  | |
| **contentType** | **String**|  | [optional] |

### Return type

[**PurchaseRechargePackage**](PurchaseRechargePackage.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="updatePaymentInfo"></a>
# **updatePaymentInfo**
> UpdatePaymentInfo updatePaymentInfo(contentType, updatePaymentInfoRequest)

Update Payment Info

_Update credit card info_  ### Properties  | Name | Type | Required | Restrictions | Description | | --- | --- | --- | --- | --- | | number | string | true | none | Credit card number | | expiry_month | integer(int32) | true | none | Expiry month of credit card | | expiry_year | integer(int32) | true | none | Expiry year of credit card | | cvc | integer(int32) | true | none | CVC number of credit card | | name | string | true | none | Name printed on credit card | | bank_name | string | true | none | Name of bank that credit card belongs to |  Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.TransactionsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    TransactionsApi apiInstance = new TransactionsApi(defaultClient);
    String contentType = "application/x-www-form-urlencoded"; // String | 
    UpdatePaymentInfoRequest updatePaymentInfoRequest = new UpdatePaymentInfoRequest(); // UpdatePaymentInfoRequest | 
    try {
      UpdatePaymentInfo result = apiInstance.updatePaymentInfo(contentType, updatePaymentInfoRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TransactionsApi#updatePaymentInfo");
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

[**UpdatePaymentInfo**](UpdatePaymentInfo.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewAllTransactions"></a>
# **viewAllTransactions**
> ViewAllTransactions viewAllTransactions(contentType)

View All Transactions

_Purchase a package_  Get all transactions  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | page | query | integer(int32) | false | [Page number](/#pagination) | | limit | query | integer(int32) | false | [Number of records per page](/#pagination) |  Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.TransactionsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    TransactionsApi apiInstance = new TransactionsApi(defaultClient);
    String contentType = "application/json"; // String | 
    try {
      ViewAllTransactions result = apiInstance.viewAllTransactions(contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TransactionsApi#viewAllTransactions");
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

[**ViewAllTransactions**](ViewAllTransactions.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewRechargePackages"></a>
# **viewRechargePackages**
> ViewRechargePackages viewRechargePackages(contentType)

View Recharge Packages

_Get list of all packages_  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | country | query | string | false | Two-letter country code ([ISO3166](https://en.wikipedia.org/wiki/ISO_3166)) |  Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.TransactionsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    TransactionsApi apiInstance = new TransactionsApi(defaultClient);
    String contentType = "application/json"; // String | 
    try {
      ViewRechargePackages result = apiInstance.viewRechargePackages(contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TransactionsApi#viewRechargePackages");
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

[**ViewRechargePackages**](ViewRechargePackages.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewSpecificTransaction"></a>
# **viewSpecificTransaction**
> ViewSpecificTransaction viewSpecificTransaction(transactionId, contentType)

View Specific Transaction

_Get specific Transaction_  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | transaction_id | path | string | true | ID of transaction to retrieve |  Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.TransactionsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    TransactionsApi apiInstance = new TransactionsApi(defaultClient);
    String transactionId = "transactionId_example"; // String | 
    String contentType = "application/json"; // String | 
    try {
      ViewSpecificTransaction result = apiInstance.viewSpecificTransaction(transactionId, contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TransactionsApi#viewSpecificTransaction");
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
| **transactionId** | **String**|  | |
| **contentType** | **String**|  | [optional] |

### Return type

[**ViewSpecificTransaction**](ViewSpecificTransaction.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

