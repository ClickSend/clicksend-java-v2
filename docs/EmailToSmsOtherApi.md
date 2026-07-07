# EmailToSmsOtherApi

All URIs are relative to *https://rest.clicksend.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**addAllowedEmail**](EmailToSmsOtherApi.md#addAllowedEmail) | **POST** /v3/sms/email-sms | Add Allowed Email |
| [**createStrippedStringRule**](EmailToSmsOtherApi.md#createStrippedStringRule) | **POST** /v3/sms/email-sms-stripped-strings | Create Stripped String Rule |
| [**deleteStrippedStringRule**](EmailToSmsOtherApi.md#deleteStrippedStringRule) | **DELETE** /v3/sms/email-sms-stripped-strings/{rule_id} | Delete Stripped String Rule |
| [**updateStrippedStringRule**](EmailToSmsOtherApi.md#updateStrippedStringRule) | **PUT** /v3/sms/email-sms-stripped-strings/{rule_id} | Update Stripped String Rule |
| [**viewAllowedEmails**](EmailToSmsOtherApi.md#viewAllowedEmails) | **GET** /v3/sms/email-sms | View Allowed Emails |
| [**viewStrippedStringRule**](EmailToSmsOtherApi.md#viewStrippedStringRule) | **GET** /v3/sms/email-sms-stripped-strings/{rule_id} | View Stripped String Rule |
| [**viewStrippedStringRules**](EmailToSmsOtherApi.md#viewStrippedStringRules) | **GET** /v3/sms/email-sms-stripped-strings | View Stripped String Rules |


<a id="addAllowedEmail"></a>
# **addAllowedEmail**
> AddAllowedEmail addAllowedEmail(contentType, addAllowedEmailRequest)

Add Allowed Email

_Create email to sms allowed address_  ### Properties  | Name | Type | Required | Restrictions | Description | | --- | --- | --- | --- | --- | | email_address | string | true | none | Your email address | | from | string | false | [yes](http://help.clicksend.com/SMS/what-is-a-sender-id-or-sender-number) | Your sender id |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.EmailToSmsOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    EmailToSmsOtherApi apiInstance = new EmailToSmsOtherApi(defaultClient);
    String contentType = "application/json"; // String | 
    AddAllowedEmailRequest addAllowedEmailRequest = new AddAllowedEmailRequest(); // AddAllowedEmailRequest | 
    try {
      AddAllowedEmail result = apiInstance.addAllowedEmail(contentType, addAllowedEmailRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling EmailToSmsOtherApi#addAllowedEmail");
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
| **addAllowedEmailRequest** | [**AddAllowedEmailRequest**](AddAllowedEmailRequest.md)|  | [optional] |

### Return type

[**AddAllowedEmail**](AddAllowedEmail.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="createStrippedStringRule"></a>
# **createStrippedStringRule**
> CreateStrippedStringRule createStrippedStringRule(contentType, createStrippedStringRuleRequest)

Create Stripped String Rule

_Create email to sms stripped string rule_  Create email to sms stripped string rules  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | stripped-string | body | string | true | String to be stripped. |  Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.  &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.EmailToSmsOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    EmailToSmsOtherApi apiInstance = new EmailToSmsOtherApi(defaultClient);
    String contentType = "application/json"; // String | 
    CreateStrippedStringRuleRequest createStrippedStringRuleRequest = new CreateStrippedStringRuleRequest(); // CreateStrippedStringRuleRequest | 
    try {
      CreateStrippedStringRule result = apiInstance.createStrippedStringRule(contentType, createStrippedStringRuleRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling EmailToSmsOtherApi#createStrippedStringRule");
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
| **createStrippedStringRuleRequest** | [**CreateStrippedStringRuleRequest**](CreateStrippedStringRuleRequest.md)|  | [optional] |

### Return type

[**CreateStrippedStringRule**](CreateStrippedStringRule.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="deleteStrippedStringRule"></a>
# **deleteStrippedStringRule**
> DeleteStrippedStringRule deleteStrippedStringRule(ruleId, contentType)

Delete Stripped String Rule

_Delete email to sms stripped string rule_  Delete email to sms stripped string rule  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | rule_id | path | integer(int32) | true | Your rule id |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.EmailToSmsOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    EmailToSmsOtherApi apiInstance = new EmailToSmsOtherApi(defaultClient);
    String ruleId = "ruleId_example"; // String | 
    String contentType = "application/json"; // String | 
    try {
      DeleteStrippedStringRule result = apiInstance.deleteStrippedStringRule(ruleId, contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling EmailToSmsOtherApi#deleteStrippedStringRule");
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
| **ruleId** | **String**|  | |
| **contentType** | **String**|  | [optional] |

### Return type

[**DeleteStrippedStringRule**](DeleteStrippedStringRule.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="updateStrippedStringRule"></a>
# **updateStrippedStringRule**
> UpdateStrippedStringRule updateStrippedStringRule(ruleId, contentType, createStrippedStringRuleRequest)

Update Stripped String Rule

_Update email to sms stripped string rule_  Update email to sms stripped string rule  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | rule_id | path | integer(int32) | true | Your rule id | | stripped-string | body | string | true | String to be stripped. |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.EmailToSmsOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    EmailToSmsOtherApi apiInstance = new EmailToSmsOtherApi(defaultClient);
    String ruleId = "ruleId_example"; // String | 
    String contentType = "application/json"; // String | 
    CreateStrippedStringRuleRequest createStrippedStringRuleRequest = new CreateStrippedStringRuleRequest(); // CreateStrippedStringRuleRequest | 
    try {
      UpdateStrippedStringRule result = apiInstance.updateStrippedStringRule(ruleId, contentType, createStrippedStringRuleRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling EmailToSmsOtherApi#updateStrippedStringRule");
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
| **ruleId** | **String**|  | |
| **contentType** | **String**|  | [optional] |
| **createStrippedStringRuleRequest** | [**CreateStrippedStringRuleRequest**](CreateStrippedStringRuleRequest.md)|  | [optional] |

### Return type

[**UpdateStrippedStringRule**](UpdateStrippedStringRule.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewAllowedEmails"></a>
# **viewAllowedEmails**
> ViewAllowedEmails viewAllowedEmails(contentType)

View Allowed Emails

_Get list of email to sms allowed addresses_  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | page | query | integer(int32) | false | [Page number](/#pagination) | | limit | query | integer(int32) | false | [Number of records per page](/#pagination) |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.EmailToSmsOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    EmailToSmsOtherApi apiInstance = new EmailToSmsOtherApi(defaultClient);
    String contentType = "application/json"; // String | 
    try {
      ViewAllowedEmails result = apiInstance.viewAllowedEmails(contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling EmailToSmsOtherApi#viewAllowedEmails");
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

[**ViewAllowedEmails**](ViewAllowedEmails.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewStrippedStringRule"></a>
# **viewStrippedStringRule**
> ViewStrippedStringRule viewStrippedStringRule(ruleId, contentType)

View Stripped String Rule

_Get email to sms stripped string rule_  Get email to sms stripped string rule  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | rule_id | path | integer(int32) | true | Your rule id |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.EmailToSmsOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    EmailToSmsOtherApi apiInstance = new EmailToSmsOtherApi(defaultClient);
    String ruleId = "ruleId_example"; // String | 
    String contentType = "application/json"; // String | 
    try {
      ViewStrippedStringRule result = apiInstance.viewStrippedStringRule(ruleId, contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling EmailToSmsOtherApi#viewStrippedStringRule");
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
| **ruleId** | **String**|  | |
| **contentType** | **String**|  | [optional] |

### Return type

[**ViewStrippedStringRule**](ViewStrippedStringRule.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewStrippedStringRules"></a>
# **viewStrippedStringRules**
> ViewStrippedStringRules viewStrippedStringRules(contentType)

View Stripped String Rules

_Get list of email to sms stripped string rules_  Get list of email to sms stripped string rules  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | page | query | integer(int32) | false | Page number | | limit | query | integer(int32) | false | Number of records per page |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.EmailToSmsOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    EmailToSmsOtherApi apiInstance = new EmailToSmsOtherApi(defaultClient);
    String contentType = "application/json"; // String | 
    try {
      ViewStrippedStringRules result = apiInstance.viewStrippedStringRules(contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling EmailToSmsOtherApi#viewStrippedStringRules");
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

[**ViewStrippedStringRules**](ViewStrippedStringRules.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

