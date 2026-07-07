

# CreateDefaultSenderRequest


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**countryCode** | **String** | The country code of the recipient. Must be a valid ISO 3166-1 alpha-2 country code. |  |
|**productType** | [**ProductTypeEnum**](#ProductTypeEnum) | The type of product for the assignment. Support for additional types coming soon. |  |
|**defaultSenderStrategies** | [**List&lt;CreateDefaultSenderRequestDefaultSenderStrategiesInner&gt;**](CreateDefaultSenderRequestDefaultSenderStrategiesInner.md) | Array detailing sender strategies. Must contain exactly 1 element. Multiple strategies support coming soon. |  |



## Enum: ProductTypeEnum

| Name | Value |
|---- | -----|
| SMS | &quot;SMS&quot; |



