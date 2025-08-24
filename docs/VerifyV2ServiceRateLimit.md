# VerifyV2ServiceRateLimit

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**sid** | Option<**String**> | A 34 character string that uniquely identifies this Rate Limit. | [optional]
**service_sid** | Option<**String**> | The SID of the [Service](https://www.twilio.com/docs/verify/api/service) the resource is associated with. | [optional]
**account_sid** | Option<**String**> | The SID of the [Account](https://www.twilio.com/docs/iam/api/account) that created the Rate Limit resource. | [optional]
**unique_name** | Option<**String**> | Provides a unique and addressable name to be assigned to this Rate Limit, assigned by the developer, to be optionally used in addition to SID. **This value should not contain PII.** | [optional]
**description** | Option<**String**> | Description of this Rate Limit | [optional]
**date_created** | Option<**String**> | The date and time in GMT when the resource was created specified in [RFC 2822](https://www.ietf.org/rfc/rfc2822.txt) format. | [optional]
**date_updated** | Option<**String**> | The date and time in GMT when the resource was last updated specified in [RFC 2822](https://www.ietf.org/rfc/rfc2822.txt) format. | [optional]
**url** | Option<**String**> | The URL of this resource. | [optional]
**links** | Option<[**serde_json::Value**](.md)> | The URLs of related resources. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


