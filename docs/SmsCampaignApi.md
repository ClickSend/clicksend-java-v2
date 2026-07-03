# SmsCampaignApi

All URIs are relative to *https://rest.clicksend.com/v3*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**smsCampaignBySmsCampaignIdGet**](SmsCampaignApi.md#smsCampaignBySmsCampaignIdGet) | **GET** /sms-campaigns/{sms_campaign_id} | Get specific sms campaign |
| [**smsCampaignsBySmsCampaignIdPut**](SmsCampaignApi.md#smsCampaignsBySmsCampaignIdPut) | **PUT** /sms-campaigns/{sms_campaign_id} | Update sms campaign |
| [**smsCampaignsCancelBySmsCampaignIdPut**](SmsCampaignApi.md#smsCampaignsCancelBySmsCampaignIdPut) | **PUT** /sms-campaigns/{sms_campaign_id}/cancel | Cancel sms campaign |
| [**smsCampaignsGet**](SmsCampaignApi.md#smsCampaignsGet) | **GET** /sms-campaigns | Get list of sms campaigns |
| [**smsCampaignsPricePost**](SmsCampaignApi.md#smsCampaignsPricePost) | **POST** /sms-campaigns/price | Calculate price for sms campaign |
| [**smsCampaignsSendPost**](SmsCampaignApi.md#smsCampaignsSendPost) | **POST** /sms-campaigns/send | Create sms campaign |


<a id="smsCampaignBySmsCampaignIdGet"></a>
# **smsCampaignBySmsCampaignIdGet**
> String smsCampaignBySmsCampaignIdGet(smsCampaignId)

Get specific sms campaign

Get specific sms campaign

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.SmsCampaignApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com/v3");
    
    // Configure HTTP basic authorization: BasicAuth
    HttpBasicAuth BasicAuth = (HttpBasicAuth) defaultClient.getAuthentication("BasicAuth");
    BasicAuth.setUsername("YOUR USERNAME");
    BasicAuth.setPassword("YOUR PASSWORD");

    SmsCampaignApi apiInstance = new SmsCampaignApi(defaultClient);
    Integer smsCampaignId = 56; // Integer | ID of SMS campaign to retrieve
    try {
      String result = apiInstance.smsCampaignBySmsCampaignIdGet(smsCampaignId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SmsCampaignApi#smsCampaignBySmsCampaignIdGet");
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
| **smsCampaignId** | **Integer**| ID of SMS campaign to retrieve | |

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

<a id="smsCampaignsBySmsCampaignIdPut"></a>
# **smsCampaignsBySmsCampaignIdPut**
> String smsCampaignsBySmsCampaignIdPut(smsCampaignId, campaign)

Update sms campaign

Update sms campaign

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.SmsCampaignApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com/v3");
    
    // Configure HTTP basic authorization: BasicAuth
    HttpBasicAuth BasicAuth = (HttpBasicAuth) defaultClient.getAuthentication("BasicAuth");
    BasicAuth.setUsername("YOUR USERNAME");
    BasicAuth.setPassword("YOUR PASSWORD");

    SmsCampaignApi apiInstance = new SmsCampaignApi(defaultClient);
    Integer smsCampaignId = 56; // Integer | ID of SMS campaign to update
    SmsCampaign campaign = new SmsCampaign(); // SmsCampaign | SmsCampaign model
    try {
      String result = apiInstance.smsCampaignsBySmsCampaignIdPut(smsCampaignId, campaign);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SmsCampaignApi#smsCampaignsBySmsCampaignIdPut");
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
| **smsCampaignId** | **Integer**| ID of SMS campaign to update | |
| **campaign** | [**SmsCampaign**](SmsCampaign.md)| SmsCampaign model | |

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

<a id="smsCampaignsCancelBySmsCampaignIdPut"></a>
# **smsCampaignsCancelBySmsCampaignIdPut**
> String smsCampaignsCancelBySmsCampaignIdPut(smsCampaignId)

Cancel sms campaign

Cancel sms campaign

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.SmsCampaignApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com/v3");
    
    // Configure HTTP basic authorization: BasicAuth
    HttpBasicAuth BasicAuth = (HttpBasicAuth) defaultClient.getAuthentication("BasicAuth");
    BasicAuth.setUsername("YOUR USERNAME");
    BasicAuth.setPassword("YOUR PASSWORD");

    SmsCampaignApi apiInstance = new SmsCampaignApi(defaultClient);
    Integer smsCampaignId = 56; // Integer | ID of SMS Campaign to cancel
    try {
      String result = apiInstance.smsCampaignsCancelBySmsCampaignIdPut(smsCampaignId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SmsCampaignApi#smsCampaignsCancelBySmsCampaignIdPut");
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
| **smsCampaignId** | **Integer**| ID of SMS Campaign to cancel | |

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

<a id="smsCampaignsGet"></a>
# **smsCampaignsGet**
> String smsCampaignsGet(page, limit)

Get list of sms campaigns

Get list of sms campaigns

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.SmsCampaignApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com/v3");
    
    // Configure HTTP basic authorization: BasicAuth
    HttpBasicAuth BasicAuth = (HttpBasicAuth) defaultClient.getAuthentication("BasicAuth");
    BasicAuth.setUsername("YOUR USERNAME");
    BasicAuth.setPassword("YOUR PASSWORD");

    SmsCampaignApi apiInstance = new SmsCampaignApi(defaultClient);
    Integer page = 1; // Integer | Page number
    Integer limit = 10; // Integer | Number of records per page
    try {
      String result = apiInstance.smsCampaignsGet(page, limit);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SmsCampaignApi#smsCampaignsGet");
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

<a id="smsCampaignsPricePost"></a>
# **smsCampaignsPricePost**
> String smsCampaignsPricePost(campaign)

Calculate price for sms campaign

Calculate price for sms campaign

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.SmsCampaignApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com/v3");
    
    // Configure HTTP basic authorization: BasicAuth
    HttpBasicAuth BasicAuth = (HttpBasicAuth) defaultClient.getAuthentication("BasicAuth");
    BasicAuth.setUsername("YOUR USERNAME");
    BasicAuth.setPassword("YOUR PASSWORD");

    SmsCampaignApi apiInstance = new SmsCampaignApi(defaultClient);
    SmsCampaign campaign = new SmsCampaign(); // SmsCampaign | SmsCampaign model
    try {
      String result = apiInstance.smsCampaignsPricePost(campaign);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SmsCampaignApi#smsCampaignsPricePost");
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
| **campaign** | [**SmsCampaign**](SmsCampaign.md)| SmsCampaign model | |

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

<a id="smsCampaignsSendPost"></a>
# **smsCampaignsSendPost**
> String smsCampaignsSendPost(campaign)

Create sms campaign

Create sms campaign

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.SmsCampaignApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com/v3");
    
    // Configure HTTP basic authorization: BasicAuth
    HttpBasicAuth BasicAuth = (HttpBasicAuth) defaultClient.getAuthentication("BasicAuth");
    BasicAuth.setUsername("YOUR USERNAME");
    BasicAuth.setPassword("YOUR PASSWORD");

    SmsCampaignApi apiInstance = new SmsCampaignApi(defaultClient);
    SmsCampaign campaign = new SmsCampaign(); // SmsCampaign | SmsCampaign model
    try {
      String result = apiInstance.smsCampaignsSendPost(campaign);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SmsCampaignApi#smsCampaignsSendPost");
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
| **campaign** | [**SmsCampaign**](SmsCampaign.md)| SmsCampaign model | |

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

