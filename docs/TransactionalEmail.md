

# TransactionalEmail


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**userId** | **Integer** | The ID of the user. |  [optional] |
|**subaccountId** | **Integer** | The ID of the subaccount. |  [optional] |
|**fromEmailAddressId** | **Integer** | The ID of the from email address. |  [optional] |
|**fromName** | **String** | The name of the sender. |  [optional] |
|**to** | [**List&lt;SendEmailRequestToInner&gt;**](SendEmailRequestToInner.md) |  |  [optional] |
|**cc** | [**List&lt;SendEmailRequestToInner&gt;**](SendEmailRequestToInner.md) |  |  [optional] |
|**bcc** | [**List&lt;SendEmailRequestToInner&gt;**](SendEmailRequestToInner.md) |  |  [optional] |
|**subject** | **String** | The subject of the email. |  [optional] |
|**body** | **String** | The HTML body of the email. |  [optional] |
|**bodyPlainText** | **String** | The plain text body of the email. |  [optional] |
|**schedule** | **Integer** | The timestamp indicating the scheduled time of the email. |  [optional] |
|**messageId** | **String** | The ID of the email message. |  [optional] |
|**status** | **String** | The status of the email. |  [optional] |
|**statusText** | **String** | The text description of the email status. |  [optional] |
|**softBounceCount** | **Integer** | The count of soft bounces. |  [optional] |
|**hardBounceCount** | **Integer** | The count of hard bounces. |  [optional] |
|**price** | **String** | The price of the email. |  [optional] |
|**dateAdded** | **Integer** | The timestamp indicating when the email was added. |  [optional] |
|**customString** | **String** | A custom string. |  [optional] |
|**attachments** | [**List&lt;Attachment&gt;**](Attachment.md) |  |  [optional] |
|**currency** | [**Currency**](Currency.md) |  |  [optional] |



