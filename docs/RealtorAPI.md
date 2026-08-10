# RealtorAPI

All URIs are relative to *https://scrapebadger.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**realtorGetFullPropertyDetail**](RealtorAPI.md#realtorgetfullpropertydetail) | **GET** /v1/realtor/properties/{property_id} | Get full property detail
[**realtorListMarkets**](RealtorAPI.md#realtorlistmarkets) | **GET** /v1/realtor/markets | List markets
[**realtorLocationAutocomplete**](RealtorAPI.md#realtorlocationautocomplete) | **GET** /v1/realtor/autocomplete | Location autocomplete
[**realtorRealtorScraperHealthCheck**](RealtorAPI.md#realtorrealtorscraperhealthcheck) | **GET** /v1/realtor/health | Realtor scraper health check
[**realtorRealtorScraperHealthCheckHead**](RealtorAPI.md#realtorrealtorscraperhealthcheckhead) | **HEAD** /v1/realtor/health | Realtor scraper health check
[**realtorSearchPropertyListings**](RealtorAPI.md#realtorsearchpropertylistings) | **GET** /v1/realtor/search | Search property listings


# **realtorGetFullPropertyDetail**
```swift
    open class func realtorGetFullPropertyDetail(propertyId: String, market: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get full property detail

Full listing detail: features, tax & price history, schools, photos, agents.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let propertyId = "propertyId_example" // String | 
let market = "market_example" // String | us (realtor.com) | ca (realtor.ca) (optional) (default to "us")

// Get full property detail
RealtorAPI.realtorGetFullPropertyDetail(propertyId: propertyId, market: market) { (response, error) in
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
 **market** | **String** | us (realtor.com) | ca (realtor.ca) | [optional] [default to &quot;us&quot;]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **realtorListMarkets**
```swift
    open class func realtorListMarkets(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

List markets

List supported Realtor markets (US = realtor.com, CA = realtor.ca).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// List markets
RealtorAPI.realtorListMarkets() { (response, error) in
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

# **realtorLocationAutocomplete**
```swift
    open class func realtorLocationAutocomplete(query: String, market: String? = nil, limit: Int? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Location autocomplete

Resolve a location query into candidate places to feed /search.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let query = "query_example" // String | Freetext location (city, ZIP/postal, address…)
let market = "market_example" // String | us (realtor.com) | ca (realtor.ca) (optional) (default to "us")
let limit = 987 // Int |  (optional) (default to 10)

// Location autocomplete
RealtorAPI.realtorLocationAutocomplete(query: query, market: market, limit: limit) { (response, error) in
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
 **query** | **String** | Freetext location (city, ZIP/postal, address…) | 
 **market** | **String** | us (realtor.com) | ca (realtor.ca) | [optional] [default to &quot;us&quot;]
 **limit** | **Int** |  | [optional] [default to 10]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **realtorRealtorScraperHealthCheck**
```swift
    open class func realtorRealtorScraperHealthCheck(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Realtor scraper health check

Check health of the realtor scraper service (accepts HEAD for UptimeRobot).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// Realtor scraper health check
RealtorAPI.realtorRealtorScraperHealthCheck() { (response, error) in
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

# **realtorRealtorScraperHealthCheckHead**
```swift
    open class func realtorRealtorScraperHealthCheckHead(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Realtor scraper health check

Check health of the realtor scraper service (accepts HEAD for UptimeRobot).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// Realtor scraper health check
RealtorAPI.realtorRealtorScraperHealthCheckHead() { (response, error) in
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

# **realtorSearchPropertyListings**
```swift
    open class func realtorSearchPropertyListings(location: String? = nil, market: String? = nil, status: String? = nil, priceMin: Double? = nil, priceMax: Double? = nil, bedsMin: Int? = nil, bathsMin: Int? = nil, sqftMin: Int? = nil, sqftMax: Int? = nil, propertyType: String? = nil, sort: String? = nil, page: Int? = nil, limit: Int? = nil, latMin: Double? = nil, latMax: Double? = nil, lngMin: Double? = nil, lngMax: Double? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Search property listings

Search for-sale/for-rent/sold listings with rich filters.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let location = "location_example" // String | 'Austin, TX', a ZIP, 'Toronto, ON'… (optional)
let market = "market_example" // String | us (realtor.com) | ca (realtor.ca) (optional) (default to "us")
let status = "status_example" // String | for_sale | for_rent | sold | pending (optional) (default to "for_sale")
let priceMin = 987 // Double |  (optional)
let priceMax = 987 // Double |  (optional)
let bedsMin = 987 // Int |  (optional)
let bathsMin = 987 // Int |  (optional)
let sqftMin = 987 // Int | US only (optional)
let sqftMax = 987 // Int | US only (optional)
let propertyType = "propertyType_example" // String | US only, CSV of property types (optional)
let sort = "sort_example" // String | relevant | newest | price_low | price_high | photo_count (optional) (default to "relevant")
let page = 987 // Int |  (optional) (default to 1)
let limit = 987 // Int |  (optional)
let latMin = 987 // Double | CA bbox south (optional)
let latMax = 987 // Double | CA bbox north (optional)
let lngMin = 987 // Double | CA bbox west (optional)
let lngMax = 987 // Double | CA bbox east (optional)

// Search property listings
RealtorAPI.realtorSearchPropertyListings(location: location, market: market, status: status, priceMin: priceMin, priceMax: priceMax, bedsMin: bedsMin, bathsMin: bathsMin, sqftMin: sqftMin, sqftMax: sqftMax, propertyType: propertyType, sort: sort, page: page, limit: limit, latMin: latMin, latMax: latMax, lngMin: lngMin, lngMax: lngMax) { (response, error) in
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
 **location** | **String** | &#39;Austin, TX&#39;, a ZIP, &#39;Toronto, ON&#39;… | [optional] 
 **market** | **String** | us (realtor.com) | ca (realtor.ca) | [optional] [default to &quot;us&quot;]
 **status** | **String** | for_sale | for_rent | sold | pending | [optional] [default to &quot;for_sale&quot;]
 **priceMin** | **Double** |  | [optional] 
 **priceMax** | **Double** |  | [optional] 
 **bedsMin** | **Int** |  | [optional] 
 **bathsMin** | **Int** |  | [optional] 
 **sqftMin** | **Int** | US only | [optional] 
 **sqftMax** | **Int** | US only | [optional] 
 **propertyType** | **String** | US only, CSV of property types | [optional] 
 **sort** | **String** | relevant | newest | price_low | price_high | photo_count | [optional] [default to &quot;relevant&quot;]
 **page** | **Int** |  | [optional] [default to 1]
 **limit** | **Int** |  | [optional] 
 **latMin** | **Double** | CA bbox south | [optional] 
 **latMax** | **Double** | CA bbox north | [optional] 
 **lngMin** | **Double** | CA bbox west | [optional] 
 **lngMax** | **Double** | CA bbox east | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

