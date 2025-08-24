# VerifyV2Form

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**form_type** | Option<[**models::FormEnumFormTypes**](form_enum_form_types.md)> |  | [optional]
**forms** | Option<[**serde_json::Value**](.md)> | Object that contains the available forms for this type. This available forms are given in the standard [JSON Schema](https://json-schema.org/) format | [optional]
**form_meta** | Option<[**serde_json::Value**](.md)> | Additional information for the available forms for this type. E.g. The separator string used for `binding` in a Factor push. | [optional]
**url** | Option<**String**> | The URL to access the forms for this type. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


