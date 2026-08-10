# ApartmentsAPI

All URIs are relative to *https://scrapebadger.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**apartmentsApartmentsScraperHealthCheck**](ApartmentsAPI.md#apartmentsapartmentsscraperhealthcheck) | **GET** /v1/apartments/health | Apartments scraper health check
[**apartmentsApartmentsScraperHealthCheckHead**](ApartmentsAPI.md#apartmentsapartmentsscraperhealthcheckhead) | **HEAD** /v1/apartments/health | Apartments scraper health check
[**apartmentsGetPropertyDetailBySlugId**](ApartmentsAPI.md#apartmentsgetpropertydetailbyslugid) | **GET** /v1/apartments/properties/{slug}/{property_id} | Get property detail by slug + id
[**apartmentsGetPropertyDetailByUrl**](ApartmentsAPI.md#apartmentsgetpropertydetailbyurl) | **GET** /v1/apartments/property | Get property detail by URL
[**apartmentsSearchRentalListings**](ApartmentsAPI.md#apartmentssearchrentallistings) | **GET** /v1/apartments/search | Search rental listings


# **apartmentsApartmentsScraperHealthCheck**
```swift
    open class func apartmentsApartmentsScraperHealthCheck(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Apartments scraper health check

Check health of the Apartments scraper service (accepts HEAD for UptimeRobot).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// Apartments scraper health check
ApartmentsAPI.apartmentsApartmentsScraperHealthCheck() { (response, error) in
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

# **apartmentsApartmentsScraperHealthCheckHead**
```swift
    open class func apartmentsApartmentsScraperHealthCheckHead(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Apartments scraper health check

Check health of the Apartments scraper service (accepts HEAD for UptimeRobot).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// Apartments scraper health check
ApartmentsAPI.apartmentsApartmentsScraperHealthCheckHead() { (response, error) in
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

# **apartmentsGetPropertyDetailBySlugId**
```swift
    open class func apartmentsGetPropertyDetailBySlugId(slug: String, propertyId: String, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get property detail by slug + id

Get a property by its SEO slug and 7-character listing id.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let slug = "slug_example" // String | 
let propertyId = "propertyId_example" // String | 

// Get property detail by slug + id
ApartmentsAPI.apartmentsGetPropertyDetailBySlugId(slug: slug, propertyId: propertyId) { (response, error) in
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
 **propertyId** | **String** |  | 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **apartmentsGetPropertyDetailByUrl**
```swift
    open class func apartmentsGetPropertyDetailByUrl(url: String, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get property detail by URL

Get an apartments.com property with full per-unit pricing and availability.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let url = "url_example" // String | Full apartments.com property URL, e.g. https://www.apartments.com/urbane-kansas-city-mo/wcd6e5k/

// Get property detail by URL
ApartmentsAPI.apartmentsGetPropertyDetailByUrl(url: url) { (response, error) in
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
 **url** | **String** | Full apartments.com property URL, e.g. https://www.apartments.com/urbane-kansas-city-mo/wcd6e5k/ | 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **apartmentsSearchRentalListings**
```swift
    open class func apartmentsSearchRentalListings(location: String, page: Int? = nil, beds: Int? = nil, minPrice: Int? = nil, maxPrice: Int? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Search rental listings

Search apartments.com for rental properties. 40 cards per page.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let location = "location_example" // String | apartments.com location slug, e.g. 'kansas-city-mo'
let page = 987 // Int |  (optional) (default to 1)
let beds = 987 // Int | 0=studio, 1-4 bedrooms (optional)
let minPrice = 987 // Int |  (optional)
let maxPrice = 987 // Int |  (optional)

// Search rental listings
ApartmentsAPI.apartmentsSearchRentalListings(location: location, page: page, beds: beds, minPrice: minPrice, maxPrice: maxPrice) { (response, error) in
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
 **location** | **String** | apartments.com location slug, e.g. &#39;kansas-city-mo&#39; | 
 **page** | **Int** |  | [optional] [default to 1]
 **beds** | **Int** | 0&#x3D;studio, 1-4 bedrooms | [optional] 
 **minPrice** | **Int** |  | [optional] 
 **maxPrice** | **Int** |  | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

