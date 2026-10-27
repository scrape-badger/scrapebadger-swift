# AccountAPI

All URIs are relative to *https://scrapebadger.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**accountGetAccountInfo**](AccountAPI.md#accountgetaccountinfo) | **GET** /v1/account/me | Get account info
[**accountGetTheWebhookSigningSecret**](AccountAPI.md#accountgetthewebhooksigningsecret) | **GET** /v1/account/webhook-secret | Get the webhook signing secret
[**accountRotateTheWebhookSigningSecret**](AccountAPI.md#accountrotatethewebhooksigningsecret) | **POST** /v1/account/webhook-secret/rotate | Rotate the webhook signing secret


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

# **accountGetTheWebhookSigningSecret**
```swift
    open class func accountGetTheWebhookSigningSecret(completion: @escaping (_ data: WebhookSecret?, _ error: Error?) -> Void)
```

Get the webhook signing secret

The secret that signs this account's async-request webhooks, created on first read. Verify a delivery by comparing ``X-ScrapeBadger-Signature`` with ``sha256=`` + hex HMAC-SHA256(secret, raw body).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// Get the webhook signing secret
AccountAPI.accountGetTheWebhookSigningSecret() { (response, error) in
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

[**WebhookSecret**](WebhookSecret.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **accountRotateTheWebhookSigningSecret**
```swift
    open class func accountRotateTheWebhookSigningSecret(completion: @escaping (_ data: WebhookSecret?, _ error: Error?) -> Void)
```

Rotate the webhook signing secret

Replace the signing secret. Deliveries that start from now on are signed with the new one; retries of a delivery already under way keep the old one.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// Rotate the webhook signing secret
AccountAPI.accountRotateTheWebhookSigningSecret() { (response, error) in
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

[**WebhookSecret**](WebhookSecret.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

