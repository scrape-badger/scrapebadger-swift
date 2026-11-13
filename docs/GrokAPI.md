# GrokAPI

All URIs are relative to *https://scrapebadger.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**grokAskGrokAQuestion**](GrokAPI.md#grokaskgrokaquestion) | **GET** /v1/grok/ask | Ask Grok a question
[**grokAskGrokAQuestionPost**](GrokAPI.md#grokaskgrokaquestionpost) | **POST** /v1/grok/ask | Ask Grok a question (POST)
[**grokGetAGrokConversation**](GrokAPI.md#grokgetagrokconversation) | **GET** /v1/grok/conversations/{conversation_id} | Get a Grok conversation
[**grokGrokScraperHealthCheck**](GrokAPI.md#grokgrokscraperhealthcheck) | **GET** /v1/grok/health | Grok scraper health check
[**grokGrokScraperHealthCheckHead**](GrokAPI.md#grokgrokscraperhealthcheckhead) | **HEAD** /v1/grok/health | Grok scraper health check
[**grokListGrokAssistantModes**](GrokAPI.md#groklistgrokassistantmodes) | **GET** /v1/grok/models | List Grok assistant modes
[**grokMeasureBrandVisibilityInGrok**](GrokAPI.md#grokmeasurebrandvisibilityingrok) | **GET** /v1/grok/brand-visibility | Measure brand visibility in Grok
[**grokMeasureBrandVisibilityInGrokPost**](GrokAPI.md#grokmeasurebrandvisibilityingrokpost) | **POST** /v1/grok/brand-visibility | Measure brand visibility in Grok (POST)


# **grokAskGrokAQuestion**
```swift
    open class func grokAskGrokAQuestion(prompt: String, conversationId: String? = nil, mode: String? = nil, webSearch: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Ask Grok a question

Ask the real Grok assistant and get its answer, web sources, and X post references.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let prompt = "prompt_example" // String | Prompt to send to Grok (max 4000 characters).
let conversationId = "conversationId_example" // String | Existing Grok conversation to continue. (optional)
let mode = "mode_example" // String | Assistant mode: auto, fast, or expert. (optional) (default to "auto")
let webSearch = "webSearch_example" // String | Web and X search: auto, force, or off. (optional) (default to "auto")

// Ask Grok a question
GrokAPI.grokAskGrokAQuestion(prompt: prompt, conversationId: conversationId, mode: mode, webSearch: webSearch) { (response, error) in
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
 **prompt** | **String** | Prompt to send to Grok (max 4000 characters). | 
 **conversationId** | **String** | Existing Grok conversation to continue. | [optional] 
 **mode** | **String** | Assistant mode: auto, fast, or expert. | [optional] [default to &quot;auto&quot;]
 **webSearch** | **String** | Web and X search: auto, force, or off. | [optional] [default to &quot;auto&quot;]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **grokAskGrokAQuestionPost**
```swift
    open class func grokAskGrokAQuestionPost(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Ask Grok a question (POST)

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// Ask Grok a question (POST)
GrokAPI.grokAskGrokAQuestionPost() { (response, error) in
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

# **grokGetAGrokConversation**
```swift
    open class func grokGetAGrokConversation(conversationId: String, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get a Grok conversation

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let conversationId = "conversationId_example" // String | 

// Get a Grok conversation
GrokAPI.grokGetAGrokConversation(conversationId: conversationId) { (response, error) in
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
 **conversationId** | **String** |  | 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **grokGrokScraperHealthCheck**
```swift
    open class func grokGrokScraperHealthCheck(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Grok scraper health check

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// Grok scraper health check
GrokAPI.grokGrokScraperHealthCheck() { (response, error) in
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

# **grokGrokScraperHealthCheckHead**
```swift
    open class func grokGrokScraperHealthCheckHead(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Grok scraper health check

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// Grok scraper health check
GrokAPI.grokGrokScraperHealthCheckHead() { (response, error) in
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

# **grokListGrokAssistantModes**
```swift
    open class func grokListGrokAssistantModes(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

List Grok assistant modes

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// List Grok assistant modes
GrokAPI.grokListGrokAssistantModes() { (response, error) in
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

# **grokMeasureBrandVisibilityInGrok**
```swift
    open class func grokMeasureBrandVisibilityInGrok(prompt: String, brand: String, competitors: [String]? = nil, brandDomain: String? = nil, mode: String? = nil, webSearch: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Measure brand visibility in Grok

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let prompt = "prompt_example" // String | Buyer or category prompt to send to Grok.
let brand = "brand_example" // String | Brand name to measure.
let competitors = ["inner_example"] // [String] | Competitor brand names. (optional)
let brandDomain = "brandDomain_example" // String | Brand domain for citation rank. (optional)
let mode = "mode_example" // String | Assistant mode: auto, fast, or expert. (optional) (default to "auto")
let webSearch = "webSearch_example" // String | Web and X search mode. (optional) (default to "force")

// Measure brand visibility in Grok
GrokAPI.grokMeasureBrandVisibilityInGrok(prompt: prompt, brand: brand, competitors: competitors, brandDomain: brandDomain, mode: mode, webSearch: webSearch) { (response, error) in
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
 **prompt** | **String** | Buyer or category prompt to send to Grok. | 
 **brand** | **String** | Brand name to measure. | 
 **competitors** | [**[String]**](String.md) | Competitor brand names. | [optional] 
 **brandDomain** | **String** | Brand domain for citation rank. | [optional] 
 **mode** | **String** | Assistant mode: auto, fast, or expert. | [optional] [default to &quot;auto&quot;]
 **webSearch** | **String** | Web and X search mode. | [optional] [default to &quot;force&quot;]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **grokMeasureBrandVisibilityInGrokPost**
```swift
    open class func grokMeasureBrandVisibilityInGrokPost(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Measure brand visibility in Grok (POST)

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// Measure brand visibility in Grok (POST)
GrokAPI.grokMeasureBrandVisibilityInGrokPost() { (response, error) in
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

