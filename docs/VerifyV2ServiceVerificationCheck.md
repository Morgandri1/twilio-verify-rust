# VerifyV2ServiceVerificationCheck

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**sid** | Option<**String**> | The unique string that we created to identify the VerificationCheck resource. | [optional]
**service_sid** | Option<**String**> | The SID of the [Service](https://www.twilio.com/docs/verify/api/service) the resource is associated with. | [optional]
**account_sid** | Option<**String**> | The SID of the [Account](https://www.twilio.com/docs/iam/api/account) that created the VerificationCheck resource. | [optional]
**to** | Option<**String**> | The phone number or [email](https://www.twilio.com/docs/verify/email) being verified. Phone numbers must be in [E.164 format](https://www.twilio.com/docs/glossary/what-e164). | [optional]
**channel** | Option<[**models::VerificationCheckEnumChannel**](verification_check_enum_channel.md)> |  | [optional]
**status** | Option<**String**> | The status of the verification. Can be: `pending`, `approved`, `canceled`, `max_attempts_reached`, `deleted`, `failed` or `expired`. | [optional]
**valid** | Option<**bool**> | Use \"status\" instead. Legacy property indicating whether the verification was successful. | [optional]
**amount** | Option<**String**> | The amount of the associated PSD2 compliant transaction. Requires the PSD2 Service flag enabled. | [optional]
**payee** | Option<**String**> | The payee of the associated PSD2 compliant transaction. Requires the PSD2 Service flag enabled. | [optional]
**date_created** | Option<**String**> | The [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) date and time in GMT when the Verification Check resource was created. | [optional]
**date_updated** | Option<**String**> | The [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) date and time in GMT when the Verification Check resource was last updated. | [optional]
**sna_attempts_error_codes** | Option<[**Vec<serde_json::Value>**](serde_json::Value.md)> | List of error codes as a result of attempting a verification using the `sna` channel. The error codes are chronologically ordered, from the first attempt to the latest attempt. This will be an empty list if no errors occured or `null` if the last channel used wasn't `sna`. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


