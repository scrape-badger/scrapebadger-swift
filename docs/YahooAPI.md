# YahooAPI

All URIs are relative to *https://scrapebadger.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**yahooImageSearch**](YahooAPI.md#yahooimagesearch) | **GET** /v1/yahoo/images | Image search
[**yahooListSupportedMarkets**](YahooAPI.md#yahoolistsupportedmarkets) | **GET** /v1/yahoo/markets | List supported markets
[**yahooNewsSearch**](YahooAPI.md#yahoonewssearch) | **GET** /v1/yahoo/news | News search
[**yahooSearchSuggestions**](YahooAPI.md#yahoosearchsuggestions) | **GET** /v1/yahoo/autocomplete | Search suggestions
[**yahooVideoSearch**](YahooAPI.md#yahoovideosearch) | **GET** /v1/yahoo/videos | Video search
[**yahooWebSearch**](YahooAPI.md#yahoowebsearch) | **GET** /v1/yahoo/search | Web search
[**yahooYahooScraperHealthCheck**](YahooAPI.md#yahooyahooscraperhealthcheck) | **GET** /v1/yahoo/health | Yahoo scraper health check
[**yahooYahooScraperHealthCheckHead**](YahooAPI.md#yahooyahooscraperhealthcheckhead) | **HEAD** /v1/yahoo/health | Yahoo scraper health check


# **yahooImageSearch**
```swift
    open class func yahooImageSearch(query: String, market: String? = nil, count: Int? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Image search

Yahoo Images — thumbnail, full-size and source URL per result.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let query = "query_example" // String | Search keywords, e.g. 'golden retriever'
let market = "market_example" // String | Yahoo market code, e.g. 'us', 'uk', 'fr', 'de'. See /markets. (optional) (default to "us")
let count = 987 // Int | Results to return (optional) (default to 30)

// Image search
YahooAPI.yahooImageSearch(query: query, market: market, count: count) { (response, error) in
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
 **market** | **String** | Yahoo market code, e.g. &#39;us&#39;, &#39;uk&#39;, &#39;fr&#39;, &#39;de&#39;. See /markets. | [optional] [default to &quot;us&quot;]
 **count** | **Int** | Results to return | [optional] [default to 30]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **yahooListSupportedMarkets**
```swift
    open class func yahooListSupportedMarkets(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

List supported markets

Supported Yahoo market codes. Free — costs no credits.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// List supported markets
YahooAPI.yahooListSupportedMarkets() { (response, error) in
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

# **yahooNewsSearch**
```swift
    open class func yahooNewsSearch(query: String, market: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

News search

Yahoo News — headline, source, published time and snippet per article.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let query = "query_example" // String | Search keywords, e.g. 'interest rates'
let market = "market_example" // String | Yahoo market code, e.g. 'us', 'uk', 'fr', 'de'. See /markets. (optional) (default to "us")

// News search
YahooAPI.yahooNewsSearch(query: query, market: market) { (response, error) in
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
 **market** | **String** | Yahoo market code, e.g. &#39;us&#39;, &#39;uk&#39;, &#39;fr&#39;, &#39;de&#39;. See /markets. | [optional] [default to &quot;us&quot;]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **yahooSearchSuggestions**
```swift
    open class func yahooSearchSuggestions(query: String, market: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Search suggestions

Yahoo search-box query suggestions.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let query = "query_example" // String | Partial search term, e.g. 'coff'
let market = "market_example" // String | Yahoo market code, e.g. 'us', 'uk', 'fr', 'de'. See /markets. (optional) (default to "us")

// Search suggestions
YahooAPI.yahooSearchSuggestions(query: query, market: market) { (response, error) in
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
 **market** | **String** | Yahoo market code, e.g. &#39;us&#39;, &#39;uk&#39;, &#39;fr&#39;, &#39;de&#39;. See /markets. | [optional] [default to &quot;us&quot;]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **yahooVideoSearch**
```swift
    open class func yahooVideoSearch(query: String, market: String? = nil, count: Int? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Video search

Yahoo Videos — title, thumbnail, duration, publisher and source per result.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let query = "query_example" // String | Search keywords, e.g. 'espresso tutorial'
let market = "market_example" // String | Yahoo market code, e.g. 'us', 'uk', 'fr', 'de'. See /markets. (optional) (default to "us")
let count = 987 // Int | Results to return (optional) (default to 30)

// Video search
YahooAPI.yahooVideoSearch(query: query, market: market, count: count) { (response, error) in
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
 **market** | **String** | Yahoo market code, e.g. &#39;us&#39;, &#39;uk&#39;, &#39;fr&#39;, &#39;de&#39;. See /markets. | [optional] [default to &quot;us&quot;]
 **count** | **Int** | Results to return | [optional] [default to 30]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **yahooWebSearch**
```swift
    open class func yahooWebSearch(query: String, market: String? = nil, offset: Int? = nil, safeSearch: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Web search

Yahoo web SERP — organic results, ads, related searches and total count.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let query = "query_example" // String | Search keywords, e.g. 'coffee machine'
let market = "market_example" // String | Yahoo market code, e.g. 'us', 'uk', 'fr', 'de'. See /markets. (optional) (default to "us")
let offset = 987 // Int | Zero-based result offset for pagination (optional) (default to 0)
let safeSearch = "safeSearch_example" // String | off | moderate | strict (default moderate) (optional)

// Web search
YahooAPI.yahooWebSearch(query: query, market: market, offset: offset, safeSearch: safeSearch) { (response, error) in
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
 **market** | **String** | Yahoo market code, e.g. &#39;us&#39;, &#39;uk&#39;, &#39;fr&#39;, &#39;de&#39;. See /markets. | [optional] [default to &quot;us&quot;]
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

# **yahooYahooScraperHealthCheck**
```swift
    open class func yahooYahooScraperHealthCheck(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Yahoo scraper health check

Check health of the Yahoo scraper service (accepts HEAD for UptimeRobot).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// Yahoo scraper health check
YahooAPI.yahooYahooScraperHealthCheck() { (response, error) in
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

# **yahooYahooScraperHealthCheckHead**
```swift
    open class func yahooYahooScraperHealthCheckHead(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Yahoo scraper health check

Check health of the Yahoo scraper service (accepts HEAD for UptimeRobot).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// Yahoo scraper health check
YahooAPI.yahooYahooScraperHealthCheckHead() { (response, error) in
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

