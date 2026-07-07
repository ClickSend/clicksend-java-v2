# MmsCampaignsApi

All URIs are relative to *https://rest.clicksend.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**calculateMmsCampaignPrice**](MmsCampaignsApi.md#calculateMmsCampaignPrice) | **POST** /v3/mms-campaigns/price | Calculate MMS Campaign Price |
| [**cancelMmsCampaign**](MmsCampaignsApi.md#cancelMmsCampaign) | **PUT** /v3/mms-campaigns/{mms_campaign_id}/cancel | Cancel MMS Campaign |
| [**sendMmsCampaign**](MmsCampaignsApi.md#sendMmsCampaign) | **POST** /v3/mms-campaigns/send | Send MMS Campaign |
| [**updateMmsCampaign**](MmsCampaignsApi.md#updateMmsCampaign) | **PUT** /v3/mms-campaigns/{mms_campaign_id} | Update MMS Campaign |
| [**viewAllMmsCampaigns**](MmsCampaignsApi.md#viewAllMmsCampaigns) | **GET** /v3/mms-campaigns | View All MMS Campaigns |
| [**viewMmsCampaign**](MmsCampaignsApi.md#viewMmsCampaign) | **GET** /v3/mms-campaigns/{mms_campaign_id} | View MMS Campaign |


<a id="calculateMmsCampaignPrice"></a>
# **calculateMmsCampaignPrice**
> CalculateMmsCampaignPrice calculateMmsCampaignPrice(contentType, body)

Calculate MMS Campaign Price

_Calculate price for mms campaign_  ### Properties  | Name | Type | Required | Restrictions | Description | | --- | --- | --- | --- | --- | | list_id | integer(int32) | true | none | Your list id. | | name | string | true | none | Your campaign name. | | body | string | true | none | Your campaign message. | | from | string | true | [yes](http://help.clicksend.com/SMS/what-is-a-sender-id-or-sender-number) | Your sender id | | schedule | integer(int32) | false | none | Your schedule timestamp. | | subject | string | true | none | Subject of MMS campaign. | | media_file | string | true | none | URL pointing to media file. |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.MmsCampaignsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    MmsCampaignsApi apiInstance = new MmsCampaignsApi(defaultClient);
    String contentType = "application/json"; // String | 
    Object body = null; // Object | 
    try {
      CalculateMmsCampaignPrice result = apiInstance.calculateMmsCampaignPrice(contentType, body);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling MmsCampaignsApi#calculateMmsCampaignPrice");
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
| **body** | **Object**|  | [optional] |

### Return type

[**CalculateMmsCampaignPrice**](CalculateMmsCampaignPrice.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="cancelMmsCampaign"></a>
# **cancelMmsCampaign**
> CancelMmsCampaign cancelMmsCampaign(mmsCampaignId, contentType, calculateSmsCampaignPriceRequest)

Cancel MMS Campaign

_Cancel mms campaign_  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | mms_campaign_id | path | integer(int32) | true | ID of MMS Campaign to cancel |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.MmsCampaignsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    MmsCampaignsApi apiInstance = new MmsCampaignsApi(defaultClient);
    String mmsCampaignId = "mmsCampaignId_example"; // String | 
    String contentType = "application/json"; // String | 
    CalculateSmsCampaignPriceRequest calculateSmsCampaignPriceRequest = new CalculateSmsCampaignPriceRequest(); // CalculateSmsCampaignPriceRequest | 
    try {
      CancelMmsCampaign result = apiInstance.cancelMmsCampaign(mmsCampaignId, contentType, calculateSmsCampaignPriceRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling MmsCampaignsApi#cancelMmsCampaign");
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
| **mmsCampaignId** | **String**|  | |
| **contentType** | **String**|  | [optional] |
| **calculateSmsCampaignPriceRequest** | [**CalculateSmsCampaignPriceRequest**](CalculateSmsCampaignPriceRequest.md)|  | [optional] |

### Return type

[**CancelMmsCampaign**](CancelMmsCampaign.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="sendMmsCampaign"></a>
# **sendMmsCampaign**
> SendMmsCampaign sendMmsCampaign(contentType, sendMmsCampaignRequest)

Send MMS Campaign

_Create mms campaign_  ### Properties  | Name | Type | Required | Restrictions | Description | | --- | --- | --- | --- | --- | | list_id | integer(int32) | true | none | Your list id. | | name | string | true | none | Your campaign name. | | body | string | true | none | Your campaign message. | | from | string | true | [yes](http://help.clicksend.com/SMS/what-is-a-sender-id-or-sender-number) | Your sender id | | schedule | integer(int32) | false | none | Your schedule timestamp. | | subject | string | true | none | Subject of MMS campaign. | | media_file | string | true | none | URL pointing to media file. |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.MmsCampaignsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    MmsCampaignsApi apiInstance = new MmsCampaignsApi(defaultClient);
    String contentType = "application/json"; // String | 
    SendMmsCampaignRequest sendMmsCampaignRequest = new SendMmsCampaignRequest(); // SendMmsCampaignRequest | 
    try {
      SendMmsCampaign result = apiInstance.sendMmsCampaign(contentType, sendMmsCampaignRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling MmsCampaignsApi#sendMmsCampaign");
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
| **sendMmsCampaignRequest** | [**SendMmsCampaignRequest**](SendMmsCampaignRequest.md)|  | [optional] |

### Return type

[**SendMmsCampaign**](SendMmsCampaign.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="updateMmsCampaign"></a>
# **updateMmsCampaign**
> UpdateMmsCampaign updateMmsCampaign(mmsCampaignId, contentType, calculateSmsCampaignPriceRequest)

Update MMS Campaign

_Update mms campaign_  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | mms_campaign_id | path | integer(int32) | true | ID of MMS campaign to update |  ### Properties  | Name | Type | Required | Restrictions | Description | | --- | --- | --- | --- | --- | | list_id | integer(int32) | true | none | Your list id. | | name | string | true | none | Your campaign name. | | body | string | true | none | Your campaign message. | | from | string | true | [yes](http://help.clicksend.com/SMS/what-is-a-sender-id-or-sender-number) | Your sender id | | schedule | integer(int32) | false | none | Your schedule timestamp. | | subject | string | true | none | Subject of MMS campaign. | | media_file | string | true | none | URL pointing to media file. |  Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.  &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.MmsCampaignsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    MmsCampaignsApi apiInstance = new MmsCampaignsApi(defaultClient);
    String mmsCampaignId = "mmsCampaignId_example"; // String | 
    String contentType = "application/json"; // String | 
    CalculateSmsCampaignPriceRequest calculateSmsCampaignPriceRequest = new CalculateSmsCampaignPriceRequest(); // CalculateSmsCampaignPriceRequest | 
    try {
      UpdateMmsCampaign result = apiInstance.updateMmsCampaign(mmsCampaignId, contentType, calculateSmsCampaignPriceRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling MmsCampaignsApi#updateMmsCampaign");
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
| **mmsCampaignId** | **String**|  | |
| **contentType** | **String**|  | [optional] |
| **calculateSmsCampaignPriceRequest** | [**CalculateSmsCampaignPriceRequest**](CalculateSmsCampaignPriceRequest.md)|  | [optional] |

### Return type

[**UpdateMmsCampaign**](UpdateMmsCampaign.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewAllMmsCampaigns"></a>
# **viewAllMmsCampaigns**
> ViewAllMmsCampaigns viewAllMmsCampaigns(contentType)

View All MMS Campaigns

_Get list of mms campaigns_  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | page | query | integer(int32) | false | [Page number](/#pagination) | | limit | query | integer(int32) | false | [Number of records per page](/#pagination) |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.MmsCampaignsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    MmsCampaignsApi apiInstance = new MmsCampaignsApi(defaultClient);
    String contentType = "application/json"; // String | 
    try {
      ViewAllMmsCampaigns result = apiInstance.viewAllMmsCampaigns(contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling MmsCampaignsApi#viewAllMmsCampaigns");
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

[**ViewAllMmsCampaigns**](ViewAllMmsCampaigns.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewMmsCampaign"></a>
# **viewMmsCampaign**
> ViewMmsCampaign viewMmsCampaign(mmsCampaignId, contentType)

View MMS Campaign

_Get specific mms campaign_  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | mms_campaign_id | path | integer(int32) | true | ID of MMS campaign to retrieve |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.MmsCampaignsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    MmsCampaignsApi apiInstance = new MmsCampaignsApi(defaultClient);
    String mmsCampaignId = "mmsCampaignId_example"; // String | 
    String contentType = "application/json"; // String | 
    try {
      ViewMmsCampaign result = apiInstance.viewMmsCampaign(mmsCampaignId, contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling MmsCampaignsApi#viewMmsCampaign");
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
| **mmsCampaignId** | **String**|  | |
| **contentType** | **String**|  | [optional] |

### Return type

[**ViewMmsCampaign**](ViewMmsCampaign.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

