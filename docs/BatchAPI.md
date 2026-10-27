# BatchAPI

All URIs are relative to *https://scrapebadger.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**batchSubmitABatchOfAsyncRequests**](BatchAPI.md#batchsubmitabatchofasyncrequests) | **POST** /v1/batch | Submit a batch of async requests


# **batchSubmitABatchOfAsyncRequests**
```swift
    open class func batchSubmitABatchOfAsyncRequests(batchRequest: BatchRequest, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Submit a batch of async requests

Submit up to 100 GET reads in one call. Each item runs as its own ``Prefer: respond-async`` request under this key, with the same auth, credit check, rate limit and billing as if it were sent alone, and returns a request_id to poll (or a webhook to ``callback_url``). At most 10 items of a batch run at the same time. Submitting is free; each item bills as it runs. Items are checked against the spendable balance first, at the endpoint's base price, so a batch never starts more than the account can pay for.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let batchRequest = BatchRequest(requests: [BatchItem(method: "method_example", path: "path_example", query: "TODO")], callbackUrl: "callbackUrl_example") // BatchRequest | 

// Submit a batch of async requests
BatchAPI.batchSubmitABatchOfAsyncRequests(batchRequest: batchRequest) { (response, error) in
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
 **batchRequest** | [**BatchRequest**](BatchRequest.md) |  | 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

