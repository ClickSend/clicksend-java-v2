

# RequestAlphaTagRequestBusinessesInner


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**country** | [**CountryEnum**](#CountryEnum) |  |  |
|**businessName** | **String** |  |  |
|**businessRelationship** | [**BusinessRelationshipEnum**](#BusinessRelationshipEnum) | Indicates your relationship to the business being registered.  - **PRIMARY**: Your primary business (linked to your ClickSend account). - **ENTITY_ASSOCIATE**: Sending on behalf of another business you represent or own.  |  |
|**businessInfo** | [**RequestAlphaTagRequestBusinessesInnerBusinessInfo**](RequestAlphaTagRequestBusinessesInnerBusinessInfo.md) |  |  |
|**businessAddress** | [**RequestAlphaTagRequestBusinessesInnerBusinessAddress**](RequestAlphaTagRequestBusinessesInnerBusinessAddress.md) |  |  |
|**representative** | [**RequestAlphaTagRequestBusinessesInnerRepresentative**](RequestAlphaTagRequestBusinessesInnerRepresentative.md) |  |  |
|**abn** | **String** | Australian Business Number (ABN), 11 digits |  |
|**partnerBusinessName** | **String** | Partner&#39;s business name. **Required** when &#x60;business_relationship&#x60; is &#x60;ENTITY_ASSOCIATE&#x60;. **Forbidden** otherwise.  |  [optional] |
|**partnerAbn** | **String** | Partner&#39;s Australian Business Number (ABN). Must contain only digits. **Required** when &#x60;business_relationship&#x60; is &#x60;ENTITY_ASSOCIATE&#x60;. **Forbidden** otherwise.  |  [optional] |
|**partnerBusinessInfo** | [**RequestAlphaTagRequestBusinessesInnerBusinessInfo**](RequestAlphaTagRequestBusinessesInnerBusinessInfo.md) |  |  [optional] |
|**partnerBusinessAddress** | [**RequestAlphaTagRequestBusinessesInnerBusinessAddress**](RequestAlphaTagRequestBusinessesInnerBusinessAddress.md) |  |  [optional] |
|**partnerRepresentative** | [**RequestAlphaTagRequestBusinessesInnerPartnerRepresentative**](RequestAlphaTagRequestBusinessesInnerPartnerRepresentative.md) |  |  [optional] |



## Enum: CountryEnum

| Name | Value |
|---- | -----|
| AU | &quot;AU&quot; |



## Enum: BusinessRelationshipEnum

| Name | Value |
|---- | -----|
| PRIMARY | &quot;PRIMARY&quot; |
| ENTITY_ASSOCIATE | &quot;ENTITY_ASSOCIATE&quot; |



