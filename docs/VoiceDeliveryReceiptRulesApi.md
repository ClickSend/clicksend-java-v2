# VoiceDeliveryReceiptRulesApi

All URIs are relative to *https://rest.clicksend.com/v3*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**voiceDeliveryReceiptAutomationDelete**](VoiceDeliveryReceiptRulesApi.md#voiceDeliveryReceiptAutomationDelete) | **DELETE** /automations/voice/receipts/{receipt_rule_id} | Delete voice delivery receipt automation |
| [**voiceDeliveryReceiptAutomationGet**](VoiceDeliveryReceiptRulesApi.md#voiceDeliveryReceiptAutomationGet) | **GET** /automations/voice/receipts/{receipt_rule_id} | Get specific voice delivery receipt automation |
| [**voiceDeliveryReceiptAutomationPost**](VoiceDeliveryReceiptRulesApi.md#voiceDeliveryReceiptAutomationPost) | **POST** /automations/voice/receipts | Create voice delivery receipt automations |
| [**voiceDeliveryReceiptAutomationPut**](VoiceDeliveryReceiptRulesApi.md#voiceDeliveryReceiptAutomationPut) | **PUT** /automations/voice/receipts/{receipt_rule_id} | Update voice delivery receipt automation |
| [**voiceDeliveryReceiptAutomationsGet**](VoiceDeliveryReceiptRulesApi.md#voiceDeliveryReceiptAutomationsGet) | **GET** /automations/voice/receipts | Get all voice delivery receipt automations |


<a id="voiceDeliveryReceiptAutomationDelete"></a>
# **voiceDeliveryReceiptAutomationDelete**
> String voiceDeliveryReceiptAutomationDelete(receiptRuleId)

Delete voice delivery receipt automation

Delete voice delivery receipt automation

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.VoiceDeliveryReceiptRulesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com/v3");
    
    // Configure HTTP basic authorization: BasicAuth
    HttpBasicAuth BasicAuth = (HttpBasicAuth) defaultClient.getAuthentication("BasicAuth");
    BasicAuth.setUsername("YOUR USERNAME");
    BasicAuth.setPassword("YOUR PASSWORD");

    VoiceDeliveryReceiptRulesApi apiInstance = new VoiceDeliveryReceiptRulesApi(defaultClient);
    Integer receiptRuleId = 56; // Integer | Receipt rule id
    try {
      String result = apiInstance.voiceDeliveryReceiptAutomationDelete(receiptRuleId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling VoiceDeliveryReceiptRulesApi#voiceDeliveryReceiptAutomationDelete");
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

<a id="voiceDeliveryReceiptAutomationGet"></a>
# **voiceDeliveryReceiptAutomationGet**
> String voiceDeliveryReceiptAutomationGet(receiptRuleId)

Get specific voice delivery receipt automation

Get specific voice delivery receipt automation

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.VoiceDeliveryReceiptRulesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com/v3");
    
    // Configure HTTP basic authorization: BasicAuth
    HttpBasicAuth BasicAuth = (HttpBasicAuth) defaultClient.getAuthentication("BasicAuth");
    BasicAuth.setUsername("YOUR USERNAME");
    BasicAuth.setPassword("YOUR PASSWORD");

    VoiceDeliveryReceiptRulesApi apiInstance = new VoiceDeliveryReceiptRulesApi(defaultClient);
    Integer receiptRuleId = 56; // Integer | Receipt rule id
    try {
      String result = apiInstance.voiceDeliveryReceiptAutomationGet(receiptRuleId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling VoiceDeliveryReceiptRulesApi#voiceDeliveryReceiptAutomationGet");
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

<a id="voiceDeliveryReceiptAutomationPost"></a>
# **voiceDeliveryReceiptAutomationPost**
> String voiceDeliveryReceiptAutomationPost(deliveryReceiptRule)

Create voice delivery receipt automations

Create voice delivery receipt automations

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.VoiceDeliveryReceiptRulesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com/v3");
    
    // Configure HTTP basic authorization: BasicAuth
    HttpBasicAuth BasicAuth = (HttpBasicAuth) defaultClient.getAuthentication("BasicAuth");
    BasicAuth.setUsername("YOUR USERNAME");
    BasicAuth.setPassword("YOUR PASSWORD");

    VoiceDeliveryReceiptRulesApi apiInstance = new VoiceDeliveryReceiptRulesApi(defaultClient);
    DeliveryReceiptRule deliveryReceiptRule = new DeliveryReceiptRule(); // DeliveryReceiptRule | voice delivery receipt rule model
    try {
      String result = apiInstance.voiceDeliveryReceiptAutomationPost(deliveryReceiptRule);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling VoiceDeliveryReceiptRulesApi#voiceDeliveryReceiptAutomationPost");
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
| **deliveryReceiptRule** | [**DeliveryReceiptRule**](DeliveryReceiptRule.md)| voice delivery receipt rule model | |

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

<a id="voiceDeliveryReceiptAutomationPut"></a>
# **voiceDeliveryReceiptAutomationPut**
> String voiceDeliveryReceiptAutomationPut(receiptRuleId, deliveryReceiptRule)

Update voice delivery receipt automation

Update voice delivery receipt automation

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.VoiceDeliveryReceiptRulesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com/v3");
    
    // Configure HTTP basic authorization: BasicAuth
    HttpBasicAuth BasicAuth = (HttpBasicAuth) defaultClient.getAuthentication("BasicAuth");
    BasicAuth.setUsername("YOUR USERNAME");
    BasicAuth.setPassword("YOUR PASSWORD");

    VoiceDeliveryReceiptRulesApi apiInstance = new VoiceDeliveryReceiptRulesApi(defaultClient);
    Integer receiptRuleId = 56; // Integer | Receipt rule id
    DeliveryReceiptRule deliveryReceiptRule = new DeliveryReceiptRule(); // DeliveryReceiptRule | Delivery receipt rule model
    try {
      String result = apiInstance.voiceDeliveryReceiptAutomationPut(receiptRuleId, deliveryReceiptRule);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling VoiceDeliveryReceiptRulesApi#voiceDeliveryReceiptAutomationPut");
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

<a id="voiceDeliveryReceiptAutomationsGet"></a>
# **voiceDeliveryReceiptAutomationsGet**
> String voiceDeliveryReceiptAutomationsGet(q, page, limit)

Get all voice delivery receipt automations

Get all voice delivery receipt automations

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.VoiceDeliveryReceiptRulesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com/v3");
    
    // Configure HTTP basic authorization: BasicAuth
    HttpBasicAuth BasicAuth = (HttpBasicAuth) defaultClient.getAuthentication("BasicAuth");
    BasicAuth.setUsername("YOUR USERNAME");
    BasicAuth.setPassword("YOUR PASSWORD");

    VoiceDeliveryReceiptRulesApi apiInstance = new VoiceDeliveryReceiptRulesApi(defaultClient);
    String q = "q_example"; // String | Your keyword or query.
    Integer page = 1; // Integer | Page number
    Integer limit = 10; // Integer | Number of records per page
    try {
      String result = apiInstance.voiceDeliveryReceiptAutomationsGet(q, page, limit);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling VoiceDeliveryReceiptRulesApi#voiceDeliveryReceiptAutomationsGet");
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

