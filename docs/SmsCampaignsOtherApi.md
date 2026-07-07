# SmsCampaignsOtherApi

All URIs are relative to *https://rest.clicksend.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**calculateSmsCampaignPrice**](SmsCampaignsOtherApi.md#calculateSmsCampaignPrice) | **POST** /v3/sms-campaigns/price | Calculate SMS Campaign Price |
| [**cancelSmsCampaign**](SmsCampaignsOtherApi.md#cancelSmsCampaign) | **PUT** /v3/sms-campaigns/{sms_campaign_id}/cancel | Cancel SMS Campaign |
| [**sendSmsCampaign**](SmsCampaignsOtherApi.md#sendSmsCampaign) | **POST** /v3/sms-campaigns/send | Send SMS Campaign |
| [**updateSmsCampaign**](SmsCampaignsOtherApi.md#updateSmsCampaign) | **PUT** /v3/sms-campaigns/{sms_campaign_id} | Update SMS Campaign |
| [**viewSmsCampaigns**](SmsCampaignsOtherApi.md#viewSmsCampaigns) | **GET** /v3/sms-campaigns | View SMS Campaigns |
| [**viewSpecificSmsCampaign**](SmsCampaignsOtherApi.md#viewSpecificSmsCampaign) | **GET** /v3/sms-campaigns/{sms_campaign_id} | View Specific SMS Campaign |


<a id="calculateSmsCampaignPrice"></a>
# **calculateSmsCampaignPrice**
> CalculateSmsCampaignPrice calculateSmsCampaignPrice(contentType, calculateSmsCampaignPriceRequest)

Calculate SMS Campaign Price

_Calculate price for sms campaign_  ### Properties  | Name | Type | Required | Restrictions | Description | | --- | --- | --- | --- | --- | | list_id | integer(int32) | true | none | Your list id. | | name | string | true | none | Your campaign name. | | body | string | true | none | Your campaign message. | | from | string | true | [yes](http://help.clicksend.com/SMS/what-is-a-sender-id-or-sender-number) | Your sender id | | schedule | integer(int32) | false | none | Your schedule timestamp. |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.SmsCampaignsOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    SmsCampaignsOtherApi apiInstance = new SmsCampaignsOtherApi(defaultClient);
    String contentType = "application/json"; // String | 
    CalculateSmsCampaignPriceRequest calculateSmsCampaignPriceRequest = new CalculateSmsCampaignPriceRequest(); // CalculateSmsCampaignPriceRequest | 
    try {
      CalculateSmsCampaignPrice result = apiInstance.calculateSmsCampaignPrice(contentType, calculateSmsCampaignPriceRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SmsCampaignsOtherApi#calculateSmsCampaignPrice");
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
| **calculateSmsCampaignPriceRequest** | [**CalculateSmsCampaignPriceRequest**](CalculateSmsCampaignPriceRequest.md)|  | [optional] |

### Return type

[**CalculateSmsCampaignPrice**](CalculateSmsCampaignPrice.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="cancelSmsCampaign"></a>
# **cancelSmsCampaign**
> CancelSmsCampaign cancelSmsCampaign(smsCampaignId, contentType)

Cancel SMS Campaign

Use this endpoint to cancel a scheduled SMS campaign.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.SmsCampaignsOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    SmsCampaignsOtherApi apiInstance = new SmsCampaignsOtherApi(defaultClient);
    String smsCampaignId = "smsCampaignId_example"; // String | ID of the scheduled SMS campaign to cancel.
    String contentType = "application/json"; // String | 
    try {
      CancelSmsCampaign result = apiInstance.cancelSmsCampaign(smsCampaignId, contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SmsCampaignsOtherApi#cancelSmsCampaign");
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
| **smsCampaignId** | **String**| ID of the scheduled SMS campaign to cancel. | |
| **contentType** | **String**|  | [optional] |

### Return type

[**CancelSmsCampaign**](CancelSmsCampaign.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="sendSmsCampaign"></a>
# **sendSmsCampaign**
> SendSmsCampaign sendSmsCampaign(contentType, sendSmsCampaignRequest)

Send SMS Campaign

### _SMS Campaign Endpoint_  You can post to a list with &#x60;up to 20000 recipients&#x60; with each API call. You can only send to a single list containing up to 20,000 recipients. The response is far less detailed than the normal Send SMS endpoint. Use the [SMS Send](/#send-sms) endpoint if you would like to send to less than 1000 recipients at once. You are required to add an opt-out message to the end of your message body if you are sending marketing message. This can be in the form of asking users to reply STOP to opt-out or by including &#x60;StopMsg.me/xxxxx&#x60; which is a placeholder that will add a link that can be clicked to out-out. Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses. &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.SmsCampaignsOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    SmsCampaignsOtherApi apiInstance = new SmsCampaignsOtherApi(defaultClient);
    String contentType = "application/json"; // String | 
    SendSmsCampaignRequest sendSmsCampaignRequest = new SendSmsCampaignRequest(); // SendSmsCampaignRequest | 
    try {
      SendSmsCampaign result = apiInstance.sendSmsCampaign(contentType, sendSmsCampaignRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SmsCampaignsOtherApi#sendSmsCampaign");
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
| **sendSmsCampaignRequest** | [**SendSmsCampaignRequest**](SendSmsCampaignRequest.md)|  | [optional] |

### Return type

[**SendSmsCampaign**](SendSmsCampaign.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="updateSmsCampaign"></a>
# **updateSmsCampaign**
> UpdateSmsCampaign updateSmsCampaign(smsCampaignId, contentType, calculateSmsCampaignPriceRequest)

Update SMS Campaign

_Update sms campaign_  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | sms_campaign_id | path | integer(int32) | true | ID of SMS campaign to update |  ### Properties  | Name | Type | Required | Restrictions | Description | | --- | --- | --- | --- | --- | | list_id | integer(int32) | true | none | Your list id. | | name | string | true | none | Your campaign name. | | body | string | true | none | Your campaign message. | | from | string | true | [yes](http://help.clicksend.com/SMS/what-is-a-sender-id-or-sender-number) | Your sender id | | schedule | integer(int32) | false | none | Your schedule timestamp. |  Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.  &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.SmsCampaignsOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    SmsCampaignsOtherApi apiInstance = new SmsCampaignsOtherApi(defaultClient);
    String smsCampaignId = "smsCampaignId_example"; // String | 
    String contentType = "application/json"; // String | 
    CalculateSmsCampaignPriceRequest calculateSmsCampaignPriceRequest = new CalculateSmsCampaignPriceRequest(); // CalculateSmsCampaignPriceRequest | 
    try {
      UpdateSmsCampaign result = apiInstance.updateSmsCampaign(smsCampaignId, contentType, calculateSmsCampaignPriceRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SmsCampaignsOtherApi#updateSmsCampaign");
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
| **smsCampaignId** | **String**|  | |
| **contentType** | **String**|  | [optional] |
| **calculateSmsCampaignPriceRequest** | [**CalculateSmsCampaignPriceRequest**](CalculateSmsCampaignPriceRequest.md)|  | [optional] |

### Return type

[**UpdateSmsCampaign**](UpdateSmsCampaign.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewSmsCampaigns"></a>
# **viewSmsCampaigns**
> ViewSmsCampaigns viewSmsCampaigns(contentType, page, limit, q, orderBy, dateFrom, dateTo)

View SMS Campaigns

Use this endpoint to view SMS campaigns.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.SmsCampaignsOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    SmsCampaignsOtherApi apiInstance = new SmsCampaignsOtherApi(defaultClient);
    String contentType = "application/json"; // String | 
    Integer page = 1; // Integer | The page number to retrieve. Use this parameter to navigate through the [pagination]/#pagination) results. The default value is 1.
    Integer limit = 15; // Integer | The number of items to return per page. This parameter controls the size of each page of results. The default value is 15.
    String q = "q_example"; // String | Allows filtering of results based on your search criteria. The query should be in the format `field_name:value`.  1. **Field Name**: The field within the SMS campaign you want to filter by. You can use the following fields:      - sms_campaign_id,name,user_id,subaccount_id,list_id,from,body,schedule,status,date_added,custom_string,url_to_shorten,unsubscribe_link,source   2. **Value**: The text or keyword you're searching for within the specified field. If left empty after the colon, the filter will look for all templates with any value in the **Field Name**.  For example, if you are searching for a SMS campaign with the status of _Scheduled_, the final query would look like this:    - `q=status:Scheduled`  <div class=\"info-box\">   <h4><i class=\"fas fa-info-circle\"></i> Note:</h4>   <p>   Some characters have to be encoded. For example, if you are searching for SMS sent from the phone number +61437085284, your search query q would be:<br/>    <ul>     <li>q=from:%2B61437085284</li>   </ul>    You can use the <a href=\"https://www.urlencoder.org/\" target=\"_blank\">URL encoder</a> to encode the text. If a character is not an alphanumeric character (A-Z, a-z, 0-9), it is typically either reserved or unsafe and should be encoded.      </p> </div>
    String orderBy = "orderBy_example"; // String | Specifies the field and order to sort the results by. The value is composed of the field name followed by a colon and the sort direction (_asc_ for ascending or _desc_ for descending).  The default sort order is by _date_added_ in ascending order. You can use the following fields:    - _name_: The name of the SMS campaign.   - _status_: The status of the SMS campaign.   - _schedule_: The schedule send date of the SMS campaign in the <a href=\"http://help.clicksend.com/what-is-a-unix-timestamp\" target=\"_blank\">Unix format</a>.   - _from_: The sender of the SMS campaign.   - _date_added_: This is the date you created or updated the SMS campaign in the <a href=\"http://help.clicksend.com/what-is-a-unix-timestamp\" target=\"_blank\">Unix format</a>.  For example, if you want to order by the most recently sent or scheduled SMS, you should sort by date in descending order. The query would look like this:    - `order_by=schedule:desc`  <div class=\"info-box\">   <h4><i class=\"fas fa-info-circle\"></i> Note:</h4>   <p>     You can also sort by these fields: <br/>     <ul>     <li>sms_campaign_id,user_id,subaccount_id,list_id,body,custom_string,url_to_shorten,unsubscribe_link, and source.</li>   </ul>   <br/>   But this is less common in practice.   </p> </div>
    Integer dateFrom = 56; // Integer | Start date to filter results. It should be in <a href=\"http://help.clicksend.com/what-is-a-unix-timestamp\" target=\"_blank\">Unix format</a>.
    Integer dateTo = 56; // Integer | End date to filter results. It should be in <a href=\"http://help.clicksend.com/what-is-a-unix-timestamp\" target=\"_blank\">Unix format</a>.
    try {
      ViewSmsCampaigns result = apiInstance.viewSmsCampaigns(contentType, page, limit, q, orderBy, dateFrom, dateTo);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SmsCampaignsOtherApi#viewSmsCampaigns");
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
| **page** | **Integer**| The page number to retrieve. Use this parameter to navigate through the [pagination]/#pagination) results. The default value is 1. | [optional] [default to 1] |
| **limit** | **Integer**| The number of items to return per page. This parameter controls the size of each page of results. The default value is 15. | [optional] [default to 15] |
| **q** | **String**| Allows filtering of results based on your search criteria. The query should be in the format &#x60;field_name:value&#x60;.  1. **Field Name**: The field within the SMS campaign you want to filter by. You can use the following fields:      - sms_campaign_id,name,user_id,subaccount_id,list_id,from,body,schedule,status,date_added,custom_string,url_to_shorten,unsubscribe_link,source   2. **Value**: The text or keyword you&#39;re searching for within the specified field. If left empty after the colon, the filter will look for all templates with any value in the **Field Name**.  For example, if you are searching for a SMS campaign with the status of _Scheduled_, the final query would look like this:    - &#x60;q&#x3D;status:Scheduled&#x60;  &lt;div class&#x3D;\&quot;info-box\&quot;&gt;   &lt;h4&gt;&lt;i class&#x3D;\&quot;fas fa-info-circle\&quot;&gt;&lt;/i&gt; Note:&lt;/h4&gt;   &lt;p&gt;   Some characters have to be encoded. For example, if you are searching for SMS sent from the phone number +61437085284, your search query q would be:&lt;br/&gt;    &lt;ul&gt;     &lt;li&gt;q&#x3D;from:%2B61437085284&lt;/li&gt;   &lt;/ul&gt;    You can use the &lt;a href&#x3D;\&quot;https://www.urlencoder.org/\&quot; target&#x3D;\&quot;_blank\&quot;&gt;URL encoder&lt;/a&gt; to encode the text. If a character is not an alphanumeric character (A-Z, a-z, 0-9), it is typically either reserved or unsafe and should be encoded.      &lt;/p&gt; &lt;/div&gt; | [optional] |
| **orderBy** | **String**| Specifies the field and order to sort the results by. The value is composed of the field name followed by a colon and the sort direction (_asc_ for ascending or _desc_ for descending).  The default sort order is by _date_added_ in ascending order. You can use the following fields:    - _name_: The name of the SMS campaign.   - _status_: The status of the SMS campaign.   - _schedule_: The schedule send date of the SMS campaign in the &lt;a href&#x3D;\&quot;http://help.clicksend.com/what-is-a-unix-timestamp\&quot; target&#x3D;\&quot;_blank\&quot;&gt;Unix format&lt;/a&gt;.   - _from_: The sender of the SMS campaign.   - _date_added_: This is the date you created or updated the SMS campaign in the &lt;a href&#x3D;\&quot;http://help.clicksend.com/what-is-a-unix-timestamp\&quot; target&#x3D;\&quot;_blank\&quot;&gt;Unix format&lt;/a&gt;.  For example, if you want to order by the most recently sent or scheduled SMS, you should sort by date in descending order. The query would look like this:    - &#x60;order_by&#x3D;schedule:desc&#x60;  &lt;div class&#x3D;\&quot;info-box\&quot;&gt;   &lt;h4&gt;&lt;i class&#x3D;\&quot;fas fa-info-circle\&quot;&gt;&lt;/i&gt; Note:&lt;/h4&gt;   &lt;p&gt;     You can also sort by these fields: &lt;br/&gt;     &lt;ul&gt;     &lt;li&gt;sms_campaign_id,user_id,subaccount_id,list_id,body,custom_string,url_to_shorten,unsubscribe_link, and source.&lt;/li&gt;   &lt;/ul&gt;   &lt;br/&gt;   But this is less common in practice.   &lt;/p&gt; &lt;/div&gt; | [optional] |
| **dateFrom** | **Integer**| Start date to filter results. It should be in &lt;a href&#x3D;\&quot;http://help.clicksend.com/what-is-a-unix-timestamp\&quot; target&#x3D;\&quot;_blank\&quot;&gt;Unix format&lt;/a&gt;. | [optional] |
| **dateTo** | **Integer**| End date to filter results. It should be in &lt;a href&#x3D;\&quot;http://help.clicksend.com/what-is-a-unix-timestamp\&quot; target&#x3D;\&quot;_blank\&quot;&gt;Unix format&lt;/a&gt;. | [optional] |

### Return type

[**ViewSmsCampaigns**](ViewSmsCampaigns.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewSpecificSmsCampaign"></a>
# **viewSpecificSmsCampaign**
> ViewSpecificSmsCampaign viewSpecificSmsCampaign(smsCampaignId, contentType)

View Specific SMS Campaign

Use this endpoint to view a specific SMS campaign.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.SmsCampaignsOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    SmsCampaignsOtherApi apiInstance = new SmsCampaignsOtherApi(defaultClient);
    String smsCampaignId = "smsCampaignId_example"; // String | ID of SMS campaign to get
    String contentType = "application/json"; // String | 
    try {
      ViewSpecificSmsCampaign result = apiInstance.viewSpecificSmsCampaign(smsCampaignId, contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SmsCampaignsOtherApi#viewSpecificSmsCampaign");
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
| **smsCampaignId** | **String**| ID of SMS campaign to get | |
| **contentType** | **String**|  | [optional] |

### Return type

[**ViewSpecificSmsCampaign**](ViewSpecificSmsCampaign.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

