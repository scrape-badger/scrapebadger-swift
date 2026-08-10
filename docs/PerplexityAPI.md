# PerplexityAPI

All URIs are relative to *https://scrapebadger.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**perplexityAskPerplexityAQuestion**](PerplexityAPI.md#perplexityaskperplexityaquestion) | **GET** /v1/perplexity/ask | Ask Perplexity a question
[**perplexityAskPerplexityAQuestionPost**](PerplexityAPI.md#perplexityaskperplexityaquestionpost) | **POST** /v1/perplexity/ask | Ask Perplexity a question (POST)
[**perplexityMeasureABrandSVisibilityInAPerplexityAnswer**](PerplexityAPI.md#perplexitymeasureabrandsvisibilityinaperplexityanswer) | **GET** /v1/perplexity/brand-visibility | Measure a brand&#39;s visibility in a Perplexity answer
[**perplexityMeasureABrandSVisibilityInAPerplexityAnswerPost**](PerplexityAPI.md#perplexitymeasureabrandsvisibilityinaperplexityanswerpost) | **POST** /v1/perplexity/brand-visibility | Measure a brand&#39;s visibility in a Perplexity answer (POST)
[**perplexityPerplexityScraperHealthCheck**](PerplexityAPI.md#perplexityperplexityscraperhealthcheck) | **GET** /v1/perplexity/health | Perplexity scraper health check
[**perplexityPerplexityScraperHealthCheckHead**](PerplexityAPI.md#perplexityperplexityscraperhealthcheckhead) | **HEAD** /v1/perplexity/health | Perplexity scraper health check


# **perplexityAskPerplexityAQuestion**
```swift
    open class func perplexityAskPerplexityAQuestion(prompt: String, country: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Ask Perplexity a question

Send a prompt to Perplexity and get the answer plus the web sources it cited.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let prompt = "prompt_example" // String | The prompt to send to Perplexity (max 4096 characters).
let country = "country_example" // String | ISO-3166 alpha-2 egress country, e.g. 'US', 'GB', 'DE'. (optional)

// Ask Perplexity a question
PerplexityAPI.perplexityAskPerplexityAQuestion(prompt: prompt, country: country) { (response, error) in
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
 **prompt** | **String** | The prompt to send to Perplexity (max 4096 characters). | 
 **country** | **String** | ISO-3166 alpha-2 egress country, e.g. &#39;US&#39;, &#39;GB&#39;, &#39;DE&#39;. | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **perplexityAskPerplexityAQuestionPost**
```swift
    open class func perplexityAskPerplexityAQuestionPost(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Ask Perplexity a question (POST)

POST form of `/ask`, for prompts too long for a query string.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// Ask Perplexity a question (POST)
PerplexityAPI.perplexityAskPerplexityAQuestionPost() { (response, error) in
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

# **perplexityMeasureABrandSVisibilityInAPerplexityAnswer**
```swift
    open class func perplexityMeasureABrandSVisibilityInAPerplexityAnswer(prompt: String, brand: String, domain: String? = nil, aliases: String? = nil, competitors: String? = nil, country: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Measure a brand's visibility in a Perplexity answer

Ask Perplexity, then report whether the brand is mentioned, cited and how prominently.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let prompt = "prompt_example" // String | The prompt to ask Perplexity.
let brand = "brand_example" // String | Brand name to look for in the answer.
let domain = "domain_example" // String | Brand domain, for citation matching. (optional)
let aliases = "aliases_example" // String | Comma-separated alternative names. (optional)
let competitors = "competitors_example" // String | Comma-separated competitor names. (optional)
let country = "country_example" // String | ISO-3166 alpha-2 egress country. (optional)

// Measure a brand's visibility in a Perplexity answer
PerplexityAPI.perplexityMeasureABrandSVisibilityInAPerplexityAnswer(prompt: prompt, brand: brand, domain: domain, aliases: aliases, competitors: competitors, country: country) { (response, error) in
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
 **prompt** | **String** | The prompt to ask Perplexity. | 
 **brand** | **String** | Brand name to look for in the answer. | 
 **domain** | **String** | Brand domain, for citation matching. | [optional] 
 **aliases** | **String** | Comma-separated alternative names. | [optional] 
 **competitors** | **String** | Comma-separated competitor names. | [optional] 
 **country** | **String** | ISO-3166 alpha-2 egress country. | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **perplexityMeasureABrandSVisibilityInAPerplexityAnswerPost**
```swift
    open class func perplexityMeasureABrandSVisibilityInAPerplexityAnswerPost(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Measure a brand's visibility in a Perplexity answer (POST)

POST form, for longer prompts and larger competitor sets.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// Measure a brand's visibility in a Perplexity answer (POST)
PerplexityAPI.perplexityMeasureABrandSVisibilityInAPerplexityAnswerPost() { (response, error) in
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

# **perplexityPerplexityScraperHealthCheck**
```swift
    open class func perplexityPerplexityScraperHealthCheck(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Perplexity scraper health check

Check health of the Perplexity scraper service (accepts HEAD).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// Perplexity scraper health check
PerplexityAPI.perplexityPerplexityScraperHealthCheck() { (response, error) in
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

# **perplexityPerplexityScraperHealthCheckHead**
```swift
    open class func perplexityPerplexityScraperHealthCheckHead(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Perplexity scraper health check

Check health of the Perplexity scraper service (accepts HEAD).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// Perplexity scraper health check
PerplexityAPI.perplexityPerplexityScraperHealthCheckHead() { (response, error) in
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

