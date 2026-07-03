# SmsDeliveryReceiptRulesApi

All URIs are relative to *https://rest.clicksend.com/v3*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**smsDeliveryReceiptAutomationDelete**](SmsDeliveryReceiptRulesApi.md#smsDeliveryReceiptAutomationDelete) | **DELETE** /automations/sms/receipts/{receipt_rule_id} | Delete sms delivery receipt automation |
| [**smsDeliveryReceiptAutomationGet**](SmsDeliveryReceiptRulesApi.md#smsDeliveryReceiptAutomationGet) | **GET** /automations/sms/receipts/{receipt_rule_id} | Get specific sms delivery receipt automation |
| [**smsDeliveryReceiptAutomationPost**](SmsDeliveryReceiptRulesApi.md#smsDeliveryReceiptAutomationPost) | **POST** /automations/sms/receipts | Create sms delivery receipt automations |
| [**smsDeliveryReceiptAutomationPut**](SmsDeliveryReceiptRulesApi.md#smsDeliveryReceiptAutomationPut) | **PUT** /automations/sms/receipts/{receipt_rule_id} | Update sms delivery receipt automation |
| [**smsDeliveryReceiptAutomationsGet**](SmsDeliveryReceiptRulesApi.md#smsDeliveryReceiptAutomationsGet) | **GET** /automations/sms/receipts | Get all sms delivery receipt automations |


<a id="smsDeliveryReceiptAutomationDelete"></a>
# **smsDeliveryReceiptAutomationDelete**
> String smsDeliveryReceiptAutomationDelete(receiptRuleId)

Delete sms delivery receipt automation

Delete sms delivery receipt automation

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.SmsDeliveryReceiptRulesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com/v3");
    
    // Configure HTTP basic authorization: BasicAuth
    HttpBasicAuth BasicAuth = (HttpBasicAuth) defaultClient.getAuthentication("BasicAuth");
    BasicAuth.setUsername("YOUR USERNAME");
    BasicAuth.setPassword("YOUR PASSWORD");

    SmsDeliveryReceiptRulesApi apiInstance = new SmsDeliveryReceiptRulesApi(defaultClient);
    Integer receiptRuleId = 56; // Integer | Receipt rule id
    try {
      String result = apiInstance.smsDeliveryReceiptAutomationDelete(receiptRuleId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SmsDeliveryReceiptRulesApi#smsDeliveryReceiptAutomationDelete");
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

<a id="smsDeliveryReceiptAutomationGet"></a>
# **smsDeliveryReceiptAutomationGet**
> String smsDeliveryReceiptAutomationGet(receiptRuleId)

Get specific sms delivery receipt automation

Get specific sms delivery receipt automation

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.SmsDeliveryReceiptRulesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com/v3");
    
    // Configure HTTP basic authorization: BasicAuth
    HttpBasicAuth BasicAuth = (HttpBasicAuth) defaultClient.getAuthentication("BasicAuth");
    BasicAuth.setUsername("YOUR USERNAME");
    BasicAuth.setPassword("YOUR PASSWORD");

    SmsDeliveryReceiptRulesApi apiInstance = new SmsDeliveryReceiptRulesApi(defaultClient);
    Integer receiptRuleId = 56; // Integer | Receipt rule id
    try {
      String result = apiInstance.smsDeliveryReceiptAutomationGet(receiptRuleId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SmsDeliveryReceiptRulesApi#smsDeliveryReceiptAutomationGet");
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

<a id="smsDeliveryReceiptAutomationPost"></a>
# **smsDeliveryReceiptAutomationPost**
> String smsDeliveryReceiptAutomationPost(deliveryReceiptRule)

Create sms delivery receipt automations

Create sms delivery receipt automations

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.SmsDeliveryReceiptRulesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com/v3");
    
    // Configure HTTP basic authorization: BasicAuth
    HttpBasicAuth BasicAuth = (HttpBasicAuth) defaultClient.getAuthentication("BasicAuth");
    BasicAuth.setUsername("YOUR USERNAME");
    BasicAuth.setPassword("YOUR PASSWORD");

    SmsDeliveryReceiptRulesApi apiInstance = new SmsDeliveryReceiptRulesApi(defaultClient);
    DeliveryReceiptRule deliveryReceiptRule = new DeliveryReceiptRule(); // DeliveryReceiptRule | sms delivery receipt rule model
    try {
      String result = apiInstance.smsDeliveryReceiptAutomationPost(deliveryReceiptRule);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SmsDeliveryReceiptRulesApi#smsDeliveryReceiptAutomationPost");
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
| **deliveryReceiptRule** | [**DeliveryReceiptRule**](DeliveryReceiptRule.md)| sms delivery receipt rule model | |

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

<a id="smsDeliveryReceiptAutomationPut"></a>
# **smsDeliveryReceiptAutomationPut**
> String smsDeliveryReceiptAutomationPut(receiptRuleId, deliveryReceiptRule)

Update sms delivery receipt automation

Update sms delivery receipt automation

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.SmsDeliveryReceiptRulesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com/v3");
    
    // Configure HTTP basic authorization: BasicAuth
    HttpBasicAuth BasicAuth = (HttpBasicAuth) defaultClient.getAuthentication("BasicAuth");
    BasicAuth.setUsername("YOUR USERNAME");
    BasicAuth.setPassword("YOUR PASSWORD");

    SmsDeliveryReceiptRulesApi apiInstance = new SmsDeliveryReceiptRulesApi(defaultClient);
    Integer receiptRuleId = 56; // Integer | Receipt rule id
    DeliveryReceiptRule deliveryReceiptRule = new DeliveryReceiptRule(); // DeliveryReceiptRule | Delivery receipt rule model
    try {
      String result = apiInstance.smsDeliveryReceiptAutomationPut(receiptRuleId, deliveryReceiptRule);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SmsDeliveryReceiptRulesApi#smsDeliveryReceiptAutomationPut");
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

<a id="smsDeliveryReceiptAutomationsGet"></a>
# **smsDeliveryReceiptAutomationsGet**
> String smsDeliveryReceiptAutomationsGet(q, page, limit)

Get all sms delivery receipt automations

Get all sms delivery receipt automations

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.SmsDeliveryReceiptRulesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com/v3");
    
    // Configure HTTP basic authorization: BasicAuth
    HttpBasicAuth BasicAuth = (HttpBasicAuth) defaultClient.getAuthentication("BasicAuth");
    BasicAuth.setUsername("YOUR USERNAME");
    BasicAuth.setPassword("YOUR PASSWORD");

    SmsDeliveryReceiptRulesApi apiInstance = new SmsDeliveryReceiptRulesApi(defaultClient);
    String q = "q_example"; // String | Your keyword or query.
    Integer page = 1; // Integer | Page number
    Integer limit = 10; // Integer | Number of records per page
    try {
      String result = apiInstance.smsDeliveryReceiptAutomationsGet(q, page, limit);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SmsDeliveryReceiptRulesApi#smsDeliveryReceiptAutomationsGet");
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

