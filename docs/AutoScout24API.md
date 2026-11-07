# AutoScout24API

All URIs are relative to *https://scrapebadger.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**autoscout24CheckAutoscout24Health**](AutoScout24API.md#autoscout24checkautoscout24health) | **GET** /v1/autoscout24/health | Check AutoScout24 health
[**autoscout24ListMarkets**](AutoScout24API.md#autoscout24listmarkets) | **GET** /v1/autoscout24/markets | List markets
[**autoscout24ListSearchFilters**](AutoScout24API.md#autoscout24listsearchfilters) | **GET** /v1/autoscout24/filters | List search filters
[**autoscout24SearchVehicles**](AutoScout24API.md#autoscout24searchvehicles) | **GET** /v1/autoscout24/search | Search vehicles


# **autoscout24CheckAutoscout24Health**
```swift
    open class func autoscout24CheckAutoscout24Health(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Check AutoScout24 health

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// Check AutoScout24 health
AutoScout24API.autoscout24CheckAutoscout24Health() { (response, error) in
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

# **autoscout24ListMarkets**
```swift
    open class func autoscout24ListMarkets(completion: @escaping (_ data: AutoScout24MarketsResponse?, _ error: Error?) -> Void)
```

List markets

Verified marketplaces, domains, languages and currency. Free reference endpoint.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// List markets
AutoScout24API.autoscout24ListMarkets() { (response, error) in
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

[**AutoScout24MarketsResponse**](AutoScout24MarketsResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **autoscout24ListSearchFilters**
```swift
    open class func autoscout24ListSearchFilters(market: Market_autoscout24ListSearchFilters? = nil, make: String? = nil, completion: @escaping (_ data: AutoScout24FiltersResponse?, _ error: Error?) -> Void)
```

List search filters

Current native make, model and vehicle filter options. Set make for its models.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let market = "market_example" // String |  (optional) (default to .de)
let make = "make_example" // String |  (optional)

// List search filters
AutoScout24API.autoscout24ListSearchFilters(market: market, make: make) { (response, error) in
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
 **market** | **String** |  | [optional] [default to .de]
 **make** | **String** |  | [optional] 

### Return type

[**AutoScout24FiltersResponse**](AutoScout24FiltersResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **autoscout24SearchVehicles**
```swift
    open class func autoscout24SearchVehicles(market: Market_autoscout24SearchVehicles? = nil, make: String? = nil, model: String? = nil, priceMin: Int? = nil, priceMax: Int? = nil, mileageMin: Int? = nil, mileageMax: Int? = nil, yearMin: Int? = nil, yearMax: Int? = nil, powerMin: Int? = nil, powerMax: Int? = nil, fuelType: FuelType_autoscout24SearchVehicles? = nil, transmission: Transmission_autoscout24SearchVehicles? = nil, bodyType: BodyType_autoscout24SearchVehicles? = nil, sellerType: SellerType_autoscout24SearchVehicles? = nil, condition: Condition_autoscout24SearchVehicles? = nil, zip: String? = nil, radius: Int? = nil, sortBy: SortBy_autoscout24SearchVehicles? = nil, page: Int? = nil, completion: @escaping (_ data: AutoScout24SearchResponse?, _ error: Error?) -> Void)
```

Search vehicles

Search live vehicle cards, seller/location information and current filter taxonomy.  Browsing is capped at 200 pages (normally 20 cards each). Narrow the query to reach more inventory. Empty results cost zero credits. Listing detail is not included in this API.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let market = "market_example" // String |  (optional) (default to .de)
let make = "make_example" // String | Native make slug, e.g. volkswagen or bmw. (optional)
let model = "model_example" // String | Native model slug, e.g. golf. Requires make. (optional)
let priceMin = 987 // Int |  (optional)
let priceMax = 987 // Int |  (optional)
let mileageMin = 987 // Int | Kilometres. (optional)
let mileageMax = 987 // Int |  (optional)
let yearMin = 987 // Int |  (optional)
let yearMax = 987 // Int |  (optional)
let powerMin = 987 // Int | Engine power in kW. (optional)
let powerMax = 987 // Int |  (optional)
let fuelType = "fuelType_example" // String |  (optional)
let transmission = "transmission_example" // String |  (optional)
let bodyType = "bodyType_example" // String |  (optional)
let sellerType = "sellerType_example" // String |  (optional)
let condition = "condition_example" // String |  (optional)
let zip = "zip_example" // String | Postal code in the requested market. (optional)
let radius = 987 // Int | Kilometres; requires zip. (optional)
let sortBy = "sortBy_example" // String |  (optional) (default to .bestMatch)
let page = 987 // Int |  (optional) (default to 1)

// Search vehicles
AutoScout24API.autoscout24SearchVehicles(market: market, make: make, model: model, priceMin: priceMin, priceMax: priceMax, mileageMin: mileageMin, mileageMax: mileageMax, yearMin: yearMin, yearMax: yearMax, powerMin: powerMin, powerMax: powerMax, fuelType: fuelType, transmission: transmission, bodyType: bodyType, sellerType: sellerType, condition: condition, zip: zip, radius: radius, sortBy: sortBy, page: page) { (response, error) in
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
 **market** | **String** |  | [optional] [default to .de]
 **make** | **String** | Native make slug, e.g. volkswagen or bmw. | [optional] 
 **model** | **String** | Native model slug, e.g. golf. Requires make. | [optional] 
 **priceMin** | **Int** |  | [optional] 
 **priceMax** | **Int** |  | [optional] 
 **mileageMin** | **Int** | Kilometres. | [optional] 
 **mileageMax** | **Int** |  | [optional] 
 **yearMin** | **Int** |  | [optional] 
 **yearMax** | **Int** |  | [optional] 
 **powerMin** | **Int** | Engine power in kW. | [optional] 
 **powerMax** | **Int** |  | [optional] 
 **fuelType** | **String** |  | [optional] 
 **transmission** | **String** |  | [optional] 
 **bodyType** | **String** |  | [optional] 
 **sellerType** | **String** |  | [optional] 
 **condition** | **String** |  | [optional] 
 **zip** | **String** | Postal code in the requested market. | [optional] 
 **radius** | **Int** | Kilometres; requires zip. | [optional] 
 **sortBy** | **String** |  | [optional] [default to .bestMatch]
 **page** | **Int** |  | [optional] [default to 1]

### Return type

[**AutoScout24SearchResponse**](AutoScout24SearchResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

