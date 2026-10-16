# AliExpressAPI

All URIs are relative to *https://scrapebadger.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**aliexpressGetCategoryNavigation**](AliExpressAPI.md#aliexpressgetcategorynavigation) | **GET** /v1/aliexpress/categories | Get category navigation
[**aliexpressGetProductDetail**](AliExpressAPI.md#aliexpressgetproductdetail) | **GET** /v1/aliexpress/products/{product_id} | Get product detail
[**aliexpressGetProductReviews**](AliExpressAPI.md#aliexpressgetproductreviews) | **GET** /v1/aliexpress/products/{product_id}/reviews | Get product reviews
[**aliexpressGetSearchSuggestions**](AliExpressAPI.md#aliexpressgetsearchsuggestions) | **GET** /v1/aliexpress/autocomplete | Get search suggestions
[**aliexpressGetStoreProductCategories**](AliExpressAPI.md#aliexpressgetstoreproductcategories) | **GET** /v1/aliexpress/stores/{store_id}/categories | Get store product categories
[**aliexpressGetStoreProducts**](AliExpressAPI.md#aliexpressgetstoreproducts) | **GET** /v1/aliexpress/stores/{store_id}/products | Get store products
[**aliexpressGetStoreProfile**](AliExpressAPI.md#aliexpressgetstoreprofile) | **GET** /v1/aliexpress/stores/{store_id} | Get store profile
[**aliexpressSearchProducts**](AliExpressAPI.md#aliexpresssearchproducts) | **GET** /v1/aliexpress/search | Search products


# **aliexpressGetCategoryNavigation**
```swift
    open class func aliexpressGetCategoryNavigation(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get category navigation

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// Get category navigation
AliExpressAPI.aliexpressGetCategoryNavigation() { (response, error) in
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

# **aliexpressGetProductDetail**
```swift
    open class func aliexpressGetProductDetail(productId: String, country: String? = nil, currency: String? = nil, language: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get product detail

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let productId = "productId_example" // String | 
let country = "country_example" // String |  (optional) (default to "US")
let currency = "currency_example" // String |  (optional) (default to "USD")
let language = "language_example" // String |  (optional) (default to "en_US")

// Get product detail
AliExpressAPI.aliexpressGetProductDetail(productId: productId, country: country, currency: currency, language: language) { (response, error) in
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
 **country** | **String** |  | [optional] [default to &quot;US&quot;]
 **currency** | **String** |  | [optional] [default to &quot;USD&quot;]
 **language** | **String** |  | [optional] [default to &quot;en_US&quot;]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **aliexpressGetProductReviews**
```swift
    open class func aliexpressGetProductReviews(productId: String, page: Int? = nil, pageSize: Int? = nil, sort: Sort_aliexpressGetProductReviews? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get product reviews

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let productId = "productId_example" // String | 
let page = 987 // Int |  (optional) (default to 1)
let pageSize = 987 // Int |  (optional) (default to 10)
let sort = "sort_example" // String |  (optional) (default to .complexDefault)

// Get product reviews
AliExpressAPI.aliexpressGetProductReviews(productId: productId, page: page, pageSize: pageSize, sort: sort) { (response, error) in
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
 **page** | **Int** |  | [optional] [default to 1]
 **pageSize** | **Int** |  | [optional] [default to 10]
 **sort** | **String** |  | [optional] [default to .complexDefault]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **aliexpressGetSearchSuggestions**
```swift
    open class func aliexpressGetSearchSuggestions(query: String, country: String? = nil, language: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get search suggestions

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let query = "query_example" // String | 
let country = "country_example" // String |  (optional) (default to "US")
let language = "language_example" // String |  (optional) (default to "en")

// Get search suggestions
AliExpressAPI.aliexpressGetSearchSuggestions(query: query, country: country, language: language) { (response, error) in
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
 **language** | **String** |  | [optional] [default to &quot;en&quot;]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **aliexpressGetStoreProductCategories**
```swift
    open class func aliexpressGetStoreProductCategories(storeId: String, country: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get store product categories

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let storeId = "storeId_example" // String | 
let country = "country_example" // String |  (optional) (default to "US")

// Get store product categories
AliExpressAPI.aliexpressGetStoreProductCategories(storeId: storeId, country: country) { (response, error) in
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
 **storeId** | **String** |  | 
 **country** | **String** |  | [optional] [default to &quot;US&quot;]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **aliexpressGetStoreProducts**
```swift
    open class func aliexpressGetStoreProducts(storeId: String, page: Int? = nil, pageSize: Int? = nil, country: String? = nil, currency: String? = nil, language: String? = nil, query: String? = nil, sort: Sort_aliexpressGetStoreProducts? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get store products

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let storeId = "storeId_example" // String | 
let page = 987 // Int |  (optional) (default to 1)
let pageSize = 987 // Int |  (optional) (default to 24)
let country = "country_example" // String |  (optional) (default to "US")
let currency = "currency_example" // String |  (optional) (default to "USD")
let language = "language_example" // String |  (optional) (default to "en")
let query = "query_example" // String |  (optional) (default to "")
let sort = "sort_example" // String |  (optional) (default to .bestmatchSort)

// Get store products
AliExpressAPI.aliexpressGetStoreProducts(storeId: storeId, page: page, pageSize: pageSize, country: country, currency: currency, language: language, query: query, sort: sort) { (response, error) in
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
 **storeId** | **String** |  | 
 **page** | **Int** |  | [optional] [default to 1]
 **pageSize** | **Int** |  | [optional] [default to 24]
 **country** | **String** |  | [optional] [default to &quot;US&quot;]
 **currency** | **String** |  | [optional] [default to &quot;USD&quot;]
 **language** | **String** |  | [optional] [default to &quot;en&quot;]
 **query** | **String** |  | [optional] [default to &quot;&quot;]
 **sort** | **String** |  | [optional] [default to .bestmatchSort]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **aliexpressGetStoreProfile**
```swift
    open class func aliexpressGetStoreProfile(storeId: String, country: String? = nil, currency: String? = nil, language: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get store profile

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let storeId = "storeId_example" // String | 
let country = "country_example" // String |  (optional) (default to "US")
let currency = "currency_example" // String |  (optional) (default to "USD")
let language = "language_example" // String |  (optional) (default to "en")

// Get store profile
AliExpressAPI.aliexpressGetStoreProfile(storeId: storeId, country: country, currency: currency, language: language) { (response, error) in
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
 **storeId** | **String** |  | 
 **country** | **String** |  | [optional] [default to &quot;US&quot;]
 **currency** | **String** |  | [optional] [default to &quot;USD&quot;]
 **language** | **String** |  | [optional] [default to &quot;en&quot;]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **aliexpressSearchProducts**
```swift
    open class func aliexpressSearchProducts(query: String, page: Int? = nil, country: String? = nil, currency: String? = nil, language: String? = nil, sort: Sort_aliexpressSearchProducts? = nil, minPrice: Double? = nil, maxPrice: Double? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Search products

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let query = "query_example" // String | 
let page = 987 // Int |  (optional) (default to 1)
let country = "country_example" // String |  (optional) (default to "US")
let currency = "currency_example" // String |  (optional) (default to "USD")
let language = "language_example" // String |  (optional) (default to "en")
let sort = "sort_example" // String |  (optional) (default to ._default)
let minPrice = 987 // Double |  (optional)
let maxPrice = 987 // Double |  (optional)

// Search products
AliExpressAPI.aliexpressSearchProducts(query: query, page: page, country: country, currency: currency, language: language, sort: sort, minPrice: minPrice, maxPrice: maxPrice) { (response, error) in
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
 **language** | **String** |  | [optional] [default to &quot;en&quot;]
 **sort** | **String** |  | [optional] [default to ._default]
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

