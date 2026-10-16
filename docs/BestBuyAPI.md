# BestBuyAPI

All URIs are relative to *https://scrapebadger.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**bestbuyBrowseACategory**](BestBuyAPI.md#bestbuybrowseacategory) | **GET** /v1/bestbuy/category | Browse a category
[**bestbuyGetCategories**](BestBuyAPI.md#bestbuygetcategories) | **GET** /v1/bestbuy/categories | Get categories
[**bestbuyGetLaptopAndComputerDeals**](BestBuyAPI.md#bestbuygetlaptopandcomputerdeals) | **GET** /v1/bestbuy/deals | Get laptop and computer deals
[**bestbuyGetProductAvailability**](BestBuyAPI.md#bestbuygetproductavailability) | **GET** /v1/bestbuy/products/{sku}/availability | Get product availability
[**bestbuyGetProductDetail**](BestBuyAPI.md#bestbuygetproductdetail) | **GET** /v1/bestbuy/products/{sku} | Get product detail
[**bestbuyGetProductQuestions**](BestBuyAPI.md#bestbuygetproductquestions) | **GET** /v1/bestbuy/products/{sku}/questions | Get product questions
[**bestbuyGetProductReviews**](BestBuyAPI.md#bestbuygetproductreviews) | **GET** /v1/bestbuy/products/{sku}/reviews | Get product reviews
[**bestbuyGetSearchSuggestions**](BestBuyAPI.md#bestbuygetsearchsuggestions) | **GET** /v1/bestbuy/autocomplete | Get search suggestions
[**bestbuyListSupportedMarkets**](BestBuyAPI.md#bestbuylistsupportedmarkets) | **GET** /v1/bestbuy/markets | List supported markets
[**bestbuySearchProducts**](BestBuyAPI.md#bestbuysearchproducts) | **GET** /v1/bestbuy/search | Search products


# **bestbuyBrowseACategory**
```swift
    open class func bestbuyBrowseACategory(categoryId: String, page: Int? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Browse a category

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let categoryId = "categoryId_example" // String | 
let page = 987 // Int |  (optional) (default to 1)

// Browse a category
BestBuyAPI.bestbuyBrowseACategory(categoryId: categoryId, page: page) { (response, error) in
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
 **categoryId** | **String** |  | 
 **page** | **Int** |  | [optional] [default to 1]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **bestbuyGetCategories**
```swift
    open class func bestbuyGetCategories(query: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get categories

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let query = "query_example" // String |  (optional) (default to "laptop")

// Get categories
BestBuyAPI.bestbuyGetCategories(query: query) { (response, error) in
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
 **query** | **String** |  | [optional] [default to &quot;laptop&quot;]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **bestbuyGetLaptopAndComputerDeals**
```swift
    open class func bestbuyGetLaptopAndComputerDeals(page: Int? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get laptop and computer deals

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let page = 987 // Int |  (optional) (default to 1)

// Get laptop and computer deals
BestBuyAPI.bestbuyGetLaptopAndComputerDeals(page: page) { (response, error) in
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

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **bestbuyGetProductAvailability**
```swift
    open class func bestbuyGetProductAvailability(sku: String, zipCode: String, storeId: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get product availability

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let sku = "sku_example" // String | 
let zipCode = "zipCode_example" // String | 
let storeId = "storeId_example" // String |  (optional) (default to "7")

// Get product availability
BestBuyAPI.bestbuyGetProductAvailability(sku: sku, zipCode: zipCode, storeId: storeId) { (response, error) in
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
 **sku** | **String** |  | 
 **zipCode** | **String** |  | 
 **storeId** | **String** |  | [optional] [default to &quot;7&quot;]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **bestbuyGetProductDetail**
```swift
    open class func bestbuyGetProductDetail(sku: String, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get product detail

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let sku = "sku_example" // String | 

// Get product detail
BestBuyAPI.bestbuyGetProductDetail(sku: sku) { (response, error) in
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
 **sku** | **String** |  | 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **bestbuyGetProductQuestions**
```swift
    open class func bestbuyGetProductQuestions(sku: String, page: Int? = nil, pageSize: Int? = nil, query: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get product questions

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let sku = "sku_example" // String | 
let page = 987 // Int |  (optional) (default to 1)
let pageSize = 987 // Int |  (optional) (default to 10)
let query = "query_example" // String |  (optional) (default to "")

// Get product questions
BestBuyAPI.bestbuyGetProductQuestions(sku: sku, page: page, pageSize: pageSize, query: query) { (response, error) in
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
 **sku** | **String** |  | 
 **page** | **Int** |  | [optional] [default to 1]
 **pageSize** | **Int** |  | [optional] [default to 10]
 **query** | **String** |  | [optional] [default to &quot;&quot;]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **bestbuyGetProductReviews**
```swift
    open class func bestbuyGetProductReviews(sku: String, page: Int? = nil, pageSize: Int? = nil, sort: Sort_bestbuyGetProductReviews? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get product reviews

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let sku = "sku_example" // String | 
let page = 987 // Int |  (optional) (default to 1)
let pageSize = 987 // Int |  (optional) (default to 10)
let sort = "sort_example" // String |  (optional) (default to .mostRecent)

// Get product reviews
BestBuyAPI.bestbuyGetProductReviews(sku: sku, page: page, pageSize: pageSize, sort: sort) { (response, error) in
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
 **sku** | **String** |  | 
 **page** | **Int** |  | [optional] [default to 1]
 **pageSize** | **Int** |  | [optional] [default to 10]
 **sort** | **String** |  | [optional] [default to .mostRecent]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **bestbuyGetSearchSuggestions**
```swift
    open class func bestbuyGetSearchSuggestions(query: String, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get search suggestions

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let query = "query_example" // String | 

// Get search suggestions
BestBuyAPI.bestbuyGetSearchSuggestions(query: query) { (response, error) in
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

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **bestbuyListSupportedMarkets**
```swift
    open class func bestbuyListSupportedMarkets(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

List supported markets

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// List supported markets
BestBuyAPI.bestbuyListSupportedMarkets() { (response, error) in
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

# **bestbuySearchProducts**
```swift
    open class func bestbuySearchProducts(query: String, page: Int? = nil, sort: Sort_bestbuySearchProducts? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Search products

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let query = "query_example" // String | 
let page = 987 // Int |  (optional) (default to 1)
let sort = "sort_example" // String |  (optional) (default to .bestMatch)

// Search products
BestBuyAPI.bestbuySearchProducts(query: query, page: page, sort: sort) { (response, error) in
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
 **sort** | **String** |  | [optional] [default to .bestMatch]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

