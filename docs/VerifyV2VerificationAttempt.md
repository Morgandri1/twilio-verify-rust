# VerifyV2VerificationAttempt

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**sid** | Option<**String**> | The SID that uniquely identifies the verification attempt resource. | [optional]
**account_sid** | Option<**String**> | The SID of the [Account](https://www.twilio.com/docs/iam/api/account) that created the Verification resource. | [optional]
**service_sid** | Option<**String**> | The SID of the [Service](https://www.twilio.com/docs/verify/api/service) used to generate the attempt. | [optional]
**verification_sid** | Option<**String**> | The SID of the [Verification](https://www.twilio.com/docs/verify/api/verification) that generated the attempt. | [optional]
**date_created** | Option<**String**> | The date that this Attempt was created, given in [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) format. | [optional]
**date_updated** | Option<**String**> | The date that this Attempt was updated, given in [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) format. | [optional]
**conversion_status** | Option<[**models::VerificationAttemptEnumConversionStatus**](verification_attempt_enum_conversion_status.md)> |  | [optional]
**channel** | Option<[**models::VerificationAttemptEnumChannels**](verification_attempt_enum_channels.md)> |  | [optional]
**price** | Option<[**serde_json::Value**](.md)> | An object containing the charge for this verification attempt related to the channel costs and the currency used. The costs related to the succeeded verifications are not included. May not be immediately available. More information on pricing is available [here](https://www.twilio.com/en-us/verify/pricing). | [optional]
**channel_data** | Option<[**serde_json::Value**](.md)> | An object containing the channel specific information for an attempt. | [optional]
**url** | Option<**String**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


