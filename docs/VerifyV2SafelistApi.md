# \VerifyV2SafelistApi

All URIs are relative to *https://verify.twilio.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_safelist**](VerifyV2SafelistApi.md#create_safelist) | **POST** /v2/SafeList/Numbers | Add a new phone number to SafeList.
[**delete_safelist**](VerifyV2SafelistApi.md#delete_safelist) | **DELETE** /v2/SafeList/Numbers/{PhoneNumber} | Remove a phone number from SafeList.
[**fetch_safelist**](VerifyV2SafelistApi.md#fetch_safelist) | **GET** /v2/SafeList/Numbers/{PhoneNumber} | Check if a phone number exists in SafeList.



## create_safelist

> models::VerifyV2Safelist create_safelist(phone_number)
Add a new phone number to SafeList.

Add a new phone number to SafeList.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**phone_number** | **String** | The phone number to be added in SafeList. Phone numbers must be in [E.164 format](https://www.twilio.com/docs/glossary/what-e164). | [required] |

### Return type

[**models::VerifyV2Safelist**](verify.v2.safelist.md)

### Authorization

[accountSid_authToken](../README.md#accountSid_authToken)

### HTTP request headers

- **Content-Type**: application/x-www-form-urlencoded
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_safelist

> delete_safelist(phone_number)
Remove a phone number from SafeList.

Remove a phone number from SafeList.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**phone_number** | **String** | The phone number to be removed from SafeList. Phone numbers must be in [E.164 format](https://www.twilio.com/docs/glossary/what-e164). | [required] |

### Return type

 (empty response body)

### Authorization

[accountSid_authToken](../README.md#accountSid_authToken)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## fetch_safelist

> models::VerifyV2Safelist fetch_safelist(phone_number)
Check if a phone number exists in SafeList.

Check if a phone number exists in SafeList.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**phone_number** | **String** | The phone number to be fetched from SafeList. Phone numbers must be in [E.164 format](https://www.twilio.com/docs/glossary/what-e164). | [required] |

### Return type

[**models::VerifyV2Safelist**](verify.v2.safelist.md)

### Authorization

[accountSid_authToken](../README.md#accountSid_authToken)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

