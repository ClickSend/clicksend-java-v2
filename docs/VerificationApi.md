# VerificationApi

All URIs are relative to *https://rest.clicksend.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**forgotPassword**](VerificationApi.md#forgotPassword) | **PUT** /v3/forgot-password | Forgot Password |
| [**forgotUsername**](VerificationApi.md#forgotUsername) | **PUT** /v3/forgot-username | Forgot Username |


<a id="forgotPassword"></a>
# **forgotPassword**
> ForgotPassword forgotPassword(contentType, forgotPasswordRequest)

Forgot Password

_Forgot password_  A user can send their username to this endpoint to be sent an email with their registered email address that will have a verification code.  Once you have this verification email containing the code you can send it to the [forgotten-password/verify](/#verify-forgot-password) endpoint along with a new password and the ID of that subaccount.  _Ask your administrator if you do not know your subaccount id._  ### Properties  | **Name** | **Type** | **Required** | **Restrictions** | **Description** | | --- | --- | --- | --- | --- | | username | string | true | none | Username belonging to account |  Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.  &lt;div style&#x3D;\&quot;background-color: #6BBD5B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint does not require authentication&lt;/span&gt;  &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.VerificationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    VerificationApi apiInstance = new VerificationApi(defaultClient);
    String contentType = "application/json"; // String | 
    ForgotPasswordRequest forgotPasswordRequest = new ForgotPasswordRequest(); // ForgotPasswordRequest | 
    try {
      ForgotPassword result = apiInstance.forgotPassword(contentType, forgotPasswordRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling VerificationApi#forgotPassword");
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
| **forgotPasswordRequest** | [**ForgotPasswordRequest**](ForgotPasswordRequest.md)|  | [optional] |

### Return type

[**ForgotPassword**](ForgotPassword.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="forgotUsername"></a>
# **forgotUsername**
> ForgotUsername forgotUsername(contentType, forgotUsernameRequest)

Forgot Username

_Forgot username_  Requires the user to pass either the email registered to an account or the phone number, **not** both  ### Properties  | **Name** | **Type** | **Required** | **Restrictions** | **Description** | | --- | --- | --- | --- | --- | | email | string | true | none | Email belonging to account | | phone_number | string | true | none | Phone belonging to account |  Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.  &lt;div style&#x3D;\&quot;background-color: #6BBD5B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint does not require authentication&lt;/span&gt;  &lt;/div&gt;   

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.VerificationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    VerificationApi apiInstance = new VerificationApi(defaultClient);
    String contentType = "application/json"; // String | 
    ForgotUsernameRequest forgotUsernameRequest = new ForgotUsernameRequest(); // ForgotUsernameRequest | 
    try {
      ForgotUsername result = apiInstance.forgotUsername(contentType, forgotUsernameRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling VerificationApi#forgotUsername");
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
| **forgotUsernameRequest** | [**ForgotUsernameRequest**](ForgotUsernameRequest.md)|  | [optional] |

### Return type

[**ForgotUsername**](ForgotUsername.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

