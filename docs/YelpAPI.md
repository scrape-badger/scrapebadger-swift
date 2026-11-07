# YelpAPI

All URIs are relative to *https://scrapebadger.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**yelpListMarkets**](YelpAPI.md#yelplistmarkets) | **GET** /v1/yelp/markets | List markets
[**yelpSearchBusinesses**](YelpAPI.md#yelpsearchbusinesses) | **GET** /v1/yelp/search | Search businesses


# **yelpListMarkets**
```swift
    open class func yelpListMarkets(completion: @escaping (_ data: YelpMarketsResponse?, _ error: Error?) -> Void)
```

List markets

Yelp sites this API verifiably searches. Free.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// List markets
YelpAPI.yelpListMarkets() { (response, error) in
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

[**YelpMarketsResponse**](YelpMarketsResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **yelpSearchBusinesses**
```swift
    open class func yelpSearchBusinesses(location: String, query: String? = nil, market: Market_yelpSearchBusinesses? = nil, category: String? = nil, sortBy: SortBy_yelpSearchBusinesses? = nil, price: String? = nil, features: String? = nil, page: Int? = nil, completion: @escaping (_ data: YelpSearchResponse?, _ error: Error?) -> Void)
```

Search businesses

Ranked Yelp businesses for a location, with ads kept separate. 15 credits; empty results free.  Ten businesses per page, pages 1-11. Narrow the location, category or filters to reach more businesses. Business detail and reviews are not part of this API.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let location = "location_example" // String | Where to search, as typed into Yelp: city, neighbourhood, address or postcode.
let query = "query_example" // String | What to search for (e.g. pizza, plumbers). Optional when category is set. (optional)
let market = "market_example" // String | Yelp site to search; see /markets. (optional) (default to .us)
let category = "category_example" // String | Yelp category alias, e.g. pizza, coffee, plumbing. (optional)
let sortBy = "sortBy_example" // String |  (optional) (default to .recommended)
let price = "price_example" // String | Comma-separated price levels 1-4 ($ to $$$$). (optional)
let features = "features_example" // String | Comma-separated refinements: delivery, takeout, reservations, outdoor_seating, good_for_kids, dogs_allowed, free_wifi, wheelchair_accessible. (optional)
let page = 987 // Int | 1-based page, ten businesses each; pages 1-11. (optional) (default to 1)

// Search businesses
YelpAPI.yelpSearchBusinesses(location: location, query: query, market: market, category: category, sortBy: sortBy, price: price, features: features, page: page) { (response, error) in
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
 **location** | **String** | Where to search, as typed into Yelp: city, neighbourhood, address or postcode. | 
 **query** | **String** | What to search for (e.g. pizza, plumbers). Optional when category is set. | [optional] 
 **market** | **String** | Yelp site to search; see /markets. | [optional] [default to .us]
 **category** | **String** | Yelp category alias, e.g. pizza, coffee, plumbing. | [optional] 
 **sortBy** | **String** |  | [optional] [default to .recommended]
 **price** | **String** | Comma-separated price levels 1-4 ($ to $$$$). | [optional] 
 **features** | **String** | Comma-separated refinements: delivery, takeout, reservations, outdoor_seating, good_for_kids, dogs_allowed, free_wifi, wheelchair_accessible. | [optional] 
 **page** | **Int** | 1-based page, ten businesses each; pages 1-11. | [optional] [default to 1]

### Return type

[**YelpSearchResponse**](YelpSearchResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

