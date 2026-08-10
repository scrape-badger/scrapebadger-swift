# ZillowAPI

All URIs are relative to *https://scrapebadger.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**zillowGetAgentProfileListings**](ZillowAPI.md#zillowgetagentprofilelistings) | **GET** /v1/zillow/agent | Get agent profile + listings
[**zillowGetPropertyDetail**](ZillowAPI.md#zillowgetpropertydetail) | **GET** /v1/zillow/property/{zpid} | Get property detail
[**zillowGetPropertyDetailByUrl**](ZillowAPI.md#zillowgetpropertydetailbyurl) | **GET** /v1/zillow/property | Get property detail by URL
[**zillowListCoverageMarkets**](ZillowAPI.md#zillowlistcoveragemarkets) | **GET** /v1/zillow/markets | List coverage markets
[**zillowRegionAddressSuggestions**](ZillowAPI.md#zillowregionaddresssuggestions) | **GET** /v1/zillow/autocomplete | Region/address suggestions
[**zillowSearchProperties**](ZillowAPI.md#zillowsearchproperties) | **GET** /v1/zillow/search | Search properties
[**zillowZillowScraperHealthCheck**](ZillowAPI.md#zillowzillowscraperhealthcheck) | **GET** /v1/zillow/health | Zillow scraper health check
[**zillowZillowScraperHealthCheckHead**](ZillowAPI.md#zillowzillowscraperhealthcheckhead) | **HEAD** /v1/zillow/health | Zillow scraper health check


# **zillowGetAgentProfileListings**
```swift
    open class func zillowGetAgentProfileListings(username: String? = nil, url: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get agent profile + listings

Get a Zillow professional's profile and their active listings.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let username = "username_example" // String | Zillow profile username (optional)
let url = "url_example" // String | Full Zillow /profile/... URL (optional)

// Get agent profile + listings
ZillowAPI.zillowGetAgentProfileListings(username: username, url: url) { (response, error) in
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
 **username** | **String** | Zillow profile username | [optional] 
 **url** | **String** | Full Zillow /profile/... URL | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **zillowGetPropertyDetail**
```swift
    open class func zillowGetPropertyDetail(zpid: String, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get property detail

Get a single Zillow property's full detail by zpid.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let zpid = "zpid_example" // String | 

// Get property detail
ZillowAPI.zillowGetPropertyDetail(zpid: zpid) { (response, error) in
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
 **zpid** | **String** |  | 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **zillowGetPropertyDetailByUrl**
```swift
    open class func zillowGetPropertyDetailByUrl(url: String, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get property detail by URL

Get a single Zillow property's full detail by its homedetails URL.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let url = "url_example" // String | Full Zillow /homedetails/... URL

// Get property detail by URL
ZillowAPI.zillowGetPropertyDetailByUrl(url: url) { (response, error) in
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
 **url** | **String** | Full Zillow /homedetails/... URL | 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **zillowListCoverageMarkets**
```swift
    open class func zillowListCoverageMarkets(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

List coverage markets

List Zillow coverage regions (US + Canada).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// List coverage markets
ZillowAPI.zillowListCoverageMarkets() { (response, error) in
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

# **zillowRegionAddressSuggestions**
```swift
    open class func zillowRegionAddressSuggestions(query: String, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Region/address suggestions

Resolve a search term to Zillow regions/addresses.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let query = "query_example" // String | Partial location — city, ZIP, address, neighborhood

// Region/address suggestions
ZillowAPI.zillowRegionAddressSuggestions(query: query) { (response, error) in
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
 **query** | **String** | Partial location — city, ZIP, address, neighborhood | 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **zillowSearchProperties**
```swift
    open class func zillowSearchProperties(location: String, status: String? = nil, page: Int? = nil, sort: String? = nil, priceMin: Int? = nil, priceMax: Int? = nil, bedsMin: Int? = nil, bathsMin: Double? = nil, homeType: String? = nil, sqftMin: Int? = nil, sqftMax: Int? = nil, lotMin: Int? = nil, lotMax: Int? = nil, yearBuiltMin: Int? = nil, yearBuiltMax: Int? = nil, hoaMax: Int? = nil, keywords: String? = nil, daysOn: String? = nil, north: Double? = nil, south: Double? = nil, east: Double? = nil, west: Double? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Search properties

Search Zillow for for-sale / for-rent / recently-sold properties.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let location = "location_example" // String | City/state, ZIP, address or neighborhood
let status = "status_example" // String | for_sale|for_rent|sold (optional) (default to "for_sale")
let page = 987 // Int |  (optional) (default to 1)
let sort = "sort_example" // String | homes_for_you|newest|price_high_to_low|price_low_to_high|bedrooms|bathrooms|square_feet|lot_size|year_built (optional)
let priceMin = 987 // Int |  (optional)
let priceMax = 987 // Int |  (optional)
let bedsMin = 987 // Int |  (optional)
let bathsMin = 987 // Double |  (optional)
let homeType = "homeType_example" // String | houses|condos|townhomes|apartments|manufactured|lots|multi_family (optional)
let sqftMin = 987 // Int |  (optional)
let sqftMax = 987 // Int |  (optional)
let lotMin = 987 // Int |  (optional)
let lotMax = 987 // Int |  (optional)
let yearBuiltMin = 987 // Int |  (optional)
let yearBuiltMax = 987 // Int |  (optional)
let hoaMax = 987 // Int |  (optional)
let keywords = "keywords_example" // String |  (optional)
let daysOn = "daysOn_example" // String |  (optional)
let north = 987 // Double | Map bounds for tiling past the 820 cap (optional)
let south = 987 // Double |  (optional)
let east = 987 // Double |  (optional)
let west = 987 // Double |  (optional)

// Search properties
ZillowAPI.zillowSearchProperties(location: location, status: status, page: page, sort: sort, priceMin: priceMin, priceMax: priceMax, bedsMin: bedsMin, bathsMin: bathsMin, homeType: homeType, sqftMin: sqftMin, sqftMax: sqftMax, lotMin: lotMin, lotMax: lotMax, yearBuiltMin: yearBuiltMin, yearBuiltMax: yearBuiltMax, hoaMax: hoaMax, keywords: keywords, daysOn: daysOn, north: north, south: south, east: east, west: west) { (response, error) in
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
 **location** | **String** | City/state, ZIP, address or neighborhood | 
 **status** | **String** | for_sale|for_rent|sold | [optional] [default to &quot;for_sale&quot;]
 **page** | **Int** |  | [optional] [default to 1]
 **sort** | **String** | homes_for_you|newest|price_high_to_low|price_low_to_high|bedrooms|bathrooms|square_feet|lot_size|year_built | [optional] 
 **priceMin** | **Int** |  | [optional] 
 **priceMax** | **Int** |  | [optional] 
 **bedsMin** | **Int** |  | [optional] 
 **bathsMin** | **Double** |  | [optional] 
 **homeType** | **String** | houses|condos|townhomes|apartments|manufactured|lots|multi_family | [optional] 
 **sqftMin** | **Int** |  | [optional] 
 **sqftMax** | **Int** |  | [optional] 
 **lotMin** | **Int** |  | [optional] 
 **lotMax** | **Int** |  | [optional] 
 **yearBuiltMin** | **Int** |  | [optional] 
 **yearBuiltMax** | **Int** |  | [optional] 
 **hoaMax** | **Int** |  | [optional] 
 **keywords** | **String** |  | [optional] 
 **daysOn** | **String** |  | [optional] 
 **north** | **Double** | Map bounds for tiling past the 820 cap | [optional] 
 **south** | **Double** |  | [optional] 
 **east** | **Double** |  | [optional] 
 **west** | **Double** |  | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **zillowZillowScraperHealthCheck**
```swift
    open class func zillowZillowScraperHealthCheck(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Zillow scraper health check

Check health of the Zillow scraper service (accepts HEAD for UptimeRobot).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// Zillow scraper health check
ZillowAPI.zillowZillowScraperHealthCheck() { (response, error) in
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

# **zillowZillowScraperHealthCheckHead**
```swift
    open class func zillowZillowScraperHealthCheckHead(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Zillow scraper health check

Check health of the Zillow scraper service (accepts HEAD for UptimeRobot).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// Zillow scraper health check
ZillowAPI.zillowZillowScraperHealthCheckHead() { (response, error) in
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

