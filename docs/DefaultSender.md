

# DefaultSender


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**id** | **String** | ID of the default sender. |  |
|**userId** | **Integer** | User ID from the version 3 system. |  |
|**subaccountId** | **Integer** | Subaccount ID from version 3. |  |
|**countryCode** | **String** | ISO 3166-1 alpha-2 formatted country code. |  |
|**productType** | [**ProductTypeEnum**](#ProductTypeEnum) | Type of product for which the setting is applied. |  |
|**defaultSenderStrategies** | [**List&lt;DefaultSenderDefaultSenderStrategiesInner&gt;**](DefaultSenderDefaultSenderStrategiesInner.md) | Default sender strategies. Must contain 1 or more objects. |  |
|**status** | [**StatusEnum**](#StatusEnum) | Overall status of the default sender. |  |
|**createdTimestamp** | **String** | Timestamp of when the default sender was created. Must be in ISO 8601 format. |  |
|**updatedTimestamp** | **String** | Timestamp of the last update to the default sender. Must be in ISO 8601 format. |  |



## Enum: ProductTypeEnum

| Name | Value |
|---- | -----|
| SMS | &quot;SMS&quot; |



## Enum: StatusEnum

| Name | Value |
|---- | -----|
| ENABLED | &quot;ENABLED&quot; |
| DISABLED | &quot;DISABLED&quot; |



