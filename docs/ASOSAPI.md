# ASOSAPI

All URIs are relative to *https://scrapebadger.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**asosGetProductDetail**](ASOSAPI.md#asosgetproductdetail) | **GET** /v1/asos/products/{product_id} | Get product detail
[**asosGetStockAndPrices**](ASOSAPI.md#asosgetstockandprices) | **GET** /v1/asos/stock-price | Get stock and prices
[**asosListCategories**](ASOSAPI.md#asoslistcategories) | **GET** /v1/asos/categories | List categories
[**asosListMarkets**](ASOSAPI.md#asoslistmarkets) | **GET** /v1/asos/markets | List markets
[**asosListSearchFilters**](ASOSAPI.md#asoslistsearchfilters) | **GET** /v1/asos/filters | List search filters
[**asosSearchProducts**](ASOSAPI.md#asossearchproducts) | **GET** /v1/asos/search | Search products
[**asosSearchSuggestions**](ASOSAPI.md#asossearchsuggestions) | **GET** /v1/asos/autocomplete | Search suggestions


# **asosGetProductDetail**
```swift
    open class func asosGetProductDetail(productId: Int, market: String? = nil, store: String? = nil, country: String? = nil, currency: String? = nil, language: String? = nil, completion: @escaping (_ data: ProductResponse?, _ error: Error?) -> Void)
```

Get product detail

Product, live per-size stock and price, images, descriptions, reviews and breadcrumbs.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let productId = 987 // Int | 
let market = "market_example" // String | Storefront: uk, us, au, de, fr, it, es, nl, se, dk, pl (optional) (default to "uk")
let store = "store_example" // String | Override store, e.g. COM or US (optional)
let country = "country_example" // String | ISO country override (optional)
let currency = "currency_example" // String | Currency override (optional)
let language = "language_example" // String | Locale override, e.g. en-GB (optional)

// Get product detail
ASOSAPI.asosGetProductDetail(productId: productId, market: market, store: store, country: country, currency: currency, language: language) { (response, error) in
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
 **productId** | **Int** |  | 
 **market** | **String** | Storefront: uk, us, au, de, fr, it, es, nl, se, dk, pl | [optional] [default to &quot;uk&quot;]
 **store** | **String** | Override store, e.g. COM or US | [optional] 
 **country** | **String** | ISO country override | [optional] 
 **currency** | **String** | Currency override | [optional] 
 **language** | **String** | Locale override, e.g. en-GB | [optional] 

### Return type

[**ProductResponse**](ProductResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **asosGetStockAndPrices**
```swift
    open class func asosGetStockAndPrices(productIds: String, market: String? = nil, store: String? = nil, country: String? = nil, currency: String? = nil, language: String? = nil, completion: @escaping (_ data: StockResponse?, _ error: Error?) -> Void)
```

Get stock and prices

Refresh product and variant stock/prices; reports missing product ids explicitly.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let productIds = "productIds_example" // String | 1–50 comma-separated product ids
let market = "market_example" // String | Storefront: uk, us, au, de, fr, it, es, nl, se, dk, pl (optional) (default to "uk")
let store = "store_example" // String | Override store, e.g. COM or US (optional)
let country = "country_example" // String | ISO country override (optional)
let currency = "currency_example" // String | Currency override (optional)
let language = "language_example" // String | Locale override, e.g. en-GB (optional)

// Get stock and prices
ASOSAPI.asosGetStockAndPrices(productIds: productIds, market: market, store: store, country: country, currency: currency, language: language) { (response, error) in
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
 **productIds** | **String** | 1–50 comma-separated product ids | 
 **market** | **String** | Storefront: uk, us, au, de, fr, it, es, nl, se, dk, pl | [optional] [default to &quot;uk&quot;]
 **store** | **String** | Override store, e.g. COM or US | [optional] 
 **country** | **String** | ISO country override | [optional] 
 **currency** | **String** | Currency override | [optional] 
 **language** | **String** | Locale override, e.g. en-GB | [optional] 

### Return type

[**StockResponse**](StockResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **asosListCategories**
```swift
    open class func asosListCategories(gender: Gender_asosListCategories? = nil, market: String? = nil, store: String? = nil, country: String? = nil, currency: String? = nil, language: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

List categories

Full nested navigation with category ids, names, images and links.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let gender = "gender_example" // String |  (optional) (default to .men)
let market = "market_example" // String | Storefront: uk, us, au, de, fr, it, es, nl, se, dk, pl (optional) (default to "uk")
let store = "store_example" // String | Override store, e.g. COM or US (optional)
let country = "country_example" // String | ISO country override (optional)
let currency = "currency_example" // String | Currency override (optional)
let language = "language_example" // String | Locale override, e.g. en-GB (optional)

// List categories
ASOSAPI.asosListCategories(gender: gender, market: market, store: store, country: country, currency: currency, language: language) { (response, error) in
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
 **gender** | **String** |  | [optional] [default to .men]
 **market** | **String** | Storefront: uk, us, au, de, fr, it, es, nl, se, dk, pl | [optional] [default to &quot;uk&quot;]
 **store** | **String** | Override store, e.g. COM or US | [optional] 
 **country** | **String** | ISO country override | [optional] 
 **currency** | **String** | Currency override | [optional] 
 **language** | **String** | Locale override, e.g. en-GB | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **asosListMarkets**
```swift
    open class func asosListMarkets(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

List markets

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// List markets
ASOSAPI.asosListMarkets() { (response, error) in
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

# **asosListSearchFilters**
```swift
    open class func asosListSearchFilters(query: String? = nil, categoryId: Int? = nil, market: String? = nil, store: String? = nil, country: String? = nil, currency: String? = nil, language: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

List search filters

Facet ids, labels, option counts and selections for a query or category.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let query = "query_example" // String |  (optional)
let categoryId = 987 // Int |  (optional)
let market = "market_example" // String | Storefront: uk, us, au, de, fr, it, es, nl, se, dk, pl (optional) (default to "uk")
let store = "store_example" // String | Override store, e.g. COM or US (optional)
let country = "country_example" // String | ISO country override (optional)
let currency = "currency_example" // String | Currency override (optional)
let language = "language_example" // String | Locale override, e.g. en-GB (optional)

// List search filters
ASOSAPI.asosListSearchFilters(query: query, categoryId: categoryId, market: market, store: store, country: country, currency: currency, language: language) { (response, error) in
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
 **query** | **String** |  | [optional] 
 **categoryId** | **Int** |  | [optional] 
 **market** | **String** | Storefront: uk, us, au, de, fr, it, es, nl, se, dk, pl | [optional] [default to &quot;uk&quot;]
 **store** | **String** | Override store, e.g. COM or US | [optional] 
 **country** | **String** | ISO country override | [optional] 
 **currency** | **String** | Currency override | [optional] 
 **language** | **String** | Locale override, e.g. en-GB | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **asosSearchProducts**
```swift
    open class func asosSearchProducts(query: String? = nil, categoryId: Int? = nil, offset: Int? = nil, limit: Int? = nil, sort: Sort_asosSearchProducts? = nil, brand: String? = nil, colour: String? = nil, size: String? = nil, minPrice: Double? = nil, maxPrice: Double? = nil, market: String? = nil, store: String? = nil, country: String? = nil, currency: String? = nil, language: String? = nil, completion: @escaping (_ data: PortalApiRoutersV1AsosSearchResponse?, _ error: Error?) -> Void)
```

Search products

Search by query, category_id, or both. Includes price, images and filter facets.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let query = "query_example" // String | Keyword, e.g. shoes (optional)
let categoryId = 987 // Int | Category id from navigation (optional)
let offset = 987 // Int |  (optional) (default to 0)
let limit = 987 // Int |  (optional) (default to 48)
let sort = "sort_example" // String |  (optional) (default to .recommended)
let brand = "brand_example" // String | Comma-separated brand facet ids (optional)
let colour = "colour_example" // String | Comma-separated colour facet ids (optional)
let size = "size_example" // String | Comma-separated size facet ids (optional)
let minPrice = 987 // Double |  (optional)
let maxPrice = 987 // Double |  (optional)
let market = "market_example" // String | Storefront: uk, us, au, de, fr, it, es, nl, se, dk, pl (optional) (default to "uk")
let store = "store_example" // String | Override store, e.g. COM or US (optional)
let country = "country_example" // String | ISO country override (optional)
let currency = "currency_example" // String | Currency override (optional)
let language = "language_example" // String | Locale override, e.g. en-GB (optional)

// Search products
ASOSAPI.asosSearchProducts(query: query, categoryId: categoryId, offset: offset, limit: limit, sort: sort, brand: brand, colour: colour, size: size, minPrice: minPrice, maxPrice: maxPrice, market: market, store: store, country: country, currency: currency, language: language) { (response, error) in
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
 **query** | **String** | Keyword, e.g. shoes | [optional] 
 **categoryId** | **Int** | Category id from navigation | [optional] 
 **offset** | **Int** |  | [optional] [default to 0]
 **limit** | **Int** |  | [optional] [default to 48]
 **sort** | **String** |  | [optional] [default to .recommended]
 **brand** | **String** | Comma-separated brand facet ids | [optional] 
 **colour** | **String** | Comma-separated colour facet ids | [optional] 
 **size** | **String** | Comma-separated size facet ids | [optional] 
 **minPrice** | **Double** |  | [optional] 
 **maxPrice** | **Double** |  | [optional] 
 **market** | **String** | Storefront: uk, us, au, de, fr, it, es, nl, se, dk, pl | [optional] [default to &quot;uk&quot;]
 **store** | **String** | Override store, e.g. COM or US | [optional] 
 **country** | **String** | ISO country override | [optional] 
 **currency** | **String** | Currency override | [optional] 
 **language** | **String** | Locale override, e.g. en-GB | [optional] 

### Return type

[**PortalApiRoutersV1AsosSearchResponse**](PortalApiRoutersV1AsosSearchResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **asosSearchSuggestions**
```swift
    open class func asosSearchSuggestions(query: String, market: String? = nil, store: String? = nil, country: String? = nil, currency: String? = nil, language: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Search suggestions

Search suggestions with result counts.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let query = "query_example" // String | 
let market = "market_example" // String | Storefront: uk, us, au, de, fr, it, es, nl, se, dk, pl (optional) (default to "uk")
let store = "store_example" // String | Override store, e.g. COM or US (optional)
let country = "country_example" // String | ISO country override (optional)
let currency = "currency_example" // String | Currency override (optional)
let language = "language_example" // String | Locale override, e.g. en-GB (optional)

// Search suggestions
ASOSAPI.asosSearchSuggestions(query: query, market: market, store: store, country: country, currency: currency, language: language) { (response, error) in
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
 **market** | **String** | Storefront: uk, us, au, de, fr, it, es, nl, se, dk, pl | [optional] [default to &quot;uk&quot;]
 **store** | **String** | Override store, e.g. COM or US | [optional] 
 **country** | **String** | ISO country override | [optional] 
 **currency** | **String** | Currency override | [optional] 
 **language** | **String** | Locale override, e.g. en-GB | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

