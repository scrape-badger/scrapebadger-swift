# AirbnbAPI

All URIs are relative to *https://scrapebadger.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**airbnbAirbnbScraperHealthCheck**](AirbnbAPI.md#airbnbairbnbscraperhealthcheck) | **GET** /v1/airbnb/health | Airbnb scraper health check
[**airbnbAirbnbScraperHealthCheckHead**](AirbnbAPI.md#airbnbairbnbscraperhealthcheckhead) | **HEAD** /v1/airbnb/health | Airbnb scraper health check
[**airbnbGetAvailabilityCalendar**](AirbnbAPI.md#airbnbgetavailabilitycalendar) | **GET** /v1/airbnb/listings/{room_id}/calendar | Get availability calendar
[**airbnbGetExperienceDetail**](AirbnbAPI.md#airbnbgetexperiencedetail) | **GET** /v1/airbnb/experiences/{experience_id} | Get experience detail
[**airbnbGetListingDetail**](AirbnbAPI.md#airbnbgetlistingdetail) | **GET** /v1/airbnb/listings/{room_id} | Get listing detail
[**airbnbGetListingReviews**](AirbnbAPI.md#airbnbgetlistingreviews) | **GET** /v1/airbnb/listings/{room_id}/reviews | Get listing reviews
[**airbnbSearchExperiences**](AirbnbAPI.md#airbnbsearchexperiences) | **GET** /v1/airbnb/experiences | Search experiences
[**airbnbSearchStays**](AirbnbAPI.md#airbnbsearchstays) | **GET** /v1/airbnb/search | Search stays


# **airbnbAirbnbScraperHealthCheck**
```swift
    open class func airbnbAirbnbScraperHealthCheck(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Airbnb scraper health check

Check health of the Airbnb scraper service (accepts HEAD).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// Airbnb scraper health check
AirbnbAPI.airbnbAirbnbScraperHealthCheck() { (response, error) in
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

# **airbnbAirbnbScraperHealthCheckHead**
```swift
    open class func airbnbAirbnbScraperHealthCheckHead(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Airbnb scraper health check

Check health of the Airbnb scraper service (accepts HEAD).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// Airbnb scraper health check
AirbnbAPI.airbnbAirbnbScraperHealthCheckHead() { (response, error) in
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

# **airbnbGetAvailabilityCalendar**
```swift
    open class func airbnbGetAvailabilityCalendar(roomId: String, month: Int? = nil, year: Int? = nil, months: Int? = nil, currency: String? = nil, locale: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get availability calendar

Day-by-day availability for up to 12 months: bookable, check-in/out windows and min/max nights per date.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let roomId = "roomId_example" // String | 
let month = 987 // Int | Start month (1-12) (optional) (default to 1)
let year = 987 // Int | Start year (optional) (default to 2026)
let months = 987 // Int | Number of months (max 12) (optional) (default to 12)
let currency = "currency_example" // String |  (optional)
let locale = "locale_example" // String |  (optional)

// Get availability calendar
AirbnbAPI.airbnbGetAvailabilityCalendar(roomId: roomId, month: month, year: year, months: months, currency: currency, locale: locale) { (response, error) in
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
 **roomId** | **String** |  | 
 **month** | **Int** | Start month (1-12) | [optional] [default to 1]
 **year** | **Int** | Start year | [optional] [default to 2026]
 **months** | **Int** | Number of months (max 12) | [optional] [default to 12]
 **currency** | **String** |  | [optional] 
 **locale** | **String** |  | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **airbnbGetExperienceDetail**
```swift
    open class func airbnbGetExperienceDetail(experienceId: String, adults: Int? = nil, children: Int? = nil, infants: Int? = nil, currency: String? = nil, locale: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get experience detail

Full detail for one experience: description, rating, host, location and photos.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let experienceId = "experienceId_example" // String | 
let adults = 987 // Int |  (optional) (default to 1)
let children = 987 // Int |  (optional) (default to 0)
let infants = 987 // Int |  (optional) (default to 0)
let currency = "currency_example" // String |  (optional)
let locale = "locale_example" // String |  (optional)

// Get experience detail
AirbnbAPI.airbnbGetExperienceDetail(experienceId: experienceId, adults: adults, children: children, infants: infants, currency: currency, locale: locale) { (response, error) in
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
 **experienceId** | **String** |  | 
 **adults** | **Int** |  | [optional] [default to 1]
 **children** | **Int** |  | [optional] [default to 0]
 **infants** | **Int** |  | [optional] [default to 0]
 **currency** | **String** |  | [optional] 
 **locale** | **String** |  | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **airbnbGetListingDetail**
```swift
    open class func airbnbGetListingDetail(roomId: String, adults: Int? = nil, currency: String? = nil, locale: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get listing detail

Full detail for one listing: amenities, house rules, host, ratings, coordinates and photos.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let roomId = "roomId_example" // String | 
let adults = 987 // Int |  (optional) (default to 1)
let currency = "currency_example" // String |  (optional)
let locale = "locale_example" // String |  (optional)

// Get listing detail
AirbnbAPI.airbnbGetListingDetail(roomId: roomId, adults: adults, currency: currency, locale: locale) { (response, error) in
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
 **roomId** | **String** |  | 
 **adults** | **Int** |  | [optional] [default to 1]
 **currency** | **String** |  | [optional] 
 **locale** | **String** |  | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **airbnbGetListingReviews**
```swift
    open class func airbnbGetListingReviews(roomId: String, limit: Int? = nil, offset: Int? = nil, sort: String? = nil, currency: String? = nil, locale: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get listing reviews

Paginated guest reviews with reviewer, rating, date, text and host response.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let roomId = "roomId_example" // String | 
let limit = 987 // Int |  (optional) (default to 24)
let offset = 987 // Int |  (optional) (default to 0)
let sort = "sort_example" // String | MOST_RECENT | RATING_DESC | RATING_ASC (optional) (default to "MOST_RECENT")
let currency = "currency_example" // String |  (optional)
let locale = "locale_example" // String |  (optional)

// Get listing reviews
AirbnbAPI.airbnbGetListingReviews(roomId: roomId, limit: limit, offset: offset, sort: sort, currency: currency, locale: locale) { (response, error) in
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
 **roomId** | **String** |  | 
 **limit** | **Int** |  | [optional] [default to 24]
 **offset** | **Int** |  | [optional] [default to 0]
 **sort** | **String** | MOST_RECENT | RATING_DESC | RATING_ASC | [optional] [default to &quot;MOST_RECENT&quot;]
 **currency** | **String** |  | [optional] 
 **locale** | **String** |  | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **airbnbSearchExperiences**
```swift
    open class func airbnbSearchExperiences(location: String, cursor: String? = nil, currency: String? = nil, locale: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Search experiences

Search Airbnb Experiences by location.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let location = "location_example" // String | Free-text place, e.g. 'Rome, Italy'
let cursor = "cursor_example" // String | next_page_cursor from a prior response (optional)
let currency = "currency_example" // String |  (optional)
let locale = "locale_example" // String |  (optional)

// Search experiences
AirbnbAPI.airbnbSearchExperiences(location: location, cursor: cursor, currency: currency, locale: locale) { (response, error) in
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
 **location** | **String** | Free-text place, e.g. &#39;Rome, Italy&#39; | 
 **cursor** | **String** | next_page_cursor from a prior response | [optional] 
 **currency** | **String** |  | [optional] 
 **locale** | **String** |  | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **airbnbSearchStays**
```swift
    open class func airbnbSearchStays(location: String? = nil, neLat: Double? = nil, neLng: Double? = nil, swLat: Double? = nil, swLng: Double? = nil, checkIn: String? = nil, checkOut: String? = nil, adults: Int? = nil, children: Int? = nil, infants: Int? = nil, pets: Int? = nil, priceMin: Int? = nil, priceMax: Int? = nil, minBedrooms: Int? = nil, minBeds: Int? = nil, minBathrooms: Int? = nil, roomType: String? = nil, cursor: String? = nil, limit: Int? = nil, currency: String? = nil, locale: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Search stays

Search Airbnb stays by place name and/or map bounding box, with dates, guests, price and property filters. Paginate with the `cursor`.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let location = "location_example" // String | Free-text place, e.g. 'Paris, France' (optional)
let neLat = 987 // Double | Map bounding-box NE latitude (optional)
let neLng = 987 // Double | Map bounding-box NE longitude (optional)
let swLat = 987 // Double | Map bounding-box SW latitude (optional)
let swLng = 987 // Double | Map bounding-box SW longitude (optional)
let checkIn = "checkIn_example" // String | Check-in date YYYY-MM-DD (optional)
let checkOut = "checkOut_example" // String | Check-out date YYYY-MM-DD (optional)
let adults = 987 // Int |  (optional) (default to 1)
let children = 987 // Int |  (optional) (default to 0)
let infants = 987 // Int |  (optional) (default to 0)
let pets = 987 // Int |  (optional) (default to 0)
let priceMin = 987 // Int |  (optional)
let priceMax = 987 // Int |  (optional)
let minBedrooms = 987 // Int |  (optional)
let minBeds = 987 // Int |  (optional)
let minBathrooms = 987 // Int |  (optional)
let roomType = "roomType_example" // String | e.g. 'Entire home/apt', 'Private room' (optional)
let cursor = "cursor_example" // String | next_page_cursor from a prior response (optional)
let limit = 987 // Int |  (optional) (default to 18)
let currency = "currency_example" // String | ISO currency, e.g. USD, EUR (optional)
let locale = "locale_example" // String | Locale, e.g. en, fr (optional)

// Search stays
AirbnbAPI.airbnbSearchStays(location: location, neLat: neLat, neLng: neLng, swLat: swLat, swLng: swLng, checkIn: checkIn, checkOut: checkOut, adults: adults, children: children, infants: infants, pets: pets, priceMin: priceMin, priceMax: priceMax, minBedrooms: minBedrooms, minBeds: minBeds, minBathrooms: minBathrooms, roomType: roomType, cursor: cursor, limit: limit, currency: currency, locale: locale) { (response, error) in
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
 **location** | **String** | Free-text place, e.g. &#39;Paris, France&#39; | [optional] 
 **neLat** | **Double** | Map bounding-box NE latitude | [optional] 
 **neLng** | **Double** | Map bounding-box NE longitude | [optional] 
 **swLat** | **Double** | Map bounding-box SW latitude | [optional] 
 **swLng** | **Double** | Map bounding-box SW longitude | [optional] 
 **checkIn** | **String** | Check-in date YYYY-MM-DD | [optional] 
 **checkOut** | **String** | Check-out date YYYY-MM-DD | [optional] 
 **adults** | **Int** |  | [optional] [default to 1]
 **children** | **Int** |  | [optional] [default to 0]
 **infants** | **Int** |  | [optional] [default to 0]
 **pets** | **Int** |  | [optional] [default to 0]
 **priceMin** | **Int** |  | [optional] 
 **priceMax** | **Int** |  | [optional] 
 **minBedrooms** | **Int** |  | [optional] 
 **minBeds** | **Int** |  | [optional] 
 **minBathrooms** | **Int** |  | [optional] 
 **roomType** | **String** | e.g. &#39;Entire home/apt&#39;, &#39;Private room&#39; | [optional] 
 **cursor** | **String** | next_page_cursor from a prior response | [optional] 
 **limit** | **Int** |  | [optional] [default to 18]
 **currency** | **String** | ISO currency, e.g. USD, EUR | [optional] 
 **locale** | **String** | Locale, e.g. en, fr | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

