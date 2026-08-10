# ImmobiliareAPI

All URIs are relative to *https://scrapebadger.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**immobiliareGetAgencyProfile**](ImmobiliareAPI.md#immobiliaregetagencyprofile) | **GET** /v1/immobiliare/agencies/{agency_id} | Get agency profile
[**immobiliareGetAnAgencySListings**](ImmobiliareAPI.md#immobiliaregetanagencyslistings) | **GET** /v1/immobiliare/agencies/{agency_id}/listings | Get an agency&#39;s listings
[**immobiliareGetListingDetail**](ImmobiliareAPI.md#immobiliaregetlistingdetail) | **GET** /v1/immobiliare/listings/{listing_id} | Get listing detail
[**immobiliareImmobiliareScraperHealthCheck**](ImmobiliareAPI.md#immobiliareimmobiliarescraperhealthcheck) | **GET** /v1/immobiliare/health | Immobiliare scraper health check
[**immobiliareImmobiliareScraperHealthCheckHead**](ImmobiliareAPI.md#immobiliareimmobiliarescraperhealthcheckhead) | **HEAD** /v1/immobiliare/health | Immobiliare scraper health check
[**immobiliareListFilterEnums**](ImmobiliareAPI.md#immobiliarelistfilterenums) | **GET** /v1/immobiliare/reference | List filter enums
[**immobiliareListMarkets**](ImmobiliareAPI.md#immobiliarelistmarkets) | **GET** /v1/immobiliare/markets | List markets
[**immobiliareLocationAutocomplete**](ImmobiliareAPI.md#immobiliarelocationautocomplete) | **GET** /v1/immobiliare/autocomplete | Location autocomplete
[**immobiliarePriceMTimeSeries**](ImmobiliareAPI.md#immobiliarepricemtimeseries) | **GET** /v1/immobiliare/market-insights/prices | Price €/m² time series
[**immobiliareSearchListings**](ImmobiliareAPI.md#immobiliaresearchlistings) | **GET** /v1/immobiliare/search | Search listings


# **immobiliareGetAgencyProfile**
```swift
    open class func immobiliareGetAgencyProfile(agencyId: Int, market: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get agency profile

Public agency/advertiser profile.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let agencyId = 987 // Int | 
let market = "market_example" // String | it | es | gr | lu (optional) (default to "it")

// Get agency profile
ImmobiliareAPI.immobiliareGetAgencyProfile(agencyId: agencyId, market: market) { (response, error) in
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
 **agencyId** | **Int** |  | 
 **market** | **String** | it | es | gr | lu | [optional] [default to &quot;it&quot;]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **immobiliareGetAnAgencySListings**
```swift
    open class func immobiliareGetAnAgencySListings(agencyId: Int, market: String? = nil, contract: String? = nil, page: Int? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get an agency's listings

An agency's active listings.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let agencyId = 987 // Int | 
let market = "market_example" // String | it | es | gr | lu (optional) (default to "it")
let contract = "contract_example" // String | sale | rent (optional) (default to "sale")
let page = 987 // Int |  (optional) (default to 1)

// Get an agency's listings
ImmobiliareAPI.immobiliareGetAnAgencySListings(agencyId: agencyId, market: market, contract: contract, page: page) { (response, error) in
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
 **agencyId** | **Int** |  | 
 **market** | **String** | it | es | gr | lu | [optional] [default to &quot;it&quot;]
 **contract** | **String** | sale | rent | [optional] [default to &quot;sale&quot;]
 **page** | **Int** |  | [optional] [default to 1]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **immobiliareGetListingDetail**
```swift
    open class func immobiliareGetListingDetail(listingId: Int, market: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get listing detail

Full detail for a single listing.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let listingId = 987 // Int | 
let market = "market_example" // String | it | es | gr | lu (optional) (default to "it")

// Get listing detail
ImmobiliareAPI.immobiliareGetListingDetail(listingId: listingId, market: market) { (response, error) in
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
 **listingId** | **Int** |  | 
 **market** | **String** | it | es | gr | lu | [optional] [default to &quot;it&quot;]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **immobiliareImmobiliareScraperHealthCheck**
```swift
    open class func immobiliareImmobiliareScraperHealthCheck(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Immobiliare scraper health check

Check health of the Immobiliare scraper service (accepts HEAD).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// Immobiliare scraper health check
ImmobiliareAPI.immobiliareImmobiliareScraperHealthCheck() { (response, error) in
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

# **immobiliareImmobiliareScraperHealthCheckHead**
```swift
    open class func immobiliareImmobiliareScraperHealthCheckHead(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Immobiliare scraper health check

Check health of the Immobiliare scraper service (accepts HEAD).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// Immobiliare scraper health check
ImmobiliareAPI.immobiliareImmobiliareScraperHealthCheckHead() { (response, error) in
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

# **immobiliareListFilterEnums**
```swift
    open class func immobiliareListFilterEnums(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

List filter enums

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// List filter enums
ImmobiliareAPI.immobiliareListFilterEnums() { (response, error) in
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

# **immobiliareListMarkets**
```swift
    open class func immobiliareListMarkets(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

List markets

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// List markets
ImmobiliareAPI.immobiliareListMarkets() { (response, error) in
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

# **immobiliareLocationAutocomplete**
```swift
    open class func immobiliareLocationAutocomplete(query: String, market: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Location autocomplete

Resolve a place name to region/province/city ids usable in search.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let query = "query_example" // String | Free-text place name, e.g. 'Milano'
let market = "market_example" // String | it | es | gr | lu (optional) (default to "it")

// Location autocomplete
ImmobiliareAPI.immobiliareLocationAutocomplete(query: query, market: market) { (response, error) in
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
 **query** | **String** | Free-text place name, e.g. &#39;Milano&#39; | 
 **market** | **String** | it | es | gr | lu | [optional] [default to &quot;it&quot;]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **immobiliarePriceMTimeSeries**
```swift
    open class func immobiliarePriceMTimeSeries(regionId: String, market: String? = nil, provinceId: String? = nil, cityId: String? = nil, contract: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Price €/m² time series

Historical €/m² price statistics for an area.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let regionId = "regionId_example" // String | Region id, e.g. 'lom'
let market = "market_example" // String | it | es | gr | lu (optional) (default to "it")
let provinceId = "provinceId_example" // String | Province id, e.g. 'MI' (optional)
let cityId = "cityId_example" // String | City id (idComune) (optional)
let contract = "contract_example" // String | sale | rent (optional) (default to "sale")

// Price €/m² time series
ImmobiliareAPI.immobiliarePriceMTimeSeries(regionId: regionId, market: market, provinceId: provinceId, cityId: cityId, contract: contract) { (response, error) in
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
 **regionId** | **String** | Region id, e.g. &#39;lom&#39; | 
 **market** | **String** | it | es | gr | lu | [optional] [default to &quot;it&quot;]
 **provinceId** | **String** | Province id, e.g. &#39;MI&#39; | [optional] 
 **cityId** | **String** | City id (idComune) | [optional] 
 **contract** | **String** | sale | rent | [optional] [default to &quot;sale&quot;]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **immobiliareSearchListings**
```swift
    open class func immobiliareSearchListings(market: String? = nil, location: String? = nil, regionId: String? = nil, provinceId: String? = nil, cityId: String? = nil, contract: String? = nil, category: String? = nil, priceMin: Int? = nil, priceMax: Int? = nil, surfaceMin: Int? = nil, surfaceMax: Int? = nil, roomsMin: Int? = nil, roomsMax: Int? = nil, bathroomsMin: Int? = nil, sort: String? = nil, page: Int? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Search listings

Search Immobiliare-group listings (scope by location + contract + filters).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let market = "market_example" // String | it | es | gr | lu (optional) (default to "it")
let location = "location_example" // String | Free-text place (auto-resolved) (optional)
let regionId = "regionId_example" // String | fkRegione (from /autocomplete) (optional)
let provinceId = "provinceId_example" // String | idProvincia (from /autocomplete) (optional)
let cityId = "cityId_example" // String | idComune (from /autocomplete) (optional)
let contract = "contract_example" // String | sale | rent (optional) (default to "sale")
let category = "category_example" // String | see /reference (optional) (default to "residential")
let priceMin = 987 // Int |  (optional)
let priceMax = 987 // Int |  (optional)
let surfaceMin = 987 // Int |  (optional)
let surfaceMax = 987 // Int |  (optional)
let roomsMin = 987 // Int |  (optional)
let roomsMax = 987 // Int |  (optional)
let bathroomsMin = 987 // Int |  (optional)
let sort = "sort_example" // String | see /reference (optional) (default to "relevance")
let page = 987 // Int |  (optional) (default to 1)

// Search listings
ImmobiliareAPI.immobiliareSearchListings(market: market, location: location, regionId: regionId, provinceId: provinceId, cityId: cityId, contract: contract, category: category, priceMin: priceMin, priceMax: priceMax, surfaceMin: surfaceMin, surfaceMax: surfaceMax, roomsMin: roomsMin, roomsMax: roomsMax, bathroomsMin: bathroomsMin, sort: sort, page: page) { (response, error) in
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
 **market** | **String** | it | es | gr | lu | [optional] [default to &quot;it&quot;]
 **location** | **String** | Free-text place (auto-resolved) | [optional] 
 **regionId** | **String** | fkRegione (from /autocomplete) | [optional] 
 **provinceId** | **String** | idProvincia (from /autocomplete) | [optional] 
 **cityId** | **String** | idComune (from /autocomplete) | [optional] 
 **contract** | **String** | sale | rent | [optional] [default to &quot;sale&quot;]
 **category** | **String** | see /reference | [optional] [default to &quot;residential&quot;]
 **priceMin** | **Int** |  | [optional] 
 **priceMax** | **Int** |  | [optional] 
 **surfaceMin** | **Int** |  | [optional] 
 **surfaceMax** | **Int** |  | [optional] 
 **roomsMin** | **Int** |  | [optional] 
 **roomsMax** | **Int** |  | [optional] 
 **bathroomsMin** | **Int** |  | [optional] 
 **sort** | **String** | see /reference | [optional] [default to &quot;relevance&quot;]
 **page** | **Int** |  | [optional] [default to 1]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

