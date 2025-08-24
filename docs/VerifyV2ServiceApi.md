# \VerifyV2ServiceApi

All URIs are relative to *https://verify.twilio.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_service**](VerifyV2ServiceApi.md#create_service) | **POST** /v2/Services | Create a new Verification Service.
[**delete_service**](VerifyV2ServiceApi.md#delete_service) | **DELETE** /v2/Services/{Sid} | Delete a specific Verification Service Instance.
[**fetch_service**](VerifyV2ServiceApi.md#fetch_service) | **GET** /v2/Services/{Sid} | Fetch specific Verification Service Instance.
[**list_service**](VerifyV2ServiceApi.md#list_service) | **GET** /v2/Services | Retrieve a list of all Verification Services for an account.
[**update_service**](VerifyV2ServiceApi.md#update_service) | **POST** /v2/Services/{Sid} | Update a specific Verification Service.



## create_service

> models::VerifyV2Service create_service(friendly_name, code_length, lookup_enabled, skip_sms_to_landlines, dtmf_input_required, tts_name, psd2_enabled, do_not_share_warning_enabled, custom_code_enabled, push_include_date, push_apn_credential_sid, push_fcm_credential_sid, totp_issuer, totp_time_step, totp_code_length, totp_skew, default_template_sid, whatsapp_msg_service_sid, whatsapp_from, passkeys_relying_party_id, passkeys_relying_party_name, passkeys_relying_party_origins, passkeys_authenticator_attachment, passkeys_discoverable_credentials, passkeys_user_verification, verify_event_subscription_enabled)
Create a new Verification Service.

Create a new Verification Service.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**friendly_name** | **String** | A descriptive string that you create to describe the verification service. It can be up to 32 characters long. **This value should not contain PII.** | [required] |
**code_length** | Option<**i32**> | The length of the verification code to generate. Must be an integer value between 4 and 10, inclusive. |  |
**lookup_enabled** | Option<**bool**> | Whether to perform a lookup with each verification started and return info about the phone number. |  |
**skip_sms_to_landlines** | Option<**bool**> | Whether to skip sending SMS verifications to landlines. Requires `lookup_enabled`. |  |
**dtmf_input_required** | Option<**bool**> | Whether to ask the user to press a number before delivering the verify code in a phone call. |  |
**tts_name** | Option<**String**> | The name of an alternative text-to-speech service to use in phone calls. Applies only to TTS languages. |  |
**psd2_enabled** | Option<**bool**> | Whether to pass PSD2 transaction parameters when starting a verification. |  |
**do_not_share_warning_enabled** | Option<**bool**> | Whether to add a security warning at the end of an SMS verification body. Disabled by default and applies only to SMS. Example SMS body: `Your AppName verification code is: 1234. Don’t share this code with anyone; our employees will never ask for the code` |  |
**custom_code_enabled** | Option<**bool**> | Whether to allow sending verifications with a custom code instead of a randomly generated one. |  |
**push_include_date** | Option<**bool**> | Optional configuration for the Push factors. If true, include the date in the Challenge's response. Otherwise, the date is omitted from the response. See [Challenge](https://www.twilio.com/docs/verify/api/challenge) resource’s details parameter for more info. Default: false. **Deprecated** do not use this parameter. This timestamp value is the same one as the one found in `date_created`, please use that one instead. |  |
**push_apn_credential_sid** | Option<**String**> | Optional configuration for the Push factors. Set the APN Credential for this service. This will allow to send push notifications to iOS devices. See [Credential Resource](https://www.twilio.com/docs/notify/api/credential-resource) |  |
**push_fcm_credential_sid** | Option<**String**> | Optional configuration for the Push factors. Set the FCM Credential for this service. This will allow to send push notifications to Android devices. See [Credential Resource](https://www.twilio.com/docs/notify/api/credential-resource) |  |
**totp_issuer** | Option<**String**> | Optional configuration for the TOTP factors. Set TOTP Issuer for this service. This will allow to configure the issuer of the TOTP URI. Defaults to the service friendly name if not provided. |  |
**totp_time_step** | Option<**i32**> | Optional configuration for the TOTP factors. Defines how often, in seconds, are TOTP codes generated. i.e, a new TOTP code is generated every time_step seconds. Must be between 20 and 60 seconds, inclusive. Defaults to 30 seconds |  |
**totp_code_length** | Option<**i32**> | Optional configuration for the TOTP factors. Number of digits for generated TOTP codes. Must be between 3 and 8, inclusive. Defaults to 6 |  |
**totp_skew** | Option<**i32**> | Optional configuration for the TOTP factors. The number of time-steps, past and future, that are valid for validation of TOTP codes. Must be between 0 and 2, inclusive. Defaults to 1 |  |
**default_template_sid** | Option<**String**> | The default message [template](https://www.twilio.com/docs/verify/api/templates). Will be used for all SMS verifications unless explicitly overriden. SMS channel only. |  |
**whatsapp_msg_service_sid** | Option<**String**> | The SID of the Messaging Service containing WhatsApp Sender(s) that Verify will use to send WhatsApp messages to your users. |  |
**whatsapp_from** | Option<**String**> | The number to use as the WhatsApp Sender that Verify will use to send WhatsApp messages to your users.This WhatsApp Sender must be associated with a Messaging Service SID. |  |
**passkeys_relying_party_id** | Option<**String**> | The Relying Party ID for Passkeys. This is the domain of your application, e.g. `example.com`. It is used to identify your application when creating Passkeys. |  |
**passkeys_relying_party_name** | Option<**String**> | The Relying Party Name for Passkeys. This is the name of your application, e.g. `Example App`. It is used to identify your application when creating Passkeys. |  |
**passkeys_relying_party_origins** | Option<**String**> | The Relying Party Origins for Passkeys. This is the origin of your application, e.g. `login.example.com,www.example.com`. It is used to identify your application when creating Passkeys, it can have multiple origins split by `,`. |  |
**passkeys_authenticator_attachment** | Option<**String**> | The Authenticator Attachment for Passkeys. This is the type of authenticator that will be used to create Passkeys. It can be empty or it can have the values `platform`, `cross-platform` or `any`. |  |
**passkeys_discoverable_credentials** | Option<**String**> | Indicates whether credentials must be discoverable by the authenticator. It can be empty or it can have the values `required`, `preferred` or `discouraged`. |  |
**passkeys_user_verification** | Option<**String**> | The User Verification for Passkeys. This is the type of user verification that will be used to create Passkeys. It can be empty or it can have the values `required`, `preferred` or `discouraged`. |  |
**verify_event_subscription_enabled** | Option<**bool**> | Whether to allow verifications from the service to reach the stream-events sinks if configured |  |

### Return type

[**models::VerifyV2Service**](verify.v2.service.md)

### Authorization

[accountSid_authToken](../README.md#accountSid_authToken)

### HTTP request headers

- **Content-Type**: application/x-www-form-urlencoded
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_service

> delete_service(sid)
Delete a specific Verification Service Instance.

Delete a specific Verification Service Instance.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**sid** | **String** | The Twilio-provided string that uniquely identifies the Verification Service resource to delete. | [required] |

### Return type

 (empty response body)

### Authorization

[accountSid_authToken](../README.md#accountSid_authToken)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## fetch_service

> models::VerifyV2Service fetch_service(sid)
Fetch specific Verification Service Instance.

Fetch specific Verification Service Instance.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**sid** | **String** | The Twilio-provided string that uniquely identifies the Verification Service resource to fetch. | [required] |

### Return type

[**models::VerifyV2Service**](verify.v2.service.md)

### Authorization

[accountSid_authToken](../README.md#accountSid_authToken)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_service

> models::ListServiceResponse list_service(page_size, page, page_token)
Retrieve a list of all Verification Services for an account.

Retrieve a list of all Verification Services for an account.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**page_size** | Option<**i64**> | How many resources to return in each list page. The default is 50, and the maximum is 1000. |  |
**page** | Option<**i32**> | The page index. This value is simply for client state. |  |
**page_token** | Option<**String**> | The page token. This is provided by the API. |  |

### Return type

[**models::ListServiceResponse**](ListServiceResponse.md)

### Authorization

[accountSid_authToken](../README.md#accountSid_authToken)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_service

> models::VerifyV2Service update_service(sid, friendly_name, code_length, lookup_enabled, skip_sms_to_landlines, dtmf_input_required, tts_name, psd2_enabled, do_not_share_warning_enabled, custom_code_enabled, push_include_date, push_apn_credential_sid, push_fcm_credential_sid, totp_issuer, totp_time_step, totp_code_length, totp_skew, default_template_sid, whatsapp_msg_service_sid, whatsapp_from, passkeys_relying_party_id, passkeys_relying_party_name, passkeys_relying_party_origins, verify_event_subscription_enabled)
Update a specific Verification Service.

Update a specific Verification Service.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**sid** | **String** | The Twilio-provided string that uniquely identifies the Service resource to update. | [required] |
**friendly_name** | Option<**String**> | A descriptive string that you create to describe the verification service. It can be up to 32 characters long. **This value should not contain PII.** |  |
**code_length** | Option<**i32**> | The length of the verification code to generate. Must be an integer value between 4 and 10, inclusive. |  |
**lookup_enabled** | Option<**bool**> | Whether to perform a lookup with each verification started and return info about the phone number. |  |
**skip_sms_to_landlines** | Option<**bool**> | Whether to skip sending SMS verifications to landlines. Requires `lookup_enabled`. |  |
**dtmf_input_required** | Option<**bool**> | Whether to ask the user to press a number before delivering the verify code in a phone call. |  |
**tts_name** | Option<**String**> | The name of an alternative text-to-speech service to use in phone calls. Applies only to TTS languages. |  |
**psd2_enabled** | Option<**bool**> | Whether to pass PSD2 transaction parameters when starting a verification. |  |
**do_not_share_warning_enabled** | Option<**bool**> | Whether to add a privacy warning at the end of an SMS. **Disabled by default and applies only for SMS.** |  |
**custom_code_enabled** | Option<**bool**> | Whether to allow sending verifications with a custom code instead of a randomly generated one. |  |
**push_include_date** | Option<**bool**> | Optional configuration for the Push factors. If true, include the date in the Challenge's response. Otherwise, the date is omitted from the response. See [Challenge](https://www.twilio.com/docs/verify/api/challenge) resource’s details parameter for more info. Default: false. **Deprecated** do not use this parameter. |  |
**push_apn_credential_sid** | Option<**String**> | Optional configuration for the Push factors. Set the APN Credential for this service. This will allow to send push notifications to iOS devices. See [Credential Resource](https://www.twilio.com/docs/notify/api/credential-resource) |  |
**push_fcm_credential_sid** | Option<**String**> | Optional configuration for the Push factors. Set the FCM Credential for this service. This will allow to send push notifications to Android devices. See [Credential Resource](https://www.twilio.com/docs/notify/api/credential-resource) |  |
**totp_issuer** | Option<**String**> | Optional configuration for the TOTP factors. Set TOTP Issuer for this service. This will allow to configure the issuer of the TOTP URI. |  |
**totp_time_step** | Option<**i32**> | Optional configuration for the TOTP factors. Defines how often, in seconds, are TOTP codes generated. i.e, a new TOTP code is generated every time_step seconds. Must be between 20 and 60 seconds, inclusive. Defaults to 30 seconds |  |
**totp_code_length** | Option<**i32**> | Optional configuration for the TOTP factors. Number of digits for generated TOTP codes. Must be between 3 and 8, inclusive. Defaults to 6 |  |
**totp_skew** | Option<**i32**> | Optional configuration for the TOTP factors. The number of time-steps, past and future, that are valid for validation of TOTP codes. Must be between 0 and 2, inclusive. Defaults to 1 |  |
**default_template_sid** | Option<**String**> | The default message [template](https://www.twilio.com/docs/verify/api/templates). Will be used for all SMS verifications unless explicitly overriden. SMS channel only. |  |
**whatsapp_msg_service_sid** | Option<**String**> | The SID of the [Messaging Service](https://www.twilio.com/docs/messaging/services) to associate with the Verification Service. |  |
**whatsapp_from** | Option<**String**> | The WhatsApp number to use as the sender of the verification messages. This number must be associated with the WhatsApp Message Service. |  |
**passkeys_relying_party_id** | Option<**String**> | The Relying Party ID for Passkeys. This is the domain of your application, e.g. `example.com`. It is used to identify your application when creating Passkeys. |  |
**passkeys_relying_party_name** | Option<**String**> | The Relying Party Name for Passkeys. This is the name of your application, e.g. `Example App`. It is used to identify your application when creating Passkeys. |  |
**passkeys_relying_party_origins** | Option<**String**> | The Relying Party Origins for Passkeys. This is the origin of your application, e.g. `login.example.com,www.example.com`. It is used to identify your application when creating Passkeys, it can have multiple origins split by `,`. |  |
**verify_event_subscription_enabled** | Option<**bool**> | Whether to allow verifications from the service to reach the stream-events sinks if configured |  |

### Return type

[**models::VerifyV2Service**](verify.v2.service.md)

### Authorization

[accountSid_authToken](../README.md#accountSid_authToken)

### HTTP request headers

- **Content-Type**: application/x-www-form-urlencoded
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

