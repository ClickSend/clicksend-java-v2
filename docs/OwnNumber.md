

# OwnNumber


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**id** | **UUID** | The unique identifier for the record. |  [optional] |
|**accountId** | **UUID** | The unique identifier for the account. |  [optional] |
|**workspaceId** | **UUID** | The unique identifier for the workspace. |  [optional] |
|**userId** | **UUID** | The unique identifier for the user. |  [optional] |
|**phoneNumber** | **String** | The user&#39;s phone number. |  [optional] |
|**country** | **String** | The country code of the phone number. |  [optional] |
|**label** | **String** | A label for the phone number. |  [optional] |
|**status** | **String** | The status of the phone number. |  [optional] |
|**verifiedTimestamp** | **OffsetDateTime** | The timestamp when the phone number was verified. |  [optional] |
|**isNearingExpiration** | **Boolean** | Indicates whether the phone number verification is nearing its expiration date: - **true:** The verification was completed more than 11 months ago and will expire soon. You should re-verify your phone number to maintain uninterrupted service. - **false:** The verification is still valid and not approaching expiration. |  [optional] |
|**createdTimestamp** | **OffsetDateTime** | The timestamp when the record was created. |  [optional] |
|**updatedTimestamp** | **OffsetDateTime** | The timestamp when the record was last updated. |  [optional] |



