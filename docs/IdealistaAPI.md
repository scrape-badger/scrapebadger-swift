# IdealistaAPI

All URIs are relative to *https://scrapebadger.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**idealistaAgencyByPhone**](IdealistaAPI.md#idealistaagencybyphone) | **GET** /v1/idealista/agency/by-phone/{phone} | Agency by phone
[**idealistaAgencyProfileListings**](IdealistaAPI.md#idealistaagencyprofilelistings) | **GET** /v1/idealista/agency/{short_name} | Agency profile + listings
[**idealistaGetListingEngagementStats**](IdealistaAPI.md#idealistagetlistingengagementstats) | **GET** /v1/idealista/properties/{property_code}/stats | Get listing engagement stats
[**idealistaGetPropertyDetail**](IdealistaAPI.md#idealistagetpropertydetail) | **GET** /v1/idealista/properties/{property_code} | Get property detail
[**idealistaIdealistaScraperHealthCheck**](IdealistaAPI.md#idealistaidealistascraperhealthcheck) | **GET** /v1/idealista/health | Idealista scraper health check
[**idealistaIdealistaScraperHealthCheckHead**](IdealistaAPI.md#idealistaidealistascraperhealthcheckhead) | **HEAD** /v1/idealista/health | Idealista scraper health check
[**idealistaListMarkets**](IdealistaAPI.md#idealistalistmarkets) | **GET** /v1/idealista/markets | List markets
[**idealistaResolveLocations**](IdealistaAPI.md#idealistaresolvelocations) | **GET** /v1/idealista/suggest | Resolve locations
[**idealistaSearchAllBeatsResultCap**](IdealistaAPI.md#idealistasearchallbeatsresultcap) | **GET** /v1/idealista/search/all | Search all (beats result cap)
[**idealistaSearchListings**](IdealistaAPI.md#idealistasearchlistings) | **GET** /v1/idealista/search | Search listings


# **idealistaAgencyByPhone**
```swift
    open class func idealistaAgencyByPhone(phone: String, market: String? = nil, operation: String? = nil, propertyType: String? = nil, page: Int? = nil, maxItems: Int? = nil, includeListings: Bool? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Agency by phone

Reverse-lookup the agency behind a contact phone (national number), with its listings.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let phone = "phone_example" // String | 
let market = "market_example" // String | es|it|pt (optional) (default to "es")
let operation = "operation_example" // String | sale|rent (optional)
let propertyType = "propertyType_example" // String | homes|offices|premises|garages|newDevelopments|lands|storageRooms|buildings|bedrooms (optional)
let page = 987 // Int |  (optional) (default to 1)
let maxItems = 987 // Int |  (optional) (default to 30)
let includeListings = true // Bool |  (optional) (default to true)

// Agency by phone
IdealistaAPI.idealistaAgencyByPhone(phone: phone, market: market, operation: operation, propertyType: propertyType, page: page, maxItems: maxItems, includeListings: includeListings) { (response, error) in
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
 **phone** | **String** |  | 
 **market** | **String** | es|it|pt | [optional] [default to &quot;es&quot;]
 **operation** | **String** | sale|rent | [optional] 
 **propertyType** | **String** | homes|offices|premises|garages|newDevelopments|lands|storageRooms|buildings|bedrooms | [optional] 
 **page** | **Int** |  | [optional] [default to 1]
 **maxItems** | **Int** |  | [optional] [default to 30]
 **includeListings** | **Bool** |  | [optional] [default to true]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **idealistaAgencyProfileListings**
```swift
    open class func idealistaAgencyProfileListings(shortName: String, market: String? = nil, operation: String? = nil, propertyType: String? = nil, page: Int? = nil, maxItems: Int? = nil, includeListings: Bool? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Agency profile + listings

An agency's microsite profile plus a page of its listings (by URL-slug shortName).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let shortName = "shortName_example" // String | 
let market = "market_example" // String | es|it|pt (optional) (default to "es")
let operation = "operation_example" // String | sale|rent (optional)
let propertyType = "propertyType_example" // String | homes|offices|premises|garages|newDevelopments|lands|storageRooms|buildings|bedrooms (optional)
let page = 987 // Int |  (optional) (default to 1)
let maxItems = 987 // Int |  (optional) (default to 30)
let includeListings = true // Bool |  (optional) (default to true)

// Agency profile + listings
IdealistaAPI.idealistaAgencyProfileListings(shortName: shortName, market: market, operation: operation, propertyType: propertyType, page: page, maxItems: maxItems, includeListings: includeListings) { (response, error) in
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
 **shortName** | **String** |  | 
 **market** | **String** | es|it|pt | [optional] [default to &quot;es&quot;]
 **operation** | **String** | sale|rent | [optional] 
 **propertyType** | **String** | homes|offices|premises|garages|newDevelopments|lands|storageRooms|buildings|bedrooms | [optional] 
 **page** | **Int** |  | [optional] [default to 1]
 **maxItems** | **Int** |  | [optional] [default to 30]
 **includeListings** | **Bool** |  | [optional] [default to true]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **idealistaGetListingEngagementStats**
```swift
    open class func idealistaGetListingEngagementStats(propertyCode: String, market: String? = nil, locale: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get listing engagement stats

Engagement counters for a listing: views, email contacts, sent-to-friend, favourites.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let propertyCode = "propertyCode_example" // String | 
let market = "market_example" // String | es|it|pt (optional) (default to "es")
let locale = "locale_example" // String | Language for stat labels (optional) (default to "en")

// Get listing engagement stats
IdealistaAPI.idealistaGetListingEngagementStats(propertyCode: propertyCode, market: market, locale: locale) { (response, error) in
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
 **propertyCode** | **String** |  | 
 **market** | **String** | es|it|pt | [optional] [default to &quot;es&quot;]
 **locale** | **String** | Language for stat labels | [optional] [default to &quot;en&quot;]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **idealistaGetPropertyDetail**
```swift
    open class func idealistaGetPropertyDetail(propertyCode: String, market: String? = nil, locale: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get property detail

Get a single Idealista listing's full detail (energy cert, characteristics, media).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let propertyCode = "propertyCode_example" // String | 
let market = "market_example" // String | es|it|pt (optional) (default to "es")
let locale = "locale_example" // String | Response language (en, es, it, pt) (optional) (default to "en")

// Get property detail
IdealistaAPI.idealistaGetPropertyDetail(propertyCode: propertyCode, market: market, locale: locale) { (response, error) in
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
 **propertyCode** | **String** |  | 
 **market** | **String** | es|it|pt | [optional] [default to &quot;es&quot;]
 **locale** | **String** | Response language (en, es, it, pt) | [optional] [default to &quot;en&quot;]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **idealistaIdealistaScraperHealthCheck**
```swift
    open class func idealistaIdealistaScraperHealthCheck(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Idealista scraper health check

Check health of the Idealista scraper service (accepts HEAD for UptimeRobot).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// Idealista scraper health check
IdealistaAPI.idealistaIdealistaScraperHealthCheck() { (response, error) in
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

# **idealistaIdealistaScraperHealthCheckHead**
```swift
    open class func idealistaIdealistaScraperHealthCheckHead(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Idealista scraper health check

Check health of the Idealista scraper service (accepts HEAD for UptimeRobot).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// Idealista scraper health check
IdealistaAPI.idealistaIdealistaScraperHealthCheckHead() { (response, error) in
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

# **idealistaListMarkets**
```swift
    open class func idealistaListMarkets(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

List markets

List supported Idealista markets (ES, IT, PT).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// List markets
IdealistaAPI.idealistaListMarkets() { (response, error) in
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

# **idealistaResolveLocations**
```swift
    open class func idealistaResolveLocations(query: String, operation: String? = nil, propertyType: String? = nil, market: String? = nil, locale: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Resolve locations

Resolve a free-text query into Idealista location codes for a search.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let query = "query_example" // String | Free-text location, e.g. 'sagrada familia'
let operation = "operation_example" // String | sale|rent (optional) (default to "sale")
let propertyType = "propertyType_example" // String | homes|offices|premises|garages|newDevelopments|lands|storageRooms|buildings|bedrooms (optional) (default to "homes")
let market = "market_example" // String | es|it|pt (optional) (default to "es")
let locale = "locale_example" // String | Response language (en, es, it, pt) (optional)

// Resolve locations
IdealistaAPI.idealistaResolveLocations(query: query, operation: operation, propertyType: propertyType, market: market, locale: locale) { (response, error) in
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
 **query** | **String** | Free-text location, e.g. &#39;sagrada familia&#39; | 
 **operation** | **String** | sale|rent | [optional] [default to &quot;sale&quot;]
 **propertyType** | **String** | homes|offices|premises|garages|newDevelopments|lands|storageRooms|buildings|bedrooms | [optional] [default to &quot;homes&quot;]
 **market** | **String** | es|it|pt | [optional] [default to &quot;es&quot;]
 **locale** | **String** | Response language (en, es, it, pt) | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **idealistaSearchAllBeatsResultCap**
```swift
    open class func idealistaSearchAllBeatsResultCap(location: String, operation: String? = nil, propertyType: String? = nil, market: String? = nil, maxResults: Int? = nil, minPrice: Double? = nil, maxPrice: Double? = nil, minSize: Double? = nil, maxSize: Double? = nil, minRooms: Int? = nil, maxRooms: Int? = nil, locale: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Search all (beats result cap)

Full inventory for a location, beating Idealista's ~1800 per-search cap via price-range tiling (deduped). Billed per page fetched.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let location = "location_example" // String | Idealista location code (from /suggest)
let operation = "operation_example" // String | sale|rent (optional) (default to "sale")
let propertyType = "propertyType_example" // String | homes|offices|premises|garages|newDevelopments|lands|storageRooms|buildings|bedrooms (optional) (default to "homes")
let market = "market_example" // String | es|it|pt (optional) (default to "es")
let maxResults = 987 // Int |  (optional) (default to 500)
let minPrice = 987 // Double |  (optional)
let maxPrice = 987 // Double |  (optional)
let minSize = 987 // Double |  (optional)
let maxSize = 987 // Double |  (optional)
let minRooms = 987 // Int |  (optional)
let maxRooms = 987 // Int |  (optional)
let locale = "locale_example" // String | Response language (en, es, it, pt) (optional)

// Search all (beats result cap)
IdealistaAPI.idealistaSearchAllBeatsResultCap(location: location, operation: operation, propertyType: propertyType, market: market, maxResults: maxResults, minPrice: minPrice, maxPrice: maxPrice, minSize: minSize, maxSize: maxSize, minRooms: minRooms, maxRooms: maxRooms, locale: locale) { (response, error) in
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
 **location** | **String** | Idealista location code (from /suggest) | 
 **operation** | **String** | sale|rent | [optional] [default to &quot;sale&quot;]
 **propertyType** | **String** | homes|offices|premises|garages|newDevelopments|lands|storageRooms|buildings|bedrooms | [optional] [default to &quot;homes&quot;]
 **market** | **String** | es|it|pt | [optional] [default to &quot;es&quot;]
 **maxResults** | **Int** |  | [optional] [default to 500]
 **minPrice** | **Double** |  | [optional] 
 **maxPrice** | **Double** |  | [optional] 
 **minSize** | **Double** |  | [optional] 
 **maxSize** | **Double** |  | [optional] 
 **minRooms** | **Int** |  | [optional] 
 **maxRooms** | **Int** |  | [optional] 
 **locale** | **String** | Response language (en, es, it, pt) | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **idealistaSearchListings**
```swift
    open class func idealistaSearchListings(location: String, operation: String? = nil, propertyType: String? = nil, market: String? = nil, page: Int? = nil, maxItems: Int? = nil, sortBy: String? = nil, sortOrder: String? = nil, minPrice: Double? = nil, maxPrice: Double? = nil, minSize: Double? = nil, maxSize: Double? = nil, minRooms: Int? = nil, maxRooms: Int? = nil, locale: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Search listings

Search Idealista real-estate listings by location code.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let location = "location_example" // String | Idealista location code (from /suggest)
let operation = "operation_example" // String | sale|rent (optional) (default to "sale")
let propertyType = "propertyType_example" // String | homes|offices|premises|garages|newDevelopments|lands|storageRooms|buildings|bedrooms (optional) (default to "homes")
let market = "market_example" // String | es|it|pt (optional) (default to "es")
let page = 987 // Int |  (optional) (default to 1)
let maxItems = 987 // Int |  (optional) (default to 30)
let sortBy = "sortBy_example" // String | distance|size|rooms|floor|ratioeurm2|price|street|photos|modificationDate|publicationDate|weigh|priceDown|preservationTypeAndPrice|privateAds (optional)
let sortOrder = "sortOrder_example" // String | asc|desc (optional) (default to "desc")
let minPrice = 987 // Double |  (optional)
let maxPrice = 987 // Double |  (optional)
let minSize = 987 // Double |  (optional)
let maxSize = 987 // Double |  (optional)
let minRooms = 987 // Int |  (optional)
let maxRooms = 987 // Int |  (optional)
let locale = "locale_example" // String | Response language (en, es, it, pt) (optional)

// Search listings
IdealistaAPI.idealistaSearchListings(location: location, operation: operation, propertyType: propertyType, market: market, page: page, maxItems: maxItems, sortBy: sortBy, sortOrder: sortOrder, minPrice: minPrice, maxPrice: maxPrice, minSize: minSize, maxSize: maxSize, minRooms: minRooms, maxRooms: maxRooms, locale: locale) { (response, error) in
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
 **location** | **String** | Idealista location code (from /suggest) | 
 **operation** | **String** | sale|rent | [optional] [default to &quot;sale&quot;]
 **propertyType** | **String** | homes|offices|premises|garages|newDevelopments|lands|storageRooms|buildings|bedrooms | [optional] [default to &quot;homes&quot;]
 **market** | **String** | es|it|pt | [optional] [default to &quot;es&quot;]
 **page** | **Int** |  | [optional] [default to 1]
 **maxItems** | **Int** |  | [optional] [default to 30]
 **sortBy** | **String** | distance|size|rooms|floor|ratioeurm2|price|street|photos|modificationDate|publicationDate|weigh|priceDown|preservationTypeAndPrice|privateAds | [optional] 
 **sortOrder** | **String** | asc|desc | [optional] [default to &quot;desc&quot;]
 **minPrice** | **Double** |  | [optional] 
 **maxPrice** | **Double** |  | [optional] 
 **minSize** | **Double** |  | [optional] 
 **maxSize** | **Double** |  | [optional] 
 **minRooms** | **Int** |  | [optional] 
 **maxRooms** | **Int** |  | [optional] 
 **locale** | **String** | Response language (en, es, it, pt) | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

