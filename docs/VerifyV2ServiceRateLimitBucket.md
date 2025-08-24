# VerifyV2ServiceRateLimitBucket

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**sid** | Option<**String**> | A 34 character string that uniquely identifies this Bucket. | [optional]
**rate_limit_sid** | Option<**String**> | The Twilio-provided string that uniquely identifies the Rate Limit resource. | [optional]
**service_sid** | Option<**String**> | The SID of the [Service](https://www.twilio.com/docs/verify/api/service) the resource is associated with. | [optional]
**account_sid** | Option<**String**> | The SID of the [Account](https://www.twilio.com/docs/iam/api/account) that created the Rate Limit resource. | [optional]
**max** | Option<**i32**> | Maximum number of requests permitted in during the interval. | [optional][default to 0]
**interval** | Option<**i32**> | Number of seconds that the rate limit will be enforced over. | [optional][default to 0]
**date_created** | Option<**String**> | The date and time in GMT when the resource was created specified in [RFC 2822](https://www.ietf.org/rfc/rfc2822.txt) format. | [optional]
**date_updated** | Option<**String**> | The date and time in GMT when the resource was last updated specified in [RFC 2822](https://www.ietf.org/rfc/rfc2822.txt) format. | [optional]
**url** | Option<**String**> | The URL of this resource. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


