# \VerifyV2RateLimitApi

All URIs are relative to *https://verify.twilio.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_rate_limit**](VerifyV2RateLimitApi.md#create_rate_limit) | **POST** /v2/Services/{ServiceSid}/RateLimits | Create a new Rate Limit for a Service
[**delete_rate_limit**](VerifyV2RateLimitApi.md#delete_rate_limit) | **DELETE** /v2/Services/{ServiceSid}/RateLimits/{Sid} | Delete a specific Rate Limit.
[**fetch_rate_limit**](VerifyV2RateLimitApi.md#fetch_rate_limit) | **GET** /v2/Services/{ServiceSid}/RateLimits/{Sid} | Fetch a specific Rate Limit.
[**list_rate_limit**](VerifyV2RateLimitApi.md#list_rate_limit) | **GET** /v2/Services/{ServiceSid}/RateLimits | Retrieve a list of all Rate Limits for a service.
[**update_rate_limit**](VerifyV2RateLimitApi.md#update_rate_limit) | **POST** /v2/Services/{ServiceSid}/RateLimits/{Sid} | Update a specific Rate Limit.



## create_rate_limit

> models::VerifyV2ServiceRateLimit create_rate_limit(service_sid, unique_name, description)
Create a new Rate Limit for a Service

Create a new Rate Limit for a Service

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**service_sid** | **String** | The SID of the [Service](https://www.twilio.com/docs/verify/api/service) the resource is associated with. | [required] |
**unique_name** | **String** | Provides a unique and addressable name to be assigned to this Rate Limit, assigned by the developer, to be optionally used in addition to SID. **This value should not contain PII.** | [required] |
**description** | Option<**String**> | Description of this Rate Limit |  |

### Return type

[**models::VerifyV2ServiceRateLimit**](verify.v2.service.rate_limit.md)

### Authorization

[accountSid_authToken](../README.md#accountSid_authToken)

### HTTP request headers

- **Content-Type**: application/x-www-form-urlencoded
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_rate_limit

> delete_rate_limit(service_sid, sid)
Delete a specific Rate Limit.

Delete a specific Rate Limit.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**service_sid** | **String** | The SID of the [Service](https://www.twilio.com/docs/verify/api/service) the resource is associated with. | [required] |
**sid** | **String** | The Twilio-provided string that uniquely identifies the Rate Limit resource to fetch. | [required] |

### Return type

 (empty response body)

### Authorization

[accountSid_authToken](../README.md#accountSid_authToken)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## fetch_rate_limit

> models::VerifyV2ServiceRateLimit fetch_rate_limit(service_sid, sid)
Fetch a specific Rate Limit.

Fetch a specific Rate Limit.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**service_sid** | **String** | The SID of the [Service](https://www.twilio.com/docs/verify/api/service) the resource is associated with. | [required] |
**sid** | **String** | The Twilio-provided string that uniquely identifies the Rate Limit resource to fetch. | [required] |

### Return type

[**models::VerifyV2ServiceRateLimit**](verify.v2.service.rate_limit.md)

### Authorization

[accountSid_authToken](../README.md#accountSid_authToken)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_rate_limit

> models::ListRateLimitResponse list_rate_limit(service_sid, page_size, page, page_token)
Retrieve a list of all Rate Limits for a service.

Retrieve a list of all Rate Limits for a service.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**service_sid** | **String** | The SID of the [Service](https://www.twilio.com/docs/verify/api/service) the resource is associated with. | [required] |
**page_size** | Option<**i64**> | How many resources to return in each list page. The default is 50, and the maximum is 1000. |  |
**page** | Option<**i32**> | The page index. This value is simply for client state. |  |
**page_token** | Option<**String**> | The page token. This is provided by the API. |  |

### Return type

[**models::ListRateLimitResponse**](ListRateLimitResponse.md)

### Authorization

[accountSid_authToken](../README.md#accountSid_authToken)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_rate_limit

> models::VerifyV2ServiceRateLimit update_rate_limit(service_sid, sid, description)
Update a specific Rate Limit.

Update a specific Rate Limit.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**service_sid** | **String** | The SID of the [Service](https://www.twilio.com/docs/verify/api/service) the resource is associated with. | [required] |
**sid** | **String** | The Twilio-provided string that uniquely identifies the Rate Limit resource to fetch. | [required] |
**description** | Option<**String**> | Description of this Rate Limit |  |

### Return type

[**models::VerifyV2ServiceRateLimit**](verify.v2.service.rate_limit.md)

### Authorization

[accountSid_authToken](../README.md#accountSid_authToken)

### HTTP request headers

- **Content-Type**: application/x-www-form-urlencoded
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

