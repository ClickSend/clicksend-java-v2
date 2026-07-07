# EmailOtherApi

All URIs are relative to *https://rest.clicksend.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**calculateEmailCampaignPrice**](EmailOtherApi.md#calculateEmailCampaignPrice) | **POST** /v3/email-campaigns/price | Calculate Email Campaign Price |
| [**calculateEmailPrice**](EmailOtherApi.md#calculateEmailPrice) | **POST** /v3/email/price | Calculate Email Price |
| [**cancelEmailCampaign**](EmailOtherApi.md#cancelEmailCampaign) | **PUT** /v3/email-campaigns/{email_campaign_id}/cancel | Cancel Email Campaign |
| [**createAllowedEmailAddress**](EmailOtherApi.md#createAllowedEmailAddress) | **POST** /v3/email/addresses | Create Allowed Email Address |
| [**createEmailDeliveryReceiptRule**](EmailOtherApi.md#createEmailDeliveryReceiptRule) | **POST** /v3/automations/email/receipts | Create Email Delivery Receipt Rule |
| [**createEmailTemplate**](EmailOtherApi.md#createEmailTemplate) | **POST** /v3/email/templates | Create Email Template |
| [**deleteAllowedEmailAddress**](EmailOtherApi.md#deleteAllowedEmailAddress) | **DELETE** /v3/email/addresses/{email_address_id} | Delete Allowed Email Address |
| [**deleteEmailDeliveryReceiptRule**](EmailOtherApi.md#deleteEmailDeliveryReceiptRule) | **DELETE** /v3/automations/email/receipts/{receipt_rule_id} | Delete Email Delivery Receipt Rule |
| [**deleteEmailTemplate**](EmailOtherApi.md#deleteEmailTemplate) | **DELETE** /v3/email/templates/{template_id} | Delete Email Template |
| [**exportEmailCampaignHistory**](EmailOtherApi.md#exportEmailCampaignHistory) | **GET** /v3/email-campaigns/{email_campaign_id}/history/export | Export Email Campaign History |
| [**exportEmailHistory**](EmailOtherApi.md#exportEmailHistory) | **GET** /v3/email/history/export | Export Email History |
| [**sendEmail**](EmailOtherApi.md#sendEmail) | **POST** /v3/email/send | Send Email |
| [**sendEmailCampaign**](EmailOtherApi.md#sendEmailCampaign) | **POST** /v3/email-campaigns/send | Send Email Campaign |
| [**sendEmailVerificationToken**](EmailOtherApi.md#sendEmailVerificationToken) | **PUT** /v3/email/address-verify/{email_address_id}/send | Send Email Verification Token |
| [**updateEmailCampaign**](EmailOtherApi.md#updateEmailCampaign) | **PUT** /v3/email-campaigns/{email_campaign_id} | Update Email Campaign |
| [**updateEmailDeliveryReceiptRule**](EmailOtherApi.md#updateEmailDeliveryReceiptRule) | **PUT** /v3/automations/email/receipts/{receipt_rule_id} | Update Email Delivery Receipt Rule |
| [**updateEmailTemplate**](EmailOtherApi.md#updateEmailTemplate) | **PUT** /v3/email/templates/{template_id} | Update Email Template |
| [**verifyAllowedEmailAddress**](EmailOtherApi.md#verifyAllowedEmailAddress) | **PUT** /v3/email/address-verify/{email_address_id}/verify/{activation_token} | Verify Allowed Email Address |
| [**viewAllEmailCampaigns**](EmailOtherApi.md#viewAllEmailCampaigns) | **GET** /v3/email-campaigns | View All Email Campaigns |
| [**viewAllowedEmailAddress**](EmailOtherApi.md#viewAllowedEmailAddress) | **GET** /v3/email/addresses/{email_address_id} | View Allowed Email Address |
| [**viewAllowedEmailAddresses**](EmailOtherApi.md#viewAllowedEmailAddresses) | **GET** /v3/email/addresses | View Allowed Email Addresses |
| [**viewEmailCampaign**](EmailOtherApi.md#viewEmailCampaign) | **GET** /v3/email-campaigns/{email_campaign_id} | View Email Campaign |
| [**viewEmailCampaignHistory**](EmailOtherApi.md#viewEmailCampaignHistory) | **GET** /v3/email-campaigns/{email_campaign_id}/history | View Email Campaign History |
| [**viewEmailDeliveryReceiptRule**](EmailOtherApi.md#viewEmailDeliveryReceiptRule) | **GET** /v3/automations/email/receipts/{receipt_rule_id} | View Email Delivery Receipt Rule |
| [**viewEmailDeliveryReceiptRules**](EmailOtherApi.md#viewEmailDeliveryReceiptRules) | **GET** /v3/automations/email/receipts | View Email Delivery Receipt Rules |
| [**viewEmailHistory**](EmailOtherApi.md#viewEmailHistory) | **GET** /v3/email/history | View Email History |
| [**viewEmailTemplate**](EmailOtherApi.md#viewEmailTemplate) | **GET** /v3/email/templates/{template_id} | View Email Template |
| [**viewEmailTemplates**](EmailOtherApi.md#viewEmailTemplates) | **GET** /v3/email/templates | View Email Templates |
| [**viewMasterEmailTemplate**](EmailOtherApi.md#viewMasterEmailTemplate) | **GET** /v3/email/master-templates/{template_id} | View Master Email Template |
| [**viewMasterEmailTemplates**](EmailOtherApi.md#viewMasterEmailTemplates) | **GET** /v3/email/master-templates | View Master Email Templates |
| [**viewTemplateCategories**](EmailOtherApi.md#viewTemplateCategories) | **GET** /v3/email/master-templates-categories | View Template Categories |
| [**viewTemplateCategory**](EmailOtherApi.md#viewTemplateCategory) | **GET** /v3/email/master-templates-categories/{category_id} | View Template Category |
| [**viewTemplatesInCategory**](EmailOtherApi.md#viewTemplatesInCategory) | **GET** /v3/email/master-templates-categories/{category_id}/master-templates | View Templates in Category |


<a id="calculateEmailCampaignPrice"></a>
# **calculateEmailCampaignPrice**
> CalculateEmailCampaignPrice calculateEmailCampaignPrice(contentType, calculateEmailCampaignPriceRequest)

Calculate Email Campaign Price

_Calculate email campaign price_  Calculate email campaign price  ### Properties  | Name | Type | Required | Restrictions | Description | | --- | --- | --- | --- | --- | | name | string | true | none | Your campaign name. | | subject | string | true | none | Your campaign subject. | | body | string | true | none | Your campaign message. | | from_email_address_id | number | true | none | The allowed email address id. | | from_name | string | true | none | Your name or business name. | | template_id | number | false | none | Your template id. | | list_id | number | true | none | Your contact list id. | | schedule | integer(int32) | false | none | Your schedule timestamp. |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.EmailOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    EmailOtherApi apiInstance = new EmailOtherApi(defaultClient);
    String contentType = "application/json"; // String | 
    CalculateEmailCampaignPriceRequest calculateEmailCampaignPriceRequest = new CalculateEmailCampaignPriceRequest(); // CalculateEmailCampaignPriceRequest | 
    try {
      CalculateEmailCampaignPrice result = apiInstance.calculateEmailCampaignPrice(contentType, calculateEmailCampaignPriceRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling EmailOtherApi#calculateEmailCampaignPrice");
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
| **calculateEmailCampaignPriceRequest** | [**CalculateEmailCampaignPriceRequest**](CalculateEmailCampaignPriceRequest.md)|  | [optional] |

### Return type

[**CalculateEmailCampaignPrice**](CalculateEmailCampaignPrice.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="calculateEmailPrice"></a>
# **calculateEmailPrice**
> CalculateEmailPrice calculateEmailPrice(contentType, calculateEmailPriceRequest)

Calculate Email Price

_Get transactional email price_  Get transactional email price  ### Properties  | Name | Type | Required | Restrictions | Description | | --- | --- | --- | --- | --- | | to | array | true | none | Array of To Recipient items. (array of names and emails) | | cc | array | false | none | Array of Cc Recipient items. (array of names and emails) | | bcc | array | false | none | Array of Bcc Recipient items. (array of names and emails) | | from | object | true | none | From Email object. (object containing name and email) | | body | string | true | none | Body of the email. | | attachments | array | false | none | Array of Attachment items. | | schedule | number | false | none | Schedule. | | name | string | false | none | Name of person email belongs to | | email | string | true | none | Email to be used. | | content | string | true | none | The base64-encoded contents of the file. | | type | string | true | none | The type of file being attached. | | filename | string | true | none | The name of the file being attached. | | disposition | string | true | none | Inline for content that can be displayed within the email, or attachment for any other files. | | content_id | string | true | none | An ID for the content. |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.EmailOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    EmailOtherApi apiInstance = new EmailOtherApi(defaultClient);
    String contentType = "application/json"; // String | 
    CalculateEmailPriceRequest calculateEmailPriceRequest = new CalculateEmailPriceRequest(); // CalculateEmailPriceRequest | 
    try {
      CalculateEmailPrice result = apiInstance.calculateEmailPrice(contentType, calculateEmailPriceRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling EmailOtherApi#calculateEmailPrice");
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
| **calculateEmailPriceRequest** | [**CalculateEmailPriceRequest**](CalculateEmailPriceRequest.md)|  | [optional] |

### Return type

[**CalculateEmailPrice**](CalculateEmailPrice.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="cancelEmailCampaign"></a>
# **cancelEmailCampaign**
> CancelEmailCampaign cancelEmailCampaign(emailCampaignId, contentType, cancelEmailCampaignRequest)

Cancel Email Campaign

_Cancel email campaign_  Cancel email campaign  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | email_campaign_id | path | integer(int32) | true | Allowed email campaign id | | date_from | query | integer(int32) | false | Start date (Unix Timestamp e.g. 1436849372) | | date_to | query | integer(int32) | false | End date (Unix Timestamp e.g. 1436879372) | | page | query | integer(int32) | false | [Page number](/#pagination) | | limit | query | integer(int32) | false | [Number of records per page](/#pagination) |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.EmailOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    EmailOtherApi apiInstance = new EmailOtherApi(defaultClient);
    String emailCampaignId = "emailCampaignId_example"; // String | 
    String contentType = "application/json"; // String | 
    CancelEmailCampaignRequest cancelEmailCampaignRequest = new CancelEmailCampaignRequest(); // CancelEmailCampaignRequest | 
    try {
      CancelEmailCampaign result = apiInstance.cancelEmailCampaign(emailCampaignId, contentType, cancelEmailCampaignRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling EmailOtherApi#cancelEmailCampaign");
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
| **emailCampaignId** | **String**|  | |
| **contentType** | **String**|  | [optional] |
| **cancelEmailCampaignRequest** | [**CancelEmailCampaignRequest**](CancelEmailCampaignRequest.md)|  | [optional] |

### Return type

[**CancelEmailCampaign**](CancelEmailCampaign.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="createAllowedEmailAddress"></a>
# **createAllowedEmailAddress**
> CreateAllowedEmailAddress createAllowedEmailAddress(contentType, createAllowedEmailAddressRequest)

Create Allowed Email Address

_Create allowed Email Address_  Create allowed Email Address  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | body | body | string | true | Email to be allowed. |  Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.  &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.EmailOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    EmailOtherApi apiInstance = new EmailOtherApi(defaultClient);
    String contentType = "application/json"; // String | 
    CreateAllowedEmailAddressRequest createAllowedEmailAddressRequest = new CreateAllowedEmailAddressRequest(); // CreateAllowedEmailAddressRequest | 
    try {
      CreateAllowedEmailAddress result = apiInstance.createAllowedEmailAddress(contentType, createAllowedEmailAddressRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling EmailOtherApi#createAllowedEmailAddress");
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
| **createAllowedEmailAddressRequest** | [**CreateAllowedEmailAddressRequest**](CreateAllowedEmailAddressRequest.md)|  | [optional] |

### Return type

[**CreateAllowedEmailAddress**](CreateAllowedEmailAddress.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="createEmailDeliveryReceiptRule"></a>
# **createEmailDeliveryReceiptRule**
> CreateEmailDeliveryReceiptRule createEmailDeliveryReceiptRule(contentType, createSmsDeliveryReceiptRuleRequest)

Create Email Delivery Receipt Rule

_Create email delivery receipt automations_  Create email delivery receipt automations  ### Properties  | Name | Type | Required | Restrictions | Description | | --- | --- | --- | --- | --- | | rule_name | string | true | none | Rule Name. | | match_type | number | true | none | Match Type. 0&#x3D;All reports. | | action | string | true | none | Action to be taken (AUTO_REPLY, EMAIL_USER, EMAIL_FIXED, URL, SMS, POLL, GROUP_SMS, MOVE_CONTACT, CREATE_CONTACT, CREATE_CONTACT_PLUS_EMAIL, CREATE_CONTACT_PLUS_NAME_EMAIL CREATE_CONTACT_PLUS_NAME, SMPP, NONE). | | action_address | string | true | none | Action address. | | enabled | number | true | none | Enabled: Disabled&#x3D;0 or Enabled&#x3D;1. |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.EmailOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    EmailOtherApi apiInstance = new EmailOtherApi(defaultClient);
    String contentType = "application/json"; // String | 
    CreateSmsDeliveryReceiptRuleRequest createSmsDeliveryReceiptRuleRequest = new CreateSmsDeliveryReceiptRuleRequest(); // CreateSmsDeliveryReceiptRuleRequest | 
    try {
      CreateEmailDeliveryReceiptRule result = apiInstance.createEmailDeliveryReceiptRule(contentType, createSmsDeliveryReceiptRuleRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling EmailOtherApi#createEmailDeliveryReceiptRule");
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
| **createSmsDeliveryReceiptRuleRequest** | [**CreateSmsDeliveryReceiptRuleRequest**](CreateSmsDeliveryReceiptRuleRequest.md)|  | [optional] |

### Return type

[**CreateEmailDeliveryReceiptRule**](CreateEmailDeliveryReceiptRule.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="createEmailTemplate"></a>
# **createEmailTemplate**
> CreateEmailTemplate createEmailTemplate(contentType, createEmailTemplateRequest)

Create Email Template

_Create email template_  Create email template  ### Properties  | Name | Type | Required | Restrictions | Description | | --- | --- | --- | --- | --- | | template_name | string | true | none | The intended name for the new template. | | template_id_master | number | true | none | The ID of the master template you want to base on. |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.EmailOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    EmailOtherApi apiInstance = new EmailOtherApi(defaultClient);
    String contentType = "application/json"; // String | 
    CreateEmailTemplateRequest createEmailTemplateRequest = new CreateEmailTemplateRequest(); // CreateEmailTemplateRequest | 
    try {
      CreateEmailTemplate result = apiInstance.createEmailTemplate(contentType, createEmailTemplateRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling EmailOtherApi#createEmailTemplate");
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
| **createEmailTemplateRequest** | [**CreateEmailTemplateRequest**](CreateEmailTemplateRequest.md)|  | [optional] |

### Return type

[**CreateEmailTemplate**](CreateEmailTemplate.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="deleteAllowedEmailAddress"></a>
# **deleteAllowedEmailAddress**
> DeleteAllowedEmailAddress deleteAllowedEmailAddress(emailAddressId, contentType)

Delete Allowed Email Address

_Delete specific email address_  Delete specific email address  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | email_address_id | path | integer(int32) | true | Allowed email address id |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.EmailOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    EmailOtherApi apiInstance = new EmailOtherApi(defaultClient);
    String emailAddressId = "emailAddressId_example"; // String | 
    String contentType = "application/json"; // String | 
    try {
      DeleteAllowedEmailAddress result = apiInstance.deleteAllowedEmailAddress(emailAddressId, contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling EmailOtherApi#deleteAllowedEmailAddress");
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
| **emailAddressId** | **String**|  | |
| **contentType** | **String**|  | [optional] |

### Return type

[**DeleteAllowedEmailAddress**](DeleteAllowedEmailAddress.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="deleteEmailDeliveryReceiptRule"></a>
# **deleteEmailDeliveryReceiptRule**
> DeleteEmailDeliveryReceiptRule deleteEmailDeliveryReceiptRule(receiptRuleId, contentType)

Delete Email Delivery Receipt Rule

_Delete email delivery receipt automation_  Delete email delivery receipt automation  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | receipt_rule_id | path | integer(int32) | true | Receipt rule id |  Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.  This endpoint requires authentication, [more info...](/#authentication)   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.EmailOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    EmailOtherApi apiInstance = new EmailOtherApi(defaultClient);
    String receiptRuleId = "receiptRuleId_example"; // String | 
    String contentType = "application/json"; // String | 
    try {
      DeleteEmailDeliveryReceiptRule result = apiInstance.deleteEmailDeliveryReceiptRule(receiptRuleId, contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling EmailOtherApi#deleteEmailDeliveryReceiptRule");
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
| **receiptRuleId** | **String**|  | |
| **contentType** | **String**|  | [optional] |

### Return type

[**DeleteEmailDeliveryReceiptRule**](DeleteEmailDeliveryReceiptRule.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="deleteEmailTemplate"></a>
# **deleteEmailTemplate**
> DeleteEmailTemplate deleteEmailTemplate(templateId, contentType)

Delete Email Template

_Delete user email template_  Delete user email template  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | template_id | path | integer(int32) | true | Email template id |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.EmailOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    EmailOtherApi apiInstance = new EmailOtherApi(defaultClient);
    String templateId = "templateId_example"; // String | 
    String contentType = "application/json"; // String | 
    try {
      DeleteEmailTemplate result = apiInstance.deleteEmailTemplate(templateId, contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling EmailOtherApi#deleteEmailTemplate");
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
| **templateId** | **String**|  | |
| **contentType** | **String**|  | [optional] |

### Return type

[**DeleteEmailTemplate**](DeleteEmailTemplate.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="exportEmailCampaignHistory"></a>
# **exportEmailCampaignHistory**
> exportEmailCampaignHistory(emailCampaignId, contentType)

Export Email Campaign History

_Export specific email campaign history_  Export specific email campaign history  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | email_campaign_id | path | integer(int32) | true | Allowed email campaign id | | date_from | query | integer(int32) | false | Start date (Unix Timestamp e.g. 1436849372) | | date_to | query | integer(int32) | false | End date (Unix Timestamp e.g. 1436879372) |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.EmailOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    EmailOtherApi apiInstance = new EmailOtherApi(defaultClient);
    String emailCampaignId = "emailCampaignId_example"; // String | 
    String contentType = "application/json"; // String | 
    try {
      apiInstance.exportEmailCampaignHistory(emailCampaignId, contentType);
    } catch (ApiException e) {
      System.err.println("Exception when calling EmailOtherApi#exportEmailCampaignHistory");
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
| **emailCampaignId** | **String**|  | |
| **contentType** | **String**|  | [optional] |

### Return type

null (empty response body)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="exportEmailHistory"></a>
# **exportEmailHistory**
> ExportEmailHistory exportEmailHistory(contentType)

Export Email History

_Export all Transactional Email history_  Export all Transactional Email history  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | filename | query | string | true | Filename to download history as | | date_from | query | integer(int32) | false | Start date (Unix Timestamp e.g. 1436849372) | | date_to | query | integer(int32) | false | End date (Unix Timestamp e.g. 1436879372) |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.EmailOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    EmailOtherApi apiInstance = new EmailOtherApi(defaultClient);
    String contentType = "application/json"; // String | 
    try {
      ExportEmailHistory result = apiInstance.exportEmailHistory(contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling EmailOtherApi#exportEmailHistory");
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

[**ExportEmailHistory**](ExportEmailHistory.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="sendEmail"></a>
# **sendEmail**
> SendEmail sendEmail(contentType, sendEmailRequest)

Send Email

_Send transactional email_  Send transactional email  ### Properties  | Name | Type | Required | Restrictions | Description | | --- | --- | --- | --- | --- | | to | array | true | none | Array of To Recipient items. (array of names and emails) | | cc | array | false | none | Array of Cc Recipient items. (array of names and emails) | | bcc | array | false | none | Array of Bcc Recipient items. (array of names and emails) | | from | object | true | none | From Email object. (object containing name and email) | | body | string | true | none | Body of the email. | | attachments | array | false | none | Array of Attachment items. | | schedule | number | false | none | Schedule. | | name | string | false | none | Name of person email belongs to | | email | string | true | none | Email to be used. | | content | string | true | none | The base64-encoded contents of the file. | | type | string | true | none | The type of file being attached. | | filename | string | true | none | The name of the file being attached. | | disposition | string | true | none | Inline for content that can be displayed within the email, or attachment for any other files. | | content_id | string | true | none | An ID for the content. |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.EmailOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    EmailOtherApi apiInstance = new EmailOtherApi(defaultClient);
    String contentType = "application/json"; // String | 
    SendEmailRequest sendEmailRequest = new SendEmailRequest(); // SendEmailRequest | 
    try {
      SendEmail result = apiInstance.sendEmail(contentType, sendEmailRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling EmailOtherApi#sendEmail");
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
| **sendEmailRequest** | [**SendEmailRequest**](SendEmailRequest.md)|  | [optional] |

### Return type

[**SendEmail**](SendEmail.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="sendEmailCampaign"></a>
# **sendEmailCampaign**
> SendEmailCampaign sendEmailCampaign(contentType, sendEmailCampaignRequest)

Send Email Campaign

_Send email campaign_  Send email campaign  ### Properties  | Name | Type | Required | Restrictions | Description | | --- | --- | --- | --- | --- | | name | string | true | none | Your campaign name. | | subject | string | true | none | Your campaign subject. | | body | string | true | none | Your campaign message. | | from_email_address_id | number | true | none | The allowed email address id. | | from_name | string | true | none | Your name or business name. | | template_id | number | false | none | Your template id. | | list_id | number | true | none | Your contact list id. | | schedule | integer(int32) | false | none | Your schedule timestamp. |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.EmailOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    EmailOtherApi apiInstance = new EmailOtherApi(defaultClient);
    String contentType = "application/json"; // String | 
    SendEmailCampaignRequest sendEmailCampaignRequest = new SendEmailCampaignRequest(); // SendEmailCampaignRequest | 
    try {
      SendEmailCampaign result = apiInstance.sendEmailCampaign(contentType, sendEmailCampaignRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling EmailOtherApi#sendEmailCampaign");
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
| **sendEmailCampaignRequest** | [**SendEmailCampaignRequest**](SendEmailCampaignRequest.md)|  | [optional] |

### Return type

[**SendEmailCampaign**](SendEmailCampaign.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="sendEmailVerificationToken"></a>
# **sendEmailVerificationToken**
> SendEmailVerificationToken sendEmailVerificationToken(emailAddressId, contentType, sendEmailVerificationTokenRequest)

Send Email Verification Token

_Send verification token_  Send verification token  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | email_address_id | path | integer(int32) | true | Allowed email address id |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.EmailOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    EmailOtherApi apiInstance = new EmailOtherApi(defaultClient);
    String emailAddressId = "emailAddressId_example"; // String | 
    String contentType = "application/json"; // String | 
    SendEmailVerificationTokenRequest sendEmailVerificationTokenRequest = new SendEmailVerificationTokenRequest(); // SendEmailVerificationTokenRequest | 
    try {
      SendEmailVerificationToken result = apiInstance.sendEmailVerificationToken(emailAddressId, contentType, sendEmailVerificationTokenRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling EmailOtherApi#sendEmailVerificationToken");
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
| **emailAddressId** | **String**|  | |
| **contentType** | **String**|  | [optional] |
| **sendEmailVerificationTokenRequest** | [**SendEmailVerificationTokenRequest**](SendEmailVerificationTokenRequest.md)|  | [optional] |

### Return type

[**SendEmailVerificationToken**](SendEmailVerificationToken.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="updateEmailCampaign"></a>
# **updateEmailCampaign**
> UpdateEmailCampaign updateEmailCampaign(emailCampaignId, contentType, updateEmailCampaignRequest)

Update Email Campaign

_Edit email campaign_  Edit email campaign  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | email_campaign_id | path | integer(int32) | true | Allowed email campaign id |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.EmailOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    EmailOtherApi apiInstance = new EmailOtherApi(defaultClient);
    String emailCampaignId = "emailCampaignId_example"; // String | 
    String contentType = "application/json"; // String | 
    UpdateEmailCampaignRequest updateEmailCampaignRequest = new UpdateEmailCampaignRequest(); // UpdateEmailCampaignRequest | 
    try {
      UpdateEmailCampaign result = apiInstance.updateEmailCampaign(emailCampaignId, contentType, updateEmailCampaignRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling EmailOtherApi#updateEmailCampaign");
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
| **emailCampaignId** | **String**|  | |
| **contentType** | **String**|  | [optional] |
| **updateEmailCampaignRequest** | [**UpdateEmailCampaignRequest**](UpdateEmailCampaignRequest.md)|  | [optional] |

### Return type

[**UpdateEmailCampaign**](UpdateEmailCampaign.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="updateEmailDeliveryReceiptRule"></a>
# **updateEmailDeliveryReceiptRule**
> UpdateEmailDeliveryReceiptRule updateEmailDeliveryReceiptRule(receiptRuleId, contentType, createSmsDeliveryReceiptRuleRequest)

Update Email Delivery Receipt Rule

_Update email delivery receipt automation_  Update email delivery receipt automation  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | receipt_rule_id | path | integer(int32) | true | Receipt rule id |  ### Properties  | Name | Type | Required | Restrictions | Description | | --- | --- | --- | --- | --- | | rule_name | string | true | none | Rule Name. | | match_type | number | true | none | Match Type. 0&#x3D;All reports. | | action | string | true | none | Action to be taken (AUTO_REPLY, EMAIL_USER, EMAIL_FIXED, URL, SMS, POLL, GROUP_SMS, MOVE_CONTACT, CREATE_CONTACT, CREATE_CONTACT_PLUS_EMAIL, CREATE_CONTACT_PLUS_NAME_EMAIL CREATE_CONTACT_PLUS_NAME, SMPP, NONE). | | action_address | string | true | none | Action address. | | enabled | number | true | none | Enabled: Disabled&#x3D;0 or Enabled&#x3D;1. |  Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.  &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.EmailOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    EmailOtherApi apiInstance = new EmailOtherApi(defaultClient);
    String receiptRuleId = "receiptRuleId_example"; // String | 
    String contentType = "application/json"; // String | 
    CreateSmsDeliveryReceiptRuleRequest createSmsDeliveryReceiptRuleRequest = new CreateSmsDeliveryReceiptRuleRequest(); // CreateSmsDeliveryReceiptRuleRequest | 
    try {
      UpdateEmailDeliveryReceiptRule result = apiInstance.updateEmailDeliveryReceiptRule(receiptRuleId, contentType, createSmsDeliveryReceiptRuleRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling EmailOtherApi#updateEmailDeliveryReceiptRule");
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
| **receiptRuleId** | **String**|  | |
| **contentType** | **String**|  | [optional] |
| **createSmsDeliveryReceiptRuleRequest** | [**CreateSmsDeliveryReceiptRuleRequest**](CreateSmsDeliveryReceiptRuleRequest.md)|  | [optional] |

### Return type

[**UpdateEmailDeliveryReceiptRule**](UpdateEmailDeliveryReceiptRule.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="updateEmailTemplate"></a>
# **updateEmailTemplate**
> UpdateEmailTemplate updateEmailTemplate(templateId, contentType, updateEmailTemplateRequest)

Update Email Template

_Update email template_  Update email template  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | template_id | path | integer(int32) | true | Email template id |  ### Properties  | Name | Type | Required | Restrictions | Description | | --- | --- | --- | --- | --- | | template_name | string | false | none | The intended name for the template. | | body | string | true | none | Your template body. |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.EmailOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    EmailOtherApi apiInstance = new EmailOtherApi(defaultClient);
    String templateId = "templateId_example"; // String | 
    String contentType = "application/json"; // String | 
    UpdateEmailTemplateRequest updateEmailTemplateRequest = new UpdateEmailTemplateRequest(); // UpdateEmailTemplateRequest | 
    try {
      UpdateEmailTemplate result = apiInstance.updateEmailTemplate(templateId, contentType, updateEmailTemplateRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling EmailOtherApi#updateEmailTemplate");
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
| **templateId** | **String**|  | |
| **contentType** | **String**|  | [optional] |
| **updateEmailTemplateRequest** | [**UpdateEmailTemplateRequest**](UpdateEmailTemplateRequest.md)|  | [optional] |

### Return type

[**UpdateEmailTemplate**](UpdateEmailTemplate.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="verifyAllowedEmailAddress"></a>
# **verifyAllowedEmailAddress**
> VerifyAllowedEmailAddress verifyAllowedEmailAddress(emailAddressId, activationToken, contentType, verifyAllowedEmailAddressRequest)

Verify Allowed Email Address

_Verify email address using verification token_  Verify email address using verification token  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | email_address_id | path | integer(int32) | true | Allowed email address id | | activation_token | path | string | true | Your activation token. |  Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.  &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.EmailOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    EmailOtherApi apiInstance = new EmailOtherApi(defaultClient);
    String emailAddressId = "emailAddressId_example"; // String | 
    String activationToken = "activationToken_example"; // String | 
    String contentType = "application/json"; // String | 
    VerifyAllowedEmailAddressRequest verifyAllowedEmailAddressRequest = new VerifyAllowedEmailAddressRequest(); // VerifyAllowedEmailAddressRequest | 
    try {
      VerifyAllowedEmailAddress result = apiInstance.verifyAllowedEmailAddress(emailAddressId, activationToken, contentType, verifyAllowedEmailAddressRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling EmailOtherApi#verifyAllowedEmailAddress");
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
| **emailAddressId** | **String**|  | |
| **activationToken** | **String**|  | |
| **contentType** | **String**|  | [optional] |
| **verifyAllowedEmailAddressRequest** | [**VerifyAllowedEmailAddressRequest**](VerifyAllowedEmailAddressRequest.md)|  | [optional] |

### Return type

[**VerifyAllowedEmailAddress**](VerifyAllowedEmailAddress.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewAllEmailCampaigns"></a>
# **viewAllEmailCampaigns**
> ViewAllEmailCampaigns viewAllEmailCampaigns(contentType)

View All Email Campaigns

_Get all email campaigns_  Get all email campaigns  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | page | query | integer(int32) | false | Page number | | limit | query | integer(int32) | false | Number of records per page |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.EmailOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    EmailOtherApi apiInstance = new EmailOtherApi(defaultClient);
    String contentType = "application/json"; // String | 
    try {
      ViewAllEmailCampaigns result = apiInstance.viewAllEmailCampaigns(contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling EmailOtherApi#viewAllEmailCampaigns");
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

[**ViewAllEmailCampaigns**](ViewAllEmailCampaigns.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewAllowedEmailAddress"></a>
# **viewAllowedEmailAddress**
> ViewAllowedEmailAddress viewAllowedEmailAddress(emailAddressId, contentType)

View Allowed Email Address

_Get specific email address_  Get specific email address  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | email_address_id | path | integer(int32) | true | Allowed email address id |  Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.  &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.EmailOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    EmailOtherApi apiInstance = new EmailOtherApi(defaultClient);
    String emailAddressId = "emailAddressId_example"; // String | 
    String contentType = "application/json"; // String | 
    try {
      ViewAllowedEmailAddress result = apiInstance.viewAllowedEmailAddress(emailAddressId, contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling EmailOtherApi#viewAllowedEmailAddress");
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
| **emailAddressId** | **String**|  | |
| **contentType** | **String**|  | [optional] |

### Return type

[**ViewAllowedEmailAddress**](ViewAllowedEmailAddress.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewAllowedEmailAddresses"></a>
# **viewAllowedEmailAddresses**
> ViewAllowedEmailAddresses viewAllowedEmailAddresses(contentType)

View Allowed Email Addresses

_Get all email addresses_  Get all email addresses  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | page | query | integer(int32) | false | Page number | | limit | query | integer(int32) | false | Number of records per page |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.EmailOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    EmailOtherApi apiInstance = new EmailOtherApi(defaultClient);
    String contentType = "application/json"; // String | 
    try {
      ViewAllowedEmailAddresses result = apiInstance.viewAllowedEmailAddresses(contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling EmailOtherApi#viewAllowedEmailAddresses");
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

[**ViewAllowedEmailAddresses**](ViewAllowedEmailAddresses.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewEmailCampaign"></a>
# **viewEmailCampaign**
> ViewEmailCampaign viewEmailCampaign(emailCampaignId, contentType)

View Email Campaign

_Get specific email campaign_  Get specific email campaign  Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.  &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.EmailOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    EmailOtherApi apiInstance = new EmailOtherApi(defaultClient);
    String emailCampaignId = "emailCampaignId_example"; // String | 
    String contentType = "application/json"; // String | 
    try {
      ViewEmailCampaign result = apiInstance.viewEmailCampaign(emailCampaignId, contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling EmailOtherApi#viewEmailCampaign");
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
| **emailCampaignId** | **String**|  | |
| **contentType** | **String**|  | [optional] |

### Return type

[**ViewEmailCampaign**](ViewEmailCampaign.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewEmailCampaignHistory"></a>
# **viewEmailCampaignHistory**
> ViewEmailCampaignHistory viewEmailCampaignHistory(emailCampaignId, contentType)

View Email Campaign History

_Get specific email campaign history_  Get specific email campaign history   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.EmailOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    EmailOtherApi apiInstance = new EmailOtherApi(defaultClient);
    String emailCampaignId = "emailCampaignId_example"; // String | 
    String contentType = "application/json"; // String | 
    try {
      ViewEmailCampaignHistory result = apiInstance.viewEmailCampaignHistory(emailCampaignId, contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling EmailOtherApi#viewEmailCampaignHistory");
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
| **emailCampaignId** | **String**|  | |
| **contentType** | **String**|  | [optional] |

### Return type

[**ViewEmailCampaignHistory**](ViewEmailCampaignHistory.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewEmailDeliveryReceiptRule"></a>
# **viewEmailDeliveryReceiptRule**
> ViewEmailDeliveryReceiptRule viewEmailDeliveryReceiptRule(receiptRuleId, contentType)

View Email Delivery Receipt Rule

_Get specific email delivery receipt automation_  Get specific email delivery receipt automation  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | receipt_rule_id | path | integer(int32) | true | Receipt rule id |  Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.  &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.EmailOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    EmailOtherApi apiInstance = new EmailOtherApi(defaultClient);
    String receiptRuleId = "receiptRuleId_example"; // String | 
    String contentType = "application/json"; // String | 
    try {
      ViewEmailDeliveryReceiptRule result = apiInstance.viewEmailDeliveryReceiptRule(receiptRuleId, contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling EmailOtherApi#viewEmailDeliveryReceiptRule");
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
| **receiptRuleId** | **String**|  | |
| **contentType** | **String**|  | [optional] |

### Return type

[**ViewEmailDeliveryReceiptRule**](ViewEmailDeliveryReceiptRule.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewEmailDeliveryReceiptRules"></a>
# **viewEmailDeliveryReceiptRules**
> ViewEmailDeliveryReceiptRules viewEmailDeliveryReceiptRules(contentType)

View Email Delivery Receipt Rules

_Get all email delivery receipt automations_  Get all email delivery receipt automations  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | page | query | integer(int32) | false | Page number | | limit | query | integer(int32) | false | Number of records per page |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.EmailOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    EmailOtherApi apiInstance = new EmailOtherApi(defaultClient);
    String contentType = "application/json"; // String | 
    try {
      ViewEmailDeliveryReceiptRules result = apiInstance.viewEmailDeliveryReceiptRules(contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling EmailOtherApi#viewEmailDeliveryReceiptRules");
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

[**ViewEmailDeliveryReceiptRules**](ViewEmailDeliveryReceiptRules.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewEmailHistory"></a>
# **viewEmailHistory**
> ViewEmailHistory viewEmailHistory(contentType)

View Email History

_Get all transactional email history_  Get all transactional email history  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | date_from | query | integer(int32) | false | Start date (Unix Timestamp e.g. 1436849372) | | date_to | query | integer(int32) | false | End date (Unix Timestamp e.g. 1436879372) | | page | query | integer(int32) | false | [Page number](/#pagination) | | limit | query | integer(int32) | false | [Number of records per page](/#pagination) |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.EmailOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    EmailOtherApi apiInstance = new EmailOtherApi(defaultClient);
    String contentType = "application/json"; // String | 
    try {
      ViewEmailHistory result = apiInstance.viewEmailHistory(contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling EmailOtherApi#viewEmailHistory");
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

[**ViewEmailHistory**](ViewEmailHistory.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewEmailTemplate"></a>
# **viewEmailTemplate**
> ViewEmailTemplate viewEmailTemplate(templateId, contentType)

View Email Template

_Get specific user email template_  Get specific user email templates  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | template_id | path | integer(int32) | true | Email template id |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.EmailOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    EmailOtherApi apiInstance = new EmailOtherApi(defaultClient);
    String templateId = "templateId_example"; // String | 
    String contentType = "application/json"; // String | 
    try {
      ViewEmailTemplate result = apiInstance.viewEmailTemplate(templateId, contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling EmailOtherApi#viewEmailTemplate");
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
| **templateId** | **String**|  | |
| **contentType** | **String**|  | [optional] |

### Return type

[**ViewEmailTemplate**](ViewEmailTemplate.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewEmailTemplates"></a>
# **viewEmailTemplates**
> ViewEmailTemplates viewEmailTemplates(contentType)

View Email Templates

_Get all user email templates_  Get all user email templates  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | page | query | integer(int32) | false | Page number | | limit | query | integer(int32) | false | Number of records per page |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.EmailOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    EmailOtherApi apiInstance = new EmailOtherApi(defaultClient);
    String contentType = "application/json"; // String | 
    try {
      ViewEmailTemplates result = apiInstance.viewEmailTemplates(contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling EmailOtherApi#viewEmailTemplates");
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

[**ViewEmailTemplates**](ViewEmailTemplates.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewMasterEmailTemplate"></a>
# **viewMasterEmailTemplate**
> ViewMasterEmailTemplate viewMasterEmailTemplate(templateId, contentType)

View Master Email Template

_Get specific master email template_  Get specific master email template  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | template_id | path | integer(int32) | true | Email template id |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.EmailOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    EmailOtherApi apiInstance = new EmailOtherApi(defaultClient);
    String templateId = "templateId_example"; // String | 
    String contentType = "application/json"; // String | 
    try {
      ViewMasterEmailTemplate result = apiInstance.viewMasterEmailTemplate(templateId, contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling EmailOtherApi#viewMasterEmailTemplate");
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
| **templateId** | **String**|  | |
| **contentType** | **String**|  | [optional] |

### Return type

[**ViewMasterEmailTemplate**](ViewMasterEmailTemplate.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewMasterEmailTemplates"></a>
# **viewMasterEmailTemplates**
> ViewMasterEmailTemplates viewMasterEmailTemplates(contentType)

View Master Email Templates

_Get all master email templates._  Get all master email templates.  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | page | query | integer(int32) | false | Page number | | limit | query | integer(int32) | false | Number of records per page |  Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.  &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.EmailOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    EmailOtherApi apiInstance = new EmailOtherApi(defaultClient);
    String contentType = "application/json"; // String | 
    try {
      ViewMasterEmailTemplates result = apiInstance.viewMasterEmailTemplates(contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling EmailOtherApi#viewMasterEmailTemplates");
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

[**ViewMasterEmailTemplates**](ViewMasterEmailTemplates.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewTemplateCategories"></a>
# **viewTemplateCategories**
> ViewTemplateCategories viewTemplateCategories(contentType)

View Template Categories

_Get all master email template categories_  Get all master email template categories  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | page | query | integer(int32) | false | Page number | | limit | query | integer(int32) | false | Number of records per page |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.EmailOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    EmailOtherApi apiInstance = new EmailOtherApi(defaultClient);
    String contentType = "application/json"; // String | 
    try {
      ViewTemplateCategories result = apiInstance.viewTemplateCategories(contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling EmailOtherApi#viewTemplateCategories");
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

[**ViewTemplateCategories**](ViewTemplateCategories.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewTemplateCategory"></a>
# **viewTemplateCategory**
> ViewTemplateCategory viewTemplateCategory(categoryId, contentType)

View Template Category

_Get specific master email template category_  Get specific master email template category  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | category_id | path | integer(int32) | true | Email category id |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.EmailOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    EmailOtherApi apiInstance = new EmailOtherApi(defaultClient);
    String categoryId = "categoryId_example"; // String | 
    String contentType = "application/json"; // String | 
    try {
      ViewTemplateCategory result = apiInstance.viewTemplateCategory(categoryId, contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling EmailOtherApi#viewTemplateCategory");
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
| **categoryId** | **String**|  | |
| **contentType** | **String**|  | [optional] |

### Return type

[**ViewTemplateCategory**](ViewTemplateCategory.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewTemplatesInCategory"></a>
# **viewTemplatesInCategory**
> ViewTemplatesInCategory viewTemplatesInCategory(categoryId, contentType)

View Templates in Category

_Get all master email templates in a category_  Get all master email templates in a category  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | category_id | path | integer(int32) | true | Email category id | | page | query | integer(int32) | false | Page number | | limit | query | integer(int32) | false | Number of records per page |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.EmailOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    EmailOtherApi apiInstance = new EmailOtherApi(defaultClient);
    String categoryId = "categoryId_example"; // String | 
    String contentType = "application/json"; // String | 
    try {
      ViewTemplatesInCategory result = apiInstance.viewTemplatesInCategory(categoryId, contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling EmailOtherApi#viewTemplatesInCategory");
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
| **categoryId** | **String**|  | |
| **contentType** | **String**|  | [optional] |

### Return type

[**ViewTemplatesInCategory**](ViewTemplatesInCategory.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

