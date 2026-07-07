

# VoiceReceipt


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**timestampSend** | **String** | Timestamp of the original send request in UNIX format. e.g 1439173980 |  [optional] |
|**timestamp** | **String** | Timestamp of delivery report in UNIX format. e.g 1439173981 |  [optional] |
|**messageId** | **String** | Message ID, returned when originally sending the message. |  [optional] |
|**statusCode** | **String** | Status code. Refer to &#39;Voice Delivery Status Codes&#39; in docs. |  [optional] |
|**statusText** | **String** | Status text. |  [optional] |
|**errorCode** | **String** | Error code. |  [optional] |
|**errorText** | **String** | Error text. |  [optional] |
|**customString** | **String** | A custom string used when sending the original message. |  [optional] |
|**messageType** | **String** | voice (constant). |  [optional] |
|**digits** | **String** | Numbers the recipient pressed on their keypad during the call. A blank string will be used if they didn&#39;t provide any input. |  [optional] |



