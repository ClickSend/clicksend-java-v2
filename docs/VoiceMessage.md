

# VoiceMessage


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**date** | **String** | The date, if applicable. May be null; see also &#x60;date_added&#x60;. |  [optional] |
|**dateAdded** | **Integer** | The Unix timestamp when the message was added. |  [optional] |
|**listId** | **String** | The ID of the list associated with the message, if applicable. |  [optional] |
|**to** | **String** | The recipient&#39;s phone number. |  [optional] |
|**toType** | **String** | The type of recipient. |  [optional] |
|**body** | **String** | The body of the message. |  [optional] |
|**from** | **String** | The sender&#39;s phone number. |  [optional] |
|**lang** | **String** | The language of the message. |  [optional] |
|**voice** | **String** | The voice of the message. |  [optional] |
|**schedule** | **String** | The timestamp when the message should be sent. Returned as a string since it may be an empty string when no schedule was set. |  [optional] |
|**messageId** | **String** | The ID of the message. |  [optional] |
|**messageParts** | **String** | The number of parts in the message. |  [optional] |
|**messagePrice** | **String** | The price of the message. |  [optional] |
|**customString** | **String** | The custom string of the message. |  [optional] |
|**userId** | **BigDecimal** | The ID of the user. |  [optional] |
|**subaccountId** | **BigDecimal** | The ID of the subaccount. |  [optional] |
|**country** | **String** | The country code of the message. |  [optional] |
|**requireInput** | **BigDecimal** | The require input of the message. |  [optional] |
|**machineDetection** | **BigDecimal** | The machine detection of the message. |  [optional] |
|**machineDetected** | **BigDecimal** | Flag indicating if an answering machine was detected. |  [optional] |
|**digits** | **String** | The digits entered by the recipient, if any input was collected. |  [optional] |
|**carrier** | **String** | The carrier of the recipient&#39;s phone number. |  [optional] |
|**statusCode** | **String** | The status code of the message. |  [optional] |
|**statusText** | **String** | A human-readable description of the status. |  [optional] |
|**status** | **String** | The status of the message. |  [optional] |
|**apiUsername** | **String** | The API username associated with the message. |  [optional] |



