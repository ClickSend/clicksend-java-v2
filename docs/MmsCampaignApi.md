# MmsCampaignApi

All URIs are relative to *https://rest.clicksend.com/v3*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**mmsCampaignByMmsCampaignIdGet**](MmsCampaignApi.md#mmsCampaignByMmsCampaignIdGet) | **GET** /mms-campaigns/{mms_campaign_id} | Get specific mms campaign |
| [**mmsCampaignsByMmsCampaignIdPut**](MmsCampaignApi.md#mmsCampaignsByMmsCampaignIdPut) | **PUT** /mms-campaigns/{mms_campaign_id} | Update mms campaign |
| [**mmsCampaignsCancelByMmsCampaignIdPut**](MmsCampaignApi.md#mmsCampaignsCancelByMmsCampaignIdPut) | **PUT** /mms-campaigns/{mms_campaign_id}/cancel | Cancel mms campaign |
| [**mmsCampaignsGet**](MmsCampaignApi.md#mmsCampaignsGet) | **GET** /mms-campaigns | Get list of mms campaigns |
| [**mmsCampaignsPricePost**](MmsCampaignApi.md#mmsCampaignsPricePost) | **POST** /mms-campaigns/price | Calculate price for mms campaign |
| [**mmsCampaignsSendPost**](MmsCampaignApi.md#mmsCampaignsSendPost) | **POST** /mms-campaigns/send | Create mms campaign |


<a id="mmsCampaignByMmsCampaignIdGet"></a>
# **mmsCampaignByMmsCampaignIdGet**
> String mmsCampaignByMmsCampaignIdGet(mmsCampaignId)

Get specific mms campaign

Get specific mms campaign

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.MmsCampaignApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com/v3");
    
    // Configure HTTP basic authorization: BasicAuth
    HttpBasicAuth BasicAuth = (HttpBasicAuth) defaultClient.getAuthentication("BasicAuth");
    BasicAuth.setUsername("YOUR USERNAME");
    BasicAuth.setPassword("YOUR PASSWORD");

    MmsCampaignApi apiInstance = new MmsCampaignApi(defaultClient);
    Integer mmsCampaignId = 56; // Integer | ID of MMS campaign to retrieve
    try {
      String result = apiInstance.mmsCampaignByMmsCampaignIdGet(mmsCampaignId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling MmsCampaignApi#mmsCampaignByMmsCampaignIdGet");
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
| **mmsCampaignId** | **Integer**| ID of MMS campaign to retrieve | |

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

<a id="mmsCampaignsByMmsCampaignIdPut"></a>
# **mmsCampaignsByMmsCampaignIdPut**
> String mmsCampaignsByMmsCampaignIdPut(mmsCampaignId, campaign)

Update mms campaign

Update mms campaign

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.MmsCampaignApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com/v3");
    
    // Configure HTTP basic authorization: BasicAuth
    HttpBasicAuth BasicAuth = (HttpBasicAuth) defaultClient.getAuthentication("BasicAuth");
    BasicAuth.setUsername("YOUR USERNAME");
    BasicAuth.setPassword("YOUR PASSWORD");

    MmsCampaignApi apiInstance = new MmsCampaignApi(defaultClient);
    Integer mmsCampaignId = 56; // Integer | ID of MMS campaign to update
    MmsCampaign campaign = new MmsCampaign(); // MmsCampaign | MmsCampaign model
    try {
      String result = apiInstance.mmsCampaignsByMmsCampaignIdPut(mmsCampaignId, campaign);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling MmsCampaignApi#mmsCampaignsByMmsCampaignIdPut");
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
| **mmsCampaignId** | **Integer**| ID of MMS campaign to update | |
| **campaign** | [**MmsCampaign**](MmsCampaign.md)| MmsCampaign model | |

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

<a id="mmsCampaignsCancelByMmsCampaignIdPut"></a>
# **mmsCampaignsCancelByMmsCampaignIdPut**
> String mmsCampaignsCancelByMmsCampaignIdPut(mmsCampaignId)

Cancel mms campaign

Cancel sms campaign

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.MmsCampaignApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com/v3");
    
    // Configure HTTP basic authorization: BasicAuth
    HttpBasicAuth BasicAuth = (HttpBasicAuth) defaultClient.getAuthentication("BasicAuth");
    BasicAuth.setUsername("YOUR USERNAME");
    BasicAuth.setPassword("YOUR PASSWORD");

    MmsCampaignApi apiInstance = new MmsCampaignApi(defaultClient);
    Integer mmsCampaignId = 56; // Integer | ID of MMS Campaign to cancel
    try {
      String result = apiInstance.mmsCampaignsCancelByMmsCampaignIdPut(mmsCampaignId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling MmsCampaignApi#mmsCampaignsCancelByMmsCampaignIdPut");
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
| **mmsCampaignId** | **Integer**| ID of MMS Campaign to cancel | |

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

<a id="mmsCampaignsGet"></a>
# **mmsCampaignsGet**
> String mmsCampaignsGet(page, limit)

Get list of mms campaigns

Get list of mms campaigns

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.MmsCampaignApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com/v3");
    
    // Configure HTTP basic authorization: BasicAuth
    HttpBasicAuth BasicAuth = (HttpBasicAuth) defaultClient.getAuthentication("BasicAuth");
    BasicAuth.setUsername("YOUR USERNAME");
    BasicAuth.setPassword("YOUR PASSWORD");

    MmsCampaignApi apiInstance = new MmsCampaignApi(defaultClient);
    Integer page = 1; // Integer | Page number
    Integer limit = 10; // Integer | Number of records per page
    try {
      String result = apiInstance.mmsCampaignsGet(page, limit);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling MmsCampaignApi#mmsCampaignsGet");
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

<a id="mmsCampaignsPricePost"></a>
# **mmsCampaignsPricePost**
> String mmsCampaignsPricePost(campaign)

Calculate price for mms campaign

Calculate price for sms campaign

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.MmsCampaignApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com/v3");
    
    // Configure HTTP basic authorization: BasicAuth
    HttpBasicAuth BasicAuth = (HttpBasicAuth) defaultClient.getAuthentication("BasicAuth");
    BasicAuth.setUsername("YOUR USERNAME");
    BasicAuth.setPassword("YOUR PASSWORD");

    MmsCampaignApi apiInstance = new MmsCampaignApi(defaultClient);
    MmsCampaign campaign = new MmsCampaign(); // MmsCampaign | MmsCampaign model
    try {
      String result = apiInstance.mmsCampaignsPricePost(campaign);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling MmsCampaignApi#mmsCampaignsPricePost");
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
| **campaign** | [**MmsCampaign**](MmsCampaign.md)| MmsCampaign model | |

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

<a id="mmsCampaignsSendPost"></a>
# **mmsCampaignsSendPost**
> String mmsCampaignsSendPost(campaign)

Create mms campaign

Create mms campaign

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.MmsCampaignApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com/v3");
    
    // Configure HTTP basic authorization: BasicAuth
    HttpBasicAuth BasicAuth = (HttpBasicAuth) defaultClient.getAuthentication("BasicAuth");
    BasicAuth.setUsername("YOUR USERNAME");
    BasicAuth.setPassword("YOUR PASSWORD");

    MmsCampaignApi apiInstance = new MmsCampaignApi(defaultClient);
    MmsCampaign campaign = new MmsCampaign(); // MmsCampaign | MmsCampaign model
    try {
      String result = apiInstance.mmsCampaignsSendPost(campaign);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling MmsCampaignApi#mmsCampaignsSendPost");
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
| **campaign** | [**MmsCampaign**](MmsCampaign.md)| MmsCampaign model | |

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

