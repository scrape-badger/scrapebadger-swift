# ResultsAPI

All URIs are relative to *https://scrapebadger.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**resultsReReadAResultRemoved**](ResultsAPI.md#resultsrereadaresultremoved) | **GET** /v1/results/{result_id} | Re-read a result (removed)


# **resultsReReadAResultRemoved**
```swift
    open class func resultsReReadAResultRemoved(resultId: String, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Re-read a result (removed)

Removed (SCR-396): ScrapeBadger no longer stores results, so there is nothing to re-read. Always 410. Narrow a call with _jq / _fields / _max_items instead.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let resultId = "resultId_example" // String | 

// Re-read a result (removed)
ResultsAPI.resultsReReadAResultRemoved(resultId: resultId) { (response, error) in
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

