# BaiduAPI

All URIs are relative to *https://scrapebadger.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**baiduBaiduImageSearch**](BaiduAPI.md#baidubaiduimagesearch) | **GET** /v1/baidu/images | Baidu image search
[**baiduBaiduNewsSearch**](BaiduAPI.md#baidubaidunewssearch) | **GET** /v1/baidu/news | Baidu news search
[**baiduBaiduScraperHealthCheck**](BaiduAPI.md#baidubaiduscraperhealthcheck) | **GET** /v1/baidu/health | Baidu scraper health check
[**baiduBaiduScraperHealthCheckHead**](BaiduAPI.md#baidubaiduscraperhealthcheckhead) | **HEAD** /v1/baidu/health | Baidu scraper health check
[**baiduBaiduWebSearch**](BaiduAPI.md#baidubaiduwebsearch) | **GET** /v1/baidu/search | Baidu web search
[**baiduSearchSuggestions**](BaiduAPI.md#baidusearchsuggestions) | **GET** /v1/baidu/autocomplete | Search suggestions


# **baiduBaiduImageSearch**
```swift
    open class func baiduBaiduImageSearch(query: String, page: Int? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Baidu image search

Baidu image search via the acjson JSON API.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let query = "query_example" // String | Search keywords
let page = 987 // Int | 30 images per page (optional) (default to 1)

// Baidu image search
BaiduAPI.baiduBaiduImageSearch(query: query, page: page) { (response, error) in
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
 **query** | **String** | Search keywords | 
 **page** | **Int** | 30 images per page | [optional] [default to 1]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **baiduBaiduNewsSearch**
```swift
    open class func baiduBaiduNewsSearch(query: String, page: Int? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Baidu news search

Baidu news vertical — articles with source, publish date and real URLs.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let query = "query_example" // String | Search keywords
let page = 987 // Int |  (optional) (default to 1)

// Baidu news search
BaiduAPI.baiduBaiduNewsSearch(query: query, page: page) { (response, error) in
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
 **query** | **String** | Search keywords | 
 **page** | **Int** |  | [optional] [default to 1]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **baiduBaiduScraperHealthCheck**
```swift
    open class func baiduBaiduScraperHealthCheck(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Baidu scraper health check

Check health of the Baidu scraper service (accepts HEAD for UptimeRobot).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// Baidu scraper health check
BaiduAPI.baiduBaiduScraperHealthCheck() { (response, error) in
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

# **baiduBaiduScraperHealthCheckHead**
```swift
    open class func baiduBaiduScraperHealthCheckHead(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Baidu scraper health check

Check health of the Baidu scraper service (accepts HEAD for UptimeRobot).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// Baidu scraper health check
BaiduAPI.baiduBaiduScraperHealthCheckHead() { (response, error) in
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

# **baiduBaiduWebSearch**
```swift
    open class func baiduBaiduWebSearch(query: String, page: Int? = nil, num: Int? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Baidu web search

Baidu web SERP — organic results with real target URLs, related searches, total count.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let query = "query_example" // String | Search keywords, e.g. '咖啡机' or 'coffee machine'
let page = 987 // Int | Result page (10 results per page) (optional) (default to 1)
let num = 987 // Int | Results per page (rn) (optional) (default to 10)

// Baidu web search
BaiduAPI.baiduBaiduWebSearch(query: query, page: page, num: num) { (response, error) in
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
 **query** | **String** | Search keywords, e.g. &#39;咖啡机&#39; or &#39;coffee machine&#39; | 
 **page** | **Int** | Result page (10 results per page) | [optional] [default to 1]
 **num** | **Int** | Results per page (rn) | [optional] [default to 10]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **baiduSearchSuggestions**
```swift
    open class func baiduSearchSuggestions(query: String, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Search suggestions

Baidu search-box suggestions.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let query = "query_example" // String | Partial search term, e.g. '咖啡' or 'coff'

// Search suggestions
BaiduAPI.baiduSearchSuggestions(query: query) { (response, error) in
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
 **query** | **String** | Partial search term, e.g. &#39;咖啡&#39; or &#39;coff&#39; | 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

