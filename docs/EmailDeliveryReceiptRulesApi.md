# EmailDeliveryReceiptRulesApi

All URIs are relative to *https://rest.clicksend.com/v3*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**emailDeliveryReceiptAutomationDelete**](EmailDeliveryReceiptRulesApi.md#emailDeliveryReceiptAutomationDelete) | **DELETE** /automations/email/receipts/{receipt_rule_id} | Delete email delivery receipt automation |
| [**emailDeliveryReceiptAutomationGet**](EmailDeliveryReceiptRulesApi.md#emailDeliveryReceiptAutomationGet) | **GET** /automations/email/receipts/{receipt_rule_id} | Get specific email delivery receipt automation |
| [**emailDeliveryReceiptAutomationPost**](EmailDeliveryReceiptRulesApi.md#emailDeliveryReceiptAutomationPost) | **POST** /automations/email/receipts | Create email delivery receipt automations |
| [**emailDeliveryReceiptAutomationPut**](EmailDeliveryReceiptRulesApi.md#emailDeliveryReceiptAutomationPut) | **PUT** /automations/email/receipts/{receipt_rule_id} | Update email delivery receipt automation |
| [**emailDeliveryReceiptAutomationsGet**](EmailDeliveryReceiptRulesApi.md#emailDeliveryReceiptAutomationsGet) | **GET** /automations/email/receipts | Get all email delivery receipt automations |


<a id="emailDeliveryReceiptAutomationDelete"></a>
# **emailDeliveryReceiptAutomationDelete**
> String emailDeliveryReceiptAutomationDelete(receiptRuleId)

Delete email delivery receipt automation

Delete email delivery receipt automation

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.EmailDeliveryReceiptRulesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com/v3");
    
    // Configure HTTP basic authorization: BasicAuth
    HttpBasicAuth BasicAuth = (HttpBasicAuth) defaultClient.getAuthentication("BasicAuth");
    BasicAuth.setUsername("YOUR USERNAME");
    BasicAuth.setPassword("YOUR PASSWORD");

    EmailDeliveryReceiptRulesApi apiInstance = new EmailDeliveryReceiptRulesApi(defaultClient);
    Integer receiptRuleId = 56; // Integer | Receipt rule id
    try {
      String result = apiInstance.emailDeliveryReceiptAutomationDelete(receiptRuleId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling EmailDeliveryReceiptRulesApi#emailDeliveryReceiptAutomationDelete");
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
| **receiptRuleId** | **Integer**| Receipt rule id | |

### Return type

**String**

### Authorization

[BasicAuth](../README.md#BasicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
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

<a id="emailDeliveryReceiptAutomationGet"></a>
# **emailDeliveryReceiptAutomationGet**
> String emailDeliveryReceiptAutomationGet(receiptRuleId)

Get specific email delivery receipt automation

Get specific email delivery receipt automation

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.EmailDeliveryReceiptRulesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com/v3");
    
    // Configure HTTP basic authorization: BasicAuth
    HttpBasicAuth BasicAuth = (HttpBasicAuth) defaultClient.getAuthentication("BasicAuth");
    BasicAuth.setUsername("YOUR USERNAME");
    BasicAuth.setPassword("YOUR PASSWORD");

    EmailDeliveryReceiptRulesApi apiInstance = new EmailDeliveryReceiptRulesApi(defaultClient);
    Integer receiptRuleId = 56; // Integer | Receipt rule id
    try {
      String result = apiInstance.emailDeliveryReceiptAutomationGet(receiptRuleId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling EmailDeliveryReceiptRulesApi#emailDeliveryReceiptAutomationGet");
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
| **receiptRuleId** | **Integer**| Receipt rule id | |

### Return type

**String**

### Authorization

[BasicAuth](../README.md#BasicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
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

<a id="emailDeliveryReceiptAutomationPost"></a>
# **emailDeliveryReceiptAutomationPost**
> String emailDeliveryReceiptAutomationPost(deliveryReceiptRule)

Create email delivery receipt automations

Create email delivery receipt automations

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.EmailDeliveryReceiptRulesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com/v3");
    
    // Configure HTTP basic authorization: BasicAuth
    HttpBasicAuth BasicAuth = (HttpBasicAuth) defaultClient.getAuthentication("BasicAuth");
    BasicAuth.setUsername("YOUR USERNAME");
    BasicAuth.setPassword("YOUR PASSWORD");

    EmailDeliveryReceiptRulesApi apiInstance = new EmailDeliveryReceiptRulesApi(defaultClient);
    DeliveryReceiptRule deliveryReceiptRule = new DeliveryReceiptRule(); // DeliveryReceiptRule | Email delivery receipt rule model
    try {
      String result = apiInstance.emailDeliveryReceiptAutomationPost(deliveryReceiptRule);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling EmailDeliveryReceiptRulesApi#emailDeliveryReceiptAutomationPost");
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
| **deliveryReceiptRule** | [**DeliveryReceiptRule**](DeliveryReceiptRule.md)| Email delivery receipt rule model | |

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

<a id="emailDeliveryReceiptAutomationPut"></a>
# **emailDeliveryReceiptAutomationPut**
> String emailDeliveryReceiptAutomationPut(receiptRuleId, deliveryReceiptRule)

Update email delivery receipt automation

Update email delivery receipt automation

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.EmailDeliveryReceiptRulesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com/v3");
    
    // Configure HTTP basic authorization: BasicAuth
    HttpBasicAuth BasicAuth = (HttpBasicAuth) defaultClient.getAuthentication("BasicAuth");
    BasicAuth.setUsername("YOUR USERNAME");
    BasicAuth.setPassword("YOUR PASSWORD");

    EmailDeliveryReceiptRulesApi apiInstance = new EmailDeliveryReceiptRulesApi(defaultClient);
    Integer receiptRuleId = 56; // Integer | Receipt rule id
    DeliveryReceiptRule deliveryReceiptRule = new DeliveryReceiptRule(); // DeliveryReceiptRule | Delivery receipt rule model
    try {
      String result = apiInstance.emailDeliveryReceiptAutomationPut(receiptRuleId, deliveryReceiptRule);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling EmailDeliveryReceiptRulesApi#emailDeliveryReceiptAutomationPut");
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
| **receiptRuleId** | **Integer**| Receipt rule id | |
| **deliveryReceiptRule** | [**DeliveryReceiptRule**](DeliveryReceiptRule.md)| Delivery receipt rule model | |

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

<a id="emailDeliveryReceiptAutomationsGet"></a>
# **emailDeliveryReceiptAutomationsGet**
> String emailDeliveryReceiptAutomationsGet(q, page, limit)

Get all email delivery receipt automations

Get all email delivery receipt automations

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.EmailDeliveryReceiptRulesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com/v3");
    
    // Configure HTTP basic authorization: BasicAuth
    HttpBasicAuth BasicAuth = (HttpBasicAuth) defaultClient.getAuthentication("BasicAuth");
    BasicAuth.setUsername("YOUR USERNAME");
    BasicAuth.setPassword("YOUR PASSWORD");

    EmailDeliveryReceiptRulesApi apiInstance = new EmailDeliveryReceiptRulesApi(defaultClient);
    String q = "q_example"; // String | Your keyword or query.
    Integer page = 1; // Integer | Page number
    Integer limit = 10; // Integer | Number of records per page
    try {
      String result = apiInstance.emailDeliveryReceiptAutomationsGet(q, page, limit);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling EmailDeliveryReceiptRulesApi#emailDeliveryReceiptAutomationsGet");
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
| **q** | **String**| Your keyword or query. | [optional] |
| **page** | **Integer**| Page number | [optional] [default to 1] |
| **limit** | **Integer**| Number of records per page | [optional] [default to 10] |

### Return type

**String**

### Authorization

[BasicAuth](../README.md#BasicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
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

