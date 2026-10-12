# GumtreeAPI

All URIs are relative to *https://scrapebadger.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**gumtreeGetListing**](GumtreeAPI.md#gumtreegetlisting) | **GET** /v1/gumtree/listings/{listing_id} | Get listing
[**gumtreeGetSearchFilters**](GumtreeAPI.md#gumtreegetsearchfilters) | **GET** /v1/gumtree/search/filters | Get search filters
[**gumtreeGetSellerListings**](GumtreeAPI.md#gumtreegetsellerlistings) | **GET** /v1/gumtree/listings/{listing_id}/seller-listings | Get seller listings
[**gumtreeGumtreeScraperHealthCheck**](GumtreeAPI.md#gumtreegumtreescraperhealthcheck) | **GET** /v1/gumtree/health | Gumtree scraper health check
[**gumtreeGumtreeScraperHealthCheckHead**](GumtreeAPI.md#gumtreegumtreescraperhealthcheckhead) | **HEAD** /v1/gumtree/health | Gumtree scraper health check
[**gumtreeListCategories**](GumtreeAPI.md#gumtreelistcategories) | **GET** /v1/gumtree/categories | List categories
[**gumtreeListLocations**](GumtreeAPI.md#gumtreelistlocations) | **GET** /v1/gumtree/locations | List locations
[**gumtreeListMarkets**](GumtreeAPI.md#gumtreelistmarkets) | **GET** /v1/gumtree/markets | List markets
[**gumtreeLocationSuggestions**](GumtreeAPI.md#gumtreelocationsuggestions) | **GET** /v1/gumtree/locations/autocomplete | Location suggestions
[**gumtreeSearchListings**](GumtreeAPI.md#gumtreesearchlistings) | **GET** /v1/gumtree/search | Search listings
[**gumtreeSearchSuggestions**](GumtreeAPI.md#gumtreesearchsuggestions) | **GET** /v1/gumtree/autocomplete | Search suggestions


# **gumtreeGetListing**
```swift
    open class func gumtreeGetListing(listingId: String, market: Market_gumtreeGetListing? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get listing

Full listing — description, attributes, images, seller, similar listings.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let listingId = "listingId_example" // String | Gumtree listing id — the number at the end of the listing URL (uk/au: ~10 digits; za: the full 26-digit ad id, not the short one)
let market = "market_example" // String | Which Gumtree: 'uk' (gumtree.com, GBP), 'au' (gumtree.com.au, AUD) or 'za' (gumtree.co.za, ZAR). Separate sites — ids from one market mean nothing in another. (optional) (default to .uk)

// Get listing
GumtreeAPI.gumtreeGetListing(listingId: listingId, market: market) { (response, error) in
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
 **listingId** | **String** | Gumtree listing id — the number at the end of the listing URL (uk/au: ~10 digits; za: the full 26-digit ad id, not the short one) | 
 **market** | **String** | Which Gumtree: &#39;uk&#39; (gumtree.com, GBP), &#39;au&#39; (gumtree.com.au, AUD) or &#39;za&#39; (gumtree.co.za, ZAR). Separate sites — ids from one market mean nothing in another. | [optional] [default to .uk]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **gumtreeGetSearchFilters**
```swift
    open class func gumtreeGetSearchFilters(category: String? = nil, location: String? = nil, query: String? = nil, filters: String? = nil, market: Market_gumtreeGetSearchFilters? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get search filters

Filters, sort orders and radius options for a category, with live counts.  Feed a `key` and a `value` back into `/search` as `filters=key:value`. au bills 2x (browser render).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let category = "category_example" // String | uk: category slug, e.g. 'cars', 'for-sale', 'property-to-rent', 'jobs', 'bicycles'. au/za: numeric category id, e.g. '18320' (au cars) or '9077' (za cars). Use /categories to browse the tree. Default 'all'. (optional) (default to "all")
let location = "location_example" // String | uk: location slug ('london'), town name or UK postcode ('SW1A 1AA'). au/za: numeric location id, e.g. '3003435' (au Sydney) or '3100003' (za Gauteng). Use /locations/autocomplete to resolve one. Default: the whole country. (optional)
let query = "query_example" // String | Optional keywords to scope the counts (optional)
let filters = "filters_example" // String | za only: filters already applied (e.g. 'ma:toyota' to list Toyota models) (optional)
let market = "market_example" // String | Which Gumtree: 'uk' (gumtree.com, GBP), 'au' (gumtree.com.au, AUD) or 'za' (gumtree.co.za, ZAR). Separate sites — ids from one market mean nothing in another. (optional) (default to .uk)

// Get search filters
GumtreeAPI.gumtreeGetSearchFilters(category: category, location: location, query: query, filters: filters, market: market) { (response, error) in
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
 **category** | **String** | uk: category slug, e.g. &#39;cars&#39;, &#39;for-sale&#39;, &#39;property-to-rent&#39;, &#39;jobs&#39;, &#39;bicycles&#39;. au/za: numeric category id, e.g. &#39;18320&#39; (au cars) or &#39;9077&#39; (za cars). Use /categories to browse the tree. Default &#39;all&#39;. | [optional] [default to &quot;all&quot;]
 **location** | **String** | uk: location slug (&#39;london&#39;), town name or UK postcode (&#39;SW1A 1AA&#39;). au/za: numeric location id, e.g. &#39;3003435&#39; (au Sydney) or &#39;3100003&#39; (za Gauteng). Use /locations/autocomplete to resolve one. Default: the whole country. | [optional] 
 **query** | **String** | Optional keywords to scope the counts | [optional] 
 **filters** | **String** | za only: filters already applied (e.g. &#39;ma:toyota&#39; to list Toyota models) | [optional] 
 **market** | **String** | Which Gumtree: &#39;uk&#39; (gumtree.com, GBP), &#39;au&#39; (gumtree.com.au, AUD) or &#39;za&#39; (gumtree.co.za, ZAR). Separate sites — ids from one market mean nothing in another. | [optional] [default to .uk]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **gumtreeGetSellerListings**
```swift
    open class func gumtreeGetSellerListings(listingId: String, page: Int? = nil, market: Market_gumtreeGetSellerListings? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get seller listings

Every live listing by the seller of the given listing.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let listingId = "listingId_example" // String | Gumtree listing id — the number at the end of the listing URL (uk/au: ~10 digits; za: the full 26-digit ad id, not the short one)
let page = 987 // Int |  (optional) (default to 1)
let market = "market_example" // String | Which Gumtree: 'uk' (gumtree.com, GBP), 'au' (gumtree.com.au, AUD) or 'za' (gumtree.co.za, ZAR). Separate sites — ids from one market mean nothing in another. (optional) (default to .uk)

// Get seller listings
GumtreeAPI.gumtreeGetSellerListings(listingId: listingId, page: page, market: market) { (response, error) in
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
 **listingId** | **String** | Gumtree listing id — the number at the end of the listing URL (uk/au: ~10 digits; za: the full 26-digit ad id, not the short one) | 
 **page** | **Int** |  | [optional] [default to 1]
 **market** | **String** | Which Gumtree: &#39;uk&#39; (gumtree.com, GBP), &#39;au&#39; (gumtree.com.au, AUD) or &#39;za&#39; (gumtree.co.za, ZAR). Separate sites — ids from one market mean nothing in another. | [optional] [default to .uk]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **gumtreeGumtreeScraperHealthCheck**
```swift
    open class func gumtreeGumtreeScraperHealthCheck(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Gumtree scraper health check

Check health of the Gumtree scraper service (accepts HEAD for UptimeRobot).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// Gumtree scraper health check
GumtreeAPI.gumtreeGumtreeScraperHealthCheck() { (response, error) in
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

# **gumtreeGumtreeScraperHealthCheckHead**
```swift
    open class func gumtreeGumtreeScraperHealthCheckHead(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Gumtree scraper health check

Check health of the Gumtree scraper service (accepts HEAD for UptimeRobot).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// Gumtree scraper health check
GumtreeAPI.gumtreeGumtreeScraperHealthCheckHead() { (response, error) in
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

# **gumtreeListCategories**
```swift
    open class func gumtreeListCategories(parentId: Int? = nil, market: Market_gumtreeListCategories? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

List categories

Browse Gumtree's category tree.  A node's `slug` (uk) or `id` (au/za) is the `/search` category.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let parentId = 987 // Int | Category id to list the children of (default: all) (optional)
let market = "market_example" // String | Which Gumtree: 'uk' (gumtree.com, GBP), 'au' (gumtree.com.au, AUD) or 'za' (gumtree.co.za, ZAR). Separate sites — ids from one market mean nothing in another. (optional) (default to .uk)

// List categories
GumtreeAPI.gumtreeListCategories(parentId: parentId, market: market) { (response, error) in
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
 **parentId** | **Int** | Category id to list the children of (default: all) | [optional] 
 **market** | **String** | Which Gumtree: &#39;uk&#39; (gumtree.com, GBP), &#39;au&#39; (gumtree.com.au, AUD) or &#39;za&#39; (gumtree.co.za, ZAR). Separate sites — ids from one market mean nothing in another. | [optional] [default to .uk]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **gumtreeListLocations**
```swift
    open class func gumtreeListLocations(parentId: Int? = nil, market: Market_gumtreeListLocations? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

List locations

Browse Gumtree's location tree.  uk: UK -> nations -> counties -> towns. au: states -> regions -> areas, each with its live ad count (browser render, bills 5x). za: provinces -> towns.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let parentId = 987 // Int | Location id to list the children of (default: the whole country) (optional)
let market = "market_example" // String | Which Gumtree: 'uk' (gumtree.com, GBP), 'au' (gumtree.com.au, AUD) or 'za' (gumtree.co.za, ZAR). Separate sites — ids from one market mean nothing in another. (optional) (default to .uk)

// List locations
GumtreeAPI.gumtreeListLocations(parentId: parentId, market: market) { (response, error) in
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
 **parentId** | **Int** | Location id to list the children of (default: the whole country) | [optional] 
 **market** | **String** | Which Gumtree: &#39;uk&#39; (gumtree.com, GBP), &#39;au&#39; (gumtree.com.au, AUD) or &#39;za&#39; (gumtree.co.za, ZAR). Separate sites — ids from one market mean nothing in another. | [optional] [default to .uk]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **gumtreeListMarkets**
```swift
    open class func gumtreeListMarkets(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

List markets

The Gumtree sites this API covers (uk, au, za) with currency and id formats.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// List markets
GumtreeAPI.gumtreeListMarkets() { (response, error) in
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

# **gumtreeLocationSuggestions**
```swift
    open class func gumtreeLocationSuggestions(query: String, market: Market_gumtreeLocationSuggestions? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Location suggestions

Resolve a place name or postcode to Gumtree location ids (uk: with coordinates).  The `id` (au/za) or `name` (uk) is what `/search` takes as `location`.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let query = "query_example" // String | Town, area or postcode prefix, e.g. 'manch' or 'SW1A'
let market = "market_example" // String | Which Gumtree: 'uk' (gumtree.com, GBP), 'au' (gumtree.com.au, AUD) or 'za' (gumtree.co.za, ZAR). Separate sites — ids from one market mean nothing in another. (optional) (default to .uk)

// Location suggestions
GumtreeAPI.gumtreeLocationSuggestions(query: query, market: market) { (response, error) in
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
 **query** | **String** | Town, area or postcode prefix, e.g. &#39;manch&#39; or &#39;SW1A&#39; | 
 **market** | **String** | Which Gumtree: &#39;uk&#39; (gumtree.com, GBP), &#39;au&#39; (gumtree.com.au, AUD) or &#39;za&#39; (gumtree.co.za, ZAR). Separate sites — ids from one market mean nothing in another. | [optional] [default to .uk]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **gumtreeSearchListings**
```swift
    open class func gumtreeSearchListings(query: String? = nil, category: String? = nil, location: String? = nil, distance: Double? = nil, minPrice: Int? = nil, maxPrice: Int? = nil, sort: Sort_gumtreeSearchListings? = nil, sellerType: SellerType_gumtreeSearchListings? = nil, urgentOnly: Bool? = nil, withPhotos: Bool? = nil, filters: String? = nil, page: Int? = nil, market: Market_gumtreeSearchListings? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Search listings

Search Gumtree listings in the UK, Australia or South Africa.  Up to 50 pages. Page size: uk 25, au 24 (plus up to 6 featured top ads), za 20. An au search runs a real browser (~10-20 s) and bills 2x.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let query = "query_example" // String | Search keywords, e.g. 'mountain bike' (optional)
let category = "category_example" // String | uk: category slug, e.g. 'cars', 'for-sale', 'property-to-rent', 'jobs', 'bicycles'. au/za: numeric category id, e.g. '18320' (au cars) or '9077' (za cars). Use /categories to browse the tree. Default 'all'. (optional) (default to "all")
let location = "location_example" // String | uk: location slug ('london'), town name or UK postcode ('SW1A 1AA'). au/za: numeric location id, e.g. '3003435' (au Sydney) or '3100003' (za Gauteng). Use /locations/autocomplete to resolve one. Default: the whole country. (optional)
let distance = 987 // Double | Radius around `location`: miles (uk) or km (au). Not offered by za. (optional)
let minPrice = 987 // Int | Minimum price in the market's currency (uk: needs a category, not 'all') (optional)
let maxPrice = 987 // Int | Maximum price in the market's currency (uk: needs a category, not 'all') (optional)
let sort = "sort_example" // String | Result ordering (default relevance). 'distance' needs uk, or au with a location. (optional)
let sellerType = "sellerType_example" // String | uk/za: 'trade' covers dealers, agencies and recruiters. au: not supported — use a category filter such as 'cars.forsaleby_s:ownr'. (optional)
let urgentOnly = true // Bool | uk only: only ads marked urgent (optional) (default to false)
let withPhotos = true // Bool | uk only: only ads with photos (optional) (default to false)
let filters = "filters_example" // String | Category-specific filters as comma-separated key:value pairs, e.g. 'vehicle_make:bmw,vehicle_fuel_type:petrol,min_vehicle_mileage:10000' (uk), 'cars.carmake_s:toyota,cars.forsaleby_s:ownr' (au) or 'ma:toyota,fu:petrol,max_km:100000' (za). Range filters take min_<key>/max_<key>. Discover keys and values with /search/filters for the same market. (optional)
let page = 987 // Int |  (optional) (default to 1)
let market = "market_example" // String | Which Gumtree: 'uk' (gumtree.com, GBP), 'au' (gumtree.com.au, AUD) or 'za' (gumtree.co.za, ZAR). Separate sites — ids from one market mean nothing in another. (optional) (default to .uk)

// Search listings
GumtreeAPI.gumtreeSearchListings(query: query, category: category, location: location, distance: distance, minPrice: minPrice, maxPrice: maxPrice, sort: sort, sellerType: sellerType, urgentOnly: urgentOnly, withPhotos: withPhotos, filters: filters, page: page, market: market) { (response, error) in
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
 **query** | **String** | Search keywords, e.g. &#39;mountain bike&#39; | [optional] 
 **category** | **String** | uk: category slug, e.g. &#39;cars&#39;, &#39;for-sale&#39;, &#39;property-to-rent&#39;, &#39;jobs&#39;, &#39;bicycles&#39;. au/za: numeric category id, e.g. &#39;18320&#39; (au cars) or &#39;9077&#39; (za cars). Use /categories to browse the tree. Default &#39;all&#39;. | [optional] [default to &quot;all&quot;]
 **location** | **String** | uk: location slug (&#39;london&#39;), town name or UK postcode (&#39;SW1A 1AA&#39;). au/za: numeric location id, e.g. &#39;3003435&#39; (au Sydney) or &#39;3100003&#39; (za Gauteng). Use /locations/autocomplete to resolve one. Default: the whole country. | [optional] 
 **distance** | **Double** | Radius around &#x60;location&#x60;: miles (uk) or km (au). Not offered by za. | [optional] 
 **minPrice** | **Int** | Minimum price in the market&#39;s currency (uk: needs a category, not &#39;all&#39;) | [optional] 
 **maxPrice** | **Int** | Maximum price in the market&#39;s currency (uk: needs a category, not &#39;all&#39;) | [optional] 
 **sort** | **String** | Result ordering (default relevance). &#39;distance&#39; needs uk, or au with a location. | [optional] 
 **sellerType** | **String** | uk/za: &#39;trade&#39; covers dealers, agencies and recruiters. au: not supported — use a category filter such as &#39;cars.forsaleby_s:ownr&#39;. | [optional] 
 **urgentOnly** | **Bool** | uk only: only ads marked urgent | [optional] [default to false]
 **withPhotos** | **Bool** | uk only: only ads with photos | [optional] [default to false]
 **filters** | **String** | Category-specific filters as comma-separated key:value pairs, e.g. &#39;vehicle_make:bmw,vehicle_fuel_type:petrol,min_vehicle_mileage:10000&#39; (uk), &#39;cars.carmake_s:toyota,cars.forsaleby_s:ownr&#39; (au) or &#39;ma:toyota,fu:petrol,max_km:100000&#39; (za). Range filters take min_&lt;key&gt;/max_&lt;key&gt;. Discover keys and values with /search/filters for the same market. | [optional] 
 **page** | **Int** |  | [optional] [default to 1]
 **market** | **String** | Which Gumtree: &#39;uk&#39; (gumtree.com, GBP), &#39;au&#39; (gumtree.com.au, AUD) or &#39;za&#39; (gumtree.co.za, ZAR). Separate sites — ids from one market mean nothing in another. | [optional] [default to .uk]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **gumtreeSearchSuggestions**
```swift
    open class func gumtreeSearchSuggestions(query: String, market: Market_gumtreeSearchSuggestions? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Search suggestions

Gumtree search-box keyword suggestions with their categories.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let query = "query_example" // String | Partial search term, e.g. 'iph'
let market = "market_example" // String | Which Gumtree: 'uk' (gumtree.com, GBP), 'au' (gumtree.com.au, AUD) or 'za' (gumtree.co.za, ZAR). Separate sites — ids from one market mean nothing in another. (optional) (default to .uk)

// Search suggestions
GumtreeAPI.gumtreeSearchSuggestions(query: query, market: market) { (response, error) in
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
 **query** | **String** | Partial search term, e.g. &#39;iph&#39; | 
 **market** | **String** | Which Gumtree: &#39;uk&#39; (gumtree.com, GBP), &#39;au&#39; (gumtree.com.au, AUD) or &#39;za&#39; (gumtree.co.za, ZAR). Separate sites — ids from one market mean nothing in another. | [optional] [default to .uk]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

