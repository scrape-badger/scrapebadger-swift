# TargetAPI

All URIs are relative to *https://scrapebadger.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**targetBrowseACategory**](TargetAPI.md#targetbrowseacategory) | **GET** /v1/target/category | Browse a category
[**targetFindNearbyStores**](TargetAPI.md#targetfindnearbystores) | **GET** /v1/target/stores | Find nearby stores
[**targetGetCategories**](TargetAPI.md#targetgetcategories) | **GET** /v1/target/categories | Get categories
[**targetGetProductAvailability**](TargetAPI.md#targetgetproductavailability) | **GET** /v1/target/products/{tcin}/availability | Get product availability
[**targetGetProductDetail**](TargetAPI.md#targetgetproductdetail) | **GET** /v1/target/products/{tcin} | Get product detail
[**targetGetProductQuestions**](TargetAPI.md#targetgetproductquestions) | **GET** /v1/target/products/{tcin}/questions | Get product questions
[**targetGetProductReviews**](TargetAPI.md#targetgetproductreviews) | **GET** /v1/target/products/{tcin}/reviews | Get product reviews
[**targetGetSearchSuggestions**](TargetAPI.md#targetgetsearchsuggestions) | **GET** /v1/target/autocomplete | Get search suggestions
[**targetGetStoreDetail**](TargetAPI.md#targetgetstoredetail) | **GET** /v1/target/stores/{store_id} | Get store detail
[**targetListSupportedMarkets**](TargetAPI.md#targetlistsupportedmarkets) | **GET** /v1/target/markets | List supported markets
[**targetSearchProducts**](TargetAPI.md#targetsearchproducts) | **GET** /v1/target/search | Search products


# **targetBrowseACategory**
```swift
    open class func targetBrowseACategory(categoryId: String, page: Int? = nil, pageSize: Int? = nil, storeId: String? = nil, zipCode: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Browse a category

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let categoryId = "categoryId_example" // String | 
let page = 987 // Int |  (optional) (default to 1)
let pageSize = 987 // Int |  (optional) (default to 24)
let storeId = "storeId_example" // String |  (optional) (default to "1375")
let zipCode = "zipCode_example" // String |  (optional) (default to "55403")

// Browse a category
TargetAPI.targetBrowseACategory(categoryId: categoryId, page: page, pageSize: pageSize, storeId: storeId, zipCode: zipCode) { (response, error) in
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
 **pageSize** | **Int** |  | [optional] [default to 24]
 **storeId** | **String** |  | [optional] [default to &quot;1375&quot;]
 **zipCode** | **String** |  | [optional] [default to &quot;55403&quot;]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **targetFindNearbyStores**
```swift
    open class func targetFindNearbyStores(zipCode: String, limit: Int? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Find nearby stores

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let zipCode = "zipCode_example" // String | 
let limit = 987 // Int |  (optional) (default to 10)

// Find nearby stores
TargetAPI.targetFindNearbyStores(zipCode: zipCode, limit: limit) { (response, error) in
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
 **zipCode** | **String** |  | 
 **limit** | **Int** |  | [optional] [default to 10]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **targetGetCategories**
```swift
    open class func targetGetCategories(categoryId: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get categories

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let categoryId = "categoryId_example" // String |  (optional) (default to "5xtly")

// Get categories
TargetAPI.targetGetCategories(categoryId: categoryId) { (response, error) in
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
 **categoryId** | **String** |  | [optional] [default to &quot;5xtly&quot;]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **targetGetProductAvailability**
```swift
    open class func targetGetProductAvailability(tcin: String, zipCode: String, limit: Int? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get product availability

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let tcin = "tcin_example" // String | 
let zipCode = "zipCode_example" // String | 
let limit = 987 // Int |  (optional) (default to 10)

// Get product availability
TargetAPI.targetGetProductAvailability(tcin: tcin, zipCode: zipCode, limit: limit) { (response, error) in
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
 **tcin** | **String** |  | 
 **zipCode** | **String** |  | 
 **limit** | **Int** |  | [optional] [default to 10]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **targetGetProductDetail**
```swift
    open class func targetGetProductDetail(tcin: String, storeId: String? = nil, zipCode: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get product detail

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let tcin = "tcin_example" // String | 
let storeId = "storeId_example" // String |  (optional) (default to "1375")
let zipCode = "zipCode_example" // String |  (optional) (default to "55403")

// Get product detail
TargetAPI.targetGetProductDetail(tcin: tcin, storeId: storeId, zipCode: zipCode) { (response, error) in
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
 **tcin** | **String** |  | 
 **storeId** | **String** |  | [optional] [default to &quot;1375&quot;]
 **zipCode** | **String** |  | [optional] [default to &quot;55403&quot;]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **targetGetProductQuestions**
```swift
    open class func targetGetProductQuestions(tcin: String, page: Int? = nil, pageSize: Int? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get product questions

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let tcin = "tcin_example" // String | 
let page = 987 // Int |  (optional) (default to 1)
let pageSize = 987 // Int |  (optional) (default to 10)

// Get product questions
TargetAPI.targetGetProductQuestions(tcin: tcin, page: page, pageSize: pageSize) { (response, error) in
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
 **tcin** | **String** |  | 
 **page** | **Int** |  | [optional] [default to 1]
 **pageSize** | **Int** |  | [optional] [default to 10]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **targetGetProductReviews**
```swift
    open class func targetGetProductReviews(tcin: String, page: Int? = nil, pageSize: Int? = nil, sort: Sort_targetGetProductReviews? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get product reviews

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let tcin = "tcin_example" // String | 
let page = 987 // Int |  (optional) (default to 1)
let pageSize = 987 // Int |  (optional) (default to 10)
let sort = "sort_example" // String |  (optional) (default to .mostRecent)

// Get product reviews
TargetAPI.targetGetProductReviews(tcin: tcin, page: page, pageSize: pageSize, sort: sort) { (response, error) in
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
 **tcin** | **String** |  | 
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

# **targetGetSearchSuggestions**
```swift
    open class func targetGetSearchSuggestions(query: String, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get search suggestions

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let query = "query_example" // String | 

// Get search suggestions
TargetAPI.targetGetSearchSuggestions(query: query) { (response, error) in
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

# **targetGetStoreDetail**
```swift
    open class func targetGetStoreDetail(storeId: String, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get store detail

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let storeId = "storeId_example" // String | 

// Get store detail
TargetAPI.targetGetStoreDetail(storeId: storeId) { (response, error) in
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

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **targetListSupportedMarkets**
```swift
    open class func targetListSupportedMarkets(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

List supported markets

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// List supported markets
TargetAPI.targetListSupportedMarkets() { (response, error) in
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

# **targetSearchProducts**
```swift
    open class func targetSearchProducts(query: String, page: Int? = nil, pageSize: Int? = nil, storeId: String? = nil, zipCode: String? = nil, sort: Sort_targetSearchProducts? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Search products

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let query = "query_example" // String | 
let page = 987 // Int |  (optional) (default to 1)
let pageSize = 987 // Int |  (optional) (default to 24)
let storeId = "storeId_example" // String |  (optional) (default to "1375")
let zipCode = "zipCode_example" // String |  (optional) (default to "55403")
let sort = "sort_example" // String |  (optional) (default to .relevance)

// Search products
TargetAPI.targetSearchProducts(query: query, page: page, pageSize: pageSize, storeId: storeId, zipCode: zipCode, sort: sort) { (response, error) in
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
 **pageSize** | **Int** |  | [optional] [default to 24]
 **storeId** | **String** |  | [optional] [default to &quot;1375&quot;]
 **zipCode** | **String** |  | [optional] [default to &quot;55403&quot;]
 **sort** | **String** |  | [optional] [default to .relevance]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

