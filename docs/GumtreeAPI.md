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
[**gumtreeLocationSuggestions**](GumtreeAPI.md#gumtreelocationsuggestions) | **GET** /v1/gumtree/locations/autocomplete | Location suggestions
[**gumtreeSearchListings**](GumtreeAPI.md#gumtreesearchlistings) | **GET** /v1/gumtree/search | Search listings
[**gumtreeSearchSuggestions**](GumtreeAPI.md#gumtreesearchsuggestions) | **GET** /v1/gumtree/autocomplete | Search suggestions


# **gumtreeGetListing**
```swift
    open class func gumtreeGetListing(listingId: String, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get listing

Full listing — description, attributes, images, seller, similar listings.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let listingId = "listingId_example" // String | Gumtree listing id — the number at the end of a gumtree.com/p/... URL

// Get listing
GumtreeAPI.gumtreeGetListing(listingId: listingId) { (response, error) in
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
 **listingId** | **String** | Gumtree listing id — the number at the end of a gumtree.com/p/... URL | 

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
    open class func gumtreeGetSearchFilters(category: String? = nil, location: String? = nil, query: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get search filters

Filters, sort orders and radius options for a category, with live counts.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let category = "category_example" // String | Category slug, e.g. 'cars', 'for-sale', 'property-to-rent', 'jobs'. Default 'all'. (optional) (default to "all")
let location = "location_example" // String | Location slug ('london'), town name or UK postcode ('SW1A 1AA'). Default 'uk'. (optional) (default to "uk")
let query = "query_example" // String |  (optional)

// Get search filters
GumtreeAPI.gumtreeGetSearchFilters(category: category, location: location, query: query) { (response, error) in
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
 **category** | **String** | Category slug, e.g. &#39;cars&#39;, &#39;for-sale&#39;, &#39;property-to-rent&#39;, &#39;jobs&#39;. Default &#39;all&#39;. | [optional] [default to &quot;all&quot;]
 **location** | **String** | Location slug (&#39;london&#39;), town name or UK postcode (&#39;SW1A 1AA&#39;). Default &#39;uk&#39;. | [optional] [default to &quot;uk&quot;]
 **query** | **String** |  | [optional] 

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
    open class func gumtreeGetSellerListings(listingId: String, page: Int? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get seller listings

Every live listing by the seller of the given listing.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let listingId = "listingId_example" // String | Gumtree listing id — the number at the end of a gumtree.com/p/... URL
let page = 987 // Int |  (optional) (default to 1)

// Get seller listings
GumtreeAPI.gumtreeGetSellerListings(listingId: listingId, page: page) { (response, error) in
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
 **listingId** | **String** | Gumtree listing id — the number at the end of a gumtree.com/p/... URL | 
 **page** | **Int** |  | [optional] [default to 1]

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
    open class func gumtreeListCategories(parentId: Int? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

List categories

Browse Gumtree's category tree. A node's `slug` is the `/search` category.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let parentId = 987 // Int | Parent category id (default: all) (optional) (default to 1)

// List categories
GumtreeAPI.gumtreeListCategories(parentId: parentId) { (response, error) in
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
 **parentId** | **Int** | Parent category id (default: all) | [optional] [default to 1]

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
    open class func gumtreeListLocations(parentId: Int? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

List locations

Browse Gumtree's location tree.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let parentId = 987 // Int | Parent location id (default: UK) (optional) (default to 10000392)

// List locations
GumtreeAPI.gumtreeListLocations(parentId: parentId) { (response, error) in
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
 **parentId** | **Int** | Parent location id (default: UK) | [optional] [default to 10000392]

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
    open class func gumtreeLocationSuggestions(query: String, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Location suggestions

Resolve a place name or postcode to Gumtree locations with coordinates.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let query = "query_example" // String | Town or postcode prefix, e.g. 'manch'

// Location suggestions
GumtreeAPI.gumtreeLocationSuggestions(query: query) { (response, error) in
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
 **query** | **String** | Town or postcode prefix, e.g. &#39;manch&#39; | 

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
    open class func gumtreeSearchListings(query: String? = nil, category: String? = nil, location: String? = nil, distance: Double? = nil, minPrice: Int? = nil, maxPrice: Int? = nil, sort: Sort_gumtreeSearchListings? = nil, sellerType: SellerType_gumtreeSearchListings? = nil, urgentOnly: Bool? = nil, withPhotos: Bool? = nil, filters: String? = nil, page: Int? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Search listings

Search gumtree.com listings. ~25-30 per page, up to 50 pages.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let query = "query_example" // String | Search keywords, e.g. 'mountain bike' (optional)
let category = "category_example" // String | Category slug, e.g. 'cars', 'for-sale', 'property-to-rent', 'jobs'. Default 'all'. (optional) (default to "all")
let location = "location_example" // String | Location slug ('london'), town name or UK postcode ('SW1A 1AA'). Default 'uk'. (optional) (default to "uk")
let distance = 987 // Double | Radius in miles (optional)
let minPrice = 987 // Int | GBP; needs a category (optional)
let maxPrice = 987 // Int | GBP; needs a category (optional)
let sort = "sort_example" // String |  (optional)
let sellerType = "sellerType_example" // String |  (optional)
let urgentOnly = true // Bool |  (optional) (default to false)
let withPhotos = true // Bool |  (optional) (default to false)
let filters = "filters_example" // String | Category filters as key:value pairs, e.g. 'vehicle_make:bmw,vehicle_fuel_type:petrol' (optional)
let page = 987 // Int |  (optional) (default to 1)

// Search listings
GumtreeAPI.gumtreeSearchListings(query: query, category: category, location: location, distance: distance, minPrice: minPrice, maxPrice: maxPrice, sort: sort, sellerType: sellerType, urgentOnly: urgentOnly, withPhotos: withPhotos, filters: filters, page: page) { (response, error) in
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
 **category** | **String** | Category slug, e.g. &#39;cars&#39;, &#39;for-sale&#39;, &#39;property-to-rent&#39;, &#39;jobs&#39;. Default &#39;all&#39;. | [optional] [default to &quot;all&quot;]
 **location** | **String** | Location slug (&#39;london&#39;), town name or UK postcode (&#39;SW1A 1AA&#39;). Default &#39;uk&#39;. | [optional] [default to &quot;uk&quot;]
 **distance** | **Double** | Radius in miles | [optional] 
 **minPrice** | **Int** | GBP; needs a category | [optional] 
 **maxPrice** | **Int** | GBP; needs a category | [optional] 
 **sort** | **String** |  | [optional] 
 **sellerType** | **String** |  | [optional] 
 **urgentOnly** | **Bool** |  | [optional] [default to false]
 **withPhotos** | **Bool** |  | [optional] [default to false]
 **filters** | **String** | Category filters as key:value pairs, e.g. &#39;vehicle_make:bmw,vehicle_fuel_type:petrol&#39; | [optional] 
 **page** | **Int** |  | [optional] [default to 1]

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
    open class func gumtreeSearchSuggestions(query: String, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Search suggestions

Gumtree search-box keyword suggestions with their categories.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let query = "query_example" // String | Partial search term, e.g. 'iph'

// Search suggestions
GumtreeAPI.gumtreeSearchSuggestions(query: query) { (response, error) in
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

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

