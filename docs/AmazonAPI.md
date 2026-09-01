# AmazonAPI

All URIs are relative to *https://scrapebadger.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**amazonAmazonScraperHealthCheck**](AmazonAPI.md#amazonamazonscraperhealthcheck) | **GET** /v1/amazon/health | Amazon scraper health check
[**amazonAmazonScraperHealthCheckHead**](AmazonAPI.md#amazonamazonscraperhealthcheckhead) | **HEAD** /v1/amazon/health | Amazon scraper health check
[**amazonBestsellersByCategory**](AmazonAPI.md#amazonbestsellersbycategory) | **GET** /v1/amazon/bestsellers | Bestsellers by category
[**amazonBrowseNodeCategoryListing**](AmazonAPI.md#amazonbrowsenodecategorylisting) | **GET** /v1/amazon/category | Browse-node category listing
[**amazonGetAllSellerOffersBuybox**](AmazonAPI.md#amazongetallselleroffersbuybox) | **GET** /v1/amazon/products/{asin}/offers | Get all seller offers (buybox)
[**amazonGetProductDetail**](AmazonAPI.md#amazongetproductdetail) | **GET** /v1/amazon/products/{asin} | Get product detail
[**amazonGetProductReviews**](AmazonAPI.md#amazongetproductreviews) | **GET** /v1/amazon/products/{asin}/reviews | Get product reviews
[**amazonGetSellerFeedback**](AmazonAPI.md#amazongetsellerfeedback) | **GET** /v1/amazon/sellers/{seller_id}/feedback | Get seller feedback
[**amazonGetSellerProfile**](AmazonAPI.md#amazongetsellerprofile) | **GET** /v1/amazon/sellers/{seller_id} | Get seller profile
[**amazonGetSellerStorefrontProducts**](AmazonAPI.md#amazongetsellerstorefrontproducts) | **GET** /v1/amazon/sellers/{seller_id}/products | Get seller storefront products
[**amazonKeywordSuggestions**](AmazonAPI.md#amazonkeywordsuggestions) | **GET** /v1/amazon/autocomplete | Keyword suggestions
[**amazonListCategoryAliases**](AmazonAPI.md#amazonlistcategoryaliases) | **GET** /v1/amazon/categories | List category aliases
[**amazonListMarketplaces**](AmazonAPI.md#amazonlistmarketplaces) | **GET** /v1/amazon/markets | List marketplaces
[**amazonNewReleasesByCategory**](AmazonAPI.md#amazonnewreleasesbycategory) | **GET** /v1/amazon/new-releases | New releases by category
[**amazonSearchAmazonProducts**](AmazonAPI.md#amazonsearchamazonproducts) | **GET** /v1/amazon/search | Search Amazon products
[**amazonTodaySDeals**](AmazonAPI.md#amazontodaysdeals) | **GET** /v1/amazon/deals | Today&#39;s deals


# **amazonAmazonScraperHealthCheck**
```swift
    open class func amazonAmazonScraperHealthCheck(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Amazon scraper health check

Check health of the Amazon scraper service (accepts HEAD for UptimeRobot).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// Amazon scraper health check
AmazonAPI.amazonAmazonScraperHealthCheck() { (response, error) in
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

# **amazonAmazonScraperHealthCheckHead**
```swift
    open class func amazonAmazonScraperHealthCheckHead(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Amazon scraper health check

Check health of the Amazon scraper service (accepts HEAD for UptimeRobot).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// Amazon scraper health check
AmazonAPI.amazonAmazonScraperHealthCheckHead() { (response, error) in
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

# **amazonBestsellersByCategory**
```swift
    open class func amazonBestsellersByCategory(domain: String? = nil, category: String? = nil, page: Int? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Bestsellers by category

Top-selling products for a category (browse node).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let domain = "domain_example" // String |  (optional) (default to "com")
let category = "category_example" // String | Bestsellers node id or slug (optional)
let page = 987 // Int |  (optional) (default to 1)

// Bestsellers by category
AmazonAPI.amazonBestsellersByCategory(domain: domain, category: category, page: page) { (response, error) in
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
 **domain** | **String** |  | [optional] [default to &quot;com&quot;]
 **category** | **String** | Bestsellers node id or slug | [optional] 
 **page** | **Int** |  | [optional] [default to 1]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **amazonBrowseNodeCategoryListing**
```swift
    open class func amazonBrowseNodeCategoryListing(node: String, domain: String? = nil, page: Int? = nil, sortBy: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Browse-node category listing

List products within an Amazon browse-node category.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let node = "node_example" // String | Amazon browse-node id
let domain = "domain_example" // String |  (optional) (default to "com")
let page = 987 // Int |  (optional) (default to 1)
let sortBy = "sortBy_example" // String |  (optional)

// Browse-node category listing
AmazonAPI.amazonBrowseNodeCategoryListing(node: node, domain: domain, page: page, sortBy: sortBy) { (response, error) in
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
 **node** | **String** | Amazon browse-node id | 
 **domain** | **String** |  | [optional] [default to &quot;com&quot;]
 **page** | **Int** |  | [optional] [default to 1]
 **sortBy** | **String** |  | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **amazonGetAllSellerOffersBuybox**
```swift
    open class func amazonGetAllSellerOffersBuybox(asin: String, domain: String? = nil, zip: String? = nil, page: Int? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get all seller offers (buybox)

All third-party offers for an ASIN, including the Buy Box winner.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let asin = "asin_example" // String | 
let domain = "domain_example" // String |  (optional) (default to "com")
let zip = "zip_example" // String |  (optional)
let page = 987 // Int | Offer page, 10 rows each (optional) (default to 1)

// Get all seller offers (buybox)
AmazonAPI.amazonGetAllSellerOffersBuybox(asin: asin, domain: domain, zip: zip, page: page) { (response, error) in
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
 **asin** | **String** |  | 
 **domain** | **String** |  | [optional] [default to &quot;com&quot;]
 **zip** | **String** |  | [optional] 
 **page** | **Int** | Offer page, 10 rows each | [optional] [default to 1]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **amazonGetProductDetail**
```swift
    open class func amazonGetProductDetail(asin: String, domain: String? = nil, zip: String? = nil, language: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get product detail

Full product detail by ASIN (price, variants, badges, buybox, ranks…).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let asin = "asin_example" // String | 
let domain = "domain_example" // String |  (optional) (default to "com")
let zip = "zip_example" // String | Delivery postal/zip for localized buybox (optional)
let language = "language_example" // String |  (optional)

// Get product detail
AmazonAPI.amazonGetProductDetail(asin: asin, domain: domain, zip: zip, language: language) { (response, error) in
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
 **asin** | **String** |  | 
 **domain** | **String** |  | [optional] [default to &quot;com&quot;]
 **zip** | **String** | Delivery postal/zip for localized buybox | [optional] 
 **language** | **String** |  | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **amazonGetProductReviews**
```swift
    open class func amazonGetProductReviews(asin: String, domain: String? = nil, page: Int? = nil, sortBy: String? = nil, star: String? = nil, verifiedOnly: Bool? = nil, mediaOnly: Bool? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get product reviews

Customer reviews for an ASIN (featured + paginated, with filters).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let asin = "asin_example" // String | 
let domain = "domain_example" // String |  (optional) (default to "com")
let page = 987 // Int | Review page (1-100, ~10 reviews/page) (optional) (default to 1)
let sortBy = "sortBy_example" // String | helpful | recent (optional) (default to "helpful")
let star = "star_example" // String | one_star..five_star | positive | critical (optional)
let verifiedOnly = true // Bool |  (optional) (default to false)
let mediaOnly = true // Bool |  (optional) (default to false)

// Get product reviews
AmazonAPI.amazonGetProductReviews(asin: asin, domain: domain, page: page, sortBy: sortBy, star: star, verifiedOnly: verifiedOnly, mediaOnly: mediaOnly) { (response, error) in
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
 **asin** | **String** |  | 
 **domain** | **String** |  | [optional] [default to &quot;com&quot;]
 **page** | **Int** | Review page (1-100, ~10 reviews/page) | [optional] [default to 1]
 **sortBy** | **String** | helpful | recent | [optional] [default to &quot;helpful&quot;]
 **star** | **String** | one_star..five_star | positive | critical | [optional] 
 **verifiedOnly** | **Bool** |  | [optional] [default to false]
 **mediaOnly** | **Bool** |  | [optional] [default to false]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **amazonGetSellerFeedback**
```swift
    open class func amazonGetSellerFeedback(sellerId: String, domain: String? = nil, page: Int? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get seller feedback

Buyer feedback entries for a seller.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let sellerId = "sellerId_example" // String | 
let domain = "domain_example" // String |  (optional) (default to "com")
let page = 987 // Int |  (optional) (default to 1)

// Get seller feedback
AmazonAPI.amazonGetSellerFeedback(sellerId: sellerId, domain: domain, page: page) { (response, error) in
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
 **sellerId** | **String** |  | 
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

# **amazonGetSellerProfile**
```swift
    open class func amazonGetSellerProfile(sellerId: String, domain: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get seller profile

Seller profile, ratings and feedback summary.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let sellerId = "sellerId_example" // String | 
let domain = "domain_example" // String |  (optional) (default to "com")

// Get seller profile
AmazonAPI.amazonGetSellerProfile(sellerId: sellerId, domain: domain) { (response, error) in
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
 **sellerId** | **String** |  | 
 **domain** | **String** |  | [optional] [default to &quot;com&quot;]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **amazonGetSellerStorefrontProducts**
```swift
    open class func amazonGetSellerStorefrontProducts(sellerId: String, domain: String? = nil, page: Int? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get seller storefront products

Products listed in a seller's storefront.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let sellerId = "sellerId_example" // String | 
let domain = "domain_example" // String |  (optional) (default to "com")
let page = 987 // Int |  (optional) (default to 1)

// Get seller storefront products
AmazonAPI.amazonGetSellerStorefrontProducts(sellerId: sellerId, domain: domain, page: page) { (response, error) in
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
 **sellerId** | **String** |  | 
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

# **amazonKeywordSuggestions**
```swift
    open class func amazonKeywordSuggestions(query: String, domain: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Keyword suggestions

Get Amazon search autocomplete suggestions for keyword research.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let query = "query_example" // String | Partial search term
let domain = "domain_example" // String |  (optional) (default to "com")

// Keyword suggestions
AmazonAPI.amazonKeywordSuggestions(query: query, domain: domain) { (response, error) in
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
 **query** | **String** | Partial search term | 
 **domain** | **String** |  | [optional] [default to &quot;com&quot;]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **amazonListCategoryAliases**
```swift
    open class func amazonListCategoryAliases(domain: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

List category aliases

List common Amazon department/category aliases and bestseller nodes.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let domain = "domain_example" // String |  (optional) (default to "com")

// List category aliases
AmazonAPI.amazonListCategoryAliases(domain: domain) { (response, error) in
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
 **domain** | **String** |  | [optional] [default to &quot;com&quot;]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **amazonListMarketplaces**
```swift
    open class func amazonListMarketplaces(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

List marketplaces

List all supported Amazon marketplaces.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// List marketplaces
AmazonAPI.amazonListMarketplaces() { (response, error) in
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

# **amazonNewReleasesByCategory**
```swift
    open class func amazonNewReleasesByCategory(domain: String? = nil, category: String? = nil, page: Int? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

New releases by category

Newly released products for a category (browse node).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let domain = "domain_example" // String |  (optional) (default to "com")
let category = "category_example" // String |  (optional)
let page = 987 // Int |  (optional) (default to 1)

// New releases by category
AmazonAPI.amazonNewReleasesByCategory(domain: domain, category: category, page: page) { (response, error) in
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
 **domain** | **String** |  | [optional] [default to &quot;com&quot;]
 **category** | **String** |  | [optional] 
 **page** | **Int** |  | [optional] [default to 1]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **amazonSearchAmazonProducts**
```swift
    open class func amazonSearchAmazonProducts(query: String, domain: String? = nil, page: Int? = nil, sortBy: String? = nil, category: String? = nil, minPrice: Double? = nil, maxPrice: Double? = nil, zip: String? = nil, language: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Search Amazon products

Search the Amazon catalog with filters and sorting.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let query = "query_example" // String | Search keywords
let domain = "domain_example" // String | Amazon marketplace TLD or code (com, co.uk, de…) (optional) (default to "com")
let page = 987 // Int |  (optional) (default to 1)
let sortBy = "sortBy_example" // String | relevance | price_low_to_high | price_high_to_low | avg_review | newest (optional)
let category = "category_example" // String | Department/category alias (i= param) (optional)
let minPrice = 987 // Double |  (optional)
let maxPrice = 987 // Double |  (optional)
let zip = "zip_example" // String | Delivery postal/zip code for localized pricing (optional)
let language = "language_example" // String | Locale for results, e.g. en_US, fr_FR (optional)

// Search Amazon products
AmazonAPI.amazonSearchAmazonProducts(query: query, domain: domain, page: page, sortBy: sortBy, category: category, minPrice: minPrice, maxPrice: maxPrice, zip: zip, language: language) { (response, error) in
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
 **domain** | **String** | Amazon marketplace TLD or code (com, co.uk, de…) | [optional] [default to &quot;com&quot;]
 **page** | **Int** |  | [optional] [default to 1]
 **sortBy** | **String** | relevance | price_low_to_high | price_high_to_low | avg_review | newest | [optional] 
 **category** | **String** | Department/category alias (i&#x3D; param) | [optional] 
 **minPrice** | **Double** |  | [optional] 
 **maxPrice** | **Double** |  | [optional] 
 **zip** | **String** | Delivery postal/zip code for localized pricing | [optional] 
 **language** | **String** | Locale for results, e.g. en_US, fr_FR | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **amazonTodaySDeals**
```swift
    open class func amazonTodaySDeals(domain: String? = nil, category: String? = nil, page: Int? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Today's deals

Current Amazon deals (lightning deals, best deals).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let domain = "domain_example" // String |  (optional) (default to "com")
let category = "category_example" // String |  (optional)
let page = 987 // Int |  (optional) (default to 1)

// Today's deals
AmazonAPI.amazonTodaySDeals(domain: domain, category: category, page: page) { (response, error) in
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
 **domain** | **String** |  | [optional] [default to &quot;com&quot;]
 **category** | **String** |  | [optional] 
 **page** | **Int** |  | [optional] [default to 1]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

