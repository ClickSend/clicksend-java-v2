

# MarkSpecificInboundSmsMessageAsRead


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**httpCode** | **Integer** | The HTTP code of the response. Visit [this page](/#status-codes) for more information. |  [optional] |
|**responseCode** | **String** | The response code of the operation. Visit [this page](/#status-codes) for more information. |  [optional] |
|**responseMsg** | **String** | A message describing the outcome of the operation. |  [optional] |
|**data** | **Integer** | The number of SMS marked as read.  If you have multiple inbound rules set to POLL, you will receive the inbound message multiple times. Reading it will mark all those messages as read. |  [optional] |



