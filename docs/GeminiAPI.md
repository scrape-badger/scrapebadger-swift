# GeminiAPI

All URIs are relative to *https://scrapebadger.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**geminiAskGeminiAQuestion**](GeminiAPI.md#geminiaskgeminiaquestion) | **GET** /v1/gemini/ask | Ask Gemini a question
[**geminiAskGeminiAQuestionPost**](GeminiAPI.md#geminiaskgeminiaquestionpost) | **POST** /v1/gemini/ask | Ask Gemini a question (POST)
[**geminiGeminiScraperHealthCheck**](GeminiAPI.md#geminigeminiscraperhealthcheck) | **GET** /v1/gemini/health | Gemini scraper health check
[**geminiGeminiScraperHealthCheckHead**](GeminiAPI.md#geminigeminiscraperhealthcheckhead) | **HEAD** /v1/gemini/health | Gemini scraper health check
[**geminiMeasureABrandSVisibilityInAGeminiAnswer**](GeminiAPI.md#geminimeasureabrandsvisibilityinageminianswer) | **GET** /v1/gemini/brand-visibility | Measure a brand&#39;s visibility in a Gemini answer
[**geminiMeasureABrandSVisibilityInAGeminiAnswerPost**](GeminiAPI.md#geminimeasureabrandsvisibilityinageminianswerpost) | **POST** /v1/gemini/brand-visibility | Measure a brand&#39;s visibility in a Gemini answer (POST)


# **geminiAskGeminiAQuestion**
```swift
    open class func geminiAskGeminiAQuestion(prompt: String, country: String? = nil, webSearch: String? = nil, imageUrl: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Ask Gemini a question

Send a prompt to Gemini and get the answer plus the web sources it cited.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let prompt = "prompt_example" // String | The prompt to send to Gemini (max 4096 characters).
let country = "country_example" // String | ISO-3166 alpha-2 egress country, e.g. 'US', 'GB', 'DE'. (optional)
let webSearch = "webSearch_example" // String | auto (let Gemini decide) | force (ask it to browse) | off (answer from memory). `web_search_triggered` in the response always reports what actually happened. (optional) (default to "auto")
let imageUrl = "imageUrl_example" // String | Public http(s) URL of an image to attach to the prompt. Gemini reads it and answers about it. POST also accepts `image_base64`. Exactly one of the two. (optional)

// Ask Gemini a question
GeminiAPI.geminiAskGeminiAQuestion(prompt: prompt, country: country, webSearch: webSearch, imageUrl: imageUrl) { (response, error) in
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
 **prompt** | **String** | The prompt to send to Gemini (max 4096 characters). | 
 **country** | **String** | ISO-3166 alpha-2 egress country, e.g. &#39;US&#39;, &#39;GB&#39;, &#39;DE&#39;. | [optional] 
 **webSearch** | **String** | auto (let Gemini decide) | force (ask it to browse) | off (answer from memory). &#x60;web_search_triggered&#x60; in the response always reports what actually happened. | [optional] [default to &quot;auto&quot;]
 **imageUrl** | **String** | Public http(s) URL of an image to attach to the prompt. Gemini reads it and answers about it. POST also accepts &#x60;image_base64&#x60;. Exactly one of the two. | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **geminiAskGeminiAQuestionPost**
```swift
    open class func geminiAskGeminiAQuestionPost(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Ask Gemini a question (POST)

POST form of `/ask`, for prompts too long for a query string.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// Ask Gemini a question (POST)
GeminiAPI.geminiAskGeminiAQuestionPost() { (response, error) in
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

# **geminiGeminiScraperHealthCheck**
```swift
    open class func geminiGeminiScraperHealthCheck(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Gemini scraper health check

Check health of the Gemini scraper service (accepts HEAD).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// Gemini scraper health check
GeminiAPI.geminiGeminiScraperHealthCheck() { (response, error) in
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

# **geminiGeminiScraperHealthCheckHead**
```swift
    open class func geminiGeminiScraperHealthCheckHead(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Gemini scraper health check

Check health of the Gemini scraper service (accepts HEAD).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// Gemini scraper health check
GeminiAPI.geminiGeminiScraperHealthCheckHead() { (response, error) in
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

# **geminiMeasureABrandSVisibilityInAGeminiAnswer**
```swift
    open class func geminiMeasureABrandSVisibilityInAGeminiAnswer(prompt: String, brand: String, domain: String? = nil, aliases: String? = nil, competitors: String? = nil, country: String? = nil, webSearch: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Measure a brand's visibility in a Gemini answer

Ask Gemini, then report whether the brand is mentioned, cited and how prominently.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let prompt = "prompt_example" // String | The prompt to ask Gemini.
let brand = "brand_example" // String | Brand name to look for in the answer.
let domain = "domain_example" // String | Brand domain, for citation matching. (optional)
let aliases = "aliases_example" // String | Comma-separated alternative names. (optional)
let competitors = "competitors_example" // String | Comma-separated competitor names. (optional)
let country = "country_example" // String | ISO-3166 alpha-2 egress country. (optional)
let webSearch = "webSearch_example" // String | auto | force | off (optional) (default to "force")

// Measure a brand's visibility in a Gemini answer
GeminiAPI.geminiMeasureABrandSVisibilityInAGeminiAnswer(prompt: prompt, brand: brand, domain: domain, aliases: aliases, competitors: competitors, country: country, webSearch: webSearch) { (response, error) in
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
 **prompt** | **String** | The prompt to ask Gemini. | 
 **brand** | **String** | Brand name to look for in the answer. | 
 **domain** | **String** | Brand domain, for citation matching. | [optional] 
 **aliases** | **String** | Comma-separated alternative names. | [optional] 
 **competitors** | **String** | Comma-separated competitor names. | [optional] 
 **country** | **String** | ISO-3166 alpha-2 egress country. | [optional] 
 **webSearch** | **String** | auto | force | off | [optional] [default to &quot;force&quot;]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **geminiMeasureABrandSVisibilityInAGeminiAnswerPost**
```swift
    open class func geminiMeasureABrandSVisibilityInAGeminiAnswerPost(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Measure a brand's visibility in a Gemini answer (POST)

POST form, for longer prompts and larger competitor sets.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// Measure a brand's visibility in a Gemini answer (POST)
GeminiAPI.geminiMeasureABrandSVisibilityInAGeminiAnswerPost() { (response, error) in
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

