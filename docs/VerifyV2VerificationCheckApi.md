# \VerifyV2VerificationCheckApi

All URIs are relative to *https://verify.twilio.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_verification_check**](VerifyV2VerificationCheckApi.md#create_verification_check) | **POST** /v2/Services/{ServiceSid}/VerificationCheck | challenge a specific Verification Check.



## create_verification_check

> models::VerifyV2ServiceVerificationCheck create_verification_check(service_sid, code, to, verification_sid, amount, payee, sna_client_token)
challenge a specific Verification Check.

challenge a specific Verification Check.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**service_sid** | **String** | The SID of the verification [Service](https://www.twilio.com/docs/verify/api/service) to create the resource under. | [required] |
**code** | Option<**String**> | The 4-10 character string being verified. |  |
**to** | Option<**String**> | The phone number or [email](https://www.twilio.com/docs/verify/email) to verify. Either this parameter or the `verification_sid` must be specified. Phone numbers must be in [E.164 format](https://www.twilio.com/docs/glossary/what-e164). |  |
**verification_sid** | Option<**String**> | A SID that uniquely identifies the Verification Check. Either this parameter or the `to` phone number/[email](https://www.twilio.com/docs/verify/email) must be specified. |  |
**amount** | Option<**String**> | The amount of the associated PSD2 compliant transaction. Requires the PSD2 Service flag enabled. |  |
**payee** | Option<**String**> | The payee of the associated PSD2 compliant transaction. Requires the PSD2 Service flag enabled. |  |
**sna_client_token** | Option<**String**> | A sna client token received in sna url invocation response needs to be passed in Verification Check request and should match to get successful response. |  |

### Return type

[**models::VerifyV2ServiceVerificationCheck**](verify.v2.service.verification_check.md)

### Authorization

[accountSid_authToken](../README.md#accountSid_authToken)

### HTTP request headers

- **Content-Type**: application/x-www-form-urlencoded
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

