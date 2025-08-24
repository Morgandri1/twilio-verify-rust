# \VerifyV2VerificationApi

All URIs are relative to *https://verify.twilio.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_verification**](VerifyV2VerificationApi.md#create_verification) | **POST** /v2/Services/{ServiceSid}/Verifications | Create a new Verification using a Service
[**fetch_verification**](VerifyV2VerificationApi.md#fetch_verification) | **GET** /v2/Services/{ServiceSid}/Verifications/{Sid} | Fetch a specific Verification
[**update_verification**](VerifyV2VerificationApi.md#update_verification) | **POST** /v2/Services/{ServiceSid}/Verifications/{Sid} | Update a Verification status



## create_verification

> models::VerifyV2ServiceVerification create_verification(service_sid, to, channel, custom_friendly_name, custom_message, send_digits, locale, custom_code, amount, payee, rate_limits, channel_configuration, app_hash, template_sid, template_custom_substitutions, device_ip, enable_sna_client_token, risk_check, tags)
Create a new Verification using a Service

Create a new Verification using a Service

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**service_sid** | **String** | The SID of the verification [Service](https://www.twilio.com/docs/verify/api/service) to create the resource under. | [required] |
**to** | **String** | The phone number or [email](https://www.twilio.com/docs/verify/email) to verify. Phone numbers must be in [E.164 format](https://www.twilio.com/docs/glossary/what-e164). | [required] |
**channel** | **String** | The verification method to use. One of: [`email`](https://www.twilio.com/docs/verify/email), `sms`, `whatsapp`, `call`, `sna` or `auto`. | [required] |
**custom_friendly_name** | Option<**String**> | A custom user defined friendly name that overwrites the existing one in the verification message |  |
**custom_message** | Option<**String**> | The text of a custom message to use for the verification. |  |
**send_digits** | Option<**String**> | The digits to send after a phone call is answered, for example, to dial an extension. For more information, see the Programmable Voice documentation of [sendDigits](https://www.twilio.com/docs/voice/twiml/number#attributes-sendDigits). |  |
**locale** | Option<**String**> | Locale will automatically resolve based on phone number country code for SMS, WhatsApp, and call channel verifications. It will fallback to English or the template’s default translation if the selected translation is not available. This parameter will override the automatic locale resolution. [See supported languages and more information here](https://www.twilio.com/docs/verify/supported-languages). |  |
**custom_code** | Option<**String**> | A pre-generated code to use for verification. The code can be between 4 and 10 characters, inclusive. |  |
**amount** | Option<**String**> | The amount of the associated PSD2 compliant transaction. Requires the PSD2 Service flag enabled. |  |
**payee** | Option<**String**> | The payee of the associated PSD2 compliant transaction. Requires the PSD2 Service flag enabled. |  |
**rate_limits** | Option<[**serde_json::Value**](serde_json::Value.md)> | The custom key-value pairs of Programmable Rate Limits. Keys correspond to `unique_name` fields defined when [creating your Rate Limit](https://www.twilio.com/docs/verify/api/service-rate-limits). Associated value pairs represent values in the request that you are rate limiting on. You may include multiple Rate Limit values in each request. |  |
**channel_configuration** | Option<[**serde_json::Value**](serde_json::Value.md)> | [`email`](https://www.twilio.com/docs/verify/email) channel configuration in json format. The fields 'from' and 'from_name' are optional but if included the 'from' field must have a valid email address. |  |
**app_hash** | Option<**String**> | Your [App Hash](https://developers.google.com/identity/sms-retriever/verify#computing_your_apps_hash_string) to be appended at the end of your verification SMS body. Applies only to SMS. Example SMS body: `<#> Your AppName verification code is: 1234 He42w354ol9`. |  |
**template_sid** | Option<**String**> | The message [template](https://www.twilio.com/docs/verify/api/templates). If provided, will override the default template for the Service. SMS and Voice channels only. |  |
**template_custom_substitutions** | Option<**String**> | A stringified JSON object in which the keys are the template's special variables and the values are the variables substitutions. |  |
**device_ip** | Option<**String**> | Strongly encouraged if using the auto channel. The IP address of the client's device. If provided, it has to be a valid IPv4 or IPv6 address. |  |
**enable_sna_client_token** | Option<**bool**> | An optional Boolean value to indicate the requirement of sna client token in the SNA URL invocation response for added security. This token must match in the Verification Check request to confirm phone number verification. |  |
**risk_check** | Option<[**models::VerificationEnumRiskCheck**](verification_enum_risk_check.md)> |  |  |
**tags** | Option<**String**> | A string containing a JSON map of key value pairs of tags to be recorded as metadata for the message. The object may contain up to 10 tags. Keys and values can each be up to 128 characters in length. |  |

### Return type

[**models::VerifyV2ServiceVerification**](verify.v2.service.verification.md)

### Authorization

[accountSid_authToken](../README.md#accountSid_authToken)

### HTTP request headers

- **Content-Type**: application/x-www-form-urlencoded
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## fetch_verification

> models::VerifyV2ServiceVerification fetch_verification(service_sid, sid)
Fetch a specific Verification

Fetch a specific Verification

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**service_sid** | **String** | The SID of the verification [Service](https://www.twilio.com/docs/verify/api/service) to fetch the resource from. | [required] |
**sid** | **String** | The Twilio-provided string that uniquely identifies the Verification resource to fetch. | [required] |

### Return type

[**models::VerifyV2ServiceVerification**](verify.v2.service.verification.md)

### Authorization

[accountSid_authToken](../README.md#accountSid_authToken)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_verification

> models::VerifyV2ServiceVerification update_verification(service_sid, sid, status)
Update a Verification status

Update a Verification status

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**service_sid** | **String** | The SID of the verification [Service](https://www.twilio.com/docs/verify/api/service) to update the resource from. | [required] |
**sid** | **String** | The Twilio-provided string that uniquely identifies the Verification resource to update. | [required] |
**status** | [**models::VerificationEnumStatus**](verification_enum_status.md) |  | [required] |

### Return type

[**models::VerifyV2ServiceVerification**](verify.v2.service.verification.md)

### Authorization

[accountSid_authToken](../README.md#accountSid_authToken)

### HTTP request headers

- **Content-Type**: application/x-www-form-urlencoded
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

