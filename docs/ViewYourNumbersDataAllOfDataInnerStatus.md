

# ViewYourNumbersDataAllOfDataInnerStatus

The registration status of the number.

## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**value** | [**ValueEnum**](#ValueEnum) | Numeric status code (0-5): - 0: Your number is ready to go. - 1: Your number is unregistered. You will not be able to send messages to certain countries. - 2: Your number registration is in progress. Email updates will follow. - 3: Action required on your number registration. Please resolve to start using it. - 4: You can send to all countries but may get restricted to some before full registration. - 5: Your number is registered and you can start using it immediately.  |  [optional] |
|**label** | [**LabelEnum**](#LabelEnum) | Status label identifier corresponding to the numeric value above, following the same order. |  [optional] |
|**description** | **String** | Human readable description of the status. |  [optional] |
|**name** | [**NameEnum**](#NameEnum) | Display name for the status corresponding to the numeric value above, following the same order. |  [optional] |



## Enum: ValueEnum

| Name | Value |
|---- | -----|
| NUMBER_0 | 0 |
| NUMBER_1 | 1 |
| NUMBER_2 | 2 |
| NUMBER_3 | 3 |
| NUMBER_4 | 4 |
| NUMBER_5 | 5 |



## Enum: LabelEnum

| Name | Value |
|---- | -----|
| REGISTRATION_NOT_REQUIRED | &quot;REGISTRATION_NOT_REQUIRED&quot; |
| REGISTRATION_NOT_INITIATED | &quot;REGISTRATION_NOT_INITIATED&quot; |
| REGISTRATION_INITIATED | &quot;REGISTRATION_INITIATED&quot; |
| CUST_ACTION_REQUIRED | &quot;CUST_ACTION_REQUIRED&quot; |
| REGISTRATION_SUBMITTED | &quot;REGISTRATION_SUBMITTED&quot; |
| REGISTERED | &quot;REGISTERED&quot; |



## Enum: NameEnum

| Name | Value |
|---- | -----|
| READY_TO_USE | &quot;Ready to use&quot; |
| UNREGISTERED | &quot;Unregistered&quot; |
| DECISION_PENDING | &quot;Decision Pending&quot; |
| ACTION_REQUIRED | &quot;Action Required&quot; |
| LIMITED_AVAILABILITY | &quot;Limited Availability&quot; |
| REGISTERED | &quot;Registered&quot; |



