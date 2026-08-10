# AccountAPI

All URIs are relative to *https://scrapebadger.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**accountGetAccountInfo**](AccountAPI.md#accountgetaccountinfo) | **GET** /v1/account/me | Get account info


# **accountGetAccountInfo**
```swift
    open class func accountGetAccountInfo(completion: @escaping (_ data: AccountInfo?, _ error: Error?) -> Void)
```

Get account info

Get account details for the authenticated API key.  Returns credit balances, tier, rate limit, and subscription details. No credits are deducted for this call.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// Get account info
AccountAPI.accountGetAccountInfo() { (response, error) in
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
This endpoint does not need any parameter.

### Return type

[**AccountInfo**](AccountInfo.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

