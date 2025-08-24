# VerifyV2VerificationTemplate

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**sid** | Option<**String**> | A 34 character string that uniquely identifies a Verification Template. | [optional]
**account_sid** | Option<**String**> | The unique SID identifier of the Account. | [optional]
**friendly_name** | Option<**String**> | A descriptive string that you create to describe a Template. It can be up to 32 characters long. | [optional]
**channels** | Option<**Vec<String>**> | A list of channels that support the Template. Can include: sms, voice. | [optional]
**translations** | Option<[**serde_json::Value**](.md)> | An object that contains the different translations of the template. Every translation is identified by the language short name and contains its respective information as the approval status, text and created/modified date. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


