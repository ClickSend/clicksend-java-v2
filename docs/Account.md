

# Account


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**userId** | **Integer** | The unique identifier for the user. |  [optional] |
|**username** | **String** | The username of the user. |  [optional] |
|**userEmail** | **String** | The email address of the user. |  [optional] |
|**active** | **Integer** | Flag indicating if the user account is active. |  [optional] |
|**banned** | **Integer** | Flag indicating if the user account is banned. |  [optional] |
|**dateSignUp** | **Integer** | The Unix timestamp of when the account was created. |  [optional] |
|**balance** | **String** | The balance of the user&#39;s account. |  [optional] |
|**userPhone** | **String** | The phone number of the user. |  [optional] |
|**replyTo** | **String** | The email address to reply to. |  [optional] |
|**deliveryTo** | **String** | The delivery email address. |  [optional] |
|**userFirstName** | **String** | The first name of the user. |  [optional] |
|**userLastName** | **String** | The last name of the user. |  [optional] |
|**account** | **Integer** | The account number. |  [optional] |
|**accountName** | **String** | The name of the account. |  [optional] |
|**accountBillingEmail** | **String** | The billing email address of the account. |  [optional] |
|**accountBillingMobile** | **String** | The billing mobile number of the account. |  [optional] |
|**priority** | **Integer** | The account&#39;s priority tier. |  [optional] |
|**country** | **String** | The country of the user. |  [optional] |
|**countryIp** | **String** | The country the user is currently connecting from, based on IP address. |  [optional] |
|**defaultCountrySms** | **String** | The default country for SMS. |  [optional] |
|**autoRecharge** | **Integer** | Flag indicating if auto-recharge is enabled. |  [optional] |
|**autoRechargeAmount** | **String** | The auto-recharge amount. |  [optional] |
|**lowCreditAmount** | **String** | The low credit amount. |  [optional] |
|**settingUnicodeSms** | **Integer** | Flag indicating if unicode SMS is enabled. |  [optional] |
|**settingEmailSmsSubject** | **Integer** | Flag indicating if email SMS subject is enabled. |  [optional] |
|**settingFixSenderId** | **Integer** | Flag indicating if fixing sender ID is enabled. |  [optional] |
|**settingSmsMessageCharLimit** | **Integer** | The SMS message character limit. |  [optional] |
|**oldDashboard** | **Integer** | Flag indicating if old dashboard is enabled. |  [optional] |
|**balanceCommission** | **String** | The balance commission. |  [optional] |
|**timezone** | **String** | The timezone of the user. |  [optional] |
|**priceRate** | **Integer** | The pricing tier used to determine the cost per message. |  [optional] |
|**privateUploads** | **Integer** | Flag indicating if uploaded media is kept private. |  [optional] |
|**faxQuality** | **Integer** | The quality setting used for outgoing faxes. |  [optional] |
|**settingSmsHideYourNumber** | **Integer** | Flag indicating if your number is hidden on outgoing SMS. |  [optional] |
|**settingSmsHideBusinessName** | **Integer** | Flag indicating if the business name is hidden on outgoing SMS. |  [optional] |
|**pricingVariant** | **Integer** | The pricing variant applied to the account. |  [optional] |
|**onTrial** | **Integer** | Flag indicating if the account is currently on a trial. |  [optional] |
|**trialExpiry** | **String** | The date the trial expires, if the account is on a trial. |  [optional] |
|**currency** | [**Currency**](Currency.md) |  |  [optional] |
|**subaccount** | [**Subaccount**](Subaccount.md) |  |  [optional] |
|**referrerChosen** | [**AccountReferrerChosen**](AccountReferrerChosen.md) |  |  [optional] |



