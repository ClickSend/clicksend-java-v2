# DefaultSendersOtherApi

All URIs are relative to *https://rest.clicksend.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createDefaultSender**](DefaultSendersOtherApi.md#createDefaultSender) | **POST** /v3/senders/default-senders | Create Default Sender |
| [**deleteDefaultSender**](DefaultSendersOtherApi.md#deleteDefaultSender) | **DELETE** /v3/senders/default-senders/{default_sender_id} | Delete Default Sender |
| [**getDefaultSenderDetails**](DefaultSendersOtherApi.md#getDefaultSenderDetails) | **GET** /v3/senders/default-senders/{default_sender_id} | Get Default Sender Details |
| [**getDefaultSendersList**](DefaultSendersOtherApi.md#getDefaultSendersList) | **GET** /v3/senders/default-senders | Get List of Default Senders |
| [**listCompliantSenderTypes**](DefaultSendersOtherApi.md#listCompliantSenderTypes) | **GET** /v3/senders/compliant-sender-types | List Compliant Sender Types |
| [**updateDefaultSender**](DefaultSendersOtherApi.md#updateDefaultSender) | **PATCH** /v3/senders/default-senders/{default_sender_id} | Update Default Sender |


<a id="createDefaultSender"></a>
# **createDefaultSender**
> CreateDefaultSender createDefaultSender(contentType, createDefaultSenderRequest)

Create Default Sender

Creates a new default sender configuration to automate the selection of compliant SenderIDs. By configuring a default sender you no longer need to define the &#x60;sender_id&#x60; string when sending SMS messages. The default sender will be picked up automatically.  For more information on Sender IDs, please refer to [What is a Sender ID or Sender Number?](https://help.clicksend.com/article/4kgj7krx00-what-is-a-sender-id-or-sender-number)

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.DefaultSendersOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultSendersOtherApi apiInstance = new DefaultSendersOtherApi(defaultClient);
    String contentType = "application/json"; // String | 
    CreateDefaultSenderRequest createDefaultSenderRequest = new CreateDefaultSenderRequest(); // CreateDefaultSenderRequest | 
    try {
      CreateDefaultSender result = apiInstance.createDefaultSender(contentType, createDefaultSenderRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultSendersOtherApi#createDefaultSender");
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
| **createDefaultSenderRequest** | [**CreateDefaultSenderRequest**](CreateDefaultSenderRequest.md)|  | [optional] |

### Return type

[**CreateDefaultSender**](CreateDefaultSender.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |
| **400** | Successful response |  -  |

<a id="deleteDefaultSender"></a>
# **deleteDefaultSender**
> deleteDefaultSender(defaultSenderId, contentType)

Delete Default Sender

Removes a specified default sender setting.  If you don&#39;t configure a default sender and leave the &#x60;sender_id&#x60; string blank when sending an SMS, Smart Assign will pick the best suitable, compliant, available SenderID for you.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.DefaultSendersOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultSendersOtherApi apiInstance = new DefaultSendersOtherApi(defaultClient);
    String defaultSenderId = "defaultSenderId_example"; // String | The ID of the default sender to delete
    String contentType = "application/json"; // String | 
    try {
      apiInstance.deleteDefaultSender(defaultSenderId, contentType);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultSendersOtherApi#deleteDefaultSender");
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
| **defaultSenderId** | **String**| The ID of the default sender to delete | |
| **contentType** | **String**|  | [optional] |

### Return type

null (empty response body)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **204** | Successful response (No Content) |  -  |

<a id="getDefaultSenderDetails"></a>
# **getDefaultSenderDetails**
> GetDefaultSenderDetails getDefaultSenderDetails(defaultSenderId, contentType)

Get Default Sender Details

Retrieve detailed information about a specific default sender configuration

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.DefaultSendersOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultSendersOtherApi apiInstance = new DefaultSendersOtherApi(defaultClient);
    String defaultSenderId = "defaultSenderId_example"; // String | The ID of the default sender to retrieve
    String contentType = "application/json"; // String | 
    try {
      GetDefaultSenderDetails result = apiInstance.getDefaultSenderDetails(defaultSenderId, contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultSendersOtherApi#getDefaultSenderDetails");
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
| **defaultSenderId** | **String**| The ID of the default sender to retrieve | |
| **contentType** | **String**|  | [optional] |

### Return type

[**GetDefaultSenderDetails**](GetDefaultSenderDetails.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="getDefaultSendersList"></a>
# **getDefaultSendersList**
> GetDefaultSendersList getDefaultSendersList(contentType, offset, perPage, sortBy, sortDirection)

Get List of Default Senders

Retrieve a list of default senders for the current user

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.DefaultSendersOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultSendersOtherApi apiInstance = new DefaultSendersOtherApi(defaultClient);
    String contentType = "application/json"; // String | 
    String offset = "offset_example"; // String | Page (offset) to be used for pagination
    Integer perPage = 10; // Integer | Size of the page in pagination
    String sortBy = "created_timestamp"; // String | Parameter to sort the results by
    String sortDirection = "asc"; // String | Direction of sorting
    try {
      GetDefaultSendersList result = apiInstance.getDefaultSendersList(contentType, offset, perPage, sortBy, sortDirection);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultSendersOtherApi#getDefaultSendersList");
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
| **offset** | **String**| Page (offset) to be used for pagination | [optional] |
| **perPage** | **Integer**| Size of the page in pagination | [optional] [default to 10] |
| **sortBy** | **String**| Parameter to sort the results by | [optional] [default to created_timestamp] |
| **sortDirection** | **String**| Direction of sorting | [optional] [default to desc] [enum: asc, desc] |

### Return type

[**GetDefaultSendersList**](GetDefaultSendersList.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="listCompliantSenderTypes"></a>
# **listCompliantSenderTypes**
> ListCompliantSenderTypes200Response listCompliantSenderTypes(filterProductType, filterCountryCodeLeftCurlyBracketIndexRightCurlyBracket)

List Compliant Sender Types

Retrieves the list of compliant sender types for specific countries

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.DefaultSendersOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultSendersOtherApi apiInstance = new DefaultSendersOtherApi(defaultClient);
    String filterProductType = "SMS"; // String | Type of the product
    List<String> filterCountryCodeLeftCurlyBracketIndexRightCurlyBracket = Arrays.asList(); // List<String> | Array of recipient country codes (ISO 3166-1 alpha-2). If not specified, will get all compliant sender types for all countries. Replace `{index}` with the appropriate index value.  <small>Example:</small> <small><code style=\"color: #424242;\">filter[country_code][0]=US&filter[country_code][1]=AU</code></small> 
    try {
      ListCompliantSenderTypes200Response result = apiInstance.listCompliantSenderTypes(filterProductType, filterCountryCodeLeftCurlyBracketIndexRightCurlyBracket);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultSendersOtherApi#listCompliantSenderTypes");
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
| **filterProductType** | **String**| Type of the product | [enum: SMS] |
| **filterCountryCodeLeftCurlyBracketIndexRightCurlyBracket** | [**List&lt;String&gt;**](String.md)| Array of recipient country codes (ISO 3166-1 alpha-2). If not specified, will get all compliant sender types for all countries. Replace &#x60;{index}&#x60; with the appropriate index value.  &lt;small&gt;Example:&lt;/small&gt; &lt;small&gt;&lt;code style&#x3D;\&quot;color: #424242;\&quot;&gt;filter[country_code][0]&#x3D;US&amp;filter[country_code][1]&#x3D;AU&lt;/code&gt;&lt;/small&gt;  | [optional] |

### Return type

[**ListCompliantSenderTypes200Response**](ListCompliantSenderTypes200Response.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="updateDefaultSender"></a>
# **updateDefaultSender**
> UpdateDefaultSender updateDefaultSender(defaultSenderId, contentType, updateDefaultSenderRequest)

Update Default Sender

Updates the details of an existing default sender configuration.  For more information on Sender IDs, please refer to [What is a Sender ID or Sender Number?](https://help.clicksend.com/article/4kgj7krx00-what-is-a-sender-id-or-sender-number)

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.DefaultSendersOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultSendersOtherApi apiInstance = new DefaultSendersOtherApi(defaultClient);
    String defaultSenderId = "defaultSenderId_example"; // String | The ID of the default sender to update
    String contentType = "application/json"; // String | 
    UpdateDefaultSenderRequest updateDefaultSenderRequest = new UpdateDefaultSenderRequest(); // UpdateDefaultSenderRequest | 
    try {
      UpdateDefaultSender result = apiInstance.updateDefaultSender(defaultSenderId, contentType, updateDefaultSenderRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultSendersOtherApi#updateDefaultSender");
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
| **defaultSenderId** | **String**| The ID of the default sender to update | |
| **contentType** | **String**|  | [optional] |
| **updateDefaultSenderRequest** | [**UpdateDefaultSenderRequest**](UpdateDefaultSenderRequest.md)|  | [optional] |

### Return type

[**UpdateDefaultSender**](UpdateDefaultSender.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |
| **400** | Bad request |  -  |

