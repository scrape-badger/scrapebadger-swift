# DuckDuckGoAPI

All URIs are relative to *https://scrapebadger.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**duckduckgoDuckduckgoScraperHealthCheck**](DuckDuckGoAPI.md#duckduckgoduckduckgoscraperhealthcheck) | **GET** /v1/duckduckgo/health | DuckDuckGo scraper health check
[**duckduckgoDuckduckgoScraperHealthCheckHead**](DuckDuckGoAPI.md#duckduckgoduckduckgoscraperhealthcheckhead) | **HEAD** /v1/duckduckgo/health | DuckDuckGo scraper health check
[**duckduckgoImageSearch**](DuckDuckGoAPI.md#duckduckgoimagesearch) | **GET** /v1/duckduckgo/images | Image search
[**duckduckgoInstantAnswer**](DuckDuckGoAPI.md#duckduckgoinstantanswer) | **GET** /v1/duckduckgo/instant | Instant Answer
[**duckduckgoListSupportedRegions**](DuckDuckGoAPI.md#duckduckgolistsupportedregions) | **GET** /v1/duckduckgo/regions | List supported regions
[**duckduckgoNewsSearch**](DuckDuckGoAPI.md#duckduckgonewssearch) | **GET** /v1/duckduckgo/news | News search
[**duckduckgoSearchSuggestions**](DuckDuckGoAPI.md#duckduckgosearchsuggestions) | **GET** /v1/duckduckgo/autocomplete | Search suggestions
[**duckduckgoVideoSearch**](DuckDuckGoAPI.md#duckduckgovideosearch) | **GET** /v1/duckduckgo/videos | Video search
[**duckduckgoWebSearch**](DuckDuckGoAPI.md#duckduckgowebsearch) | **GET** /v1/duckduckgo/search | Web search


# **duckduckgoDuckduckgoScraperHealthCheck**
```swift
    open class func duckduckgoDuckduckgoScraperHealthCheck(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

DuckDuckGo scraper health check

Check health of the DuckDuckGo scraper service (accepts HEAD for UptimeRobot).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// DuckDuckGo scraper health check
DuckDuckGoAPI.duckduckgoDuckduckgoScraperHealthCheck() { (response, error) in
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

# **duckduckgoDuckduckgoScraperHealthCheckHead**
```swift
    open class func duckduckgoDuckduckgoScraperHealthCheckHead(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

DuckDuckGo scraper health check

Check health of the DuckDuckGo scraper service (accepts HEAD for UptimeRobot).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// DuckDuckGo scraper health check
DuckDuckGoAPI.duckduckgoDuckduckgoScraperHealthCheckHead() { (response, error) in
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

# **duckduckgoImageSearch**
```swift
    open class func duckduckgoImageSearch(query: String, region: String? = nil, safesearch: String? = nil, page: Int? = nil, size: String? = nil, color: String? = nil, imageType: String? = nil, layout: String? = nil, license: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Image search

DuckDuckGo image search with size/color/type/layout/license filters.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let query = "query_example" // String | Search query
let region = "region_example" // String | DuckDuckGo region code (kl), e.g. us-en, uk-en, de-de. wt-wt = all regions. (optional) (default to "wt-wt")
let safesearch = "safesearch_example" // String | on | moderate | off (optional) (default to "moderate")
let page = 987 // Int | 100 results per page (optional) (default to 1)
let size = "size_example" // String | Small | Medium | Large | Wallpaper (optional) (default to "")
let color = "color_example" // String | color | Monochrome | Red | Blue | … (optional) (default to "")
let imageType = "imageType_example" // String | photo | clipart | gif | transparent | line (optional) (default to "")
let layout = "layout_example" // String | Square | Tall | Wide (optional) (default to "")
let license = "license_example" // String | Any | Public | Share | ShareCommercially | Modify (optional) (default to "")

// Image search
DuckDuckGoAPI.duckduckgoImageSearch(query: query, region: region, safesearch: safesearch, page: page, size: size, color: color, imageType: imageType, layout: layout, license: license) { (response, error) in
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
 **query** | **String** | Search query | 
 **region** | **String** | DuckDuckGo region code (kl), e.g. us-en, uk-en, de-de. wt-wt &#x3D; all regions. | [optional] [default to &quot;wt-wt&quot;]
 **safesearch** | **String** | on | moderate | off | [optional] [default to &quot;moderate&quot;]
 **page** | **Int** | 100 results per page | [optional] [default to 1]
 **size** | **String** | Small | Medium | Large | Wallpaper | [optional] [default to &quot;&quot;]
 **color** | **String** | color | Monochrome | Red | Blue | … | [optional] [default to &quot;&quot;]
 **imageType** | **String** | photo | clipart | gif | transparent | line | [optional] [default to &quot;&quot;]
 **layout** | **String** | Square | Tall | Wide | [optional] [default to &quot;&quot;]
 **license** | **String** | Any | Public | Share | ShareCommercially | Modify | [optional] [default to &quot;&quot;]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **duckduckgoInstantAnswer**
```swift
    open class func duckduckgoInstantAnswer(query: String, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Instant Answer

DuckDuckGo Instant Answer — abstract, definition, direct answer, related topics.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let query = "query_example" // String | Query for the Instant Answer API

// Instant Answer
DuckDuckGoAPI.duckduckgoInstantAnswer(query: query) { (response, error) in
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
 **query** | **String** | Query for the Instant Answer API | 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **duckduckgoListSupportedRegions**
```swift
    open class func duckduckgoListSupportedRegions(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

List supported regions

The full DuckDuckGo region (kl) code list.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// List supported regions
DuckDuckGoAPI.duckduckgoListSupportedRegions() { (response, error) in
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

# **duckduckgoNewsSearch**
```swift
    open class func duckduckgoNewsSearch(query: String, region: String? = nil, safesearch: String? = nil, timelimit: String? = nil, page: Int? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

News search

DuckDuckGo news search — headline, source, excerpt, unix + ISO date, image.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let query = "query_example" // String | Search query
let region = "region_example" // String | DuckDuckGo region code (kl), e.g. us-en, uk-en, de-de. wt-wt = all regions. (optional) (default to "wt-wt")
let safesearch = "safesearch_example" // String | on | moderate | off (optional) (default to "moderate")
let timelimit = "timelimit_example" // String | day | week | month | year (optional) (default to "")
let page = 987 // Int | 30 results per page (optional) (default to 1)

// News search
DuckDuckGoAPI.duckduckgoNewsSearch(query: query, region: region, safesearch: safesearch, timelimit: timelimit, page: page) { (response, error) in
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
 **query** | **String** | Search query | 
 **region** | **String** | DuckDuckGo region code (kl), e.g. us-en, uk-en, de-de. wt-wt &#x3D; all regions. | [optional] [default to &quot;wt-wt&quot;]
 **safesearch** | **String** | on | moderate | off | [optional] [default to &quot;moderate&quot;]
 **timelimit** | **String** | day | week | month | year | [optional] [default to &quot;&quot;]
 **page** | **Int** | 30 results per page | [optional] [default to 1]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **duckduckgoSearchSuggestions**
```swift
    open class func duckduckgoSearchSuggestions(query: String, region: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Search suggestions

DuckDuckGo search-box suggestions.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let query = "query_example" // String | Partial query to complete
let region = "region_example" // String | DuckDuckGo region code (kl), e.g. us-en, uk-en, de-de. wt-wt = all regions. (optional) (default to "wt-wt")

// Search suggestions
DuckDuckGoAPI.duckduckgoSearchSuggestions(query: query, region: region) { (response, error) in
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
 **query** | **String** | Partial query to complete | 
 **region** | **String** | DuckDuckGo region code (kl), e.g. us-en, uk-en, de-de. wt-wt &#x3D; all regions. | [optional] [default to &quot;wt-wt&quot;]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **duckduckgoVideoSearch**
```swift
    open class func duckduckgoVideoSearch(query: String, region: String? = nil, safesearch: String? = nil, page: Int? = nil, duration: String? = nil, resolution: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Video search

DuckDuckGo video search — title, publisher, uploader, duration, views, thumbnails.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let query = "query_example" // String | Search query
let region = "region_example" // String | DuckDuckGo region code (kl), e.g. us-en, uk-en, de-de. wt-wt = all regions. (optional) (default to "wt-wt")
let safesearch = "safesearch_example" // String | on | moderate | off (optional) (default to "moderate")
let page = 987 // Int | 60 results per page (optional) (default to 1)
let duration = "duration_example" // String | short | medium | long (optional) (default to "")
let resolution = "resolution_example" // String | high | standard (optional) (default to "")

// Video search
DuckDuckGoAPI.duckduckgoVideoSearch(query: query, region: region, safesearch: safesearch, page: page, duration: duration, resolution: resolution) { (response, error) in
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
 **query** | **String** | Search query | 
 **region** | **String** | DuckDuckGo region code (kl), e.g. us-en, uk-en, de-de. wt-wt &#x3D; all regions. | [optional] [default to &quot;wt-wt&quot;]
 **safesearch** | **String** | on | moderate | off | [optional] [default to &quot;moderate&quot;]
 **page** | **Int** | 60 results per page | [optional] [default to 1]
 **duration** | **String** | short | medium | long | [optional] [default to &quot;&quot;]
 **resolution** | **String** | high | standard | [optional] [default to &quot;&quot;]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **duckduckgoWebSearch**
```swift
    open class func duckduckgoWebSearch(query: String, region: String? = nil, safesearch: String? = nil, timelimit: String? = nil, page: Int? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Web search

DuckDuckGo web SERP — organic results, the zero-click abstract box, ads flagged.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let query = "query_example" // String | Search query
let region = "region_example" // String | DuckDuckGo region code (kl), e.g. us-en, uk-en, de-de. wt-wt = all regions. (optional) (default to "wt-wt")
let safesearch = "safesearch_example" // String | on | moderate | off (optional) (default to "moderate")
let timelimit = "timelimit_example" // String | day | week | month | year (optional) (default to "")
let page = 987 // Int |  (optional) (default to 1)

// Web search
DuckDuckGoAPI.duckduckgoWebSearch(query: query, region: region, safesearch: safesearch, timelimit: timelimit, page: page) { (response, error) in
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
 **query** | **String** | Search query | 
 **region** | **String** | DuckDuckGo region code (kl), e.g. us-en, uk-en, de-de. wt-wt &#x3D; all regions. | [optional] [default to &quot;wt-wt&quot;]
 **safesearch** | **String** | on | moderate | off | [optional] [default to &quot;moderate&quot;]
 **timelimit** | **String** | day | week | month | year | [optional] [default to &quot;&quot;]
 **page** | **Int** |  | [optional] [default to 1]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

