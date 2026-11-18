# RequestsAPI

All URIs are relative to *https://scrapebadger.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**requestsCallbackStatus**](RequestsAPI.md#requestscallbackstatus) | **GET** /v1/requests/{request_id}/callback | Callback status
[**requestsPollAnAsyncRequest**](RequestsAPI.md#requestspollanasyncrequest) | **GET** /v1/requests/{request_id} | Poll an async request


# **requestsCallbackStatus**
```swift
    open class func requestsCallbackStatus(requestId: String, completion: @escaping (_ data: AsyncCallbackStatus?, _ error: Error?) -> Void)
```

Callback status

Webhook delivery state of a call submitted with `X-Callback-URL` / `callback_url`: kept for 24 h. Free. `404 callback_not_found` for a request without a callback, of another account, or older than 24 h.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let requestId = "requestId_example" // String | 

// Callback status
RequestsAPI.requestsCallbackStatus(requestId: requestId) { (response, error) in
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

[**AsyncCallbackStatus**](AsyncCallbackStatus.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **requestsPollAnAsyncRequest**
```swift
    open class func requestsPollAnAsyncRequest(requestId: String, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Poll an async request

Status or final response of a call made with ``Prefer: respond-async``. While it runs: 202. When done: the original status, headers and body.  The final response carries `X-Callback-Status`, `X-Callback-Attempts` and `X-Callback-Error` for a call submitted with a callback; while it runs, the `202` body has a `callback` object. Full delivery state: `GET /v1/requests/{request_id}/callback`.

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

