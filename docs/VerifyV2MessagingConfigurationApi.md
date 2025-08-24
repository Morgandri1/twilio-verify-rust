# \VerifyV2MessagingConfigurationApi

All URIs are relative to *https://verify.twilio.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_messaging_configuration**](VerifyV2MessagingConfigurationApi.md#create_messaging_configuration) | **POST** /v2/Services/{ServiceSid}/MessagingConfigurations | Create a new MessagingConfiguration for a service.
[**delete_messaging_configuration**](VerifyV2MessagingConfigurationApi.md#delete_messaging_configuration) | **DELETE** /v2/Services/{ServiceSid}/MessagingConfigurations/{Country} | Delete a specific MessagingConfiguration.
[**fetch_messaging_configuration**](VerifyV2MessagingConfigurationApi.md#fetch_messaging_configuration) | **GET** /v2/Services/{ServiceSid}/MessagingConfigurations/{Country} | Fetch a specific MessagingConfiguration.
[**list_messaging_configuration**](VerifyV2MessagingConfigurationApi.md#list_messaging_configuration) | **GET** /v2/Services/{ServiceSid}/MessagingConfigurations | Retrieve a list of all Messaging Configurations for a Service.
[**update_messaging_configuration**](VerifyV2MessagingConfigurationApi.md#update_messaging_configuration) | **POST** /v2/Services/{ServiceSid}/MessagingConfigurations/{Country} | Update a specific MessagingConfiguration



## create_messaging_configuration

> models::VerifyV2ServiceMessagingConfiguration create_messaging_configuration(service_sid, country, messaging_service_sid)
Create a new MessagingConfiguration for a service.

Create a new MessagingConfiguration for a service.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**service_sid** | **String** | The SID of the [Service](https://www.twilio.com/docs/verify/api/service) that the resource is associated with. | [required] |
**country** | **String** | The [ISO-3166-1](https://en.wikipedia.org/wiki/ISO_3166-1_alpha-2) country code of the country this configuration will be applied to. If this is a global configuration, Country will take the value `all`. | [required] |
**messaging_service_sid** | **String** | The SID of the [Messaging Service](https://www.twilio.com/docs/messaging/api/service-resource) to be used to send SMS to the country of this configuration. | [required] |

### Return type

[**models::VerifyV2ServiceMessagingConfiguration**](verify.v2.service.messaging_configuration.md)

### Authorization

[accountSid_authToken](../README.md#accountSid_authToken)

### HTTP request headers

- **Content-Type**: application/x-www-form-urlencoded
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_messaging_configuration

> delete_messaging_configuration(service_sid, country)
Delete a specific MessagingConfiguration.

Delete a specific MessagingConfiguration.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**service_sid** | **String** | The SID of the [Service](https://www.twilio.com/docs/verify/api/service) that the resource is associated with. | [required] |
**country** | **String** | The [ISO-3166-1](https://en.wikipedia.org/wiki/ISO_3166-1_alpha-2) country code of the country this configuration will be applied to. If this is a global configuration, Country will take the value `all`. | [required] |

### Return type

 (empty response body)

### Authorization

[accountSid_authToken](../README.md#accountSid_authToken)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## fetch_messaging_configuration

> models::VerifyV2ServiceMessagingConfiguration fetch_messaging_configuration(service_sid, country)
Fetch a specific MessagingConfiguration.

Fetch a specific MessagingConfiguration.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**service_sid** | **String** | The SID of the [Service](https://www.twilio.com/docs/verify/api/service) that the resource is associated with. | [required] |
**country** | **String** | The [ISO-3166-1](https://en.wikipedia.org/wiki/ISO_3166-1_alpha-2) country code of the country this configuration will be applied to. If this is a global configuration, Country will take the value `all`. | [required] |

### Return type

[**models::VerifyV2ServiceMessagingConfiguration**](verify.v2.service.messaging_configuration.md)

### Authorization

[accountSid_authToken](../README.md#accountSid_authToken)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_messaging_configuration

> models::ListMessagingConfigurationResponse list_messaging_configuration(service_sid, page_size, page, page_token)
Retrieve a list of all Messaging Configurations for a Service.

Retrieve a list of all Messaging Configurations for a Service.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**service_sid** | **String** | The SID of the [Service](https://www.twilio.com/docs/verify/api/service) that the resource is associated with. | [required] |
**page_size** | Option<**i64**> | How many resources to return in each list page. The default is 50, and the maximum is 1000. |  |
**page** | Option<**i32**> | The page index. This value is simply for client state. |  |
**page_token** | Option<**String**> | The page token. This is provided by the API. |  |

### Return type

[**models::ListMessagingConfigurationResponse**](ListMessagingConfigurationResponse.md)

### Authorization

[accountSid_authToken](../README.md#accountSid_authToken)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_messaging_configuration

> models::VerifyV2ServiceMessagingConfiguration update_messaging_configuration(service_sid, country, messaging_service_sid)
Update a specific MessagingConfiguration

Update a specific MessagingConfiguration

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**service_sid** | **String** | The SID of the [Service](https://www.twilio.com/docs/verify/api/service) that the resource is associated with. | [required] |
**country** | **String** | The [ISO-3166-1](https://en.wikipedia.org/wiki/ISO_3166-1_alpha-2) country code of the country this configuration will be applied to. If this is a global configuration, Country will take the value `all`. | [required] |
**messaging_service_sid** | **String** | The SID of the [Messaging Service](https://www.twilio.com/docs/messaging/api/service-resource) to be used to send SMS to the country of this configuration. | [required] |

### Return type

[**models::VerifyV2ServiceMessagingConfiguration**](verify.v2.service.messaging_configuration.md)

### Authorization

[accountSid_authToken](../README.md#accountSid_authToken)

### HTTP request headers

- **Content-Type**: application/x-www-form-urlencoded
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

