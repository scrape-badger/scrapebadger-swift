# GooglePlayAPI

All URIs are relative to *https://scrapebadger.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**googlePlayBrowseACategory**](GooglePlayAPI.md#googleplaybrowseacategory) | **GET** /v1/google-play/categories/{category_id} | Browse a category
[**googlePlayGetAppDetail**](GooglePlayAPI.md#googleplaygetappdetail) | **GET** /v1/google-play/apps/{app_id} | Get app detail
[**googlePlayGetAppPermissions**](GooglePlayAPI.md#googleplaygetapppermissions) | **GET** /v1/google-play/apps/{app_id}/permissions | Get app permissions
[**googlePlayGetAppReviews**](GooglePlayAPI.md#googleplaygetappreviews) | **GET** /v1/google-play/apps/{app_id}/reviews | Get app reviews
[**googlePlayGetDeveloperApps**](GooglePlayAPI.md#googleplaygetdeveloperapps) | **GET** /v1/google-play/developers/{developer} | Get developer apps
[**googlePlayGetSimilarApps**](GooglePlayAPI.md#googleplaygetsimilarapps) | **GET** /v1/google-play/apps/{app_id}/similar | Get similar apps
[**googlePlayListCategories**](GooglePlayAPI.md#googleplaylistcategories) | **GET** /v1/google-play/categories | List categories
[**googlePlayListMarkets**](GooglePlayAPI.md#googleplaylistmarkets) | **GET** /v1/google-play/markets | List markets
[**googlePlaySearchApps**](GooglePlayAPI.md#googleplaysearchapps) | **GET** /v1/google-play/search | Search apps
[**googlePlayTopCharts**](GooglePlayAPI.md#googleplaytopcharts) | **GET** /v1/google-play/collections/{collection} | Top charts


# **googlePlayBrowseACategory**
```swift
    open class func googlePlayBrowseACategory(categoryId: String, country: String? = nil, lang: String? = nil, num: Int? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Browse a category

The top apps within a Play category.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let categoryId = "categoryId_example" // String | Play category id, e.g. 'GAME_PUZZLE' or 'SOCIAL'
let country = "country_example" // String | Play storefront country (gl), ISO 3166-1 alpha-2, e.g. 'US' (optional) (default to "US")
let lang = "lang_example" // String | Play content language (hl), e.g. 'en' or 'pt-BR' (optional) (default to "en")
let num = 987 // Int | Max apps; follows each rail's 'see more' continuation above the ~40-120 the page renders directly (optional) (default to 100)

// Browse a category
GooglePlayAPI.googlePlayBrowseACategory(categoryId: categoryId, country: country, lang: lang, num: num) { (response, error) in
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
 **categoryId** | **String** | Play category id, e.g. &#39;GAME_PUZZLE&#39; or &#39;SOCIAL&#39; | 
 **country** | **String** | Play storefront country (gl), ISO 3166-1 alpha-2, e.g. &#39;US&#39; | [optional] [default to &quot;US&quot;]
 **lang** | **String** | Play content language (hl), e.g. &#39;en&#39; or &#39;pt-BR&#39; | [optional] [default to &quot;en&quot;]
 **num** | **Int** | Max apps; follows each rail&#39;s &#39;see more&#39; continuation above the ~40-120 the page renders directly | [optional] [default to 100]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **googlePlayGetAppDetail**
```swift
    open class func googlePlayGetAppDetail(appId: String, country: String? = nil, lang: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get app detail

Full app detail: ratings histogram, installs, pricing, IAP, developer, screenshots, version metadata and what's-new.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let appId = "appId_example" // String | Android package id, e.g. 'com.whatsapp'.
let country = "country_example" // String | Play storefront country (gl), ISO 3166-1 alpha-2, e.g. 'US' (optional) (default to "US")
let lang = "lang_example" // String | Play content language (hl), e.g. 'en' or 'pt-BR' (optional) (default to "en")

// Get app detail
GooglePlayAPI.googlePlayGetAppDetail(appId: appId, country: country, lang: lang) { (response, error) in
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
 **appId** | **String** | Android package id, e.g. &#39;com.whatsapp&#39;. | 
 **country** | **String** | Play storefront country (gl), ISO 3166-1 alpha-2, e.g. &#39;US&#39; | [optional] [default to &quot;US&quot;]
 **lang** | **String** | Play content language (hl), e.g. &#39;en&#39; or &#39;pt-BR&#39; | [optional] [default to &quot;en&quot;]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **googlePlayGetAppPermissions**
```swift
    open class func googlePlayGetAppPermissions(appId: String, lang: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get app permissions

The app's requested Android permissions, grouped.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let appId = "appId_example" // String | Android package id, e.g. 'com.whatsapp'.
let lang = "lang_example" // String | Play content language (hl), e.g. 'en' or 'pt-BR' (optional) (default to "en")

// Get app permissions
GooglePlayAPI.googlePlayGetAppPermissions(appId: appId, lang: lang) { (response, error) in
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
 **appId** | **String** | Android package id, e.g. &#39;com.whatsapp&#39;. | 
 **lang** | **String** | Play content language (hl), e.g. &#39;en&#39; or &#39;pt-BR&#39; | [optional] [default to &quot;en&quot;]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **googlePlayGetAppReviews**
```swift
    open class func googlePlayGetAppReviews(appId: String, country: String? = nil, lang: String? = nil, sort: String? = nil, count: Int? = nil, pageToken: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get app reviews

Paginated app reviews via the Play batchexecute RPC.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let appId = "appId_example" // String | Android package id, e.g. 'com.whatsapp'.
let country = "country_example" // String | Play storefront country (gl), ISO 3166-1 alpha-2, e.g. 'US' (optional) (default to "US")
let lang = "lang_example" // String | Play content language (hl), e.g. 'en' or 'pt-BR' (optional) (default to "en")
let sort = "sort_example" // String | newest | rating | helpfulness (optional) (default to "newest")
let count = 987 // Int |  (optional) (default to 40)
let pageToken = "pageToken_example" // String | Pagination token (optional)

// Get app reviews
GooglePlayAPI.googlePlayGetAppReviews(appId: appId, country: country, lang: lang, sort: sort, count: count, pageToken: pageToken) { (response, error) in
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
 **appId** | **String** | Android package id, e.g. &#39;com.whatsapp&#39;. | 
 **country** | **String** | Play storefront country (gl), ISO 3166-1 alpha-2, e.g. &#39;US&#39; | [optional] [default to &quot;US&quot;]
 **lang** | **String** | Play content language (hl), e.g. &#39;en&#39; or &#39;pt-BR&#39; | [optional] [default to &quot;en&quot;]
 **sort** | **String** | newest | rating | helpfulness | [optional] [default to &quot;newest&quot;]
 **count** | **Int** |  | [optional] [default to 40]
 **pageToken** | **String** | Pagination token | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **googlePlayGetDeveloperApps**
```swift
    open class func googlePlayGetDeveloperApps(developer: String, country: String? = nil, lang: String? = nil, num: Int? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get developer apps

A developer's published apps.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let developer = "developer_example" // String | Developer name or numeric id
let country = "country_example" // String | Play storefront country (gl), ISO 3166-1 alpha-2, e.g. 'US' (optional) (default to "US")
let lang = "lang_example" // String | Play content language (hl), e.g. 'en' or 'pt-BR' (optional) (default to "en")
let num = 987 // Int | Max apps; follows rail continuations above the page's directly-rendered slice (optional) (default to 100)

// Get developer apps
GooglePlayAPI.googlePlayGetDeveloperApps(developer: developer, country: country, lang: lang, num: num) { (response, error) in
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
 **developer** | **String** | Developer name or numeric id | 
 **country** | **String** | Play storefront country (gl), ISO 3166-1 alpha-2, e.g. &#39;US&#39; | [optional] [default to &quot;US&quot;]
 **lang** | **String** | Play content language (hl), e.g. &#39;en&#39; or &#39;pt-BR&#39; | [optional] [default to &quot;en&quot;]
 **num** | **Int** | Max apps; follows rail continuations above the page&#39;s directly-rendered slice | [optional] [default to 100]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **googlePlayGetSimilarApps**
```swift
    open class func googlePlayGetSimilarApps(appId: String, country: String? = nil, lang: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get similar apps

Apps Google Play lists as similar to this one.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let appId = "appId_example" // String | Android package id, e.g. 'com.whatsapp'.
let country = "country_example" // String | Play storefront country (gl), ISO 3166-1 alpha-2, e.g. 'US' (optional) (default to "US")
let lang = "lang_example" // String | Play content language (hl), e.g. 'en' or 'pt-BR' (optional) (default to "en")

// Get similar apps
GooglePlayAPI.googlePlayGetSimilarApps(appId: appId, country: country, lang: lang) { (response, error) in
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
 **appId** | **String** | Android package id, e.g. &#39;com.whatsapp&#39;. | 
 **country** | **String** | Play storefront country (gl), ISO 3166-1 alpha-2, e.g. &#39;US&#39; | [optional] [default to &quot;US&quot;]
 **lang** | **String** | Play content language (hl), e.g. &#39;en&#39; or &#39;pt-BR&#39; | [optional] [default to &quot;en&quot;]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **googlePlayListCategories**
```swift
    open class func googlePlayListCategories(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

List categories

The Google Play app/game category ids.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// List categories
GooglePlayAPI.googlePlayListCategories() { (response, error) in
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

# **googlePlayListMarkets**
```swift
    open class func googlePlayListMarkets(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

List markets

Supported Google Play store countries and languages.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// List markets
GooglePlayAPI.googlePlayListMarkets() { (response, error) in
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

# **googlePlaySearchApps**
```swift
    open class func googlePlaySearchApps(query: String, country: String? = nil, lang: String? = nil, price: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Search apps

Search Google Play for apps and games (the ~30 server-rendered results; Play exposes no page parameter).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let query = "query_example" // String | Search keywords, e.g. 'puzzle'
let country = "country_example" // String | Play storefront country (gl), ISO 3166-1 alpha-2, e.g. 'US' (optional) (default to "US")
let lang = "lang_example" // String | Play content language (hl), e.g. 'en' or 'pt-BR' (optional) (default to "en")
let price = "price_example" // String | free | paid | all (optional)

// Search apps
GooglePlayAPI.googlePlaySearchApps(query: query, country: country, lang: lang, price: price) { (response, error) in
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
 **query** | **String** | Search keywords, e.g. &#39;puzzle&#39; | 
 **country** | **String** | Play storefront country (gl), ISO 3166-1 alpha-2, e.g. &#39;US&#39; | [optional] [default to &quot;US&quot;]
 **lang** | **String** | Play content language (hl), e.g. &#39;en&#39; or &#39;pt-BR&#39; | [optional] [default to &quot;en&quot;]
 **price** | **String** | free | paid | all | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **googlePlayTopCharts**
```swift
    open class func googlePlayTopCharts(collection: String, category: String? = nil, country: String? = nil, lang: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Top charts

Top charts for a collection, optionally scoped to a category.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let collection = "collection_example" // String | topselling_free | topselling_paid | topgrossing
let category = "category_example" // String | Play category, e.g. 'GAME' (optional) (default to "APPLICATION")
let country = "country_example" // String | Play storefront country (gl), ISO 3166-1 alpha-2, e.g. 'US' (optional) (default to "US")
let lang = "lang_example" // String | Play content language (hl), e.g. 'en' or 'pt-BR' (optional) (default to "en")

// Top charts
GooglePlayAPI.googlePlayTopCharts(collection: collection, category: category, country: country, lang: lang) { (response, error) in
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
 **collection** | **String** | topselling_free | topselling_paid | topgrossing | 
 **category** | **String** | Play category, e.g. &#39;GAME&#39; | [optional] [default to &quot;APPLICATION&quot;]
 **country** | **String** | Play storefront country (gl), ISO 3166-1 alpha-2, e.g. &#39;US&#39; | [optional] [default to &quot;US&quot;]
 **lang** | **String** | Play content language (hl), e.g. &#39;en&#39; or &#39;pt-BR&#39; | [optional] [default to &quot;en&quot;]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

