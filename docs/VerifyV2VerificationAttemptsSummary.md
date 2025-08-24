# VerifyV2VerificationAttemptsSummary

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**total_attempts** | Option<**i32**> | Total of attempts made according to the provided filters | [optional][default to 0]
**total_converted** | Option<**i32**> | Total of  attempts made that were confirmed by the end user, according to the provided filters. | [optional][default to 0]
**total_unconverted** | Option<**i32**> | Total of attempts made that were not confirmed by the end user, according to the provided filters. | [optional][default to 0]
**conversion_rate_percentage** | Option<**String**> | Percentage of the confirmed messages over the total, defined by (total_converted/total_attempts)*100.  | [optional]
**url** | Option<**String**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


