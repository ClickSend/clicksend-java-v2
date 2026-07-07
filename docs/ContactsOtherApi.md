# ContactsOtherApi

All URIs are relative to *https://rest.clicksend.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**deleteContact**](ContactsOtherApi.md#deleteContact) | **DELETE** /v3/lists/{list_id}/contacts/{contact_id} | Delete Contact |
| [**getSpecificContact**](ContactsOtherApi.md#getSpecificContact) | **GET** /v3/lists/{list_id}/contacts/{contact_id} | Get Specific Contact |
| [**updateContact**](ContactsOtherApi.md#updateContact) | **PUT** /v3/lists/{list_id}/contacts/{contact_id} | Update Contact |


<a id="deleteContact"></a>
# **deleteContact**
> DeleteContact deleteContact(listId, contactId, contentType)

Delete Contact

_Delete a contact_  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | list_id | path | integer(int32) | true | List ID | | contact_id | path | integer(int32) | true | Contact ID |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.ContactsOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    ContactsOtherApi apiInstance = new ContactsOtherApi(defaultClient);
    String listId = "listId_example"; // String | 
    String contactId = "contactId_example"; // String | 
    String contentType = "application/json"; // String | 
    try {
      DeleteContact result = apiInstance.deleteContact(listId, contactId, contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ContactsOtherApi#deleteContact");
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
| **listId** | **String**|  | |
| **contactId** | **String**|  | |
| **contentType** | **String**|  | [optional] |

### Return type

[**DeleteContact**](DeleteContact.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="getSpecificContact"></a>
# **getSpecificContact**
> GetSpecificContact getSpecificContact(listId, contactId, contentType)

Get Specific Contact

_Get a specific contact_  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | list_id | path | integer(int32) | true | Your contact list id you want to access. | | contact_id | path | integer(int32) | true | Your contact id you want to access. |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.ContactsOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    ContactsOtherApi apiInstance = new ContactsOtherApi(defaultClient);
    String listId = "listId_example"; // String | 
    String contactId = "contactId_example"; // String | 
    String contentType = "application/json"; // String | 
    try {
      GetSpecificContact result = apiInstance.getSpecificContact(listId, contactId, contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ContactsOtherApi#getSpecificContact");
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
| **listId** | **String**|  | |
| **contactId** | **String**|  | |
| **contentType** | **String**|  | [optional] |

### Return type

[**GetSpecificContact**](GetSpecificContact.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="updateContact"></a>
# **updateContact**
> UpdateContact updateContact(listId, contactId, contentType, createNewContactRequest)

Update Contact

_Update specific contact_  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | list_id | path | integer(int32) | true | Contact list id | | contact_id | path | integer(int32) | true | Contact ID |  ### Properties  | Name | Type | Required | Restrictions | Description | | --- | --- | --- | --- | --- | | phone_number | string | true | none | Your phone number in [E.164](https://en.wikipedia.org/wiki/E.164) format. Must be provided if no fax number or email. | | email | string | false | none | Your email. Must be provided if no phone number or fax number. | | fax_number | string | false | none | Your fax number. Must be provided if no phone number or email. | | first_name | string | false | none | Your first name. | | address_line_1 | string | false | none | Your street address | | address_line_2 | string | false | none | none | | address_city | string | false | none | Your nearest city | | address_state | string | false | none | Your current state | | address_postal_code | string | false | none | Your current postcode | | address_country | string | false | none | Your current country | | organization_name | string | false | none | Your organisation name | | custom_1 | string | true | none | none | | custom_2 | string | false | none | none | | custom_3 | string | false | none | none | | custom_4 | string | false | none | none | | last_name | string | false | none | Your last name |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.ContactsOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    ContactsOtherApi apiInstance = new ContactsOtherApi(defaultClient);
    String listId = "listId_example"; // String | 
    String contactId = "contactId_example"; // String | 
    String contentType = "application/json"; // String | 
    CreateNewContactRequest createNewContactRequest = new CreateNewContactRequest(); // CreateNewContactRequest | 
    try {
      UpdateContact result = apiInstance.updateContact(listId, contactId, contentType, createNewContactRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ContactsOtherApi#updateContact");
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
| **listId** | **String**|  | |
| **contactId** | **String**|  | |
| **contentType** | **String**|  | [optional] |
| **createNewContactRequest** | [**CreateNewContactRequest**](CreateNewContactRequest.md)|  | [optional] |

### Return type

[**UpdateContact**](UpdateContact.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

