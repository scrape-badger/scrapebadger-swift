# YandexAPI

All URIs are relative to *https://scrapebadger.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**yandexImageSearch**](YandexAPI.md#yandeximagesearch) | **GET** /v1/yandex/images/search | Image search
[**yandexListSupportedMarkets**](YandexAPI.md#yandexlistsupportedmarkets) | **GET** /v1/yandex/markets | List supported markets
[**yandexReverseImageSearch**](YandexAPI.md#yandexreverseimagesearch) | **GET** /v1/yandex/images/reverse | Reverse image search
[**yandexWebSearch**](YandexAPI.md#yandexwebsearch) | **GET** /v1/yandex/search | Web search
[**yandexYandexScraperHealthCheck**](YandexAPI.md#yandexyandexscraperhealthcheck) | **GET** /v1/yandex/health | Yandex scraper health check
[**yandexYandexScraperHealthCheckHead**](YandexAPI.md#yandexyandexscraperhealthcheckhead) | **HEAD** /v1/yandex/health | Yandex scraper health check


# **yandexImageSearch**
```swift
    open class func yandexImageSearch(query: String, domain: String? = nil, page: Int? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Image search

Search Yandex Images by text — thumbnail, full-res URL, dimensions, source page.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let query = "query_example" // String | Image search query, e.g. 'coffee machine'
let domain = "domain_example" // String | Yandex market: 'tr' (yandex.com.tr, DEFAULT — the domain that reliably clears anti-bot), 'com', 'ru', 'by', 'kz', 'uz'. 'com'/'ru' have a lower success rate. (optional) (default to "tr")
let page = 987 // Int |  (optional) (default to 1)

// Image search
YandexAPI.yandexImageSearch(query: query, domain: domain, page: page) { (response, error) in
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
 **query** | **String** | Image search query, e.g. &#39;coffee machine&#39; | 
 **domain** | **String** | Yandex market: &#39;tr&#39; (yandex.com.tr, DEFAULT — the domain that reliably clears anti-bot), &#39;com&#39;, &#39;ru&#39;, &#39;by&#39;, &#39;kz&#39;, &#39;uz&#39;. &#39;com&#39;/&#39;ru&#39; have a lower success rate. | [optional] [default to &quot;tr&quot;]
 **page** | **Int** |  | [optional] [default to 1]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **yandexListSupportedMarkets**
```swift
    open class func yandexListSupportedMarkets(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

List supported markets

Supported Yandex markets (domains, default region and language).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// List supported markets
YandexAPI.yandexListSupportedMarkets() { (response, error) in
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

# **yandexReverseImageSearch**
```swift
    open class func yandexReverseImageSearch(imageUrl: String, domain: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Reverse image search

Reverse image search by URL — hosting pages, similar images, tags, other sizes.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let imageUrl = "imageUrl_example" // String | Public URL of the image to reverse-search
let domain = "domain_example" // String | Yandex market: 'tr' (yandex.com.tr, DEFAULT — the domain that reliably clears anti-bot), 'com', 'ru', 'by', 'kz', 'uz'. 'com'/'ru' have a lower success rate. (optional) (default to "tr")

// Reverse image search
YandexAPI.yandexReverseImageSearch(imageUrl: imageUrl, domain: domain) { (response, error) in
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
 **imageUrl** | **String** | Public URL of the image to reverse-search | 
 **domain** | **String** | Yandex market: &#39;tr&#39; (yandex.com.tr, DEFAULT — the domain that reliably clears anti-bot), &#39;com&#39;, &#39;ru&#39;, &#39;by&#39;, &#39;kz&#39;, &#39;uz&#39;. &#39;com&#39;/&#39;ru&#39; have a lower success rate. | [optional] [default to &quot;tr&quot;]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **yandexWebSearch**
```swift
    open class func yandexWebSearch(query: String, domain: String? = nil, page: Int? = nil, lr: Int? = nil, lang: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Web search

Search Yandex web results — organic results, ads, displayed URLs, snippets.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let query = "query_example" // String | Search query, e.g. 'coffee machine'
let domain = "domain_example" // String | Yandex market: 'tr' (yandex.com.tr, DEFAULT — the domain that reliably clears anti-bot), 'com', 'ru', 'by', 'kz', 'uz'. 'com'/'ru' have a lower success rate. (optional) (default to "tr")
let page = 987 // Int |  (optional) (default to 1)
let lr = 987 // Int | Yandex region id, e.g. 213=Moscow, 84=USA (optional)
let lang = "lang_example" // String | UI language: ru, en, tr, be, kk, uk (optional)

// Web search
YandexAPI.yandexWebSearch(query: query, domain: domain, page: page, lr: lr, lang: lang) { (response, error) in
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
 **query** | **String** | Search query, e.g. &#39;coffee machine&#39; | 
 **domain** | **String** | Yandex market: &#39;tr&#39; (yandex.com.tr, DEFAULT — the domain that reliably clears anti-bot), &#39;com&#39;, &#39;ru&#39;, &#39;by&#39;, &#39;kz&#39;, &#39;uz&#39;. &#39;com&#39;/&#39;ru&#39; have a lower success rate. | [optional] [default to &quot;tr&quot;]
 **page** | **Int** |  | [optional] [default to 1]
 **lr** | **Int** | Yandex region id, e.g. 213&#x3D;Moscow, 84&#x3D;USA | [optional] 
 **lang** | **String** | UI language: ru, en, tr, be, kk, uk | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **yandexYandexScraperHealthCheck**
```swift
    open class func yandexYandexScraperHealthCheck(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Yandex scraper health check

Check health of the Yandex scraper service (accepts HEAD for UptimeRobot).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// Yandex scraper health check
YandexAPI.yandexYandexScraperHealthCheck() { (response, error) in
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

# **yandexYandexScraperHealthCheckHead**
```swift
    open class func yandexYandexScraperHealthCheckHead(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Yandex scraper health check

Check health of the Yandex scraper service (accepts HEAD for UptimeRobot).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// Yandex scraper health check
YandexAPI.yandexYandexScraperHealthCheckHead() { (response, error) in
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

