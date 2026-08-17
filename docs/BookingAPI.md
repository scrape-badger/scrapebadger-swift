# BookingAPI

All URIs are relative to *https://scrapebadger.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**bookingBookingScraperHealthCheck**](BookingAPI.md#bookingbookingscraperhealthcheck) | **GET** /v1/booking/health | Booking scraper health check
[**bookingBookingScraperHealthCheckHead**](BookingAPI.md#bookingbookingscraperhealthcheckhead) | **HEAD** /v1/booking/health | Booking scraper health check
[**bookingGetPropertyDetail**](BookingAPI.md#bookinggetpropertydetail) | **GET** /v1/booking/properties/{country_code}/{slug} | Get property detail
[**bookingGetPropertyReviews**](BookingAPI.md#bookinggetpropertyreviews) | **GET** /v1/booking/properties/{country_code}/{slug}/reviews | Get property reviews
[**bookingSearchDestinations**](BookingAPI.md#bookingsearchdestinations) | **GET** /v1/booking/destinations | Search destinations
[**bookingSearchProperties**](BookingAPI.md#bookingsearchproperties) | **GET** /v1/booking/search | Search properties


# **bookingBookingScraperHealthCheck**
```swift
    open class func bookingBookingScraperHealthCheck(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Booking scraper health check

Check health of the Booking scraper service (accepts HEAD).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// Booking scraper health check
BookingAPI.bookingBookingScraperHealthCheck() { (response, error) in
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

# **bookingBookingScraperHealthCheckHead**
```swift
    open class func bookingBookingScraperHealthCheckHead(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Booking scraper health check

Check health of the Booking scraper service (accepts HEAD).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// Booking scraper health check
BookingAPI.bookingBookingScraperHealthCheckHead() { (response, error) in
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

# **bookingGetPropertyDetail**
```swift
    open class func bookingGetPropertyDetail(countryCode: String, slug: String, photos: Int? = nil, questions: Int? = nil, language: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get property detail

Full detail for one property: description, address and coordinates, star rating, review score with per-category breakdown, facilities, house rules, room types with occupancy and beds, photos and guest Q&A.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let countryCode = "countryCode_example" // String | Two-letter country code, e.g. 'it'
let slug = "slug_example" // String | Booking page name, e.g. 'hotel-artemide'
let photos = 987 // Int | Gallery photos to return (optional) (default to 40)
let questions = 987 // Int | Guest Q&A pairs to return (optional) (default to 10)
let language = "language_example" // String | Locale, e.g. en-us, fr (optional)

// Get property detail
BookingAPI.bookingGetPropertyDetail(countryCode: countryCode, slug: slug, photos: photos, questions: questions, language: language) { (response, error) in
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
 **countryCode** | **String** | Two-letter country code, e.g. &#39;it&#39; | 
 **slug** | **String** | Booking page name, e.g. &#39;hotel-artemide&#39; | 
 **photos** | **Int** | Gallery photos to return | [optional] [default to 40]
 **questions** | **Int** | Guest Q&amp;A pairs to return | [optional] [default to 10]
 **language** | **String** | Locale, e.g. en-us, fr | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **bookingGetPropertyReviews**
```swift
    open class func bookingGetPropertyReviews(countryCode: String, slug: String, limit: Int? = nil, offset: Int? = nil, sort: String? = nil, reviewLanguage: String? = nil, guestType: String? = nil, language: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get property reviews

Paginated guest reviews with score, positive and negative text, stay dates, room type, guest country and type, photos and the partner's reply.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let countryCode = "countryCode_example" // String | Two-letter country code, e.g. 'it'
let slug = "slug_example" // String | Booking page name, e.g. 'hotel-artemide'
let limit = 987 // Int |  (optional) (default to 25)
let offset = 987 // Int |  (optional) (default to 0)
let sort = "sort_example" // String | MOST_RELEVANT | NEWEST_FIRST | OLDEST_FIRST | SCORE_DESC | SCORE_ASC (optional) (default to "MOST_RELEVANT")
let reviewLanguage = "reviewLanguage_example" // String | Only reviews written in this language, e.g. 'fr' (optional)
let guestType = "guestType_example" // String | FAMILIES | COUPLES | GROUP_OF_FRIENDS | SOLO_TRAVELLERS | BUSINESS_TRAVELLERS (optional)
let language = "language_example" // String | Locale for labels, e.g. en-us (optional)

// Get property reviews
BookingAPI.bookingGetPropertyReviews(countryCode: countryCode, slug: slug, limit: limit, offset: offset, sort: sort, reviewLanguage: reviewLanguage, guestType: guestType, language: language) { (response, error) in
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
 **countryCode** | **String** | Two-letter country code, e.g. &#39;it&#39; | 
 **slug** | **String** | Booking page name, e.g. &#39;hotel-artemide&#39; | 
 **limit** | **Int** |  | [optional] [default to 25]
 **offset** | **Int** |  | [optional] [default to 0]
 **sort** | **String** | MOST_RELEVANT | NEWEST_FIRST | OLDEST_FIRST | SCORE_DESC | SCORE_ASC | [optional] [default to &quot;MOST_RELEVANT&quot;]
 **reviewLanguage** | **String** | Only reviews written in this language, e.g. &#39;fr&#39; | [optional] 
 **guestType** | **String** | FAMILIES | COUPLES | GROUP_OF_FRIENDS | SOLO_TRAVELLERS | BUSINESS_TRAVELLERS | [optional] 
 **language** | **String** | Locale for labels, e.g. en-us | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **bookingSearchDestinations**
```swift
    open class func bookingSearchDestinations(query: String, limit: Int? = nil, language: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Search destinations

Resolve a place name to Booking's `dest_id`/`dest_type`, with coordinates and country — feed the pair back into /search for an exact match.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let query = "query_example" // String | Free-text place, e.g. 'amsterd'
let limit = 987 // Int |  (optional) (default to 8)
let language = "language_example" // String | Locale, e.g. en-us, fr (optional)

// Search destinations
BookingAPI.bookingSearchDestinations(query: query, limit: limit, language: language) { (response, error) in
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
 **query** | **String** | Free-text place, e.g. &#39;amsterd&#39; | 
 **limit** | **Int** |  | [optional] [default to 8]
 **language** | **String** | Locale, e.g. en-us, fr | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **bookingSearchProperties**
```swift
    open class func bookingSearchProperties(location: String? = nil, destId: Int? = nil, destType: String? = nil, checkin: String? = nil, checkout: String? = nil, adults: Int? = nil, children: String? = nil, rooms: Int? = nil, offset: Int? = nil, limit: Int? = nil, sort: String? = nil, filters: String? = nil, currency: String? = nil, language: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Search properties

Search Booking.com properties by destination, with dates, occupancy, sorting and filters. Returns prices, review scores, coordinates, room configuration and photos. Paginate with `offset`.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let location = "location_example" // String | Free-text destination, e.g. 'Rome' (optional)
let destId = 987 // Int | Exact destination id (ufi) from /destinations (optional)
let destType = "destType_example" // String | Destination type, e.g. CITY (optional) (default to "NO_DEST_TYPE")
let checkin = "checkin_example" // String | Check-in date YYYY-MM-DD (optional)
let checkout = "checkout_example" // String | Check-out date YYYY-MM-DD (optional)
let adults = 987 // Int |  (optional) (default to 2)
let children = "children_example" // String | Comma-separated children ages, e.g. '4,9' (optional)
let rooms = 987 // Int |  (optional) (default to 1)
let offset = 987 // Int | Result offset for pagination (optional) (default to 0)
let limit = 987 // Int |  (optional) (default to 25)
let sort = "sort_example" // String | popularity | price | class_descending | class_ascending | distance_from_search | bayesian_review_score | review_score_and_price | upsort_bh (optional)
let filters = "filters_example" // String | Semicolon-separated Booking filter ids, e.g. 'class=4' (optional)
let currency = "currency_example" // String | ISO currency, e.g. EUR, USD, GBP (optional)
let language = "language_example" // String | Locale, e.g. en-us, fr, de, es (optional)

// Search properties
BookingAPI.bookingSearchProperties(location: location, destId: destId, destType: destType, checkin: checkin, checkout: checkout, adults: adults, children: children, rooms: rooms, offset: offset, limit: limit, sort: sort, filters: filters, currency: currency, language: language) { (response, error) in
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
 **location** | **String** | Free-text destination, e.g. &#39;Rome&#39; | [optional] 
 **destId** | **Int** | Exact destination id (ufi) from /destinations | [optional] 
 **destType** | **String** | Destination type, e.g. CITY | [optional] [default to &quot;NO_DEST_TYPE&quot;]
 **checkin** | **String** | Check-in date YYYY-MM-DD | [optional] 
 **checkout** | **String** | Check-out date YYYY-MM-DD | [optional] 
 **adults** | **Int** |  | [optional] [default to 2]
 **children** | **String** | Comma-separated children ages, e.g. &#39;4,9&#39; | [optional] 
 **rooms** | **Int** |  | [optional] [default to 1]
 **offset** | **Int** | Result offset for pagination | [optional] [default to 0]
 **limit** | **Int** |  | [optional] [default to 25]
 **sort** | **String** | popularity | price | class_descending | class_ascending | distance_from_search | bayesian_review_score | review_score_and_price | upsort_bh | [optional] 
 **filters** | **String** | Semicolon-separated Booking filter ids, e.g. &#39;class&#x3D;4&#39; | [optional] 
 **currency** | **String** | ISO currency, e.g. EUR, USD, GBP | [optional] 
 **language** | **String** | Locale, e.g. en-us, fr, de, es | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

