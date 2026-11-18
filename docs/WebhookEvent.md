# WebhookEvent

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**event** | **String** |  | 
**requestId** | **String** |  | 
**batchId** | **String** |  | 
**status** | **Int** | The call&#39;s own HTTP status. | 
**headers** | **[String: String]** | The call&#39;s kept response headers, lower-case (content-type, x-credits-used, x-request-duration-ms, x-api-tier). | 
**resultUrl** | **String** |  | 
**resultExpiresAt** | **Int** | Unix time. | 
**bodySize** | **Int** |  | 
**body** | **AnyCodable** |  | 
**bodyOmitted** | **Bool** | Present (true) when the body was over 1 MB: fetch &#x60;result_url&#x60;. | [optional] 
**attempt** | **Int** |  | 
**sentAt** | **Int** | Unix time of this attempt. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


