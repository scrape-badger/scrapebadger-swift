# QuoteAPI

All URIs are relative to *https://scrapebadger.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**quoteQuoteACall**](QuoteAPI.md#quotequoteacall) | **POST** /v1/quote | Quote a call


# **quoteQuoteACall**
```swift
    open class func quoteQuoteACall(quoteRequest: QuoteRequest, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Quote a call

What a call would cost (credits and USD), whether its parameters are valid, and how long it usually takes. Free: nothing runs and nothing is charged.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let quoteRequest = QuoteRequest(method: "method_example", path: "path_example", params: "TODO", body: "TODO") // QuoteRequest | 

// Quote a call
QuoteAPI.quoteQuoteACall(quoteRequest: quoteRequest) { (response, error) in
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
 **quoteRequest** | [**QuoteRequest**](QuoteRequest.md) |  | 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

