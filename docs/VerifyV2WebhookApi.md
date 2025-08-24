# \VerifyV2WebhookApi

All URIs are relative to *https://verify.twilio.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_webhook**](VerifyV2WebhookApi.md#create_webhook) | **POST** /v2/Services/{ServiceSid}/Webhooks | Create a new Webhook for the Service
[**delete_webhook**](VerifyV2WebhookApi.md#delete_webhook) | **DELETE** /v2/Services/{ServiceSid}/Webhooks/{Sid} | Delete a specific Webhook.
[**fetch_webhook**](VerifyV2WebhookApi.md#fetch_webhook) | **GET** /v2/Services/{ServiceSid}/Webhooks/{Sid} | Fetch a specific Webhook.
[**list_webhook**](VerifyV2WebhookApi.md#list_webhook) | **GET** /v2/Services/{ServiceSid}/Webhooks | Retrieve a list of all Webhooks for a Service.
[**update_webhook**](VerifyV2WebhookApi.md#update_webhook) | **POST** /v2/Services/{ServiceSid}/Webhooks/{Sid} | 



## create_webhook

> models::VerifyV2ServiceWebhook create_webhook(service_sid, friendly_name, event_types, webhook_url, status, version)
Create a new Webhook for the Service

Create a new Webhook for the Service

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**service_sid** | **String** | The unique SID identifier of the Service. | [required] |
**friendly_name** | **String** | The string that you assigned to describe the webhook. **This value should not contain PII.** | [required] |
**event_types** | [**Vec<String>**](String.md) | The array of events that this Webhook is subscribed to. Possible event types: `*, factor.deleted, factor.created, factor.verified, challenge.approved, challenge.denied` | [required] |
**webhook_url** | **String** | The URL associated with this Webhook. | [required] |
**status** | Option<[**models::WebhookEnumStatus**](webhook_enum_status.md)> |  |  |
**version** | Option<[**models::WebhookEnumVersion**](webhook_enum_version.md)> |  |  |

### Return type

[**models::VerifyV2ServiceWebhook**](verify.v2.service.webhook.md)

### Authorization

[accountSid_authToken](../README.md#accountSid_authToken)

### HTTP request headers

- **Content-Type**: application/x-www-form-urlencoded
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_webhook

> delete_webhook(service_sid, sid)
Delete a specific Webhook.

Delete a specific Webhook.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**service_sid** | **String** | The unique SID identifier of the Service. | [required] |
**sid** | **String** | The Twilio-provided string that uniquely identifies the Webhook resource to delete. | [required] |

### Return type

 (empty response body)

### Authorization

[accountSid_authToken](../README.md#accountSid_authToken)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## fetch_webhook

> models::VerifyV2ServiceWebhook fetch_webhook(service_sid, sid)
Fetch a specific Webhook.

Fetch a specific Webhook.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**service_sid** | **String** | The unique SID identifier of the Service. | [required] |
**sid** | **String** | The Twilio-provided string that uniquely identifies the Webhook resource to fetch. | [required] |

### Return type

[**models::VerifyV2ServiceWebhook**](verify.v2.service.webhook.md)

### Authorization

[accountSid_authToken](../README.md#accountSid_authToken)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_webhook

> models::ListWebhookResponse list_webhook(service_sid, page_size, page, page_token)
Retrieve a list of all Webhooks for a Service.

Retrieve a list of all Webhooks for a Service.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**service_sid** | **String** | The unique SID identifier of the Service. | [required] |
**page_size** | Option<**i64**> | How many resources to return in each list page. The default is 50, and the maximum is 1000. |  |
**page** | Option<**i32**> | The page index. This value is simply for client state. |  |
**page_token** | Option<**String**> | The page token. This is provided by the API. |  |

### Return type

[**models::ListWebhookResponse**](ListWebhookResponse.md)

### Authorization

[accountSid_authToken](../README.md#accountSid_authToken)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_webhook

> models::VerifyV2ServiceWebhook update_webhook(service_sid, sid, friendly_name, event_types, webhook_url, status, version)




### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**service_sid** | **String** | The unique SID identifier of the Service. | [required] |
**sid** | **String** | The Twilio-provided string that uniquely identifies the Webhook resource to update. | [required] |
**friendly_name** | Option<**String**> | The string that you assigned to describe the webhook. **This value should not contain PII.** |  |
**event_types** | Option<[**Vec<String>**](String.md)> | The array of events that this Webhook is subscribed to. Possible event types: `*, factor.deleted, factor.created, factor.verified, challenge.approved, challenge.denied` |  |
**webhook_url** | Option<**String**> | The URL associated with this Webhook. |  |
**status** | Option<[**models::WebhookEnumStatus**](webhook_enum_status.md)> |  |  |
**version** | Option<[**models::WebhookEnumVersion**](webhook_enum_version.md)> |  |  |

### Return type

[**models::VerifyV2ServiceWebhook**](verify.v2.service.webhook.md)

### Authorization

[accountSid_authToken](../README.md#accountSid_authToken)

### HTTP request headers

- **Content-Type**: application/x-www-form-urlencoded
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

