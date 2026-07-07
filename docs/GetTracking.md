

# GetTracking


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**total** | **BigDecimal** | Total number of short URLs associated with the long URL ID |  [optional] |
|**perPage** | **BigDecimal** | The limit of tracking data per page |  [optional] |
|**currentPageSize** | **BigDecimal** | The number of data in the current page |  [optional] |
|**prevPageUrl** | **String** | Link to the previous page. This attribute will not be present if there is no previous page. |  [optional] |
|**nextPageUrl** | **String** | Link to the next page. This attribute will not be present if there is no next page. |  [optional] |
|**data** | [**List&lt;GetTrackingDataInner&gt;**](GetTrackingDataInner.md) | Tracking data of the short URLs associated with the specified long URL ID. Note that only the data from the most recent click of the recipient (country, region, device, browser, and os) is recorded. |  [optional] |



