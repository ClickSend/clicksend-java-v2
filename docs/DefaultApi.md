# DefaultApi

All URIs are relative to *https://rest.clicksend.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**addAllowedEmail**](DefaultApi.md#addAllowedEmail) | **POST** /v3/sms/email-sms | Add Allowed Email |
| [**agreeToRulesAndRegulation**](DefaultApi.md#agreeToRulesAndRegulation) | **POST** /v3/user-countries/agree | Agree to rules and regulation |
| [**calculateEmailCampaignPrice**](DefaultApi.md#calculateEmailCampaignPrice) | **POST** /v3/email-campaigns/price | Calculate Email Campaign Price |
| [**calculateEmailPrice**](DefaultApi.md#calculateEmailPrice) | **POST** /v3/email/price | Calculate Email Price |
| [**calculateFaxPrice**](DefaultApi.md#calculateFaxPrice) | **POST** /v3/fax/price | Calculate Fax Price |
| [**calculateLetterPrice**](DefaultApi.md#calculateLetterPrice) | **POST** /v3/post/letters/price | Calculate Letter Price |
| [**calculateMmsCampaignPrice**](DefaultApi.md#calculateMmsCampaignPrice) | **POST** /v3/mms-campaigns/price | Calculate MMS Campaign Price |
| [**calculateMmsPrice**](DefaultApi.md#calculateMmsPrice) | **POST** /v3/mms/price | Calculate MMS Price |
| [**calculatePostcardPrice**](DefaultApi.md#calculatePostcardPrice) | **POST** /v3/post/postcards/price | Calculate Postcard Price |
| [**calculateSmsCampaignPrice**](DefaultApi.md#calculateSmsCampaignPrice) | **POST** /v3/sms-campaigns/price | Calculate SMS Campaign Price |
| [**calculateSmsPrice**](DefaultApi.md#calculateSmsPrice) | **POST** /v3/sms/price | Calculate SMS Price |
| [**calculateVoicePrice**](DefaultApi.md#calculateVoicePrice) | **POST** /v3/voice/price | Calculate Voice Price |
| [**cancelAllSms**](DefaultApi.md#cancelAllSms) | **PUT** /v3/sms/cancel-all | Cancel All SMS |
| [**cancelAllVoiceMessages**](DefaultApi.md#cancelAllVoiceMessages) | **PUT** /v3/voice/cancel-all | Cancel All Voice Messages |
| [**cancelEmailCampaign**](DefaultApi.md#cancelEmailCampaign) | **PUT** /v3/email-campaigns/{email_campaign_id}/cancel | Cancel Email Campaign |
| [**cancelMmsCampaign**](DefaultApi.md#cancelMmsCampaign) | **PUT** /v3/mms-campaigns/{mms_campaign_id}/cancel | Cancel MMS Campaign |
| [**cancelScheduledLetter**](DefaultApi.md#cancelScheduledLetter) | **PUT** /v3/post/letters/{message_id}/cancel | Cancel Scheduled Letter |
| [**cancelScheduledPostcard**](DefaultApi.md#cancelScheduledPostcard) | **PUT** /v3/post/postcards/{message_id}/cancel | Cancel Scheduled Postcard |
| [**cancelSms**](DefaultApi.md#cancelSms) | **PUT** /v3/sms/{message_id}/cancel | Cancel SMS |
| [**cancelSmsCampaign**](DefaultApi.md#cancelSmsCampaign) | **PUT** /v3/sms-campaigns/{sms_campaign_id}/cancel | Cancel SMS Campaign |
| [**cancelVoiceMessage**](DefaultApi.md#cancelVoiceMessage) | **PUT** /v3/voice/{message_id}/cancel | Cancel Voice Message |
| [**copyContactToList**](DefaultApi.md#copyContactToList) | **PUT** /v3/lists/{from_list_id}/contacts/{contact_id}/copy/{to_list_id} | Copy Contact to List |
| [**createAllowedEmailAddress**](DefaultApi.md#createAllowedEmailAddress) | **POST** /v3/email/addresses | Create Allowed Email Address |
| [**createDefaultSender**](DefaultApi.md#createDefaultSender) | **POST** /v3/senders/default-senders | Create Default Sender |
| [**createDeliveryIssue**](DefaultApi.md#createDeliveryIssue) | **POST** /v3/delivery-issues | Create Delivery Issues |
| [**createEmailDeliveryReceiptRule**](DefaultApi.md#createEmailDeliveryReceiptRule) | **POST** /v3/automations/email/receipts | Create Email Delivery Receipt Rule |
| [**createEmailTemplate**](DefaultApi.md#createEmailTemplate) | **POST** /v3/email/templates | Create Email Template |
| [**createFaxDeliveryReceiptRule**](DefaultApi.md#createFaxDeliveryReceiptRule) | **POST** /v3/automations/fax/receipts | Create FAX Delivery Receipt Rule |
| [**createFaxInboundRule**](DefaultApi.md#createFaxInboundRule) | **POST** /v3/automations/fax/inbound | Create Fax Inbound Rule |
| [**createList**](DefaultApi.md#createList) | **POST** /v3/lists | Create List |
| [**createNewContact**](DefaultApi.md#createNewContact) | **POST** /v3/lists/{list_id}/contacts | Create New Contact |
| [**createResellerAccount**](DefaultApi.md#createResellerAccount) | **POST** /v3/reseller/accounts | Create Reseller Account |
| [**createReturnAddress**](DefaultApi.md#createReturnAddress) | **POST** /v3/post/return-addresses | Create Return Address |
| [**createSmsDeliveryReceiptRule**](DefaultApi.md#createSmsDeliveryReceiptRule) | **POST** /v3/automations/sms/receipts | Create SMS Delivery Receipt Rule |
| [**createSmsInboundAutomation**](DefaultApi.md#createSmsInboundAutomation) | **POST** /v3/automations/sms/inbound | Create SMS Inbound Automation |
| [**createSmsTemplate**](DefaultApi.md#createSmsTemplate) | **POST** /v3/sms/templates | Create SMS Template |
| [**createStrippedStringRule**](DefaultApi.md#createStrippedStringRule) | **POST** /v3/sms/email-sms-stripped-strings | Create Stripped String Rule |
| [**createSubaccount**](DefaultApi.md#createSubaccount) | **POST** /v3/subaccounts | Create Subaccount |
| [**createTestInboundSms**](DefaultApi.md#createTestInboundSms) | **POST** /v3/sms/inbound | Create Test Inbound SMS |
| [**createTestSmsReceipt**](DefaultApi.md#createTestSmsReceipt) | **POST** /v3/sms/receipts | Create Test SMS Receipt |
| [**createVoiceDeliveryReceiptRule**](DefaultApi.md#createVoiceDeliveryReceiptRule) | **POST** /v3/automations/voice/receipts | Create Voice Delivery Receipt Rule |
| [**currentPaymentInfo**](DefaultApi.md#currentPaymentInfo) | **GET** /v3/recharge/credit-card | Current Payment Info |
| [**deleteAllowedEmailAddress**](DefaultApi.md#deleteAllowedEmailAddress) | **DELETE** /v3/email/addresses/{email_address_id} | Delete Allowed Email Address |
| [**deleteAlphaTag**](DefaultApi.md#deleteAlphaTag) | **DELETE** /v3/alpha-tags/{alpha_tag_id} | Delete Alpha Tag |
| [**deleteContact**](DefaultApi.md#deleteContact) | **DELETE** /v3/lists/{list_id}/contacts/{contact_id} | Delete Contact |
| [**deleteDefaultSender**](DefaultApi.md#deleteDefaultSender) | **DELETE** /v3/senders/default-senders/{default_sender_id} | Delete Default Sender |
| [**deleteEmailDeliveryReceiptRule**](DefaultApi.md#deleteEmailDeliveryReceiptRule) | **DELETE** /v3/automations/email/receipts/{receipt_rule_id} | Delete Email Delivery Receipt Rule |
| [**deleteEmailTemplate**](DefaultApi.md#deleteEmailTemplate) | **DELETE** /v3/email/templates/{template_id} | Delete Email Template |
| [**deleteFaxDeliveryReceiptRule**](DefaultApi.md#deleteFaxDeliveryReceiptRule) | **DELETE** /v3/automations/fax/receipts/{receipt_rule_id} | Delete FAX Delivery Receipt Rule |
| [**deleteFaxInboundRule**](DefaultApi.md#deleteFaxInboundRule) | **DELETE** /v3/automations/fax/inbound/{inbound_rule_id} | Delete Fax Inbound Rule |
| [**deleteList**](DefaultApi.md#deleteList) | **DELETE** /v3/lists/{list_id} | Delete List |
| [**deleteOwnNumber**](DefaultApi.md#deleteOwnNumber) | **DELETE** /v3/own-numbers/{own_number_id} | Delete Own Number |
| [**deleteReturnAddress**](DefaultApi.md#deleteReturnAddress) | **DELETE** /v3/post/return-addresses/{return_address_id} | Delete Return Address |
| [**deleteSmsDeliveryReceiptRule**](DefaultApi.md#deleteSmsDeliveryReceiptRule) | **DELETE** /v3/automations/sms/receipts/{receipt_rule_id} | Delete SMS Delivery Receipt Rule |
| [**deleteSmsInboundAutomation**](DefaultApi.md#deleteSmsInboundAutomation) | **DELETE** /v3/automations/sms/inbound/{inbound_rule_id} | Delete SMS Inbound Automation |
| [**deleteSmsTemplate**](DefaultApi.md#deleteSmsTemplate) | **DELETE** /v3/sms/templates/{template_id} | Delete SMS Template |
| [**deleteStrippedStringRule**](DefaultApi.md#deleteStrippedStringRule) | **DELETE** /v3/sms/email-sms-stripped-strings/{rule_id} | Delete Stripped String Rule |
| [**deleteSubaccount**](DefaultApi.md#deleteSubaccount) | **DELETE** /v3/subaccounts/{subaccount_id} | Delete Subaccount |
| [**deleteVoiceDeliveryReceiptRule**](DefaultApi.md#deleteVoiceDeliveryReceiptRule) | **DELETE** /v3/automations/voice/receipts/{receipt_rule_id} | Delete Voice Delivery Receipt Rule |
| [**detectAddress**](DefaultApi.md#detectAddress) | **POST** /v3/post/letters/detect-address | Detect Address |
| [**exportEmailCampaignHistory**](DefaultApi.md#exportEmailCampaignHistory) | **GET** /v3/email-campaigns/{email_campaign_id}/history/export | Export Email Campaign History |
| [**exportEmailHistory**](DefaultApi.md#exportEmailHistory) | **GET** /v3/email/history/export | Export Email History |
| [**exportLetterHistory**](DefaultApi.md#exportLetterHistory) | **GET** /v3/post/letters/history/export | Export Letter History |
| [**exportMmsHistory**](DefaultApi.md#exportMmsHistory) | **GET** /v3/mms/history/export | Export MMS History |
| [**exportPostcardHistory**](DefaultApi.md#exportPostcardHistory) | **GET** /v3/post/postcards/history/export | Export Postcard History |
| [**exportSmsHistory**](DefaultApi.md#exportSmsHistory) | **GET** /v3/sms/history/export | Export SMS History |
| [**exportVoiceHistory**](DefaultApi.md#exportVoiceHistory) | **GET** /v3/voice/history/export | Export Voice History |
| [**forgotPassword**](DefaultApi.md#forgotPassword) | **PUT** /v3/forgot-password | Forgot Password |
| [**forgotUsername**](DefaultApi.md#forgotUsername) | **PUT** /v3/forgot-username | Forgot Username |
| [**generateNewApiKey**](DefaultApi.md#generateNewApiKey) | **PUT** /v3/subaccounts/{subaccount_id}/regen-api-key | Generate New API Key |
| [**getAllDeliveryIssues**](DefaultApi.md#getAllDeliveryIssues) | **GET** /v3/delivery-issues | Get All Delivery Issues |
| [**getAlphaTag**](DefaultApi.md#getAlphaTag) | **GET** /v3/alpha-tags/{alpha_tag_id} | Get Alpha Tag |
| [**getCountriesForGlobalSending**](DefaultApi.md#getCountriesForGlobalSending) | **GET** /v3/user-countries | Get Countries for Global Sending |
| [**getDefaultSenderDetails**](DefaultApi.md#getDefaultSenderDetails) | **GET** /v3/senders/default-senders/{default_sender_id} | Get Default Sender Details |
| [**getDefaultSendersList**](DefaultApi.md#getDefaultSendersList) | **GET** /v3/senders/default-senders | Get List of Default Senders |
| [**getOwnNumberDetail**](DefaultApi.md#getOwnNumberDetail) | **GET** /v3/own-numbers/{own_number_id} | Get Own Number Detail |
| [**getSpecificContact**](DefaultApi.md#getSpecificContact) | **GET** /v3/lists/{list_id}/contacts/{contact_id} | Get Specific Contact |
| [**getVoiceHistory**](DefaultApi.md#getVoiceHistory) | **GET** /v3/voice/history | Get Voice History |
| [**importContacts**](DefaultApi.md#importContacts) | **POST** /v3/lists/{list_id}/import | Import Contacts |
| [**listAlphaTags**](DefaultApi.md#listAlphaTags) | **GET** /v3/alpha-tags | List Alpha Tags |
| [**listCompliantSenderTypes**](DefaultApi.md#listCompliantSenderTypes) | **GET** /v3/senders/compliant-sender-types | List Compliant Sender Types |
| [**listCountries**](DefaultApi.md#listCountries) | **GET** /v3/country-list | International Messaging |
| [**listOwnNumbers**](DefaultApi.md#listOwnNumbers) | **GET** /v3/own-numbers | List Own Numbers |
| [**markInboundSmsAsRead**](DefaultApi.md#markInboundSmsAsRead) | **PUT** /v3/sms/inbound-read | Mark Inbound SMS as Read |
| [**markSmsReceiptAsRead**](DefaultApi.md#markSmsReceiptAsRead) | **PUT** /v3/sms/receipts-read | Mark SMS Receipt As Read |
| [**markSpecificInboundSmsMessageAsRead**](DefaultApi.md#markSpecificInboundSmsMessageAsRead) | **PUT** /v3/sms/inbound-read/{message_id} | Mark Specific Inbound SMS Message As Read |
| [**purchaseDedicatedNumber**](DefaultApi.md#purchaseDedicatedNumber) | **POST** /v3/numbers/buy/{dedicated_number} | Purchase Dedicated Number |
| [**purchaseRechargePackage**](DefaultApi.md#purchaseRechargePackage) | **PUT** /v3/recharge/purchase/{package_id} | Purchase Recharge Package |
| [**registerNumbers**](DefaultApi.md#registerNumbers) | **POST** /v3/numbers/registrations/number-types/{number_type}/country/{country_code} | Register Numbers |
| [**removeDuplicateContacts**](DefaultApi.md#removeDuplicateContacts) | **PUT** /v3/lists/{list_id}/remove-duplicates/ | Remove Duplicate Contacts |
| [**removeOptedOutContacts**](DefaultApi.md#removeOptedOutContacts) | **PUT** /v3/lists/{list_id}/remove-opted-out-contacts/{opt_out_list_id} | Remove Opted Out Contacts |
| [**requestAlphaTag**](DefaultApi.md#requestAlphaTag) | **POST** /v3/alpha-tags | Request Alpha Tag |
| [**requestOwnNumberVerificationOtp**](DefaultApi.md#requestOwnNumberVerificationOtp) | **POST** /v3/own-numbers/verifications | Request Own Number Verification OTP |
| [**resellerTransferCredit**](DefaultApi.md#resellerTransferCredit) | **PUT** /v3/reseller/transfer-credit | Reseller Transfer Credit |
| [**selectCountriesForGlobalSending**](DefaultApi.md#selectCountriesForGlobalSending) | **POST** /v3/user-countries | Select Countries for Global Sending |
| [**sendEmail**](DefaultApi.md#sendEmail) | **POST** /v3/email/send | Send Email |
| [**sendEmailCampaign**](DefaultApi.md#sendEmailCampaign) | **POST** /v3/email-campaigns/send | Send Email Campaign |
| [**sendEmailVerificationToken**](DefaultApi.md#sendEmailVerificationToken) | **PUT** /v3/email/address-verify/{email_address_id}/send | Send Email Verification Token |
| [**sendFax**](DefaultApi.md#sendFax) | **POST** /v3/fax/send | Send Fax |
| [**sendLetter**](DefaultApi.md#sendLetter) | **POST** /v3/post/letters/send | Send Letter |
| [**sendMms**](DefaultApi.md#sendMms) | **POST** /v3/mms/send | Send MMS |
| [**sendMmsCampaign**](DefaultApi.md#sendMmsCampaign) | **POST** /v3/mms-campaigns/send | Send MMS Campaign |
| [**sendPostcard**](DefaultApi.md#sendPostcard) | **POST** /v3/post/postcards/send | Send Postcard |
| [**sendSms**](DefaultApi.md#sendSms) | **POST** /v3/sms/send | Send SMS |
| [**sendSmsCampaign**](DefaultApi.md#sendSmsCampaign) | **POST** /v3/sms-campaigns/send | Send SMS Campaign |
| [**sendVoiceMessage**](DefaultApi.md#sendVoiceMessage) | **POST** /v3/voice/send | Send Voice Message |
| [**shortUrlGetStatistics**](DefaultApi.md#shortUrlGetStatistics) | **GET** /v3/short-url/statistics/{source}/{source_id} | Get Statistics |
| [**shortUrlGetTracking**](DefaultApi.md#shortUrlGetTracking) | **GET** /v3/short-url/tracking/{long_url_id} | Get Tracking |
| [**timezones**](DefaultApi.md#timezones) | **GET** /v3/timezones | Timezones |
| [**transferContactToList**](DefaultApi.md#transferContactToList) | **PUT** /v3/lists/{from_list_id}/contacts/{contact_id}/transfer/{to_list_id} | Transfer Contact to List |
| [**updateClientAccount**](DefaultApi.md#updateClientAccount) | **PUT** /v3/reseller/accounts/{client_user_id} | Update Client Account |
| [**updateContact**](DefaultApi.md#updateContact) | **PUT** /v3/lists/{list_id}/contacts/{contact_id} | Update Contact |
| [**updateDefaultSender**](DefaultApi.md#updateDefaultSender) | **PATCH** /v3/senders/default-senders/{default_sender_id} | Update Default Sender |
| [**updateEmailCampaign**](DefaultApi.md#updateEmailCampaign) | **PUT** /v3/email-campaigns/{email_campaign_id} | Update Email Campaign |
| [**updateEmailDeliveryReceiptRule**](DefaultApi.md#updateEmailDeliveryReceiptRule) | **PUT** /v3/automations/email/receipts/{receipt_rule_id} | Update Email Delivery Receipt Rule |
| [**updateEmailTemplate**](DefaultApi.md#updateEmailTemplate) | **PUT** /v3/email/templates/{template_id} | Update Email Template |
| [**updateFaxDeliveryReceiptRule**](DefaultApi.md#updateFaxDeliveryReceiptRule) | **PUT** /v3/automations/fax/receipts/{receipt_rule_id} | Update FAX Delivery Receipt Rule |
| [**updateFaxInboundRule**](DefaultApi.md#updateFaxInboundRule) | **PUT** /v3/automations/fax/inbound/{inbound_rule_id} | Update Fax Inbound Rule |
| [**updateList**](DefaultApi.md#updateList) | **PUT** /v3/lists/{list_id} | Update List |
| [**updateMmsCampaign**](DefaultApi.md#updateMmsCampaign) | **PUT** /v3/mms-campaigns/{mms_campaign_id} | Update MMS Campaign |
| [**updateOwnNumber**](DefaultApi.md#updateOwnNumber) | **PATCH** /v3/own-numbers/{own_number_id} | Update Own Number |
| [**updatePaymentInfo**](DefaultApi.md#updatePaymentInfo) | **PUT** /v3/recharge/credit-card | Update Payment Info |
| [**updateReturnAddress**](DefaultApi.md#updateReturnAddress) | **PUT** /v3/post/return-addresses/{return_address_id} | Update Return Address |
| [**updateSmsCampaign**](DefaultApi.md#updateSmsCampaign) | **PUT** /v3/sms-campaigns/{sms_campaign_id} | Update SMS Campaign |
| [**updateSmsDeliveryReceiptRule**](DefaultApi.md#updateSmsDeliveryReceiptRule) | **PUT** /v3/automations/sms/receipts/{receipt_rule_id} | Update SMS Delivery Receipt Rule |
| [**updateSmsInboundAutomation**](DefaultApi.md#updateSmsInboundAutomation) | **PUT** /v3/automations/sms/inbound/{inbound_rule_id} | Update SMS Inbound Automation |
| [**updateSmsTemplate**](DefaultApi.md#updateSmsTemplate) | **PUT** /v3/sms/templates/{template_id} | Update SMS Template |
| [**updateStrippedStringRule**](DefaultApi.md#updateStrippedStringRule) | **PUT** /v3/sms/email-sms-stripped-strings/{rule_id} | Update Stripped String Rule |
| [**updateSubaccount**](DefaultApi.md#updateSubaccount) | **PUT** /v3/subaccounts/{subaccount_id} | Update Subaccount |
| [**updateVoiceDeliveryReceiptRule**](DefaultApi.md#updateVoiceDeliveryReceiptRule) | **PUT** /v3/automations/voice/receipts/{receipt_rule_id} | Update Voice Delivery Receipt Rule |
| [**uploadAMediaFile**](DefaultApi.md#uploadAMediaFile) | **POST** /v3/uploads | Upload Media File |
| [**verifyAllowedEmailAddress**](DefaultApi.md#verifyAllowedEmailAddress) | **PUT** /v3/email/address-verify/{email_address_id}/verify/{activation_token} | Verify Allowed Email Address |
| [**verifyOwnNumberOtp**](DefaultApi.md#verifyOwnNumberOtp) | **POST** /v3/own-numbers/verifications/{verification_id}/verify | Verify Own Number OTP |
| [**viewASpecificInboundSmsMessage**](DefaultApi.md#viewASpecificInboundSmsMessage) | **GET** /v3/sms/inbound/{original_message_id} | View a specific inbound SMS message |
| [**viewASpecificSmsTemplate**](DefaultApi.md#viewASpecificSmsTemplate) | **GET** /v3/sms/templates/{template_id} | View a Specific SMS Template |
| [**viewAccountDetails**](DefaultApi.md#viewAccountDetails) | **GET** /v3/account | View Account Details |
| [**viewAccountUsage**](DefaultApi.md#viewAccountUsage) | **GET** /v3/account/usage/{year}/{month}/subaccount | View Account Usage |
| [**viewAllEmailCampaigns**](DefaultApi.md#viewAllEmailCampaigns) | **GET** /v3/email-campaigns | View All Email Campaigns |
| [**viewAllMmsCampaigns**](DefaultApi.md#viewAllMmsCampaigns) | **GET** /v3/mms-campaigns | View All MMS Campaigns |
| [**viewAllTransactions**](DefaultApi.md#viewAllTransactions) | **GET** /v3/recharge/transactions | View All Transactions |
| [**viewAllowedEmailAddress**](DefaultApi.md#viewAllowedEmailAddress) | **GET** /v3/email/addresses/{email_address_id} | View Allowed Email Address |
| [**viewAllowedEmailAddresses**](DefaultApi.md#viewAllowedEmailAddresses) | **GET** /v3/email/addresses | View Allowed Email Addresses |
| [**viewAllowedEmails**](DefaultApi.md#viewAllowedEmails) | **GET** /v3/sms/email-sms | View Allowed Emails |
| [**viewAvailableNumbers**](DefaultApi.md#viewAvailableNumbers) | **GET** /v3/numbers/search/{country} | View Available Numbers |
| [**viewClientAccounts**](DefaultApi.md#viewClientAccounts) | **GET** /v3/reseller/accounts | View Client Accounts |
| [**viewContactLists**](DefaultApi.md#viewContactLists) | **GET** /v3/search/contacts-lists | View Contact Lists |
| [**viewCountries**](DefaultApi.md#viewCountries) | **GET** /v3/countries | View Countries |
| [**viewEmailCampaign**](DefaultApi.md#viewEmailCampaign) | **GET** /v3/email-campaigns/{email_campaign_id} | View Email Campaign |
| [**viewEmailCampaignHistory**](DefaultApi.md#viewEmailCampaignHistory) | **GET** /v3/email-campaigns/{email_campaign_id}/history | View Email Campaign History |
| [**viewEmailDeliveryReceiptRule**](DefaultApi.md#viewEmailDeliveryReceiptRule) | **GET** /v3/automations/email/receipts/{receipt_rule_id} | View Email Delivery Receipt Rule |
| [**viewEmailDeliveryReceiptRules**](DefaultApi.md#viewEmailDeliveryReceiptRules) | **GET** /v3/automations/email/receipts | View Email Delivery Receipt Rules |
| [**viewEmailHistory**](DefaultApi.md#viewEmailHistory) | **GET** /v3/email/history | View Email History |
| [**viewEmailTemplate**](DefaultApi.md#viewEmailTemplate) | **GET** /v3/email/templates/{template_id} | View Email Template |
| [**viewEmailTemplates**](DefaultApi.md#viewEmailTemplates) | **GET** /v3/email/templates | View Email Templates |
| [**viewFaxDeliveryReceiptRule**](DefaultApi.md#viewFaxDeliveryReceiptRule) | **GET** /v3/automations/fax/receipts/{receipt_rule_id} | View FAX Delivery Receipt Rule |
| [**viewFaxDeliveryReceiptRules**](DefaultApi.md#viewFaxDeliveryReceiptRules) | **GET** /v3/automations/fax/receipts | View FAX Delivery Receipt Rules |
| [**viewFaxHistory**](DefaultApi.md#viewFaxHistory) | **GET** /v3/fax/history | View Fax History |
| [**viewFaxInboundRule**](DefaultApi.md#viewFaxInboundRule) | **GET** /v3/automations/fax/inbound/{inbound_rule_id} | View Fax Inbound Rule |
| [**viewFaxInboundRules**](DefaultApi.md#viewFaxInboundRules) | **GET** /v3/automations/fax/inbound | View Fax Inbound Rules |
| [**viewFaxReceipts**](DefaultApi.md#viewFaxReceipts) | **GET** /v3/fax/receipts | View Fax Receipts |
| [**viewInboundSms**](DefaultApi.md#viewInboundSms) | **GET** /v3/sms/inbound | View Inbound SMS |
| [**viewLetterHistory**](DefaultApi.md#viewLetterHistory) | **GET** /v3/post/letters/history | View Letter History |
| [**viewListContacts**](DefaultApi.md#viewListContacts) | **GET** /v3/lists/{list_id}/contacts | View List Contacts |
| [**viewLists**](DefaultApi.md#viewLists) | **GET** /v3/lists | View Lists |
| [**viewMasterEmailTemplate**](DefaultApi.md#viewMasterEmailTemplate) | **GET** /v3/email/master-templates/{template_id} | View Master Email Template |
| [**viewMasterEmailTemplates**](DefaultApi.md#viewMasterEmailTemplates) | **GET** /v3/email/master-templates | View Master Email Templates |
| [**viewMmsCampaign**](DefaultApi.md#viewMmsCampaign) | **GET** /v3/mms-campaigns/{mms_campaign_id} | View MMS Campaign |
| [**viewMmsHistory**](DefaultApi.md#viewMmsHistory) | **GET** /v3/mms/history | View MMS History |
| [**viewPostcardHistory**](DefaultApi.md#viewPostcardHistory) | **GET** /v3/post/postcards/history | View Postcard History |
| [**viewRechargePackages**](DefaultApi.md#viewRechargePackages) | **GET** /v3/recharge/packages | View Recharge Packages |
| [**viewReferralAccounts**](DefaultApi.md#viewReferralAccounts) | **GET** /v3/referral/accounts/ | View Referral Accounts |
| [**viewSmsCampaigns**](DefaultApi.md#viewSmsCampaigns) | **GET** /v3/sms-campaigns | View SMS Campaigns |
| [**viewSmsDeliveryReceiptRule**](DefaultApi.md#viewSmsDeliveryReceiptRule) | **GET** /v3/automations/sms/receipts/{receipt_rule_id} | View SMS Delivery Receipt Rule |
| [**viewSmsDeliveryReceiptRules**](DefaultApi.md#viewSmsDeliveryReceiptRules) | **GET** /v3/automations/sms/receipts | View SMS Delivery Receipt Rules |
| [**viewSmsHistory**](DefaultApi.md#viewSmsHistory) | **GET** /v3/sms/history | View SMS History |
| [**viewSmsInboundAutomation**](DefaultApi.md#viewSmsInboundAutomation) | **GET** /v3/automations/sms/inbound/{inbound_rule_id} | View SMS Inbound Automation |
| [**viewSmsInboundAutomations**](DefaultApi.md#viewSmsInboundAutomations) | **GET** /v3/automations/sms/inbound | View SMS Inbound Automations |
| [**viewSmsReceipts**](DefaultApi.md#viewSmsReceipts) | **GET** /v3/sms/receipts | View SMS Receipts |
| [**viewSmsStatistics**](DefaultApi.md#viewSmsStatistics) | **GET** /v3/statistics/sms | View SMS Statistics |
| [**viewSmsTemplates**](DefaultApi.md#viewSmsTemplates) | **GET** /v3/sms/templates | View SMS Templates |
| [**viewSpecificClientAccount**](DefaultApi.md#viewSpecificClientAccount) | **GET** /v3/reseller/accounts/{client_user_id} | View Specific Client Account |
| [**viewSpecificFaxReceipt**](DefaultApi.md#viewSpecificFaxReceipt) | **GET** /v3/fax/receipts/{message_id} | View Specific Fax Receipt |
| [**viewSpecificList**](DefaultApi.md#viewSpecificList) | **GET** /v3/lists/{list_id} | View Specific List |
| [**viewSpecificReturnAddress**](DefaultApi.md#viewSpecificReturnAddress) | **GET** /v3/post/return-addresses/{return_address_id} | View Specific Return Address |
| [**viewSpecificSmsCampaign**](DefaultApi.md#viewSpecificSmsCampaign) | **GET** /v3/sms-campaigns/{sms_campaign_id} | View Specific SMS Campaign |
| [**viewSpecificSmsReceipt**](DefaultApi.md#viewSpecificSmsReceipt) | **GET** /v3/sms/receipts/{message_id} | View Specific SMS Receipt |
| [**viewSpecificSubaccount**](DefaultApi.md#viewSpecificSubaccount) | **GET** /v3/subaccounts/{subaccount_id} | View Specific Subaccount |
| [**viewSpecificTransaction**](DefaultApi.md#viewSpecificTransaction) | **GET** /v3/recharge/transactions/{transaction_id} | View Specific Transaction |
| [**viewStrippedStringRule**](DefaultApi.md#viewStrippedStringRule) | **GET** /v3/sms/email-sms-stripped-strings/{rule_id} | View Stripped String Rule |
| [**viewStrippedStringRules**](DefaultApi.md#viewStrippedStringRules) | **GET** /v3/sms/email-sms-stripped-strings | View Stripped String Rules |
| [**viewSubaccounts**](DefaultApi.md#viewSubaccounts) | **GET** /v3/subaccounts | View Subaccounts |
| [**viewTemplateCategories**](DefaultApi.md#viewTemplateCategories) | **GET** /v3/email/master-templates-categories | View Template Categories |
| [**viewTemplateCategory**](DefaultApi.md#viewTemplateCategory) | **GET** /v3/email/master-templates-categories/{category_id} | View Template Category |
| [**viewTemplatesInCategory**](DefaultApi.md#viewTemplatesInCategory) | **GET** /v3/email/master-templates-categories/{category_id}/master-templates | View Templates in Category |
| [**viewVoiceDeliveryReceiptRule**](DefaultApi.md#viewVoiceDeliveryReceiptRule) | **GET** /v3/automations/voice/receipts/{receipt_rule_id} | View Voice Delivery Receipt Rule |
| [**viewVoiceDeliveryReceiptRules**](DefaultApi.md#viewVoiceDeliveryReceiptRules) | **GET** /v3/automations/voice/receipts | View Voice Delivery Receipt Rules |
| [**viewVoiceLanguages**](DefaultApi.md#viewVoiceLanguages) | **GET** /v3/voice/lang | View Voice Languages |
| [**viewVoiceReceipts**](DefaultApi.md#viewVoiceReceipts) | **GET** /v3/voice/receipts | View Voice Receipts |
| [**viewVoiceStatistics**](DefaultApi.md#viewVoiceStatistics) | **GET** /v3/statistics/voice | View Voice Statistics |
| [**viewYourNumbers**](DefaultApi.md#viewYourNumbers) | **GET** /v3/numbers | View Your Numbers |
| [**viewYourReturnAddresses**](DefaultApi.md#viewYourReturnAddresses) | **GET** /v3/post/return-addresses | View Your Return Addresses |


<a id="addAllowedEmail"></a>
# **addAllowedEmail**
> AddAllowedEmail addAllowedEmail(contentType, addAllowedEmailRequest)

Add Allowed Email

_Create email to sms allowed address_  ### Properties  | Name | Type | Required | Restrictions | Description | | --- | --- | --- | --- | --- | | email_address | string | true | none | Your email address | | from | string | false | [yes](http://help.clicksend.com/SMS/what-is-a-sender-id-or-sender-number) | Your sender id |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String contentType = "application/json"; // String | 
    AddAllowedEmailRequest addAllowedEmailRequest = new AddAllowedEmailRequest(); // AddAllowedEmailRequest | 
    try {
      AddAllowedEmail result = apiInstance.addAllowedEmail(contentType, addAllowedEmailRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#addAllowedEmail");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **contentType** | **String**|  | [optional] |
| **addAllowedEmailRequest** | [**AddAllowedEmailRequest**](AddAllowedEmailRequest.md)|  | [optional] |

### Return type

[**AddAllowedEmail**](AddAllowedEmail.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="agreeToRulesAndRegulation"></a>
# **agreeToRulesAndRegulation**
> AgreeToRulesAndRegulation agreeToRulesAndRegulation()

Agree to rules and regulation

_Update Country Rule_  To agree on rules and regulations of selected countries and confirm selection.  ### Properties  | Name | Type | Required | Restrictions | Description | | --- | --- | --- | --- | --- | | country_list_ids | number | true | none | Country list ID&#39;s |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    try {
      AgreeToRulesAndRegulation result = apiInstance.agreeToRulesAndRegulation();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#agreeToRulesAndRegulation");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**AgreeToRulesAndRegulation**](AgreeToRulesAndRegulation.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="calculateEmailCampaignPrice"></a>
# **calculateEmailCampaignPrice**
> CalculateEmailCampaignPrice calculateEmailCampaignPrice(contentType, calculateEmailCampaignPriceRequest)

Calculate Email Campaign Price

_Calculate email campaign price_  Calculate email campaign price  ### Properties  | Name | Type | Required | Restrictions | Description | | --- | --- | --- | --- | --- | | name | string | true | none | Your campaign name. | | subject | string | true | none | Your campaign subject. | | body | string | true | none | Your campaign message. | | from_email_address_id | number | true | none | The allowed email address id. | | from_name | string | true | none | Your name or business name. | | template_id | number | false | none | Your template id. | | list_id | number | true | none | Your contact list id. | | schedule | integer(int32) | false | none | Your schedule timestamp. |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String contentType = "application/json"; // String | 
    CalculateEmailCampaignPriceRequest calculateEmailCampaignPriceRequest = new CalculateEmailCampaignPriceRequest(); // CalculateEmailCampaignPriceRequest | 
    try {
      CalculateEmailCampaignPrice result = apiInstance.calculateEmailCampaignPrice(contentType, calculateEmailCampaignPriceRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#calculateEmailCampaignPrice");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **contentType** | **String**|  | [optional] |
| **calculateEmailCampaignPriceRequest** | [**CalculateEmailCampaignPriceRequest**](CalculateEmailCampaignPriceRequest.md)|  | [optional] |

### Return type

[**CalculateEmailCampaignPrice**](CalculateEmailCampaignPrice.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="calculateEmailPrice"></a>
# **calculateEmailPrice**
> CalculateEmailPrice calculateEmailPrice(contentType, calculateEmailPriceRequest)

Calculate Email Price

_Get transactional email price_  Get transactional email price  ### Properties  | Name | Type | Required | Restrictions | Description | | --- | --- | --- | --- | --- | | to | array | true | none | Array of To Recipient items. (array of names and emails) | | cc | array | false | none | Array of Cc Recipient items. (array of names and emails) | | bcc | array | false | none | Array of Bcc Recipient items. (array of names and emails) | | from | object | true | none | From Email object. (object containing name and email) | | body | string | true | none | Body of the email. | | attachments | array | false | none | Array of Attachment items. | | schedule | number | false | none | Schedule. | | name | string | false | none | Name of person email belongs to | | email | string | true | none | Email to be used. | | content | string | true | none | The base64-encoded contents of the file. | | type | string | true | none | The type of file being attached. | | filename | string | true | none | The name of the file being attached. | | disposition | string | true | none | Inline for content that can be displayed within the email, or attachment for any other files. | | content_id | string | true | none | An ID for the content. |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String contentType = "application/json"; // String | 
    CalculateEmailPriceRequest calculateEmailPriceRequest = new CalculateEmailPriceRequest(); // CalculateEmailPriceRequest | 
    try {
      CalculateEmailPrice result = apiInstance.calculateEmailPrice(contentType, calculateEmailPriceRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#calculateEmailPrice");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **contentType** | **String**|  | [optional] |
| **calculateEmailPriceRequest** | [**CalculateEmailPriceRequest**](CalculateEmailPriceRequest.md)|  | [optional] |

### Return type

[**CalculateEmailPrice**](CalculateEmailPrice.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="calculateFaxPrice"></a>
# **calculateFaxPrice**
> CalculateFaxPrice calculateFaxPrice(contentType, calculateFaxPriceRequest)

Calculate Fax Price

_Calculate Total Price for Fax Messages sent_  ### Properties  | Name | Type | Required | Restrictions | Description | | --- | --- | --- | --- | --- | | file_url | string | true | none | URL of file to send | | source | string | true | none | Your method of sending e.g. &#39;wordpress&#39;, &#39;php&#39;, &#39;c#&#39;. | | to | string | true | none | Recipient fax number in [E.164](https://en.wikipedia.org/wiki/E.164) format. | | list_id | integer(int32) | false | none | Your list ID if sending to a whole list. Can be used instead of &#39;to&#39;. | | from | string | true | [yes](http://help.clicksend.com/SMS/what-is-a-sender-id-or-sender-number) | Your sender id. Must be a valid fax number. | | schedule | integer(int32) | false | none | Leave blank for immediate delivery. Your schedule time in unix format [http://help.clicksend.com/what-is-a-unix-timestamp](http://help.clicksend.com/what-is-a-unix-timestamp) | | custom_string | string | false | none | Your reference. Will be passed back with all replies and delivery reports. | | country | string | false | none | ISO alpha-2 character country code e.g. &#39;US&#39;, we use this to format the recipient number if it&#39;s not in international format. | | from_email | string | false | none | An email address where the reply should be emailed to. |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String contentType = "application/json"; // String | 
    CalculateFaxPriceRequest calculateFaxPriceRequest = new CalculateFaxPriceRequest(); // CalculateFaxPriceRequest | 
    try {
      CalculateFaxPrice result = apiInstance.calculateFaxPrice(contentType, calculateFaxPriceRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#calculateFaxPrice");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **contentType** | **String**|  | [optional] |
| **calculateFaxPriceRequest** | [**CalculateFaxPriceRequest**](CalculateFaxPriceRequest.md)|  | [optional] |

### Return type

[**CalculateFaxPrice**](CalculateFaxPrice.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="calculateLetterPrice"></a>
# **calculateLetterPrice**
> CalculateLetterPrice calculateLetterPrice(contentType, calculateLetterPriceRequest)

Calculate Letter Price

_Calculate letter price_  ### Properties  | Name | Type | Required | Restrictions | Description | | --- | --- | --- | --- | --- | | file_url | string | true | none | URL of file to send | | address_name | string | true | none | Name of address | | address_line_1 | string | true | none | First line of address | | address_line_2 | string | true | none | Second line of address | | address_city | string | true | none | City | | address_state | string | true | none | State | | address_postal_code | string | true | none | Postal code | | address_country | string | true | none | Country | | return_address_id | integer(int32) | true | none | ID of return address to use | | schedule | integer(int32) | false | none | When to send letter (0/null&#x3D;now) | | template_used | integer(int1) | false | none | Whether using our letter template. Flag value must be 1 for yes or 0 for no. | | duplex | integer(int1) | false | none | Whether letter is duplex. Flag value must be 1 for yes or 0 for no. | | colour | integer(int1) | false | none | Whether letter is in colour. Flag value must be 1 for yes or 0 for no. | | priority_post | integer(int1) | false | none | Whether letter is priority. Flag value must be 1 for yes or 0 for no. | | source | string | false | none | Source being sent from |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String contentType = "application/json"; // String | 
    CalculateLetterPriceRequest calculateLetterPriceRequest = new CalculateLetterPriceRequest(); // CalculateLetterPriceRequest | 
    try {
      CalculateLetterPrice result = apiInstance.calculateLetterPrice(contentType, calculateLetterPriceRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#calculateLetterPrice");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **contentType** | **String**|  | [optional] |
| **calculateLetterPriceRequest** | [**CalculateLetterPriceRequest**](CalculateLetterPriceRequest.md)|  | [optional] |

### Return type

[**CalculateLetterPrice**](CalculateLetterPrice.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="calculateMmsCampaignPrice"></a>
# **calculateMmsCampaignPrice**
> CalculateMmsCampaignPrice calculateMmsCampaignPrice(contentType, body)

Calculate MMS Campaign Price

_Calculate price for mms campaign_  ### Properties  | Name | Type | Required | Restrictions | Description | | --- | --- | --- | --- | --- | | list_id | integer(int32) | true | none | Your list id. | | name | string | true | none | Your campaign name. | | body | string | true | none | Your campaign message. | | from | string | true | [yes](http://help.clicksend.com/SMS/what-is-a-sender-id-or-sender-number) | Your sender id | | schedule | integer(int32) | false | none | Your schedule timestamp. | | subject | string | true | none | Subject of MMS campaign. | | media_file | string | true | none | URL pointing to media file. |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String contentType = "application/json"; // String | 
    Object body = null; // Object | 
    try {
      CalculateMmsCampaignPrice result = apiInstance.calculateMmsCampaignPrice(contentType, body);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#calculateMmsCampaignPrice");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **contentType** | **String**|  | [optional] |
| **body** | **Object**|  | [optional] |

### Return type

[**CalculateMmsCampaignPrice**](CalculateMmsCampaignPrice.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="calculateMmsPrice"></a>
# **calculateMmsPrice**
> CalculateMmsPrice calculateMmsPrice(contentType, calculateMmsPriceRequest)

Calculate MMS Price

_Get Price for MMS sent_  ### Properties  | Name | Type | Required | Restrictions | Description | | --- | --- | --- | --- | --- | | media_file | string | true | none | Media file you want to send | | to | string | true | none | Recipient phone number in [E.164](https://en.wikipedia.org/wiki/E.164) format | | body | string | true | none | Your message | | subject | string | true | none | Subject line (max 20 characters) | | from | string | true | [yes](http://help.clicksend.com/SMS/what-is-a-sender-id-or-sender-number) | Your sender id |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String contentType = "application/json"; // String | 
    CalculateMmsPriceRequest calculateMmsPriceRequest = new CalculateMmsPriceRequest(); // CalculateMmsPriceRequest | 
    try {
      CalculateMmsPrice result = apiInstance.calculateMmsPrice(contentType, calculateMmsPriceRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#calculateMmsPrice");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **contentType** | **String**|  | [optional] |
| **calculateMmsPriceRequest** | [**CalculateMmsPriceRequest**](CalculateMmsPriceRequest.md)|  | [optional] |

### Return type

[**CalculateMmsPrice**](CalculateMmsPrice.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="calculatePostcardPrice"></a>
# **calculatePostcardPrice**
> CalculatePostcardPrice calculatePostcardPrice(contentType, sendPostcardRequest)

Calculate Postcard Price

_Calculate price for sending one or more postcards_  For &#x60;file_urls&#x60; field. You can attach at least 1 and max of 2 PDF file urls.  - Supply a single pdf with 2 pages (front and back) - Supply 2 urls to seperate PDFs       ### Properties  | Name | Type | Required | Restrictions | Description | | --- | --- | --- | --- | --- | | file_urls | \\[string\\] | true | none | Postcard file URLs | | address_name | string | true | none | Name of address | | address_line_1 | string | true | none | First line of address | | address_line_2 | string | true | none | Second line of address | | address_city | string | true | none | City | | address_state | string | true | none | State | | address_postal_code | string | true | none | Postal code | | address_country | string | true | none | Country | | return_address_id | integer(int32) | true | none | ID of return address to use | | schedule | integer(int32) | false | none | When to send letter (0/null&#x3D;now) |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String contentType = "application/json"; // String | 
    SendPostcardRequest sendPostcardRequest = new SendPostcardRequest(); // SendPostcardRequest | 
    try {
      CalculatePostcardPrice result = apiInstance.calculatePostcardPrice(contentType, sendPostcardRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#calculatePostcardPrice");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **contentType** | **String**|  | [optional] |
| **sendPostcardRequest** | [**SendPostcardRequest**](SendPostcardRequest.md)|  | [optional] |

### Return type

[**CalculatePostcardPrice**](CalculatePostcardPrice.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="calculateSmsCampaignPrice"></a>
# **calculateSmsCampaignPrice**
> CalculateSmsCampaignPrice calculateSmsCampaignPrice(contentType, calculateSmsCampaignPriceRequest)

Calculate SMS Campaign Price

_Calculate price for sms campaign_  ### Properties  | Name | Type | Required | Restrictions | Description | | --- | --- | --- | --- | --- | | list_id | integer(int32) | true | none | Your list id. | | name | string | true | none | Your campaign name. | | body | string | true | none | Your campaign message. | | from | string | true | [yes](http://help.clicksend.com/SMS/what-is-a-sender-id-or-sender-number) | Your sender id | | schedule | integer(int32) | false | none | Your schedule timestamp. |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String contentType = "application/json"; // String | 
    CalculateSmsCampaignPriceRequest calculateSmsCampaignPriceRequest = new CalculateSmsCampaignPriceRequest(); // CalculateSmsCampaignPriceRequest | 
    try {
      CalculateSmsCampaignPrice result = apiInstance.calculateSmsCampaignPrice(contentType, calculateSmsCampaignPriceRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#calculateSmsCampaignPrice");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **contentType** | **String**|  | [optional] |
| **calculateSmsCampaignPriceRequest** | [**CalculateSmsCampaignPriceRequest**](CalculateSmsCampaignPriceRequest.md)|  | [optional] |

### Return type

[**CalculateSmsCampaignPrice**](CalculateSmsCampaignPrice.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="calculateSmsPrice"></a>
# **calculateSmsPrice**
> CalculateSmsPrice calculateSmsPrice(contentType, calculateSmsPriceRequest)

Calculate SMS Price

Use this endpoint to calculate the price of sending messages. The cost of sending messages varies based on the &lt;a href&#x3D;\&quot;https://help.clicksend.com/article/h474eseq3a-how-many-characters-can-i-send-in-an-sms\&quot; target&#x3D;\&quot;_blank\&quot;&gt;type&lt;/a&gt; and length of the message.

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String contentType = "application/json"; // String | 
    CalculateSmsPriceRequest calculateSmsPriceRequest = new CalculateSmsPriceRequest(); // CalculateSmsPriceRequest | 
    try {
      CalculateSmsPrice result = apiInstance.calculateSmsPrice(contentType, calculateSmsPriceRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#calculateSmsPrice");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **contentType** | **String**|  | [optional] |
| **calculateSmsPriceRequest** | [**CalculateSmsPriceRequest**](CalculateSmsPriceRequest.md)|  | [optional] |

### Return type

[**CalculateSmsPrice**](CalculateSmsPrice.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="calculateVoicePrice"></a>
# **calculateVoicePrice**
> CalculateVoicePrice calculateVoicePrice(contentType, calculateVoicePriceRequest)

Calculate Voice Price

_Calculate voice price_  ### Properties  | Name | Type | Required | Restrictions | Description | | --- | --- | --- | --- | --- | | to | string | true | none | Your phone number in [E.164](https://en.wikipedia.org/wiki/E.164) format. | | body | string | true | none | Biscuit uv3nlCOjRk croissant chocolate lollipop chocolate muffin. | | voice | string | true | none | Either &#39;female&#39; or &#39;male&#39;. | | custom_string | string | true | none | Your reference. Will be passed back with all replies and delivery reports. | | country | string | true | none | The country of the recipient. | | source | string | false | none | Your method of sending e.g. &#39;wordpress&#39;, &#39;php&#39;, &#39;c#&#39;. | | list_id | integer(int32) | false | none | Your list ID if sending to a whole list. Can be used instead of &#39;to&#39;. | | lang | string | false | none | au (string, required) - See section on available languages. | | schedule | integer(int32) | false | none | Leave blank for immediate delivery. Your schedule time in unix format [http://help.clicksend.com/what-is-a-unix-timestamp](http://help.clicksend.com/what-is-a-unix-timestamp) | | require_input | integer(int1) | false | none | Recieve a keypress from the recipient. Flag value must be 1 for yes or 0 for no. | | machine_detection | integer(int1) | false | none | Detect answering machine or voicemail and leave a message. Flag value must be 1 for yes or 0 for no. |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String contentType = "application/json"; // String | 
    CalculateVoicePriceRequest calculateVoicePriceRequest = new CalculateVoicePriceRequest(); // CalculateVoicePriceRequest | 
    try {
      CalculateVoicePrice result = apiInstance.calculateVoicePrice(contentType, calculateVoicePriceRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#calculateVoicePrice");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **contentType** | **String**|  | [optional] |
| **calculateVoicePriceRequest** | [**CalculateVoicePriceRequest**](CalculateVoicePriceRequest.md)|  | [optional] |

### Return type

[**CalculateVoicePrice**](CalculateVoicePrice.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="cancelAllSms"></a>
# **cancelAllSms**
> CancelAllSms cancelAllSms(contentType, cancelAllSmsRequest)

Cancel All SMS

Use this endpoint to cancel all scheduled SMS. To cancel only one scheduled SMS, use the **Cancel SMS** endpoint.

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String contentType = "application/json"; // String | 
    CancelAllSmsRequest cancelAllSmsRequest = new CancelAllSmsRequest(); // CancelAllSmsRequest | 
    try {
      CancelAllSms result = apiInstance.cancelAllSms(contentType, cancelAllSmsRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#cancelAllSms");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **contentType** | **String**|  | [optional] |
| **cancelAllSmsRequest** | [**CancelAllSmsRequest**](CancelAllSmsRequest.md)|  | [optional] |

### Return type

[**CancelAllSms**](CancelAllSms.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="cancelAllVoiceMessages"></a>
# **cancelAllVoiceMessages**
> CancelAllVoiceMessages cancelAllVoiceMessages(contentType, body)

Cancel All Voice Messages

_Update all voice messages as cancelled_  Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.  &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String contentType = "application/x-www-form-urlencoded"; // String | 
    Object body = null; // Object | 
    try {
      CancelAllVoiceMessages result = apiInstance.cancelAllVoiceMessages(contentType, body);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#cancelAllVoiceMessages");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **contentType** | **String**|  | [optional] |
| **body** | **Object**|  | [optional] |

### Return type

[**CancelAllVoiceMessages**](CancelAllVoiceMessages.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="cancelEmailCampaign"></a>
# **cancelEmailCampaign**
> CancelEmailCampaign cancelEmailCampaign(emailCampaignId, contentType, cancelEmailCampaignRequest)

Cancel Email Campaign

_Cancel email campaign_  Cancel email campaign  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | email_campaign_id | path | integer(int32) | true | Allowed email campaign id | | date_from | query | integer(int32) | false | Start date (Unix Timestamp e.g. 1436849372) | | date_to | query | integer(int32) | false | End date (Unix Timestamp e.g. 1436879372) | | page | query | integer(int32) | false | [Page number](/#pagination) | | limit | query | integer(int32) | false | [Number of records per page](/#pagination) |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String emailCampaignId = "emailCampaignId_example"; // String | 
    String contentType = "application/json"; // String | 
    CancelEmailCampaignRequest cancelEmailCampaignRequest = new CancelEmailCampaignRequest(); // CancelEmailCampaignRequest | 
    try {
      CancelEmailCampaign result = apiInstance.cancelEmailCampaign(emailCampaignId, contentType, cancelEmailCampaignRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#cancelEmailCampaign");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **emailCampaignId** | **String**|  | |
| **contentType** | **String**|  | [optional] |
| **cancelEmailCampaignRequest** | [**CancelEmailCampaignRequest**](CancelEmailCampaignRequest.md)|  | [optional] |

### Return type

[**CancelEmailCampaign**](CancelEmailCampaign.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="cancelMmsCampaign"></a>
# **cancelMmsCampaign**
> CancelMmsCampaign cancelMmsCampaign(mmsCampaignId, contentType, calculateSmsCampaignPriceRequest)

Cancel MMS Campaign

_Cancel mms campaign_  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | mms_campaign_id | path | integer(int32) | true | ID of MMS Campaign to cancel |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String mmsCampaignId = "mmsCampaignId_example"; // String | 
    String contentType = "application/json"; // String | 
    CalculateSmsCampaignPriceRequest calculateSmsCampaignPriceRequest = new CalculateSmsCampaignPriceRequest(); // CalculateSmsCampaignPriceRequest | 
    try {
      CancelMmsCampaign result = apiInstance.cancelMmsCampaign(mmsCampaignId, contentType, calculateSmsCampaignPriceRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#cancelMmsCampaign");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **mmsCampaignId** | **String**|  | |
| **contentType** | **String**|  | [optional] |
| **calculateSmsCampaignPriceRequest** | [**CalculateSmsCampaignPriceRequest**](CalculateSmsCampaignPriceRequest.md)|  | [optional] |

### Return type

[**CancelMmsCampaign**](CancelMmsCampaign.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="cancelScheduledLetter"></a>
# **cancelScheduledLetter**
> CancelScheduledLetter cancelScheduledLetter(messageId)

Cancel Scheduled Letter

_Cancel scheduled letter_  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | message_id | query | string | true | Message ID of the scheduled letter that is to be cancelled. |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String messageId = "messageId_example"; // String | 
    try {
      CancelScheduledLetter result = apiInstance.cancelScheduledLetter(messageId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#cancelScheduledLetter");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **messageId** | **String**|  | |

### Return type

[**CancelScheduledLetter**](CancelScheduledLetter.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="cancelScheduledPostcard"></a>
# **cancelScheduledPostcard**
> CancelScheduledPostcard cancelScheduledPostcard(messageId)

Cancel Scheduled Postcard

_Cancel scheduled postcard_  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | message_id | query | string | true | Message ID of the scheduled postcard that is to be cancelled. |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String messageId = "messageId_example"; // String | 
    try {
      CancelScheduledPostcard result = apiInstance.cancelScheduledPostcard(messageId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#cancelScheduledPostcard");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **messageId** | **String**|  | |

### Return type

[**CancelScheduledPostcard**](CancelScheduledPostcard.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="cancelSms"></a>
# **cancelSms**
> CancelSms cancelSms(messageId, contentType)

Cancel SMS

Use this endpoint to cancel a specific scheduled SMS. Unlike the **Cancel All SMS** endpoint, which cancels all scheduled SMS, this endpoint only cancels one specified scheduled SMS.  Specify the scheduled SMS to cancel by providing its _message_id_.

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String messageId = "messageId_example"; // String | The _message_id_ of the scheduled SMS to cancel.
    String contentType = "application/json"; // String | 
    try {
      CancelSms result = apiInstance.cancelSms(messageId, contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#cancelSms");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **messageId** | **String**| The _message_id_ of the scheduled SMS to cancel. | |
| **contentType** | **String**|  | [optional] |

### Return type

[**CancelSms**](CancelSms.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="cancelSmsCampaign"></a>
# **cancelSmsCampaign**
> CancelSmsCampaign cancelSmsCampaign(smsCampaignId, contentType)

Cancel SMS Campaign

Use this endpoint to cancel a scheduled SMS campaign.

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String smsCampaignId = "smsCampaignId_example"; // String | ID of the scheduled SMS campaign to cancel.
    String contentType = "application/json"; // String | 
    try {
      CancelSmsCampaign result = apiInstance.cancelSmsCampaign(smsCampaignId, contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#cancelSmsCampaign");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **smsCampaignId** | **String**| ID of the scheduled SMS campaign to cancel. | |
| **contentType** | **String**|  | [optional] |

### Return type

[**CancelSmsCampaign**](CancelSmsCampaign.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="cancelVoiceMessage"></a>
# **cancelVoiceMessage**
> CancelVoiceMessage cancelVoiceMessage(messageId, contentType, body)

Cancel Voice Message

_Update voice message status as cancelled_  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | message_id | path | string | true | Your voice message id |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String messageId = "messageId_example"; // String | 
    String contentType = "application/x-www-form-urlencoded"; // String | 
    Object body = null; // Object | 
    try {
      CancelVoiceMessage result = apiInstance.cancelVoiceMessage(messageId, contentType, body);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#cancelVoiceMessage");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **messageId** | **String**|  | |
| **contentType** | **String**|  | [optional] |
| **body** | **Object**|  | [optional] |

### Return type

[**CancelVoiceMessage**](CancelVoiceMessage.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="copyContactToList"></a>
# **copyContactToList**
> CopyContactToList copyContactToList(fromListId, contactId, toListId, contentType, body)

Copy Contact to List

_Copy contact to another list_  Copy contact to another list  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | from_list_id | path | integer(int32) | true | List ID for list that contains contact. | | contact_id | path | integer(int32) | true | Contact ID | | to_list_id | path | integer(int32) | true | List ID for list you want to copy contact to. |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String fromListId = "fromListId_example"; // String | 
    String contactId = "contactId_example"; // String | 
    String toListId = "toListId_example"; // String | 
    String contentType = "application/json"; // String | 
    Object body = null; // Object | 
    try {
      CopyContactToList result = apiInstance.copyContactToList(fromListId, contactId, toListId, contentType, body);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#copyContactToList");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **fromListId** | **String**|  | |
| **contactId** | **String**|  | |
| **toListId** | **String**|  | |
| **contentType** | **String**|  | [optional] |
| **body** | **Object**|  | [optional] |

### Return type

[**CopyContactToList**](CopyContactToList.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="createAllowedEmailAddress"></a>
# **createAllowedEmailAddress**
> CreateAllowedEmailAddress createAllowedEmailAddress(contentType, createAllowedEmailAddressRequest)

Create Allowed Email Address

_Create allowed Email Address_  Create allowed Email Address  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | body | body | string | true | Email to be allowed. |  Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.  &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String contentType = "application/json"; // String | 
    CreateAllowedEmailAddressRequest createAllowedEmailAddressRequest = new CreateAllowedEmailAddressRequest(); // CreateAllowedEmailAddressRequest | 
    try {
      CreateAllowedEmailAddress result = apiInstance.createAllowedEmailAddress(contentType, createAllowedEmailAddressRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#createAllowedEmailAddress");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **contentType** | **String**|  | [optional] |
| **createAllowedEmailAddressRequest** | [**CreateAllowedEmailAddressRequest**](CreateAllowedEmailAddressRequest.md)|  | [optional] |

### Return type

[**CreateAllowedEmailAddress**](CreateAllowedEmailAddress.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="createDefaultSender"></a>
# **createDefaultSender**
> CreateDefaultSender createDefaultSender(contentType, createDefaultSenderRequest)

Create Default Sender

Creates a new default sender configuration to automate the selection of compliant SenderIDs. By configuring a default sender you no longer need to define the &#x60;sender_id&#x60; string when sending SMS messages. The default sender will be picked up automatically.  For more information on Sender IDs, please refer to [What is a Sender ID or Sender Number?](https://help.clicksend.com/article/4kgj7krx00-what-is-a-sender-id-or-sender-number)

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String contentType = "application/json"; // String | 
    CreateDefaultSenderRequest createDefaultSenderRequest = new CreateDefaultSenderRequest(); // CreateDefaultSenderRequest | 
    try {
      CreateDefaultSender result = apiInstance.createDefaultSender(contentType, createDefaultSenderRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#createDefaultSender");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **contentType** | **String**|  | [optional] |
| **createDefaultSenderRequest** | [**CreateDefaultSenderRequest**](CreateDefaultSenderRequest.md)|  | [optional] |

### Return type

[**CreateDefaultSender**](CreateDefaultSender.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |
| **400** | Successful response |  -  |

<a id="createDeliveryIssue"></a>
# **createDeliveryIssue**
> CreateDeliveryIssue createDeliveryIssue(contentType, createDeliveryIssueRequest)

Create Delivery Issues

_Create delivery Issue_  Create delivery Issue  ### Properties  | Name | Type | Required | Restrictions | Description | | --- | --- | --- | --- | --- | | message_id | string | false | none | The message id of the message. | | type | string | true | none | The type of message, must be one of the following values SMS, MMS, VOICE, EMAIL_MARKETING, EMAIL_TRANSACTIONAL, FAX, POST. | | description | string | true | none | The description of the message. | | client_comments | string | false | none | The user&#39;s comments. | | email-address | string | true | none | The user&#39;s email address. |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String contentType = "application/json"; // String | 
    CreateDeliveryIssueRequest createDeliveryIssueRequest = new CreateDeliveryIssueRequest(); // CreateDeliveryIssueRequest | 
    try {
      CreateDeliveryIssue result = apiInstance.createDeliveryIssue(contentType, createDeliveryIssueRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#createDeliveryIssue");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **contentType** | **String**|  | [optional] |
| **createDeliveryIssueRequest** | [**CreateDeliveryIssueRequest**](CreateDeliveryIssueRequest.md)|  | [optional] |

### Return type

[**CreateDeliveryIssue**](CreateDeliveryIssue.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="createEmailDeliveryReceiptRule"></a>
# **createEmailDeliveryReceiptRule**
> CreateEmailDeliveryReceiptRule createEmailDeliveryReceiptRule(contentType, createSmsDeliveryReceiptRuleRequest)

Create Email Delivery Receipt Rule

_Create email delivery receipt automations_  Create email delivery receipt automations  ### Properties  | Name | Type | Required | Restrictions | Description | | --- | --- | --- | --- | --- | | rule_name | string | true | none | Rule Name. | | match_type | number | true | none | Match Type. 0&#x3D;All reports. | | action | string | true | none | Action to be taken (AUTO_REPLY, EMAIL_USER, EMAIL_FIXED, URL, SMS, POLL, GROUP_SMS, MOVE_CONTACT, CREATE_CONTACT, CREATE_CONTACT_PLUS_EMAIL, CREATE_CONTACT_PLUS_NAME_EMAIL CREATE_CONTACT_PLUS_NAME, SMPP, NONE). | | action_address | string | true | none | Action address. | | enabled | number | true | none | Enabled: Disabled&#x3D;0 or Enabled&#x3D;1. |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String contentType = "application/json"; // String | 
    CreateSmsDeliveryReceiptRuleRequest createSmsDeliveryReceiptRuleRequest = new CreateSmsDeliveryReceiptRuleRequest(); // CreateSmsDeliveryReceiptRuleRequest | 
    try {
      CreateEmailDeliveryReceiptRule result = apiInstance.createEmailDeliveryReceiptRule(contentType, createSmsDeliveryReceiptRuleRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#createEmailDeliveryReceiptRule");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **contentType** | **String**|  | [optional] |
| **createSmsDeliveryReceiptRuleRequest** | [**CreateSmsDeliveryReceiptRuleRequest**](CreateSmsDeliveryReceiptRuleRequest.md)|  | [optional] |

### Return type

[**CreateEmailDeliveryReceiptRule**](CreateEmailDeliveryReceiptRule.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="createEmailTemplate"></a>
# **createEmailTemplate**
> CreateEmailTemplate createEmailTemplate(contentType, createEmailTemplateRequest)

Create Email Template

_Create email template_  Create email template  ### Properties  | Name | Type | Required | Restrictions | Description | | --- | --- | --- | --- | --- | | template_name | string | true | none | The intended name for the new template. | | template_id_master | number | true | none | The ID of the master template you want to base on. |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String contentType = "application/json"; // String | 
    CreateEmailTemplateRequest createEmailTemplateRequest = new CreateEmailTemplateRequest(); // CreateEmailTemplateRequest | 
    try {
      CreateEmailTemplate result = apiInstance.createEmailTemplate(contentType, createEmailTemplateRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#createEmailTemplate");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **contentType** | **String**|  | [optional] |
| **createEmailTemplateRequest** | [**CreateEmailTemplateRequest**](CreateEmailTemplateRequest.md)|  | [optional] |

### Return type

[**CreateEmailTemplate**](CreateEmailTemplate.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="createFaxDeliveryReceiptRule"></a>
# **createFaxDeliveryReceiptRule**
> CreateFaxDeliveryReceiptRule createFaxDeliveryReceiptRule(contentType, createFaxDeliveryReceiptRuleRequest)

Create FAX Delivery Receipt Rule

_Create fax delivery receipt automations_  Create fax delivery receipt automations  ### Properties  | Name | Type | Required | Restrictions | Description | | --- | --- | --- | --- | --- | | rule_name | string | true | none | Rule Name. | | match_type | number | true | none | Match Type. 0&#x3D;All reports. | | action | string | true | none | Action to be taken (AUTO_REPLY, EMAIL_USER, EMAIL_FIXED, URL, SMS, POLL, GROUP_SMS, MOVE_CONTACT, CREATE_CONTACT, CREATE_CONTACT_PLUS_EMAIL, CREATE_CONTACT_PLUS_NAME_EMAIL CREATE_CONTACT_PLUS_NAME, SMPP, NONE). | | action_address | string | true | none | Action address. | | enabled | number | true | none | Enabled: Disabled&#x3D;0 or Enabled&#x3D;1. |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String contentType = "application/json"; // String | 
    CreateFaxDeliveryReceiptRuleRequest createFaxDeliveryReceiptRuleRequest = new CreateFaxDeliveryReceiptRuleRequest(); // CreateFaxDeliveryReceiptRuleRequest | 
    try {
      CreateFaxDeliveryReceiptRule result = apiInstance.createFaxDeliveryReceiptRule(contentType, createFaxDeliveryReceiptRuleRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#createFaxDeliveryReceiptRule");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **contentType** | **String**|  | [optional] |
| **createFaxDeliveryReceiptRuleRequest** | [**CreateFaxDeliveryReceiptRuleRequest**](CreateFaxDeliveryReceiptRuleRequest.md)|  | [optional] |

### Return type

[**CreateFaxDeliveryReceiptRule**](CreateFaxDeliveryReceiptRule.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="createFaxInboundRule"></a>
# **createFaxInboundRule**
> CreateFaxInboundRule createFaxInboundRule(contentType, createFaxInboundRuleRequest)

Create Fax Inbound Rule

_Create new inbound fax automation_  Create new inbound fax automation  ### Properties  | Name | Type | Required | Restrictions | Description | | --- | --- | --- | --- | --- | | dedicated_number | string | true | none | Dedicated Number. Can be &#39;\\*&#39; to apply to all numbers. | | rule_name | string | true | none | Rule Name. | | action | string | true | none | Action to be taken (AUTO_REPLY, EMAIL_USER, EMAIL_FIXED, URL, SMS, POLL, GROUP_SMS, MOVE_CONTACT, CREATE_CONTACT, CREATE_CONTACT_PLUS_EMAIL, CREATE_CONTACT_PLUS_NAME_EMAIL CREATE_CONTACT_PLUS_NAME, SMPP, NONE). | | action_address | string | true | none | Action address. | | enabled | number | true | none | Enabled: Disabled&#x3D;0 or Enabled&#x3D;1. |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String contentType = "application/json"; // String | 
    CreateFaxInboundRuleRequest createFaxInboundRuleRequest = new CreateFaxInboundRuleRequest(); // CreateFaxInboundRuleRequest | 
    try {
      CreateFaxInboundRule result = apiInstance.createFaxInboundRule(contentType, createFaxInboundRuleRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#createFaxInboundRule");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **contentType** | **String**|  | [optional] |
| **createFaxInboundRuleRequest** | [**CreateFaxInboundRuleRequest**](CreateFaxInboundRuleRequest.md)|  | [optional] |

### Return type

[**CreateFaxInboundRule**](CreateFaxInboundRule.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="createList"></a>
# **createList**
> CreateList createList(contentType, createListRequest)

Create List

_Create new contact list_  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | list_name | body | string | true | Your contact list name |  Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.  &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String contentType = "application/json"; // String | 
    CreateListRequest createListRequest = new CreateListRequest(); // CreateListRequest | 
    try {
      CreateList result = apiInstance.createList(contentType, createListRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#createList");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **contentType** | **String**|  | [optional] |
| **createListRequest** | [**CreateListRequest**](CreateListRequest.md)|  | [optional] |

### Return type

[**CreateList**](CreateList.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="createNewContact"></a>
# **createNewContact**
> CreateNewContact createNewContact(listId, contentType, createNewContactRequest)

Create New Contact

_Create new contact_  ### parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | list_id | path | integer(int32) | true | List id | | page | query | integer(int32) | false | [Page number](/#pagination) | | limit | query | integer(int32) | false | [Number of records per page](/#pagination) |   ### Properties  | Name | Type | Required | Restrictions | Description | | --- | --- | --- | --- | --- | | phone_number | string | true | none | Your phone number in\\_[E.164](https://en.wikipedia.org/wiki/E.164)\\_format. Must be provided if no fax number or email. | | email | string | false | none | Your email. Must be provided if no phone number or fax number. | | fax_number | string | false | none | Your fax number. Must be provided if no phone number or email. | | first_name | string | false | none | Your first name. | | address_line_1 | string | false | none | Your street address | | address_line_2 | string | false | none | none | | address_city | string | false | none | Your nearest city | | address_state | string | false | none | Your current state | | address_postal_code | string | false | none | Your current postcode | | address_country | string | false | none | Your current country | | organization_name | string | false | none | Your organisation name | | custom_1 | string | true | none | none | | custom_2 | string | false | none | none | | custom_3 | string | false | none | none | | custom_4 | string | false | none | none | | last_name | string | false | none | Your last name |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String listId = "listId_example"; // String | 
    String contentType = "application/json"; // String | 
    CreateNewContactRequest createNewContactRequest = new CreateNewContactRequest(); // CreateNewContactRequest | 
    try {
      CreateNewContact result = apiInstance.createNewContact(listId, contentType, createNewContactRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#createNewContact");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **listId** | **String**|  | |
| **contentType** | **String**|  | [optional] |
| **createNewContactRequest** | [**CreateNewContactRequest**](CreateNewContactRequest.md)|  | [optional] |

### Return type

[**CreateNewContact**](CreateNewContact.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="createResellerAccount"></a>
# **createResellerAccount**
> CreateResellerAccount createResellerAccount(contentType, createResellerAccountRequest)

Create Reseller Account

_Create reseller account_  ### Properties  | Name | Type | Required | Restrictions | Description | | --- | --- | --- | --- | --- | | username | string | true | none | Account username | | password | string | true | none | Account password (unhashed) | | user_email | string | true | none | Account email | | user_phone | string | true | none | Account phone number | | user_first_name | string | true | none | Account owner first name | | user_last_name | string | true | none | Account owner last name | | account_name | string | true | none | Account name (usually company name) | | country | string | true | none | Country of account holder |  Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String contentType = "application/json"; // String | 
    CreateResellerAccountRequest createResellerAccountRequest = new CreateResellerAccountRequest(); // CreateResellerAccountRequest | 
    try {
      CreateResellerAccount result = apiInstance.createResellerAccount(contentType, createResellerAccountRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#createResellerAccount");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **contentType** | **String**|  | [optional] |
| **createResellerAccountRequest** | [**CreateResellerAccountRequest**](CreateResellerAccountRequest.md)|  | [optional] |

### Return type

[**CreateResellerAccount**](CreateResellerAccount.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="createReturnAddress"></a>
# **createReturnAddress**
> CreateReturnAddress createReturnAddress(contentType, createReturnAddressRequest)

Create Return Address

_Create post return address_  ### Properties  | Name | Type | Required | Restrictions | Description | | --- | --- | --- | --- | --- | | address_name | string | true | none | Your address name. | | address_line_1 | string | true | none | Your address line 1 | | address_city | string | true | none | Your city | | address_postal_code | string | true | none | Your postal code | | address_country | string | true | none | Your country | | address_line_2 | string | false | none | Your address line 2 | | address_state | string | false | none | Your state |    Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.    &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String contentType = "application/json"; // String | 
    CreateReturnAddressRequest createReturnAddressRequest = new CreateReturnAddressRequest(); // CreateReturnAddressRequest | 
    try {
      CreateReturnAddress result = apiInstance.createReturnAddress(contentType, createReturnAddressRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#createReturnAddress");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **contentType** | **String**|  | [optional] |
| **createReturnAddressRequest** | [**CreateReturnAddressRequest**](CreateReturnAddressRequest.md)|  | [optional] |

### Return type

[**CreateReturnAddress**](CreateReturnAddress.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="createSmsDeliveryReceiptRule"></a>
# **createSmsDeliveryReceiptRule**
> CreateSmsDeliveryReceiptRule createSmsDeliveryReceiptRule(contentType, createSmsDeliveryReceiptRuleRequest)

Create SMS Delivery Receipt Rule

_Create sms delivery receipt automations_  Create sms delivery receipt automations  ### Properties  | Name | Type | Required | Restrictions | Description | | --- | --- | --- | --- | --- | | rule_name | string | true | none | Rule Name. | | match_type | number | true | none | Match Type. 0&#x3D;All reports. | | action | string | true | none | Action to be taken (AUTO_REPLY, EMAIL_USER, EMAIL_FIXED, URL, SMS, POLL, GROUP_SMS, MOVE_CONTACT, CREATE_CONTACT, CREATE_CONTACT_PLUS_EMAIL, CREATE_CONTACT_PLUS_NAME_EMAIL CREATE_CONTACT_PLUS_NAME, SMPP, NONE). | | action_address | string | true | none | Action address. | | enabled | number | true | none | Enabled: Disabled&#x3D;0 or Enabled&#x3D;1. |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String contentType = "application/json"; // String | 
    CreateSmsDeliveryReceiptRuleRequest createSmsDeliveryReceiptRuleRequest = new CreateSmsDeliveryReceiptRuleRequest(); // CreateSmsDeliveryReceiptRuleRequest | 
    try {
      CreateSmsDeliveryReceiptRule result = apiInstance.createSmsDeliveryReceiptRule(contentType, createSmsDeliveryReceiptRuleRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#createSmsDeliveryReceiptRule");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **contentType** | **String**|  | [optional] |
| **createSmsDeliveryReceiptRuleRequest** | [**CreateSmsDeliveryReceiptRuleRequest**](CreateSmsDeliveryReceiptRuleRequest.md)|  | [optional] |

### Return type

[**CreateSmsDeliveryReceiptRule**](CreateSmsDeliveryReceiptRule.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="createSmsInboundAutomation"></a>
# **createSmsInboundAutomation**
> CreateSmsInboundAutomation createSmsInboundAutomation(contentType, createSmsInboundAutomationRequest)

Create SMS Inbound Automation

_Create new inbound sms automation_  Create new inbound sms automation  | Name | Type | Required | Restrictions | Description | | --- | --- | --- | --- | --- | | dedicated_number | string | true | none | Decicated Number. Can be &#39;\\*&#39; to apply to all numbers. | | rule_name | string | true | none | Rule Name. | | message_search_type | number | true | none | Message Search Type: 0&#x3D;Any message, 1&#x3D;starts with, 2&#x3D;contains, 3&#x3D;does not contain. | | message_search_term | string | true | none | Message search term. | | action | string | true | none | Action to be taken (AUTO_REPLY, EMAIL_USER, EMAIL_FIXED, URL, SMS, POLL, GROUP_SMS, MOVE_CONTACT, CREATE_CONTACT, CREATE_CONTACT_PLUS_EMAIL, CREATE_CONTACT_PLUS_NAME_EMAIL CREATE_CONTACT_PLUS_NAME, SMPP, NONE). | | action_address | string | true | none | Action address. | | enabled | number | true | none | Enabled: Disabled&#x3D;0 or Enabled&#x3D;1. | | webhook_type | string | false | Required when action &#x3D; URL only | Set as post, get, or json to change the format of the request sent. |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String contentType = "application/json"; // String | 
    CreateSmsInboundAutomationRequest createSmsInboundAutomationRequest = new CreateSmsInboundAutomationRequest(); // CreateSmsInboundAutomationRequest | 
    try {
      CreateSmsInboundAutomation result = apiInstance.createSmsInboundAutomation(contentType, createSmsInboundAutomationRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#createSmsInboundAutomation");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **contentType** | **String**|  | [optional] |
| **createSmsInboundAutomationRequest** | [**CreateSmsInboundAutomationRequest**](CreateSmsInboundAutomationRequest.md)|  | [optional] |

### Return type

[**CreateSmsInboundAutomation**](CreateSmsInboundAutomation.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="createSmsTemplate"></a>
# **createSmsTemplate**
> CreateSmsTemplate createSmsTemplate(contentType, createSmsTemplateRequest)

Create SMS Template

Use this endpoint to create a SMS template that you can use for sending SMS.

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String contentType = "application/json"; // String | 
    CreateSmsTemplateRequest createSmsTemplateRequest = new CreateSmsTemplateRequest(); // CreateSmsTemplateRequest | 
    try {
      CreateSmsTemplate result = apiInstance.createSmsTemplate(contentType, createSmsTemplateRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#createSmsTemplate");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **contentType** | **String**|  | [optional] |
| **createSmsTemplateRequest** | [**CreateSmsTemplateRequest**](CreateSmsTemplateRequest.md)|  | [optional] |

### Return type

[**CreateSmsTemplate**](CreateSmsTemplate.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="createStrippedStringRule"></a>
# **createStrippedStringRule**
> CreateStrippedStringRule createStrippedStringRule(contentType, createStrippedStringRuleRequest)

Create Stripped String Rule

_Create email to sms stripped string rule_  Create email to sms stripped string rules  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | stripped-string | body | string | true | String to be stripped. |  Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.  &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String contentType = "application/json"; // String | 
    CreateStrippedStringRuleRequest createStrippedStringRuleRequest = new CreateStrippedStringRuleRequest(); // CreateStrippedStringRuleRequest | 
    try {
      CreateStrippedStringRule result = apiInstance.createStrippedStringRule(contentType, createStrippedStringRuleRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#createStrippedStringRule");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **contentType** | **String**|  | [optional] |
| **createStrippedStringRuleRequest** | [**CreateStrippedStringRuleRequest**](CreateStrippedStringRuleRequest.md)|  | [optional] |

### Return type

[**CreateStrippedStringRule**](CreateStrippedStringRule.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="createSubaccount"></a>
# **createSubaccount**
> CreateSubaccount createSubaccount(contentType, createSubaccountRequest)

Create Subaccount

_Create new subaccount_  ### Properties  | Name | Type | Required | Restrictions | Description | | --- | --- | --- | --- | --- | | api_username | string | true | none | Your new api username. | | password | string | true | none | Your new password | | email | string | true | none | Your new email. | | phone_number | string | true | none | Your phone number in [E.164](https://en.wikipedia.org/wiki/E.164) format. | | first_name | string | true | none | Your firstname | | last_name | string | true | none | Your lastname | | access_users | integer(int1) | false | none | Flag value must be 1 for yes or 0 for no. | | access_billing | integer(int1) | false | none | Flag value must be 1 for yes or 0 for no. | | access_reporting | integer(int1) | false | none | Flag value must be 1 for yes or 0 for no. | | access_contacts | integer(int1) | false | none | Flag value must be 1 for yes or 0 for no. | | access_settings | integer(int1) | false | none | Flag value must be 1 for yes or 0 for no. |  Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.  &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String contentType = "application/json"; // String | 
    CreateSubaccountRequest createSubaccountRequest = new CreateSubaccountRequest(); // CreateSubaccountRequest | 
    try {
      CreateSubaccount result = apiInstance.createSubaccount(contentType, createSubaccountRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#createSubaccount");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **contentType** | **String**|  | [optional] |
| **createSubaccountRequest** | [**CreateSubaccountRequest**](CreateSubaccountRequest.md)|  | [optional] |

### Return type

[**CreateSubaccount**](CreateSubaccount.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="createTestInboundSms"></a>
# **createTestInboundSms**
> CreateTestInboundSms createTestInboundSms(contentType, createTestInboundSmsRequest)

Create Test Inbound SMS

Use this endpoint to generate and send a test &lt;a href&#x3D;\&quot;https://help.clicksend.com/article/ik4hw5xu35-can-i-receive-inbound-sms-to-my-url\&quot; target&#x3D;\&quot;_blank\&quot;&gt;inbound SMS&lt;/a&gt; to your webhook URL. Inbound SMS are messages sent by your recipient to you.  This test endpoint allows you to verify that the inbound SMS is correctly sent to your webhook URL.

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String contentType = "application/json"; // String | 
    CreateTestInboundSmsRequest createTestInboundSmsRequest = new CreateTestInboundSmsRequest(); // CreateTestInboundSmsRequest | 
    try {
      CreateTestInboundSms result = apiInstance.createTestInboundSms(contentType, createTestInboundSmsRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#createTestInboundSms");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **contentType** | **String**|  | [optional] |
| **createTestInboundSmsRequest** | [**CreateTestInboundSmsRequest**](CreateTestInboundSmsRequest.md)|  | [optional] |

### Return type

[**CreateTestInboundSms**](CreateTestInboundSms.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="createTestSmsReceipt"></a>
# **createTestSmsReceipt**
> CreateTestSmsReceipt createTestSmsReceipt(contentType, createTestSmsReceiptRequest)

Create Test SMS Receipt

Use this endpoint to generate and send a test &lt;a href&#x3D;\&quot;https://help.clicksend.com/article/49eq1qdcui-how-do-i-receive-sms-delivery-receipts-delivery-status-updates\&quot; target&#x3D;\&quot;_blank\&quot;&gt;SMS delivery receipt&lt;/a&gt; to your webhook URL. When you send an SMS, a delivery receipt is generated and can be received at your webhook URL. This test endpoint allows you to verify that the receipt is correctly sent to your webhook URL.  Additionally, you can obtain SMS receipts by setting the webhook URL to **poll** and periodically calling the **View SMS Receipt** endpoint to check for new receipts. This process is known as _polling_.

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String contentType = "application/json"; // String | 
    CreateTestSmsReceiptRequest createTestSmsReceiptRequest = new CreateTestSmsReceiptRequest(); // CreateTestSmsReceiptRequest | 
    try {
      CreateTestSmsReceipt result = apiInstance.createTestSmsReceipt(contentType, createTestSmsReceiptRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#createTestSmsReceipt");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **contentType** | **String**|  | [optional] |
| **createTestSmsReceiptRequest** | [**CreateTestSmsReceiptRequest**](CreateTestSmsReceiptRequest.md)|  | [optional] |

### Return type

[**CreateTestSmsReceipt**](CreateTestSmsReceipt.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="createVoiceDeliveryReceiptRule"></a>
# **createVoiceDeliveryReceiptRule**
> CreateVoiceDeliveryReceiptRule createVoiceDeliveryReceiptRule(contentType, createSmsDeliveryReceiptRuleRequest)

Create Voice Delivery Receipt Rule

_Create voice delivery receipt automations_  Create voice delivery receipt automations  ### Properties  | Name | Type | Required | Restrictions | Description | | --- | --- | --- | --- | --- | | rule_name | string | true | none | Rule Name. | | match_type | number | true | none | Match Type. 0&#x3D;All reports. | | action | string | true | none | Action to be taken (AUTO_REPLY, EMAIL_USER, EMAIL_FIXED, URL, SMS, POLL, GROUP_SMS, MOVE_CONTACT, CREATE_CONTACT, CREATE_CONTACT_PLUS_EMAIL, CREATE_CONTACT_PLUS_NAME_EMAIL CREATE_CONTACT_PLUS_NAME, SMPP, NONE). | | action_address | string | true | none | Action address. | | enabled | number | true | none | Enabled: Disabled&#x3D;0 or Enabled&#x3D;1. |  Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.  &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String contentType = "application/json"; // String | 
    CreateSmsDeliveryReceiptRuleRequest createSmsDeliveryReceiptRuleRequest = new CreateSmsDeliveryReceiptRuleRequest(); // CreateSmsDeliveryReceiptRuleRequest | 
    try {
      CreateVoiceDeliveryReceiptRule result = apiInstance.createVoiceDeliveryReceiptRule(contentType, createSmsDeliveryReceiptRuleRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#createVoiceDeliveryReceiptRule");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **contentType** | **String**|  | [optional] |
| **createSmsDeliveryReceiptRuleRequest** | [**CreateSmsDeliveryReceiptRuleRequest**](CreateSmsDeliveryReceiptRuleRequest.md)|  | [optional] |

### Return type

[**CreateVoiceDeliveryReceiptRule**](CreateVoiceDeliveryReceiptRule.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="currentPaymentInfo"></a>
# **currentPaymentInfo**
> CurrentPaymentInfo currentPaymentInfo(contentType)

Current Payment Info

_Get current payment info_  This endpoint returns your current payment info, we do not store credit card numbers, only a card token for security reasons.  Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String contentType = "application/json"; // String | 
    try {
      CurrentPaymentInfo result = apiInstance.currentPaymentInfo(contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#currentPaymentInfo");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **contentType** | **String**|  | [optional] |

### Return type

[**CurrentPaymentInfo**](CurrentPaymentInfo.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="deleteAllowedEmailAddress"></a>
# **deleteAllowedEmailAddress**
> DeleteAllowedEmailAddress deleteAllowedEmailAddress(emailAddressId, contentType)

Delete Allowed Email Address

_Delete specific email address_  Delete specific email address  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | email_address_id | path | integer(int32) | true | Allowed email address id |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String emailAddressId = "emailAddressId_example"; // String | 
    String contentType = "application/json"; // String | 
    try {
      DeleteAllowedEmailAddress result = apiInstance.deleteAllowedEmailAddress(emailAddressId, contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#deleteAllowedEmailAddress");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **emailAddressId** | **String**|  | |
| **contentType** | **String**|  | [optional] |

### Return type

[**DeleteAllowedEmailAddress**](DeleteAllowedEmailAddress.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="deleteAlphaTag"></a>
# **deleteAlphaTag**
> deleteAlphaTag(alphaTagId, contentType)

Delete Alpha Tag

_Delete a specific alpha tag._  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | alpha_tag_id | path | uuid | true | ID of the alpha tag |  Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.  This endpoint requires authentication, [more info...](/#authentication)

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String alphaTagId = "alphaTagId_example"; // String | 
    String contentType = "application/json"; // String | 
    try {
      apiInstance.deleteAlphaTag(alphaTagId, contentType);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#deleteAlphaTag");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **alphaTagId** | **String**|  | |
| **contentType** | **String**|  | [optional] |

### Return type

null (empty response body)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="deleteContact"></a>
# **deleteContact**
> DeleteContact deleteContact(listId, contactId, contentType)

Delete Contact

_Delete a contact_  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | list_id | path | integer(int32) | true | List ID | | contact_id | path | integer(int32) | true | Contact ID |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String listId = "listId_example"; // String | 
    String contactId = "contactId_example"; // String | 
    String contentType = "application/json"; // String | 
    try {
      DeleteContact result = apiInstance.deleteContact(listId, contactId, contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#deleteContact");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **listId** | **String**|  | |
| **contactId** | **String**|  | |
| **contentType** | **String**|  | [optional] |

### Return type

[**DeleteContact**](DeleteContact.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="deleteDefaultSender"></a>
# **deleteDefaultSender**
> deleteDefaultSender(defaultSenderId, contentType)

Delete Default Sender

Removes a specified default sender setting.  If you don&#39;t configure a default sender and leave the &#x60;sender_id&#x60; string blank when sending an SMS, Smart Assign will pick the best suitable, compliant, available SenderID for you.

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String defaultSenderId = "defaultSenderId_example"; // String | The ID of the default sender to delete
    String contentType = "application/json"; // String | 
    try {
      apiInstance.deleteDefaultSender(defaultSenderId, contentType);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#deleteDefaultSender");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **defaultSenderId** | **String**| The ID of the default sender to delete | |
| **contentType** | **String**|  | [optional] |

### Return type

null (empty response body)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **204** | Successful response (No Content) |  -  |

<a id="deleteEmailDeliveryReceiptRule"></a>
# **deleteEmailDeliveryReceiptRule**
> DeleteEmailDeliveryReceiptRule deleteEmailDeliveryReceiptRule(receiptRuleId, contentType)

Delete Email Delivery Receipt Rule

_Delete email delivery receipt automation_  Delete email delivery receipt automation  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | receipt_rule_id | path | integer(int32) | true | Receipt rule id |  Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.  This endpoint requires authentication, [more info...](/#authentication)   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String receiptRuleId = "receiptRuleId_example"; // String | 
    String contentType = "application/json"; // String | 
    try {
      DeleteEmailDeliveryReceiptRule result = apiInstance.deleteEmailDeliveryReceiptRule(receiptRuleId, contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#deleteEmailDeliveryReceiptRule");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **receiptRuleId** | **String**|  | |
| **contentType** | **String**|  | [optional] |

### Return type

[**DeleteEmailDeliveryReceiptRule**](DeleteEmailDeliveryReceiptRule.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="deleteEmailTemplate"></a>
# **deleteEmailTemplate**
> DeleteEmailTemplate deleteEmailTemplate(templateId, contentType)

Delete Email Template

_Delete user email template_  Delete user email template  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | template_id | path | integer(int32) | true | Email template id |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String templateId = "templateId_example"; // String | 
    String contentType = "application/json"; // String | 
    try {
      DeleteEmailTemplate result = apiInstance.deleteEmailTemplate(templateId, contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#deleteEmailTemplate");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **templateId** | **String**|  | |
| **contentType** | **String**|  | [optional] |

### Return type

[**DeleteEmailTemplate**](DeleteEmailTemplate.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="deleteFaxDeliveryReceiptRule"></a>
# **deleteFaxDeliveryReceiptRule**
> DeleteFaxDeliveryReceiptRule deleteFaxDeliveryReceiptRule(receiptRuleId, contentType)

Delete FAX Delivery Receipt Rule

_Delete fax delivery receipt automation_  Delete fax delivery receipt automation  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | receipt_rule_id | path | integer(int32) | true | Receipt rule id |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String receiptRuleId = "receiptRuleId_example"; // String | 
    String contentType = "application/json"; // String | 
    try {
      DeleteFaxDeliveryReceiptRule result = apiInstance.deleteFaxDeliveryReceiptRule(receiptRuleId, contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#deleteFaxDeliveryReceiptRule");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **receiptRuleId** | **String**|  | |
| **contentType** | **String**|  | [optional] |

### Return type

[**DeleteFaxDeliveryReceiptRule**](DeleteFaxDeliveryReceiptRule.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="deleteFaxInboundRule"></a>
# **deleteFaxInboundRule**
> DeleteFaxInboundRule deleteFaxInboundRule(inboundRuleId, contentType)

Delete Fax Inbound Rule

_Delete inbound fax automation_  Delete inbound fax automation  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | inbound_rule_id | path | integer(int32) | true | Inbound rule id |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String inboundRuleId = "inboundRuleId_example"; // String | 
    String contentType = "application/json"; // String | 
    try {
      DeleteFaxInboundRule result = apiInstance.deleteFaxInboundRule(inboundRuleId, contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#deleteFaxInboundRule");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **inboundRuleId** | **String**|  | |
| **contentType** | **String**|  | [optional] |

### Return type

[**DeleteFaxInboundRule**](DeleteFaxInboundRule.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="deleteList"></a>
# **deleteList**
> DeleteList deleteList(listId, contentType)

Delete List

_ListsByListIdDelete_  Delete a specific contact list  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | list_id | path | integer(int32) | true | List ID |  Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.  &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String listId = "listId_example"; // String | 
    String contentType = "application/json"; // String | 
    try {
      DeleteList result = apiInstance.deleteList(listId, contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#deleteList");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **listId** | **String**|  | |
| **contentType** | **String**|  | [optional] |

### Return type

[**DeleteList**](DeleteList.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="deleteOwnNumber"></a>
# **deleteOwnNumber**
> OwnNumber deleteOwnNumber(ownNumberId, contentType)

Delete Own Number

_Delete a specific own numbers._  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | own_number_id | path | uuid | true | ID of the own number |  Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.  This endpoint requires authentication, [more info...](/#authentication)

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String ownNumberId = "ownNumberId_example"; // String | 
    String contentType = "application/json"; // String | 
    try {
      OwnNumber result = apiInstance.deleteOwnNumber(ownNumberId, contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#deleteOwnNumber");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **ownNumberId** | **String**|  | |
| **contentType** | **String**|  | [optional] |

### Return type

[**OwnNumber**](OwnNumber.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="deleteReturnAddress"></a>
# **deleteReturnAddress**
> DeleteReturnAddress deleteReturnAddress(returnAddressId, contentType)

Delete Return Address

_Delete specific post return address_  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | return_address_id | path | integer(int32) | true | Return address ID |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String returnAddressId = "returnAddressId_example"; // String | 
    String contentType = "application/json"; // String | 
    try {
      DeleteReturnAddress result = apiInstance.deleteReturnAddress(returnAddressId, contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#deleteReturnAddress");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **returnAddressId** | **String**|  | |
| **contentType** | **String**|  | [optional] |

### Return type

[**DeleteReturnAddress**](DeleteReturnAddress.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="deleteSmsDeliveryReceiptRule"></a>
# **deleteSmsDeliveryReceiptRule**
> DeleteSmsDeliveryReceiptRule deleteSmsDeliveryReceiptRule(receiptRuleId, contentType)

Delete SMS Delivery Receipt Rule

_Delete sms delivery receipt automation_  Delete sms delivery receipt automation  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | receipt_rule_id | path | integer(int32) | true | Receipt rule id |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String receiptRuleId = "receiptRuleId_example"; // String | 
    String contentType = "application/json"; // String | 
    try {
      DeleteSmsDeliveryReceiptRule result = apiInstance.deleteSmsDeliveryReceiptRule(receiptRuleId, contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#deleteSmsDeliveryReceiptRule");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **receiptRuleId** | **String**|  | |
| **contentType** | **String**|  | [optional] |

### Return type

[**DeleteSmsDeliveryReceiptRule**](DeleteSmsDeliveryReceiptRule.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="deleteSmsInboundAutomation"></a>
# **deleteSmsInboundAutomation**
> DeleteSmsInboundAutomation deleteSmsInboundAutomation(inboundRuleId, contentType)

Delete SMS Inbound Automation

_Delete inbound sms automation_  Delete inbound sms automation  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | inbound_rule_id | path | integer(int32) | true | Inbound rule id |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String inboundRuleId = "inboundRuleId_example"; // String | 
    String contentType = "application/json"; // String | 
    try {
      DeleteSmsInboundAutomation result = apiInstance.deleteSmsInboundAutomation(inboundRuleId, contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#deleteSmsInboundAutomation");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **inboundRuleId** | **String**|  | |
| **contentType** | **String**|  | [optional] |

### Return type

[**DeleteSmsInboundAutomation**](DeleteSmsInboundAutomation.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="deleteSmsTemplate"></a>
# **deleteSmsTemplate**
> DeleteSmsTemplate deleteSmsTemplate(templateId, contentType)

Delete SMS Template

Use this endpoint to delete a &lt;a href&#x3D;\&quot;https://help.clicksend.com/article/9z9uloaz8y-sms-templates-for-different-industries\&quot; target&#x3D;\&quot;_blank\&quot;&gt;SMS template&lt;/a&gt;. Specify the SMS template to delete by providing its _template_id_.

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String templateId = "templateId_example"; // String | The ID of the template to delete.
    String contentType = "application/json"; // String | 
    try {
      DeleteSmsTemplate result = apiInstance.deleteSmsTemplate(templateId, contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#deleteSmsTemplate");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **templateId** | **String**| The ID of the template to delete. | |
| **contentType** | **String**|  | [optional] |

### Return type

[**DeleteSmsTemplate**](DeleteSmsTemplate.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="deleteStrippedStringRule"></a>
# **deleteStrippedStringRule**
> DeleteStrippedStringRule deleteStrippedStringRule(ruleId, contentType)

Delete Stripped String Rule

_Delete email to sms stripped string rule_  Delete email to sms stripped string rule  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | rule_id | path | integer(int32) | true | Your rule id |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String ruleId = "ruleId_example"; // String | 
    String contentType = "application/json"; // String | 
    try {
      DeleteStrippedStringRule result = apiInstance.deleteStrippedStringRule(ruleId, contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#deleteStrippedStringRule");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **ruleId** | **String**|  | |
| **contentType** | **String**|  | [optional] |

### Return type

[**DeleteStrippedStringRule**](DeleteStrippedStringRule.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="deleteSubaccount"></a>
# **deleteSubaccount**
> DeleteSubaccount deleteSubaccount(subaccountId, contentType)

Delete Subaccount

_Delete a subaccount_  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | subaccount_id | path | integer(int32) | true | ID of subaccount to delete |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String subaccountId = "subaccountId_example"; // String | 
    String contentType = "application/json"; // String | 
    try {
      DeleteSubaccount result = apiInstance.deleteSubaccount(subaccountId, contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#deleteSubaccount");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **subaccountId** | **String**|  | |
| **contentType** | **String**|  | [optional] |

### Return type

[**DeleteSubaccount**](DeleteSubaccount.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="deleteVoiceDeliveryReceiptRule"></a>
# **deleteVoiceDeliveryReceiptRule**
> DeleteVoiceDeliveryReceiptRule deleteVoiceDeliveryReceiptRule(receiptRuleId, contentType)

Delete Voice Delivery Receipt Rule

_Delete voice delivery receipt automation_  Delete voice delivery receipt automation  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | receipt_rule_id | path | integer(int32) | true | Receipt rule id |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String receiptRuleId = "receiptRuleId_example"; // String | 
    String contentType = "application/json"; // String | 
    try {
      DeleteVoiceDeliveryReceiptRule result = apiInstance.deleteVoiceDeliveryReceiptRule(receiptRuleId, contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#deleteVoiceDeliveryReceiptRule");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **receiptRuleId** | **String**|  | |
| **contentType** | **String**|  | [optional] |

### Return type

[**DeleteVoiceDeliveryReceiptRule**](DeleteVoiceDeliveryReceiptRule.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="detectAddress"></a>
# **detectAddress**
> DetectAddress detectAddress(contentType, body)

Detect Address

_Detects address in uploaded file._  The &#x60;detect-address&#x60; endpoint accepts either a letter in PDF format or an address string and attempts to convert it to a standard address format. Note that the PDF should be in standard address format, having the recipient&#39;s name and address listed at the top.  The endpoint accepts two types of data: 1. A PDF file in &#x60;base64&#x60; encoding. In this case, submit the &#x60;base64&#x60;\\-encoded PDF file contents in the &#x60;content&#x60; field of the request body. 2. An address string. In this case, submit the address in a string using the &#x60;address&#x60; field of the request body.  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | convert | query | string | true | none | | content | body | string | true | Base64-encoded file contents |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String contentType = "application/json"; // String | 
    Object body = null; // Object | 
    try {
      DetectAddress result = apiInstance.detectAddress(contentType, body);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#detectAddress");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **contentType** | **String**|  | [optional] |
| **body** | **Object**|  | [optional] |

### Return type

[**DetectAddress**](DetectAddress.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="exportEmailCampaignHistory"></a>
# **exportEmailCampaignHistory**
> exportEmailCampaignHistory(emailCampaignId, contentType)

Export Email Campaign History

_Export specific email campaign history_  Export specific email campaign history  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | email_campaign_id | path | integer(int32) | true | Allowed email campaign id | | date_from | query | integer(int32) | false | Start date (Unix Timestamp e.g. 1436849372) | | date_to | query | integer(int32) | false | End date (Unix Timestamp e.g. 1436879372) |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String emailCampaignId = "emailCampaignId_example"; // String | 
    String contentType = "application/json"; // String | 
    try {
      apiInstance.exportEmailCampaignHistory(emailCampaignId, contentType);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#exportEmailCampaignHistory");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **emailCampaignId** | **String**|  | |
| **contentType** | **String**|  | [optional] |

### Return type

null (empty response body)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="exportEmailHistory"></a>
# **exportEmailHistory**
> ExportEmailHistory exportEmailHistory(contentType)

Export Email History

_Export all Transactional Email history_  Export all Transactional Email history  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | filename | query | string | true | Filename to download history as | | date_from | query | integer(int32) | false | Start date (Unix Timestamp e.g. 1436849372) | | date_to | query | integer(int32) | false | End date (Unix Timestamp e.g. 1436879372) |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String contentType = "application/json"; // String | 
    try {
      ExportEmailHistory result = apiInstance.exportEmailHistory(contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#exportEmailHistory");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **contentType** | **String**|  | [optional] |

### Return type

[**ExportEmailHistory**](ExportEmailHistory.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="exportLetterHistory"></a>
# **exportLetterHistory**
> ExportLetterHistory exportLetterHistory(contentType, filename, q, orderBy, dateFrom, dateTo, limit)

Export Letter History

_export letter history_  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | filename | query | string | true | Filename to export to |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String contentType = "application/json"; // String | 
    String filename = "Post_history.csv"; // String | 
    String q = "q_example"; // String | 
    String orderBy = "date_added:desc"; // String | 
    String dateFrom = "dateFrom_example"; // String | 
    String dateTo = "dateTo_example"; // String | 
    Integer limit = 50000; // Integer | 
    try {
      ExportLetterHistory result = apiInstance.exportLetterHistory(contentType, filename, q, orderBy, dateFrom, dateTo, limit);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#exportLetterHistory");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **contentType** | **String**|  | [optional] |
| **filename** | **String**|  | [optional] |
| **q** | **String**|  | [optional] |
| **orderBy** | **String**|  | [optional] |
| **dateFrom** | **String**|  | [optional] |
| **dateTo** | **String**|  | [optional] |
| **limit** | **Integer**|  | [optional] |

### Return type

[**ExportLetterHistory**](ExportLetterHistory.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="exportMmsHistory"></a>
# **exportMmsHistory**
> ExportMmsHistory exportMmsHistory(contentType, filename, q, orderBy, dateFrom, dateTo, limit)

Export MMS History

_Export all mms history_  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | filename | query | string | true | Filename to download history as |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String contentType = "application/json"; // String | 
    String filename = "MMS_history.csv"; // String | 
    String q = "q_example"; // String | 
    String orderBy = "date_added:desc"; // String | 
    String dateFrom = "dateFrom_example"; // String | 
    String dateTo = "dateTo_example"; // String | 
    Integer limit = 50000; // Integer | 
    try {
      ExportMmsHistory result = apiInstance.exportMmsHistory(contentType, filename, q, orderBy, dateFrom, dateTo, limit);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#exportMmsHistory");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **contentType** | **String**|  | [optional] |
| **filename** | **String**|  | [optional] |
| **q** | **String**|  | [optional] |
| **orderBy** | **String**|  | [optional] |
| **dateFrom** | **String**|  | [optional] |
| **dateTo** | **String**|  | [optional] |
| **limit** | **Integer**|  | [optional] |

### Return type

[**ExportMmsHistory**](ExportMmsHistory.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="exportPostcardHistory"></a>
# **exportPostcardHistory**
> ExportPostcardHistory exportPostcardHistory(contentType)

Export Postcard History

_Export postcard history to a CSV file_  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | filename | query | string | true | Filename to export to |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String contentType = "application/json"; // String | 
    try {
      ExportPostcardHistory result = apiInstance.exportPostcardHistory(contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#exportPostcardHistory");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **contentType** | **String**|  | [optional] |

### Return type

[**ExportPostcardHistory**](ExportPostcardHistory.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="exportSmsHistory"></a>
# **exportSmsHistory**
> ExportSmsHistory exportSmsHistory(contentType, filename, page, limit, q, orderBy, dateFrom, dateTo)

Export SMS History

Use this endpoint to create a download link of your SMS history. You can filter the SMS history result using the query parameters.

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String contentType = "application/json"; // String | 
    String filename = "export.csv"; // String | The filename of the result. It should be in the .csv format.
    Integer page = 1; // Integer | The page number to retrieve. Use this parameter to navigate through the [pagination](/#pagination) results. The default value is 1.
    Integer limit = 15; // Integer | The number of items to return per page. This parameter controls the size of each page of results. The default value is 15.
    String q = "field_name"; // String | Allows filtering of results based on your search criteria. The query should be in the format `field_name:value`.  1. **Field Name**: The field within the SMS history you want to filter by. You can use the following fields:          - _Status_: The status of the SMS. Available values for status are: Queued, Completed, Scheduled, WaitApproval, Failed, Cancelled, CancelledAfterReview, Received, Sent.              - _To_: The recipient of the SMS.              - _from_: The sender of the SMS.              - _subaccount_id_: The sub-account identifier.              - _message_id_: The ID of your SMS.          2. **Value**: The text or keyword you're searching for within the specified field. If left empty after the colon, the filter will look for all templates with any value in the **Field Name**.             For example, if you are searching for a SMS with the status of _Scheduled_, the final query would look like this:    `q=status:Scheduled`  <div class=\"info-box\">   <h4><i class=\"fas fa-info-circle\"></i> Note:</h4>   <div>   <p>Some characters have to be encoded. For example, if you are searching for SMS sent from the phone number +61437085284, your search query q would be:<br/></p>     <ul>       <li>q=from:%2B61437085284</li>     </ul>     <p>You can use the <a href=\"https://www.urlencoder.org/\" target=\"_blank\">URL encoder</a> to encode the text. If a character is not an alphanumeric character (A-Z, a-z, 0-9), it is typically either reserved or unsafe and should be encoded.</p>   </div> </div>
    String orderBy = "date:asc"; // String | Specifies the field and order to sort the results by. The value is composed of the field name followed by a colon and the sort direction (asc for ascending or desc for descending).  The default sort order is by date in ascending order. You can use the following fields:    - _date_    - _username_   - _from_    - _to_   - _status_    - _body_  For example, if you want to order by the most recently sent SMS, you should sort by date in descending order. The query would look like this:    `order_by=date:desc`
    Integer dateFrom = 56; // Integer | Start date to filter results. It should be in <a href=\"http://help.clicksend.com/what-is-a-unix-timestamp\" target=\"_blank\">Unix format</a>.
    Integer dateTo = 56; // Integer | End date to filter results. It should be in <a href=\"http://help.clicksend.com/what-is-a-unix-timestamp\" target=\"_blank\">Unix format</a>.
    try {
      ExportSmsHistory result = apiInstance.exportSmsHistory(contentType, filename, page, limit, q, orderBy, dateFrom, dateTo);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#exportSmsHistory");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **contentType** | **String**|  | [optional] |
| **filename** | **String**| The filename of the result. It should be in the .csv format. | [optional] [default to export.csv] |
| **page** | **Integer**| The page number to retrieve. Use this parameter to navigate through the [pagination](/#pagination) results. The default value is 1. | [optional] [default to 1] |
| **limit** | **Integer**| The number of items to return per page. This parameter controls the size of each page of results. The default value is 15. | [optional] [default to 15] |
| **q** | **String**| Allows filtering of results based on your search criteria. The query should be in the format &#x60;field_name:value&#x60;.  1. **Field Name**: The field within the SMS history you want to filter by. You can use the following fields:          - _Status_: The status of the SMS. Available values for status are: Queued, Completed, Scheduled, WaitApproval, Failed, Cancelled, CancelledAfterReview, Received, Sent.              - _To_: The recipient of the SMS.              - _from_: The sender of the SMS.              - _subaccount_id_: The sub-account identifier.              - _message_id_: The ID of your SMS.          2. **Value**: The text or keyword you&#39;re searching for within the specified field. If left empty after the colon, the filter will look for all templates with any value in the **Field Name**.             For example, if you are searching for a SMS with the status of _Scheduled_, the final query would look like this:    &#x60;q&#x3D;status:Scheduled&#x60;  &lt;div class&#x3D;\&quot;info-box\&quot;&gt;   &lt;h4&gt;&lt;i class&#x3D;\&quot;fas fa-info-circle\&quot;&gt;&lt;/i&gt; Note:&lt;/h4&gt;   &lt;div&gt;   &lt;p&gt;Some characters have to be encoded. For example, if you are searching for SMS sent from the phone number +61437085284, your search query q would be:&lt;br/&gt;&lt;/p&gt;     &lt;ul&gt;       &lt;li&gt;q&#x3D;from:%2B61437085284&lt;/li&gt;     &lt;/ul&gt;     &lt;p&gt;You can use the &lt;a href&#x3D;\&quot;https://www.urlencoder.org/\&quot; target&#x3D;\&quot;_blank\&quot;&gt;URL encoder&lt;/a&gt; to encode the text. If a character is not an alphanumeric character (A-Z, a-z, 0-9), it is typically either reserved or unsafe and should be encoded.&lt;/p&gt;   &lt;/div&gt; &lt;/div&gt; | [optional] [default to field_name] |
| **orderBy** | **String**| Specifies the field and order to sort the results by. The value is composed of the field name followed by a colon and the sort direction (asc for ascending or desc for descending).  The default sort order is by date in ascending order. You can use the following fields:    - _date_    - _username_   - _from_    - _to_   - _status_    - _body_  For example, if you want to order by the most recently sent SMS, you should sort by date in descending order. The query would look like this:    &#x60;order_by&#x3D;date:desc&#x60; | [optional] [default to date:asc] |
| **dateFrom** | **Integer**| Start date to filter results. It should be in &lt;a href&#x3D;\&quot;http://help.clicksend.com/what-is-a-unix-timestamp\&quot; target&#x3D;\&quot;_blank\&quot;&gt;Unix format&lt;/a&gt;. | [optional] |
| **dateTo** | **Integer**| End date to filter results. It should be in &lt;a href&#x3D;\&quot;http://help.clicksend.com/what-is-a-unix-timestamp\&quot; target&#x3D;\&quot;_blank\&quot;&gt;Unix format&lt;/a&gt;. | [optional] |

### Return type

[**ExportSmsHistory**](ExportSmsHistory.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="exportVoiceHistory"></a>
# **exportVoiceHistory**
> ExportVoiceHistory exportVoiceHistory(contentType, filename, q, orderBy, dateFrom, dateTo, limit)

Export Voice History

_Export voice history_  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | filename | query | string | true | Filename to export to |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String contentType = "application/json"; // String | 
    String filename = "Voice_history.csv"; // String | 
    String q = "q_example"; // String | 
    String orderBy = "date_added:desc"; // String | 
    String dateFrom = "dateFrom_example"; // String | 
    String dateTo = "dateTo_example"; // String | 
    Integer limit = 50000; // Integer | 
    try {
      ExportVoiceHistory result = apiInstance.exportVoiceHistory(contentType, filename, q, orderBy, dateFrom, dateTo, limit);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#exportVoiceHistory");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **contentType** | **String**|  | [optional] |
| **filename** | **String**|  | [optional] |
| **q** | **String**|  | [optional] |
| **orderBy** | **String**|  | [optional] |
| **dateFrom** | **String**|  | [optional] |
| **dateTo** | **String**|  | [optional] |
| **limit** | **Integer**|  | [optional] |

### Return type

[**ExportVoiceHistory**](ExportVoiceHistory.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="forgotPassword"></a>
# **forgotPassword**
> ForgotPassword forgotPassword(contentType, forgotPasswordRequest)

Forgot Password

_Forgot password_  A user can send their username to this endpoint to be sent an email with their registered email address that will have a verification code.  Once you have this verification email containing the code you can send it to the [forgotten-password/verify](/#verify-forgot-password) endpoint along with a new password and the ID of that subaccount.  _Ask your administrator if you do not know your subaccount id._  ### Properties  | **Name** | **Type** | **Required** | **Restrictions** | **Description** | | --- | --- | --- | --- | --- | | username | string | true | none | Username belonging to account |  Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.  &lt;div style&#x3D;\&quot;background-color: #6BBD5B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint does not require authentication&lt;/span&gt;  &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String contentType = "application/json"; // String | 
    ForgotPasswordRequest forgotPasswordRequest = new ForgotPasswordRequest(); // ForgotPasswordRequest | 
    try {
      ForgotPassword result = apiInstance.forgotPassword(contentType, forgotPasswordRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#forgotPassword");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **contentType** | **String**|  | [optional] |
| **forgotPasswordRequest** | [**ForgotPasswordRequest**](ForgotPasswordRequest.md)|  | [optional] |

### Return type

[**ForgotPassword**](ForgotPassword.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="forgotUsername"></a>
# **forgotUsername**
> ForgotUsername forgotUsername(contentType, forgotUsernameRequest)

Forgot Username

_Forgot username_  Requires the user to pass either the email registered to an account or the phone number, **not** both  ### Properties  | **Name** | **Type** | **Required** | **Restrictions** | **Description** | | --- | --- | --- | --- | --- | | email | string | true | none | Email belonging to account | | phone_number | string | true | none | Phone belonging to account |  Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.  &lt;div style&#x3D;\&quot;background-color: #6BBD5B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint does not require authentication&lt;/span&gt;  &lt;/div&gt;   

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String contentType = "application/json"; // String | 
    ForgotUsernameRequest forgotUsernameRequest = new ForgotUsernameRequest(); // ForgotUsernameRequest | 
    try {
      ForgotUsername result = apiInstance.forgotUsername(contentType, forgotUsernameRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#forgotUsername");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **contentType** | **String**|  | [optional] |
| **forgotUsernameRequest** | [**ForgotUsernameRequest**](ForgotUsernameRequest.md)|  | [optional] |

### Return type

[**ForgotUsername**](ForgotUsername.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="generateNewApiKey"></a>
# **generateNewApiKey**
> GenerateNewApiKey generateNewApiKey(subaccountId, contentType, generateNewApiKeyRequest)

Generate New API Key

_Regenerate an API Key_  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | subaccount_id | path | integer(int32) | true | ID of subaccount to regenerate API key for |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String subaccountId = "subaccountId_example"; // String | 
    String contentType = "application/json"; // String | 
    GenerateNewApiKeyRequest generateNewApiKeyRequest = new GenerateNewApiKeyRequest(); // GenerateNewApiKeyRequest | 
    try {
      GenerateNewApiKey result = apiInstance.generateNewApiKey(subaccountId, contentType, generateNewApiKeyRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#generateNewApiKey");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **subaccountId** | **String**|  | |
| **contentType** | **String**|  | [optional] |
| **generateNewApiKeyRequest** | [**GenerateNewApiKeyRequest**](GenerateNewApiKeyRequest.md)|  | [optional] |

### Return type

[**GenerateNewApiKey**](GenerateNewApiKey.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="getAllDeliveryIssues"></a>
# **getAllDeliveryIssues**
> GetAllDeliveryIssues getAllDeliveryIssues(contentType)

Get All Delivery Issues

_Get all delivery issues_  Get all delivery issues  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | page | query | integer(int32) | false | Page number | | limit | query | integer(int32) | false | Number of records per page |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String contentType = "application/json"; // String | 
    try {
      GetAllDeliveryIssues result = apiInstance.getAllDeliveryIssues(contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#getAllDeliveryIssues");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **contentType** | **String**|  | [optional] |

### Return type

[**GetAllDeliveryIssues**](GetAllDeliveryIssues.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="getAlphaTag"></a>
# **getAlphaTag**
> AlphaTag getAlphaTag(alphaTagId, contentType)

Get Alpha Tag

_Get a specific alpha tag._  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | alpha_tag_id | path | uuid | true | ID of the alpha tag |  Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   This endpoint requires authentication, [more info...](/#authentication)

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String alphaTagId = "alphaTagId_example"; // String | 
    String contentType = "application/json"; // String | 
    try {
      AlphaTag result = apiInstance.getAlphaTag(alphaTagId, contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#getAlphaTag");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **alphaTagId** | **String**|  | |
| **contentType** | **String**|  | [optional] |

### Return type

[**AlphaTag**](AlphaTag.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="getCountriesForGlobalSending"></a>
# **getCountriesForGlobalSending**
> GetCountriesForGlobalSending getCountriesForGlobalSending()

Get Countries for Global Sending

_Get Countries for global sending_  Get the list of selected countries.  Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.  &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    try {
      GetCountriesForGlobalSending result = apiInstance.getCountriesForGlobalSending();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#getCountriesForGlobalSending");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**GetCountriesForGlobalSending**](GetCountriesForGlobalSending.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="getDefaultSenderDetails"></a>
# **getDefaultSenderDetails**
> GetDefaultSenderDetails getDefaultSenderDetails(defaultSenderId, contentType)

Get Default Sender Details

Retrieve detailed information about a specific default sender configuration

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String defaultSenderId = "defaultSenderId_example"; // String | The ID of the default sender to retrieve
    String contentType = "application/json"; // String | 
    try {
      GetDefaultSenderDetails result = apiInstance.getDefaultSenderDetails(defaultSenderId, contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#getDefaultSenderDetails");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **defaultSenderId** | **String**| The ID of the default sender to retrieve | |
| **contentType** | **String**|  | [optional] |

### Return type

[**GetDefaultSenderDetails**](GetDefaultSenderDetails.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="getDefaultSendersList"></a>
# **getDefaultSendersList**
> GetDefaultSendersList getDefaultSendersList(contentType, offset, perPage, sortBy, sortDirection)

Get List of Default Senders

Retrieve a list of default senders for the current user

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String contentType = "application/json"; // String | 
    String offset = "offset_example"; // String | Page (offset) to be used for pagination
    Integer perPage = 10; // Integer | Size of the page in pagination
    String sortBy = "created_timestamp"; // String | Parameter to sort the results by
    String sortDirection = "asc"; // String | Direction of sorting
    try {
      GetDefaultSendersList result = apiInstance.getDefaultSendersList(contentType, offset, perPage, sortBy, sortDirection);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#getDefaultSendersList");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **contentType** | **String**|  | [optional] |
| **offset** | **String**| Page (offset) to be used for pagination | [optional] |
| **perPage** | **Integer**| Size of the page in pagination | [optional] [default to 10] |
| **sortBy** | **String**| Parameter to sort the results by | [optional] [default to created_timestamp] |
| **sortDirection** | **String**| Direction of sorting | [optional] [default to desc] [enum: asc, desc] |

### Return type

[**GetDefaultSendersList**](GetDefaultSendersList.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="getOwnNumberDetail"></a>
# **getOwnNumberDetail**
> OwnNumber getOwnNumberDetail(ownNumberId, contentType)

Get Own Number Detail

_Get a specific own numbers._  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | own_number_id | path | uuid | true | ID of the own number |  Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.  This endpoint requires authentication, [more info...](/#authentication)

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String ownNumberId = "ownNumberId_example"; // String | 
    String contentType = "application/json"; // String | 
    try {
      OwnNumber result = apiInstance.getOwnNumberDetail(ownNumberId, contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#getOwnNumberDetail");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **ownNumberId** | **String**|  | |
| **contentType** | **String**|  | [optional] |

### Return type

[**OwnNumber**](OwnNumber.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="getSpecificContact"></a>
# **getSpecificContact**
> GetSpecificContact getSpecificContact(listId, contactId, contentType)

Get Specific Contact

_Get a specific contact_  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | list_id | path | integer(int32) | true | Your contact list id you want to access. | | contact_id | path | integer(int32) | true | Your contact id you want to access. |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String listId = "listId_example"; // String | 
    String contactId = "contactId_example"; // String | 
    String contentType = "application/json"; // String | 
    try {
      GetSpecificContact result = apiInstance.getSpecificContact(listId, contactId, contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#getSpecificContact");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **listId** | **String**|  | |
| **contactId** | **String**|  | |
| **contentType** | **String**|  | [optional] |

### Return type

[**GetSpecificContact**](GetSpecificContact.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="getVoiceHistory"></a>
# **getVoiceHistory**
> GetVoiceHistory getVoiceHistory(contentType, dateTo, limit, operator, orderBy, page)

Get Voice History

_Get all voice history_  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | date_from | query | integer(int32) | false | Start date (Unix Timestamp e.g. 1436849372) | | date_to | query | integer(int32) | false | End date (Unix Timestamp e.g. 1436879372) | | page | query | integer(int32) | false | [Page number](/#pagination) | | limit | query | integer(int32) | false | [Number of records per page](/#pagination) |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String contentType = "application/json"; // String | 
    String dateTo = "dateTo_example"; // String | 
    Integer limit = 20; // Integer | 
    String operator = "AND"; // String | 
    String orderBy = "date_added:desc"; // String | 
    Integer page = 1; // Integer | 
    try {
      GetVoiceHistory result = apiInstance.getVoiceHistory(contentType, dateTo, limit, operator, orderBy, page);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#getVoiceHistory");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **contentType** | **String**|  | [optional] |
| **dateTo** | **String**|  | [optional] |
| **limit** | **Integer**|  | [optional] |
| **operator** | **String**|  | [optional] |
| **orderBy** | **String**|  | [optional] |
| **page** | **Integer**|  | [optional] |

### Return type

[**GetVoiceHistory**](GetVoiceHistory.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="importContacts"></a>
# **importContacts**
> ImportContacts importContacts(listId, contentType, importContactsRequest)

Import Contacts

_Import contacts to list_  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | list_id | path | integer(int32) | true | Your contact list id you want to access. |  ### Properties  | Name | Type | Required | Restrictions | Description | | --- | --- | --- | --- | --- | | file_url | string | true | none | URL of file to process | | field_order | \\[string\\] | true | none | Order of fields in file |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String listId = "listId_example"; // String | 
    String contentType = "application/json"; // String | 
    ImportContactsRequest importContactsRequest = new ImportContactsRequest(); // ImportContactsRequest | 
    try {
      ImportContacts result = apiInstance.importContacts(listId, contentType, importContactsRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#importContacts");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **listId** | **String**|  | |
| **contentType** | **String**|  | [optional] |
| **importContactsRequest** | [**ImportContactsRequest**](ImportContactsRequest.md)|  | [optional] |

### Return type

[**ImportContacts**](ImportContacts.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="listAlphaTags"></a>
# **listAlphaTags**
> ListAlphaTags listAlphaTags(sortDirection, pageSize)

List Alpha Tags



### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String sortDirection = "asc"; // String | The sort direction for the results. The default value is asc.
    Integer pageSize = 10; // Integer | The number of items to return per page. This parameter controls the size of each page of results. The default value is 10.
    try {
      ListAlphaTags result = apiInstance.listAlphaTags(sortDirection, pageSize);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#listAlphaTags");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **sortDirection** | **String**| The sort direction for the results. The default value is asc. | [optional] [default to asc] [enum: asc, desc] |
| **pageSize** | **Integer**| The number of items to return per page. This parameter controls the size of each page of results. The default value is 10. | [optional] [default to 10] |

### Return type

[**ListAlphaTags**](ListAlphaTags.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="listCompliantSenderTypes"></a>
# **listCompliantSenderTypes**
> ListCompliantSenderTypes200Response listCompliantSenderTypes(filterProductType, filterCountryCodeLeftCurlyBracketIndexRightCurlyBracket)

List Compliant Sender Types

Retrieves the list of compliant sender types for specific countries

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String filterProductType = "SMS"; // String | Type of the product
    List<String> filterCountryCodeLeftCurlyBracketIndexRightCurlyBracket = Arrays.asList(); // List<String> | Array of recipient country codes (ISO 3166-1 alpha-2). If not specified, will get all compliant sender types for all countries. Replace `{index}` with the appropriate index value.  <small>Example:</small> <small><code style=\"color: #424242;\">filter[country_code][0]=US&filter[country_code][1]=AU</code></small> 
    try {
      ListCompliantSenderTypes200Response result = apiInstance.listCompliantSenderTypes(filterProductType, filterCountryCodeLeftCurlyBracketIndexRightCurlyBracket);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#listCompliantSenderTypes");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **filterProductType** | **String**| Type of the product | [enum: SMS] |
| **filterCountryCodeLeftCurlyBracketIndexRightCurlyBracket** | [**List&lt;String&gt;**](String.md)| Array of recipient country codes (ISO 3166-1 alpha-2). If not specified, will get all compliant sender types for all countries. Replace &#x60;{index}&#x60; with the appropriate index value.  &lt;small&gt;Example:&lt;/small&gt; &lt;small&gt;&lt;code style&#x3D;\&quot;color: #424242;\&quot;&gt;filter[country_code][0]&#x3D;US&amp;filter[country_code][1]&#x3D;AU&lt;/code&gt;&lt;/small&gt;  | [optional] |

### Return type

[**ListCompliantSenderTypes200Response**](ListCompliantSenderTypes200Response.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="listCountries"></a>
# **listCountries**
> ListCountries listCountries()

International Messaging

_List of countries_  List of countries with IDs that can be used in selecting countries for Global sending.  Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.  &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    try {
      ListCountries result = apiInstance.listCountries();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#listCountries");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**ListCountries**](ListCountries.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="listOwnNumbers"></a>
# **listOwnNumbers**
> ListOwnNumbers listOwnNumbers(contentType)

List Own Numbers

_List own numbers._  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | offset | query | uuid | false | Page(offset) to be used for pagination. Example: &#x60;offset&#x3D;f99872cc-11a6-48ba-a9f2-bcfb6dd1e3d4#8fa5ebc2-777b-45db-a448-ec76a40d4384&#x60; | | page_size | query | integer | false | Number of records per page. Default: 10. Range \\[1..500\\] | | filter\\[status\\]\\[\\] | query | string | false | Filter by statuses. Value must be in enum \\[&#x60;PENDING&#x60;, &#x60;APPROVED&#x60;, &#x60;REJECTED&#x60;\\]. For example: &#x60;filter[status][0]&#x3D;PENDING&amp;filter[status][1]&#x3D;APPROVED&#x60; . | | sort_by | query | string | false | Sort by parameter. Default: &#x60;created_timestamp&#x60; | | sort_direction | query | string | false | Direction of sorting. Default: &#x60;asc&#x60;. Value must be in enum \\[&#x60;asc&#x60;, &#x60;desc&#x60;\\]. |  Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   This endpoint requires authentication, [more info...](/#authentication)

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String contentType = "application/json"; // String | 
    try {
      ListOwnNumbers result = apiInstance.listOwnNumbers(contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#listOwnNumbers");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **contentType** | **String**|  | [optional] |

### Return type

[**ListOwnNumbers**](ListOwnNumbers.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="markInboundSmsAsRead"></a>
# **markInboundSmsAsRead**
> MarkInboundSmsAsRead markInboundSmsAsRead(contentType, markSmsReceiptAsReadRequest)

Mark Inbound SMS as Read

Use this endpoint to mark all &lt;a href&#x3D;\&quot;https://help.clicksend.com/article/ik4hw5xu35-can-i-receive-inbound-sms-to-my-url\&quot; target&#x3D;\&quot;_blank\&quot;&gt;inbound SMS&lt;/a&gt; as read. Inbound SMS that has been marked as read won’t be shown in the **View Inbound SMS** endpoint. You can still use the **View Specific Inbound SMS** endpoint to view inbound SMS marked as read.  In the request, you can optionally add a _date_before_ parameter to only mark inbound SMS sent before that date as read.

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String contentType = "application/json"; // String | 
    MarkSmsReceiptAsReadRequest markSmsReceiptAsReadRequest = new MarkSmsReceiptAsReadRequest(); // MarkSmsReceiptAsReadRequest | 
    try {
      MarkInboundSmsAsRead result = apiInstance.markInboundSmsAsRead(contentType, markSmsReceiptAsReadRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#markInboundSmsAsRead");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **contentType** | **String**|  | [optional] |
| **markSmsReceiptAsReadRequest** | [**MarkSmsReceiptAsReadRequest**](MarkSmsReceiptAsReadRequest.md)|  | [optional] |

### Return type

[**MarkInboundSmsAsRead**](MarkInboundSmsAsRead.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="markSmsReceiptAsRead"></a>
# **markSmsReceiptAsRead**
> MarkSmsReceiptAsRead markSmsReceiptAsRead(contentType, markSmsReceiptAsReadRequest)

Mark SMS Receipt As Read

Use this endpoint to mark all &lt;a target&#x3D;\&quot;_blank\&quot; href&#x3D;\&quot;https://help.clicksend.com/article/49eq1qdcui-how-do-i-receive-sms-delivery-receipts-delivery-status-updates\&quot;&gt;SMS delivery receipts&lt;/a&gt; as read. Delivery receipts that have been marked as read won’t be shown in the **View SMS Receipts** endpoint.  You can still use the **View Specific SMS Receipt** endpoint to view delivery receipts marked as read. In the request, you can optionally add a _date_before_ parameter to only mark receipts sent before that date as read

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String contentType = "application/json"; // String | 
    MarkSmsReceiptAsReadRequest markSmsReceiptAsReadRequest = new MarkSmsReceiptAsReadRequest(); // MarkSmsReceiptAsReadRequest | 
    try {
      MarkSmsReceiptAsRead result = apiInstance.markSmsReceiptAsRead(contentType, markSmsReceiptAsReadRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#markSmsReceiptAsRead");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **contentType** | **String**|  | [optional] |
| **markSmsReceiptAsReadRequest** | [**MarkSmsReceiptAsReadRequest**](MarkSmsReceiptAsReadRequest.md)|  | [optional] |

### Return type

[**MarkSmsReceiptAsRead**](MarkSmsReceiptAsRead.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="markSpecificInboundSmsMessageAsRead"></a>
# **markSpecificInboundSmsMessageAsRead**
> MarkSpecificInboundSmsMessageAsRead markSpecificInboundSmsMessageAsRead(messageId, contentType)

Mark Specific Inbound SMS Message As Read

Use this endpoint to mark a specific &lt;a href&#x3D;\&quot;https://help.clicksend.com/article/ik4hw5xu35-can-i-receive-inbound-sms-to-my-url\&quot; target&#x3D;\&quot;_blank\&quot;&gt;inbound SMS&lt;/a&gt; as read. Unlike the **View Inbound SMS** endpoint, which marks all inbound SMS as read,  this endpoint only marks one specified inbound SMS. Specify the SMS to be marked as read by providing its _message_id_.

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String messageId = "messageId_example"; // String | The message_id of the inbound SMS to mark as read.  <div class=\"info-box\">   <h4><i class=\"fas fa-info-circle\"></i> Note:</h4>   <p>     When you receive an inbound message, you will get two parameters: <em>original_message_id</em> and <em>message_id</em>:   </p>   <ul>     <li><em>original_message_id</em>: This is the ID of the outbound message sent to the recipient</li>     <li><em>message_id</em>: This is the ID of the inbound message sent by the recipient.</li>   </ul> </div>
    String contentType = "application/json"; // String | 
    try {
      MarkSpecificInboundSmsMessageAsRead result = apiInstance.markSpecificInboundSmsMessageAsRead(messageId, contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#markSpecificInboundSmsMessageAsRead");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **messageId** | **String**| The message_id of the inbound SMS to mark as read.  &lt;div class&#x3D;\&quot;info-box\&quot;&gt;   &lt;h4&gt;&lt;i class&#x3D;\&quot;fas fa-info-circle\&quot;&gt;&lt;/i&gt; Note:&lt;/h4&gt;   &lt;p&gt;     When you receive an inbound message, you will get two parameters: &lt;em&gt;original_message_id&lt;/em&gt; and &lt;em&gt;message_id&lt;/em&gt;:   &lt;/p&gt;   &lt;ul&gt;     &lt;li&gt;&lt;em&gt;original_message_id&lt;/em&gt;: This is the ID of the outbound message sent to the recipient&lt;/li&gt;     &lt;li&gt;&lt;em&gt;message_id&lt;/em&gt;: This is the ID of the inbound message sent by the recipient.&lt;/li&gt;   &lt;/ul&gt; &lt;/div&gt; | |
| **contentType** | **String**|  | [optional] |

### Return type

[**MarkSpecificInboundSmsMessageAsRead**](MarkSpecificInboundSmsMessageAsRead.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="purchaseDedicatedNumber"></a>
# **purchaseDedicatedNumber**
> PurchaseDedicatedNumber purchaseDedicatedNumber(dedicatedNumber, buyNumberRequest, contentType, type)

Purchase Dedicated Number

_Buy dedicated number_  This endpoint allows you to purchase a dedicated phone number for messaging services. You can optionally include registration data for compliance purposes.  ### Request Body  | Field | Type | Required | Description | | --- | --- | --- | --- | | dedicated_number | string | true | Phone number to purchase | | type | string | true | Service type (sms, mms) | | registration_data | object | false | Registration data for compliance (AU SMS/MMS numbers only) |  #### Registration Data Fields (Optional)  | Field | Type | Required | Description | | --- | --- | --- | --- | | business_name | string | true | Name of the business (2 - 100 characters) | | business_address | string | true | Business address (5 - 150 characters) | | suburb | string | true | Suburb/City (2 - 50 characters) | | postcode | string | true | Postal code (2 - 20 characters) | | state | string | true | State/Province (2 - 50 characters) | | contact_name | string | true | Contact person name (2 - 100 characters) | | contact_number | string | true | Contact phone number (valid local or international phone number) | | country | string | true | Country code (ISO 3166-1 alpha-2) |   ### Path Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | dedicated_number | path | string | true | Phone number to purchase |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String dedicatedNumber = "+614197651956"; // String | Phone number to purchase
    BuyNumberRequest buyNumberRequest = new BuyNumberRequest(); // BuyNumberRequest | 
    String contentType = "application/json"; // String | 
    String type = "sms"; // String | 
    try {
      PurchaseDedicatedNumber result = apiInstance.purchaseDedicatedNumber(dedicatedNumber, buyNumberRequest, contentType, type);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#purchaseDedicatedNumber");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **dedicatedNumber** | **String**| Phone number to purchase | |
| **buyNumberRequest** | [**BuyNumberRequest**](BuyNumberRequest.md)|  | |
| **contentType** | **String**|  | [optional] |
| **type** | **String**|  | [optional] |

### Return type

[**PurchaseDedicatedNumber**](PurchaseDedicatedNumber.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="purchaseRechargePackage"></a>
# **purchaseRechargePackage**
> PurchaseRechargePackage purchaseRechargePackage(packageId, contentType)

Purchase Recharge Package

_Purchase a package_  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | package_id | path | integer(int32) | true | ID of package to purchase |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String packageId = "packageId_example"; // String | 
    String contentType = "application/x-www-form-urlencoded"; // String | 
    try {
      PurchaseRechargePackage result = apiInstance.purchaseRechargePackage(packageId, contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#purchaseRechargePackage");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **packageId** | **String**|  | |
| **contentType** | **String**|  | [optional] |

### Return type

[**PurchaseRechargePackage**](PurchaseRechargePackage.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="registerNumbers"></a>
# **registerNumbers**
> RegisterNumbers registerNumbers(numberType, countryCode, contentType, registerNumbersRequest)

Register Numbers

&lt;div style&#x3D;\&quot;background-color: #e8f4ff; padding: 15px; border-radius: 4px; border-left: 4px solid #0066cc;\&quot;&gt; This endpoint is currently only available for &lt;b&gt;Canada 10DLC&lt;/b&gt; number registration. &lt;/div&gt;  Registers a number that requires additional verification information. This endpoint facilitates the registration process for numbers requiring special compliance documentation.  After submission, ClickSend&#39;s compliance team will review the registration and notify you of the approval status.  Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses. &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String numberType = "10dlc"; // String | The type of number being registered
    String countryCode = "US, CA"; // String | Two-character ISO country code
    String contentType = "application/json"; // String | 
    RegisterNumbersRequest registerNumbersRequest = new RegisterNumbersRequest(); // RegisterNumbersRequest | 
    try {
      RegisterNumbers result = apiInstance.registerNumbers(numberType, countryCode, contentType, registerNumbersRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#registerNumbers");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **numberType** | **String**| The type of number being registered | |
| **countryCode** | **String**| Two-character ISO country code | |
| **contentType** | **String**|  | [optional] |
| **registerNumbersRequest** | [**RegisterNumbersRequest**](RegisterNumbersRequest.md)|  | [optional] |

### Return type

[**RegisterNumbers**](RegisterNumbers.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |
| **400** | Bad request |  -  |

<a id="removeDuplicateContacts"></a>
# **removeDuplicateContacts**
> RemoveDuplicateContacts removeDuplicateContacts(listId, contentType, removeDuplicateContactsRequest)

Remove Duplicate Contacts

_Remove duplicate contacts_  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | list_id | path | integer(int32) | true | Your list id |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String listId = "listId_example"; // String | 
    String contentType = "application/json"; // String | 
    RemoveDuplicateContactsRequest removeDuplicateContactsRequest = new RemoveDuplicateContactsRequest(); // RemoveDuplicateContactsRequest | 
    try {
      RemoveDuplicateContacts result = apiInstance.removeDuplicateContacts(listId, contentType, removeDuplicateContactsRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#removeDuplicateContacts");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **listId** | **String**|  | |
| **contentType** | **String**|  | [optional] |
| **removeDuplicateContactsRequest** | [**RemoveDuplicateContactsRequest**](RemoveDuplicateContactsRequest.md)|  | [optional] |

### Return type

[**RemoveDuplicateContacts**](RemoveDuplicateContacts.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="removeOptedOutContacts"></a>
# **removeOptedOutContacts**
> RemoveOptedOutContacts removeOptedOutContacts(listId, optOutListId, contentType, body)

Remove Opted Out Contacts

_Remove all opted out contacts_  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | list_id | path | integer(int32) | true | Your list id | | opt_out_list_id | path | integer(int32) | true | Your opt out list id |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String listId = "listId_example"; // String | 
    String optOutListId = "optOutListId_example"; // String | 
    String contentType = "application/json"; // String | 
    Object body = null; // Object | 
    try {
      RemoveOptedOutContacts result = apiInstance.removeOptedOutContacts(listId, optOutListId, contentType, body);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#removeOptedOutContacts");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **listId** | **String**|  | |
| **optOutListId** | **String**|  | |
| **contentType** | **String**|  | [optional] |
| **body** | **Object**|  | [optional] |

### Return type

[**RemoveOptedOutContacts**](RemoveOptedOutContacts.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="requestAlphaTag"></a>
# **requestAlphaTag**
> AlphaTag requestAlphaTag(contentType, requestAlphaTagRequest)

Request Alpha Tag

_Request to register an alpha tag. After requested, the alpha tag will be reviewed by ClickSend and either approved or rejected. Some countries (e.g Australia) require you to submit additional fields due to government mandated compliance checks._  ### Properties  | Name | Type | Required | Restrictions | Description | | --- | --- | --- | --- | --- | | alpha_tag | string | true | [yes](https://help.clicksend.com/article/1qxfxkcwm2-global-generic-alpha-tags) | The alpha tag name. Length must be between 3 - 11 characters, can only contain a-z A-Z 0-9 + and must contain at least one non numeric. | | reason | string | false | none | Must be one of the following: &#x60;Sole Trader Name&#x60;, &#x60;Company Name&#x60;, &#x60;Partnership Name&#x60;, &#x60;Registered Trust Name&#x60;, &#x60;Co-Operative Name&#x60;, &#x60;Indigenous Corporation Name&#x60;, &#x60;Registered Organisation Name&#x60;, &#x60;Personal Name&#x60;, &#x60;Trademark&#x60;, &#x60;Government Agency or Entity&#x60;, &#x60;Product or Service Name&#x60;, &#x60;Acronym/Initialism&#x60;, &#x60;Contraction of Name&#x60;, &#x60;Third Party&#x60;. In case of &#x60;Third Party&#x60;, we will contact you to collect the relevant information. | | countries | array of strings | false | none | List of country codes (e.g., \&quot;AU\&quot;, \&quot;US\&quot;) where the alpha tag is requested. Only supported and required for AU. | | businesses | array of objects | false | none | List of business details required for alpha tag registration. Each object contains country, business information, ... Required if &#x60;countries&#x60; is provided. When &#x60;business_relationship&#x60; is &#x60;ENTITY_ASSOCIATE&#x60;, the following partner fields are also **required**: &#x60;partner_business_name&#x60;, &#x60;partner_abn&#x60;, &#x60;partner_business_info&#x60;, &#x60;partner_business_address&#x60;, &#x60;partner_representative&#x60;. These fields are **forbidden** for any other &#x60;business_relationship&#x60; value. |  Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.  _This endpoint requires authentication,_ [more info...](/#authentication) 

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String contentType = "application/json"; // String | 
    RequestAlphaTagRequest requestAlphaTagRequest = new RequestAlphaTagRequest(); // RequestAlphaTagRequest | 
    try {
      AlphaTag result = apiInstance.requestAlphaTag(contentType, requestAlphaTagRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#requestAlphaTag");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **contentType** | **String**|  | [optional] |
| **requestAlphaTagRequest** | [**RequestAlphaTagRequest**](RequestAlphaTagRequest.md)|  | [optional] |

### Return type

[**AlphaTag**](AlphaTag.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="requestOwnNumberVerificationOtp"></a>
# **requestOwnNumberVerificationOtp**
> RequestOwnNumberVerificationOtp requestOwnNumberVerificationOtp(contentType, requestOwnNumberVerificationOtpRequest)

Request Own Number Verification OTP

_Request to generate own number verification OTP_  ### Properties  | Name | Type | Required | Restrictions | Description | | --- | --- | --- | --- | --- | | label | string | false | none | Custom label for phone number. Length must be between 1 - 200 characters. | | phone_number | string | true | none | Phone number. | | country | string | false | none | Country code. |  Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.  This endpoint requires authentication, [more info...](/#authentication)

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String contentType = "application/json"; // String | 
    RequestOwnNumberVerificationOtpRequest requestOwnNumberVerificationOtpRequest = new RequestOwnNumberVerificationOtpRequest(); // RequestOwnNumberVerificationOtpRequest | 
    try {
      RequestOwnNumberVerificationOtp result = apiInstance.requestOwnNumberVerificationOtp(contentType, requestOwnNumberVerificationOtpRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#requestOwnNumberVerificationOtp");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **contentType** | **String**|  | [optional] |
| **requestOwnNumberVerificationOtpRequest** | [**RequestOwnNumberVerificationOtpRequest**](RequestOwnNumberVerificationOtpRequest.md)|  | [optional] |

### Return type

[**RequestOwnNumberVerificationOtp**](RequestOwnNumberVerificationOtp.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="resellerTransferCredit"></a>
# **resellerTransferCredit**
> ResellerTransferCredit resellerTransferCredit(contentType, updatePaymentInfoRequest)

Reseller Transfer Credit

_Transfer Credit_  ### Properties  | Name | Type | Required | Restrictions | Description | | --- | --- | --- | --- | --- | | client_user_id | integer(int32) | true | none | User ID of client | | balance | integer(int32) | true | none | Balance to transfer | | currency | string | true | none | Currency of balance to transfer |  Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.  &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String contentType = "application/x-www-form-urlencoded"; // String | 
    UpdatePaymentInfoRequest updatePaymentInfoRequest = new UpdatePaymentInfoRequest(); // UpdatePaymentInfoRequest | 
    try {
      ResellerTransferCredit result = apiInstance.resellerTransferCredit(contentType, updatePaymentInfoRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#resellerTransferCredit");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **contentType** | **String**|  | [optional] |
| **updatePaymentInfoRequest** | [**UpdatePaymentInfoRequest**](UpdatePaymentInfoRequest.md)|  | [optional] |

### Return type

[**ResellerTransferCredit**](ResellerTransferCredit.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="selectCountriesForGlobalSending"></a>
# **selectCountriesForGlobalSending**
> SelectCountriesForGlobalSending selectCountriesForGlobalSending(selectCountriesForGlobalSendingRequest)

Select Countries for Global Sending

_Select Countries_  Use this endpoint to select countries that you intend to send sms / mms to. To remove / unselect a country, just remove the country id from the array in the payload.  ### Properties  | Name | Type | Required | Restrictions | Description | | --- | --- | --- | --- | --- | | country_list_ids | number | true | none | Country list ID&#39;s |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    SelectCountriesForGlobalSendingRequest selectCountriesForGlobalSendingRequest = new SelectCountriesForGlobalSendingRequest(); // SelectCountriesForGlobalSendingRequest | 
    try {
      SelectCountriesForGlobalSending result = apiInstance.selectCountriesForGlobalSending(selectCountriesForGlobalSendingRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#selectCountriesForGlobalSending");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **selectCountriesForGlobalSendingRequest** | [**SelectCountriesForGlobalSendingRequest**](SelectCountriesForGlobalSendingRequest.md)|  | [optional] |

### Return type

[**SelectCountriesForGlobalSending**](SelectCountriesForGlobalSending.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="sendEmail"></a>
# **sendEmail**
> SendEmail sendEmail(contentType, sendEmailRequest)

Send Email

_Send transactional email_  Send transactional email  ### Properties  | Name | Type | Required | Restrictions | Description | | --- | --- | --- | --- | --- | | to | array | true | none | Array of To Recipient items. (array of names and emails) | | cc | array | false | none | Array of Cc Recipient items. (array of names and emails) | | bcc | array | false | none | Array of Bcc Recipient items. (array of names and emails) | | from | object | true | none | From Email object. (object containing name and email) | | body | string | true | none | Body of the email. | | attachments | array | false | none | Array of Attachment items. | | schedule | number | false | none | Schedule. | | name | string | false | none | Name of person email belongs to | | email | string | true | none | Email to be used. | | content | string | true | none | The base64-encoded contents of the file. | | type | string | true | none | The type of file being attached. | | filename | string | true | none | The name of the file being attached. | | disposition | string | true | none | Inline for content that can be displayed within the email, or attachment for any other files. | | content_id | string | true | none | An ID for the content. |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String contentType = "application/json"; // String | 
    SendEmailRequest sendEmailRequest = new SendEmailRequest(); // SendEmailRequest | 
    try {
      SendEmail result = apiInstance.sendEmail(contentType, sendEmailRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#sendEmail");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **contentType** | **String**|  | [optional] |
| **sendEmailRequest** | [**SendEmailRequest**](SendEmailRequest.md)|  | [optional] |

### Return type

[**SendEmail**](SendEmail.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="sendEmailCampaign"></a>
# **sendEmailCampaign**
> SendEmailCampaign sendEmailCampaign(contentType, sendEmailCampaignRequest)

Send Email Campaign

_Send email campaign_  Send email campaign  ### Properties  | Name | Type | Required | Restrictions | Description | | --- | --- | --- | --- | --- | | name | string | true | none | Your campaign name. | | subject | string | true | none | Your campaign subject. | | body | string | true | none | Your campaign message. | | from_email_address_id | number | true | none | The allowed email address id. | | from_name | string | true | none | Your name or business name. | | template_id | number | false | none | Your template id. | | list_id | number | true | none | Your contact list id. | | schedule | integer(int32) | false | none | Your schedule timestamp. |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String contentType = "application/json"; // String | 
    SendEmailCampaignRequest sendEmailCampaignRequest = new SendEmailCampaignRequest(); // SendEmailCampaignRequest | 
    try {
      SendEmailCampaign result = apiInstance.sendEmailCampaign(contentType, sendEmailCampaignRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#sendEmailCampaign");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **contentType** | **String**|  | [optional] |
| **sendEmailCampaignRequest** | [**SendEmailCampaignRequest**](SendEmailCampaignRequest.md)|  | [optional] |

### Return type

[**SendEmailCampaign**](SendEmailCampaign.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="sendEmailVerificationToken"></a>
# **sendEmailVerificationToken**
> SendEmailVerificationToken sendEmailVerificationToken(emailAddressId, contentType, sendEmailVerificationTokenRequest)

Send Email Verification Token

_Send verification token_  Send verification token  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | email_address_id | path | integer(int32) | true | Allowed email address id |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String emailAddressId = "emailAddressId_example"; // String | 
    String contentType = "application/json"; // String | 
    SendEmailVerificationTokenRequest sendEmailVerificationTokenRequest = new SendEmailVerificationTokenRequest(); // SendEmailVerificationTokenRequest | 
    try {
      SendEmailVerificationToken result = apiInstance.sendEmailVerificationToken(emailAddressId, contentType, sendEmailVerificationTokenRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#sendEmailVerificationToken");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **emailAddressId** | **String**|  | |
| **contentType** | **String**|  | [optional] |
| **sendEmailVerificationTokenRequest** | [**SendEmailVerificationTokenRequest**](SendEmailVerificationTokenRequest.md)|  | [optional] |

### Return type

[**SendEmailVerificationToken**](SendEmailVerificationToken.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="sendFax"></a>
# **sendFax**
> SendFax sendFax(contentType, sendFaxRequest)

Send Fax

### **Supported File Types**  - Supported file types are listed below. If you need to convert a file to a supported format, it can be first passed to our uploads endpoint: &#x60;/uploads?convert&#x3D;fax&#x60; - This will return a URL to the converted pdf file that can be used in the /fax/send endpoint. - Contact us to add support for any other file type.       ### Documents  | File type | Required to be passed to uploads endpoint first? | | --- | --- | | pdf | No | | docx | Yes | | doc | Yes | | rtf | Yes |  _Send a fax using supplied supported file-types._  ### **Letter File Options**  ### Use existing URL  With this option, you can use an existing URL to a &#x60;pdf&#x60; document. For example, you might generate the &#x60;pdf&#x60; on your server.  When using an existing url make sure that it is publicly accessible as it will not work if it is private.  ### Upload File to Our Server  With this option, you can use the [/uploads](/#upload-media-file) endpoint to upload the document. The &#x60;/uploads&#x60; endpoint returns a URL that can be used in the &#x60;/fax/send&#x60; endpoint.  ### Properties  | Name | Type | Required | Restrictions | Description | | --- | --- | --- | --- | --- | | file_url | string | true | none | URL of file to send | | source | string | true | none | Your method of sending e.g. &#39;wordpress&#39;, &#39;php&#39;, &#39;c#&#39;. | | to | string | true | none | Recipient fax number in [E.164](https://en.wikipedia.org/wiki/E.164) format. | | list_id | integer(int32) | false | none | Your list ID if sending to a whole list. Can be used instead of &#39;to&#39;. | | from | string | true | [yes](http://help.clicksend.com/SMS/what-is-a-sender-id-or-sender-number) | Your sender id. Must be a valid fax number. | | schedule | integer(int32) | false | none | Leave blank for immediate delivery. Your schedule time in unix format [http://help.clicksend.com/what-is-a-unix-timestamp](http://help.clicksend.com/what-is-a-unix-timestamp) | | custom_string | string | false | none | Your reference. Will be passed back with all replies and delivery reports. | | country | string | false | none | ISO alpha-2 character country code e.g. &#39;US&#39;, we use this to format the recipient number if it&#39;s not in international format. | | from_email | string | false | none | An email address where the reply should be emailed to. |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String contentType = "application/json"; // String | 
    SendFaxRequest sendFaxRequest = new SendFaxRequest(); // SendFaxRequest | 
    try {
      SendFax result = apiInstance.sendFax(contentType, sendFaxRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#sendFax");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **contentType** | **String**|  | [optional] |
| **sendFaxRequest** | [**SendFaxRequest**](SendFaxRequest.md)|  | [optional] |

### Return type

[**SendFax**](SendFax.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="sendLetter"></a>
# **sendLetter**
> SendLetter sendLetter(contentType, sendLetterRequest)

Send Letter

### Send letter  ### **Supported File Types**  We support &#x60;pdf&#x60;, &#x60;docx&#x60; and &#x60;doc&#x60; files. Contact us to add support for any other file type. If you&#39;re using &#x60;docx&#x60; or &#x60;doc&#x60; files, you&#39;ll need to convert the file first using our uploads endpoint with the querystring parameter &#x60;convert&#x3D;post&#x60; e.g. &#x60;POST https://rest.clicksend.com/v3/uploads?convert&#x3D;post&#x60;. This will return a URL to the converted pdf file that can be used in the &#x60;/post/letters/send&#x60; endpoint.  ### **Letter Specification Guide**  Follow our [Letter specification guide](https://help.clicksend.com/article/wcpkkoou6c-post-letter-template) to ensure correct sending and letter template information.  ### **Letter File Options**  ### Use existing URL  With this option, you can use an existing URL to a &#x60;pdf&#x60; document. For example, you might generate the &#x60;pdf&#x60; on your server.  When using an existing url make sure that it is publicly accessible as it will not work if it is private.  ### Upload File to Our Server  With this option, you can use the [/uploads](/#upload-media-file) endpoint to upload the document. The &#x60;/uploads&#x60; endpoint returns a URL that can be used in the &#x60;/post/letters/send&#x60; endpoint.  ### Properties  | Name | Type | Required | Restrictions | Description | | --- | --- | --- | --- | --- | | file_url | string | true | none | URL of file to send | | address_name | string | true | none | Name of address | | address_line_1 | string | true | none | First line of address | | address_line_2 | string | true | none | Second line of address | | address_city | string | true | none | City | | address_state | string | true | none | State | | address_postal_code | string | true | none | Postal code | | address_country | string | true | none | Country | | return_address_id | integer(int32) | true | none | ID of return address to use | | schedule | integer(int32) | false | none | When to send letter (0/null&#x3D;now) | | template_used | integer(int1) | false | none | Whether using our letter template. Flag value must be 1 for yes or 0 for no. | | duplex | integer(int1) | false | none | Whether letter is duplex. Flag value must be 1 for yes or 0 for no. | | colour | integer(int1) | false | none | Whether letter is in colour. Flag value must be 1 for yes or 0 for no. | | priority_post | integer(int1) | false | none | Whether letter is priority, Flag value must be 1 for yes or 0 for no. | | source | string | false | none | Source being sent from |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String contentType = "application/json"; // String | 
    SendLetterRequest sendLetterRequest = new SendLetterRequest(); // SendLetterRequest | 
    try {
      SendLetter result = apiInstance.sendLetter(contentType, sendLetterRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#sendLetter");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **contentType** | **String**|  | [optional] |
| **sendLetterRequest** | [**SendLetterRequest**](SendLetterRequest.md)|  | [optional] |

### Return type

[**SendLetter**](SendLetter.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="sendMms"></a>
# **sendMms**
> SendMms sendMms(contentType, sendMmsRequest)

Send MMS

_Send MMS_  You can post **up to 1000 messages** with each API call. You can send to a mix of contacts and contact lists, as long as the total number of recipients is up to 1000. The response contains a status and details for each recipient.  Refer to [&lt;b&gt;Application Status Codes&lt;/b&gt;](/#application-status-codes) for the possible response message status strings.  ### **How many characters can I send in a message?**  ### Standard MMS Message  1500 characters  ### Unicode MMS Message  500 characters  If a message is longer the allowed number of characters it will be truncated. If a message contains any characters that aren&#39;t in the GSM 03.38 character set, the message type will be treated as unicode. ([https://en.wikipedia.org/wiki/GSM_03.38](https://en.wikipedia.org/wiki/GSM_03.38))  ### Maximum File Size  You can send a single attachment with a size of up to 250 kB. Some older devices can only accept attachments with up to 30 kB.  ### Supported File Types  - Supported file types are listed below. If you need to convert a file to a supported format, it can be first passed to our uploads endpoint: &#x60;/uploads?convert&#x3D;mms&#x60; - This will return a URL to the converted image file that can be used in the /mms/send endpoint. - Contact us to add support for any other file type.       ### Images  | File type | Required to be passed to uploads endpoint first? | | --- | --- | | &#x60;jpg&#x60; | No | | &#x60;gif&#x60; | No | | &#x60;jpeg&#x60; | Yes | | &#x60;png&#x60; | Yes | | &#x60;bmp&#x60; | Yes |  ### Properties  | Name | Type | Required | Restrictions | Description | | --- | --- | --- | --- | --- | | media_file | string | true | none | Media file you want to send | | to | string | true | none | Recipient phone number in [E.164](https://en.wikipedia.org/wiki/E.164) format | | body | string | true | none | Your message | | subject | string | true | none | Subject line (max 20 characters) | | from | string | true | [yes](http://help.clicksend.com/SMS/what-is-a-sender-id-or-sender-number) | Your sender id |  Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.  &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String contentType = "application/json"; // String | 
    SendMmsRequest sendMmsRequest = new SendMmsRequest(); // SendMmsRequest | 
    try {
      SendMms result = apiInstance.sendMms(contentType, sendMmsRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#sendMms");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **contentType** | **String**|  | [optional] |
| **sendMmsRequest** | [**SendMmsRequest**](SendMmsRequest.md)|  | [optional] |

### Return type

[**SendMms**](SendMms.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="sendMmsCampaign"></a>
# **sendMmsCampaign**
> SendMmsCampaign sendMmsCampaign(contentType, sendMmsCampaignRequest)

Send MMS Campaign

_Create mms campaign_  ### Properties  | Name | Type | Required | Restrictions | Description | | --- | --- | --- | --- | --- | | list_id | integer(int32) | true | none | Your list id. | | name | string | true | none | Your campaign name. | | body | string | true | none | Your campaign message. | | from | string | true | [yes](http://help.clicksend.com/SMS/what-is-a-sender-id-or-sender-number) | Your sender id | | schedule | integer(int32) | false | none | Your schedule timestamp. | | subject | string | true | none | Subject of MMS campaign. | | media_file | string | true | none | URL pointing to media file. |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String contentType = "application/json"; // String | 
    SendMmsCampaignRequest sendMmsCampaignRequest = new SendMmsCampaignRequest(); // SendMmsCampaignRequest | 
    try {
      SendMmsCampaign result = apiInstance.sendMmsCampaign(contentType, sendMmsCampaignRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#sendMmsCampaign");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **contentType** | **String**|  | [optional] |
| **sendMmsCampaignRequest** | [**SendMmsCampaignRequest**](SendMmsCampaignRequest.md)|  | [optional] |

### Return type

[**SendMmsCampaign**](SendMmsCampaign.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="sendPostcard"></a>
# **sendPostcard**
> SendPostcard sendPostcard(contentType, sendPostcardRequest)

Send Postcard

_Send one or more postcards_  ### **Supported File Types**  We support PDF, docx, doc, jpg, gif, png, and bmp. Contact us to add support for any other file type. If you&#39;re using docx, doc, jpg, gif, png, or bmp files, you&#39;ll need to convert the file first using our uploads endpoint with the querystring parameter ?convert&#x3D;postcard. e.g. POST /uploads?convert&#x3D;postcard. This will return a URL to the converted pdf file that can be used in the /post/postcards/send endpoint.  ### **Postcard Specification Guide**  Follow our [Postcard specification guide](https://help.clicksend.com/article/ysyql7bsr1-postcard-template) to ensure correct sending and postcard template information.  ### **Postcard File Options**  ### Use existing URL  With this option, you can use an existing URL to a &#x60;pdf&#x60; document. For example, you might generate the &#x60;pdf&#x60; on your server.  When using an existing url make sure that it is publicly accessible as it will not work if it is private.  For &#x60;file_urls&#x60; field. You can attach at least 1 and max of 2 PDF file urls.  - Supply a single pdf with 2 pages (front and back) - Supply 2 urls to seperate PDFs       ### Upload File to Our Server  With this option, you can use the [/uploads](/#upload-media-file) endpoint to upload the document. The &#x60;/uploads&#x60; endpoint returns a URL that can be used in the &#x60;/post/postcards/send&#x60; endpoint.  ### Properties  | Name | Type | Required | Restrictions | Description | | --- | --- | --- | --- | --- | | file_urls | \\[string\\] | true | none | Postcard file URLs | | address_name | string | true | none | Name of address | | address_line_1 | string | true | none | First line of address | | address_line_2 | string | true | none | Second line of address | | address_city | string | true | none | City | | address_state | string | true | none | State | | address_postal_code | string | true | none | Postal code | | address_country | string | true | none | Country | | return_address_id | integer(int32) | true | none | ID of return address to use | | schedule | integer(int32) | false | none | When to send letter (0/null&#x3D;now) |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String contentType = "application/json"; // String | 
    SendPostcardRequest sendPostcardRequest = new SendPostcardRequest(); // SendPostcardRequest | 
    try {
      SendPostcard result = apiInstance.sendPostcard(contentType, sendPostcardRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#sendPostcard");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **contentType** | **String**|  | [optional] |
| **sendPostcardRequest** | [**SendPostcardRequest**](SendPostcardRequest.md)|  | [optional] |

### Return type

[**SendPostcard**](SendPostcard.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="sendSms"></a>
# **sendSms**
> SendSms sendSms(contentType, sendSmsRequest)

Send SMS

Use this endpoint to send messages to your recipients, either as phone numbers or contacts from your contact list.  The sender of the message (&lt;a href&#x3D;\&quot;https://help.clicksend.com/article/4kgj7krx00-what-is-a-sender-id-or-sender-number\&quot; target&#x3D;\&quot;_blank\&quot;&gt;&lt;strong&gt;Sender ID&lt;/strong&gt;&lt;/a&gt;) can be a shared number, a dedicated number, alpha tag (business name), or your own number.  You can send messages both locally and globally, subject to the country restrictions. The cost of sending messages varies based on the &lt;a href&#x3D;\&quot;https://help.clicksend.com/article/h474eseq3a-how-many-characters-can-i-send-in-an-sms\&quot; target&#x3D;\&quot;_blank\&quot;&gt;type&lt;/a&gt; and length of the message.

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String contentType = "application/json"; // String | 
    SendSmsRequest sendSmsRequest = new SendSmsRequest(); // SendSmsRequest | 
    try {
      SendSms result = apiInstance.sendSms(contentType, sendSmsRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#sendSms");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **contentType** | **String**|  | [optional] |
| **sendSmsRequest** | [**SendSmsRequest**](SendSmsRequest.md)|  | [optional] |

### Return type

[**SendSms**](SendSms.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="sendSmsCampaign"></a>
# **sendSmsCampaign**
> SendSmsCampaign sendSmsCampaign(contentType, sendSmsCampaignRequest)

Send SMS Campaign

### _SMS Campaign Endpoint_  You can post to a list with &#x60;up to 20000 recipients&#x60; with each API call. You can only send to a single list containing up to 20,000 recipients. The response is far less detailed than the normal Send SMS endpoint. Use the [SMS Send](/#send-sms) endpoint if you would like to send to less than 1000 recipients at once. You are required to add an opt-out message to the end of your message body if you are sending marketing message. This can be in the form of asking users to reply STOP to opt-out or by including &#x60;StopMsg.me/xxxxx&#x60; which is a placeholder that will add a link that can be clicked to out-out. Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses. &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String contentType = "application/json"; // String | 
    SendSmsCampaignRequest sendSmsCampaignRequest = new SendSmsCampaignRequest(); // SendSmsCampaignRequest | 
    try {
      SendSmsCampaign result = apiInstance.sendSmsCampaign(contentType, sendSmsCampaignRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#sendSmsCampaign");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **contentType** | **String**|  | [optional] |
| **sendSmsCampaignRequest** | [**SendSmsCampaignRequest**](SendSmsCampaignRequest.md)|  | [optional] |

### Return type

[**SendSmsCampaign**](SendSmsCampaign.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="sendVoiceMessage"></a>
# **sendVoiceMessage**
> SendVoiceMessage sendVoiceMessage(contentType, sendVoiceMessageRequest)

Send Voice Message

_Send voice message(s)_  Send TTS (Text-to-speech) voice calls  ### How many messages can I send?  You can post **up to 1000 messages** with each API call. You can send to a mix of contacts and contact lists, as long as the total number of recipients is up to 1000. The response contains a status and details for each recipient.  ### How many characters can I send in a message?  If a message is longer than 4 message parts, it will be truncated (see below). If a message contains any characters that aren&#39;t in the GSM 03.38 character set, the message type will be treated as unicode. (&#x60;https://en.wikipedia.org/wiki/GSM_03.38&#x60;)  ### _Standard English Characters:_  | Number of Characters | Message Credits | | --- | --- | | 1 - 300 | 1 | | 301 - 600 | 2 | | 601 - 900 | 3 | | 901 - 1200 | 4 |  ### _Non-GSM (Unicode) characters:_  | Number of Characters | Message Credits | | --- | --- | | 1 - 150 | 1 | | 151 - 300 | 2 | | 301 - 450 | 3 | | 451 - 600 | 4 |  ### _Allowed Languages_  | Language, Locale | lang | voice | | --- | --- | --- | | &#x60;English&#x60;, US | en-us | female (default) / male | | &#x60;English&#x60;, Australia | en-au | female (default) / male | | &#x60;English&#x60;, UK | en-gb | female (default) / male | | &#x60;English&#x60;, India | en-in | female | | &#x60;English&#x60;, Wales | en-gb-wls | female (default) / male | | &#x60;Celtic&#x60;, Wales | cy-gb-wls | female (default) / male | | &#x60;German&#x60;, Germany | de-de | female (default) / male | | &#x60;Spanish&#x60;, Spain | es-es | female (default) / male | | &#x60;Spanish&#x60;, US | es-us | female (default) / male | | &#x60;French&#x60;, Canada | fr-ca | female | | &#x60;French&#x60;, France | fr-fr | female (default) / male | | &#x60;Icelandic&#x60;, Iceland | is-is | female (default) / male | | &#x60;Italian&#x60;, Italy | it-it | female (default) / male | | &#x60;Danish&#x60;, Denmark | da-dk | female (default) / male | | &#x60;Dutch&#x60;, Netherlands | nl-nl | female (default) / male | | &#x60;Norwegian&#x60;, Norway | nb-no | female | | &#x60;Polish&#x60;, Poland | pl-pl | female (default) / male | | &#x60;Portuguese&#x60;, Portugal | pt-pt | male | | &#x60;Portuguese&#x60;, Brazil | pt-br | female (default) / male | | &#x60;Romanian&#x60;, Romania | ro-ro | female | | &#x60;Russian&#x60;, Russia | ru-ru | female (default) / male | | &#x60;Swedish&#x60;, Sweden | sv-se | female | | &#x60;Turkish&#x60;, Turkey | tr-tr | female |  _Tips_  To introduce a small delay between words or digits you can use a comma (,).  For example: &#x60;Please enter your activation code 9, 0, 9, 0, in the next 20 minutes.&#x60;  We support some SSML tags allowing custom breaks or pauses to be entered, and the readout rate to be altered.  [More info...](https://help.clicksend.com/en/articles/42982-customising-text-to-voice-output)  ### Properties  | Name | Type | Required | Restrictions | Description | | --- | --- | --- | --- | --- | | to | string | true | none | Your phone number in [E.164](https://en.wikipedia.org/wiki/E.164) format. | | body | string | true | none | Biscuit uv3nlCOjRk croissant chocolate lollipop chocolate muffin. | | voice | string | true | none | Either &#39;female&#39; or &#39;male&#39;. | | custom_string | string | true | none | Your reference. Will be passed back with all replies and delivery reports. | | country | string | true | none | The country of the recipient. | | source | string | false | none | Your method of sending e.g. &#39;wordpress&#39;, &#39;php&#39;, &#39;c#&#39;. | | list_id | integer(int32) | false | none | Your list ID if sending to a whole list. Can be used instead of &#39;to&#39;. | | lang | string | false | none | au (string, required) - See section on available languages. | | schedule | integer(int32) | false | none | Leave blank for immediate delivery. Your schedule time in unix format [http://help.clicksend.com/what-is-a-unix-timestamp](http://help.clicksend.com/what-is-a-unix-timestamp) | | require_input | integer(int1) | false | none | Recieve a keypress from the recipient. Flag value must be 1 for yes or 0 for no. | | machine_detection | integer(int1) | false | none | Detect answering machine or voicemail and leave a message. Flag value must be 1 for yes or 0 for no. |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String contentType = "application/json"; // String | 
    SendVoiceMessageRequest sendVoiceMessageRequest = new SendVoiceMessageRequest(); // SendVoiceMessageRequest | 
    try {
      SendVoiceMessage result = apiInstance.sendVoiceMessage(contentType, sendVoiceMessageRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#sendVoiceMessage");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **contentType** | **String**|  | [optional] |
| **sendVoiceMessageRequest** | [**SendVoiceMessageRequest**](SendVoiceMessageRequest.md)|  | [optional] |

### Return type

[**SendVoiceMessage**](SendVoiceMessage.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="shortUrlGetStatistics"></a>
# **shortUrlGetStatistics**
> GetStatistics shortUrlGetStatistics(source, sourceId, contentType)

Get Statistics

Use this endpoint to get the aggregated statistics for a shortened URL. This allows you to track the total number of clicks on the link. You can gather details such as the device type and where it was opened from as well.

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String source = "quick_sms"; // String | Source of the request.
    String sourceId = "sourceId_example"; // String | ID of the source (e.g. message ID).
    String contentType = "application/json"; // String | 
    try {
      GetStatistics result = apiInstance.shortUrlGetStatistics(source, sourceId, contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#shortUrlGetStatistics");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **source** | **String**| Source of the request. | [enum: quick_sms] |
| **sourceId** | **String**| ID of the source (e.g. message ID). | |
| **contentType** | **String**|  | [optional] |

### Return type

[**GetStatistics**](GetStatistics.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="shortUrlGetTracking"></a>
# **shortUrlGetTracking**
> GetTracking shortUrlGetTracking(longUrlId, contentType)

Get Tracking

Use this endpoint to track how individual recipients interact with the link.  It returns data from the most recent click, including statistics such as how many times they’ve visited the link and when it was last opened. To use this endpoint, reference the _long_url_id_ provided in the [GET /short-url/statistics](/messaging/url-shortening/other/short-url-get-statistics) endpoint.

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String longUrlId = "longUrlId_example"; // String | ID of the long URL (uniquely defined by the source, source ID, and long URL). Obtained from the GET statistics endpoint.
    String contentType = "application/json"; // String | 
    try {
      GetTracking result = apiInstance.shortUrlGetTracking(longUrlId, contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#shortUrlGetTracking");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **longUrlId** | **String**| ID of the long URL (uniquely defined by the source, source ID, and long URL). Obtained from the GET statistics endpoint. | |
| **contentType** | **String**|  | [optional] |

### Return type

[**GetTracking**](GetTracking.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="timezones"></a>
# **timezones**
> Timezones timezones(contentType)

Timezones

_Get supported list of timezones._  Get supported list of timezones.  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | page | query | integer(int32) | false | Page number | | limit | query | integer(int32) | false | Number of records per page |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String contentType = "application/json"; // String | 
    try {
      Timezones result = apiInstance.timezones(contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#timezones");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **contentType** | **String**|  | [optional] |

### Return type

[**Timezones**](Timezones.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="transferContactToList"></a>
# **transferContactToList**
> TransferContactToList transferContactToList(fromListId, contactId, toListId, contentType, body)

Transfer Contact to List

_Transfer contact to another list_  Transfer contact to another list  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | from_list_id | path | integer(int32) | true | List ID for list that contains contact. | | contact_id | path | integer(int32) | true | Contact ID | | to_list_id | path | integer(int32) | true | List ID for list you want to transfer contact to. |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String fromListId = "fromListId_example"; // String | 
    String contactId = "contactId_example"; // String | 
    String toListId = "toListId_example"; // String | 
    String contentType = "application/json"; // String | 
    Object body = null; // Object | 
    try {
      TransferContactToList result = apiInstance.transferContactToList(fromListId, contactId, toListId, contentType, body);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#transferContactToList");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **fromListId** | **String**|  | |
| **contactId** | **String**|  | |
| **toListId** | **String**|  | |
| **contentType** | **String**|  | [optional] |
| **body** | **Object**|  | [optional] |

### Return type

[**TransferContactToList**](TransferContactToList.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="updateClientAccount"></a>
# **updateClientAccount**
> UpdateClientAccount updateClientAccount(clientUserId, contentType, updatePaymentInfoRequest)

Update Client Account

_Update Reseller clients Account_  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | client_user_id | path | integer(int32) | true | User ID of client |  ### Properties  | Name | Type | Required | Restrictions | Description | | --- | --- | --- | --- | --- | | username | string | true | none | Account username | | password | string | true | none | Account password (unhashed) | | user_email | string | true | none | Account email | | user_phone | string | true | none | Account phone number | | user_first_name | string | true | none | Account owner first name | | user_last_name | string | true | none | Account owner last name | | account_name | string | true | none | Account name (usually company name) | | country | string | true | none | Country of account holder |  Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.  &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String clientUserId = "clientUserId_example"; // String | 
    String contentType = "application/x-www-form-urlencoded"; // String | 
    UpdatePaymentInfoRequest updatePaymentInfoRequest = new UpdatePaymentInfoRequest(); // UpdatePaymentInfoRequest | 
    try {
      UpdateClientAccount result = apiInstance.updateClientAccount(clientUserId, contentType, updatePaymentInfoRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#updateClientAccount");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **clientUserId** | **String**|  | |
| **contentType** | **String**|  | [optional] |
| **updatePaymentInfoRequest** | [**UpdatePaymentInfoRequest**](UpdatePaymentInfoRequest.md)|  | [optional] |

### Return type

[**UpdateClientAccount**](UpdateClientAccount.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="updateContact"></a>
# **updateContact**
> UpdateContact updateContact(listId, contactId, contentType, createNewContactRequest)

Update Contact

_Update specific contact_  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | list_id | path | integer(int32) | true | Contact list id | | contact_id | path | integer(int32) | true | Contact ID |  ### Properties  | Name | Type | Required | Restrictions | Description | | --- | --- | --- | --- | --- | | phone_number | string | true | none | Your phone number in [E.164](https://en.wikipedia.org/wiki/E.164) format. Must be provided if no fax number or email. | | email | string | false | none | Your email. Must be provided if no phone number or fax number. | | fax_number | string | false | none | Your fax number. Must be provided if no phone number or email. | | first_name | string | false | none | Your first name. | | address_line_1 | string | false | none | Your street address | | address_line_2 | string | false | none | none | | address_city | string | false | none | Your nearest city | | address_state | string | false | none | Your current state | | address_postal_code | string | false | none | Your current postcode | | address_country | string | false | none | Your current country | | organization_name | string | false | none | Your organisation name | | custom_1 | string | true | none | none | | custom_2 | string | false | none | none | | custom_3 | string | false | none | none | | custom_4 | string | false | none | none | | last_name | string | false | none | Your last name |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String listId = "listId_example"; // String | 
    String contactId = "contactId_example"; // String | 
    String contentType = "application/json"; // String | 
    CreateNewContactRequest createNewContactRequest = new CreateNewContactRequest(); // CreateNewContactRequest | 
    try {
      UpdateContact result = apiInstance.updateContact(listId, contactId, contentType, createNewContactRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#updateContact");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **listId** | **String**|  | |
| **contactId** | **String**|  | |
| **contentType** | **String**|  | [optional] |
| **createNewContactRequest** | [**CreateNewContactRequest**](CreateNewContactRequest.md)|  | [optional] |

### Return type

[**UpdateContact**](UpdateContact.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="updateDefaultSender"></a>
# **updateDefaultSender**
> UpdateDefaultSender updateDefaultSender(defaultSenderId, contentType, updateDefaultSenderRequest)

Update Default Sender

Updates the details of an existing default sender configuration.  For more information on Sender IDs, please refer to [What is a Sender ID or Sender Number?](https://help.clicksend.com/article/4kgj7krx00-what-is-a-sender-id-or-sender-number)

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String defaultSenderId = "defaultSenderId_example"; // String | The ID of the default sender to update
    String contentType = "application/json"; // String | 
    UpdateDefaultSenderRequest updateDefaultSenderRequest = new UpdateDefaultSenderRequest(); // UpdateDefaultSenderRequest | 
    try {
      UpdateDefaultSender result = apiInstance.updateDefaultSender(defaultSenderId, contentType, updateDefaultSenderRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#updateDefaultSender");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **defaultSenderId** | **String**| The ID of the default sender to update | |
| **contentType** | **String**|  | [optional] |
| **updateDefaultSenderRequest** | [**UpdateDefaultSenderRequest**](UpdateDefaultSenderRequest.md)|  | [optional] |

### Return type

[**UpdateDefaultSender**](UpdateDefaultSender.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |
| **400** | Bad request |  -  |

<a id="updateEmailCampaign"></a>
# **updateEmailCampaign**
> UpdateEmailCampaign updateEmailCampaign(emailCampaignId, contentType, updateEmailCampaignRequest)

Update Email Campaign

_Edit email campaign_  Edit email campaign  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | email_campaign_id | path | integer(int32) | true | Allowed email campaign id |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String emailCampaignId = "emailCampaignId_example"; // String | 
    String contentType = "application/json"; // String | 
    UpdateEmailCampaignRequest updateEmailCampaignRequest = new UpdateEmailCampaignRequest(); // UpdateEmailCampaignRequest | 
    try {
      UpdateEmailCampaign result = apiInstance.updateEmailCampaign(emailCampaignId, contentType, updateEmailCampaignRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#updateEmailCampaign");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **emailCampaignId** | **String**|  | |
| **contentType** | **String**|  | [optional] |
| **updateEmailCampaignRequest** | [**UpdateEmailCampaignRequest**](UpdateEmailCampaignRequest.md)|  | [optional] |

### Return type

[**UpdateEmailCampaign**](UpdateEmailCampaign.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="updateEmailDeliveryReceiptRule"></a>
# **updateEmailDeliveryReceiptRule**
> UpdateEmailDeliveryReceiptRule updateEmailDeliveryReceiptRule(receiptRuleId, contentType, createSmsDeliveryReceiptRuleRequest)

Update Email Delivery Receipt Rule

_Update email delivery receipt automation_  Update email delivery receipt automation  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | receipt_rule_id | path | integer(int32) | true | Receipt rule id |  ### Properties  | Name | Type | Required | Restrictions | Description | | --- | --- | --- | --- | --- | | rule_name | string | true | none | Rule Name. | | match_type | number | true | none | Match Type. 0&#x3D;All reports. | | action | string | true | none | Action to be taken (AUTO_REPLY, EMAIL_USER, EMAIL_FIXED, URL, SMS, POLL, GROUP_SMS, MOVE_CONTACT, CREATE_CONTACT, CREATE_CONTACT_PLUS_EMAIL, CREATE_CONTACT_PLUS_NAME_EMAIL CREATE_CONTACT_PLUS_NAME, SMPP, NONE). | | action_address | string | true | none | Action address. | | enabled | number | true | none | Enabled: Disabled&#x3D;0 or Enabled&#x3D;1. |  Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.  &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String receiptRuleId = "receiptRuleId_example"; // String | 
    String contentType = "application/json"; // String | 
    CreateSmsDeliveryReceiptRuleRequest createSmsDeliveryReceiptRuleRequest = new CreateSmsDeliveryReceiptRuleRequest(); // CreateSmsDeliveryReceiptRuleRequest | 
    try {
      UpdateEmailDeliveryReceiptRule result = apiInstance.updateEmailDeliveryReceiptRule(receiptRuleId, contentType, createSmsDeliveryReceiptRuleRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#updateEmailDeliveryReceiptRule");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **receiptRuleId** | **String**|  | |
| **contentType** | **String**|  | [optional] |
| **createSmsDeliveryReceiptRuleRequest** | [**CreateSmsDeliveryReceiptRuleRequest**](CreateSmsDeliveryReceiptRuleRequest.md)|  | [optional] |

### Return type

[**UpdateEmailDeliveryReceiptRule**](UpdateEmailDeliveryReceiptRule.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="updateEmailTemplate"></a>
# **updateEmailTemplate**
> UpdateEmailTemplate updateEmailTemplate(templateId, contentType, updateEmailTemplateRequest)

Update Email Template

_Update email template_  Update email template  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | template_id | path | integer(int32) | true | Email template id |  ### Properties  | Name | Type | Required | Restrictions | Description | | --- | --- | --- | --- | --- | | template_name | string | false | none | The intended name for the template. | | body | string | true | none | Your template body. |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String templateId = "templateId_example"; // String | 
    String contentType = "application/json"; // String | 
    UpdateEmailTemplateRequest updateEmailTemplateRequest = new UpdateEmailTemplateRequest(); // UpdateEmailTemplateRequest | 
    try {
      UpdateEmailTemplate result = apiInstance.updateEmailTemplate(templateId, contentType, updateEmailTemplateRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#updateEmailTemplate");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **templateId** | **String**|  | |
| **contentType** | **String**|  | [optional] |
| **updateEmailTemplateRequest** | [**UpdateEmailTemplateRequest**](UpdateEmailTemplateRequest.md)|  | [optional] |

### Return type

[**UpdateEmailTemplate**](UpdateEmailTemplate.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="updateFaxDeliveryReceiptRule"></a>
# **updateFaxDeliveryReceiptRule**
> UpdateFaxDeliveryReceiptRule updateFaxDeliveryReceiptRule(receiptRuleId, contentType, updateFaxDeliveryReceiptRuleRequest)

Update FAX Delivery Receipt Rule

_Update fax delivery receipt automation_  Update fax delivery receipt automation  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | receipt_rule_id | path | integer(int32) | true | Receipt rule id |  ### Properties  | Name | Type | Required | Restrictions | Description | | --- | --- | --- | --- | --- | | rule_name | string | true | none | Rule Name. | | match_type | number | true | none | Match Type. 0&#x3D;All reports. | | action | string | true | none | Action to be taken (AUTO_REPLY, EMAIL_USER, EMAIL_FIXED, URL, SMS, POLL, GROUP_SMS, MOVE_CONTACT, CREATE_CONTACT, CREATE_CONTACT_PLUS_EMAIL, CREATE_CONTACT_PLUS_NAME_EMAIL CREATE_CONTACT_PLUS_NAME, SMPP, NONE). | | action_address | string | true | none | Action address. | | enabled | number | true | none | Enabled: Disabled&#x3D;0 or Enabled&#x3D;1. |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String receiptRuleId = "receiptRuleId_example"; // String | 
    String contentType = "application/json"; // String | 
    UpdateFaxDeliveryReceiptRuleRequest updateFaxDeliveryReceiptRuleRequest = new UpdateFaxDeliveryReceiptRuleRequest(); // UpdateFaxDeliveryReceiptRuleRequest | 
    try {
      UpdateFaxDeliveryReceiptRule result = apiInstance.updateFaxDeliveryReceiptRule(receiptRuleId, contentType, updateFaxDeliveryReceiptRuleRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#updateFaxDeliveryReceiptRule");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **receiptRuleId** | **String**|  | |
| **contentType** | **String**|  | [optional] |
| **updateFaxDeliveryReceiptRuleRequest** | [**UpdateFaxDeliveryReceiptRuleRequest**](UpdateFaxDeliveryReceiptRuleRequest.md)|  | [optional] |

### Return type

[**UpdateFaxDeliveryReceiptRule**](UpdateFaxDeliveryReceiptRule.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="updateFaxInboundRule"></a>
# **updateFaxInboundRule**
> UpdateFaxInboundRule updateFaxInboundRule(inboundRuleId, contentType, createFaxInboundRuleRequest)

Update Fax Inbound Rule

_Update inbound fax automation_  Update inbound fax automation  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | inbound_rule_id | path | integer(int32) | true | Inbound rule id |  ### Properties  | Name | Type | Required | Restrictions | Description | | --- | --- | --- | --- | --- | | dedicated_number | string | true | none | Dedicated Number. Can be &#39;\\*&#39; to apply to all numbers. | | rule_name | string | true | none | Rule Name. | | action | string | true | none | Action to be taken (AUTO_REPLY, EMAIL_USER, EMAIL_FIXED, URL, SMS, POLL, GROUP_SMS, MOVE_CONTACT, CREATE_CONTACT, CREATE_CONTACT_PLUS_EMAIL, CREATE_CONTACT_PLUS_NAME_EMAIL CREATE_CONTACT_PLUS_NAME, SMPP, NONE). | | action_address | string | true | none | Action address. | | enabled | number | true | none | Enabled: Disabled&#x3D;0 or Enabled&#x3D;1. |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String inboundRuleId = "inboundRuleId_example"; // String | 
    String contentType = "application/json"; // String | 
    CreateFaxInboundRuleRequest createFaxInboundRuleRequest = new CreateFaxInboundRuleRequest(); // CreateFaxInboundRuleRequest | 
    try {
      UpdateFaxInboundRule result = apiInstance.updateFaxInboundRule(inboundRuleId, contentType, createFaxInboundRuleRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#updateFaxInboundRule");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **inboundRuleId** | **String**|  | |
| **contentType** | **String**|  | [optional] |
| **createFaxInboundRuleRequest** | [**CreateFaxInboundRuleRequest**](CreateFaxInboundRuleRequest.md)|  | [optional] |

### Return type

[**UpdateFaxInboundRule**](UpdateFaxInboundRule.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="updateList"></a>
# **updateList**
> UpdateList updateList(listId, contentType, createListRequest)

Update List

_Update specific contact list_  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | list_id | path | integer(int32) | true | Your list id | | list_name | body | string | true | Your new list name |  Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.  &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String listId = "listId_example"; // String | 
    String contentType = "application/json"; // String | 
    CreateListRequest createListRequest = new CreateListRequest(); // CreateListRequest | 
    try {
      UpdateList result = apiInstance.updateList(listId, contentType, createListRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#updateList");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **listId** | **String**|  | |
| **contentType** | **String**|  | [optional] |
| **createListRequest** | [**CreateListRequest**](CreateListRequest.md)|  | [optional] |

### Return type

[**UpdateList**](UpdateList.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="updateMmsCampaign"></a>
# **updateMmsCampaign**
> UpdateMmsCampaign updateMmsCampaign(mmsCampaignId, contentType, calculateSmsCampaignPriceRequest)

Update MMS Campaign

_Update mms campaign_  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | mms_campaign_id | path | integer(int32) | true | ID of MMS campaign to update |  ### Properties  | Name | Type | Required | Restrictions | Description | | --- | --- | --- | --- | --- | | list_id | integer(int32) | true | none | Your list id. | | name | string | true | none | Your campaign name. | | body | string | true | none | Your campaign message. | | from | string | true | [yes](http://help.clicksend.com/SMS/what-is-a-sender-id-or-sender-number) | Your sender id | | schedule | integer(int32) | false | none | Your schedule timestamp. | | subject | string | true | none | Subject of MMS campaign. | | media_file | string | true | none | URL pointing to media file. |  Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.  &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String mmsCampaignId = "mmsCampaignId_example"; // String | 
    String contentType = "application/json"; // String | 
    CalculateSmsCampaignPriceRequest calculateSmsCampaignPriceRequest = new CalculateSmsCampaignPriceRequest(); // CalculateSmsCampaignPriceRequest | 
    try {
      UpdateMmsCampaign result = apiInstance.updateMmsCampaign(mmsCampaignId, contentType, calculateSmsCampaignPriceRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#updateMmsCampaign");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **mmsCampaignId** | **String**|  | |
| **contentType** | **String**|  | [optional] |
| **calculateSmsCampaignPriceRequest** | [**CalculateSmsCampaignPriceRequest**](CalculateSmsCampaignPriceRequest.md)|  | [optional] |

### Return type

[**UpdateMmsCampaign**](UpdateMmsCampaign.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="updateOwnNumber"></a>
# **updateOwnNumber**
> OwnNumber updateOwnNumber(ownNumberId)

Update Own Number

_Update details of a specific own numbers._  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | own_number_id | path | uuid | true | ID of the own number |  ### Properties  | Name | Type | Required | Restrictions | Description | | --- | --- | --- | --- | --- | | label | string | false | none | Custom label for phone number. Length must be between 1 - 200 characters. |  Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.  This endpoint requires authentication, [more info...](/#authentication)

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String ownNumberId = "ownNumberId_example"; // String | 
    try {
      OwnNumber result = apiInstance.updateOwnNumber(ownNumberId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#updateOwnNumber");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **ownNumberId** | **String**|  | |

### Return type

[**OwnNumber**](OwnNumber.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="updatePaymentInfo"></a>
# **updatePaymentInfo**
> UpdatePaymentInfo updatePaymentInfo(contentType, updatePaymentInfoRequest)

Update Payment Info

_Update credit card info_  ### Properties  | Name | Type | Required | Restrictions | Description | | --- | --- | --- | --- | --- | | number | string | true | none | Credit card number | | expiry_month | integer(int32) | true | none | Expiry month of credit card | | expiry_year | integer(int32) | true | none | Expiry year of credit card | | cvc | integer(int32) | true | none | CVC number of credit card | | name | string | true | none | Name printed on credit card | | bank_name | string | true | none | Name of bank that credit card belongs to |  Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String contentType = "application/x-www-form-urlencoded"; // String | 
    UpdatePaymentInfoRequest updatePaymentInfoRequest = new UpdatePaymentInfoRequest(); // UpdatePaymentInfoRequest | 
    try {
      UpdatePaymentInfo result = apiInstance.updatePaymentInfo(contentType, updatePaymentInfoRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#updatePaymentInfo");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **contentType** | **String**|  | [optional] |
| **updatePaymentInfoRequest** | [**UpdatePaymentInfoRequest**](UpdatePaymentInfoRequest.md)|  | [optional] |

### Return type

[**UpdatePaymentInfo**](UpdatePaymentInfo.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="updateReturnAddress"></a>
# **updateReturnAddress**
> UpdateReturnAddress updateReturnAddress(returnAddressId, contentType, updateReturnAddressRequest)

Update Return Address

_Update post return address_  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | return_address_id | path | integer(int32) | true | Return address ID |  ### Properties  | Name | Type | Required | Restrictions | Description | | --- | --- | --- | --- | --- | | address_name | string | true | none | Your address name. | | address_line_1 | string | true | none | Your address line 1 | | address_city | string | true | none | Your city | | address_postal_code | string | true | none | Your postal code | | address_country | string | true | none | Your country | | address_line_2 | string | false | none | Your address line 2 | | address_state | string | false | none | Your state |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String returnAddressId = "returnAddressId_example"; // String | 
    String contentType = "application/json"; // String | 
    UpdateReturnAddressRequest updateReturnAddressRequest = new UpdateReturnAddressRequest(); // UpdateReturnAddressRequest | 
    try {
      UpdateReturnAddress result = apiInstance.updateReturnAddress(returnAddressId, contentType, updateReturnAddressRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#updateReturnAddress");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **returnAddressId** | **String**|  | |
| **contentType** | **String**|  | [optional] |
| **updateReturnAddressRequest** | [**UpdateReturnAddressRequest**](UpdateReturnAddressRequest.md)|  | [optional] |

### Return type

[**UpdateReturnAddress**](UpdateReturnAddress.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="updateSmsCampaign"></a>
# **updateSmsCampaign**
> UpdateSmsCampaign updateSmsCampaign(smsCampaignId, contentType, calculateSmsCampaignPriceRequest)

Update SMS Campaign

_Update sms campaign_  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | sms_campaign_id | path | integer(int32) | true | ID of SMS campaign to update |  ### Properties  | Name | Type | Required | Restrictions | Description | | --- | --- | --- | --- | --- | | list_id | integer(int32) | true | none | Your list id. | | name | string | true | none | Your campaign name. | | body | string | true | none | Your campaign message. | | from | string | true | [yes](http://help.clicksend.com/SMS/what-is-a-sender-id-or-sender-number) | Your sender id | | schedule | integer(int32) | false | none | Your schedule timestamp. |  Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.  &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String smsCampaignId = "smsCampaignId_example"; // String | 
    String contentType = "application/json"; // String | 
    CalculateSmsCampaignPriceRequest calculateSmsCampaignPriceRequest = new CalculateSmsCampaignPriceRequest(); // CalculateSmsCampaignPriceRequest | 
    try {
      UpdateSmsCampaign result = apiInstance.updateSmsCampaign(smsCampaignId, contentType, calculateSmsCampaignPriceRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#updateSmsCampaign");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **smsCampaignId** | **String**|  | |
| **contentType** | **String**|  | [optional] |
| **calculateSmsCampaignPriceRequest** | [**CalculateSmsCampaignPriceRequest**](CalculateSmsCampaignPriceRequest.md)|  | [optional] |

### Return type

[**UpdateSmsCampaign**](UpdateSmsCampaign.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="updateSmsDeliveryReceiptRule"></a>
# **updateSmsDeliveryReceiptRule**
> UpdateSmsDeliveryReceiptRule updateSmsDeliveryReceiptRule(receiptRuleId, contentType, createSmsDeliveryReceiptRuleRequest)

Update SMS Delivery Receipt Rule

_Update sms delivery receipt automation_  Update sms delivery receipt automation  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | receipt_rule_id | path | integer(int32) | true | Receipt rule id |  ### Properties  | Name | Type | Required | Restrictions | Description | | --- | --- | --- | --- | --- | | rule_name | string | true | none | Rule Name. | | match_type | number | true | none | Match Type. 0&#x3D;All reports. | | action | string | true | none | Action to be taken (AUTO_REPLY, EMAIL_USER, EMAIL_FIXED, URL, SMS, POLL, GROUP_SMS, MOVE_CONTACT, CREATE_CONTACT, CREATE_CONTACT_PLUS_EMAIL, CREATE_CONTACT_PLUS_NAME_EMAIL CREATE_CONTACT_PLUS_NAME, SMPP, NONE). | | action_address | string | true | none | Action address. | | enabled | number | true | none | Enabled: Disabled&#x3D;0 or Enabled&#x3D;1. |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String receiptRuleId = "receiptRuleId_example"; // String | 
    String contentType = "application/json"; // String | 
    CreateSmsDeliveryReceiptRuleRequest createSmsDeliveryReceiptRuleRequest = new CreateSmsDeliveryReceiptRuleRequest(); // CreateSmsDeliveryReceiptRuleRequest | 
    try {
      UpdateSmsDeliveryReceiptRule result = apiInstance.updateSmsDeliveryReceiptRule(receiptRuleId, contentType, createSmsDeliveryReceiptRuleRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#updateSmsDeliveryReceiptRule");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **receiptRuleId** | **String**|  | |
| **contentType** | **String**|  | [optional] |
| **createSmsDeliveryReceiptRuleRequest** | [**CreateSmsDeliveryReceiptRuleRequest**](CreateSmsDeliveryReceiptRuleRequest.md)|  | [optional] |

### Return type

[**UpdateSmsDeliveryReceiptRule**](UpdateSmsDeliveryReceiptRule.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="updateSmsInboundAutomation"></a>
# **updateSmsInboundAutomation**
> UpdateSmsInboundAutomation updateSmsInboundAutomation(inboundRuleId, contentType, updateSmsInboundAutomationRequest)

Update SMS Inbound Automation

_Update inbound sms automation_  Update inbound sms automation  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | inbound_rule_id | path | integer(int32) | true | Inbound rule id |  ### Properties  | Name | Type | Required | Restrictions | Description | | --- | --- | --- | --- | --- | | dedicated_number | string | true | none | Dedicated Number. Can be &#39;\\*&#39; to apply to all numbers. | | rule_name | string | true | none | Rule Name. | | message_search_type | number | true | none | Message Search Type: 0&#x3D;Any message, 1&#x3D;starts with, 2&#x3D;contains, 3&#x3D;does not contain. | | message_search_term | string | true | none | Message search term. | | action | string | true | none | Action to be taken (AUTO_REPLY, EMAIL_USER, EMAIL_FIXED, URL, SMS, POLL, GROUP_SMS, MOVE_CONTACT, CREATE_CONTACT, CREATE_CONTACT_PLUS_EMAIL, CREATE_CONTACT_PLUS_NAME_EMAIL CREATE_CONTACT_PLUS_NAME, SMPP, NONE). | | action_address | string | true | none | Action address. | | enabled | number | true | none | Enabled: Disabled&#x3D;0 or Enabled&#x3D;1. | | webhook_type | string | false | Required when action &#x3D; URL only | Set as post, get, or json to change the format of the request sent. |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String inboundRuleId = "inboundRuleId_example"; // String | 
    String contentType = "application/json"; // String | 
    UpdateSmsInboundAutomationRequest updateSmsInboundAutomationRequest = new UpdateSmsInboundAutomationRequest(); // UpdateSmsInboundAutomationRequest | 
    try {
      UpdateSmsInboundAutomation result = apiInstance.updateSmsInboundAutomation(inboundRuleId, contentType, updateSmsInboundAutomationRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#updateSmsInboundAutomation");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **inboundRuleId** | **String**|  | |
| **contentType** | **String**|  | [optional] |
| **updateSmsInboundAutomationRequest** | [**UpdateSmsInboundAutomationRequest**](UpdateSmsInboundAutomationRequest.md)|  | [optional] |

### Return type

[**UpdateSmsInboundAutomation**](UpdateSmsInboundAutomation.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="updateSmsTemplate"></a>
# **updateSmsTemplate**
> UpdateSmsTemplate updateSmsTemplate(templateId, contentType, createSmsTemplateRequest)

Update SMS Template

Use this endpoint to update a &lt;a href&#x3D;\&quot;https://help.clicksend.com/article/9z9uloaz8y-sms-templates-for-different-industries\&quot; target&#x3D;\&quot;_blank\&quot;&gt;SMS template&lt;/a&gt;.

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String templateId = "templateId_example"; // String | The ID of the template to update.
    String contentType = "application/json"; // String | 
    CreateSmsTemplateRequest createSmsTemplateRequest = new CreateSmsTemplateRequest(); // CreateSmsTemplateRequest | 
    try {
      UpdateSmsTemplate result = apiInstance.updateSmsTemplate(templateId, contentType, createSmsTemplateRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#updateSmsTemplate");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **templateId** | **String**| The ID of the template to update. | |
| **contentType** | **String**|  | [optional] |
| **createSmsTemplateRequest** | [**CreateSmsTemplateRequest**](CreateSmsTemplateRequest.md)|  | [optional] |

### Return type

[**UpdateSmsTemplate**](UpdateSmsTemplate.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="updateStrippedStringRule"></a>
# **updateStrippedStringRule**
> UpdateStrippedStringRule updateStrippedStringRule(ruleId, contentType, createStrippedStringRuleRequest)

Update Stripped String Rule

_Update email to sms stripped string rule_  Update email to sms stripped string rule  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | rule_id | path | integer(int32) | true | Your rule id | | stripped-string | body | string | true | String to be stripped. |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String ruleId = "ruleId_example"; // String | 
    String contentType = "application/json"; // String | 
    CreateStrippedStringRuleRequest createStrippedStringRuleRequest = new CreateStrippedStringRuleRequest(); // CreateStrippedStringRuleRequest | 
    try {
      UpdateStrippedStringRule result = apiInstance.updateStrippedStringRule(ruleId, contentType, createStrippedStringRuleRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#updateStrippedStringRule");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **ruleId** | **String**|  | |
| **contentType** | **String**|  | [optional] |
| **createStrippedStringRuleRequest** | [**CreateStrippedStringRuleRequest**](CreateStrippedStringRuleRequest.md)|  | [optional] |

### Return type

[**UpdateStrippedStringRule**](UpdateStrippedStringRule.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="updateSubaccount"></a>
# **updateSubaccount**
> UpdateSubaccount updateSubaccount(subaccountId, contentType, updateSubaccountRequest)

Update Subaccount

_Update subaccount_  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | subaccount_id | path | integer(int32) | true | ID of subaccount to update |  ### Properties  | Name | Type | Required | Restrictions | Description | | --- | --- | --- | --- | --- | | api_username | string | true | none | Your new api username. | | password | string | true | none | Your new password | | email | string | true | none | Your new email. | | phone_number | string | true | none | Your phone number in [E.164](https://en.wikipedia.org/wiki/E.164) format. | | first_name | string | true | none | Your firstname | | last_name | string | true | none | Your lastname | | access_users | integer(int1) | false | none | Flag value must be 1 for yes or 0 for no. | | access_billing | integer(int1) | false | none | Flag value must be 1 for yes or 0 for no. | | access_reporting | integer(int1) | false | none | Flag value must be 1 for yes or 0 for no. | | access_contacts | integer(int1) | false | none | Flag value must be 1 for yes or 0 for no. | | access_settings | integer(int1) | false | none | Flag value must be 1 for yes or 0 for no. |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String subaccountId = "subaccountId_example"; // String | 
    String contentType = "application/json"; // String | 
    UpdateSubaccountRequest updateSubaccountRequest = new UpdateSubaccountRequest(); // UpdateSubaccountRequest | 
    try {
      UpdateSubaccount result = apiInstance.updateSubaccount(subaccountId, contentType, updateSubaccountRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#updateSubaccount");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **subaccountId** | **String**|  | |
| **contentType** | **String**|  | [optional] |
| **updateSubaccountRequest** | [**UpdateSubaccountRequest**](UpdateSubaccountRequest.md)|  | [optional] |

### Return type

[**UpdateSubaccount**](UpdateSubaccount.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="updateVoiceDeliveryReceiptRule"></a>
# **updateVoiceDeliveryReceiptRule**
> UpdateVoiceDeliveryReceiptRule updateVoiceDeliveryReceiptRule(receiptRuleId, contentType, createSmsDeliveryReceiptRuleRequest)

Update Voice Delivery Receipt Rule

_Update voice delivery receipt automation_  Update voice delivery receipt automation  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | receipt_rule_id | path | integer(int32) | true | Receipt rule id |  ### Properties  | Name | Type | Required | Restrictions | Description | | --- | --- | --- | --- | --- | | rule_name | string | true | none | Rule Name. | | match_type | number | true | none | Match Type. 0&#x3D;All reports. | | action | string | true | none | Action to be taken (AUTO_REPLY, EMAIL_USER, EMAIL_FIXED, URL, SMS, POLL, GROUP_SMS, MOVE_CONTACT, CREATE_CONTACT, CREATE_CONTACT_PLUS_EMAIL, CREATE_CONTACT_PLUS_NAME_EMAIL CREATE_CONTACT_PLUS_NAME, SMPP, NONE). | | action_address | string | true | none | Action address. | | enabled | number | true | none | Enabled: Disabled&#x3D;0 or Enabled&#x3D;1. |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String receiptRuleId = "receiptRuleId_example"; // String | 
    String contentType = "application/json"; // String | 
    CreateSmsDeliveryReceiptRuleRequest createSmsDeliveryReceiptRuleRequest = new CreateSmsDeliveryReceiptRuleRequest(); // CreateSmsDeliveryReceiptRuleRequest | 
    try {
      UpdateVoiceDeliveryReceiptRule result = apiInstance.updateVoiceDeliveryReceiptRule(receiptRuleId, contentType, createSmsDeliveryReceiptRuleRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#updateVoiceDeliveryReceiptRule");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **receiptRuleId** | **String**|  | |
| **contentType** | **String**|  | [optional] |
| **createSmsDeliveryReceiptRuleRequest** | [**CreateSmsDeliveryReceiptRuleRequest**](CreateSmsDeliveryReceiptRuleRequest.md)|  | [optional] |

### Return type

[**UpdateVoiceDeliveryReceiptRule**](UpdateVoiceDeliveryReceiptRule.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="uploadAMediaFile"></a>
# **uploadAMediaFile**
> uploadAMediaFile(contentType, body)

Upload Media File

The &#x60;upload&#x60; endpoint provides a method for converting files from an unsupported format to a format that one of our endpoints can handle.  Files can be submitted two ways: 1. Using &#x60;base64&#x60; encoding in an &#x60;application/json&#x60; request. In this case, submit the &#x60;base64&#x60;\\-encoded file contents in the &#x60;content&#x60; field of the request body, and &#x60;convert&#x60; can be specified either also in the body or as part of the query string. 2. Using &#x60;multipart/form-data&#x60; encoding, in the same way it would be submitted using a HTML form. You may find cURL useful for this. For an example of how to do this, see one of our [SDKs](https://dashboard.clicksend.com/#/libraries-sdk/main). In this case, specify &#x60;convert&#x60; in the query string.  Note that &#x60;convert&#x60; specifies the conversion to take place. That is, what the result should be compatible with and can be any of the following:  - &#x60;fax&#x60; - &#x60;mms&#x60; - &#x60;csv&#x60; - &#x60;post&#x60; - &#x60;postcard&#x60;       All files will expire 10 minutes after being uploaded.  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | convert | query | string | true | none | | content | body | string | true | Base64-encoded file contents |  Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.  This endpoint requires authentication, [more info...](/#authentication)

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String contentType = "application/json"; // String | 
    Object body = null; // Object | 
    try {
      apiInstance.uploadAMediaFile(contentType, body);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#uploadAMediaFile");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **contentType** | **String**|  | [optional] |
| **body** | **Object**|  | [optional] |

### Return type

null (empty response body)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="verifyAllowedEmailAddress"></a>
# **verifyAllowedEmailAddress**
> VerifyAllowedEmailAddress verifyAllowedEmailAddress(emailAddressId, activationToken, contentType, verifyAllowedEmailAddressRequest)

Verify Allowed Email Address

_Verify email address using verification token_  Verify email address using verification token  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | email_address_id | path | integer(int32) | true | Allowed email address id | | activation_token | path | string | true | Your activation token. |  Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.  &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String emailAddressId = "emailAddressId_example"; // String | 
    String activationToken = "activationToken_example"; // String | 
    String contentType = "application/json"; // String | 
    VerifyAllowedEmailAddressRequest verifyAllowedEmailAddressRequest = new VerifyAllowedEmailAddressRequest(); // VerifyAllowedEmailAddressRequest | 
    try {
      VerifyAllowedEmailAddress result = apiInstance.verifyAllowedEmailAddress(emailAddressId, activationToken, contentType, verifyAllowedEmailAddressRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#verifyAllowedEmailAddress");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **emailAddressId** | **String**|  | |
| **activationToken** | **String**|  | |
| **contentType** | **String**|  | [optional] |
| **verifyAllowedEmailAddressRequest** | [**VerifyAllowedEmailAddressRequest**](VerifyAllowedEmailAddressRequest.md)|  | [optional] |

### Return type

[**VerifyAllowedEmailAddress**](VerifyAllowedEmailAddress.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="verifyOwnNumberOtp"></a>
# **verifyOwnNumberOtp**
> VerifyOwnNumberOtp verifyOwnNumberOtp(verificationId, contentType, verifyOwnNumberOtpRequest)

Verify Own Number OTP

_Request to verify an OTP for Own Number verification_  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | verification_id | path | uuid | true | ID of the Own Number verification |  ### Properties  | Name | Type | Required | Restrictions | Description | | --- | --- | --- | --- | --- | | code | string | true | none | OTP code. Length must be 6 characters | | phone_number | string | true | none | Phone number. | | country | string | false | none | Country code. |  Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.  This endpoint requires authentication, [more info...](/#authentication)

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String verificationId = "verificationId_example"; // String | 
    String contentType = "application/json"; // String | 
    VerifyOwnNumberOtpRequest verifyOwnNumberOtpRequest = new VerifyOwnNumberOtpRequest(); // VerifyOwnNumberOtpRequest | 
    try {
      VerifyOwnNumberOtp result = apiInstance.verifyOwnNumberOtp(verificationId, contentType, verifyOwnNumberOtpRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#verifyOwnNumberOtp");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **verificationId** | **String**|  | |
| **contentType** | **String**|  | [optional] |
| **verifyOwnNumberOtpRequest** | [**VerifyOwnNumberOtpRequest**](VerifyOwnNumberOtpRequest.md)|  | [optional] |

### Return type

[**VerifyOwnNumberOtp**](VerifyOwnNumberOtp.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewASpecificInboundSmsMessage"></a>
# **viewASpecificInboundSmsMessage**
> ViewASpecificInboundSmsMessage viewASpecificInboundSmsMessage(originalMessageId, contentType)

View a specific inbound SMS message

Use this endpoint to retrieve a specific inbound SMS, including those that have been marked as read.  Inbound SMS are messages sent by your recipient to you. This endpoint enables you to retrieve those inbound SMS.

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String originalMessageId = "originalMessageId_example"; // String | The _original_message_id_ of the inbound SMS to view. If the recipient replied with multiple messages, this endpoint returns the first inbound SMS received.  <div class=\"info-box\">   <h4><i class=\"fas fa-info-circle\"></i> Note:</h4>   <p>     When you receive an inbound message, you will get two parameters: <em>original_message_id</em> and <em>message_id</em>:   </p>   <ul>     <li><em>original_message_id</em>: This is the ID of the outbound message sent to the recipient</li>     <li><em>message_id</em>: This is the ID of the inbound message sent by the recipient.</li>   </ul> </div>
    String contentType = "application/json"; // String | 
    try {
      ViewASpecificInboundSmsMessage result = apiInstance.viewASpecificInboundSmsMessage(originalMessageId, contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#viewASpecificInboundSmsMessage");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **originalMessageId** | **String**| The _original_message_id_ of the inbound SMS to view. If the recipient replied with multiple messages, this endpoint returns the first inbound SMS received.  &lt;div class&#x3D;\&quot;info-box\&quot;&gt;   &lt;h4&gt;&lt;i class&#x3D;\&quot;fas fa-info-circle\&quot;&gt;&lt;/i&gt; Note:&lt;/h4&gt;   &lt;p&gt;     When you receive an inbound message, you will get two parameters: &lt;em&gt;original_message_id&lt;/em&gt; and &lt;em&gt;message_id&lt;/em&gt;:   &lt;/p&gt;   &lt;ul&gt;     &lt;li&gt;&lt;em&gt;original_message_id&lt;/em&gt;: This is the ID of the outbound message sent to the recipient&lt;/li&gt;     &lt;li&gt;&lt;em&gt;message_id&lt;/em&gt;: This is the ID of the inbound message sent by the recipient.&lt;/li&gt;   &lt;/ul&gt; &lt;/div&gt; | |
| **contentType** | **String**|  | [optional] |

### Return type

[**ViewASpecificInboundSmsMessage**](ViewASpecificInboundSmsMessage.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewASpecificSmsTemplate"></a>
# **viewASpecificSmsTemplate**
> ViewASpecificSmsTemplate viewASpecificSmsTemplate(templateId, contentType)

View a Specific SMS Template

Use this endpoint to retrieve a &lt;a href&#x3D;\&quot;https://help.clicksend.com/article/9z9uloaz8y-sms-templates-for-different-industries\&quot; target&#x3D;\&quot;_blank\&quot;&gt;SMS template&lt;/a&gt;. Specify which template to retrieve using the template ID.

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String templateId = "templateId_example"; // String | The ID of the template to retrieve
    String contentType = "application/json"; // String | 
    try {
      ViewASpecificSmsTemplate result = apiInstance.viewASpecificSmsTemplate(templateId, contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#viewASpecificSmsTemplate");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **templateId** | **String**| The ID of the template to retrieve | |
| **contentType** | **String**|  | [optional] |

### Return type

[**ViewASpecificSmsTemplate**](ViewASpecificSmsTemplate.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewAccountDetails"></a>
# **viewAccountDetails**
> ViewAccountDetails viewAccountDetails(contentType)

View Account Details

_Get account information_  Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.  &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/#pagination\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String contentType = "application/json"; // String | 
    try {
      ViewAccountDetails result = apiInstance.viewAccountDetails(contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#viewAccountDetails");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **contentType** | **String**|  | [optional] |

### Return type

[**ViewAccountDetails**](ViewAccountDetails.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewAccountUsage"></a>
# **viewAccountUsage**
> ViewAccountUsage viewAccountUsage(year, month, contentType)

View Account Usage

_Get account usage_  | **Name** | **Type** | **Required** | **Restrictions** | **Description** | | --- | --- | --- | --- | --- | | year | string | true | none | Your account usage year. Example: 2019 | | month | string | true | none | Your account usage month. Example: 4 |  Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.  &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/#pagination\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String year = "year_example"; // String | 
    String month = "month_example"; // String | 
    String contentType = "application/json"; // String | 
    try {
      ViewAccountUsage result = apiInstance.viewAccountUsage(year, month, contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#viewAccountUsage");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **year** | **String**|  | |
| **month** | **String**|  | |
| **contentType** | **String**|  | [optional] |

### Return type

[**ViewAccountUsage**](ViewAccountUsage.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewAllEmailCampaigns"></a>
# **viewAllEmailCampaigns**
> ViewAllEmailCampaigns viewAllEmailCampaigns(contentType)

View All Email Campaigns

_Get all email campaigns_  Get all email campaigns  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | page | query | integer(int32) | false | Page number | | limit | query | integer(int32) | false | Number of records per page |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String contentType = "application/json"; // String | 
    try {
      ViewAllEmailCampaigns result = apiInstance.viewAllEmailCampaigns(contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#viewAllEmailCampaigns");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **contentType** | **String**|  | [optional] |

### Return type

[**ViewAllEmailCampaigns**](ViewAllEmailCampaigns.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewAllMmsCampaigns"></a>
# **viewAllMmsCampaigns**
> ViewAllMmsCampaigns viewAllMmsCampaigns(contentType)

View All MMS Campaigns

_Get list of mms campaigns_  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | page | query | integer(int32) | false | [Page number](/#pagination) | | limit | query | integer(int32) | false | [Number of records per page](/#pagination) |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String contentType = "application/json"; // String | 
    try {
      ViewAllMmsCampaigns result = apiInstance.viewAllMmsCampaigns(contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#viewAllMmsCampaigns");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **contentType** | **String**|  | [optional] |

### Return type

[**ViewAllMmsCampaigns**](ViewAllMmsCampaigns.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewAllTransactions"></a>
# **viewAllTransactions**
> ViewAllTransactions viewAllTransactions(contentType)

View All Transactions

_Purchase a package_  Get all transactions  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | page | query | integer(int32) | false | [Page number](/#pagination) | | limit | query | integer(int32) | false | [Number of records per page](/#pagination) |  Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String contentType = "application/json"; // String | 
    try {
      ViewAllTransactions result = apiInstance.viewAllTransactions(contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#viewAllTransactions");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **contentType** | **String**|  | [optional] |

### Return type

[**ViewAllTransactions**](ViewAllTransactions.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewAllowedEmailAddress"></a>
# **viewAllowedEmailAddress**
> ViewAllowedEmailAddress viewAllowedEmailAddress(emailAddressId, contentType)

View Allowed Email Address

_Get specific email address_  Get specific email address  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | email_address_id | path | integer(int32) | true | Allowed email address id |  Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.  &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String emailAddressId = "emailAddressId_example"; // String | 
    String contentType = "application/json"; // String | 
    try {
      ViewAllowedEmailAddress result = apiInstance.viewAllowedEmailAddress(emailAddressId, contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#viewAllowedEmailAddress");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **emailAddressId** | **String**|  | |
| **contentType** | **String**|  | [optional] |

### Return type

[**ViewAllowedEmailAddress**](ViewAllowedEmailAddress.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewAllowedEmailAddresses"></a>
# **viewAllowedEmailAddresses**
> ViewAllowedEmailAddresses viewAllowedEmailAddresses(contentType)

View Allowed Email Addresses

_Get all email addresses_  Get all email addresses  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | page | query | integer(int32) | false | Page number | | limit | query | integer(int32) | false | Number of records per page |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String contentType = "application/json"; // String | 
    try {
      ViewAllowedEmailAddresses result = apiInstance.viewAllowedEmailAddresses(contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#viewAllowedEmailAddresses");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **contentType** | **String**|  | [optional] |

### Return type

[**ViewAllowedEmailAddresses**](ViewAllowedEmailAddresses.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewAllowedEmails"></a>
# **viewAllowedEmails**
> ViewAllowedEmails viewAllowedEmails(contentType)

View Allowed Emails

_Get list of email to sms allowed addresses_  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | page | query | integer(int32) | false | [Page number](/#pagination) | | limit | query | integer(int32) | false | [Number of records per page](/#pagination) |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String contentType = "application/json"; // String | 
    try {
      ViewAllowedEmails result = apiInstance.viewAllowedEmails(contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#viewAllowedEmails");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **contentType** | **String**|  | [optional] |

### Return type

[**ViewAllowedEmails**](ViewAllowedEmails.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewAvailableNumbers"></a>
# **viewAvailableNumbers**
> ViewAvailableNumbers viewAvailableNumbers(country, contentType)

View Available Numbers

_Get all dedicated numbers by country_  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | country | path | string | true | Country code to search | | search | query | string | false | Your search pattern or query. | | search_type | query | integer(int32) | false | Your strategy for searching, 0 &#x3D; starts with, 1 &#x3D; anywhere, 2 &#x3D; ends with. | | page | query | integer(int32) | false | [Page number](/#pagination) | | limit | query | integer(int32) | false | [Number of records per page](/#pagination) |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String country = "country_example"; // String | 
    String contentType = "application/json"; // String | 
    try {
      ViewAvailableNumbers result = apiInstance.viewAvailableNumbers(country, contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#viewAvailableNumbers");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **country** | **String**|  | |
| **contentType** | **String**|  | [optional] |

### Return type

[**ViewAvailableNumbers**](ViewAvailableNumbers.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewClientAccounts"></a>
# **viewClientAccounts**
> ViewClientAccounts viewClientAccounts(contentType)

View Client Accounts

_Get list of reseller accounts_  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | page | query | integer(int32) | false | [Page number](/#pagination) | | limit | query | integer(int32) | false | [Number of records per page](/#pagination) |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String contentType = "application/json"; // String | 
    try {
      ViewClientAccounts result = apiInstance.viewClientAccounts(contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#viewClientAccounts");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **contentType** | **String**|  | [optional] |

### Return type

[**ViewClientAccounts**](ViewClientAccounts.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewContactLists"></a>
# **viewContactLists**
> viewContactLists(q)

View Contact Lists

_Get list of searched contact list_  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | q | query | string | true | Your keyword or query. | | page | query | integer(int32) | false | [Page number](/#pagination) | | limit | query | integer(int32) | false | [Number of records per page](/#pagination) |  Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.  This endpoint requires authentication, [more info...](/#authentication)

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String q = "Test"; // String | 
    try {
      apiInstance.viewContactLists(q);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#viewContactLists");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **q** | **String**|  | [optional] |

### Return type

null (empty response body)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewCountries"></a>
# **viewCountries**
> ViewCountries viewCountries()

View Countries

_Get all country codes_  Get all countries   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #6BBD5B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint does not require authentication&lt;/span&gt;  &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    try {
      ViewCountries result = apiInstance.viewCountries();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#viewCountries");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**ViewCountries**](ViewCountries.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewEmailCampaign"></a>
# **viewEmailCampaign**
> ViewEmailCampaign viewEmailCampaign(emailCampaignId, contentType)

View Email Campaign

_Get specific email campaign_  Get specific email campaign  Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.  &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String emailCampaignId = "emailCampaignId_example"; // String | 
    String contentType = "application/json"; // String | 
    try {
      ViewEmailCampaign result = apiInstance.viewEmailCampaign(emailCampaignId, contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#viewEmailCampaign");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **emailCampaignId** | **String**|  | |
| **contentType** | **String**|  | [optional] |

### Return type

[**ViewEmailCampaign**](ViewEmailCampaign.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewEmailCampaignHistory"></a>
# **viewEmailCampaignHistory**
> ViewEmailCampaignHistory viewEmailCampaignHistory(emailCampaignId, contentType)

View Email Campaign History

_Get specific email campaign history_  Get specific email campaign history   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String emailCampaignId = "emailCampaignId_example"; // String | 
    String contentType = "application/json"; // String | 
    try {
      ViewEmailCampaignHistory result = apiInstance.viewEmailCampaignHistory(emailCampaignId, contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#viewEmailCampaignHistory");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **emailCampaignId** | **String**|  | |
| **contentType** | **String**|  | [optional] |

### Return type

[**ViewEmailCampaignHistory**](ViewEmailCampaignHistory.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewEmailDeliveryReceiptRule"></a>
# **viewEmailDeliveryReceiptRule**
> ViewEmailDeliveryReceiptRule viewEmailDeliveryReceiptRule(receiptRuleId, contentType)

View Email Delivery Receipt Rule

_Get specific email delivery receipt automation_  Get specific email delivery receipt automation  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | receipt_rule_id | path | integer(int32) | true | Receipt rule id |  Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.  &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String receiptRuleId = "receiptRuleId_example"; // String | 
    String contentType = "application/json"; // String | 
    try {
      ViewEmailDeliveryReceiptRule result = apiInstance.viewEmailDeliveryReceiptRule(receiptRuleId, contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#viewEmailDeliveryReceiptRule");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **receiptRuleId** | **String**|  | |
| **contentType** | **String**|  | [optional] |

### Return type

[**ViewEmailDeliveryReceiptRule**](ViewEmailDeliveryReceiptRule.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewEmailDeliveryReceiptRules"></a>
# **viewEmailDeliveryReceiptRules**
> ViewEmailDeliveryReceiptRules viewEmailDeliveryReceiptRules(contentType)

View Email Delivery Receipt Rules

_Get all email delivery receipt automations_  Get all email delivery receipt automations  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | page | query | integer(int32) | false | Page number | | limit | query | integer(int32) | false | Number of records per page |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String contentType = "application/json"; // String | 
    try {
      ViewEmailDeliveryReceiptRules result = apiInstance.viewEmailDeliveryReceiptRules(contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#viewEmailDeliveryReceiptRules");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **contentType** | **String**|  | [optional] |

### Return type

[**ViewEmailDeliveryReceiptRules**](ViewEmailDeliveryReceiptRules.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewEmailHistory"></a>
# **viewEmailHistory**
> ViewEmailHistory viewEmailHistory(contentType)

View Email History

_Get all transactional email history_  Get all transactional email history  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | date_from | query | integer(int32) | false | Start date (Unix Timestamp e.g. 1436849372) | | date_to | query | integer(int32) | false | End date (Unix Timestamp e.g. 1436879372) | | page | query | integer(int32) | false | [Page number](/#pagination) | | limit | query | integer(int32) | false | [Number of records per page](/#pagination) |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String contentType = "application/json"; // String | 
    try {
      ViewEmailHistory result = apiInstance.viewEmailHistory(contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#viewEmailHistory");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **contentType** | **String**|  | [optional] |

### Return type

[**ViewEmailHistory**](ViewEmailHistory.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewEmailTemplate"></a>
# **viewEmailTemplate**
> ViewEmailTemplate viewEmailTemplate(templateId, contentType)

View Email Template

_Get specific user email template_  Get specific user email templates  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | template_id | path | integer(int32) | true | Email template id |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String templateId = "templateId_example"; // String | 
    String contentType = "application/json"; // String | 
    try {
      ViewEmailTemplate result = apiInstance.viewEmailTemplate(templateId, contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#viewEmailTemplate");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **templateId** | **String**|  | |
| **contentType** | **String**|  | [optional] |

### Return type

[**ViewEmailTemplate**](ViewEmailTemplate.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewEmailTemplates"></a>
# **viewEmailTemplates**
> ViewEmailTemplates viewEmailTemplates(contentType)

View Email Templates

_Get all user email templates_  Get all user email templates  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | page | query | integer(int32) | false | Page number | | limit | query | integer(int32) | false | Number of records per page |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String contentType = "application/json"; // String | 
    try {
      ViewEmailTemplates result = apiInstance.viewEmailTemplates(contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#viewEmailTemplates");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **contentType** | **String**|  | [optional] |

### Return type

[**ViewEmailTemplates**](ViewEmailTemplates.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewFaxDeliveryReceiptRule"></a>
# **viewFaxDeliveryReceiptRule**
> ViewFaxDeliveryReceiptRule viewFaxDeliveryReceiptRule(receiptRuleId, contentType)

View FAX Delivery Receipt Rule

_Get specific fax delivery receipt automation_  Get specific fax delivery receipt automation  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | receipt_rule_id | path | integer(int32) | true | Receipt rule id |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String receiptRuleId = "receiptRuleId_example"; // String | 
    String contentType = "application/json"; // String | 
    try {
      ViewFaxDeliveryReceiptRule result = apiInstance.viewFaxDeliveryReceiptRule(receiptRuleId, contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#viewFaxDeliveryReceiptRule");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **receiptRuleId** | **String**|  | |
| **contentType** | **String**|  | [optional] |

### Return type

[**ViewFaxDeliveryReceiptRule**](ViewFaxDeliveryReceiptRule.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewFaxDeliveryReceiptRules"></a>
# **viewFaxDeliveryReceiptRules**
> ViewFaxDeliveryReceiptRules viewFaxDeliveryReceiptRules(contentType)

View FAX Delivery Receipt Rules

_Get all fax delivery receipt automations_  Get all fax delivery receipt automations  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | page | query | integer(int32) | false | Page number | | limit | query | integer(int32) | false | Number of records per page |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String contentType = "application/json"; // String | 
    try {
      ViewFaxDeliveryReceiptRules result = apiInstance.viewFaxDeliveryReceiptRules(contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#viewFaxDeliveryReceiptRules");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **contentType** | **String**|  | [optional] |

### Return type

[**ViewFaxDeliveryReceiptRules**](ViewFaxDeliveryReceiptRules.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewFaxHistory"></a>
# **viewFaxHistory**
> ViewFaxHistory viewFaxHistory(contentType)

View Fax History

_Get a list of Fax History._  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | date_from | query | integer(int32) | false | Start date (Unix Timestamp e.g. 1436849372) | | date_to | query | integer(int32) | false | End date (Unix Timestamp e.g. 1436879372) | | q | query | string | false | Custom query Example: status:Sent,status_code:201. | | order | query | string | false | Order result by Example: date_added:desc,list_id:desc. | | page | query | integer(int32) | false | [Page number](/#pagination) | | limit | query | integer(int32) | false | [Number of records per page](/#pagination) |  Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.  This endpoint requires authentication, [more info...](/#authentication)   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String contentType = "application/json"; // String | 
    try {
      ViewFaxHistory result = apiInstance.viewFaxHistory(contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#viewFaxHistory");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **contentType** | **String**|  | [optional] |

### Return type

[**ViewFaxHistory**](ViewFaxHistory.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewFaxInboundRule"></a>
# **viewFaxInboundRule**
> ViewFaxInboundRule viewFaxInboundRule(inboundRuleId, contentType)

View Fax Inbound Rule

_Get specific inbound fax automation_  Get specific inbound fax automation  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | inbound_rule_id | path | integer(int32) | true | Inbound rule id |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String inboundRuleId = "inboundRuleId_example"; // String | 
    String contentType = "application/json"; // String | 
    try {
      ViewFaxInboundRule result = apiInstance.viewFaxInboundRule(inboundRuleId, contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#viewFaxInboundRule");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **inboundRuleId** | **String**|  | |
| **contentType** | **String**|  | [optional] |

### Return type

[**ViewFaxInboundRule**](ViewFaxInboundRule.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewFaxInboundRules"></a>
# **viewFaxInboundRules**
> ViewFaxInboundRules viewFaxInboundRules(contentType)

View Fax Inbound Rules

_Get all inbound fax automations_  Get all inbound fax automations  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | page | query | integer(int32) | false | Page number | | limit | query | integer(int32) | false | Number of records per page |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String contentType = "application/json"; // String | 
    try {
      ViewFaxInboundRules result = apiInstance.viewFaxInboundRules(contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#viewFaxInboundRules");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **contentType** | **String**|  | [optional] |

### Return type

[**ViewFaxInboundRules**](ViewFaxInboundRules.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewFaxReceipts"></a>
# **viewFaxReceipts**
> ViewFaxReceipts viewFaxReceipts(contentType)

View Fax Receipts

_Get List of Fax Receipts_  **Push Delivery Receipts**  If you prefer, we can push message replies to your server as they arrive with us.  1. Log into your account. 2. Click on your profile on the top right. 3. Then click on the Messaging Settings option. 4. Click on Fax then Delivery Reports. 5. Click the &#39;Add New Rule&#39; button. 6. Select the &#39;URL&#39; action. 7. Enter the URL and click &#39;Save&#39;.       The following variables will be posted to the URL specified:  | Variable | Description | | --- | --- | | &#x60;timestamp_send&#x60; | Timestamp of the original send request in UNIX format. e.g 1439173980 | | &#x60;timestamp&#x60; | Timestamp of delivery report in UNIX format. e.g 1439173981 | | &#x60;message_id&#x60; | Message ID, returned when originally sending the message. | | &#x60;status&#x60; | Delivered or Undelivered | | &#x60;status_code&#x60; | Status code. Refer to &#39;Fax Delivery Status Codes&#39; in docs. | | &#x60;status_text&#x60; | Status text. | | &#x60;error_code&#x60; | Error code. | | &#x60;error_text&#x60; | Error text. | | &#x60;custom_string&#x60; | A custom string used when sending the original message. | | &#x60;user_id&#x60; | The user ID of the user who sent the message. | | &#x60;subaccount_id&#x60; | The subaccount ID of the user who sent the message. | | &#x60;message_type&#x60; | &#39;fax&#39; (constant). |  **Pull Delivery Receipts**  Receive delivery reports by polling. You can poll our server and retrieve delivery reports at a time that suits you.  1. Log into your account. 2. Click on your profile on the top right. 3. Then click on the Messaging Settings option. 4. Click on Fax then Delivery Rules. 5. Click the &#39;Add New Rule&#39; button. 6. Select the &#39;Poll&#39; action. 7. Then click &#39;Save&#39;.       Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String contentType = "application/json"; // String | 
    try {
      ViewFaxReceipts result = apiInstance.viewFaxReceipts(contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#viewFaxReceipts");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **contentType** | **String**|  | [optional] |

### Return type

[**ViewFaxReceipts**](ViewFaxReceipts.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewInboundSms"></a>
# **viewInboundSms**
> ViewInboundSms viewInboundSms(contentType, page, limit)

View Inbound SMS

Use this endpoint to retrieve &lt;a href&#x3D;\&quot;https://help.clicksend.com/article/49eq1qdcui-how-do-i-receive-sms-delivery-receipts-delivery-status-updates\&quot; target&#x3D;\&quot;_blank\&quot;&gt;SMS delivery receipts&lt;/a&gt; sent by your recipient.  To be able to view receipts, add a &lt;a href&#x3D;\&quot;https://help.clicksend.com/article/ut4ttdrrai-incoming-reply-sms-options\&quot;&gt;inbound rule&lt;/a&gt; with the Action set to **POLL** in the Dashboard, or use the [**Create SMS Inbound Automation**](/automations/sms/other/create-sms-inbound-automation) endpoint.  Control [pagination](/#pagination) with the _page_ and _limit_ query parameters to specify the page of results and the number of items returned.  &lt;div class&#x3D;\&quot;info-box\&quot;&gt;   &lt;h4&gt;&lt;i class&#x3D;\&quot;fas fa-info-circle\&quot;&gt;&lt;/i&gt; Note:&lt;/h4&gt;   &lt;p&gt;If you have multiple inbound rules set to &lt;strong&gt;POLL&lt;/strong&gt;, you will receive the inbound message multiple times.&lt;/p&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String contentType = "application/json"; // String | 
    Integer page = 1; // Integer | The page number to retrieve. Use this parameter to navigate through the [pagination](/#pagination) results. The default value is 1.
    Integer limit = 15; // Integer | The number of items to return per page. This parameter controls the size of each page of results. The default value is 15.
    try {
      ViewInboundSms result = apiInstance.viewInboundSms(contentType, page, limit);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#viewInboundSms");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **contentType** | **String**|  | [optional] |
| **page** | **Integer**| The page number to retrieve. Use this parameter to navigate through the [pagination](/#pagination) results. The default value is 1. | [optional] [default to 1] |
| **limit** | **Integer**| The number of items to return per page. This parameter controls the size of each page of results. The default value is 15. | [optional] [default to 15] |

### Return type

[**ViewInboundSms**](ViewInboundSms.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewLetterHistory"></a>
# **viewLetterHistory**
> ViewLetterHistory viewLetterHistory(contentType)

View Letter History

_Get all letter history_  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | page | query | integer(int32) | false | [Page number](/#pagination) | | limit | query | integer(int32) | false | [Number of records per page](/#pagination) |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String contentType = "application/json"; // String | 
    try {
      ViewLetterHistory result = apiInstance.viewLetterHistory(contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#viewLetterHistory");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **contentType** | **String**|  | [optional] |

### Return type

[**ViewLetterHistory**](ViewLetterHistory.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewListContacts"></a>
# **viewListContacts**
> ViewListContacts viewListContacts(listId, contentType)

View List Contacts

_Get all contacts in a list_  ### parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | list_id | path | integer(int32) | true | Contact list ID | | page | query | integer(int32) | false | [Page number](/#pagination) | | limit | query | integer(int32) | false | [Number of records per page](/#pagination) | | updated_after | query | integer(int32) | false | Get all contacts updated after a given timestamp. |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String listId = "listId_example"; // String | 
    String contentType = "application/json"; // String | 
    try {
      ViewListContacts result = apiInstance.viewListContacts(listId, contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#viewListContacts");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **listId** | **String**|  | |
| **contentType** | **String**|  | [optional] |

### Return type

[**ViewListContacts**](ViewListContacts.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewLists"></a>
# **viewLists**
> ViewLists viewLists(contentType)

View Lists

_Get all contact lists_  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | page | query | integer(int32) | false | [Page number](/#pagination) | | limit | query | integer(int32) | false | [Number of records per page](/#pagination) |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String contentType = "application/json"; // String | 
    try {
      ViewLists result = apiInstance.viewLists(contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#viewLists");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **contentType** | **String**|  | [optional] |

### Return type

[**ViewLists**](ViewLists.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewMasterEmailTemplate"></a>
# **viewMasterEmailTemplate**
> ViewMasterEmailTemplate viewMasterEmailTemplate(templateId, contentType)

View Master Email Template

_Get specific master email template_  Get specific master email template  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | template_id | path | integer(int32) | true | Email template id |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String templateId = "templateId_example"; // String | 
    String contentType = "application/json"; // String | 
    try {
      ViewMasterEmailTemplate result = apiInstance.viewMasterEmailTemplate(templateId, contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#viewMasterEmailTemplate");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **templateId** | **String**|  | |
| **contentType** | **String**|  | [optional] |

### Return type

[**ViewMasterEmailTemplate**](ViewMasterEmailTemplate.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewMasterEmailTemplates"></a>
# **viewMasterEmailTemplates**
> ViewMasterEmailTemplates viewMasterEmailTemplates(contentType)

View Master Email Templates

_Get all master email templates._  Get all master email templates.  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | page | query | integer(int32) | false | Page number | | limit | query | integer(int32) | false | Number of records per page |  Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.  &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String contentType = "application/json"; // String | 
    try {
      ViewMasterEmailTemplates result = apiInstance.viewMasterEmailTemplates(contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#viewMasterEmailTemplates");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **contentType** | **String**|  | [optional] |

### Return type

[**ViewMasterEmailTemplates**](ViewMasterEmailTemplates.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewMmsCampaign"></a>
# **viewMmsCampaign**
> ViewMmsCampaign viewMmsCampaign(mmsCampaignId, contentType)

View MMS Campaign

_Get specific mms campaign_  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | mms_campaign_id | path | integer(int32) | true | ID of MMS campaign to retrieve |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String mmsCampaignId = "mmsCampaignId_example"; // String | 
    String contentType = "application/json"; // String | 
    try {
      ViewMmsCampaign result = apiInstance.viewMmsCampaign(mmsCampaignId, contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#viewMmsCampaign");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **mmsCampaignId** | **String**|  | |
| **contentType** | **String**|  | [optional] |

### Return type

[**ViewMmsCampaign**](ViewMmsCampaign.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewMmsHistory"></a>
# **viewMmsHistory**
> ViewMmsHistory viewMmsHistory(contentType, limit)

View MMS History

_Get all mms history_  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | date_from | query | integer(int32) | false | Start date (Unix Timestamp e.g. 1436849372) | | date_to | query | integer(int32) | false | End date (Unix Timestamp e.g. 1436879372) | | page | query | integer(int32) | false | [Page number](/#pagination) | | limit | query | integer(int32) | false | [Number of records per page](/#pagination) |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String contentType = "application/json"; // String | 
    Integer limit = 100; // Integer | 
    try {
      ViewMmsHistory result = apiInstance.viewMmsHistory(contentType, limit);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#viewMmsHistory");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **contentType** | **String**|  | [optional] |
| **limit** | **Integer**|  | [optional] |

### Return type

[**ViewMmsHistory**](ViewMmsHistory.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewPostcardHistory"></a>
# **viewPostcardHistory**
> ViewPostcardHistory viewPostcardHistory(contentType)

View Postcard History

_Retrieve the history of postcards sent or scheduled_  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | page | query | integer(int32) | false | [Page number](/#pagination) | | limit | query | integer(int32) | false | [Number of records per page](/#pagination) |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String contentType = "application/json"; // String | 
    try {
      ViewPostcardHistory result = apiInstance.viewPostcardHistory(contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#viewPostcardHistory");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **contentType** | **String**|  | [optional] |

### Return type

[**ViewPostcardHistory**](ViewPostcardHistory.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewRechargePackages"></a>
# **viewRechargePackages**
> ViewRechargePackages viewRechargePackages(contentType)

View Recharge Packages

_Get list of all packages_  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | country | query | string | false | Two-letter country code ([ISO3166](https://en.wikipedia.org/wiki/ISO_3166)) |  Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String contentType = "application/json"; // String | 
    try {
      ViewRechargePackages result = apiInstance.viewRechargePackages(contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#viewRechargePackages");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **contentType** | **String**|  | [optional] |

### Return type

[**ViewRechargePackages**](ViewRechargePackages.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewReferralAccounts"></a>
# **viewReferralAccounts**
> ViewReferralAccounts viewReferralAccounts(contentType)

View Referral Accounts

_Get all referral accounts_  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | page | query | integer(int32) | false | [Page number](/#pagination) | | limit | query | integer(int32) | false | [Number of records per page](/#pagination) |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String contentType = "application/json"; // String | 
    try {
      ViewReferralAccounts result = apiInstance.viewReferralAccounts(contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#viewReferralAccounts");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **contentType** | **String**|  | [optional] |

### Return type

[**ViewReferralAccounts**](ViewReferralAccounts.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewSmsCampaigns"></a>
# **viewSmsCampaigns**
> ViewSmsCampaigns viewSmsCampaigns(contentType, page, limit, q, orderBy, dateFrom, dateTo)

View SMS Campaigns

Use this endpoint to view SMS campaigns.

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String contentType = "application/json"; // String | 
    Integer page = 1; // Integer | The page number to retrieve. Use this parameter to navigate through the [pagination]/#pagination) results. The default value is 1.
    Integer limit = 15; // Integer | The number of items to return per page. This parameter controls the size of each page of results. The default value is 15.
    String q = "q_example"; // String | Allows filtering of results based on your search criteria. The query should be in the format `field_name:value`.  1. **Field Name**: The field within the SMS campaign you want to filter by. You can use the following fields:      - sms_campaign_id,name,user_id,subaccount_id,list_id,from,body,schedule,status,date_added,custom_string,url_to_shorten,unsubscribe_link,source   2. **Value**: The text or keyword you're searching for within the specified field. If left empty after the colon, the filter will look for all templates with any value in the **Field Name**.  For example, if you are searching for a SMS campaign with the status of _Scheduled_, the final query would look like this:    - `q=status:Scheduled`  <div class=\"info-box\">   <h4><i class=\"fas fa-info-circle\"></i> Note:</h4>   <p>   Some characters have to be encoded. For example, if you are searching for SMS sent from the phone number +61437085284, your search query q would be:<br/>    <ul>     <li>q=from:%2B61437085284</li>   </ul>    You can use the <a href=\"https://www.urlencoder.org/\" target=\"_blank\">URL encoder</a> to encode the text. If a character is not an alphanumeric character (A-Z, a-z, 0-9), it is typically either reserved or unsafe and should be encoded.      </p> </div>
    String orderBy = "orderBy_example"; // String | Specifies the field and order to sort the results by. The value is composed of the field name followed by a colon and the sort direction (_asc_ for ascending or _desc_ for descending).  The default sort order is by _date_added_ in ascending order. You can use the following fields:    - _name_: The name of the SMS campaign.   - _status_: The status of the SMS campaign.   - _schedule_: The schedule send date of the SMS campaign in the <a href=\"http://help.clicksend.com/what-is-a-unix-timestamp\" target=\"_blank\">Unix format</a>.   - _from_: The sender of the SMS campaign.   - _date_added_: This is the date you created or updated the SMS campaign in the <a href=\"http://help.clicksend.com/what-is-a-unix-timestamp\" target=\"_blank\">Unix format</a>.  For example, if you want to order by the most recently sent or scheduled SMS, you should sort by date in descending order. The query would look like this:    - `order_by=schedule:desc`  <div class=\"info-box\">   <h4><i class=\"fas fa-info-circle\"></i> Note:</h4>   <p>     You can also sort by these fields: <br/>     <ul>     <li>sms_campaign_id,user_id,subaccount_id,list_id,body,custom_string,url_to_shorten,unsubscribe_link, and source.</li>   </ul>   <br/>   But this is less common in practice.   </p> </div>
    Integer dateFrom = 56; // Integer | Start date to filter results. It should be in <a href=\"http://help.clicksend.com/what-is-a-unix-timestamp\" target=\"_blank\">Unix format</a>.
    Integer dateTo = 56; // Integer | End date to filter results. It should be in <a href=\"http://help.clicksend.com/what-is-a-unix-timestamp\" target=\"_blank\">Unix format</a>.
    try {
      ViewSmsCampaigns result = apiInstance.viewSmsCampaigns(contentType, page, limit, q, orderBy, dateFrom, dateTo);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#viewSmsCampaigns");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **contentType** | **String**|  | [optional] |
| **page** | **Integer**| The page number to retrieve. Use this parameter to navigate through the [pagination]/#pagination) results. The default value is 1. | [optional] [default to 1] |
| **limit** | **Integer**| The number of items to return per page. This parameter controls the size of each page of results. The default value is 15. | [optional] [default to 15] |
| **q** | **String**| Allows filtering of results based on your search criteria. The query should be in the format &#x60;field_name:value&#x60;.  1. **Field Name**: The field within the SMS campaign you want to filter by. You can use the following fields:      - sms_campaign_id,name,user_id,subaccount_id,list_id,from,body,schedule,status,date_added,custom_string,url_to_shorten,unsubscribe_link,source   2. **Value**: The text or keyword you&#39;re searching for within the specified field. If left empty after the colon, the filter will look for all templates with any value in the **Field Name**.  For example, if you are searching for a SMS campaign with the status of _Scheduled_, the final query would look like this:    - &#x60;q&#x3D;status:Scheduled&#x60;  &lt;div class&#x3D;\&quot;info-box\&quot;&gt;   &lt;h4&gt;&lt;i class&#x3D;\&quot;fas fa-info-circle\&quot;&gt;&lt;/i&gt; Note:&lt;/h4&gt;   &lt;p&gt;   Some characters have to be encoded. For example, if you are searching for SMS sent from the phone number +61437085284, your search query q would be:&lt;br/&gt;    &lt;ul&gt;     &lt;li&gt;q&#x3D;from:%2B61437085284&lt;/li&gt;   &lt;/ul&gt;    You can use the &lt;a href&#x3D;\&quot;https://www.urlencoder.org/\&quot; target&#x3D;\&quot;_blank\&quot;&gt;URL encoder&lt;/a&gt; to encode the text. If a character is not an alphanumeric character (A-Z, a-z, 0-9), it is typically either reserved or unsafe and should be encoded.      &lt;/p&gt; &lt;/div&gt; | [optional] |
| **orderBy** | **String**| Specifies the field and order to sort the results by. The value is composed of the field name followed by a colon and the sort direction (_asc_ for ascending or _desc_ for descending).  The default sort order is by _date_added_ in ascending order. You can use the following fields:    - _name_: The name of the SMS campaign.   - _status_: The status of the SMS campaign.   - _schedule_: The schedule send date of the SMS campaign in the &lt;a href&#x3D;\&quot;http://help.clicksend.com/what-is-a-unix-timestamp\&quot; target&#x3D;\&quot;_blank\&quot;&gt;Unix format&lt;/a&gt;.   - _from_: The sender of the SMS campaign.   - _date_added_: This is the date you created or updated the SMS campaign in the &lt;a href&#x3D;\&quot;http://help.clicksend.com/what-is-a-unix-timestamp\&quot; target&#x3D;\&quot;_blank\&quot;&gt;Unix format&lt;/a&gt;.  For example, if you want to order by the most recently sent or scheduled SMS, you should sort by date in descending order. The query would look like this:    - &#x60;order_by&#x3D;schedule:desc&#x60;  &lt;div class&#x3D;\&quot;info-box\&quot;&gt;   &lt;h4&gt;&lt;i class&#x3D;\&quot;fas fa-info-circle\&quot;&gt;&lt;/i&gt; Note:&lt;/h4&gt;   &lt;p&gt;     You can also sort by these fields: &lt;br/&gt;     &lt;ul&gt;     &lt;li&gt;sms_campaign_id,user_id,subaccount_id,list_id,body,custom_string,url_to_shorten,unsubscribe_link, and source.&lt;/li&gt;   &lt;/ul&gt;   &lt;br/&gt;   But this is less common in practice.   &lt;/p&gt; &lt;/div&gt; | [optional] |
| **dateFrom** | **Integer**| Start date to filter results. It should be in &lt;a href&#x3D;\&quot;http://help.clicksend.com/what-is-a-unix-timestamp\&quot; target&#x3D;\&quot;_blank\&quot;&gt;Unix format&lt;/a&gt;. | [optional] |
| **dateTo** | **Integer**| End date to filter results. It should be in &lt;a href&#x3D;\&quot;http://help.clicksend.com/what-is-a-unix-timestamp\&quot; target&#x3D;\&quot;_blank\&quot;&gt;Unix format&lt;/a&gt;. | [optional] |

### Return type

[**ViewSmsCampaigns**](ViewSmsCampaigns.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewSmsDeliveryReceiptRule"></a>
# **viewSmsDeliveryReceiptRule**
> ViewSmsDeliveryReceiptRule viewSmsDeliveryReceiptRule(receiptRuleId, contentType)

View SMS Delivery Receipt Rule

_Get specific sms delivery receipt automation_  Get specific sms delivery receipt automation  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | receipt_rule_id | path | integer(int32) | true | Receipt rule id |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String receiptRuleId = "receiptRuleId_example"; // String | 
    String contentType = "application/json"; // String | 
    try {
      ViewSmsDeliveryReceiptRule result = apiInstance.viewSmsDeliveryReceiptRule(receiptRuleId, contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#viewSmsDeliveryReceiptRule");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **receiptRuleId** | **String**|  | |
| **contentType** | **String**|  | [optional] |

### Return type

[**ViewSmsDeliveryReceiptRule**](ViewSmsDeliveryReceiptRule.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewSmsDeliveryReceiptRules"></a>
# **viewSmsDeliveryReceiptRules**
> ViewSmsDeliveryReceiptRules viewSmsDeliveryReceiptRules(contentType)

View SMS Delivery Receipt Rules

_Get all sms delivery receipt automations_  Get all sms delivery receipt automations  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | page | query | integer(int32) | false | Page number | | limit | query | integer(int32) | false | Number of records per page |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String contentType = "application/json"; // String | 
    try {
      ViewSmsDeliveryReceiptRules result = apiInstance.viewSmsDeliveryReceiptRules(contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#viewSmsDeliveryReceiptRules");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **contentType** | **String**|  | [optional] |

### Return type

[**ViewSmsDeliveryReceiptRules**](ViewSmsDeliveryReceiptRules.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewSmsHistory"></a>
# **viewSmsHistory**
> ViewSmsHistory viewSmsHistory(contentType, page, limit, q, orderBy, dateFrom, dateTo)

View SMS History

Use this endpoint to view previously sent SMS. You can filter the SMS history result using the query parameters.

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String contentType = "application/json"; // String | 
    Integer page = 1; // Integer | The page number to retrieve. Use this parameter to navigate through the [pagination](/#pagination) results. The default value is 1.
    Integer limit = 15; // Integer | The number of items to return per page. This parameter controls the size of each page of results. The default value is 15.
    String q = "field_name"; // String | Allows filtering of results based on your search criteria. The query should be in the format `field_name:value`.  1. **Field Name**: The field within the SMS history you want to filter by. You can use the following fields:          - _Status_: The status of the SMS. Available values for status are: Queued, Completed, Scheduled, WaitApproval, Failed, Cancelled, CancelledAfterReview, Received, Sent.              - _To_: The recipient of the SMS.              - _from_: The sender of the SMS.              - _subaccount_id_: The sub-account identifier.              - _message_id_: The ID of your SMS.          2. **Value**: The text or keyword you're searching for within the specified field. If left empty after the colon, the filter will look for all templates with any value in the **Field Name**.             For example, if you are searching for a SMS with the status of Scheduled, the final query would look like this:    `q=status:Scheduled`  <div class=\"info-box\">   <h4><i class=\"fas fa-info-circle\"></i> Note:</h4>   <div>    <p>Some characters have to be encoded. For example, if you are searching for SMS sent from the phone number +61437085284, your search query q would be:<br/></p>     <ul>       <li>q=from:%2B61437085284</li>     </ul>     <p>You can use the <a href=\"https://www.urlencoder.org/\" target=\"_blank\">URL encoder</a> to encode the text. If a character is not an alphanumeric character (A-Z, a-z, 0-9), it is typically either reserved or unsafe and should be encoded.</p>   </div> </div>
    String orderBy = "date:asc"; // String | Specifies the field and order to sort the results by. The value is composed of the field name followed by a colon and the sort direction (_asc_ for ascending or _desc_ for descending).  The default sort order is by _date_ in ascending order. You can use the following fields:    - _date_   - _username_   - _from_    - _to_   - _status_   - _body_  For example, if you want to order by the most recently sent SMS, you should sort by date in descending order. The query would look like this:    `order_by=date:desc`
    Integer dateFrom = 56; // Integer | Start date to filter results. It should be in <a href=\"http://help.clicksend.com/what-is-a-unix-timestamp\" target=\"_blank\">Unix format</a>.
    Integer dateTo = 56; // Integer | End date to filter results. It should be in <a href=\"http://help.clicksend.com/what-is-a-unix-timestamp\" target=\"_blank\">Unix format</a>.
    try {
      ViewSmsHistory result = apiInstance.viewSmsHistory(contentType, page, limit, q, orderBy, dateFrom, dateTo);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#viewSmsHistory");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **contentType** | **String**|  | [optional] |
| **page** | **Integer**| The page number to retrieve. Use this parameter to navigate through the [pagination](/#pagination) results. The default value is 1. | [optional] [default to 1] |
| **limit** | **Integer**| The number of items to return per page. This parameter controls the size of each page of results. The default value is 15. | [optional] [default to 15] |
| **q** | **String**| Allows filtering of results based on your search criteria. The query should be in the format &#x60;field_name:value&#x60;.  1. **Field Name**: The field within the SMS history you want to filter by. You can use the following fields:          - _Status_: The status of the SMS. Available values for status are: Queued, Completed, Scheduled, WaitApproval, Failed, Cancelled, CancelledAfterReview, Received, Sent.              - _To_: The recipient of the SMS.              - _from_: The sender of the SMS.              - _subaccount_id_: The sub-account identifier.              - _message_id_: The ID of your SMS.          2. **Value**: The text or keyword you&#39;re searching for within the specified field. If left empty after the colon, the filter will look for all templates with any value in the **Field Name**.             For example, if you are searching for a SMS with the status of Scheduled, the final query would look like this:    &#x60;q&#x3D;status:Scheduled&#x60;  &lt;div class&#x3D;\&quot;info-box\&quot;&gt;   &lt;h4&gt;&lt;i class&#x3D;\&quot;fas fa-info-circle\&quot;&gt;&lt;/i&gt; Note:&lt;/h4&gt;   &lt;div&gt;    &lt;p&gt;Some characters have to be encoded. For example, if you are searching for SMS sent from the phone number +61437085284, your search query q would be:&lt;br/&gt;&lt;/p&gt;     &lt;ul&gt;       &lt;li&gt;q&#x3D;from:%2B61437085284&lt;/li&gt;     &lt;/ul&gt;     &lt;p&gt;You can use the &lt;a href&#x3D;\&quot;https://www.urlencoder.org/\&quot; target&#x3D;\&quot;_blank\&quot;&gt;URL encoder&lt;/a&gt; to encode the text. If a character is not an alphanumeric character (A-Z, a-z, 0-9), it is typically either reserved or unsafe and should be encoded.&lt;/p&gt;   &lt;/div&gt; &lt;/div&gt; | [optional] [default to field_name] |
| **orderBy** | **String**| Specifies the field and order to sort the results by. The value is composed of the field name followed by a colon and the sort direction (_asc_ for ascending or _desc_ for descending).  The default sort order is by _date_ in ascending order. You can use the following fields:    - _date_   - _username_   - _from_    - _to_   - _status_   - _body_  For example, if you want to order by the most recently sent SMS, you should sort by date in descending order. The query would look like this:    &#x60;order_by&#x3D;date:desc&#x60; | [optional] [default to date:asc] |
| **dateFrom** | **Integer**| Start date to filter results. It should be in &lt;a href&#x3D;\&quot;http://help.clicksend.com/what-is-a-unix-timestamp\&quot; target&#x3D;\&quot;_blank\&quot;&gt;Unix format&lt;/a&gt;. | [optional] |
| **dateTo** | **Integer**| End date to filter results. It should be in &lt;a href&#x3D;\&quot;http://help.clicksend.com/what-is-a-unix-timestamp\&quot; target&#x3D;\&quot;_blank\&quot;&gt;Unix format&lt;/a&gt;. | [optional] |

### Return type

[**ViewSmsHistory**](ViewSmsHistory.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewSmsInboundAutomation"></a>
# **viewSmsInboundAutomation**
> ViewSmsInboundAutomation viewSmsInboundAutomation(inboundRuleId, contentType)

View SMS Inbound Automation

_Get specific inbound sms automation_  Get specific inbound sms automation  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | inbound_rule_id | path | integer(int32) | true | Inbound rule id |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String inboundRuleId = "inboundRuleId_example"; // String | 
    String contentType = "application/json"; // String | 
    try {
      ViewSmsInboundAutomation result = apiInstance.viewSmsInboundAutomation(inboundRuleId, contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#viewSmsInboundAutomation");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **inboundRuleId** | **String**|  | |
| **contentType** | **String**|  | [optional] |

### Return type

[**ViewSmsInboundAutomation**](ViewSmsInboundAutomation.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewSmsInboundAutomations"></a>
# **viewSmsInboundAutomations**
> ViewSmsInboundAutomations viewSmsInboundAutomations(contentType)

View SMS Inbound Automations

_Get all inbound sms automations_  Get all inbound sms automations  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | page | query | integer(int32) | false | Page number | | limit | query | integer(int32) | false | Number of records per page |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String contentType = "application/json"; // String | 
    try {
      ViewSmsInboundAutomations result = apiInstance.viewSmsInboundAutomations(contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#viewSmsInboundAutomations");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **contentType** | **String**|  | [optional] |

### Return type

[**ViewSmsInboundAutomations**](ViewSmsInboundAutomations.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewSmsReceipts"></a>
# **viewSmsReceipts**
> ViewSmsReceipts viewSmsReceipts(contentType, page, limit)

View SMS Receipts

Use this endpoint to retrieve &lt;a href&#x3D;\&quot;https://help.clicksend.com/article/49eq1qdcui-how-do-i-receive-sms-delivery-receipts-delivery-status-updates\&quot; target&#x3D;\&quot;_blank\&quot;&gt;SMS delivery receipts&lt;/a&gt; sent by your recipient.  To be able to view receipts, add a &lt;a href&#x3D;\&quot;https://help.clicksend.com/en/articles/42317-delivery-notifications-reports\&quot; target&#x3D;\&quot;_blank\&quot;&gt;delivery report&lt;/a&gt; rule with the Action set to **POLL** in the Dashboard, or use the [**Create SMS Delivery Receipt Rule**](/automations/sms/other/create-sms-delivery-receipt-rule) endpoint.  Control [pagination](/#pagination) with the _page_ and _limit_ query parameters to specify the page of results and the number of items returned.

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String contentType = "application/json"; // String | 
    Integer page = 1; // Integer | The page number to retrieve. Use this parameter to navigate through the [pagination](/#pagination) results. The default value is 1.
    Integer limit = 15; // Integer | The number of items to return per page. This parameter controls the size of each page of results. The default value is 15.
    try {
      ViewSmsReceipts result = apiInstance.viewSmsReceipts(contentType, page, limit);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#viewSmsReceipts");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **contentType** | **String**|  | [optional] |
| **page** | **Integer**| The page number to retrieve. Use this parameter to navigate through the [pagination](/#pagination) results. The default value is 1. | [optional] [default to 1] |
| **limit** | **Integer**| The number of items to return per page. This parameter controls the size of each page of results. The default value is 15. | [optional] [default to 15] |

### Return type

[**ViewSmsReceipts**](ViewSmsReceipts.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewSmsStatistics"></a>
# **viewSmsStatistics**
> ViewSmsStatistics viewSmsStatistics(contentType)

View SMS Statistics

_Get sms statistics_   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String contentType = "application/json"; // String | 
    try {
      ViewSmsStatistics result = apiInstance.viewSmsStatistics(contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#viewSmsStatistics");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **contentType** | **String**|  | [optional] |

### Return type

[**ViewSmsStatistics**](ViewSmsStatistics.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewSmsTemplates"></a>
# **viewSmsTemplates**
> ViewSmsTemplates viewSmsTemplates(contentType, page, limit, q, orderBy)

View SMS Templates

Use this endpoint to retrieve &lt;a href&#x3D;\&quot;https://help.clicksend.com/article/9z9uloaz8y-sms-templates-for-different-industries\&quot; target&#x3D;\&quot;_blank\&quot;&gt;SMS templates&lt;/a&gt;. You can filter the SMS templates result using the query parameters.

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String contentType = "application/json"; // String | 
    Integer page = 1; // Integer | The page number to retrieve. Use this parameter to navigate through the [pagination](/#pagination) results. The default value is 1.
    Integer limit = 15; // Integer | The number of items to return per page. This parameter controls the size of each page of results. The default value is 15.
    String q = "field_name"; // String | Allows filtering of results based on your search criteria. The query should be in the format `field_name:value`.  1. **Field Name**: The field within the SMS history you want to filter by. You can use the following fields:    - _template_id_ : The ID of the template   - _template_name_ : The name of the template   - _body_ : The body content of the template.          2. **Value**: The text or keyword you're searching for within the specified field. If left empty after the colon, the filter will look for all templates with any value in the **Field Name**.      For example, if you are searching for the template with the name of _sample_name_, the final query would look like this:     `q=template_name:sample_name`  <div class=\"info-box\">   <h4><i class=\"fas fa-info-circle\"></i> Note:</h4>   <div>    <p>Some characters have to be encoded. For example, if you are searching for SMS sent from the phone number +61437085284, your search query q would be:<br/></p>     <ul>       <li>q=from:%2B61437085284</li>     </ul>     <p>You can use the <a href=\"https://www.urlencoder.org/\" target=\"_blank\">URL encoder</a> to encode the text. If a character is not an alphanumeric character (A-Z, a-z, 0-9), it is typically either reserved or unsafe and should be encoded.</p>   </div> </div>
    String orderBy = "template_id:asc"; // String | Specifies the field and order to sort the results by.  The value is composed of the field name followed by a colon and the sort direction (_asc_ for ascending or _desc_ for descending).  The default sort order is by _template_id_ in ascending order. You can use the following fields:      - _template_id_ : The ID of the Template - _template_name_ : The name of the Template - _body_ : The body content of the Template  For example, if you want to order by the _template_id_ in descending order, the query would look like this:    `order_by=template_id:desc`
    try {
      ViewSmsTemplates result = apiInstance.viewSmsTemplates(contentType, page, limit, q, orderBy);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#viewSmsTemplates");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **contentType** | **String**|  | [optional] |
| **page** | **Integer**| The page number to retrieve. Use this parameter to navigate through the [pagination](/#pagination) results. The default value is 1. | [optional] [default to 1] |
| **limit** | **Integer**| The number of items to return per page. This parameter controls the size of each page of results. The default value is 15. | [optional] [default to 15] |
| **q** | **String**| Allows filtering of results based on your search criteria. The query should be in the format &#x60;field_name:value&#x60;.  1. **Field Name**: The field within the SMS history you want to filter by. You can use the following fields:    - _template_id_ : The ID of the template   - _template_name_ : The name of the template   - _body_ : The body content of the template.          2. **Value**: The text or keyword you&#39;re searching for within the specified field. If left empty after the colon, the filter will look for all templates with any value in the **Field Name**.      For example, if you are searching for the template with the name of _sample_name_, the final query would look like this:     &#x60;q&#x3D;template_name:sample_name&#x60;  &lt;div class&#x3D;\&quot;info-box\&quot;&gt;   &lt;h4&gt;&lt;i class&#x3D;\&quot;fas fa-info-circle\&quot;&gt;&lt;/i&gt; Note:&lt;/h4&gt;   &lt;div&gt;    &lt;p&gt;Some characters have to be encoded. For example, if you are searching for SMS sent from the phone number +61437085284, your search query q would be:&lt;br/&gt;&lt;/p&gt;     &lt;ul&gt;       &lt;li&gt;q&#x3D;from:%2B61437085284&lt;/li&gt;     &lt;/ul&gt;     &lt;p&gt;You can use the &lt;a href&#x3D;\&quot;https://www.urlencoder.org/\&quot; target&#x3D;\&quot;_blank\&quot;&gt;URL encoder&lt;/a&gt; to encode the text. If a character is not an alphanumeric character (A-Z, a-z, 0-9), it is typically either reserved or unsafe and should be encoded.&lt;/p&gt;   &lt;/div&gt; &lt;/div&gt; | [optional] [default to field_name] |
| **orderBy** | **String**| Specifies the field and order to sort the results by.  The value is composed of the field name followed by a colon and the sort direction (_asc_ for ascending or _desc_ for descending).  The default sort order is by _template_id_ in ascending order. You can use the following fields:      - _template_id_ : The ID of the Template - _template_name_ : The name of the Template - _body_ : The body content of the Template  For example, if you want to order by the _template_id_ in descending order, the query would look like this:    &#x60;order_by&#x3D;template_id:desc&#x60; | [optional] [default to template_id:asc] |

### Return type

[**ViewSmsTemplates**](ViewSmsTemplates.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewSpecificClientAccount"></a>
# **viewSpecificClientAccount**
> ViewSpecificClientAccount viewSpecificClientAccount(clientUserId, contentType)

View Specific Client Account

_Get Reseller clients Account_  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | client_user_id | path | integer(int32) | true | User ID of client |  Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.  &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String clientUserId = "clientUserId_example"; // String | 
    String contentType = "application/json"; // String | 
    try {
      ViewSpecificClientAccount result = apiInstance.viewSpecificClientAccount(clientUserId, contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#viewSpecificClientAccount");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **clientUserId** | **String**|  | |
| **contentType** | **String**|  | [optional] |

### Return type

[**ViewSpecificClientAccount**](ViewSpecificClientAccount.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewSpecificFaxReceipt"></a>
# **viewSpecificFaxReceipt**
> ViewSpecificFaxReceipt viewSpecificFaxReceipt(messageId, contentType)

View Specific Fax Receipt

_Get a single fax receipt based on message id._  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | message_id | path | string | true | ID of the message receipt to retrieve |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String messageId = "messageId_example"; // String | 
    String contentType = "application/json"; // String | 
    try {
      ViewSpecificFaxReceipt result = apiInstance.viewSpecificFaxReceipt(messageId, contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#viewSpecificFaxReceipt");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **messageId** | **String**|  | |
| **contentType** | **String**|  | [optional] |

### Return type

[**ViewSpecificFaxReceipt**](ViewSpecificFaxReceipt.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewSpecificList"></a>
# **viewSpecificList**
> ViewSpecificList viewSpecificList(listId, contentType)

View Specific List

_Get specific contact list_  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | list_id | path | integer(int32) | true | List ID |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String listId = "listId_example"; // String | 
    String contentType = "application/json"; // String | 
    try {
      ViewSpecificList result = apiInstance.viewSpecificList(listId, contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#viewSpecificList");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **listId** | **String**|  | |
| **contentType** | **String**|  | [optional] |

### Return type

[**ViewSpecificList**](ViewSpecificList.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewSpecificReturnAddress"></a>
# **viewSpecificReturnAddress**
> ViewSpecificReturnAddress viewSpecificReturnAddress(returnAddressId, contentType)

View Specific Return Address

_Get specific post return address_  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | return_address_id | path | integer(int32) | true | Return address ID |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String returnAddressId = "returnAddressId_example"; // String | 
    String contentType = "application/json"; // String | 
    try {
      ViewSpecificReturnAddress result = apiInstance.viewSpecificReturnAddress(returnAddressId, contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#viewSpecificReturnAddress");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **returnAddressId** | **String**|  | |
| **contentType** | **String**|  | [optional] |

### Return type

[**ViewSpecificReturnAddress**](ViewSpecificReturnAddress.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewSpecificSmsCampaign"></a>
# **viewSpecificSmsCampaign**
> ViewSpecificSmsCampaign viewSpecificSmsCampaign(smsCampaignId, contentType)

View Specific SMS Campaign

Use this endpoint to view a specific SMS campaign.

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String smsCampaignId = "smsCampaignId_example"; // String | ID of SMS campaign to get
    String contentType = "application/json"; // String | 
    try {
      ViewSpecificSmsCampaign result = apiInstance.viewSpecificSmsCampaign(smsCampaignId, contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#viewSpecificSmsCampaign");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **smsCampaignId** | **String**| ID of SMS campaign to get | |
| **contentType** | **String**|  | [optional] |

### Return type

[**ViewSpecificSmsCampaign**](ViewSpecificSmsCampaign.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewSpecificSmsReceipt"></a>
# **viewSpecificSmsReceipt**
> ViewSpecificSmsReceipt viewSpecificSmsReceipt(messageId, contentType)

View Specific SMS Receipt

Use this endpoint to retrieve a specific &lt;a href&#x3D;\&quot;https://help.clicksend.com/article/49eq1qdcui-how-do-i-receive-sms-delivery-receipts-delivery-status-updates\&quot; target&#x3D;\&quot;_blank\&quot;&gt;SMS delivery receipt&lt;/a&gt;, including those that have been marked as read. When you send an SMS, a delivery receipt is generated and can be received.  This endpoint enables you to retrieve those receipts.

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String messageId = "messageId_example"; // String | The _message_id_ of the SMS delivery receipt to retrieve
    String contentType = "application/json"; // String | 
    try {
      ViewSpecificSmsReceipt result = apiInstance.viewSpecificSmsReceipt(messageId, contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#viewSpecificSmsReceipt");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **messageId** | **String**| The _message_id_ of the SMS delivery receipt to retrieve | |
| **contentType** | **String**|  | [optional] |

### Return type

[**ViewSpecificSmsReceipt**](ViewSpecificSmsReceipt.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewSpecificSubaccount"></a>
# **viewSpecificSubaccount**
> ViewSpecificSubaccount viewSpecificSubaccount(subaccountId, contentType)

View Specific Subaccount

_Get specific subaccount_  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | subaccount_id | path | integer(int32) | true | ID of subaccount to get |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String subaccountId = "subaccountId_example"; // String | 
    String contentType = "application/json"; // String | 
    try {
      ViewSpecificSubaccount result = apiInstance.viewSpecificSubaccount(subaccountId, contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#viewSpecificSubaccount");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **subaccountId** | **String**|  | |
| **contentType** | **String**|  | [optional] |

### Return type

[**ViewSpecificSubaccount**](ViewSpecificSubaccount.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewSpecificTransaction"></a>
# **viewSpecificTransaction**
> ViewSpecificTransaction viewSpecificTransaction(transactionId, contentType)

View Specific Transaction

_Get specific Transaction_  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | transaction_id | path | string | true | ID of transaction to retrieve |  Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String transactionId = "transactionId_example"; // String | 
    String contentType = "application/json"; // String | 
    try {
      ViewSpecificTransaction result = apiInstance.viewSpecificTransaction(transactionId, contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#viewSpecificTransaction");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **transactionId** | **String**|  | |
| **contentType** | **String**|  | [optional] |

### Return type

[**ViewSpecificTransaction**](ViewSpecificTransaction.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewStrippedStringRule"></a>
# **viewStrippedStringRule**
> ViewStrippedStringRule viewStrippedStringRule(ruleId, contentType)

View Stripped String Rule

_Get email to sms stripped string rule_  Get email to sms stripped string rule  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | rule_id | path | integer(int32) | true | Your rule id |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String ruleId = "ruleId_example"; // String | 
    String contentType = "application/json"; // String | 
    try {
      ViewStrippedStringRule result = apiInstance.viewStrippedStringRule(ruleId, contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#viewStrippedStringRule");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **ruleId** | **String**|  | |
| **contentType** | **String**|  | [optional] |

### Return type

[**ViewStrippedStringRule**](ViewStrippedStringRule.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewStrippedStringRules"></a>
# **viewStrippedStringRules**
> ViewStrippedStringRules viewStrippedStringRules(contentType)

View Stripped String Rules

_Get list of email to sms stripped string rules_  Get list of email to sms stripped string rules  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | page | query | integer(int32) | false | Page number | | limit | query | integer(int32) | false | Number of records per page |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String contentType = "application/json"; // String | 
    try {
      ViewStrippedStringRules result = apiInstance.viewStrippedStringRules(contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#viewStrippedStringRules");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **contentType** | **String**|  | [optional] |

### Return type

[**ViewStrippedStringRules**](ViewStrippedStringRules.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewSubaccounts"></a>
# **viewSubaccounts**
> ViewSubaccounts viewSubaccounts(contentType)

View Subaccounts

_Get all subaccounts_  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | page | query | integer(int32) | false | [Page number](/#pagination) | | limit | query | integer(int32) | false | [Number of records per page](/#pagination) |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String contentType = "application/json"; // String | 
    try {
      ViewSubaccounts result = apiInstance.viewSubaccounts(contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#viewSubaccounts");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **contentType** | **String**|  | [optional] |

### Return type

[**ViewSubaccounts**](ViewSubaccounts.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewTemplateCategories"></a>
# **viewTemplateCategories**
> ViewTemplateCategories viewTemplateCategories(contentType)

View Template Categories

_Get all master email template categories_  Get all master email template categories  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | page | query | integer(int32) | false | Page number | | limit | query | integer(int32) | false | Number of records per page |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String contentType = "application/json"; // String | 
    try {
      ViewTemplateCategories result = apiInstance.viewTemplateCategories(contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#viewTemplateCategories");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **contentType** | **String**|  | [optional] |

### Return type

[**ViewTemplateCategories**](ViewTemplateCategories.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewTemplateCategory"></a>
# **viewTemplateCategory**
> ViewTemplateCategory viewTemplateCategory(categoryId, contentType)

View Template Category

_Get specific master email template category_  Get specific master email template category  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | category_id | path | integer(int32) | true | Email category id |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String categoryId = "categoryId_example"; // String | 
    String contentType = "application/json"; // String | 
    try {
      ViewTemplateCategory result = apiInstance.viewTemplateCategory(categoryId, contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#viewTemplateCategory");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **categoryId** | **String**|  | |
| **contentType** | **String**|  | [optional] |

### Return type

[**ViewTemplateCategory**](ViewTemplateCategory.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewTemplatesInCategory"></a>
# **viewTemplatesInCategory**
> ViewTemplatesInCategory viewTemplatesInCategory(categoryId, contentType)

View Templates in Category

_Get all master email templates in a category_  Get all master email templates in a category  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | category_id | path | integer(int32) | true | Email category id | | page | query | integer(int32) | false | Page number | | limit | query | integer(int32) | false | Number of records per page |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String categoryId = "categoryId_example"; // String | 
    String contentType = "application/json"; // String | 
    try {
      ViewTemplatesInCategory result = apiInstance.viewTemplatesInCategory(categoryId, contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#viewTemplatesInCategory");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **categoryId** | **String**|  | |
| **contentType** | **String**|  | [optional] |

### Return type

[**ViewTemplatesInCategory**](ViewTemplatesInCategory.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewVoiceDeliveryReceiptRule"></a>
# **viewVoiceDeliveryReceiptRule**
> ViewVoiceDeliveryReceiptRule viewVoiceDeliveryReceiptRule(receiptRuleId, contentType)

View Voice Delivery Receipt Rule

_Get specific voice delivery receipt automation_  Get specific voice delivery receipt automation  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | receipt_rule_id | path | integer(int32) | true | Receipt rule id |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String receiptRuleId = "receiptRuleId_example"; // String | 
    String contentType = "application/json"; // String | 
    try {
      ViewVoiceDeliveryReceiptRule result = apiInstance.viewVoiceDeliveryReceiptRule(receiptRuleId, contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#viewVoiceDeliveryReceiptRule");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **receiptRuleId** | **String**|  | |
| **contentType** | **String**|  | [optional] |

### Return type

[**ViewVoiceDeliveryReceiptRule**](ViewVoiceDeliveryReceiptRule.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewVoiceDeliveryReceiptRules"></a>
# **viewVoiceDeliveryReceiptRules**
> ViewVoiceDeliveryReceiptRules viewVoiceDeliveryReceiptRules(contentType)

View Voice Delivery Receipt Rules

_Get all voice delivery receipt automations_  Get all voice delivery receipt automations  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | page | query | integer(int32) | false | Page number | | limit | query | integer(int32) | false | Number of records per page |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String contentType = "application/json"; // String | 
    try {
      ViewVoiceDeliveryReceiptRules result = apiInstance.viewVoiceDeliveryReceiptRules(contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#viewVoiceDeliveryReceiptRules");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **contentType** | **String**|  | [optional] |

### Return type

[**ViewVoiceDeliveryReceiptRules**](ViewVoiceDeliveryReceiptRules.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewVoiceLanguages"></a>
# **viewVoiceLanguages**
> ViewVoiceLanguages viewVoiceLanguages(contentType)

View Voice Languages

_Get all voice languages_   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String contentType = "application/json"; // String | 
    try {
      ViewVoiceLanguages result = apiInstance.viewVoiceLanguages(contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#viewVoiceLanguages");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **contentType** | **String**|  | [optional] |

### Return type

[**ViewVoiceLanguages**](ViewVoiceLanguages.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewVoiceReceipts"></a>
# **viewVoiceReceipts**
> ViewVoiceReceipts viewVoiceReceipts(contentType)

View Voice Receipts

_Get all voice receipts_  **Push Delivery Receipts**  If you prefer, we can push message replies to your server as they arrive with us.  1. Log into your account. 2. Click on your profile on the top right. 3. Then click on the Messaging Settings option. 4. Click on Voice then Delivery Report Rules. 5. Click the &#39;Add New Rule&#39; button. 6. Select the &#39;URL&#39; action. 7. Enter the URL and click &#39;Save&#39;.       The following variables will be posted to the URL specified:  | Variable | Description | | --- | --- | | &#x60;timestamp_send&#x60; | Timestamp of the original send request in UNIX format. e.g 1439173980 | | &#x60;timestamp&#x60; | Timestamp of delivery report in UNIX format. e.g 1439173981 | | &#x60;message_id&#x60; | Message ID, returned when originally sending the message. | | &#x60;status&#x60; | Delivered or Undelivered | | &#x60;status_code&#x60; | Status code. Refer to &#39;Voice Delivery Status Codes&#39; in docs. | | &#x60;status_text&#x60; | Status text. | | &#x60;error_code&#x60; | Error code. | | &#x60;error_text&#x60; | Error text. | | &#x60;custom_string&#x60; | A custom string used when sending the original message. | | &#x60;user_id&#x60; | The user ID of the user who sent the message. | | &#x60;subaccount_id&#x60; | The subaccount ID of the user who sent the message. | | &#x60;message_type&#x60; | &#39;voice&#39; (constant). | | &#x60;digits&#x60; | Numbers the recipient pressed on their keypad during the call. A blank string will be used if they didn&#39;t provide any input. |  **Pull Delivery Receipts**  Receive delivery reports by polling. You can poll our server and retrieve delivery reports at a time that suits you.  1. Log into your account. 2. Click on your profile on the top right. 3. Then click on the Messaging Settings option. 4. Click on Voice then Delivery Report Rules. 5. Click the &#39;Add New Rule&#39; button. 6. Select the &#39;Poll&#39; action. 7. Then click &#39;Save&#39;.       ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | page | query | integer(int32) | false | [Page number](/#pagination) | | limit | query | integer(int32) | false | [Number of records per page](/#pagination) |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String contentType = "application/json"; // String | 
    try {
      ViewVoiceReceipts result = apiInstance.viewVoiceReceipts(contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#viewVoiceReceipts");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **contentType** | **String**|  | [optional] |

### Return type

[**ViewVoiceReceipts**](ViewVoiceReceipts.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewVoiceStatistics"></a>
# **viewVoiceStatistics**
> ViewVoiceStatistics viewVoiceStatistics(contentType)

View Voice Statistics

_Get voice statistics_  Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.  &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String contentType = "application/json"; // String | 
    try {
      ViewVoiceStatistics result = apiInstance.viewVoiceStatistics(contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#viewVoiceStatistics");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **contentType** | **String**|  | [optional] |

### Return type

[**ViewVoiceStatistics**](ViewVoiceStatistics.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewYourNumbers"></a>
# **viewYourNumbers**
> ViewYourNumbers viewYourNumbers(contentType, page, limit, q, q2, excludingNumberType, exclude10dlcCampaign)

View Your Numbers

_Get all available dedicated numbers_  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | page | query | integer(int32) | false | [Page number](/#pagination) | | limit | query | integer(int32) | false | [Number of records per page](/#pagination) | | q | query | string | false | Filter numbers based on multiple criteria. The query string should be formatted as key-value pairs separated by commas. Available filter keys: &#x60;type&#x60;, &#x60;number_type&#x60;, &#x60;country&#x60; | | q2 | query | string | false | Filter numbers based on multiple criteria. The query string should be formatted as key-value pairs separated by commas. Available filter keys: &#x60;type&#x60; | | excluding_number_type | query | string | false | Exclude specific number types from the results. Available number types: &#x60;shortcode&#x60;, &#x60;tollfree&#x60;, &#x60;10DLC&#x60; | | exclude_10dlc_campaign | query | boolean | false | When set to true, excludes all numbers that are associated with 10DLC campaigns |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String contentType = "application/json"; // String | 
    Integer page = 1; // Integer | Page number
    Integer limit = 15; // Integer | Number of records per page
    String q = "type:sms,number_type:longcode,country:AU"; // String | Filter numbers based on multiple criteria. The query string should be formatted as key-value pairs separated by commas. Available filter keys: - `type`: Message type (e.g., `SMS`, `MMS`) - `number_type`: Number classification (e.g., `longcode`, `shortcode`, `tollfree`, `10DLC`) - `country`: Two-letter country code (e.g., `AU`, `US`) 
    String q2 = "type:mms"; // String | 
    String excludingNumberType = "10DLC"; // String | Exclude specific number types from the results. Available number types: - `shortcode` - `tollfree` - `10DLC` 
    Boolean exclude10dlcCampaign = false; // Boolean | When set to true, excludes all numbers that are associated with 10DLC campaigns
    try {
      ViewYourNumbers result = apiInstance.viewYourNumbers(contentType, page, limit, q, q2, excludingNumberType, exclude10dlcCampaign);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#viewYourNumbers");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **contentType** | **String**|  | [optional] |
| **page** | **Integer**| Page number | [optional] [default to 1] |
| **limit** | **Integer**| Number of records per page | [optional] [default to 15] |
| **q** | **String**| Filter numbers based on multiple criteria. The query string should be formatted as key-value pairs separated by commas. Available filter keys: - &#x60;type&#x60;: Message type (e.g., &#x60;SMS&#x60;, &#x60;MMS&#x60;) - &#x60;number_type&#x60;: Number classification (e.g., &#x60;longcode&#x60;, &#x60;shortcode&#x60;, &#x60;tollfree&#x60;, &#x60;10DLC&#x60;) - &#x60;country&#x60;: Two-letter country code (e.g., &#x60;AU&#x60;, &#x60;US&#x60;)  | [optional] |
| **q2** | **String**|  | [optional] |
| **excludingNumberType** | **String**| Exclude specific number types from the results. Available number types: - &#x60;shortcode&#x60; - &#x60;tollfree&#x60; - &#x60;10DLC&#x60;  | [optional] |
| **exclude10dlcCampaign** | **Boolean**| When set to true, excludes all numbers that are associated with 10DLC campaigns | [optional] [default to false] |

### Return type

[**ViewYourNumbers**](ViewYourNumbers.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

<a id="viewYourReturnAddresses"></a>
# **viewYourReturnAddresses**
> ViewYourReturnAddresses viewYourReturnAddresses(contentType)

View Your Return Addresses

_Get list of post return addresses_  ### Parameters  | Parameter | In | Type | Required | Description | | --- | --- | --- | --- | --- | | page | query | integer(int32) | false | [Page number](/#pagination) | | limit | query | integer(int32) | false | [Number of records per page](/#pagination) |   Refer to [Status Codes](/#status-codes) for definitions of HTTP status code responses.   &lt;div style&#x3D;\&quot;background-color: #FF6A4B; padding: 10px; border-radius: 8px;\&quot;&gt;   &lt;span style&#x3D;\&quot;color: white;\&quot;&gt;This endpoint requires authentication,&lt;/span&gt;    &lt;a href&#x3D;\&quot;/docs/#authentication\&quot; style&#x3D;\&quot;color: white; text-decoration: underline;\&quot;&gt;more info...&lt;/a&gt; &lt;/div&gt;

### Example
```java
// Import classes:
import ClickSend.ApiClient;
import ClickSend.ApiException;
import ClickSend.Configuration;
import ClickSend.auth.*;
import ClickSend.models.*;
import ClickSend.Api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://rest.clicksend.com");
    
    // Configure HTTP basic authorization: basicAuth
    HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
    basicAuth.setUsername("YOUR USERNAME");
    basicAuth.setPassword("YOUR PASSWORD");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String contentType = "application/json"; // String | 
    try {
      ViewYourReturnAddresses result = apiInstance.viewYourReturnAddresses(contentType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#viewYourReturnAddresses");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **contentType** | **String**|  | [optional] |

### Return type

[**ViewYourReturnAddresses**](ViewYourReturnAddresses.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |

