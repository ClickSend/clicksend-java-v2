

# ViewYourNumbersData


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**total** | **Integer** | The total number of items available for viewing. |  [optional] |
|**perPage** | **Integer** | The number of items returned per page. This is specified in the limit parameter. You can have 100 items at maximum, and 15 at minimum. |  [optional] |
|**currentPage** | **Integer** | The current page number. |  [optional] |
|**lastPage** | **Integer** | The last page number. |  [optional] |
|**nextPageUrl** | **String** | A URL of the next page. It will return **null** if there’s no next page. |  [optional] |
|**prevPageUrl** | **String** | A URL of the previous page. It will return **null** if there’s no previous page. |  [optional] |
|**from** | **Integer** | The number of the first result in the current page. |  [optional] |
|**to** | **Integer** | The number of the last result in the current page. |  [optional] |
|**data** | [**List&lt;ViewYourNumbersDataAllOfDataInner&gt;**](ViewYourNumbersDataAllOfDataInner.md) |  |  [optional] |
|**currency** | [**Currency**](Currency.md) |  |  [optional] |



