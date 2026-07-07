

# InboundSms

The parameters related to the message receipt.

## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**timestamp** | **Integer** | The time you receive the inbound message.. It’s in the &lt;a href&#x3D;\&quot;http://help.clicksend.com/what-is-a-unix-timestamp\&quot;&gt;Unix format.&lt;/a&gt; |  [optional] |
|**from** | **String** | The sender of the message, which is the phone number of the recipient who replied to you. Your recipient can’t reply to an alpha tag (business name). |  [optional] |
|**body** | **String** | The message you received from your recipient. |  [optional] |
|**originalBody** | **String** | The last message you sent to your recipient. |  [optional] |
|**originalMessageId** | **String** | The generated ID of the message that you sent to your receipient. |  [optional] |
|**to** | **String** | The receiver of the inbound message, which can be either the shared number or the dedicated number you used to send the message. |  [optional] |
|**customString** | **String** | A note that was included with the inbound SMS. If no note was included, the value will be an empty string. |  [optional] |
|**messageId** | **String** | The generated ID of the inbound SMS. This ID is typically used as a reference for &lt;a href&#x3D;\&quot;https://www.clicksend.com/au/help/\&quot; target&#x3D;\&quot;_blank\&quot;&gt;customer support&lt;/a&gt; in case of any issues. |  [optional] |
|**keyword** | **String** | The keyword of the inbound SMS.  &lt;div class&#x3D;\&quot;warning-box\&quot;&gt;   &lt;h4&gt;&lt;i class&#x3D;\&quot;fas fa-exclamation-triangle\&quot;&gt;&lt;/i&gt; Warning:&lt;/h4&gt;   &lt;p&gt;This parameter is deprecated and will return the first word of the body message.&lt;/p&gt; &lt;/div&gt; |  [optional] |



