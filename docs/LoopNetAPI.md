# LoopNetAPI

All URIs are relative to *https://scrapebadger.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**loopnetGetBrokerProfile**](LoopNetAPI.md#loopnetgetbrokerprofile) | **GET** /v1/loopnet/brokers/{slug}/{broker_id} | Get broker profile
[**loopnetGetListingDetail**](LoopNetAPI.md#loopnetgetlistingdetail) | **GET** /v1/loopnet/listings/{listing_id} | Get listing detail
[**loopnetListCoverageMarkets**](LoopNetAPI.md#loopnetlistcoveragemarkets) | **GET** /v1/loopnet/markets | List coverage markets
[**loopnetListPropertyTypes**](LoopNetAPI.md#loopnetlistpropertytypes) | **GET** /v1/loopnet/property-types | List property types
[**loopnetLoopnetScraperHealthCheck**](LoopNetAPI.md#loopnetloopnetscraperhealthcheck) | **GET** /v1/loopnet/health | LoopNet scraper health check
[**loopnetLoopnetScraperHealthCheckHead**](LoopNetAPI.md#loopnetloopnetscraperhealthcheckhead) | **HEAD** /v1/loopnet/health | LoopNet scraper health check
[**loopnetSearchCommercialRealEstate**](LoopNetAPI.md#loopnetsearchcommercialrealestate) | **GET** /v1/loopnet/search | Search commercial real estate


# **loopnetGetBrokerProfile**
```swift
    open class func loopnetGetBrokerProfile(slug: String, brokerId: String, market: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get broker profile

Get a LoopNet broker profile + their listings by slug + id.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let slug = "slug_example" // String | 
let brokerId = "brokerId_example" // String | 
let market = "market_example" // String | us|ca|uk|fr|es (optional) (default to "us")

// Get broker profile
LoopNetAPI.loopnetGetBrokerProfile(slug: slug, brokerId: brokerId, market: market) { (response, error) in
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
 **slug** | **String** |  | 
 **brokerId** | **String** |  | 
 **market** | **String** | us|ca|uk|fr|es | [optional] [default to &quot;us&quot;]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **loopnetGetListingDetail**
```swift
    open class func loopnetGetListingDetail(listingId: String, market: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get listing detail

Get a single LoopNet listing's full detail by its numeric id.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let listingId = "listingId_example" // String | 
let market = "market_example" // String | us|ca|uk|fr|es (optional) (default to "us")

// Get listing detail
LoopNetAPI.loopnetGetListingDetail(listingId: listingId, market: market) { (response, error) in
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
 **listingId** | **String** |  | 
 **market** | **String** | us|ca|uk|fr|es | [optional] [default to &quot;us&quot;]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **loopnetListCoverageMarkets**
```swift
    open class func loopnetListCoverageMarkets(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

List coverage markets

List LoopNet coverage markets (US, CA, UK, FR, ES).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// List coverage markets
LoopNetAPI.loopnetListCoverageMarkets() { (response, error) in
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

# **loopnetListPropertyTypes**
```swift
    open class func loopnetListPropertyTypes(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

List property types

List LoopNet property-type facets accepted by /search.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// List property types
LoopNetAPI.loopnetListPropertyTypes() { (response, error) in
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

# **loopnetLoopnetScraperHealthCheck**
```swift
    open class func loopnetLoopnetScraperHealthCheck(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

LoopNet scraper health check

Check health of the LoopNet scraper service (accepts HEAD for UptimeRobot).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// LoopNet scraper health check
LoopNetAPI.loopnetLoopnetScraperHealthCheck() { (response, error) in
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

# **loopnetLoopnetScraperHealthCheckHead**
```swift
    open class func loopnetLoopnetScraperHealthCheckHead(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

LoopNet scraper health check

Check health of the LoopNet scraper service (accepts HEAD for UptimeRobot).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// LoopNet scraper health check
LoopNetAPI.loopnetLoopnetScraperHealthCheckHead() { (response, error) in
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

# **loopnetSearchCommercialRealEstate**
```swift
    open class func loopnetSearchCommercialRealEstate(location: String, market: String? = nil, listingType: String? = nil, propertyType: String? = nil, page: Int? = nil, minPrice: Int? = nil, maxPrice: Int? = nil, priceType: String? = nil, minSize: Int? = nil, maxSize: Int? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Search commercial real estate

Search LoopNet for-lease / for-sale / auction listings across all markets.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let location = "location_example" // String | City/state, ZIP, state code, or 'usa'
let market = "market_example" // String | us|ca|uk|fr|es (optional) (default to "us")
let listingType = "listingType_example" // String | for-lease|for-sale|auctions (optional) (default to "for-lease")
let propertyType = "propertyType_example" // String | Slug from /property-types (optional)
let page = 987 // Int |  (optional) (default to 1)
let minPrice = 987 // Int |  (optional)
let maxPrice = 987 // Int |  (optional)
let priceType = "priceType_example" // String | unit | sf | acre (optional)
let minSize = 987 // Int |  (optional)
let maxSize = 987 // Int |  (optional)

// Search commercial real estate
LoopNetAPI.loopnetSearchCommercialRealEstate(location: location, market: market, listingType: listingType, propertyType: propertyType, page: page, minPrice: minPrice, maxPrice: maxPrice, priceType: priceType, minSize: minSize, maxSize: maxSize) { (response, error) in
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
 **location** | **String** | City/state, ZIP, state code, or &#39;usa&#39; | 
 **market** | **String** | us|ca|uk|fr|es | [optional] [default to &quot;us&quot;]
 **listingType** | **String** | for-lease|for-sale|auctions | [optional] [default to &quot;for-lease&quot;]
 **propertyType** | **String** | Slug from /property-types | [optional] 
 **page** | **Int** |  | [optional] [default to 1]
 **minPrice** | **Int** |  | [optional] 
 **maxPrice** | **Int** |  | [optional] 
 **priceType** | **String** | unit | sf | acre | [optional] 
 **minSize** | **Int** |  | [optional] 
 **maxSize** | **Int** |  | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

