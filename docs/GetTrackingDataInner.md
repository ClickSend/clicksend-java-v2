

# GetTrackingDataInner


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**openCount** | **BigDecimal** | Number of times the short URL was opened |  [optional] |
|**dateOpened** | **BigDecimal** | Date in unix seconds when the short URL was first opened. Null if the short URL was never opened. |  [optional] |
|**userGeoCountry** | **String** | Country where the recipient is located when the short URL was opened. Null if the short URL was never opened. |  [optional] |
|**userGeoRegion** | **String** | Geographical region where the recipient is located when the short URL was opened. Null if the short URL was never opened. |  [optional] |
|**userDevice** | **String** | Deviced used by the recipient to open the short URL. Null if the short URL was never opened. |  [optional] |
|**userBrowser** | **String** | Browser used by the recipient to open the short URL. Null if the short URL was never opened. |  [optional] |
|**userOs** | **String** | Opearating system used by the recipient to open the short URL. Null if the short URL was never opened. |  [optional] |
|**contact** | [**GetTrackingDataInnerContact**](GetTrackingDataInnerContact.md) |  |  [optional] |



