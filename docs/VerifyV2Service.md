# VerifyV2Service

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**sid** | Option<**String**> | The unique string that we created to identify the Service resource. | [optional]
**account_sid** | Option<**String**> | The SID of the [Account](https://www.twilio.com/docs/iam/api/account) that created the Service resource. | [optional]
**friendly_name** | Option<**String**> | The name that appears in the body of your verification messages. It can be up to 30 characters long and can include letters, numbers, spaces, dashes, underscores. Phone numbers, special characters or links are NOT allowed. It cannot contain more than 4 (consecutive or non-consecutive) digits. **This value should not contain PII.** | [optional]
**code_length** | Option<**i32**> | The length of the verification code to generate. | [optional][default to 0]
**lookup_enabled** | Option<**bool**> | Whether to perform a lookup with each verification started and return info about the phone number. | [optional]
**psd2_enabled** | Option<**bool**> | Whether to pass PSD2 transaction parameters when starting a verification. | [optional]
**skip_sms_to_landlines** | Option<**bool**> | Whether to skip sending SMS verifications to landlines. Requires `lookup_enabled`. | [optional]
**dtmf_input_required** | Option<**bool**> | Whether to ask the user to press a number before delivering the verify code in a phone call. | [optional]
**tts_name** | Option<**String**> | The name of an alternative text-to-speech service to use in phone calls. Applies only to TTS languages. | [optional]
**do_not_share_warning_enabled** | Option<**bool**> | Whether to add a security warning at the end of an SMS verification body. Disabled by default and applies only to SMS. Example SMS body: `Your AppName verification code is: 1234. Don’t share this code with anyone; our employees will never ask for the code` | [optional]
**custom_code_enabled** | Option<**bool**> | Whether to allow sending verifications with a custom code instead of a randomly generated one. | [optional]
**push** | Option<[**serde_json::Value**](.md)> | Configurations for the Push factors (channel) created under this Service. | [optional]
**totp** | Option<[**serde_json::Value**](.md)> | Configurations for the TOTP factors (channel) created under this Service. | [optional]
**default_template_sid** | Option<**String**> |  | [optional]
**whatsapp** | Option<[**serde_json::Value**](.md)> |  | [optional]
**passkeys** | Option<[**serde_json::Value**](.md)> |  | [optional]
**verify_event_subscription_enabled** | Option<**bool**> | Whether to allow verifications from the service to reach the stream-events sinks if configured | [optional]
**date_created** | Option<**String**> | The date and time in GMT when the resource was created specified in [RFC 2822](https://www.ietf.org/rfc/rfc2822.txt) format. | [optional]
**date_updated** | Option<**String**> | The date and time in GMT when the resource was last updated specified in [RFC 2822](https://www.ietf.org/rfc/rfc2822.txt) format. | [optional]
**url** | Option<**String**> | The absolute URL of the resource. | [optional]
**links** | Option<[**serde_json::Value**](.md)> | The URLs of related resources. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


