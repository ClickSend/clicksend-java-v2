

# AlphaTag


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**id** | **String** | The unique identifier for the record. |  [optional] |
|**accountId** | **String** | The unique identifier for the account. |  [optional] |
|**workspaceId** | **String** | The unique identifier for the workspace. |  [optional] |
|**userId** | **String** | The unique identifier for the user. |  [optional] |
|**alphaTag** | **String** | The alpha tag. |  [optional] |
|**status** | **String** | The status of the record. |  [optional] |
|**reason** | **String** | The reason for the status. |  [optional] |
|**countries** | **List&lt;String&gt;** | List of country codes where the alpha tag is requested. If not provided, it means a global alpha tag. |  [optional] |
|**createdTimestamp** | **String** | The timestamp when the record was created. Usually ISO 8601 (e.g. \&quot;2021-05-11T01:00:00.123Z\&quot;), but returned as a plain string rather than a strict date-time since some older records don&#39;t include a UTC offset (e.g. \&quot;2024-01-10T10:55:26.818097\&quot;). |  [optional] |
|**updatedTimestamp** | **String** | The timestamp when the record was last updated. Usually ISO 8601 (e.g. \&quot;2021-05-11T01:05:00.123Z\&quot;), but returned as a plain string rather than a strict date-time since some older records don&#39;t include a UTC offset. |  [optional] |



