# BingAPI

All URIs are relative to *https://scrapebadger.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**bingBingScraperHealthCheck**](BingAPI.md#bingbingscraperhealthcheck) | **GET** /v1/bing/health | Bing scraper health check
[**bingBingScraperHealthCheckHead**](BingAPI.md#bingbingscraperhealthcheckhead) | **HEAD** /v1/bing/health | Bing scraper health check
[**bingImageSearch**](BingAPI.md#bingimagesearch) | **GET** /v1/bing/images | Image search
[**bingListSupportedMarkets**](BingAPI.md#binglistsupportedmarkets) | **GET** /v1/bing/markets | List supported markets
[**bingNewsSearch**](BingAPI.md#bingnewssearch) | **GET** /v1/bing/news | News search
[**bingSearchSuggestions**](BingAPI.md#bingsearchsuggestions) | **GET** /v1/bing/autocomplete | Search suggestions
[**bingVideoSearch**](BingAPI.md#bingvideosearch) | **GET** /v1/bing/videos | Video search
[**bingWebSearch**](BingAPI.md#bingwebsearch) | **GET** /v1/bing/search | Web search


# **bingBingScraperHealthCheck**
```swift
    open class func bingBingScraperHealthCheck(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Bing scraper health check

Check health of the Bing scraper service (accepts HEAD for UptimeRobot).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// Bing scraper health check
BingAPI.bingBingScraperHealthCheck() { (response, error) in
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

# **bingBingScraperHealthCheckHead**
```swift
    open class func bingBingScraperHealthCheckHead(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Bing scraper health check

Check health of the Bing scraper service (accepts HEAD for UptimeRobot).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// Bing scraper health check
BingAPI.bingBingScraperHealthCheckHead() { (response, error) in
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

# **bingImageSearch**
```swift
    open class func bingImageSearch(query: String, market: String? = nil, count: Int? = nil, safeSearch: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Image search

Bing Images — thumbnail, full-size and source URL per result.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let query = "query_example" // String | Search keywords, e.g. 'golden retriever'
let market = "market_example" // String | Bing market code, e.g. 'en-US', 'en-GB', 'de-DE'. See /markets. (optional) (default to "en-US")
let count = 987 // Int | Results to return (optional) (default to 35)
let safeSearch = "safeSearch_example" // String | off | moderate | strict (optional)

// Image search
BingAPI.bingImageSearch(query: query, market: market, count: count, safeSearch: safeSearch) { (response, error) in
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
 **query** | **String** | Search keywords, e.g. &#39;golden retriever&#39; | 
 **market** | **String** | Bing market code, e.g. &#39;en-US&#39;, &#39;en-GB&#39;, &#39;de-DE&#39;. See /markets. | [optional] [default to &quot;en-US&quot;]
 **count** | **Int** | Results to return | [optional] [default to 35]
 **safeSearch** | **String** | off | moderate | strict | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **bingListSupportedMarkets**
```swift
    open class func bingListSupportedMarkets(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

List supported markets

Supported Bing market codes. Free — costs no credits.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// List supported markets
BingAPI.bingListSupportedMarkets() { (response, error) in
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

# **bingNewsSearch**
```swift
    open class func bingNewsSearch(query: String, market: String? = nil, freshness: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

News search

Bing News — headline, source, published time and snippet per article.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let query = "query_example" // String | Search keywords, e.g. 'interest rates'
let market = "market_example" // String | Bing market code, e.g. 'en-US', 'en-GB', 'de-DE'. See /markets. (optional) (default to "en-US")
let freshness = "freshness_example" // String | day | week | month — restrict to recent articles (optional)

// News search
BingAPI.bingNewsSearch(query: query, market: market, freshness: freshness) { (response, error) in
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
 **query** | **String** | Search keywords, e.g. &#39;interest rates&#39; | 
 **market** | **String** | Bing market code, e.g. &#39;en-US&#39;, &#39;en-GB&#39;, &#39;de-DE&#39;. See /markets. | [optional] [default to &quot;en-US&quot;]
 **freshness** | **String** | day | week | month — restrict to recent articles | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **bingSearchSuggestions**
```swift
    open class func bingSearchSuggestions(query: String, market: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Search suggestions

Bing search-box query suggestions.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let query = "query_example" // String | Partial search term, e.g. 'coff'
let market = "market_example" // String | Bing market code, e.g. 'en-US', 'en-GB', 'de-DE'. See /markets. (optional) (default to "en-US")

// Search suggestions
BingAPI.bingSearchSuggestions(query: query, market: market) { (response, error) in
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
 **query** | **String** | Partial search term, e.g. &#39;coff&#39; | 
 **market** | **String** | Bing market code, e.g. &#39;en-US&#39;, &#39;en-GB&#39;, &#39;de-DE&#39;. See /markets. | [optional] [default to &quot;en-US&quot;]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **bingVideoSearch**
```swift
    open class func bingVideoSearch(query: String, market: String? = nil, count: Int? = nil, safeSearch: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Video search

Bing Videos — title, thumbnail, duration, publisher and source per result.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let query = "query_example" // String | Search keywords, e.g. 'espresso tutorial'
let market = "market_example" // String | Bing market code, e.g. 'en-US', 'en-GB', 'de-DE'. See /markets. (optional) (default to "en-US")
let count = 987 // Int | Results to return (optional) (default to 35)
let safeSearch = "safeSearch_example" // String | off | moderate | strict (optional)

// Video search
BingAPI.bingVideoSearch(query: query, market: market, count: count, safeSearch: safeSearch) { (response, error) in
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
 **query** | **String** | Search keywords, e.g. &#39;espresso tutorial&#39; | 
 **market** | **String** | Bing market code, e.g. &#39;en-US&#39;, &#39;en-GB&#39;, &#39;de-DE&#39;. See /markets. | [optional] [default to &quot;en-US&quot;]
 **count** | **Int** | Results to return | [optional] [default to 35]
 **safeSearch** | **String** | off | moderate | strict | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **bingWebSearch**
```swift
    open class func bingWebSearch(query: String, market: String? = nil, count: Int? = nil, offset: Int? = nil, safeSearch: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Web search

Bing web SERP — organic results, ads, related searches and total count.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let query = "query_example" // String | Search keywords, e.g. 'coffee machine'
let market = "market_example" // String | Bing market code, e.g. 'en-US', 'en-GB', 'de-DE'. See /markets. (optional) (default to "en-US")
let count = 987 // Int | Results per page (1-50) (optional) (default to 10)
let offset = 987 // Int | Zero-based result offset for pagination (optional) (default to 0)
let safeSearch = "safeSearch_example" // String | off | moderate | strict (default moderate) (optional)

// Web search
BingAPI.bingWebSearch(query: query, market: market, count: count, offset: offset, safeSearch: safeSearch) { (response, error) in
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
 **query** | **String** | Search keywords, e.g. &#39;coffee machine&#39; | 
 **market** | **String** | Bing market code, e.g. &#39;en-US&#39;, &#39;en-GB&#39;, &#39;de-DE&#39;. See /markets. | [optional] [default to &quot;en-US&quot;]
 **count** | **Int** | Results per page (1-50) | [optional] [default to 10]
 **offset** | **Int** | Zero-based result offset for pagination | [optional] [default to 0]
 **safeSearch** | **String** | off | moderate | strict (default moderate) | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

