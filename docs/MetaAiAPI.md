# MetaAiAPI

All URIs are relative to *https://scrapebadger.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**metaAiAskMetaAiAQuestion**](MetaAiAPI.md#metaaiaskmetaaiaquestion) | **GET** /v1/meta-ai/ask | Ask Meta AI a question
[**metaAiAskMetaAiAQuestionPost**](MetaAiAPI.md#metaaiaskmetaaiaquestionpost) | **POST** /v1/meta-ai/ask | Ask Meta AI a question (POST)
[**metaAiListMetaAiAssistantModes**](MetaAiAPI.md#metaailistmetaaiassistantmodes) | **GET** /v1/meta-ai/models | List Meta AI assistant modes
[**metaAiMetaAiScraperHealthCheck**](MetaAiAPI.md#metaaimetaaiscraperhealthcheck) | **GET** /v1/meta-ai/health | Meta AI scraper health check
[**metaAiMetaAiScraperHealthCheckHead**](MetaAiAPI.md#metaaimetaaiscraperhealthcheckhead) | **HEAD** /v1/meta-ai/health | Meta AI scraper health check


# **metaAiAskMetaAiAQuestion**
```swift
    open class func metaAiAskMetaAiAQuestion(prompt: String, country: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Ask Meta AI a question

Send a prompt to meta.ai and get the answer (anonymous, no Meta account).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let prompt = "prompt_example" // String | The prompt to send to Meta AI (max 4000 characters).
let country = "country_example" // String | ISO-3166 alpha-2 egress country, e.g. 'US', 'GB', 'DE'. (optional)

// Ask Meta AI a question
MetaAiAPI.metaAiAskMetaAiAQuestion(prompt: prompt, country: country) { (response, error) in
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
 **prompt** | **String** | The prompt to send to Meta AI (max 4000 characters). | 
 **country** | **String** | ISO-3166 alpha-2 egress country, e.g. &#39;US&#39;, &#39;GB&#39;, &#39;DE&#39;. | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **metaAiAskMetaAiAQuestionPost**
```swift
    open class func metaAiAskMetaAiAQuestionPost(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Ask Meta AI a question (POST)

POST form of `/ask`, for prompts too long for a query string.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// Ask Meta AI a question (POST)
MetaAiAPI.metaAiAskMetaAiAQuestionPost() { (response, error) in
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

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **metaAiListMetaAiAssistantModes**
```swift
    open class func metaAiListMetaAiAssistantModes(country: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

List Meta AI assistant modes

Assistant modes meta.ai currently serves to an anonymous visitor.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let country = "country_example" // String | ISO-3166 alpha-2 egress country. (optional)

// List Meta AI assistant modes
MetaAiAPI.metaAiListMetaAiAssistantModes(country: country) { (response, error) in
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
 **country** | **String** | ISO-3166 alpha-2 egress country. | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **metaAiMetaAiScraperHealthCheck**
```swift
    open class func metaAiMetaAiScraperHealthCheck(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Meta AI scraper health check

Check health of the Meta AI scraper service (accepts HEAD).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// Meta AI scraper health check
MetaAiAPI.metaAiMetaAiScraperHealthCheck() { (response, error) in
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

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **metaAiMetaAiScraperHealthCheckHead**
```swift
    open class func metaAiMetaAiScraperHealthCheckHead(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Meta AI scraper health check

Check health of the Meta AI scraper service (accepts HEAD).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// Meta AI scraper health check
MetaAiAPI.metaAiMetaAiScraperHealthCheckHead() { (response, error) in
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

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

