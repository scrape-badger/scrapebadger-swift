# VintedAPI

All URIs are relative to *https://scrapebadger.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**vintedGetItemDetails**](VintedAPI.md#vintedgetitemdetails) | **GET** /v1/vinted/items/{item_id} | Get item details
[**vintedGetUserProfile**](VintedAPI.md#vintedgetuserprofile) | **GET** /v1/vinted/users/{user_id} | Get user profile
[**vintedGetUserSListedItems**](VintedAPI.md#vintedgetuserslisteditems) | **GET** /v1/vinted/users/{user_id}/items | Get user&#39;s listed items
[**vintedListColors**](VintedAPI.md#vintedlistcolors) | **GET** /v1/vinted/colors | List colors
[**vintedListItemConditions**](VintedAPI.md#vintedlistitemconditions) | **GET** /v1/vinted/statuses | List item conditions
[**vintedListMarkets**](VintedAPI.md#vintedlistmarkets) | **GET** /v1/vinted/markets | List markets
[**vintedSearchBrands**](VintedAPI.md#vintedsearchbrands) | **GET** /v1/vinted/brands | Search brands
[**vintedSearchVintedItems**](VintedAPI.md#vintedsearchvinteditems) | **GET** /v1/vinted/search | Search Vinted items
[**vintedVintedScraperHealthCheck**](VintedAPI.md#vintedvintedscraperhealthcheck) | **GET** /v1/vinted/health | Vinted scraper health check
[**vintedVintedScraperHealthCheckHead**](VintedAPI.md#vintedvintedscraperhealthcheckhead) | **HEAD** /v1/vinted/health | Vinted scraper health check


# **vintedGetItemDetails**
```swift
    open class func vintedGetItemDetails(itemId: Int, market: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get item details

Get detailed information about a Vinted item.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let itemId = 987 // Int | 
let market = "market_example" // String |  (optional) (default to "fr")

// Get item details
VintedAPI.vintedGetItemDetails(itemId: itemId, market: market) { (response, error) in
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
 **itemId** | **Int** |  | 
 **market** | **String** |  | [optional] [default to &quot;fr&quot;]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **vintedGetUserProfile**
```swift
    open class func vintedGetUserProfile(userId: Int, market: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get user profile

Get a Vinted user's profile.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let userId = 987 // Int | 
let market = "market_example" // String |  (optional) (default to "fr")

// Get user profile
VintedAPI.vintedGetUserProfile(userId: userId, market: market) { (response, error) in
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
 **userId** | **Int** |  | 
 **market** | **String** |  | [optional] [default to &quot;fr&quot;]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **vintedGetUserSListedItems**
```swift
    open class func vintedGetUserSListedItems(userId: Int, market: String? = nil, page: Int? = nil, perPage: Int? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get user's listed items

Get items listed by a Vinted user.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let userId = 987 // Int | 
let market = "market_example" // String |  (optional) (default to "fr")
let page = 987 // Int |  (optional) (default to 1)
let perPage = 987 // Int |  (optional) (default to 20)

// Get user's listed items
VintedAPI.vintedGetUserSListedItems(userId: userId, market: market, page: page, perPage: perPage) { (response, error) in
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
 **userId** | **Int** |  | 
 **market** | **String** |  | [optional] [default to &quot;fr&quot;]
 **page** | **Int** |  | [optional] [default to 1]
 **perPage** | **Int** |  | [optional] [default to 20]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **vintedListColors**
```swift
    open class func vintedListColors(market: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

List colors

Get available Vinted colors for filtering.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let market = "market_example" // String |  (optional) (default to "fr")

// List colors
VintedAPI.vintedListColors(market: market) { (response, error) in
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
 **market** | **String** |  | [optional] [default to &quot;fr&quot;]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **vintedListItemConditions**
```swift
    open class func vintedListItemConditions(market: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

List item conditions

Get available item condition statuses.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let market = "market_example" // String |  (optional) (default to "fr")

// List item conditions
VintedAPI.vintedListItemConditions(market: market) { (response, error) in
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
 **market** | **String** |  | [optional] [default to &quot;fr&quot;]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **vintedListMarkets**
```swift
    open class func vintedListMarkets(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

List markets

List all supported Vinted markets.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// List markets
VintedAPI.vintedListMarkets() { (response, error) in
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

# **vintedSearchBrands**
```swift
    open class func vintedSearchBrands(keyword: String, market: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Search brands

Search Vinted brands.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let keyword = "keyword_example" // String | Brand search keyword
let market = "market_example" // String |  (optional) (default to "fr")

// Search brands
VintedAPI.vintedSearchBrands(keyword: keyword, market: market) { (response, error) in
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
 **keyword** | **String** | Brand search keyword | 
 **market** | **String** |  | [optional] [default to &quot;fr&quot;]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **vintedSearchVintedItems**
```swift
    open class func vintedSearchVintedItems(query: String, market: String? = nil, sellerCountry: String? = nil, page: Int? = nil, perPage: Int? = nil, priceFrom: Double? = nil, priceTo: Double? = nil, brandIds: String? = nil, catalogIds: String? = nil, colorIds: String? = nil, statusIds: String? = nil, order: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Search Vinted items

Search Vinted catalog items with filters.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let query = "query_example" // String | Search text
let market = "market_example" // String | Market code (optional) (default to "fr")
let sellerCountry = "sellerCountry_example" // String | Filter to items whose seller is physically located in one of these comma-separated ISO-2 country codes (e.g. 'fr' or 'fr,be'). Market domains federate cross-border EU listings and Vinted has no native country filter, so each item is enriched with its seller's country and non-matching ones are dropped. Adds 1 credit per uncached seller looked up (cached for 7 days). (optional)
let page = 987 // Int |  (optional) (default to 1)
let perPage = 987 // Int |  (optional) (default to 20)
let priceFrom = 987 // Double |  (optional)
let priceTo = 987 // Double |  (optional)
let brandIds = "brandIds_example" // String |  (optional)
let catalogIds = "catalogIds_example" // String | Comma-separated Vinted catalog (category) IDs to restrict the search to, e.g. '1904' or '1904,79'. Vinted applies this before searching, so pagination totals reflect the filtered set. A catalog ID is the `catalog[]` value in a Vinted category URL (vinted.fr/catalog?catalog[]=1904). (optional)
let colorIds = "colorIds_example" // String | Comma-separated color IDs (optional)
let statusIds = "statusIds_example" // String | Comma-separated condition/status IDs (optional)
let order = "order_example" // String |  (optional)

// Search Vinted items
VintedAPI.vintedSearchVintedItems(query: query, market: market, sellerCountry: sellerCountry, page: page, perPage: perPage, priceFrom: priceFrom, priceTo: priceTo, brandIds: brandIds, catalogIds: catalogIds, colorIds: colorIds, statusIds: statusIds, order: order) { (response, error) in
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
 **query** | **String** | Search text | 
 **market** | **String** | Market code | [optional] [default to &quot;fr&quot;]
 **sellerCountry** | **String** | Filter to items whose seller is physically located in one of these comma-separated ISO-2 country codes (e.g. &#39;fr&#39; or &#39;fr,be&#39;). Market domains federate cross-border EU listings and Vinted has no native country filter, so each item is enriched with its seller&#39;s country and non-matching ones are dropped. Adds 1 credit per uncached seller looked up (cached for 7 days). | [optional] 
 **page** | **Int** |  | [optional] [default to 1]
 **perPage** | **Int** |  | [optional] [default to 20]
 **priceFrom** | **Double** |  | [optional] 
 **priceTo** | **Double** |  | [optional] 
 **brandIds** | **String** |  | [optional] 
 **catalogIds** | **String** | Comma-separated Vinted catalog (category) IDs to restrict the search to, e.g. &#39;1904&#39; or &#39;1904,79&#39;. Vinted applies this before searching, so pagination totals reflect the filtered set. A catalog ID is the &#x60;catalog[]&#x60; value in a Vinted category URL (vinted.fr/catalog?catalog[]&#x3D;1904). | [optional] 
 **colorIds** | **String** | Comma-separated color IDs | [optional] 
 **statusIds** | **String** | Comma-separated condition/status IDs | [optional] 
 **order** | **String** |  | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **vintedVintedScraperHealthCheck**
```swift
    open class func vintedVintedScraperHealthCheck(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Vinted scraper health check

Check health of the Vinted scraper service.  Accepts ``HEAD`` so external uptime checkers (UptimeRobot uses HEAD by default for HTTP monitors) don't get a 405 Method Not Allowed.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// Vinted scraper health check
VintedAPI.vintedVintedScraperHealthCheck() { (response, error) in
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

# **vintedVintedScraperHealthCheckHead**
```swift
    open class func vintedVintedScraperHealthCheckHead(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Vinted scraper health check

Check health of the Vinted scraper service.  Accepts ``HEAD`` so external uptime checkers (UptimeRobot uses HEAD by default for HTTP monitors) don't get a 405 Method Not Allowed.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// Vinted scraper health check
VintedAPI.vintedVintedScraperHealthCheckHead() { (response, error) in
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

