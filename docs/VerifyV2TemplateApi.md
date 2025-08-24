# \VerifyV2TemplateApi

All URIs are relative to *https://verify.twilio.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**list_verification_template**](VerifyV2TemplateApi.md#list_verification_template) | **GET** /v2/Templates | List all the available templates for a given Account.



## list_verification_template

> models::ListVerificationTemplateResponse list_verification_template(friendly_name, page_size, page, page_token)
List all the available templates for a given Account.

List all the available templates for a given Account.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**friendly_name** | Option<**String**> | String filter used to query templates with a given friendly name. |  |
**page_size** | Option<**i64**> | How many resources to return in each list page. The default is 50, and the maximum is 1000. |  |
**page** | Option<**i32**> | The page index. This value is simply for client state. |  |
**page_token** | Option<**String**> | The page token. This is provided by the API. |  |

### Return type

[**models::ListVerificationTemplateResponse**](ListVerificationTemplateResponse.md)

### Authorization

[accountSid_authToken](../README.md#accountSid_authToken)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

