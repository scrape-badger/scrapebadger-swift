# WallapopAPI

All URIs are relative to *https://scrapebadger.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**wallapopAutocomplete**](WallapopAPI.md#wallapopautocomplete) | **GET** /v1/wallapop/autocomplete | Autocomplete
[**wallapopGetListingDetail**](WallapopAPI.md#wallapopgetlistingdetail) | **GET** /v1/wallapop/items/{item_id} | Get listing detail
[**wallapopGetUserListings**](WallapopAPI.md#wallapopgetuserlistings) | **GET** /v1/wallapop/users/{user_id}/items | Get user listings
[**wallapopGetUserProfile**](WallapopAPI.md#wallapopgetuserprofile) | **GET** /v1/wallapop/users/{user_id} | Get user profile
[**wallapopGetUserReviews**](WallapopAPI.md#wallapopgetuserreviews) | **GET** /v1/wallapop/users/{user_id}/reviews | Get user reviews
[**wallapopListCategories**](WallapopAPI.md#wallapoplistcategories) | **GET** /v1/wallapop/categories | List categories
[**wallapopListFilterOptions**](WallapopAPI.md#wallapoplistfilteroptions) | **GET** /v1/wallapop/filters/{filter_id}/options | List filter options
[**wallapopListMarkets**](WallapopAPI.md#wallapoplistmarkets) | **GET** /v1/wallapop/markets | List markets
[**wallapopListSearchFilters**](WallapopAPI.md#wallapoplistsearchfilters) | **GET** /v1/wallapop/filters | List search filters
[**wallapopSearchListings**](WallapopAPI.md#wallapopsearchlistings) | **GET** /v1/wallapop/search | Search listings
[**wallapopWallapopScraperHealthCheck**](WallapopAPI.md#wallapopwallapopscraperhealthcheck) | **GET** /v1/wallapop/health | Wallapop scraper health check
[**wallapopWallapopScraperHealthCheckHead**](WallapopAPI.md#wallapopwallapopscraperhealthcheckhead) | **HEAD** /v1/wallapop/health | Wallapop scraper health check


# **wallapopAutocomplete**
```swift
    open class func wallapopAutocomplete(query: String, market: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Autocomplete

Wallapop's search-box suggestions for a partial query.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let query = "query_example" // String | Partial search text, e.g. 'bici'
let market = "market_example" // String | Market: es (Spain), it (Italy), pt (Portugal) (optional) (default to "es")

// Autocomplete
WallapopAPI.wallapopAutocomplete(query: query, market: market) { (response, error) in
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
 **query** | **String** | Partial search text, e.g. &#39;bici&#39; | 
 **market** | **String** | Market: es (Spain), it (Italy), pt (Portugal) | [optional] [default to &quot;es&quot;]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **wallapopGetListingDetail**
```swift
    open class func wallapopGetListingDetail(itemId: String, market: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get listing detail

Full listing detail by id (e.g. nzxeknm5x562) or listing slug.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let itemId = "itemId_example" // String | 
let market = "market_example" // String | Market: es (Spain), it (Italy), pt (Portugal) (optional) (default to "es")

// Get listing detail
WallapopAPI.wallapopGetListingDetail(itemId: itemId, market: market) { (response, error) in
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
 **itemId** | **String** |  | 
 **market** | **String** | Market: es (Spain), it (Italy), pt (Portugal) | [optional] [default to &quot;es&quot;]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **wallapopGetUserListings**
```swift
    open class func wallapopGetUserListings(userId: String, market: String? = nil, nextPage: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get user listings

A seller's live listings, 40 per page.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let userId = "userId_example" // String | 
let market = "market_example" // String | Market: es (Spain), it (Italy), pt (Portugal) (optional) (default to "es")
let nextPage = "nextPage_example" // String | Cursor from the previous page's next_page (optional)

// Get user listings
WallapopAPI.wallapopGetUserListings(userId: userId, market: market, nextPage: nextPage) { (response, error) in
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
 **userId** | **String** |  | 
 **market** | **String** | Market: es (Spain), it (Italy), pt (Portugal) | [optional] [default to &quot;es&quot;]
 **nextPage** | **String** | Cursor from the previous page&#39;s next_page | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **wallapopGetUserProfile**
```swift
    open class func wallapopGetUserProfile(userId: String, market: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get user profile

Seller profile with ratings, sales counters, response rate and verifications.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let userId = "userId_example" // String | 
let market = "market_example" // String | Market: es (Spain), it (Italy), pt (Portugal) (optional) (default to "es")

// Get user profile
WallapopAPI.wallapopGetUserProfile(userId: userId, market: market) { (response, error) in
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
 **userId** | **String** |  | 
 **market** | **String** | Market: es (Spain), it (Italy), pt (Portugal) | [optional] [default to &quot;es&quot;]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **wallapopGetUserReviews**
```swift
    open class func wallapopGetUserReviews(userId: String, market: String? = nil, nextPage: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get user reviews

Reviews a seller received, newest first, 40 per page.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let userId = "userId_example" // String | 
let market = "market_example" // String | Market: es (Spain), it (Italy), pt (Portugal) (optional) (default to "es")
let nextPage = "nextPage_example" // String | Cursor from the previous page's next_page (optional)

// Get user reviews
WallapopAPI.wallapopGetUserReviews(userId: userId, market: market, nextPage: nextPage) { (response, error) in
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
 **userId** | **String** |  | 
 **market** | **String** | Market: es (Spain), it (Italy), pt (Portugal) | [optional] [default to &quot;es&quot;]
 **nextPage** | **String** | Cursor from the previous page&#39;s next_page | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **wallapopListCategories**
```swift
    open class func wallapopListCategories(market: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

List categories

The full category tree; ids are usable as the search category_id.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let market = "market_example" // String | Market: es (Spain), it (Italy), pt (Portugal) (optional) (default to "es")

// List categories
WallapopAPI.wallapopListCategories(market: market) { (response, error) in
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
 **market** | **String** | Market: es (Spain), it (Italy), pt (Portugal) | [optional] [default to &quot;es&quot;]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **wallapopListFilterOptions**
```swift
    open class func wallapopListFilterOptions(filterId: String, categoryId: Int? = nil, query: String? = nil, market: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

List filter options

Long option lists (e.g. brand, model) for filters flagged options_endpoint.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let filterId = "filterId_example" // String | 
let categoryId = 987 // Int | Category to scope options to (optional)
let query = "query_example" // String | Search text to scope options to (optional)
let market = "market_example" // String | Market: es (Spain), it (Italy), pt (Portugal) (optional) (default to "es")

// List filter options
WallapopAPI.wallapopListFilterOptions(filterId: filterId, categoryId: categoryId, query: query, market: market) { (response, error) in
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
 **filterId** | **String** |  | 
 **categoryId** | **Int** | Category to scope options to | [optional] 
 **query** | **String** | Search text to scope options to | [optional] 
 **market** | **String** | Market: es (Spain), it (Italy), pt (Portugal) | [optional] [default to &quot;es&quot;]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **wallapopListMarkets**
```swift
    open class func wallapopListMarkets(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

List markets

Supported Wallapop markets and their default search location.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// List markets
WallapopAPI.wallapopListMarkets() { (response, error) in
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

# **wallapopListSearchFilters**
```swift
    open class func wallapopListSearchFilters(categoryId: Int? = nil, query: String? = nil, market: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

List search filters

The filters Wallapop offers for a category or query, with option ids.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let categoryId = 987 // Int | Category the filters apply to (optional)
let query = "query_example" // String | Search text the filters apply to (optional)
let market = "market_example" // String | Market: es (Spain), it (Italy), pt (Portugal) (optional) (default to "es")

// List search filters
WallapopAPI.wallapopListSearchFilters(categoryId: categoryId, query: query, market: market) { (response, error) in
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
 **categoryId** | **Int** | Category the filters apply to | [optional] 
 **query** | **String** | Search text the filters apply to | [optional] 
 **market** | **String** | Market: es (Spain), it (Italy), pt (Portugal) | [optional] [default to &quot;es&quot;]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **wallapopSearchListings**
```swift
    open class func wallapopSearchListings(query: String? = nil, market: String? = nil, latitude: Double? = nil, longitude: Double? = nil, distanceKm: Int? = nil, categoryId: Int? = nil, minPrice: Double? = nil, maxPrice: Double? = nil, condition: String? = nil, brand: String? = nil, model: String? = nil, color: String? = nil, timeFilter: TimeFilter_wallapopSearchListings? = nil, shippable: Bool? = nil, hasWarranty: Bool? = nil, refurbished: Bool? = nil, minYear: Int? = nil, maxYear: Int? = nil, minKm: Int? = nil, maxKm: Int? = nil, gearbox: Gearbox_wallapopSearchListings? = nil, minHorsepower: Int? = nil, maxHorsepower: Int? = nil, orderBy: OrderBy_wallapopSearchListings? = nil, nextPage: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Search listings

Search Wallapop listings (40 per page). Needs a query, a category_id, or both.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let query = "query_example" // String | Search text, e.g. 'iphone 14' (optional)
let market = "market_example" // String | Market: es (Spain), it (Italy), pt (Portugal) (optional) (default to "es")
let latitude = 987 // Double | Search centre latitude (defaults to the market capital) (optional)
let longitude = 987 // Double | Search centre longitude (optional)
let distanceKm = 987 // Int | Search radius (optional)
let categoryId = 987 // Int | Category id from /categories (optional)
let minPrice = 987 // Double | Minimum price (EUR) (optional)
let maxPrice = 987 // Double | Maximum price (EUR) (optional)
let condition = "condition_example" // String | Comma-separated: un_opened, in_box, new, as_good_as_new, good, fair, has_given_it_all (optional)
let brand = "brand_example" // String | Brand, e.g. Apple (optional)
let model = "model_example" // String | Model, e.g. iPhone 14 (optional)
let color = "color_example" // String | Colour id, e.g. black (optional)
let timeFilter = "timeFilter_example" // String | Only listings published within this window (optional)
let shippable = true // Bool | Only listings that ship (optional) (default to false)
let hasWarranty = true // Bool | Only listings with a warranty (optional) (default to false)
let refurbished = true // Bool | Only refurbished listings (optional) (default to false)
let minYear = 987 // Int | Cars: earliest model year (optional)
let maxYear = 987 // Int | Cars: latest model year (optional)
let minKm = 987 // Int | Cars: minimum mileage (optional)
let maxKm = 987 // Int | Cars: maximum mileage (optional)
let gearbox = "gearbox_example" // String | Cars (optional)
let minHorsepower = 987 // Int | Cars: minimum power (optional)
let maxHorsepower = 987 // Int | Cars: maximum power (optional)
let orderBy = "orderBy_example" // String | Sort order (optional) (default to .mostRelevance)
let nextPage = "nextPage_example" // String | Cursor from the previous page's next_page; other parameters are then ignored (optional)

// Search listings
WallapopAPI.wallapopSearchListings(query: query, market: market, latitude: latitude, longitude: longitude, distanceKm: distanceKm, categoryId: categoryId, minPrice: minPrice, maxPrice: maxPrice, condition: condition, brand: brand, model: model, color: color, timeFilter: timeFilter, shippable: shippable, hasWarranty: hasWarranty, refurbished: refurbished, minYear: minYear, maxYear: maxYear, minKm: minKm, maxKm: maxKm, gearbox: gearbox, minHorsepower: minHorsepower, maxHorsepower: maxHorsepower, orderBy: orderBy, nextPage: nextPage) { (response, error) in
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
 **query** | **String** | Search text, e.g. &#39;iphone 14&#39; | [optional] 
 **market** | **String** | Market: es (Spain), it (Italy), pt (Portugal) | [optional] [default to &quot;es&quot;]
 **latitude** | **Double** | Search centre latitude (defaults to the market capital) | [optional] 
 **longitude** | **Double** | Search centre longitude | [optional] 
 **distanceKm** | **Int** | Search radius | [optional] 
 **categoryId** | **Int** | Category id from /categories | [optional] 
 **minPrice** | **Double** | Minimum price (EUR) | [optional] 
 **maxPrice** | **Double** | Maximum price (EUR) | [optional] 
 **condition** | **String** | Comma-separated: un_opened, in_box, new, as_good_as_new, good, fair, has_given_it_all | [optional] 
 **brand** | **String** | Brand, e.g. Apple | [optional] 
 **model** | **String** | Model, e.g. iPhone 14 | [optional] 
 **color** | **String** | Colour id, e.g. black | [optional] 
 **timeFilter** | **String** | Only listings published within this window | [optional] 
 **shippable** | **Bool** | Only listings that ship | [optional] [default to false]
 **hasWarranty** | **Bool** | Only listings with a warranty | [optional] [default to false]
 **refurbished** | **Bool** | Only refurbished listings | [optional] [default to false]
 **minYear** | **Int** | Cars: earliest model year | [optional] 
 **maxYear** | **Int** | Cars: latest model year | [optional] 
 **minKm** | **Int** | Cars: minimum mileage | [optional] 
 **maxKm** | **Int** | Cars: maximum mileage | [optional] 
 **gearbox** | **String** | Cars | [optional] 
 **minHorsepower** | **Int** | Cars: minimum power | [optional] 
 **maxHorsepower** | **Int** | Cars: maximum power | [optional] 
 **orderBy** | **String** | Sort order | [optional] [default to .mostRelevance]
 **nextPage** | **String** | Cursor from the previous page&#39;s next_page; other parameters are then ignored | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **wallapopWallapopScraperHealthCheck**
```swift
    open class func wallapopWallapopScraperHealthCheck(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Wallapop scraper health check

Check health of the Wallapop scraper service (accepts HEAD).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// Wallapop scraper health check
WallapopAPI.wallapopWallapopScraperHealthCheck() { (response, error) in
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

# **wallapopWallapopScraperHealthCheckHead**
```swift
    open class func wallapopWallapopScraperHealthCheckHead(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Wallapop scraper health check

Check health of the Wallapop scraper service (accepts HEAD).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// Wallapop scraper health check
WallapopAPI.wallapopWallapopScraperHealthCheckHead() { (response, error) in
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

