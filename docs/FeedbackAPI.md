# FeedbackAPI

All URIs are relative to *https://scrapebadger.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**feedbackReportABugOrSendFeedback**](FeedbackAPI.md#feedbackreportabugorsendfeedback) | **POST** /v1/feedback | Report a bug or send feedback


# **feedbackReportABugOrSendFeedback**
```swift
    open class func feedbackReportABugOrSendFeedback(feedbackRequest: FeedbackRequest, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Report a bug or send feedback

File a bug (wrong/empty result for valid input, misleading error, price mismatch) or feedback (an API or field you needed and couldn't find). Free, never billed. Pass the failing call's X-Request-ID so we can find it.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let feedbackRequest = FeedbackRequest(type: "type_example", summary: "summary_example", details: "details_example", requestId: "requestId_example", endpoint: "endpoint_example", contact: "contact_example") // FeedbackRequest | 

// Report a bug or send feedback
FeedbackAPI.feedbackReportABugOrSendFeedback(feedbackRequest: feedbackRequest) { (response, error) in
    guard error == nil else {
        print(error)
        return
    }

    if (response) {
        dump(response)
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **feedbackRequest** | [**FeedbackRequest**](FeedbackRequest.md) |  | 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

