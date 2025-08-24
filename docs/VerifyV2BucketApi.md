# \VerifyV2BucketApi

All URIs are relative to *https://verify.twilio.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_bucket**](VerifyV2BucketApi.md#create_bucket) | **POST** /v2/Services/{ServiceSid}/RateLimits/{RateLimitSid}/Buckets | Create a new Bucket for a Rate Limit
[**delete_bucket**](VerifyV2BucketApi.md#delete_bucket) | **DELETE** /v2/Services/{ServiceSid}/RateLimits/{RateLimitSid}/Buckets/{Sid} | Delete a specific Bucket.
[**fetch_bucket**](VerifyV2BucketApi.md#fetch_bucket) | **GET** /v2/Services/{ServiceSid}/RateLimits/{RateLimitSid}/Buckets/{Sid} | Fetch a specific Bucket.
[**list_bucket**](VerifyV2BucketApi.md#list_bucket) | **GET** /v2/Services/{ServiceSid}/RateLimits/{RateLimitSid}/Buckets | Retrieve a list of all Buckets for a Rate Limit.
[**update_bucket**](VerifyV2BucketApi.md#update_bucket) | **POST** /v2/Services/{ServiceSid}/RateLimits/{RateLimitSid}/Buckets/{Sid} | Update a specific Bucket.



## create_bucket

> models::VerifyV2ServiceRateLimitBucket create_bucket(service_sid, rate_limit_sid, max, interval)
Create a new Bucket for a Rate Limit

Create a new Bucket for a Rate Limit

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**service_sid** | **String** | The SID of the [Service](https://www.twilio.com/docs/verify/api/service) the resource is associated with. | [required] |
**rate_limit_sid** | **String** | The Twilio-provided string that uniquely identifies the Rate Limit resource. | [required] |
**max** | **i32** | Maximum number of requests permitted in during the interval. | [required] |
**interval** | **i32** | Number of seconds that the rate limit will be enforced over. | [required] |

### Return type

[**models::VerifyV2ServiceRateLimitBucket**](verify.v2.service.rate_limit.bucket.md)

### Authorization

[accountSid_authToken](../README.md#accountSid_authToken)

### HTTP request headers

- **Content-Type**: application/x-www-form-urlencoded
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_bucket

> delete_bucket(service_sid, rate_limit_sid, sid)
Delete a specific Bucket.

Delete a specific Bucket.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**service_sid** | **String** | The SID of the [Service](https://www.twilio.com/docs/verify/api/service) the resource is associated with. | [required] |
**rate_limit_sid** | **String** | The Twilio-provided string that uniquely identifies the Rate Limit resource. | [required] |
**sid** | **String** | A 34 character string that uniquely identifies this Bucket. | [required] |

### Return type

 (empty response body)

### Authorization

[accountSid_authToken](../README.md#accountSid_authToken)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## fetch_bucket

> models::VerifyV2ServiceRateLimitBucket fetch_bucket(service_sid, rate_limit_sid, sid)
Fetch a specific Bucket.

Fetch a specific Bucket.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**service_sid** | **String** | The SID of the [Service](https://www.twilio.com/docs/verify/api/service) the resource is associated with. | [required] |
**rate_limit_sid** | **String** | The Twilio-provided string that uniquely identifies the Rate Limit resource. | [required] |
**sid** | **String** | A 34 character string that uniquely identifies this Bucket. | [required] |

### Return type

[**models::VerifyV2ServiceRateLimitBucket**](verify.v2.service.rate_limit.bucket.md)

### Authorization

[accountSid_authToken](../README.md#accountSid_authToken)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_bucket

> models::ListBucketResponse list_bucket(service_sid, rate_limit_sid, page_size, page, page_token)
Retrieve a list of all Buckets for a Rate Limit.

Retrieve a list of all Buckets for a Rate Limit.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**service_sid** | **String** | The SID of the [Service](https://www.twilio.com/docs/verify/api/service) the resource is associated with. | [required] |
**rate_limit_sid** | **String** | The Twilio-provided string that uniquely identifies the Rate Limit resource. | [required] |
**page_size** | Option<**i64**> | How many resources to return in each list page. The default is 50, and the maximum is 1000. |  |
**page** | Option<**i32**> | The page index. This value is simply for client state. |  |
**page_token** | Option<**String**> | The page token. This is provided by the API. |  |

### Return type

[**models::ListBucketResponse**](ListBucketResponse.md)

### Authorization

[accountSid_authToken](../README.md#accountSid_authToken)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_bucket

> models::VerifyV2ServiceRateLimitBucket update_bucket(service_sid, rate_limit_sid, sid, max, interval)
Update a specific Bucket.

Update a specific Bucket.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**service_sid** | **String** | The SID of the [Service](https://www.twilio.com/docs/verify/api/service) the resource is associated with. | [required] |
**rate_limit_sid** | **String** | The Twilio-provided string that uniquely identifies the Rate Limit resource. | [required] |
**sid** | **String** | A 34 character string that uniquely identifies this Bucket. | [required] |
**max** | Option<**i32**> | Maximum number of requests permitted in during the interval. |  |
**interval** | Option<**i32**> | Number of seconds that the rate limit will be enforced over. |  |

### Return type

[**models::VerifyV2ServiceRateLimitBucket**](verify.v2.service.rate_limit.bucket.md)

### Authorization

[accountSid_authToken](../README.md#accountSid_authToken)

### HTTP request headers

- **Content-Type**: application/x-www-form-urlencoded
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

