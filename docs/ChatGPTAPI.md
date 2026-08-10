# ChatGPTAPI

All URIs are relative to *https://scrapebadger.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**chatgptAskChatgptAQuestion**](ChatGPTAPI.md#chatgptaskchatgptaquestion) | **GET** /v1/chatgpt/ask | Ask ChatGPT a question
[**chatgptAskChatgptAQuestionPost**](ChatGPTAPI.md#chatgptaskchatgptaquestionpost) | **POST** /v1/chatgpt/ask | Ask ChatGPT a question (POST)
[**chatgptChatgptScraperHealthCheck**](ChatGPTAPI.md#chatgptchatgptscraperhealthcheck) | **GET** /v1/chatgpt/health | ChatGPT scraper health check
[**chatgptChatgptScraperHealthCheckHead**](ChatGPTAPI.md#chatgptchatgptscraperhealthcheckhead) | **HEAD** /v1/chatgpt/health | ChatGPT scraper health check
[**chatgptListChatgptModels**](ChatGPTAPI.md#chatgptlistchatgptmodels) | **GET** /v1/chatgpt/models | List ChatGPT models
[**chatgptMeasureABrandSVisibilityInAChatgptAnswer**](ChatGPTAPI.md#chatgptmeasureabrandsvisibilityinachatgptanswer) | **GET** /v1/chatgpt/brand-visibility | Measure a brand&#39;s visibility in a ChatGPT answer
[**chatgptMeasureABrandSVisibilityInAChatgptAnswerPost**](ChatGPTAPI.md#chatgptmeasureabrandsvisibilityinachatgptanswerpost) | **POST** /v1/chatgpt/brand-visibility | Measure a brand&#39;s visibility in a ChatGPT answer (POST)


# **chatgptAskChatgptAQuestion**
```swift
    open class func chatgptAskChatgptAQuestion(prompt: String, country: String? = nil, webSearch: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Ask ChatGPT a question

Send a prompt to ChatGPT and get the answer plus the web sources it cited.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let prompt = "prompt_example" // String | The prompt to send to ChatGPT (max 4096 characters).
let country = "country_example" // String | ISO-3166 alpha-2 egress country, e.g. 'US', 'GB', 'DE'. (optional)
let webSearch = "webSearch_example" // String | auto (let ChatGPT decide) | force (ask it to browse) | off (answer from memory). `web_search_triggered` in the response always reports what actually happened. (optional) (default to "auto")

// Ask ChatGPT a question
ChatGPTAPI.chatgptAskChatgptAQuestion(prompt: prompt, country: country, webSearch: webSearch) { (response, error) in
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
 **prompt** | **String** | The prompt to send to ChatGPT (max 4096 characters). | 
 **country** | **String** | ISO-3166 alpha-2 egress country, e.g. &#39;US&#39;, &#39;GB&#39;, &#39;DE&#39;. | [optional] 
 **webSearch** | **String** | auto (let ChatGPT decide) | force (ask it to browse) | off (answer from memory). &#x60;web_search_triggered&#x60; in the response always reports what actually happened. | [optional] [default to &quot;auto&quot;]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **chatgptAskChatgptAQuestionPost**
```swift
    open class func chatgptAskChatgptAQuestionPost(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Ask ChatGPT a question (POST)

POST form of `/ask`, for prompts too long for a query string.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// Ask ChatGPT a question (POST)
ChatGPTAPI.chatgptAskChatgptAQuestionPost() { (response, error) in
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

# **chatgptChatgptScraperHealthCheck**
```swift
    open class func chatgptChatgptScraperHealthCheck(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

ChatGPT scraper health check

Check health of the ChatGPT scraper service (accepts HEAD).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// ChatGPT scraper health check
ChatGPTAPI.chatgptChatgptScraperHealthCheck() { (response, error) in
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

# **chatgptChatgptScraperHealthCheckHead**
```swift
    open class func chatgptChatgptScraperHealthCheckHead(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

ChatGPT scraper health check

Check health of the ChatGPT scraper service (accepts HEAD).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// ChatGPT scraper health check
ChatGPTAPI.chatgptChatgptScraperHealthCheckHead() { (response, error) in
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

# **chatgptListChatgptModels**
```swift
    open class func chatgptListChatgptModels(country: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

List ChatGPT models

Models chatgpt.com currently serves to an anonymous visitor.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let country = "country_example" // String | ISO-3166 alpha-2 egress country. (optional)

// List ChatGPT models
ChatGPTAPI.chatgptListChatgptModels(country: country) { (response, error) in
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

# **chatgptMeasureABrandSVisibilityInAChatgptAnswer**
```swift
    open class func chatgptMeasureABrandSVisibilityInAChatgptAnswer(prompt: String, brand: String, domain: String? = nil, aliases: String? = nil, competitors: String? = nil, country: String? = nil, webSearch: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Measure a brand's visibility in a ChatGPT answer

Ask ChatGPT, then report whether the brand is mentioned, cited and how prominently.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let prompt = "prompt_example" // String | The prompt to ask ChatGPT.
let brand = "brand_example" // String | Brand name to look for in the answer.
let domain = "domain_example" // String | Brand domain, for citation matching. (optional)
let aliases = "aliases_example" // String | Comma-separated alternative names. (optional)
let competitors = "competitors_example" // String | Comma-separated competitor names. (optional)
let country = "country_example" // String | ISO-3166 alpha-2 egress country. (optional)
let webSearch = "webSearch_example" // String | auto | force | off (optional) (default to "force")

// Measure a brand's visibility in a ChatGPT answer
ChatGPTAPI.chatgptMeasureABrandSVisibilityInAChatgptAnswer(prompt: prompt, brand: brand, domain: domain, aliases: aliases, competitors: competitors, country: country, webSearch: webSearch) { (response, error) in
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
 **prompt** | **String** | The prompt to ask ChatGPT. | 
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

# **chatgptMeasureABrandSVisibilityInAChatgptAnswerPost**
```swift
    open class func chatgptMeasureABrandSVisibilityInAChatgptAnswerPost(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Measure a brand's visibility in a ChatGPT answer (POST)

POST form, for longer prompts and larger competitor sets.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// Measure a brand's visibility in a ChatGPT answer (POST)
ChatGPTAPI.chatgptMeasureABrandSVisibilityInAChatgptAnswerPost() { (response, error) in
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

