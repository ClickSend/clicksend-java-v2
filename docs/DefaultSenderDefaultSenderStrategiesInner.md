

# DefaultSenderDefaultSenderStrategiesInner


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**senderType** | [**SenderTypeEnum**](#SenderTypeEnum) | Type of the sender. |  |
|**senderId** | **String** | Identifier for the sender. Must be between 3-20 characters. |  |
|**senderCountryCode** | **String** | ISO 3166-1 alpha-2 formatted country code. |  [optional] |
|**priority** | **Integer** | Priority level of the sender in the strategy. Must be a positive integer. |  |
|**status** | [**StatusEnum**](#StatusEnum) | Status of the sender in the strategy. |  |
|**note** | **String** | Note providing additional context about the sender. Maximum length of 200 characters. Optional. |  [optional] |



## Enum: SenderTypeEnum

| Name | Value |
|---- | -----|
| ALPHA_TAG | &quot;alpha_tag&quot; |
| _10_DLC | &quot;10DLC&quot; |
| TOLLFREE | &quot;tollfree&quot; |
| OWN_NUMBER | &quot;own_number&quot; |
| SHORTCODE | &quot;shortcode&quot; |
| LONGCODE | &quot;longcode&quot; |
| SHARED_LONGCODE | &quot;shared_longcode&quot; |



## Enum: StatusEnum

| Name | Value |
|---- | -----|
| ENABLED | &quot;ENABLED&quot; |
| DISABLED | &quot;DISABLED&quot; |



