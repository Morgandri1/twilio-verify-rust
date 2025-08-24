# VerifyV2ServiceWebhook

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**sid** | Option<**String**> | The unique string that we created to identify the Webhook resource. | [optional]
**service_sid** | Option<**String**> | The unique SID identifier of the Service. | [optional]
**account_sid** | Option<**String**> | The SID of the [Account](https://www.twilio.com/docs/iam/api/account) that created the Service resource. | [optional]
**friendly_name** | Option<**String**> | The string that you assigned to describe the webhook. **This value should not contain PII.** | [optional]
**event_types** | Option<**Vec<String>**> | The array of events that this Webhook is subscribed to. Possible event types: `*, factor.deleted, factor.created, factor.verified, challenge.approved, challenge.denied` | [optional]
**status** | Option<[**models::WebhookEnumStatus**](webhook_enum_status.md)> |  | [optional]
**version** | Option<[**models::WebhookEnumVersion**](webhook_enum_version.md)> |  | [optional]
**webhook_url** | Option<**String**> | The URL associated with this Webhook. | [optional]
**webhook_method** | Option<[**models::WebhookEnumMethods**](webhook_enum_methods.md)> |  | [optional]
**date_created** | Option<**String**> | The date and time in GMT when the resource was created specified in [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) format. | [optional]
**date_updated** | Option<**String**> | The date and time in GMT when the resource was last updated specified in [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) format. | [optional]
**url** | Option<**String**> | The absolute URL of the Webhook resource. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


