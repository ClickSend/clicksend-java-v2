# NumbersApi

All URIs are relative to *https://rest.clicksend.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**purchaseDedicatedNumber**](NumbersApi.md#purchaseDedicatedNumber) | **POST** /v3/numbers/buy/{dedicated_number} | Purchase Dedicated Number |
| [**registerNumbers**](NumbersApi.md#registerNumbers) | **POST** /v3/numbers/registrations/number-types/{number_type}/country/{country_code} | Register Numbers |
| [**viewAvailableNumbers**](NumbersApi.md#viewAvailableNumbers) | **GET** /v3/numbers/search/{country} | View Available Numbers |
| [**viewYourNumbers**](NumbersApi.md#viewYourNumbers) | **GET** /v3/numbers | View Your Numbers |


<a id="purchaseDedicatedNumber"></a>
# **purchaseDedicatedNumber**
> PurchaseDedicatedNumber purchaseDedicatedNumber(dedicatedNumber, buyNumberRequest, contentType, type)

Purchase Dedicated Number

_Buy dedicated number_  This endpoint allows you to purchase a dedicated phone number for messaging services. You can optionally include registration data for compliance purposes.  ### Request Body  | Field | Type | Required | Description | | --- | --- | --- | --- | | dedicated_number | string | true | Phone number to purchase | | type | string | true | Service type (sms, mms) | | registration_data | object | false | Registration data for compliance (AU SMS/MMS numbers only) |  #### Registration Data Fields (Optional)  | Field | Type | Required | Description | | --- | --- | --- | --- | | business_name | string | true | Name of the business (2 - 100 characters) | | business_address | string | true | Business address (5 - 150 characters) | | suburb | string | true | Suburb/City (2 - 50 characters) | | postcode | string | true | Postal code (2 - 20 characters) | | state | string | true | State/Province (2 - 50 characters) | | contact_name | string | true | Contact person name (2 - 100 characters) | | contact_number | string | true | Contact phone number (valid local or international phone number) | | country | string | true | Country code (ISO 3166-1 alpha-2) |   ### Path Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | dedicated_number | path | string | true | Phone number to purchase |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.NumbersApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    NumbersApi apiInstance = new NumbersApi(defaultClient);
    String dedicatedNumber = "+614197651956"; // String | Phone number to purchase
    BuyNumberRequest buyNumberRequest = new BuyNumberRequest(); // BuyNumberRequest | 
    String contentType = "application/json"; // String | 
    String type = "sms"; // String | 
    try {
      PurchaseDedicatedNumber result = apiInstance.purchaseDedicatedNumber(dedicatedNumber, buyNumberRequest, contentType, type);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling NumbersApi#purchaseDedicatedNumber");
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
| **dedicatedNumber** | **String**| Phone number to purchase | |
| **buyNumberRequest** | [**BuyNumberRequest**](BuyNumberRequest.md)|  | |
| **contentType** | **String**|  | [optional] |
| **type** | **String**|  | [optional] |

### Return type

[**PurchaseDedicatedNumber**](PurchaseDedicatedNumber.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="registerNumbers"></a>
# **registerNumbers**
> RegisterNumbers registerNumbers(numberType, countryCode, contentType, registerNumbersRequest)

Register Numbers

&lt;div style&#x3D;\&quot;background-color: #e8f4ff; padding: 15px; border-radius: 4px; border-left: 4px solid #0066cc;\&quot;&gt; This endpoint is currently only available for &lt;b&gt;Canada 10DLC&lt;/b&gt; number registration. &lt;/div&gt;  Registers a number that requires additional verification information. This endpoint facilitates the registration process for numbers requiring special compliance documentation.  After submission, ClickSend&#39;s compliance team will review the registration and notify you of the approval status.  Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses. &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.NumbersApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    NumbersApi apiInstance = new NumbersApi(defaultClient);
    String numberType = "10dlc"; // String | The type of number being registered
    String countryCode = "US, CA"; // String | Two-character ISO country code
    String contentType = "application/json"; // String | 
    RegisterNumbersRequest registerNumbersRequest = new RegisterNumbersRequest(); // RegisterNumbersRequest | 
    try {
      RegisterNumbers result = apiInstance.registerNumbers(numberType, countryCode, contentType, registerNumbersRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling NumbersApi#registerNumbers");
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
| **numberType** | **String**| The type of number being registered | |
| **countryCode** | **String**| Two-character ISO country code | |
| **contentType** | **String**|  | [optional] |
| **registerNumbersRequest** | [**RegisterNumbersRequest**](RegisterNumbersRequest.md)|  | [optional] |

### Return type

[**RegisterNumbers**](RegisterNumbers.md)

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

<a id="viewAvailableNumbers"></a>
# **viewAvailableNumbers**
> ViewAvailableNumbers viewAvailableNumbers(country, contentType)

View Available Numbers

_Get all dedicated numbers by country_  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | country | path | string | true | Country code to search | | search | query | string | false | Your search pattern or query. | | search_type | query | integer(int32) | false | Your strategy for searching, 0 &#x3D; starts with, 1 &#x3D; anywhere, 2 &#x3D; ends with. | | page | query | integer(int32) | false | [Page number](/#pagination) | | limit | query | integer(int32) | false | [Number of records per page](/#pagination) |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.NumbersApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    NumbersApi apiInstance = new NumbersApi(defaultClient);
    String country = "country_example"; // String | 
    String contentType = "application/json"; // String | 
    try {
      ViewAvailableNumbers result = apiInstance.viewAvailableNumbers(country, contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling NumbersApi#viewAvailableNumbers");
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
| **country** | **String**|  | |
| **contentType** | **String**|  | [optional] |

### Return type

[**ViewAvailableNumbers**](ViewAvailableNumbers.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewYourNumbers"></a>
# **viewYourNumbers**
> ViewYourNumbers viewYourNumbers(contentType, page, limit, q, q2, excludingNumberType, exclude10dlcCampaign)

View Your Numbers

_Get all available dedicated numbers_  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | page | query | integer(int32) | false | [Page number](/#pagination) | | limit | query | integer(int32) | false | [Number of records per page](/#pagination) | | q | query | string | false | Filter numbers based on multiple criteria. The query string should be formatted as key-value pairs separated by commas. Available filter keys: &#x60;type&#x60;, &#x60;number_type&#x60;, &#x60;country&#x60; | | q2 | query | string | false | Filter numbers based on multiple criteria. The query string should be formatted as key-value pairs separated by commas. Available filter keys: &#x60;type&#x60; | | excluding_number_type | query | string | false | Exclude specific number types from the results. Available number types: &#x60;shortcode&#x60;, &#x60;tollfree&#x60;, &#x60;10DLC&#x60; | | exclude_10dlc_campaign | query | boolean | false | When set to true, excludes all numbers that are associated with 10DLC campaigns |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.NumbersApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    NumbersApi apiInstance = new NumbersApi(defaultClient);
    String contentType = "application/json"; // String | 
    Integer page = 1; // Integer | Page number
    Integer limit = 15; // Integer | Number of records per page
    String q = "type:sms,number_type:longcode,country:AU"; // String | Filter numbers based on multiple criteria. The query string should be formatted as key-value pairs separated by commas. Available filter keys: - `type`: Message type (e.g., `SMS`, `MMS`) - `number_type`: Number classification (e.g., `longcode`, `shortcode`, `tollfree`, `10DLC`) - `country`: Two-letter country code (e.g., `AU`, `US`) 
    String q2 = "type:mms"; // String | 
    String excludingNumberType = "10DLC"; // String | Exclude specific number types from the results. Available number types: - `shortcode` - `tollfree` - `10DLC` 
    Boolean exclude10dlcCampaign = false; // Boolean | When set to true, excludes all numbers that are associated with 10DLC campaigns
    try {
      ViewYourNumbers result = apiInstance.viewYourNumbers(contentType, page, limit, q, q2, excludingNumberType, exclude10dlcCampaign);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling NumbersApi#viewYourNumbers");
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
| **page** | **Integer**| Page number | [optional] [default to 1] |
| **limit** | **Integer**| Number of records per page | [optional] [default to 15] |
| **q** | **String**| Filter numbers based on multiple criteria. The query string should be formatted as key-value pairs separated by commas. Available filter keys: - &#x60;type&#x60;: Message type (e.g., &#x60;SMS&#x60;, &#x60;MMS&#x60;) - &#x60;number_type&#x60;: Number classification (e.g., &#x60;longcode&#x60;, &#x60;shortcode&#x60;, &#x60;tollfree&#x60;, &#x60;10DLC&#x60;) - &#x60;country&#x60;: Two-letter country code (e.g., &#x60;AU&#x60;, &#x60;US&#x60;)  | [optional] |
| **q2** | **String**|  | [optional] |
| **excludingNumberType** | **String**| Exclude specific number types from the results. Available number types: - &#x60;shortcode&#x60; - &#x60;tollfree&#x60; - &#x60;10DLC&#x60;  | [optional] |
| **exclude10dlcCampaign** | **Boolean**| When set to true, excludes all numbers that are associated with 10DLC campaigns | [optional] [default to false] |

### Return type

[**ViewYourNumbers**](ViewYourNumbers.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

