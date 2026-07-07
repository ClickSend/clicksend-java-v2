

# CalculateSmsPriceData

The parameters related to the messages price.

## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**totalPrice** | **BigDecimal** | The total price of sending the messages. Visit [this page](/#status-codes) for more information. |  [optional] |
|**totalCount** | **Integer** | The total number of messages sent from the request. |  [optional] |
|**queuedCount** | **Integer** | The messages will be put in a queue if it goes through the validation process. The validation process checks whether the **Sender ID** is registered or not. Some countries don&#39;t require messages to go through the validation process.  Messages scheduled to be sent right away will be sent immediately. If not, it will be queued. |  [optional] |
|**messages** | [**List&lt;Sms&gt;**](Sms.md) | The parameters related to messages. |  [optional] |
|**currency** | [**Currency**](Currency.md) |  |  [optional] |
|**summary** | [**CalculateSmsPriceDataSummary**](CalculateSmsPriceDataSummary.md) |  |  [optional] |
|**blockedCount** | **Integer** | The number of messages unable to be sent. This is often caused by:  - Receipient’s country not enabled for global sending.      - Sender ID resitriction.      - Number registration restrcition. |  [optional] |



