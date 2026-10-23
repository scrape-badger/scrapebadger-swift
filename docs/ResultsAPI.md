# ResultsAPI

All URIs are relative to *https://scrapebadger.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**resultsReReadAResult**](ResultsAPI.md#resultsrereadaresult) | **GET** /v1/results/{result_id} | Re-read a result


# **resultsReReadAResult**
```swift
    open class func resultsReReadAResult(resultId: String, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Re-read a result

Replay a billed result (X-Result-ID) for free for ~15 minutes, optionally trimmed with jq / fields / max_items / summary. Never re-run a paid call just to reshape it.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let resultId = "resultId_example" // String | 

// Re-read a result
ResultsAPI.resultsReReadAResult(resultId: resultId) { (response, error) in
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
 **resultId** | **String** |  | 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

