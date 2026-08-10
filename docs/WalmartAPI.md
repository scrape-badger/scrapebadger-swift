# WalmartAPI

All URIs are relative to *https://scrapebadger.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**walmartBrowseACategory**](WalmartAPI.md#walmartbrowseacategory) | **GET** /v1/walmart/category | Browse a category
[**walmartDealsRollbacksAndClearance**](WalmartAPI.md#walmartdealsrollbacksandclearance) | **GET** /v1/walmart/deals | Deals, rollbacks and clearance
[**walmartGetASellerSCatalogue**](WalmartAPI.md#walmartgetasellerscatalogue) | **GET** /v1/walmart/sellers/{seller_id}/products | Get a seller&#39;s catalogue
[**walmartGetProductDetail**](WalmartAPI.md#walmartgetproductdetail) | **GET** /v1/walmart/products/{item_id} | Get product detail
[**walmartGetProductReviews**](WalmartAPI.md#walmartgetproductreviews) | **GET** /v1/walmart/products/{item_id}/reviews | Get product reviews
[**walmartGetSellerProfile**](WalmartAPI.md#walmartgetsellerprofile) | **GET** /v1/walmart/sellers/{seller_id} | Get seller profile
[**walmartGetStoreNearbyStores**](WalmartAPI.md#walmartgetstorenearbystores) | **GET** /v1/walmart/stores/{store_id} | Get store + nearby stores
[**walmartListSupportedMarkets**](WalmartAPI.md#walmartlistsupportedmarkets) | **GET** /v1/walmart/markets | List supported markets
[**walmartSearchProducts**](WalmartAPI.md#walmartsearchproducts) | **GET** /v1/walmart/search | Search products
[**walmartSearchSuggestions**](WalmartAPI.md#walmartsearchsuggestions) | **GET** /v1/walmart/autocomplete | Search suggestions
[**walmartWalmartScraperHealthCheck**](WalmartAPI.md#walmartwalmartscraperhealthcheck) | **GET** /v1/walmart/health | Walmart scraper health check
[**walmartWalmartScraperHealthCheckHead**](WalmartAPI.md#walmartwalmartscraperhealthcheckhead) | **HEAD** /v1/walmart/health | Walmart scraper health check


# **walmartBrowseACategory**
```swift
    open class func walmartBrowseACategory(path: String, page: Int? = nil, minPrice: Double? = nil, maxPrice: Double? = nil, facet: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Browse a category

Browse a Walmart category. Same result shape as search.  No `sort`: Walmart's browse pages ignore it. Sort on `/search` instead.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let path = "path_example" // String | Browse path, e.g. 'electronics/3944', or a '/cp/...' path
let page = 987 // Int |  (optional) (default to 1)
let minPrice = 987 // Double |  (optional)
let maxPrice = 987 // Double |  (optional)
let facet = "facet_example" // String |  (optional)

// Browse a category
WalmartAPI.walmartBrowseACategory(path: path, page: page, minPrice: minPrice, maxPrice: maxPrice, facet: facet) { (response, error) in
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
 **path** | **String** | Browse path, e.g. &#39;electronics/3944&#39;, or a &#39;/cp/...&#39; path | 
 **page** | **Int** |  | [optional] [default to 1]
 **minPrice** | **Double** |  | [optional] 
 **maxPrice** | **Double** |  | [optional] 
 **facet** | **String** |  | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **walmartDealsRollbacksAndClearance**
```swift
    open class func walmartDealsRollbacksAndClearance(page: Int? = nil, minPrice: Double? = nil, maxPrice: Double? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Deals, rollbacks and clearance

Walmart's current deals, rollbacks and clearance.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let page = 987 // Int |  (optional) (default to 1)
let minPrice = 987 // Double |  (optional)
let maxPrice = 987 // Double |  (optional)

// Deals, rollbacks and clearance
WalmartAPI.walmartDealsRollbacksAndClearance(page: page, minPrice: minPrice, maxPrice: maxPrice) { (response, error) in
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
 **page** | **Int** |  | [optional] [default to 1]
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

# **walmartGetASellerSCatalogue**
```swift
    open class func walmartGetASellerSCatalogue(sellerId: String, query: String, page: Int? = nil, sort: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get a seller's catalogue

A marketplace seller's catalogue, scoped by a search term.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let sellerId = "sellerId_example" // String | Numeric catalog seller id, e.g. '101040442' — the `catalog_seller_id` on a product, NOT the 32-char hex `seller_id` (which 404s).
let query = "query_example" // String | Required — Walmart returns nothing for a seller facet alone
let page = 987 // Int |  (optional) (default to 1)
let sort = "sort_example" // String |  (optional)

// Get a seller's catalogue
WalmartAPI.walmartGetASellerSCatalogue(sellerId: sellerId, query: query, page: page, sort: sort) { (response, error) in
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
 **sellerId** | **String** | Numeric catalog seller id, e.g. &#39;101040442&#39; — the &#x60;catalog_seller_id&#x60; on a product, NOT the 32-char hex &#x60;seller_id&#x60; (which 404s). | 
 **query** | **String** | Required — Walmart returns nothing for a seller facet alone | 
 **page** | **Int** |  | [optional] [default to 1]
 **sort** | **String** |  | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **walmartGetProductDetail**
```swift
    open class func walmartGetProductDetail(itemId: String, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get product detail

Full product detail — price, stock, specs, variants, seller, reviews sample.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let itemId = "itemId_example" // String | Walmart usItemId, e.g. '5689919121'

// Get product detail
WalmartAPI.walmartGetProductDetail(itemId: itemId) { (response, error) in
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
 **itemId** | **String** | Walmart usItemId, e.g. &#39;5689919121&#39; | 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **walmartGetProductReviews**
```swift
    open class func walmartGetProductReviews(itemId: String, page: Int? = nil, sort: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get product reviews

Paginated reviews with the full star histogram. 10 per page.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let itemId = "itemId_example" // String | Walmart usItemId, e.g. '5689919121'
let page = 987 // Int |  (optional) (default to 1)
let sort = "sort_example" // String | relevancy | submission-desc | submission-asc | rating-desc | rating-asc | helpful (optional)

// Get product reviews
WalmartAPI.walmartGetProductReviews(itemId: itemId, page: page, sort: sort) { (response, error) in
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
 **itemId** | **String** | Walmart usItemId, e.g. &#39;5689919121&#39; | 
 **page** | **Int** |  | [optional] [default to 1]
 **sort** | **String** | relevancy | submission-desc | submission-asc | rating-desc | rating-asc | helpful | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **walmartGetSellerProfile**
```swift
    open class func walmartGetSellerProfile(sellerId: String, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get seller profile

Marketplace seller profile — contact details, address, rating, policies.  No `page`: adding one makes Walmart's own SSR throw. Use `/sellers/{id}/products` for the catalogue.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let sellerId = "sellerId_example" // String | Numeric catalog seller id, e.g. '101040442' — the `catalog_seller_id` on a product, NOT the 32-char hex `seller_id` (which 404s).

// Get seller profile
WalmartAPI.walmartGetSellerProfile(sellerId: sellerId) { (response, error) in
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
 **sellerId** | **String** | Numeric catalog seller id, e.g. &#39;101040442&#39; — the &#x60;catalog_seller_id&#x60; on a product, NOT the 32-char hex &#x60;seller_id&#x60; (which 404s). | 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **walmartGetStoreNearbyStores**
```swift
    open class func walmartGetStoreNearbyStores(storeId: String, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get store + nearby stores

Store detail with hours, per-department services, and nearby stores.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let storeId = "storeId_example" // String | Walmart store number, e.g. '100'

// Get store + nearby stores
WalmartAPI.walmartGetStoreNearbyStores(storeId: storeId) { (response, error) in
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
 **storeId** | **String** | Walmart store number, e.g. &#39;100&#39; | 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **walmartListSupportedMarkets**
```swift
    open class func walmartListSupportedMarkets(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

List supported markets

Supported Walmart markets.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// List supported markets
WalmartAPI.walmartListSupportedMarkets() { (response, error) in
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

# **walmartSearchProducts**
```swift
    open class func walmartSearchProducts(query: String, page: Int? = nil, sort: String? = nil, minPrice: Double? = nil, maxPrice: Double? = nil, facet: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Search products

Search walmart.com. ~40-60 organic products per page; ad tiles are dropped.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let query = "query_example" // String | Search keywords, e.g. 'laptop'
let page = 987 // Int | Results dry up after page 10 (optional) (default to 1)
let sort = "sort_example" // String | best_match | best_seller | price_low | price_high | rating_high | new (optional)
let minPrice = 987 // Double |  (optional)
let maxPrice = 987 // Double |  (optional)
let facet = "facet_example" // String | Facet filter, e.g. 'brand:HP' (optional)

// Search products
WalmartAPI.walmartSearchProducts(query: query, page: page, sort: sort, minPrice: minPrice, maxPrice: maxPrice, facet: facet) { (response, error) in
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
 **query** | **String** | Search keywords, e.g. &#39;laptop&#39; | 
 **page** | **Int** | Results dry up after page 10 | [optional] [default to 1]
 **sort** | **String** | best_match | best_seller | price_low | price_high | rating_high | new | [optional] 
 **minPrice** | **Double** |  | [optional] 
 **maxPrice** | **Double** |  | [optional] 
 **facet** | **String** | Facet filter, e.g. &#39;brand:HP&#39; | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **walmartSearchSuggestions**
```swift
    open class func walmartSearchSuggestions(query: String, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Search suggestions

Walmart search-box suggestions.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let query = "query_example" // String | Partial search term, e.g. 'lapt'

// Search suggestions
WalmartAPI.walmartSearchSuggestions(query: query) { (response, error) in
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
 **query** | **String** | Partial search term, e.g. &#39;lapt&#39; | 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **walmartWalmartScraperHealthCheck**
```swift
    open class func walmartWalmartScraperHealthCheck(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Walmart scraper health check

Check health of the Walmart scraper service (accepts HEAD for UptimeRobot).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// Walmart scraper health check
WalmartAPI.walmartWalmartScraperHealthCheck() { (response, error) in
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

# **walmartWalmartScraperHealthCheckHead**
```swift
    open class func walmartWalmartScraperHealthCheckHead(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Walmart scraper health check

Check health of the Walmart scraper service (accepts HEAD for UptimeRobot).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// Walmart scraper health check
WalmartAPI.walmartWalmartScraperHealthCheckHead() { (response, error) in
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

