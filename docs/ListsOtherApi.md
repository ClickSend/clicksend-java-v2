# ListsOtherApi

All URIs are relative to *https://rest.clicksend.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**copyContactToList**](ListsOtherApi.md#copyContactToList) | **PUT** /v3/lists/{from_list_id}/contacts/{contact_id}/copy/{to_list_id} | Copy Contact to List |
| [**createList**](ListsOtherApi.md#createList) | **POST** /v3/lists | Create List |
| [**createNewContact**](ListsOtherApi.md#createNewContact) | **POST** /v3/lists/{list_id}/contacts | Create New Contact |
| [**deleteList**](ListsOtherApi.md#deleteList) | **DELETE** /v3/lists/{list_id} | Delete List |
| [**importContacts**](ListsOtherApi.md#importContacts) | **POST** /v3/lists/{list_id}/import | Import Contacts |
| [**removeDuplicateContacts**](ListsOtherApi.md#removeDuplicateContacts) | **PUT** /v3/lists/{list_id}/remove-duplicates/ | Remove Duplicate Contacts |
| [**removeOptedOutContacts**](ListsOtherApi.md#removeOptedOutContacts) | **PUT** /v3/lists/{list_id}/remove-opted-out-contacts/{opt_out_list_id} | Remove Opted Out Contacts |
| [**transferContactToList**](ListsOtherApi.md#transferContactToList) | **PUT** /v3/lists/{from_list_id}/contacts/{contact_id}/transfer/{to_list_id} | Transfer Contact to List |
| [**updateList**](ListsOtherApi.md#updateList) | **PUT** /v3/lists/{list_id} | Update List |
| [**viewContactLists**](ListsOtherApi.md#viewContactLists) | **GET** /v3/search/contacts-lists | View Contact Lists |
| [**viewListContacts**](ListsOtherApi.md#viewListContacts) | **GET** /v3/lists/{list_id}/contacts | View List Contacts |
| [**viewLists**](ListsOtherApi.md#viewLists) | **GET** /v3/lists | View Lists |
| [**viewSpecificList**](ListsOtherApi.md#viewSpecificList) | **GET** /v3/lists/{list_id} | View Specific List |


<a id="copyContactToList"></a>
# **copyContactToList**
> CopyContactToList copyContactToList(fromListId, contactId, toListId, contentType, body)

Copy Contact to List

_Copy contact to another list_  Copy contact to another list  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | from_list_id | path | integer(int32) | true | List ID for list that contains contact. | | contact_id | path | integer(int32) | true | Contact ID | | to_list_id | path | integer(int32) | true | List ID for list you want to copy contact to. |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.ListsOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    ListsOtherApi apiInstance = new ListsOtherApi(defaultClient);
    String fromListId = "fromListId_example"; // String | 
    String contactId = "contactId_example"; // String | 
    String toListId = "toListId_example"; // String | 
    String contentType = "application/json"; // String | 
    Object body = null; // Object | 
    try {
      CopyContactToList result = apiInstance.copyContactToList(fromListId, contactId, toListId, contentType, body);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ListsOtherApi#copyContactToList");
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
| **fromListId** | **String**|  | |
| **contactId** | **String**|  | |
| **toListId** | **String**|  | |
| **contentType** | **String**|  | [optional] |
| **body** | **Object**|  | [optional] |

### Return type

[**CopyContactToList**](CopyContactToList.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="createList"></a>
# **createList**
> CreateList createList(contentType, createListRequest)

Create List

_Create new contact list_  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | list_name | body | string | true | Your contact list name |  Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.  &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.ListsOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    ListsOtherApi apiInstance = new ListsOtherApi(defaultClient);
    String contentType = "application/json"; // String | 
    CreateListRequest createListRequest = new CreateListRequest(); // CreateListRequest | 
    try {
      CreateList result = apiInstance.createList(contentType, createListRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ListsOtherApi#createList");
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
| **createListRequest** | [**CreateListRequest**](CreateListRequest.md)|  | [optional] |

### Return type

[**CreateList**](CreateList.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="createNewContact"></a>
# **createNewContact**
> CreateNewContact createNewContact(listId, contentType, createNewContactRequest)

Create New Contact

_Create new contact_  ### parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | list_id | path | integer(int32) | true | List id | | page | query | integer(int32) | false | [Page number](/#pagination) | | limit | query | integer(int32) | false | [Number of records per page](/#pagination) |   ### Properties  | Name | Type | Required | Restrictions | Description | | --- | --- | --- | --- | --- | | phone_number | string | true | none | Your phone number in\\_[E.164](https://en.wikipedia.org/wiki/E.164)\\_format. Must be provided if no fax number or email. | | email | string | false | none | Your email. Must be provided if no phone number or fax number. | | fax_number | string | false | none | Your fax number. Must be provided if no phone number or email. | | first_name | string | false | none | Your first name. | | address_line_1 | string | false | none | Your street address | | address_line_2 | string | false | none | none | | address_city | string | false | none | Your nearest city | | address_state | string | false | none | Your current state | | address_postal_code | string | false | none | Your current postcode | | address_country | string | false | none | Your current country | | organization_name | string | false | none | Your organisation name | | custom_1 | string | true | none | none | | custom_2 | string | false | none | none | | custom_3 | string | false | none | none | | custom_4 | string | false | none | none | | last_name | string | false | none | Your last name |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.ListsOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    ListsOtherApi apiInstance = new ListsOtherApi(defaultClient);
    String listId = "listId_example"; // String | 
    String contentType = "application/json"; // String | 
    CreateNewContactRequest createNewContactRequest = new CreateNewContactRequest(); // CreateNewContactRequest | 
    try {
      CreateNewContact result = apiInstance.createNewContact(listId, contentType, createNewContactRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ListsOtherApi#createNewContact");
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
| **contentType** | **String**|  | [optional] |
| **createNewContactRequest** | [**CreateNewContactRequest**](CreateNewContactRequest.md)|  | [optional] |

### Return type

[**CreateNewContact**](CreateNewContact.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="deleteList"></a>
# **deleteList**
> DeleteList deleteList(listId, contentType)

Delete List

_ListsByListIdDelete_  Delete a specific contact list  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | list_id | path | integer(int32) | true | List ID |  Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.  &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.ListsOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    ListsOtherApi apiInstance = new ListsOtherApi(defaultClient);
    String listId = "listId_example"; // String | 
    String contentType = "application/json"; // String | 
    try {
      DeleteList result = apiInstance.deleteList(listId, contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ListsOtherApi#deleteList");
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
| **contentType** | **String**|  | [optional] |

### Return type

[**DeleteList**](DeleteList.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="importContacts"></a>
# **importContacts**
> ImportContacts importContacts(listId, contentType, importContactsRequest)

Import Contacts

_Import contacts to list_  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | list_id | path | integer(int32) | true | Your contact list id you want to access. |  ### Properties  | Name | Type | Required | Restrictions | Description | | --- | --- | --- | --- | --- | | file_url | string | true | none | URL of file to process | | field_order | \\[string\\] | true | none | Order of fields in file |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.ListsOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    ListsOtherApi apiInstance = new ListsOtherApi(defaultClient);
    String listId = "listId_example"; // String | 
    String contentType = "application/json"; // String | 
    ImportContactsRequest importContactsRequest = new ImportContactsRequest(); // ImportContactsRequest | 
    try {
      ImportContacts result = apiInstance.importContacts(listId, contentType, importContactsRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ListsOtherApi#importContacts");
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
| **contentType** | **String**|  | [optional] |
| **importContactsRequest** | [**ImportContactsRequest**](ImportContactsRequest.md)|  | [optional] |

### Return type

[**ImportContacts**](ImportContacts.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="removeDuplicateContacts"></a>
# **removeDuplicateContacts**
> RemoveDuplicateContacts removeDuplicateContacts(listId, contentType, removeDuplicateContactsRequest)

Remove Duplicate Contacts

_Remove duplicate contacts_  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | list_id | path | integer(int32) | true | Your list id |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.ListsOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    ListsOtherApi apiInstance = new ListsOtherApi(defaultClient);
    String listId = "listId_example"; // String | 
    String contentType = "application/json"; // String | 
    RemoveDuplicateContactsRequest removeDuplicateContactsRequest = new RemoveDuplicateContactsRequest(); // RemoveDuplicateContactsRequest | 
    try {
      RemoveDuplicateContacts result = apiInstance.removeDuplicateContacts(listId, contentType, removeDuplicateContactsRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ListsOtherApi#removeDuplicateContacts");
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
| **contentType** | **String**|  | [optional] |
| **removeDuplicateContactsRequest** | [**RemoveDuplicateContactsRequest**](RemoveDuplicateContactsRequest.md)|  | [optional] |

### Return type

[**RemoveDuplicateContacts**](RemoveDuplicateContacts.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="removeOptedOutContacts"></a>
# **removeOptedOutContacts**
> RemoveOptedOutContacts removeOptedOutContacts(listId, optOutListId, contentType, body)

Remove Opted Out Contacts

_Remove all opted out contacts_  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | list_id | path | integer(int32) | true | Your list id | | opt_out_list_id | path | integer(int32) | true | Your opt out list id |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.ListsOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    ListsOtherApi apiInstance = new ListsOtherApi(defaultClient);
    String listId = "listId_example"; // String | 
    String optOutListId = "optOutListId_example"; // String | 
    String contentType = "application/json"; // String | 
    Object body = null; // Object | 
    try {
      RemoveOptedOutContacts result = apiInstance.removeOptedOutContacts(listId, optOutListId, contentType, body);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ListsOtherApi#removeOptedOutContacts");
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
| **optOutListId** | **String**|  | |
| **contentType** | **String**|  | [optional] |
| **body** | **Object**|  | [optional] |

### Return type

[**RemoveOptedOutContacts**](RemoveOptedOutContacts.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="transferContactToList"></a>
# **transferContactToList**
> TransferContactToList transferContactToList(fromListId, contactId, toListId, contentType, body)

Transfer Contact to List

_Transfer contact to another list_  Transfer contact to another list  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | from_list_id | path | integer(int32) | true | List ID for list that contains contact. | | contact_id | path | integer(int32) | true | Contact ID | | to_list_id | path | integer(int32) | true | List ID for list you want to transfer contact to. |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.ListsOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    ListsOtherApi apiInstance = new ListsOtherApi(defaultClient);
    String fromListId = "fromListId_example"; // String | 
    String contactId = "contactId_example"; // String | 
    String toListId = "toListId_example"; // String | 
    String contentType = "application/json"; // String | 
    Object body = null; // Object | 
    try {
      TransferContactToList result = apiInstance.transferContactToList(fromListId, contactId, toListId, contentType, body);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ListsOtherApi#transferContactToList");
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
| **fromListId** | **String**|  | |
| **contactId** | **String**|  | |
| **toListId** | **String**|  | |
| **contentType** | **String**|  | [optional] |
| **body** | **Object**|  | [optional] |

### Return type

[**TransferContactToList**](TransferContactToList.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="updateList"></a>
# **updateList**
> UpdateList updateList(listId, contentType, createListRequest)

Update List

_Update specific contact list_  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | list_id | path | integer(int32) | true | Your list id | | list_name | body | string | true | Your new list name |  Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.  &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.ListsOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    ListsOtherApi apiInstance = new ListsOtherApi(defaultClient);
    String listId = "listId_example"; // String | 
    String contentType = "application/json"; // String | 
    CreateListRequest createListRequest = new CreateListRequest(); // CreateListRequest | 
    try {
      UpdateList result = apiInstance.updateList(listId, contentType, createListRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ListsOtherApi#updateList");
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
| **contentType** | **String**|  | [optional] |
| **createListRequest** | [**CreateListRequest**](CreateListRequest.md)|  | [optional] |

### Return type

[**UpdateList**](UpdateList.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewContactLists"></a>
# **viewContactLists**
> viewContactLists(q)

View Contact Lists

_Get list of searched contact list_  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | q | query | string | true | Your keyword or query. | | page | query | integer(int32) | false | [Page number](/#pagination) | | limit | query | integer(int32) | false | [Number of records per page](/#pagination) |  Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.  This endpoint requires authentication, [more info...](/#authentication)

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.ListsOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    ListsOtherApi apiInstance = new ListsOtherApi(defaultClient);
    String q = "Test"; // String | 
    try {
      apiInstance.viewContactLists(q);
    } catch (ApiException e) {
      System.err.println("Exception when calling ListsOtherApi#viewContactLists");
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
| **q** | **String**|  | [optional] |

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

<a id="viewListContacts"></a>
# **viewListContacts**
> ViewListContacts viewListContacts(listId, contentType)

View List Contacts

_Get all contacts in a list_  ### parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | list_id | path | integer(int32) | true | Contact list ID | | page | query | integer(int32) | false | [Page number](/#pagination) | | limit | query | integer(int32) | false | [Number of records per page](/#pagination) | | updated_after | query | integer(int32) | false | Get all contacts updated after a given timestamp. |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.ListsOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    ListsOtherApi apiInstance = new ListsOtherApi(defaultClient);
    String listId = "listId_example"; // String | 
    String contentType = "application/json"; // String | 
    try {
      ViewListContacts result = apiInstance.viewListContacts(listId, contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ListsOtherApi#viewListContacts");
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
| **contentType** | **String**|  | [optional] |

### Return type

[**ViewListContacts**](ViewListContacts.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewLists"></a>
# **viewLists**
> ViewLists viewLists(contentType)

View Lists

_Get all contact lists_  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | page | query | integer(int32) | false | [Page number](/#pagination) | | limit | query | integer(int32) | false | [Number of records per page](/#pagination) |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.ListsOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    ListsOtherApi apiInstance = new ListsOtherApi(defaultClient);
    String contentType = "application/json"; // String | 
    try {
      ViewLists result = apiInstance.viewLists(contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ListsOtherApi#viewLists");
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

[**ViewLists**](ViewLists.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewSpecificList"></a>
# **viewSpecificList**
> ViewSpecificList viewSpecificList(listId, contentType)

View Specific List

_Get specific contact list_  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | list_id | path | integer(int32) | true | List ID |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.ListsOtherApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    ListsOtherApi apiInstance = new ListsOtherApi(defaultClient);
    String listId = "listId_example"; // String | 
    String contentType = "application/json"; // String | 
    try {
      ViewSpecificList result = apiInstance.viewSpecificList(listId, contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ListsOtherApi#viewSpecificList");
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
| **contentType** | **String**|  | [optional] |

### Return type

[**ViewSpecificList**](ViewSpecificList.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

