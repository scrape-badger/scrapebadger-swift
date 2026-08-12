# AppStoreAPI

All URIs are relative to *https://scrapebadger.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**appStoreGetAppDetail**](AppStoreAPI.md#appstoregetappdetail) | **GET** /v1/app-store/apps/{app_id} | Get app detail
[**appStoreGetAppReviews**](AppStoreAPI.md#appstoregetappreviews) | **GET** /v1/app-store/apps/{app_id}/reviews | Get app reviews
[**appStoreGetDeveloperApps**](AppStoreAPI.md#appstoregetdeveloperapps) | **GET** /v1/app-store/developers/{artist_id} | Get developer apps
[**appStoreListGenres**](AppStoreAPI.md#appstorelistgenres) | **GET** /v1/app-store/genres | List genres
[**appStoreListMarkets**](AppStoreAPI.md#appstorelistmarkets) | **GET** /v1/app-store/markets | List markets
[**appStoreSearchApps**](AppStoreAPI.md#appstoresearchapps) | **GET** /v1/app-store/search | Search apps
[**appStoreTopCharts**](AppStoreAPI.md#appstoretopcharts) | **GET** /v1/app-store/charts | Top charts


# **appStoreGetAppDetail**
```swift
    open class func appStoreGetAppDetail(appId: String, country: String? = nil, lang: String? = nil, includeExtras: Bool? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get app detail

App detail: bundle id, version, pricing, ratings, genres, min OS, size, languages, screenshots, in-app purchases and version history.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let appId = "appId_example" // String | Numeric trackId (e.g. '310633997') or bundle id (e.g. 'net.whatsapp.WhatsApp').
let country = "country_example" // String |  (optional) (default to "us")
let lang = "lang_example" // String | Result language, e.g. 'en_us' (optional)
let includeExtras = true // Bool | Fetch the storefront page for rating histogram, IAP list, full-res screenshots and App Privacy. Set false to skip the 2nd fetch. (optional) (default to true)

// Get app detail
AppStoreAPI.appStoreGetAppDetail(appId: appId, country: country, lang: lang, includeExtras: includeExtras) { (response, error) in
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
 **appId** | **String** | Numeric trackId (e.g. &#39;310633997&#39;) or bundle id (e.g. &#39;net.whatsapp.WhatsApp&#39;). | 
 **country** | **String** |  | [optional] [default to &quot;us&quot;]
 **lang** | **String** | Result language, e.g. &#39;en_us&#39; | [optional] 
 **includeExtras** | **Bool** | Fetch the storefront page for rating histogram, IAP list, full-res screenshots and App Privacy. Set false to skip the 2nd fetch. | [optional] [default to true]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **appStoreGetAppReviews**
```swift
    open class func appStoreGetAppReviews(appId: String, country: String? = nil, page: Int? = nil, sort: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get app reviews

Paginated customer reviews (50 per page, up to 10 pages).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let appId = "appId_example" // String | Numeric trackId, e.g. '310633997'
let country = "country_example" // String |  (optional) (default to "us")
let page = 987 // Int | Apple caps reviews at 10 pages (optional) (default to 1)
let sort = "sort_example" // String | mostRecent | mostHelpful (optional) (default to "mostRecent")

// Get app reviews
AppStoreAPI.appStoreGetAppReviews(appId: appId, country: country, page: page, sort: sort) { (response, error) in
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
 **appId** | **String** | Numeric trackId, e.g. &#39;310633997&#39; | 
 **country** | **String** |  | [optional] [default to &quot;us&quot;]
 **page** | **Int** | Apple caps reviews at 10 pages | [optional] [default to 1]
 **sort** | **String** | mostRecent | mostHelpful | [optional] [default to &quot;mostRecent&quot;]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **appStoreGetDeveloperApps**
```swift
    open class func appStoreGetDeveloperApps(artistId: String, country: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get developer apps

Developer info and their published apps.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let artistId = "artistId_example" // String | Numeric artistId (developer id)
let country = "country_example" // String |  (optional) (default to "us")

// Get developer apps
AppStoreAPI.appStoreGetDeveloperApps(artistId: artistId, country: country) { (response, error) in
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
 **artistId** | **String** | Numeric artistId (developer id) | 
 **country** | **String** |  | [optional] [default to &quot;us&quot;]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **appStoreListGenres**
```swift
    open class func appStoreListGenres(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

List genres

The Apple App Store genre/category ids.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// List genres
AppStoreAPI.appStoreListGenres() { (response, error) in
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

# **appStoreListMarkets**
```swift
    open class func appStoreListMarkets(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

List markets

Supported App Store country codes.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// List markets
AppStoreAPI.appStoreListMarkets() { (response, error) in
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

# **appStoreSearchApps**
```swift
    open class func appStoreSearchApps(query: String, country: String? = nil, entity: String? = nil, limit: Int? = nil, offset: Int? = nil, lang: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Search apps

Search the Apple App Store.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let query = "query_example" // String | Search term, e.g. 'chat'
let country = "country_example" // String | App Store country code (optional) (default to "us")
let entity = "entity_example" // String | software | iPadSoftware | macSoftware (optional) (default to "software")
let limit = 987 // Int |  (optional) (default to 25)
let offset = 987 // Int |  (optional) (default to 0)
let lang = "lang_example" // String | Language, e.g. 'en_us' (optional)

// Search apps
AppStoreAPI.appStoreSearchApps(query: query, country: country, entity: entity, limit: limit, offset: offset, lang: lang) { (response, error) in
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
 **query** | **String** | Search term, e.g. &#39;chat&#39; | 
 **country** | **String** | App Store country code | [optional] [default to &quot;us&quot;]
 **entity** | **String** | software | iPadSoftware | macSoftware | [optional] [default to &quot;software&quot;]
 **limit** | **Int** |  | [optional] [default to 25]
 **offset** | **Int** |  | [optional] [default to 0]
 **lang** | **String** | Language, e.g. &#39;en_us&#39; | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **appStoreTopCharts**
```swift
    open class func appStoreTopCharts(country: String? = nil, type: String? = nil, genre: Int? = nil, limit: Int? = nil, entity: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Top charts

Top charts, optionally scoped to a genre.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let country = "country_example" // String |  (optional) (default to "us")
let type = "type_example" // String | top-free | top-paid | top-grossing (optional) (default to "top-free")
let genre = 987 // Int | Apple genre id (optional), e.g. 6014 (optional)
let limit = 987 // Int |  (optional) (default to 50)
let entity = "entity_example" // String | apps (iPhone) | ipad (optional) (default to "apps")

// Top charts
AppStoreAPI.appStoreTopCharts(country: country, type: type, genre: genre, limit: limit, entity: entity) { (response, error) in
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
 **country** | **String** |  | [optional] [default to &quot;us&quot;]
 **type** | **String** | top-free | top-paid | top-grossing | [optional] [default to &quot;top-free&quot;]
 **genre** | **Int** | Apple genre id (optional), e.g. 6014 | [optional] 
 **limit** | **Int** |  | [optional] [default to 50]
 **entity** | **String** | apps (iPhone) | ipad | [optional] [default to &quot;apps&quot;]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

