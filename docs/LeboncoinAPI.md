# LeboncoinAPI

All URIs are relative to *https://scrapebadger.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**leboncoinGetASellerSAds**](LeboncoinAPI.md#leboncoingetasellersads) | **GET** /v1/leboncoin/sellers/{user_id}/listings | Get a seller&#39;s ads
[**leboncoinGetAdDetail**](LeboncoinAPI.md#leboncoingetaddetail) | **GET** /v1/leboncoin/ads/{list_id} | Get ad detail
[**leboncoinGetSellerProfile**](LeboncoinAPI.md#leboncoingetsellerprofile) | **GET** /v1/leboncoin/sellers/{user_id} | Get seller profile
[**leboncoinGetSimilarAds**](LeboncoinAPI.md#leboncoingetsimilarads) | **GET** /v1/leboncoin/ads/{list_id}/similar | Get similar ads
[**leboncoinLeboncoinScraperHealthCheck**](LeboncoinAPI.md#leboncoinleboncoinscraperhealthcheck) | **GET** /v1/leboncoin/health | Leboncoin scraper health check
[**leboncoinLeboncoinScraperHealthCheckHead**](LeboncoinAPI.md#leboncoinleboncoinscraperhealthcheckhead) | **HEAD** /v1/leboncoin/health | Leboncoin scraper health check
[**leboncoinListCategories**](LeboncoinAPI.md#leboncoinlistcategories) | **GET** /v1/leboncoin/categories | List categories
[**leboncoinListDepartments**](LeboncoinAPI.md#leboncoinlistdepartments) | **GET** /v1/leboncoin/departments | List departments
[**leboncoinListMarkets**](LeboncoinAPI.md#leboncoinlistmarkets) | **GET** /v1/leboncoin/markets | List markets
[**leboncoinListRegions**](LeboncoinAPI.md#leboncoinlistregions) | **GET** /v1/leboncoin/regions | List regions
[**leboncoinLocationAutocomplete**](LeboncoinAPI.md#leboncoinlocationautocomplete) | **GET** /v1/leboncoin/locations/search | Location autocomplete
[**leboncoinSearchLeboncoinAds**](LeboncoinAPI.md#leboncoinsearchleboncoinads) | **GET** /v1/leboncoin/search | Search Leboncoin ads


# **leboncoinGetASellerSAds**
```swift
    open class func leboncoinGetASellerSAds(userId: String, page: Int? = nil, limit: Int? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get a seller's ads

A seller's active ads.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let userId = "userId_example" // String | 
let page = 987 // Int |  (optional) (default to 1)
let limit = 987 // Int |  (optional) (default to 35)

// Get a seller's ads
LeboncoinAPI.leboncoinGetASellerSAds(userId: userId, page: page, limit: limit) { (response, error) in
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
 **page** | **Int** |  | [optional] [default to 1]
 **limit** | **Int** |  | [optional] [default to 35]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **leboncoinGetAdDetail**
```swift
    open class func leboncoinGetAdDetail(listId: Int, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get ad detail

Full detail for a Leboncoin ad.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let listId = 987 // Int | 

// Get ad detail
LeboncoinAPI.leboncoinGetAdDetail(listId: listId) { (response, error) in
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
 **listId** | **Int** |  | 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **leboncoinGetSellerProfile**
```swift
    open class func leboncoinGetSellerProfile(userId: String, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get seller profile

Public seller/pro-store profile.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let userId = "userId_example" // String | 

// Get seller profile
LeboncoinAPI.leboncoinGetSellerProfile(userId: userId) { (response, error) in
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

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **leboncoinGetSimilarAds**
```swift
    open class func leboncoinGetSimilarAds(listId: Int, limit: Int? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get similar ads

Ads Leboncoin surfaces as similar to the given ad.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let listId = 987 // Int | 
let limit = 987 // Int |  (optional) (default to 20)

// Get similar ads
LeboncoinAPI.leboncoinGetSimilarAds(listId: listId, limit: limit) { (response, error) in
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
 **listId** | **Int** |  | 
 **limit** | **Int** |  | [optional] [default to 20]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **leboncoinLeboncoinScraperHealthCheck**
```swift
    open class func leboncoinLeboncoinScraperHealthCheck(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Leboncoin scraper health check

Check health of the Leboncoin scraper service (accepts HEAD).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// Leboncoin scraper health check
LeboncoinAPI.leboncoinLeboncoinScraperHealthCheck() { (response, error) in
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

# **leboncoinLeboncoinScraperHealthCheckHead**
```swift
    open class func leboncoinLeboncoinScraperHealthCheckHead(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Leboncoin scraper health check

Check health of the Leboncoin scraper service (accepts HEAD).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// Leboncoin scraper health check
LeboncoinAPI.leboncoinLeboncoinScraperHealthCheckHead() { (response, error) in
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

# **leboncoinListCategories**
```swift
    open class func leboncoinListCategories(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

List categories

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// List categories
LeboncoinAPI.leboncoinListCategories() { (response, error) in
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

# **leboncoinListDepartments**
```swift
    open class func leboncoinListDepartments(regionId: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

List departments

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let regionId = "regionId_example" // String |  (optional)

// List departments
LeboncoinAPI.leboncoinListDepartments(regionId: regionId) { (response, error) in
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
 **regionId** | **String** |  | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **leboncoinListMarkets**
```swift
    open class func leboncoinListMarkets(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

List markets

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// List markets
LeboncoinAPI.leboncoinListMarkets() { (response, error) in
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

# **leboncoinListRegions**
```swift
    open class func leboncoinListRegions(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

List regions

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// List regions
LeboncoinAPI.leboncoinListRegions() { (response, error) in
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

# **leboncoinLocationAutocomplete**
```swift
    open class func leboncoinLocationAutocomplete(q: String, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Location autocomplete

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let q = "q_example" // String | Place name

// Location autocomplete
LeboncoinAPI.leboncoinLocationAutocomplete(q: q) { (response, error) in
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
 **q** | **String** | Place name | 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **leboncoinSearchLeboncoinAds**
```swift
    open class func leboncoinSearchLeboncoinAds(text: String? = nil, category: String? = nil, regionId: String? = nil, departmentId: String? = nil, city: String? = nil, zipcode: String? = nil, priceMin: Int? = nil, priceMax: Int? = nil, ownerType: String? = nil, adType: String? = nil, sort: String? = nil, page: Int? = nil, limit: Int? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Search Leboncoin ads

Search Leboncoin classifieds (France; scope by region/department/city).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let text = "text_example" // String | Free-text query (optional)
let category = "category_example" // String | Category id (see /categories) (optional)
let regionId = "regionId_example" // String | Region id (see /regions) (optional)
let departmentId = "departmentId_example" // String | Department id, e.g. 75 (optional)
let city = "city_example" // String |  (optional)
let zipcode = "zipcode_example" // String |  (optional)
let priceMin = 987 // Int |  (optional)
let priceMax = 987 // Int |  (optional)
let ownerType = "ownerType_example" // String | all | pro | private (optional) (default to "all")
let adType = "adType_example" // String | offer | demand (optional) (default to "offer")
let sort = "sort_example" // String | relevance|newest|oldest|price_low|price_high (optional) (default to "relevance")
let page = 987 // Int |  (optional) (default to 1)
let limit = 987 // Int |  (optional) (default to 35)

// Search Leboncoin ads
LeboncoinAPI.leboncoinSearchLeboncoinAds(text: text, category: category, regionId: regionId, departmentId: departmentId, city: city, zipcode: zipcode, priceMin: priceMin, priceMax: priceMax, ownerType: ownerType, adType: adType, sort: sort, page: page, limit: limit) { (response, error) in
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
 **text** | **String** | Free-text query | [optional] 
 **category** | **String** | Category id (see /categories) | [optional] 
 **regionId** | **String** | Region id (see /regions) | [optional] 
 **departmentId** | **String** | Department id, e.g. 75 | [optional] 
 **city** | **String** |  | [optional] 
 **zipcode** | **String** |  | [optional] 
 **priceMin** | **Int** |  | [optional] 
 **priceMax** | **Int** |  | [optional] 
 **ownerType** | **String** | all | pro | private | [optional] [default to &quot;all&quot;]
 **adType** | **String** | offer | demand | [optional] [default to &quot;offer&quot;]
 **sort** | **String** | relevance|newest|oldest|price_low|price_high | [optional] [default to &quot;relevance&quot;]
 **page** | **Int** |  | [optional] [default to 1]
 **limit** | **Int** |  | [optional] [default to 35]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

