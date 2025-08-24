# \VerifyV2VerificationAttemptsSummaryApi

All URIs are relative to *https://verify.twilio.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**fetch_verification_attempts_summary**](VerifyV2VerificationAttemptsSummaryApi.md#fetch_verification_attempts_summary) | **GET** /v2/Attempts/Summary | Get a summary of how many attempts were made and how many were converted.



## fetch_verification_attempts_summary

> models::VerifyV2VerificationAttemptsSummary fetch_verification_attempts_summary(verify_service_sid, date_created_after, date_created_before, country, channel, destination_prefix)
Get a summary of how many attempts were made and how many were converted.

Get a summary of how many attempts were made and how many were converted.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**verify_service_sid** | Option<**String**> | Filter used to consider only Verification Attempts of the given verify service on the summary aggregation. |  |
**date_created_after** | Option<**String**> | Datetime filter used to consider only Verification Attempts created after this datetime on the summary aggregation. Given as GMT in ISO 8601 formatted datetime string: yyyy-MM-dd'T'HH:mm:ss'Z. |  |
**date_created_before** | Option<**String**> | Datetime filter used to consider only Verification Attempts created before this datetime on the summary aggregation. Given as GMT in ISO 8601 formatted datetime string: yyyy-MM-dd'T'HH:mm:ss'Z. |  |
**country** | Option<**String**> | Filter used to consider only Verification Attempts sent to the specified destination country on the summary aggregation. |  |
**channel** | Option<[**VerificationAttemptsSummaryEnumChannels**](.md)> | Filter Verification Attempts considered on the summary aggregation by communication channel. |  |
**destination_prefix** | Option<**String**> | Filter the Verification Attempts considered on the summary aggregation by Destination prefix. It is the prefix of a phone number in E.164 format. |  |

### Return type

[**models::VerifyV2VerificationAttemptsSummary**](verify.v2.verification_attempts_summary.md)

### Authorization

[accountSid_authToken](../README.md#accountSid_authToken)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

