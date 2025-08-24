# \VerifyV2VerificationAttemptApi

All URIs are relative to *https://verify.twilio.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**fetch_verification_attempt**](VerifyV2VerificationAttemptApi.md#fetch_verification_attempt) | **GET** /v2/Attempts/{Sid} | Fetch a specific verification attempt.
[**list_verification_attempt**](VerifyV2VerificationAttemptApi.md#list_verification_attempt) | **GET** /v2/Attempts | List all the verification attempts for a given Account.



## fetch_verification_attempt

> models::VerifyV2VerificationAttempt fetch_verification_attempt(sid)
Fetch a specific verification attempt.

Fetch a specific verification attempt.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**sid** | **String** | The unique SID identifier of a Verification Attempt | [required] |

### Return type

[**models::VerifyV2VerificationAttempt**](verify.v2.verification_attempt.md)

### Authorization

[accountSid_authToken](../README.md#accountSid_authToken)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_verification_attempt

> models::ListVerificationAttemptResponse list_verification_attempt(date_created_after, date_created_before, channel_data_to, country, channel, verify_service_sid, verification_sid, status, page_size, page, page_token)
List all the verification attempts for a given Account.

List all the verification attempts for a given Account.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**date_created_after** | Option<**String**> | Datetime filter used to consider only Verification Attempts created after this datetime on the summary aggregation. Given as GMT in ISO 8601 formatted datetime string: yyyy-MM-dd'T'HH:mm:ss'Z. |  |
**date_created_before** | Option<**String**> | Datetime filter used to consider only Verification Attempts created before this datetime on the summary aggregation. Given as GMT in ISO 8601 formatted datetime string: yyyy-MM-dd'T'HH:mm:ss'Z. |  |
**channel_data_to** | Option<**String**> | Destination of a verification. It is phone number in E.164 format. |  |
**country** | Option<**String**> | Filter used to query Verification Attempts sent to the specified destination country. |  |
**channel** | Option<[**VerificationAttemptEnumChannels**](.md)> | Filter used to query Verification Attempts by communication channel. |  |
**verify_service_sid** | Option<**String**> | Filter used to query Verification Attempts by verify service. Only attempts of the provided SID will be returned. |  |
**verification_sid** | Option<**String**> | Filter used to return all the Verification Attempts of a single verification. Only attempts of the provided verification SID will be returned. |  |
**status** | Option<[**VerificationAttemptEnumConversionStatus**](.md)> | Filter used to query Verification Attempts by conversion status. Valid values are `UNCONVERTED`, for attempts that were not converted, and `CONVERTED`, for attempts that were confirmed. |  |
**page_size** | Option<**i64**> | How many resources to return in each list page. The default is 50, and the maximum is 1000. |  |
**page** | Option<**i32**> | The page index. This value is simply for client state. |  |
**page_token** | Option<**String**> | The page token. This is provided by the API. |  |

### Return type

[**models::ListVerificationAttemptResponse**](ListVerificationAttemptResponse.md)

### Authorization

[accountSid_authToken](../README.md#accountSid_authToken)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

