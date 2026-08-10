# RedfinAPI

All URIs are relative to *https://scrapebadger.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**redfinGetAgentProfileListings**](RedfinAPI.md#redfingetagentprofilelistings) | **GET** /v1/redfin/agent | Get agent profile + listings
[**redfinGetPropertyDetail**](RedfinAPI.md#redfingetpropertydetail) | **GET** /v1/redfin/property/{property_id} | Get property detail
[**redfinGetPropertyDetailByUrl**](RedfinAPI.md#redfingetpropertydetailbyurl) | **GET** /v1/redfin/property | Get property detail by URL
[**redfinListCoverageMarkets**](RedfinAPI.md#redfinlistcoveragemarkets) | **GET** /v1/redfin/markets | List coverage markets
[**redfinRedfinScraperHealthCheck**](RedfinAPI.md#redfinredfinscraperhealthcheck) | **GET** /v1/redfin/health | Redfin scraper health check
[**redfinRedfinScraperHealthCheckHead**](RedfinAPI.md#redfinredfinscraperhealthcheckhead) | **HEAD** /v1/redfin/health | Redfin scraper health check
[**redfinRegionAddressSuggestions**](RedfinAPI.md#redfinregionaddresssuggestions) | **GET** /v1/redfin/autocomplete | Region/address suggestions
[**redfinSearchProperties**](RedfinAPI.md#redfinsearchproperties) | **GET** /v1/redfin/search | Search properties


# **redfinGetAgentProfileListings**
```swift
    open class func redfinGetAgentProfileListings(url: String? = nil, agentId: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get agent profile + listings

Get a Redfin real-estate agent's profile and their active listings.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let url = "url_example" // String | Full Redfin /realestateagents/ URL (optional)
let agentId = "agentId_example" // String | Redfin agent id (optional)

// Get agent profile + listings
RedfinAPI.redfinGetAgentProfileListings(url: url, agentId: agentId) { (response, error) in
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
 **url** | **String** | Full Redfin /realestateagents/ URL | [optional] 
 **agentId** | **String** | Redfin agent id | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **redfinGetPropertyDetail**
```swift
    open class func redfinGetPropertyDetail(propertyId: String, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get property detail

Get a single Redfin property's full detail by its numeric propertyId.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let propertyId = "propertyId_example" // String | 

// Get property detail
RedfinAPI.redfinGetPropertyDetail(propertyId: propertyId) { (response, error) in
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
 **propertyId** | **String** |  | 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **redfinGetPropertyDetailByUrl**
```swift
    open class func redfinGetPropertyDetailByUrl(url: String, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get property detail by URL

Get a single Redfin property's full detail by its home URL.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let url = "url_example" // String | Full Redfin property URL (/CA/City/.../home/12345678)

// Get property detail by URL
RedfinAPI.redfinGetPropertyDetailByUrl(url: url) { (response, error) in
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
 **url** | **String** | Full Redfin property URL (/CA/City/.../home/12345678) | 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **redfinListCoverageMarkets**
```swift
    open class func redfinListCoverageMarkets(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

List coverage markets

List Redfin coverage regions (US).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// List coverage markets
RedfinAPI.redfinListCoverageMarkets() { (response, error) in
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

# **redfinRedfinScraperHealthCheck**
```swift
    open class func redfinRedfinScraperHealthCheck(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Redfin scraper health check

Check health of the Redfin scraper service (accepts HEAD for UptimeRobot).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// Redfin scraper health check
RedfinAPI.redfinRedfinScraperHealthCheck() { (response, error) in
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

# **redfinRedfinScraperHealthCheckHead**
```swift
    open class func redfinRedfinScraperHealthCheckHead(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Redfin scraper health check

Check health of the Redfin scraper service (accepts HEAD for UptimeRobot).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// Redfin scraper health check
RedfinAPI.redfinRedfinScraperHealthCheckHead() { (response, error) in
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

# **redfinRegionAddressSuggestions**
```swift
    open class func redfinRegionAddressSuggestions(query: String, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Region/address suggestions

Resolve a search term to Redfin regions/addresses.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let query = "query_example" // String | Partial location — city, ZIP, address, neighborhood

// Region/address suggestions
RedfinAPI.redfinRegionAddressSuggestions(query: query) { (response, error) in
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

# **redfinSearchProperties**
```swift
    open class func redfinSearchProperties(location: String, page: Int? = nil, sort: String? = nil, priceMin: Int? = nil, priceMax: Int? = nil, bedsMin: Int? = nil, bathsMin: Double? = nil, homeType: String? = nil, sqftMin: Int? = nil, sqftMax: Int? = nil, lotMin: Int? = nil, lotMax: Int? = nil, yearBuiltMin: Int? = nil, yearBuiltMax: Int? = nil, maxDaysOnMarket: Int? = nil, north: Double? = nil, south: Double? = nil, east: Double? = nil, west: Double? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Search properties

Search Redfin for for-sale / for-rent / recently-sold properties.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let location = "location_example" // String | City/state, ZIP, address or neighborhood
let page = 987 // Int |  (optional) (default to 1)
let sort = "sort_example" // String | relevant|newest|price_high_to_low|price_low_to_high|square_feet|lot_size|price_per_sqft|beds|baths (optional)
let priceMin = 987 // Int |  (optional)
let priceMax = 987 // Int |  (optional)
let bedsMin = 987 // Int |  (optional)
let bathsMin = 987 // Double |  (optional)
let homeType = "homeType_example" // String | house|condo|townhouse|multi_family|land|mobile|coop|other (optional)
let sqftMin = 987 // Int |  (optional)
let sqftMax = 987 // Int |  (optional)
let lotMin = 987 // Int |  (optional)
let lotMax = 987 // Int |  (optional)
let yearBuiltMin = 987 // Int |  (optional)
let yearBuiltMax = 987 // Int |  (optional)
let maxDaysOnMarket = 987 // Int |  (optional)
let north = 987 // Double | Map bounds for tiling past the cap (optional)
let south = 987 // Double |  (optional)
let east = 987 // Double |  (optional)
let west = 987 // Double |  (optional)

// Search properties
RedfinAPI.redfinSearchProperties(location: location, page: page, sort: sort, priceMin: priceMin, priceMax: priceMax, bedsMin: bedsMin, bathsMin: bathsMin, homeType: homeType, sqftMin: sqftMin, sqftMax: sqftMax, lotMin: lotMin, lotMax: lotMax, yearBuiltMin: yearBuiltMin, yearBuiltMax: yearBuiltMax, maxDaysOnMarket: maxDaysOnMarket, north: north, south: south, east: east, west: west) { (response, error) in
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
 **page** | **Int** |  | [optional] [default to 1]
 **sort** | **String** | relevant|newest|price_high_to_low|price_low_to_high|square_feet|lot_size|price_per_sqft|beds|baths | [optional] 
 **priceMin** | **Int** |  | [optional] 
 **priceMax** | **Int** |  | [optional] 
 **bedsMin** | **Int** |  | [optional] 
 **bathsMin** | **Double** |  | [optional] 
 **homeType** | **String** | house|condo|townhouse|multi_family|land|mobile|coop|other | [optional] 
 **sqftMin** | **Int** |  | [optional] 
 **sqftMax** | **Int** |  | [optional] 
 **lotMin** | **Int** |  | [optional] 
 **lotMax** | **Int** |  | [optional] 
 **yearBuiltMin** | **Int** |  | [optional] 
 **yearBuiltMax** | **Int** |  | [optional] 
 **maxDaysOnMarket** | **Int** |  | [optional] 
 **north** | **Double** | Map bounds for tiling past the cap | [optional] 
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

