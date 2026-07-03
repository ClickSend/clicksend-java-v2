# FaxDeliveryReceiptRulesApi

All URIs are relative to *https://rest.clicksend.com/v3*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**faxDeliveryReceiptAutomationDelete**](FaxDeliveryReceiptRulesApi.md#faxDeliveryReceiptAutomationDelete) | **DELETE** /automations/fax/receipts/{receipt_rule_id} | Delete fax delivery receipt automation |
| [**faxDeliveryReceiptAutomationGet**](FaxDeliveryReceiptRulesApi.md#faxDeliveryReceiptAutomationGet) | **GET** /automations/fax/receipts/{receipt_rule_id} | Get specific fax delivery receipt automation |
| [**faxDeliveryReceiptAutomationPost**](FaxDeliveryReceiptRulesApi.md#faxDeliveryReceiptAutomationPost) | **POST** /automations/fax/receipts | Create fax delivery receipt automations |
| [**faxDeliveryReceiptAutomationPut**](FaxDeliveryReceiptRulesApi.md#faxDeliveryReceiptAutomationPut) | **PUT** /automations/fax/receipts/{receipt_rule_id} | Update fax delivery receipt automation |
| [**faxDeliveryReceiptAutomationsGet**](FaxDeliveryReceiptRulesApi.md#faxDeliveryReceiptAutomationsGet) | **GET** /automations/fax/receipts | Get all fax delivery receipt automations |


<a id="faxDeliveryReceiptAutomationDelete"></a>
# **faxDeliveryReceiptAutomationDelete**
> String faxDeliveryReceiptAutomationDelete(receiptRuleId)

Delete fax delivery receipt automation

Delete fax delivery receipt automation

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.FaxDeliveryReceiptRulesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com/v3");
    
    // Configure HTTP basic authorization: BasicAuth
    HttpBasicAuth BasicAuth = (HttpBasicAuth) defaultClient.getAuthentication("BasicAuth");
    BasicAuth.setUsername("YOUR USERNAME");
    BasicAuth.setPassword("YOUR PASSWORD");

    FaxDeliveryReceiptRulesApi apiInstance = new FaxDeliveryReceiptRulesApi(defaultClient);
    Integer receiptRuleId = 56; // Integer | Receipt rule id
    try {
      String result = apiInstance.faxDeliveryReceiptAutomationDelete(receiptRuleId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling FaxDeliveryReceiptRulesApi#faxDeliveryReceiptAutomationDelete");
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

<a id="faxDeliveryReceiptAutomationGet"></a>
# **faxDeliveryReceiptAutomationGet**
> String faxDeliveryReceiptAutomationGet(receiptRuleId)

Get specific fax delivery receipt automation

Get specific fax delivery receipt automation

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.FaxDeliveryReceiptRulesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com/v3");
    
    // Configure HTTP basic authorization: BasicAuth
    HttpBasicAuth BasicAuth = (HttpBasicAuth) defaultClient.getAuthentication("BasicAuth");
    BasicAuth.setUsername("YOUR USERNAME");
    BasicAuth.setPassword("YOUR PASSWORD");

    FaxDeliveryReceiptRulesApi apiInstance = new FaxDeliveryReceiptRulesApi(defaultClient);
    Integer receiptRuleId = 56; // Integer | Receipt rule id
    try {
      String result = apiInstance.faxDeliveryReceiptAutomationGet(receiptRuleId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling FaxDeliveryReceiptRulesApi#faxDeliveryReceiptAutomationGet");
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

<a id="faxDeliveryReceiptAutomationPost"></a>
# **faxDeliveryReceiptAutomationPost**
> String faxDeliveryReceiptAutomationPost(deliveryReceiptRule)

Create fax delivery receipt automations

Create fax delivery receipt automations

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.FaxDeliveryReceiptRulesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com/v3");
    
    // Configure HTTP basic authorization: BasicAuth
    HttpBasicAuth BasicAuth = (HttpBasicAuth) defaultClient.getAuthentication("BasicAuth");
    BasicAuth.setUsername("YOUR USERNAME");
    BasicAuth.setPassword("YOUR PASSWORD");

    FaxDeliveryReceiptRulesApi apiInstance = new FaxDeliveryReceiptRulesApi(defaultClient);
    DeliveryReceiptRule deliveryReceiptRule = new DeliveryReceiptRule(); // DeliveryReceiptRule | fax delivery receipt rule model
    try {
      String result = apiInstance.faxDeliveryReceiptAutomationPost(deliveryReceiptRule);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling FaxDeliveryReceiptRulesApi#faxDeliveryReceiptAutomationPost");
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
| **deliveryReceiptRule** | [**DeliveryReceiptRule**](DeliveryReceiptRule.md)| fax delivery receipt rule model | |

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

<a id="faxDeliveryReceiptAutomationPut"></a>
# **faxDeliveryReceiptAutomationPut**
> String faxDeliveryReceiptAutomationPut(receiptRuleId, deliveryReceiptRule)

Update fax delivery receipt automation

Update fax delivery receipt automation

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.FaxDeliveryReceiptRulesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com/v3");
    
    // Configure HTTP basic authorization: BasicAuth
    HttpBasicAuth BasicAuth = (HttpBasicAuth) defaultClient.getAuthentication("BasicAuth");
    BasicAuth.setUsername("YOUR USERNAME");
    BasicAuth.setPassword("YOUR PASSWORD");

    FaxDeliveryReceiptRulesApi apiInstance = new FaxDeliveryReceiptRulesApi(defaultClient);
    Integer receiptRuleId = 56; // Integer | Receipt rule id
    DeliveryReceiptRule deliveryReceiptRule = new DeliveryReceiptRule(); // DeliveryReceiptRule | Delivery receipt rule model
    try {
      String result = apiInstance.faxDeliveryReceiptAutomationPut(receiptRuleId, deliveryReceiptRule);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling FaxDeliveryReceiptRulesApi#faxDeliveryReceiptAutomationPut");
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

<a id="faxDeliveryReceiptAutomationsGet"></a>
# **faxDeliveryReceiptAutomationsGet**
> String faxDeliveryReceiptAutomationsGet(q, page, limit)

Get all fax delivery receipt automations

Get all fax delivery receipt automations

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.FaxDeliveryReceiptRulesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com/v3");
    
    // Configure HTTP basic authorization: BasicAuth
    HttpBasicAuth BasicAuth = (HttpBasicAuth) defaultClient.getAuthentication("BasicAuth");
    BasicAuth.setUsername("YOUR USERNAME");
    BasicAuth.setPassword("YOUR PASSWORD");

    FaxDeliveryReceiptRulesApi apiInstance = new FaxDeliveryReceiptRulesApi(defaultClient);
    String q = "q_example"; // String | Your keyword or query.
    Integer page = 1; // Integer | Page number
    Integer limit = 10; // Integer | Number of records per page
    try {
      String result = apiInstance.faxDeliveryReceiptAutomationsGet(q, page, limit);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling FaxDeliveryReceiptRulesApi#faxDeliveryReceiptAutomationsGet");
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

