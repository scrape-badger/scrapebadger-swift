# BraveAPI

All URIs are relative to *https://scrapebadger.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**braveAutocomplete**](BraveAPI.md#braveautocomplete) | **GET** /v1/brave/autocomplete | Autocomplete
[**braveImageSearch**](BraveAPI.md#braveimagesearch) | **GET** /v1/brave/images | Image search
[**braveListSupportedLocales**](BraveAPI.md#bravelistsupportedlocales) | **GET** /v1/brave/locales | List supported locales
[**braveNewsSearch**](BraveAPI.md#bravenewssearch) | **GET** /v1/brave/news | News search
[**braveVideoSearch**](BraveAPI.md#bravevideosearch) | **GET** /v1/brave/videos | Video search
[**braveWebSearch**](BraveAPI.md#bravewebsearch) | **GET** /v1/brave/search | Web search


# **braveAutocomplete**
```swift
    open class func braveAutocomplete(query: String, country: Country_braveAutocomplete? = nil, completion: @escaping (_ data: BraveAutocompleteResponse?, _ error: Error?) -> Void)
```

Autocomplete

Native search-box suggestions with entity descriptions and images. Two credits.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let query = "query_example" // String | 
let country = "country_example" // String |  (optional) (default to .us)

// Autocomplete
BraveAPI.braveAutocomplete(query: query, country: country) { (response, error) in
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
 **query** | **String** |  | 
 **country** | **String** |  | [optional] [default to .us]

### Return type

[**BraveAutocompleteResponse**](BraveAutocompleteResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **braveImageSearch**
```swift
    open class func braveImageSearch(query: String, country: Country_braveImageSearch? = nil, uiLanguage: UiLanguage_braveImageSearch? = nil, safeSearch: SafeSearch_braveImageSearch? = nil, count: Int? = nil, completion: @escaping (_ data: BraveResponse?, _ error: Error?) -> Void)
```

Image search

Native image batch with original URLs, source pages, thumbnails and dimensions.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let query = "query_example" // String | Native Brave search query
let country = "country_example" // String | Native result region; see /locales (optional) (default to .us)
let uiLanguage = "uiLanguage_example" // String | UI labels/date language; does not restrict result language (optional) (default to .enUs)
let safeSearch = "safeSearch_example" // String |  (optional) (default to .moderate)
let count = 987 // Int | Slice the initial native image batch (optional) (default to 50)

// Image search
BraveAPI.braveImageSearch(query: query, country: country, uiLanguage: uiLanguage, safeSearch: safeSearch, count: count) { (response, error) in
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
 **query** | **String** | Native Brave search query | 
 **country** | **String** | Native result region; see /locales | [optional] [default to .us]
 **uiLanguage** | **String** | UI labels/date language; does not restrict result language | [optional] [default to .enUs]
 **safeSearch** | **String** |  | [optional] [default to .moderate]
 **count** | **Int** | Slice the initial native image batch | [optional] [default to 50]

### Return type

[**BraveResponse**](BraveResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **braveListSupportedLocales**
```swift
    open class func braveListSupportedLocales(completion: @escaping (_ data: BraveLocalesResponse?, _ error: Error?) -> Void)
```

List supported locales

Native country and UI-language choices. Free; result language is a separate preference.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// List supported locales
BraveAPI.braveListSupportedLocales() { (response, error) in
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

[**BraveLocalesResponse**](BraveLocalesResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **braveNewsSearch**
```swift
    open class func braveNewsSearch(query: String, country: Country_braveNewsSearch? = nil, uiLanguage: UiLanguage_braveNewsSearch? = nil, safeSearch: SafeSearch_braveNewsSearch? = nil, count: Int? = nil, completion: @escaping (_ data: BraveResponse?, _ error: Error?) -> Void)
```

News search

Native news batch; relative source dates stay display strings.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let query = "query_example" // String | Native Brave search query
let country = "country_example" // String | Native result region; see /locales (optional) (default to .us)
let uiLanguage = "uiLanguage_example" // String | UI labels/date language; does not restrict result language (optional) (default to .enUs)
let safeSearch = "safeSearch_example" // String |  (optional) (default to .moderate)
let count = 987 // Int | Slice the initial native news batch (optional) (default to 35)

// News search
BraveAPI.braveNewsSearch(query: query, country: country, uiLanguage: uiLanguage, safeSearch: safeSearch, count: count) { (response, error) in
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
 **query** | **String** | Native Brave search query | 
 **country** | **String** | Native result region; see /locales | [optional] [default to .us]
 **uiLanguage** | **String** | UI labels/date language; does not restrict result language | [optional] [default to .enUs]
 **safeSearch** | **String** |  | [optional] [default to .moderate]
 **count** | **Int** | Slice the initial native news batch | [optional] [default to 35]

### Return type

[**BraveResponse**](BraveResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **braveVideoSearch**
```swift
    open class func braveVideoSearch(query: String, country: Country_braveVideoSearch? = nil, uiLanguage: UiLanguage_braveVideoSearch? = nil, safeSearch: SafeSearch_braveVideoSearch? = nil, page: Int? = nil, count: Int? = nil, completion: @escaping (_ data: BravePagedResponse?, _ error: Error?) -> Void)
```

Video search

Native video results with duration, creator, publisher and verified page ordinals.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let query = "query_example" // String | Native Brave search query
let country = "country_example" // String | Native result region; see /locales (optional) (default to .us)
let uiLanguage = "uiLanguage_example" // String | UI labels/date language; does not restrict result language (optional) (default to .enUs)
let safeSearch = "safeSearch_example" // String |  (optional) (default to .moderate)
let page = 987 // Int | 1-based native page ordinal (optional) (default to 1)
let count = 987 // Int |  (optional) (default to 50)

// Video search
BraveAPI.braveVideoSearch(query: query, country: country, uiLanguage: uiLanguage, safeSearch: safeSearch, page: page, count: count) { (response, error) in
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
 **query** | **String** | Native Brave search query | 
 **country** | **String** | Native result region; see /locales | [optional] [default to .us]
 **uiLanguage** | **String** | UI labels/date language; does not restrict result language | [optional] [default to .enUs]
 **safeSearch** | **String** |  | [optional] [default to .moderate]
 **page** | **Int** | 1-based native page ordinal | [optional] [default to 1]
 **count** | **Int** |  | [optional] [default to 50]

### Return type

[**BravePagedResponse**](BravePagedResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **braveWebSearch**
```swift
    open class func braveWebSearch(query: String, country: Country_braveWebSearch? = nil, uiLanguage: UiLanguage_braveWebSearch? = nil, safeSearch: SafeSearch_braveWebSearch? = nil, page: Int? = nil, count: Int? = nil, freshness: Freshness_braveWebSearch? = nil, spellcheck: Bool? = nil, completion: @escaping (_ data: BraveSearchResponse?, _ error: Error?) -> Void)
```

Web search

Native Brave organic results, rich source blocks and page metadata. Seven credits.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let query = "query_example" // String | Native Brave search query
let country = "country_example" // String | Native result region; see /locales (optional) (default to .us)
let uiLanguage = "uiLanguage_example" // String | UI labels/date language; does not restrict result language (optional) (default to .enUs)
let safeSearch = "safeSearch_example" // String |  (optional) (default to .moderate)
let page = 987 // Int | 1-based native page ordinal (optional) (default to 1)
let count = 987 // Int | Slice one native page; does not change native page boundaries (optional) (default to 20)
let freshness = "freshness_example" // String |  (optional) (default to .any)
let spellcheck = true // Bool | Allow native spelling correction (optional) (default to false)

// Web search
BraveAPI.braveWebSearch(query: query, country: country, uiLanguage: uiLanguage, safeSearch: safeSearch, page: page, count: count, freshness: freshness, spellcheck: spellcheck) { (response, error) in
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
 **query** | **String** | Native Brave search query | 
 **country** | **String** | Native result region; see /locales | [optional] [default to .us]
 **uiLanguage** | **String** | UI labels/date language; does not restrict result language | [optional] [default to .enUs]
 **safeSearch** | **String** |  | [optional] [default to .moderate]
 **page** | **Int** | 1-based native page ordinal | [optional] [default to 1]
 **count** | **Int** | Slice one native page; does not change native page boundaries | [optional] [default to 20]
 **freshness** | **String** |  | [optional] [default to .any]
 **spellcheck** | **Bool** | Allow native spelling correction | [optional] [default to false]

### Return type

[**BraveSearchResponse**](BraveSearchResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

