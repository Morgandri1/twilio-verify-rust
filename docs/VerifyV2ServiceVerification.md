# VerifyV2ServiceVerification

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**sid** | Option<**String**> | The unique string that we created to identify the Verification resource. | [optional]
**service_sid** | Option<**String**> | The SID of the [Service](https://www.twilio.com/docs/verify/api/service) the resource is associated with. | [optional]
**account_sid** | Option<**String**> | The SID of the [Account](https://www.twilio.com/docs/iam/api/account) that created the Verification resource. | [optional]
**to** | Option<**String**> | The phone number or [email](https://www.twilio.com/docs/verify/email) being verified. Phone numbers must be in [E.164 format](https://www.twilio.com/docs/glossary/what-e164). | [optional]
**channel** | Option<[**models::VerificationEnumChannel**](verification_enum_channel.md)> |  | [optional]
**status** | Option<**String**> | The status of the verification. Can be: `pending`, `approved`, `canceled`, `max_attempts_reached`, `deleted`, `failed` or `expired`. | [optional]
**valid** | Option<**bool**> | Use \"status\" instead. Legacy property indicating whether the verification was successful. | [optional]
**lookup** | Option<[**serde_json::Value**](.md)> | Information about the phone number being verified. | [optional]
**amount** | Option<**String**> | The amount of the associated PSD2 compliant transaction. Requires the PSD2 Service flag enabled. | [optional]
**payee** | Option<**String**> | The payee of the associated PSD2 compliant transaction. Requires the PSD2 Service flag enabled. | [optional]
**send_code_attempts** | Option<[**Vec<serde_json::Value>**](serde_json::Value.md)> | An array of verification attempt objects containing the channel attempted and the channel-specific transaction SID. | [optional]
**date_created** | Option<**String**> | The date and time in GMT when the resource was created specified in [RFC 2822](https://www.ietf.org/rfc/rfc2822.txt) format. | [optional]
**date_updated** | Option<**String**> | The date and time in GMT when the resource was last updated specified in [RFC 2822](https://www.ietf.org/rfc/rfc2822.txt) format. | [optional]
**sna** | Option<[**serde_json::Value**](.md)> | The set of fields used for a silent network auth (`sna`) verification. Contains a single field with the URL to be invoked to verify the phone number. | [optional]
**url** | Option<**String**> | The absolute URL of the Verification resource. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


