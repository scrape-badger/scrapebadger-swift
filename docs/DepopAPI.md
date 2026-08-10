# DepopAPI

All URIs are relative to *https://scrapebadger.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**depopDepopScraperHealthCheck**](DepopAPI.md#depopdepopscraperhealthcheck) | **GET** /v1/depop/health | Depop scraper health check
[**depopDepopScraperHealthCheckHead**](DepopAPI.md#depopdepopscraperhealthcheckhead) | **HEAD** /v1/depop/health | Depop scraper health check
[**depopGetAUserSProducts**](DepopAPI.md#depopgetausersproducts) | **GET** /v1/depop/users/{username}/products | Get a user&#39;s products
[**depopGetProductDetail**](DepopAPI.md#depopgetproductdetail) | **GET** /v1/depop/products/{product_id} | Get product detail
[**depopGetShopUserProfile**](DepopAPI.md#depopgetshopuserprofile) | **GET** /v1/depop/users/{username} | Get shop/user profile
[**depopListMarkets**](DepopAPI.md#depoplistmarkets) | **GET** /v1/depop/markets | List markets
[**depopSearchDepopProducts**](DepopAPI.md#depopsearchdepopproducts) | **GET** /v1/depop/search | Search Depop products


# **depopDepopScraperHealthCheck**
```swift
    open class func depopDepopScraperHealthCheck(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Depop scraper health check

Check health of the Depop scraper service (accepts HEAD).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// Depop scraper health check
DepopAPI.depopDepopScraperHealthCheck() { (response, error) in
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

# **depopDepopScraperHealthCheckHead**
```swift
    open class func depopDepopScraperHealthCheckHead(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Depop scraper health check

Check health of the Depop scraper service (accepts HEAD).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// Depop scraper health check
DepopAPI.depopDepopScraperHealthCheckHead() { (response, error) in
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

# **depopGetAUserSProducts**
```swift
    open class func depopGetAUserSProducts(username: String, market: String? = nil, perPage: Int? = nil, cursor: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get a user's products

A user's active listings (cursor-paginated).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let username = "username_example" // String | 
let market = "market_example" // String | Market code (optional) (default to "us")
let perPage = 987 // Int |  (optional) (default to 24)
let cursor = "cursor_example" // String | Pagination cursor (optional)

// Get a user's products
DepopAPI.depopGetAUserSProducts(username: username, market: market, perPage: perPage, cursor: cursor) { (response, error) in
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
 **username** | **String** |  | 
 **market** | **String** | Market code | [optional] [default to &quot;us&quot;]
 **perPage** | **Int** |  | [optional] [default to 24]
 **cursor** | **String** | Pagination cursor | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **depopGetProductDetail**
```swift
    open class func depopGetProductDetail(productId: String, market: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get product detail

Full detail for a single product (by numeric id or slug).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let productId = "productId_example" // String | 
let market = "market_example" // String | Market code (optional) (default to "us")

// Get product detail
DepopAPI.depopGetProductDetail(productId: productId, market: market) { (response, error) in
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
 **productId** | **String** |  | 
 **market** | **String** | Market code | [optional] [default to &quot;us&quot;]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **depopGetShopUserProfile**
```swift
    open class func depopGetShopUserProfile(username: String, market: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get shop/user profile

Public shop/user profile by username.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let username = "username_example" // String | 
let market = "market_example" // String | Market code (optional) (default to "us")

// Get shop/user profile
DepopAPI.depopGetShopUserProfile(username: username, market: market) { (response, error) in
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
 **username** | **String** |  | 
 **market** | **String** | Market code | [optional] [default to &quot;us&quot;]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **depopListMarkets**
```swift
    open class func depopListMarkets(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

List markets

List supported Depop markets (country + currency).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// List markets
DepopAPI.depopListMarkets() { (response, error) in
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

# **depopSearchDepopProducts**
```swift
    open class func depopSearchDepopProducts(query: String, market: String? = nil, perPage: Int? = nil, cursor: String? = nil, priceMin: Double? = nil, priceMax: Double? = nil, brands: String? = nil, categories: String? = nil, sizes: String? = nil, conditions: String? = nil, gender: String? = nil, sort: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Search Depop products

Search the Depop catalog with filters (cursor-paginated).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let query = "query_example" // String | Search text, e.g. 'nike vintage'
let market = "market_example" // String | Market code (us, gb, au, it, fr, ...) (optional) (default to "us")
let perPage = 987 // Int | Results per page (optional) (default to 24)
let cursor = "cursor_example" // String | Pagination cursor (from previous page) (optional)
let priceMin = 987 // Double | Minimum price (optional)
let priceMax = 987 // Double | Maximum price (optional)
let brands = "brands_example" // String | Comma-separated brand IDs (optional)
let categories = "categories_example" // String | Comma-separated category IDs (optional)
let sizes = "sizes_example" // String | Comma-separated size IDs (optional)
let conditions = "conditions_example" // String | Comma-separated condition slugs (brand_new, used_excellent, ...) (optional)
let gender = "gender_example" // String | male | female (optional)
let sort = "sort_example" // String | relevance | newlyListed | priceAscending | priceDescending (optional)

// Search Depop products
DepopAPI.depopSearchDepopProducts(query: query, market: market, perPage: perPage, cursor: cursor, priceMin: priceMin, priceMax: priceMax, brands: brands, categories: categories, sizes: sizes, conditions: conditions, gender: gender, sort: sort) { (response, error) in
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
 **query** | **String** | Search text, e.g. &#39;nike vintage&#39; | 
 **market** | **String** | Market code (us, gb, au, it, fr, ...) | [optional] [default to &quot;us&quot;]
 **perPage** | **Int** | Results per page | [optional] [default to 24]
 **cursor** | **String** | Pagination cursor (from previous page) | [optional] 
 **priceMin** | **Double** | Minimum price | [optional] 
 **priceMax** | **Double** | Maximum price | [optional] 
 **brands** | **String** | Comma-separated brand IDs | [optional] 
 **categories** | **String** | Comma-separated category IDs | [optional] 
 **sizes** | **String** | Comma-separated size IDs | [optional] 
 **conditions** | **String** | Comma-separated condition slugs (brand_new, used_excellent, ...) | [optional] 
 **gender** | **String** | male | female | [optional] 
 **sort** | **String** | relevance | newlyListed | priceAscending | priceDescending | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

