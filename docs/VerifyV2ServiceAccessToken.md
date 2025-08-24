# VerifyV2ServiceAccessToken

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**sid** | Option<**String**> | A 34 character string that uniquely identifies this Access Token. | [optional]
**account_sid** | Option<**String**> | The unique SID identifier of the Account. | [optional]
**service_sid** | Option<**String**> | The unique SID identifier of the Verify Service. | [optional]
**entity_identity** | Option<**String**> | The unique external identifier for the Entity of the Service. | [optional]
**factor_type** | Option<[**models::AccessTokenEnumFactorTypes**](access_token_enum_factor_types.md)> |  | [optional]
**factor_friendly_name** | Option<**String**> | A human readable description of this factor, up to 64 characters. For a push factor, this can be the device's name. | [optional]
**token** | Option<**String**> | The access token generated for enrollment, this is an encrypted json web token. | [optional]
**url** | Option<**String**> | The URL of this resource. | [optional]
**ttl** | Option<**i32**> | How long, in seconds, the access token is valid. Max: 5 minutes | [optional][default to 0]
**date_created** | Option<**String**> | The date that this access token was created, given in [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) format. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


