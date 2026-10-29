# CopilotAPI

All URIs are relative to *https://scrapebadger.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**copilotAskCopilotAQuestion**](CopilotAPI.md#copilotaskcopilotaquestion) | **GET** /v1/copilot/ask | Ask Copilot a question
[**copilotAskCopilotAQuestionPost**](CopilotAPI.md#copilotaskcopilotaquestionpost) | **POST** /v1/copilot/ask | Ask Copilot a question (POST)
[**copilotCopilotScraperHealthCheck**](CopilotAPI.md#copilotcopilotscraperhealthcheck) | **GET** /v1/copilot/health | Copilot scraper health check
[**copilotCopilotScraperHealthCheckHead**](CopilotAPI.md#copilotcopilotscraperhealthcheckhead) | **HEAD** /v1/copilot/health | Copilot scraper health check
[**copilotListCopilotMarkets**](CopilotAPI.md#copilotlistcopilotmarkets) | **GET** /v1/copilot/markets | List Copilot markets
[**copilotMeasureABrandSVisibilityInACopilotAnswer**](CopilotAPI.md#copilotmeasureabrandsvisibilityinacopilotanswer) | **GET** /v1/copilot/brand-visibility | Measure a brand&#39;s visibility in a Copilot answer
[**copilotMeasureABrandSVisibilityInACopilotAnswerPost**](CopilotAPI.md#copilotmeasureabrandsvisibilityinacopilotanswerpost) | **POST** /v1/copilot/brand-visibility | Measure a brand&#39;s visibility in a Copilot answer (POST)


# **copilotAskCopilotAQuestion**
```swift
    open class func copilotAskCopilotAQuestion(prompt: String, country: String? = nil, market: String? = nil, strictCountry: Bool? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Ask Copilot a question

Ask Microsoft Copilot (Copilot Search in Bing) and get the answer plus its cited sources.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let prompt = "prompt_example" // String | The prompt to send to Copilot (max 2000 characters).
let country = "country_example" // String | ISO-3166 alpha-2 country to ask from, e.g. 'JP', 'US', 'GB'. Unless `market` is set, Copilot also answers in that country's market. (optional)
let market = "market_example" // String | Bing market (language-COUNTRY), e.g. 'ja-JP', 'en-GB'. Defaults to the country's. (optional)
let strictCountry = true // Bool | Answer only from an exit in `country`, never another one; 503 `country_unavailable` (not billed) when none answers. Requires `country`. (optional) (default to false)

// Ask Copilot a question
CopilotAPI.copilotAskCopilotAQuestion(prompt: prompt, country: country, market: market, strictCountry: strictCountry) { (response, error) in
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
 **prompt** | **String** | The prompt to send to Copilot (max 2000 characters). | 
 **country** | **String** | ISO-3166 alpha-2 country to ask from, e.g. &#39;JP&#39;, &#39;US&#39;, &#39;GB&#39;. Unless &#x60;market&#x60; is set, Copilot also answers in that country&#39;s market. | [optional] 
 **market** | **String** | Bing market (language-COUNTRY), e.g. &#39;ja-JP&#39;, &#39;en-GB&#39;. Defaults to the country&#39;s. | [optional] 
 **strictCountry** | **Bool** | Answer only from an exit in &#x60;country&#x60;, never another one; 503 &#x60;country_unavailable&#x60; (not billed) when none answers. Requires &#x60;country&#x60;. | [optional] [default to false]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **copilotAskCopilotAQuestionPost**
```swift
    open class func copilotAskCopilotAQuestionPost(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Ask Copilot a question (POST)

POST form of `/ask`, for prompts too long for a query string.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// Ask Copilot a question (POST)
CopilotAPI.copilotAskCopilotAQuestionPost() { (response, error) in
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

# **copilotCopilotScraperHealthCheck**
```swift
    open class func copilotCopilotScraperHealthCheck(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Copilot scraper health check

Check health of the Copilot scraper service (accepts HEAD).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// Copilot scraper health check
CopilotAPI.copilotCopilotScraperHealthCheck() { (response, error) in
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

# **copilotCopilotScraperHealthCheckHead**
```swift
    open class func copilotCopilotScraperHealthCheckHead(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Copilot scraper health check

Check health of the Copilot scraper service (accepts HEAD).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// Copilot scraper health check
CopilotAPI.copilotCopilotScraperHealthCheckHead() { (response, error) in
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

# **copilotListCopilotMarkets**
```swift
    open class func copilotListCopilotMarkets(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

List Copilot markets

The Bing markets Copilot can be asked in.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// List Copilot markets
CopilotAPI.copilotListCopilotMarkets() { (response, error) in
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

# **copilotMeasureABrandSVisibilityInACopilotAnswer**
```swift
    open class func copilotMeasureABrandSVisibilityInACopilotAnswer(prompt: String, brand: String, domain: String? = nil, aliases: String? = nil, competitors: String? = nil, country: String? = nil, market: String? = nil, strictCountry: Bool? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Measure a brand's visibility in a Copilot answer

Ask Copilot, then report whether the brand is mentioned, cited and how prominently.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let prompt = "prompt_example" // String | The prompt to ask Copilot.
let brand = "brand_example" // String | Brand name to look for in the answer.
let domain = "domain_example" // String | Brand domain, for citation matching. (optional)
let aliases = "aliases_example" // String | Comma-separated alternative names. (optional)
let competitors = "competitors_example" // String | Comma-separated competitor names. (optional)
let country = "country_example" // String | ISO-3166 alpha-2 country to ask from, e.g. 'JP', 'US', 'GB'. Unless `market` is set, Copilot also answers in that country's market. (optional)
let market = "market_example" // String | Bing market (language-COUNTRY), e.g. 'ja-JP', 'en-GB'. Defaults to the country's. (optional)
let strictCountry = true // Bool | Answer only from an exit in `country`, never another one; 503 `country_unavailable` (not billed) when none answers. Requires `country`. (optional) (default to false)

// Measure a brand's visibility in a Copilot answer
CopilotAPI.copilotMeasureABrandSVisibilityInACopilotAnswer(prompt: prompt, brand: brand, domain: domain, aliases: aliases, competitors: competitors, country: country, market: market, strictCountry: strictCountry) { (response, error) in
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
 **prompt** | **String** | The prompt to ask Copilot. | 
 **brand** | **String** | Brand name to look for in the answer. | 
 **domain** | **String** | Brand domain, for citation matching. | [optional] 
 **aliases** | **String** | Comma-separated alternative names. | [optional] 
 **competitors** | **String** | Comma-separated competitor names. | [optional] 
 **country** | **String** | ISO-3166 alpha-2 country to ask from, e.g. &#39;JP&#39;, &#39;US&#39;, &#39;GB&#39;. Unless &#x60;market&#x60; is set, Copilot also answers in that country&#39;s market. | [optional] 
 **market** | **String** | Bing market (language-COUNTRY), e.g. &#39;ja-JP&#39;, &#39;en-GB&#39;. Defaults to the country&#39;s. | [optional] 
 **strictCountry** | **Bool** | Answer only from an exit in &#x60;country&#x60;, never another one; 503 &#x60;country_unavailable&#x60; (not billed) when none answers. Requires &#x60;country&#x60;. | [optional] [default to false]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **copilotMeasureABrandSVisibilityInACopilotAnswerPost**
```swift
    open class func copilotMeasureABrandSVisibilityInACopilotAnswerPost(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Measure a brand's visibility in a Copilot answer (POST)

POST form, for longer prompts and larger competitor sets.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// Measure a brand's visibility in a Copilot answer (POST)
CopilotAPI.copilotMeasureABrandSVisibilityInACopilotAnswerPost() { (response, error) in
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

