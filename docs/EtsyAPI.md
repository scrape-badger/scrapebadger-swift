# EtsyAPI

All URIs are relative to *https://scrapebadger.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**etsyGetCategories**](EtsyAPI.md#etsygetcategories) | **GET** /v1/etsy/categories | Get categories
[**etsyGetListingDetail**](EtsyAPI.md#etsygetlistingdetail) | **GET** /v1/etsy/listings/{listing_id} | Get listing detail
[**etsyGetListingReviews**](EtsyAPI.md#etsygetlistingreviews) | **GET** /v1/etsy/listings/{listing_id}/reviews | Get listing reviews
[**etsyGetSearchSuggestions**](EtsyAPI.md#etsygetsearchsuggestions) | **GET** /v1/etsy/autocomplete | Get search suggestions
[**etsyGetShopListings**](EtsyAPI.md#etsygetshoplistings) | **GET** /v1/etsy/shops/{shop_name}/listings | Get shop listings
[**etsyGetShopProfile**](EtsyAPI.md#etsygetshopprofile) | **GET** /v1/etsy/shops/{shop_name} | Get shop profile
[**etsyGetShopReviews**](EtsyAPI.md#etsygetshopreviews) | **GET** /v1/etsy/shops/{shop_name}/reviews | Get shop reviews
[**etsySearchListings**](EtsyAPI.md#etsysearchlistings) | **GET** /v1/etsy/search | Search listings


# **etsyGetCategories**
```swift
    open class func etsyGetCategories(country: String? = nil, currency: String? = nil, language: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get categories

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let country = "country_example" // String |  (optional) (default to "US")
let currency = "currency_example" // String |  (optional) (default to "USD")
let language = "language_example" // String |  (optional) (default to "en-US")

// Get categories
EtsyAPI.etsyGetCategories(country: country, currency: currency, language: language) { (response, error) in
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
 **country** | **String** |  | [optional] [default to &quot;US&quot;]
 **currency** | **String** |  | [optional] [default to &quot;USD&quot;]
 **language** | **String** |  | [optional] [default to &quot;en-US&quot;]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **etsyGetListingDetail**
```swift
    open class func etsyGetListingDetail(listingId: String, country: String? = nil, currency: String? = nil, language: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get listing detail

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let listingId = "listingId_example" // String | 
let country = "country_example" // String |  (optional) (default to "US")
let currency = "currency_example" // String |  (optional) (default to "USD")
let language = "language_example" // String |  (optional) (default to "en-US")

// Get listing detail
EtsyAPI.etsyGetListingDetail(listingId: listingId, country: country, currency: currency, language: language) { (response, error) in
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
 **listingId** | **String** |  | 
 **country** | **String** |  | [optional] [default to &quot;US&quot;]
 **currency** | **String** |  | [optional] [default to &quot;USD&quot;]
 **language** | **String** |  | [optional] [default to &quot;en-US&quot;]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **etsyGetListingReviews**
```swift
    open class func etsyGetListingReviews(listingId: String, page: Int? = nil, sort: Sort_etsyGetListingReviews? = nil, country: String? = nil, currency: String? = nil, language: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get listing reviews

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let listingId = "listingId_example" // String | 
let page = 987 // Int |  (optional) (default to 1)
let sort = "sort_example" // String |  (optional) (default to .relevancy)
let country = "country_example" // String |  (optional) (default to "US")
let currency = "currency_example" // String |  (optional) (default to "USD")
let language = "language_example" // String |  (optional) (default to "en-US")

// Get listing reviews
EtsyAPI.etsyGetListingReviews(listingId: listingId, page: page, sort: sort, country: country, currency: currency, language: language) { (response, error) in
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
 **listingId** | **String** |  | 
 **page** | **Int** |  | [optional] [default to 1]
 **sort** | **String** |  | [optional] [default to .relevancy]
 **country** | **String** |  | [optional] [default to &quot;US&quot;]
 **currency** | **String** |  | [optional] [default to &quot;USD&quot;]
 **language** | **String** |  | [optional] [default to &quot;en-US&quot;]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **etsyGetSearchSuggestions**
```swift
    open class func etsyGetSearchSuggestions(query: String, country: String? = nil, currency: String? = nil, language: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get search suggestions

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let query = "query_example" // String | 
let country = "country_example" // String |  (optional) (default to "US")
let currency = "currency_example" // String |  (optional) (default to "USD")
let language = "language_example" // String |  (optional) (default to "en-US")

// Get search suggestions
EtsyAPI.etsyGetSearchSuggestions(query: query, country: country, currency: currency, language: language) { (response, error) in
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
 **country** | **String** |  | [optional] [default to &quot;US&quot;]
 **currency** | **String** |  | [optional] [default to &quot;USD&quot;]
 **language** | **String** |  | [optional] [default to &quot;en-US&quot;]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **etsyGetShopListings**
```swift
    open class func etsyGetShopListings(shopName: String, page: Int? = nil, country: String? = nil, currency: String? = nil, language: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get shop listings

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let shopName = "shopName_example" // String | 
let page = 987 // Int |  (optional) (default to 1)
let country = "country_example" // String |  (optional) (default to "US")
let currency = "currency_example" // String |  (optional) (default to "USD")
let language = "language_example" // String |  (optional) (default to "en-US")

// Get shop listings
EtsyAPI.etsyGetShopListings(shopName: shopName, page: page, country: country, currency: currency, language: language) { (response, error) in
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
 **shopName** | **String** |  | 
 **page** | **Int** |  | [optional] [default to 1]
 **country** | **String** |  | [optional] [default to &quot;US&quot;]
 **currency** | **String** |  | [optional] [default to &quot;USD&quot;]
 **language** | **String** |  | [optional] [default to &quot;en-US&quot;]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **etsyGetShopProfile**
```swift
    open class func etsyGetShopProfile(shopName: String, country: String? = nil, currency: String? = nil, language: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get shop profile

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let shopName = "shopName_example" // String | 
let country = "country_example" // String |  (optional) (default to "US")
let currency = "currency_example" // String |  (optional) (default to "USD")
let language = "language_example" // String |  (optional) (default to "en-US")

// Get shop profile
EtsyAPI.etsyGetShopProfile(shopName: shopName, country: country, currency: currency, language: language) { (response, error) in
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
 **shopName** | **String** |  | 
 **country** | **String** |  | [optional] [default to &quot;US&quot;]
 **currency** | **String** |  | [optional] [default to &quot;USD&quot;]
 **language** | **String** |  | [optional] [default to &quot;en-US&quot;]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **etsyGetShopReviews**
```swift
    open class func etsyGetShopReviews(shopName: String, page: Int? = nil, country: String? = nil, currency: String? = nil, language: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get shop reviews

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let shopName = "shopName_example" // String | 
let page = 987 // Int |  (optional) (default to 1)
let country = "country_example" // String |  (optional) (default to "US")
let currency = "currency_example" // String |  (optional) (default to "USD")
let language = "language_example" // String |  (optional) (default to "en-US")

// Get shop reviews
EtsyAPI.etsyGetShopReviews(shopName: shopName, page: page, country: country, currency: currency, language: language) { (response, error) in
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
 **shopName** | **String** |  | 
 **page** | **Int** |  | [optional] [default to 1]
 **country** | **String** |  | [optional] [default to &quot;US&quot;]
 **currency** | **String** |  | [optional] [default to &quot;USD&quot;]
 **language** | **String** |  | [optional] [default to &quot;en-US&quot;]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **etsySearchListings**
```swift
    open class func etsySearchListings(query: String, page: Int? = nil, country: String? = nil, currency: String? = nil, language: String? = nil, sort: Sort_etsySearchListings? = nil, minPrice: Double? = nil, maxPrice: Double? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Search listings

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let query = "query_example" // String | 
let page = 987 // Int |  (optional) (default to 1)
let country = "country_example" // String |  (optional) (default to "US")
let currency = "currency_example" // String |  (optional) (default to "USD")
let language = "language_example" // String |  (optional) (default to "en-US")
let sort = "sort_example" // String |  (optional) (default to .mostRelevant)
let minPrice = 987 // Double |  (optional)
let maxPrice = 987 // Double |  (optional)

// Search listings
EtsyAPI.etsySearchListings(query: query, page: page, country: country, currency: currency, language: language, sort: sort, minPrice: minPrice, maxPrice: maxPrice) { (response, error) in
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
 **page** | **Int** |  | [optional] [default to 1]
 **country** | **String** |  | [optional] [default to &quot;US&quot;]
 **currency** | **String** |  | [optional] [default to &quot;USD&quot;]
 **language** | **String** |  | [optional] [default to &quot;en-US&quot;]
 **sort** | **String** |  | [optional] [default to .mostRelevant]
 **minPrice** | **Double** |  | [optional] 
 **maxPrice** | **Double** |  | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

