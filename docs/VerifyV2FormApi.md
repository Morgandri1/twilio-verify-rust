# \VerifyV2FormApi

All URIs are relative to *https://verify.twilio.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**fetch_form**](VerifyV2FormApi.md#fetch_form) | **GET** /v2/Forms/{FormType} | Fetch the forms for a specific Form Type.



## fetch_form

> models::VerifyV2Form fetch_form(form_type)
Fetch the forms for a specific Form Type.

Fetch the forms for a specific Form Type.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**form_type** | [**FormEnumFormTypes**](.md) | The Type of this Form. Currently only `form-push` is supported. | [required] |

### Return type

[**models::VerifyV2Form**](verify.v2.form.md)

### Authorization

[accountSid_authToken](../README.md#accountSid_authToken)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

