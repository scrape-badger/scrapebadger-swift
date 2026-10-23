# RequestsAPI

All URIs are relative to *https://scrapebadger.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**requestsPollAnAsyncRequest**](RequestsAPI.md#requestspollanasyncrequest) | **GET** /v1/requests/{request_id} | Poll an async request


# **requestsPollAnAsyncRequest**
```swift
    open class func requestsPollAnAsyncRequest(requestId: String, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Poll an async request

Status or final response of a call made with ``Prefer: respond-async``. While it runs: 202. When done: the original status, headers and body.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let requestId = "requestId_example" // String | 

// Poll an async request
RequestsAPI.requestsPollAnAsyncRequest(requestId: requestId) { (response, error) in
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
 **requestId** | **String** |  | 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

