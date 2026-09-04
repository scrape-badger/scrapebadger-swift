# EBayAPI

All URIs are relative to *https://scrapebadger.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**ebayBrowseACategory**](EBayAPI.md#ebaybrowseacategory) | **GET** /v1/ebay/categories/{category_id}/items | Browse a category
[**ebayCompletedSoldListings**](EBayAPI.md#ebaycompletedsoldlistings) | **GET** /v1/ebay/completed | Completed / sold listings
[**ebayEbayScraperHealthCheck**](EBayAPI.md#ebayebayscraperhealthcheck) | **GET** /v1/ebay/health | eBay scraper health check
[**ebayEbayScraperHealthCheckHead**](EBayAPI.md#ebayebayscraperhealthcheckhead) | **HEAD** /v1/ebay/health | eBay scraper health check
[**ebayGetItemDetail**](EBayAPI.md#ebaygetitemdetail) | **GET** /v1/ebay/items/{item_id} | Get item detail
[**ebayGetItemReviews**](EBayAPI.md#ebaygetitemreviews) | **GET** /v1/ebay/items/{item_id}/reviews | Get item reviews
[**ebayGetSellerFeedback**](EBayAPI.md#ebaygetsellerfeedback) | **GET** /v1/ebay/sellers/{username}/feedback | Get seller feedback
[**ebayGetSellerListings**](EBayAPI.md#ebaygetsellerlistings) | **GET** /v1/ebay/sellers/{username}/items | Get seller listings
[**ebayGetSellerProfile**](EBayAPI.md#ebaygetsellerprofile) | **GET** /v1/ebay/sellers/{username} | Get seller profile
[**ebayKeywordSuggestions**](EBayAPI.md#ebaykeywordsuggestions) | **GET** /v1/ebay/autocomplete | Keyword suggestions
[**ebayListCategories**](EBayAPI.md#ebaylistcategories) | **GET** /v1/ebay/categories | List categories
[**ebayListMarkets**](EBayAPI.md#ebaylistmarkets) | **GET** /v1/ebay/markets | List markets
[**ebaySearchListings**](EBayAPI.md#ebaysearchlistings) | **GET** /v1/ebay/search | Search listings


# **ebayBrowseACategory**
```swift
    open class func ebayBrowseACategory(categoryId: String, domain: String? = nil, page: Int? = nil, perPage: Int? = nil, sortBy: String? = nil, minPrice: Double? = nil, maxPrice: Double? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Browse a category

List active listings within an eBay category.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let categoryId = "categoryId_example" // String | 
let domain = "domain_example" // String |  (optional) (default to "com")
let page = 987 // Int |  (optional) (default to 1)
let perPage = 987 // Int |  (optional)
let sortBy = "sortBy_example" // String | best_match|ending_soonest|newly_listed|price_low_to_high|price_high_to_low (optional) (default to "best_match")
let minPrice = 987 // Double |  (optional)
let maxPrice = 987 // Double |  (optional)

// Browse a category
EBayAPI.ebayBrowseACategory(categoryId: categoryId, domain: domain, page: page, perPage: perPage, sortBy: sortBy, minPrice: minPrice, maxPrice: maxPrice) { (response, error) in
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
 **domain** | **String** |  | [optional] [default to &quot;com&quot;]
 **page** | **Int** |  | [optional] [default to 1]
 **perPage** | **Int** |  | [optional] 
 **sortBy** | **String** | best_match|ending_soonest|newly_listed|price_low_to_high|price_high_to_low | [optional] [default to &quot;best_match&quot;]
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

# **ebayCompletedSoldListings**
```swift
    open class func ebayCompletedSoldListings(query: String, domain: String? = nil, categoryId: String? = nil, page: Int? = nil, perPage: Int? = nil, sortBy: String? = nil, condition: String? = nil, minPrice: Double? = nil, maxPrice: Double? = nil, location: String? = nil, language: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Completed / sold listings

Search completed/sold listings — eBay's sold-price history.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let query = "query_example" // String | Search keywords
let domain = "domain_example" // String | Marketplace domain (com, co.uk, de …) (optional) (default to "com")
let categoryId = "categoryId_example" // String | Restrict to a category id (optional)
let page = 987 // Int |  (optional) (default to 1)
let perPage = 987 // Int | 60, 120 or 240 (optional)
let sortBy = "sortBy_example" // String | best_match|ending_soonest|newly_listed|price_low_to_high|price_high_to_low (optional) (default to "best_match")
let condition = "condition_example" // String | new|open_box|refurbished|used|for_parts|graded|ungraded (optional)
let minPrice = 987 // Double |  (optional)
let maxPrice = 987 // Double |  (optional)
let location = "location_example" // String | domestic|worldwide (optional)
let language = "language_example" // String | english|japanese|chinese|korean (optional)

// Completed / sold listings
EBayAPI.ebayCompletedSoldListings(query: query, domain: domain, categoryId: categoryId, page: page, perPage: perPage, sortBy: sortBy, condition: condition, minPrice: minPrice, maxPrice: maxPrice, location: location, language: language) { (response, error) in
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
 **query** | **String** | Search keywords | 
 **domain** | **String** | Marketplace domain (com, co.uk, de …) | [optional] [default to &quot;com&quot;]
 **categoryId** | **String** | Restrict to a category id | [optional] 
 **page** | **Int** |  | [optional] [default to 1]
 **perPage** | **Int** | 60, 120 or 240 | [optional] 
 **sortBy** | **String** | best_match|ending_soonest|newly_listed|price_low_to_high|price_high_to_low | [optional] [default to &quot;best_match&quot;]
 **condition** | **String** | new|open_box|refurbished|used|for_parts|graded|ungraded | [optional] 
 **minPrice** | **Double** |  | [optional] 
 **maxPrice** | **Double** |  | [optional] 
 **location** | **String** | domestic|worldwide | [optional] 
 **language** | **String** | english|japanese|chinese|korean | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **ebayEbayScraperHealthCheck**
```swift
    open class func ebayEbayScraperHealthCheck(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

eBay scraper health check

Check health of the eBay scraper service (accepts HEAD for UptimeRobot).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// eBay scraper health check
EBayAPI.ebayEbayScraperHealthCheck() { (response, error) in
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

# **ebayEbayScraperHealthCheckHead**
```swift
    open class func ebayEbayScraperHealthCheckHead(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

eBay scraper health check

Check health of the eBay scraper service (accepts HEAD for UptimeRobot).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// eBay scraper health check
EBayAPI.ebayEbayScraperHealthCheckHead() { (response, error) in
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

# **ebayGetItemDetail**
```swift
    open class func ebayGetItemDetail(itemId: String, domain: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get item detail

Get a single eBay listing's full detail.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let itemId = "itemId_example" // String | 
let domain = "domain_example" // String |  (optional) (default to "com")

// Get item detail
EBayAPI.ebayGetItemDetail(itemId: itemId, domain: domain) { (response, error) in
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
 **domain** | **String** |  | [optional] [default to &quot;com&quot;]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **ebayGetItemReviews**
```swift
    open class func ebayGetItemReviews(itemId: String, domain: String? = nil, page: Int? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get item reviews

Get catalog product reviews shown on an eBay listing.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let itemId = "itemId_example" // String | 
let domain = "domain_example" // String |  (optional) (default to "com")
let page = 987 // Int |  (optional) (default to 1)

// Get item reviews
EBayAPI.ebayGetItemReviews(itemId: itemId, domain: domain, page: page) { (response, error) in
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
 **domain** | **String** |  | [optional] [default to &quot;com&quot;]
 **page** | **Int** |  | [optional] [default to 1]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **ebayGetSellerFeedback**
```swift
    open class func ebayGetSellerFeedback(username: String, domain: String? = nil, page: Int? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get seller feedback

Get a seller's recent feedback comments.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let username = "username_example" // String | 
let domain = "domain_example" // String |  (optional) (default to "com")
let page = 987 // Int |  (optional) (default to 1)

// Get seller feedback
EBayAPI.ebayGetSellerFeedback(username: username, domain: domain, page: page) { (response, error) in
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
 **domain** | **String** |  | [optional] [default to &quot;com&quot;]
 **page** | **Int** |  | [optional] [default to 1]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **ebayGetSellerListings**
```swift
    open class func ebayGetSellerListings(username: String, domain: String? = nil, query: String? = nil, page: Int? = nil, perPage: Int? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get seller listings

List the active listings of a single eBay seller.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let username = "username_example" // String | 
let domain = "domain_example" // String |  (optional) (default to "com")
let query = "query_example" // String |  (optional)
let page = 987 // Int |  (optional) (default to 1)
let perPage = 987 // Int |  (optional)

// Get seller listings
EBayAPI.ebayGetSellerListings(username: username, domain: domain, query: query, page: page, perPage: perPage) { (response, error) in
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
 **domain** | **String** |  | [optional] [default to &quot;com&quot;]
 **query** | **String** |  | [optional] 
 **page** | **Int** |  | [optional] [default to 1]
 **perPage** | **Int** |  | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **ebayGetSellerProfile**
```swift
    open class func ebayGetSellerProfile(username: String, domain: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get seller profile

Get an eBay seller's public profile.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let username = "username_example" // String | 
let domain = "domain_example" // String |  (optional) (default to "com")

// Get seller profile
EBayAPI.ebayGetSellerProfile(username: username, domain: domain) { (response, error) in
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
 **domain** | **String** |  | [optional] [default to &quot;com&quot;]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **ebayKeywordSuggestions**
```swift
    open class func ebayKeywordSuggestions(query: String, domain: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Keyword suggestions

Return eBay keyword autocomplete suggestions.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let query = "query_example" // String | Partial query prefix
let domain = "domain_example" // String |  (optional) (default to "com")

// Keyword suggestions
EBayAPI.ebayKeywordSuggestions(query: query, domain: domain) { (response, error) in
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
 **query** | **String** | Partial query prefix | 
 **domain** | **String** |  | [optional] [default to &quot;com&quot;]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **ebayListCategories**
```swift
    open class func ebayListCategories(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

List categories

List eBay's top-level category ids.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// List categories
EBayAPI.ebayListCategories() { (response, error) in
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

# **ebayListMarkets**
```swift
    open class func ebayListMarkets(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

List markets

List all supported eBay marketplaces.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// List markets
EBayAPI.ebayListMarkets() { (response, error) in
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

# **ebaySearchListings**
```swift
    open class func ebaySearchListings(query: String, domain: String? = nil, categoryId: String? = nil, page: Int? = nil, perPage: Int? = nil, sortBy: String? = nil, condition: String? = nil, buyingFormat: String? = nil, minPrice: Double? = nil, maxPrice: Double? = nil, freeShipping: Bool? = nil, location: String? = nil, language: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Search listings

Search an eBay marketplace for active listings.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let query = "query_example" // String | Search keywords
let domain = "domain_example" // String | Marketplace domain (com, co.uk, de …) (optional) (default to "com")
let categoryId = "categoryId_example" // String | Restrict to a category id (optional)
let page = 987 // Int |  (optional) (default to 1)
let perPage = 987 // Int | 60, 120 or 240 (optional)
let sortBy = "sortBy_example" // String | best_match|ending_soonest|newly_listed|price_low_to_high|price_high_to_low (optional) (default to "best_match")
let condition = "condition_example" // String | new|open_box|refurbished|used|for_parts|graded|ungraded (optional)
let buyingFormat = "buyingFormat_example" // String | auction|buy_it_now|best_offer (optional)
let minPrice = 987 // Double |  (optional)
let maxPrice = 987 // Double |  (optional)
let freeShipping = true // Bool |  (optional) (default to false)
let location = "location_example" // String | domestic|worldwide (optional)
let language = "language_example" // String | english|japanese|chinese|korean (optional)

// Search listings
EBayAPI.ebaySearchListings(query: query, domain: domain, categoryId: categoryId, page: page, perPage: perPage, sortBy: sortBy, condition: condition, buyingFormat: buyingFormat, minPrice: minPrice, maxPrice: maxPrice, freeShipping: freeShipping, location: location, language: language) { (response, error) in
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
 **query** | **String** | Search keywords | 
 **domain** | **String** | Marketplace domain (com, co.uk, de …) | [optional] [default to &quot;com&quot;]
 **categoryId** | **String** | Restrict to a category id | [optional] 
 **page** | **Int** |  | [optional] [default to 1]
 **perPage** | **Int** | 60, 120 or 240 | [optional] 
 **sortBy** | **String** | best_match|ending_soonest|newly_listed|price_low_to_high|price_high_to_low | [optional] [default to &quot;best_match&quot;]
 **condition** | **String** | new|open_box|refurbished|used|for_parts|graded|ungraded | [optional] 
 **buyingFormat** | **String** | auction|buy_it_now|best_offer | [optional] 
 **minPrice** | **Double** |  | [optional] 
 **maxPrice** | **Double** |  | [optional] 
 **freeShipping** | **Bool** |  | [optional] [default to false]
 **location** | **String** | domestic|worldwide | [optional] 
 **language** | **String** | english|japanese|chinese|korean | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

