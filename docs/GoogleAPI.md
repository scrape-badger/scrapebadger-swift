# GoogleAPI

All URIs are relative to *https://scrapebadger.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**googleGetAuthorCitationsPerYearChart**](GoogleAPI.md#googlegetauthorcitationsperyearchart) | **GET** /v1/google/scholar/author/citation | Get author citations-per-year chart
[**googleGetBusinessPosts**](GoogleAPI.md#googlegetbusinessposts) | **GET** /v1/google/maps/posts | Get business posts
[**googleGetCitationFormatsForAScholarPaper**](GoogleAPI.md#googlegetcitationformatsforascholarpaper) | **GET** /v1/google/scholar/cite | Get citation formats for a Scholar paper
[**googleGetPlaceDetails**](GoogleAPI.md#googlegetplacedetails) | **GET** /v1/google/maps/place | Get place details
[**googleGetPlacePhotos**](GoogleAPI.md#googlegetplacephotos) | **GET** /v1/google/maps/photos | Get place photos
[**googleGetPlaceReviews**](GoogleAPI.md#googlegetplacereviews) | **GET** /v1/google/maps/reviews | Get place reviews
[**googleGetScholarAuthorProfile**](GoogleAPI.md#googlegetscholarauthorprofile) | **GET** /v1/google/scholar/author | Get Scholar author profile
[**googleGetStockIndexQuote**](GoogleAPI.md#googlegetstockindexquote) | **GET** /v1/google/finance/quote | Get stock/index quote
[**googleGoogleAiModeSearch**](GoogleAPI.md#googlegoogleaimodesearch) | **GET** /v1/google/ai-mode/search | Google AI Mode search
[**googleGoogleAiOverviewInlineSerpBlock**](GoogleAPI.md#googlegoogleaioverviewinlineserpblock) | **GET** /v1/google/ai-overview | Google AI Overview (inline SERP block)
[**googleGoogleFlightsCalendarCheapestFarePerDate**](GoogleAPI.md#googlegoogleflightscalendarcheapestfareperdate) | **GET** /v1/google/flights/calendar | Google Flights calendar — cheapest fare per date
[**googleGoogleFlightsSearch**](GoogleAPI.md#googlegoogleflightssearch) | **GET** /v1/google/flights/search | Google Flights search
[**googleGoogleLensVisualSearch**](GoogleAPI.md#googlegooglelensvisualsearch) | **GET** /v1/google/lens/search | Google Lens visual search
[**googleGoogleScraperHealthCheck**](GoogleAPI.md#googlegooglescraperhealthcheck) | **GET** /v1/google/health | Google scraper health check
[**googleGoogleScraperHealthCheckHead**](GoogleAPI.md#googlegooglescraperhealthcheckhead) | **HEAD** /v1/google/health | Google scraper health check
[**googleGoogleSearchSuggestions**](GoogleAPI.md#googlegooglesearchsuggestions) | **GET** /v1/google/autocomplete | Google search suggestions
[**googleGoogleShortsSearch**](GoogleAPI.md#googlegoogleshortssearch) | **GET** /v1/google/shorts/search | Google Shorts search
[**googleGoogleWebSearch**](GoogleAPI.md#googlegooglewebsearch) | **GET** /v1/google/search | Google web search
[**googleHotelDetails**](GoogleAPI.md#googlehoteldetails) | **GET** /v1/google/hotels/details | Hotel details
[**googleImmersiveProductDetail**](GoogleAPI.md#googleimmersiveproductdetail) | **GET** /v1/google/products/detail | Immersive product detail
[**googleInterestByRegion**](GoogleAPI.md#googleinterestbyregion) | **GET** /v1/google/trends/regions | Interest by region
[**googleInterestOverTime**](GoogleAPI.md#googleinterestovertime) | **GET** /v1/google/trends/interest | Interest over time
[**googleMultiSellerOffersByBarcode**](GoogleAPI.md#googlemultiselleroffersbybarcode) | **GET** /v1/google/shopping/offers | Multi-seller offers by barcode
[**googleNewsByTopic**](GoogleAPI.md#googlenewsbytopic) | **GET** /v1/google/news/topics | News by topic
[**googlePatentDetails**](GoogleAPI.md#googlepatentdetails) | **GET** /v1/google/patents/detail | Patent details
[**googleRelatedTopicsQueries**](GoogleAPI.md#googlerelatedtopicsqueries) | **GET** /v1/google/trends/related | Related topics &amp; queries
[**googleSearchGoogleImages**](GoogleAPI.md#googlesearchgoogleimages) | **GET** /v1/google/images/search | Search Google Images
[**googleSearchGoogleJobs**](GoogleAPI.md#googlesearchgooglejobs) | **GET** /v1/google/jobs/search | Search Google Jobs
[**googleSearchGoogleMapsPlaces**](GoogleAPI.md#googlesearchgooglemapsplaces) | **GET** /v1/google/maps/search | Search Google Maps places
[**googleSearchGoogleNews**](GoogleAPI.md#googlesearchgooglenews) | **GET** /v1/google/news/search | Search Google News
[**googleSearchGoogleScholar**](GoogleAPI.md#googlesearchgooglescholar) | **GET** /v1/google/scholar/search | Search Google Scholar
[**googleSearchGoogleVideos**](GoogleAPI.md#googlesearchgooglevideos) | **GET** /v1/google/videos/search | Search Google Videos
[**googleSearchHotels**](GoogleAPI.md#googlesearchhotels) | **GET** /v1/google/hotels/search | Search hotels
[**googleSearchPatents**](GoogleAPI.md#googlesearchpatents) | **GET** /v1/google/patents/search | Search patents
[**googleSearchProducts**](GoogleAPI.md#googlesearchproducts) | **GET** /v1/google/shopping/search | Search products
[**googleSearchScholarAuthorProfiles**](GoogleAPI.md#googlesearchscholarauthorprofiles) | **GET** /v1/google/scholar/profiles | Search Scholar author profiles
[**googleTrendingNews**](GoogleAPI.md#googletrendingnews) | **GET** /v1/google/news/trending | Trending news
[**googleTrendingSearches**](GoogleAPI.md#googletrendingsearches) | **GET** /v1/google/trends/trending | Trending searches
[**googleTrendsTopicAutocomplete**](GoogleAPI.md#googletrendstopicautocomplete) | **GET** /v1/google/trends/autocomplete | Trends topic autocomplete


# **googleGetAuthorCitationsPerYearChart**
```swift
    open class func googleGetAuthorCitationsPerYearChart(authorId: String, hl: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get author citations-per-year chart

Return the citations-per-year chart for a Google Scholar author.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let authorId = "authorId_example" // String | Scholar user ID
let hl = "hl_example" // String | Language code (optional) (default to "en")

// Get author citations-per-year chart
GoogleAPI.googleGetAuthorCitationsPerYearChart(authorId: authorId, hl: hl) { (response, error) in
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
 **authorId** | **String** | Scholar user ID | 
 **hl** | **String** | Language code | [optional] [default to &quot;en&quot;]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **googleGetBusinessPosts**
```swift
    open class func googleGetBusinessPosts(dataId: String, nextPageToken: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get business posts

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let dataId = "dataId_example" // String | Maps data ID
let nextPageToken = "nextPageToken_example" // String |  (optional)

// Get business posts
GoogleAPI.googleGetBusinessPosts(dataId: dataId, nextPageToken: nextPageToken) { (response, error) in
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
 **dataId** | **String** | Maps data ID | 
 **nextPageToken** | **String** |  | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **googleGetCitationFormatsForAScholarPaper**
```swift
    open class func googleGetCitationFormatsForAScholarPaper(q: String, hl: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get citation formats for a Scholar paper

Return MLA, APA, Chicago, Harvard, and Vancouver citation formats for a paper.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let q = "q_example" // String | Cluster ID from a search result
let hl = "hl_example" // String | Language code (optional) (default to "en")

// Get citation formats for a Scholar paper
GoogleAPI.googleGetCitationFormatsForAScholarPaper(q: q, hl: hl) { (response, error) in
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
 **q** | **String** | Cluster ID from a search result | 
 **hl** | **String** | Language code | [optional] [default to &quot;en&quot;]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **googleGetPlaceDetails**
```swift
    open class func googleGetPlaceDetails(placeId: String? = nil, dataId: String? = nil, hl: String? = nil, gl: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get place details

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let placeId = "placeId_example" // String |  (optional)
let dataId = "dataId_example" // String |  (optional)
let hl = "hl_example" // String |  (optional) (default to "en")
let gl = "gl_example" // String |  (optional) (default to "us")

// Get place details
GoogleAPI.googleGetPlaceDetails(placeId: placeId, dataId: dataId, hl: hl, gl: gl) { (response, error) in
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
 **placeId** | **String** |  | [optional] 
 **dataId** | **String** |  | [optional] 
 **hl** | **String** |  | [optional] [default to &quot;en&quot;]
 **gl** | **String** |  | [optional] [default to &quot;us&quot;]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **googleGetPlacePhotos**
```swift
    open class func googleGetPlacePhotos(dataId: String, hl: String? = nil, nextPageToken: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get place photos

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let dataId = "dataId_example" // String | Maps data ID
let hl = "hl_example" // String |  (optional) (default to "en")
let nextPageToken = "nextPageToken_example" // String |  (optional)

// Get place photos
GoogleAPI.googleGetPlacePhotos(dataId: dataId, hl: hl, nextPageToken: nextPageToken) { (response, error) in
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
 **dataId** | **String** | Maps data ID | 
 **hl** | **String** |  | [optional] [default to &quot;en&quot;]
 **nextPageToken** | **String** |  | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **googleGetPlaceReviews**
```swift
    open class func googleGetPlaceReviews(dataId: String, sortBy: String? = nil, hl: String? = nil, nextPageToken: String? = nil, results: Int? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get place reviews

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let dataId = "dataId_example" // String | Maps data ID
let sortBy = "sortBy_example" // String |  (optional) (default to "qualityScore")
let hl = "hl_example" // String |  (optional) (default to "en")
let nextPageToken = "nextPageToken_example" // String |  (optional)
let results = 987 // Int |  (optional) (default to 10)

// Get place reviews
GoogleAPI.googleGetPlaceReviews(dataId: dataId, sortBy: sortBy, hl: hl, nextPageToken: nextPageToken, results: results) { (response, error) in
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
 **dataId** | **String** | Maps data ID | 
 **sortBy** | **String** |  | [optional] [default to &quot;qualityScore&quot;]
 **hl** | **String** |  | [optional] [default to &quot;en&quot;]
 **nextPageToken** | **String** |  | [optional] 
 **results** | **Int** |  | [optional] [default to 10]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **googleGetScholarAuthorProfile**
```swift
    open class func googleGetScholarAuthorProfile(authorId: String, hl: String? = nil, cstart: Int? = nil, pagesize: Int? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get Scholar author profile

Get detailed Google Scholar author profile including articles, stats, co-authors.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let authorId = "authorId_example" // String | Scholar user ID (the `user` query parameter)
let hl = "hl_example" // String | Language code (optional) (default to "en")
let cstart = 987 // Int | Articles pagination offset (optional) (default to 0)
let pagesize = 987 // Int | Articles per page (optional) (default to 20)

// Get Scholar author profile
GoogleAPI.googleGetScholarAuthorProfile(authorId: authorId, hl: hl, cstart: cstart, pagesize: pagesize) { (response, error) in
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
 **authorId** | **String** | Scholar user ID (the &#x60;user&#x60; query parameter) | 
 **hl** | **String** | Language code | [optional] [default to &quot;en&quot;]
 **cstart** | **Int** | Articles pagination offset | [optional] [default to 0]
 **pagesize** | **Int** | Articles per page | [optional] [default to 20]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **googleGetStockIndexQuote**
```swift
    open class func googleGetStockIndexQuote(q: String, hl: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get stock/index quote

Get a stock or index quote from Google Finance.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let q = "q_example" // String | Ticker and exchange (e.g. \"AAPL:NASDAQ\", \"BTC-USD\")
let hl = "hl_example" // String | Language code (optional) (default to "en")

// Get stock/index quote
GoogleAPI.googleGetStockIndexQuote(q: q, hl: hl) { (response, error) in
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
 **q** | **String** | Ticker and exchange (e.g. \&quot;AAPL:NASDAQ\&quot;, \&quot;BTC-USD\&quot;) | 
 **hl** | **String** | Language code | [optional] [default to &quot;en&quot;]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **googleGoogleAiModeSearch**
```swift
    open class func googleGoogleAiModeSearch(q: String, gl: String? = nil, hl: String? = nil, includeHtml: Bool? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Google AI Mode search

Get AI-generated search results from Google AI Mode.  Returns the structured `text_blocks` (paragraphs, headings, comparison `table` blocks and lists), a flat `references` source list, a compact `markdown` rendering of the whole answer and — unless `include_html` is false — the raw `answer_html` body.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let q = "q_example" // String | Search query for AI-generated response
let gl = "gl_example" // String | Country code (optional) (default to "us")
let hl = "hl_example" // String | Language code (optional) (default to "en")
let includeHtml = true // Bool | Include the raw `answer_html` (full answer body HTML) in the response for maximum parity. It can be 100s of KB — set false when you only need the structured `text_blocks` + `markdown`. (optional) (default to true)

// Google AI Mode search
GoogleAPI.googleGoogleAiModeSearch(q: q, gl: gl, hl: hl, includeHtml: includeHtml) { (response, error) in
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
 **q** | **String** | Search query for AI-generated response | 
 **gl** | **String** | Country code | [optional] [default to &quot;us&quot;]
 **hl** | **String** | Language code | [optional] [default to &quot;en&quot;]
 **includeHtml** | **Bool** | Include the raw &#x60;answer_html&#x60; (full answer body HTML) in the response for maximum parity. It can be 100s of KB — set false when you only need the structured &#x60;text_blocks&#x60; + &#x60;markdown&#x60;. | [optional] [default to true]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **googleGoogleAiOverviewInlineSerpBlock**
```swift
    open class func googleGoogleAiOverviewInlineSerpBlock(q: String, gl: String? = nil, hl: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Google AI Overview (inline SERP block)

Get the AI Overview block Google renders inline at the top of a SERP.  Deferred overviews (where Google lazy-loads the block via a follow-up ``page_token``) are chased automatically.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let q = "q_example" // String | Search query — same shape as a Google Search query
let gl = "gl_example" // String | Country code (optional) (default to "us")
let hl = "hl_example" // String | Language code (optional) (default to "en")

// Google AI Overview (inline SERP block)
GoogleAPI.googleGoogleAiOverviewInlineSerpBlock(q: q, gl: gl, hl: hl) { (response, error) in
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
 **q** | **String** | Search query — same shape as a Google Search query | 
 **gl** | **String** | Country code | [optional] [default to &quot;us&quot;]
 **hl** | **String** | Language code | [optional] [default to &quot;en&quot;]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **googleGoogleFlightsCalendarCheapestFarePerDate**
```swift
    open class func googleGoogleFlightsCalendarCheapestFarePerDate(departureId: String, arrivalId: String, outboundDateFrom: String, outboundDateTo: String, tripType: String? = nil, tripLengthDays: Int? = nil, returnDateFrom: String? = nil, returnDateTo: String? = nil, adults: Int? = nil, children: Int? = nil, infantsInSeat: Int? = nil, infantsOnLap: Int? = nil, travelClass: String? = nil, currency: String? = nil, gl: String? = nil, hl: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Google Flights calendar — cheapest fare per date

Price a whole range of dates in one call — up to 200 dates per request.  Google Flights' own price graph / date grid: the cheapest fare per departure date instead of one search per date. Prices match `/flights/search` exactly.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let departureId = "departureId_example" // String | Departure airport IATA code or location ID
let arrivalId = "arrivalId_example" // String | Arrival airport IATA code or location ID
let outboundDateFrom = "outboundDateFrom_example" // String | First outbound date to price (YYYY-MM-DD)
let outboundDateTo = "outboundDateTo_example" // String | Last outbound date to price (YYYY-MM-DD). At most 200 days from outbound_date_from, or 14 in date-grid mode.
let tripType = "tripType_example" // String | one_way | round_trip (optional) (default to "one_way")
let tripLengthDays = 987 // Int | Round-trip stay length in nights (price-graph mode). Defaults to 7. (optional)
let returnDateFrom = "returnDateFrom_example" // String | Date-grid mode: first return date. With return_date_to, returns the full outbound x return matrix (each range at most 14 days). Round-trip only. (optional)
let returnDateTo = "returnDateTo_example" // String | Date-grid mode: last return date (optional)
let adults = 987 // Int |  (optional) (default to 1)
let children = 987 // Int |  (optional) (default to 0)
let infantsInSeat = 987 // Int |  (optional) (default to 0)
let infantsOnLap = 987 // Int |  (optional) (default to 0)
let travelClass = "travelClass_example" // String |  (optional) (default to "economy")
let currency = "currency_example" // String | ISO-4217 currency (optional) (default to "USD")
let gl = "gl_example" // String |  (optional) (default to "us")
let hl = "hl_example" // String |  (optional) (default to "en")

// Google Flights calendar — cheapest fare per date
GoogleAPI.googleGoogleFlightsCalendarCheapestFarePerDate(departureId: departureId, arrivalId: arrivalId, outboundDateFrom: outboundDateFrom, outboundDateTo: outboundDateTo, tripType: tripType, tripLengthDays: tripLengthDays, returnDateFrom: returnDateFrom, returnDateTo: returnDateTo, adults: adults, children: children, infantsInSeat: infantsInSeat, infantsOnLap: infantsOnLap, travelClass: travelClass, currency: currency, gl: gl, hl: hl) { (response, error) in
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
 **departureId** | **String** | Departure airport IATA code or location ID | 
 **arrivalId** | **String** | Arrival airport IATA code or location ID | 
 **outboundDateFrom** | **String** | First outbound date to price (YYYY-MM-DD) | 
 **outboundDateTo** | **String** | Last outbound date to price (YYYY-MM-DD). At most 200 days from outbound_date_from, or 14 in date-grid mode. | 
 **tripType** | **String** | one_way | round_trip | [optional] [default to &quot;one_way&quot;]
 **tripLengthDays** | **Int** | Round-trip stay length in nights (price-graph mode). Defaults to 7. | [optional] 
 **returnDateFrom** | **String** | Date-grid mode: first return date. With return_date_to, returns the full outbound x return matrix (each range at most 14 days). Round-trip only. | [optional] 
 **returnDateTo** | **String** | Date-grid mode: last return date | [optional] 
 **adults** | **Int** |  | [optional] [default to 1]
 **children** | **Int** |  | [optional] [default to 0]
 **infantsInSeat** | **Int** |  | [optional] [default to 0]
 **infantsOnLap** | **Int** |  | [optional] [default to 0]
 **travelClass** | **String** |  | [optional] [default to &quot;economy&quot;]
 **currency** | **String** | ISO-4217 currency | [optional] [default to &quot;USD&quot;]
 **gl** | **String** |  | [optional] [default to &quot;us&quot;]
 **hl** | **String** |  | [optional] [default to &quot;en&quot;]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **googleGoogleFlightsSearch**
```swift
    open class func googleGoogleFlightsSearch(departureId: String, arrivalId: String, outboundDate: String, returnDate: String? = nil, tripType: String? = nil, adults: Int? = nil, children: Int? = nil, infantsInSeat: Int? = nil, infantsOnLap: Int? = nil, travelClass: String? = nil, currency: String? = nil, gl: String? = nil, hl: String? = nil, stops: String? = nil, maxPrice: Int? = nil, departureToken: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Google Flights search

Search Google Flights for available itineraries.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let departureId = "departureId_example" // String | Departure airport IATA code or location ID
let arrivalId = "arrivalId_example" // String | Arrival airport IATA code or location ID
let outboundDate = "outboundDate_example" // String | Outbound date (YYYY-MM-DD)
let returnDate = "returnDate_example" // String | Return date (round-trip only) (optional)
let tripType = "tripType_example" // String | round_trip | one_way | multi_city (optional) (default to "round_trip")
let adults = 987 // Int |  (optional) (default to 1)
let children = 987 // Int |  (optional) (default to 0)
let infantsInSeat = 987 // Int |  (optional) (default to 0)
let infantsOnLap = 987 // Int |  (optional) (default to 0)
let travelClass = "travelClass_example" // String |  (optional) (default to "economy")
let currency = "currency_example" // String | ISO-4217 currency (optional) (default to "USD")
let gl = "gl_example" // String |  (optional) (default to "us")
let hl = "hl_example" // String |  (optional) (default to "en")
let stops = "stops_example" // String |  (optional) (default to "any")
let maxPrice = 987 // Int |  (optional)
let departureToken = "departureToken_example" // String | A round-trip offer's departure_token; returns the return-leg flights for that selected outbound (round-trip only). (optional)

// Google Flights search
GoogleAPI.googleGoogleFlightsSearch(departureId: departureId, arrivalId: arrivalId, outboundDate: outboundDate, returnDate: returnDate, tripType: tripType, adults: adults, children: children, infantsInSeat: infantsInSeat, infantsOnLap: infantsOnLap, travelClass: travelClass, currency: currency, gl: gl, hl: hl, stops: stops, maxPrice: maxPrice, departureToken: departureToken) { (response, error) in
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
 **departureId** | **String** | Departure airport IATA code or location ID | 
 **arrivalId** | **String** | Arrival airport IATA code or location ID | 
 **outboundDate** | **String** | Outbound date (YYYY-MM-DD) | 
 **returnDate** | **String** | Return date (round-trip only) | [optional] 
 **tripType** | **String** | round_trip | one_way | multi_city | [optional] [default to &quot;round_trip&quot;]
 **adults** | **Int** |  | [optional] [default to 1]
 **children** | **Int** |  | [optional] [default to 0]
 **infantsInSeat** | **Int** |  | [optional] [default to 0]
 **infantsOnLap** | **Int** |  | [optional] [default to 0]
 **travelClass** | **String** |  | [optional] [default to &quot;economy&quot;]
 **currency** | **String** | ISO-4217 currency | [optional] [default to &quot;USD&quot;]
 **gl** | **String** |  | [optional] [default to &quot;us&quot;]
 **hl** | **String** |  | [optional] [default to &quot;en&quot;]
 **stops** | **String** |  | [optional] [default to &quot;any&quot;]
 **maxPrice** | **Int** |  | [optional] 
 **departureToken** | **String** | A round-trip offer&#39;s departure_token; returns the return-leg flights for that selected outbound (round-trip only). | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **googleGoogleLensVisualSearch**
```swift
    open class func googleGoogleLensVisualSearch(url: String, query: String? = nil, country: String? = nil, language: String? = nil, gl: String? = nil, hl: String? = nil, product: Bool? = nil, visualMatches: Bool? = nil, exactMatches: Bool? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Google Lens visual search

Google Lens visual search.  Response carries ``lens_results`` (Scrapingdog parity alias) with ``title`` / ``source`` / ``source_favicon`` / ``thumbnail`` / ``original_thumbnail`` / ``rating`` / ``reviews`` / ``in_stock``, plus ``price`` (``{value, currency, extracted}``) and the raw ``tag`` chip it is parsed from, on shoppable matches. ``related_searches`` chips come alongside. Legacy ``results`` alias kept for backwards compat.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let url = "url_example" // String | Public URL of the image to search visually
let query = "query_example" // String | Optional text refinement (e.g. 'pizza') (optional)
let country = "country_example" // String | ISO country code (alias for gl) (optional)
let language = "language_example" // String | Language code (alias for hl) (optional)
let gl = "gl_example" // String | Country code (optional) (default to "us")
let hl = "hl_example" // String | Language code (optional) (default to "en")
let product = true // Bool | Bias towards shoppable product matches (optional) (default to false)
let visualMatches = true // Bool | Include the visual-matches carousel (optional) (default to true)
let exactMatches = true // Bool | Restrict to exact-match results (optional) (default to false)

// Google Lens visual search
GoogleAPI.googleGoogleLensVisualSearch(url: url, query: query, country: country, language: language, gl: gl, hl: hl, product: product, visualMatches: visualMatches, exactMatches: exactMatches) { (response, error) in
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
 **url** | **String** | Public URL of the image to search visually | 
 **query** | **String** | Optional text refinement (e.g. &#39;pizza&#39;) | [optional] 
 **country** | **String** | ISO country code (alias for gl) | [optional] 
 **language** | **String** | Language code (alias for hl) | [optional] 
 **gl** | **String** | Country code | [optional] [default to &quot;us&quot;]
 **hl** | **String** | Language code | [optional] [default to &quot;en&quot;]
 **product** | **Bool** | Bias towards shoppable product matches | [optional] [default to false]
 **visualMatches** | **Bool** | Include the visual-matches carousel | [optional] [default to true]
 **exactMatches** | **Bool** | Restrict to exact-match results | [optional] [default to false]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **googleGoogleScraperHealthCheck**
```swift
    open class func googleGoogleScraperHealthCheck(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Google scraper health check

Check health of the Google scraper service.  Accepts ``HEAD`` so external uptime checkers (UptimeRobot uses HEAD by default for HTTP monitors) don't get a 405 Method Not Allowed.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// Google scraper health check
GoogleAPI.googleGoogleScraperHealthCheck() { (response, error) in
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

# **googleGoogleScraperHealthCheckHead**
```swift
    open class func googleGoogleScraperHealthCheckHead(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Google scraper health check

Check health of the Google scraper service.  Accepts ``HEAD`` so external uptime checkers (UptimeRobot uses HEAD by default for HTTP monitors) don't get a 405 Method Not Allowed.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// Google scraper health check
GoogleAPI.googleGoogleScraperHealthCheckHead() { (response, error) in
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

# **googleGoogleSearchSuggestions**
```swift
    open class func googleGoogleSearchSuggestions(q: String, hl: String? = nil, gl: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Google search suggestions

Get Google search autocomplete suggestions.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let q = "q_example" // String | Search query to get suggestions for
let hl = "hl_example" // String | Language code (optional) (default to "en")
let gl = "gl_example" // String | Country code (optional) (default to "us")

// Google search suggestions
GoogleAPI.googleGoogleSearchSuggestions(q: q, hl: hl, gl: gl) { (response, error) in
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
 **q** | **String** | Search query to get suggestions for | 
 **hl** | **String** | Language code | [optional] [default to &quot;en&quot;]
 **gl** | **String** | Country code | [optional] [default to &quot;us&quot;]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **googleGoogleShortsSearch**
```swift
    open class func googleGoogleShortsSearch(q: String, gl: String? = nil, hl: String? = nil, domain: String? = nil, num: Int? = nil, start: Int? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Google Shorts search

Return short-form video results (YouTube Shorts, TikToks) from Google Shorts mode.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let q = "q_example" // String | Search query
let gl = "gl_example" // String | Country code (optional) (default to "us")
let hl = "hl_example" // String | Language code (optional) (default to "en")
let domain = "domain_example" // String | Google domain (optional) (default to "google.com")
let num = 987 // Int | Results per page (optional) (default to 20)
let start = 987 // Int | Pagination offset (optional) (default to 0)

// Google Shorts search
GoogleAPI.googleGoogleShortsSearch(q: q, gl: gl, hl: hl, domain: domain, num: num, start: start) { (response, error) in
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
 **q** | **String** | Search query | 
 **gl** | **String** | Country code | [optional] [default to &quot;us&quot;]
 **hl** | **String** | Language code | [optional] [default to &quot;en&quot;]
 **domain** | **String** | Google domain | [optional] [default to &quot;google.com&quot;]
 **num** | **Int** | Results per page | [optional] [default to 20]
 **start** | **Int** | Pagination offset | [optional] [default to 0]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **googleGoogleWebSearch**
```swift
    open class func googleGoogleWebSearch(q: String, gl: String? = nil, hl: String? = nil, num: Int? = nil, start: Int? = nil, domain: String? = nil, device: Device_googleGoogleWebSearch? = nil, userAgent: String? = nil, output: Output_googleGoogleWebSearch? = nil, location: String? = nil, lr: String? = nil, tbs: String? = nil, safe: String? = nil, uule: String? = nil, filter: Int? = nil, nfpr: Int? = nil, cr: String? = nil, ludocid: String? = nil, lsig: String? = nil, kgmid: String? = nil, si: String? = nil, ibp: String? = nil, uds: String? = nil, aiOverview: Bool? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Google web search

Search Google and get structured results (organic, ads, KG, AI overview, PAA).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let q = "q_example" // String | Search query (supports Google operators)
let gl = "gl_example" // String | Country code (optional) (default to "us")
let hl = "hl_example" // String | Language code (optional) (default to "en")
let num = 987 // Int |  (optional) (default to 10)
let start = 987 // Int | Page offset (0, 10, 20...) (optional) (default to 0)
let domain = "domain_example" // String | Google domain (optional) (default to "google.com")
let device = "device_example" // String | Device target: desktop, mobile, iphone, android, tablet (optional) (default to .desktop)
let userAgent = "userAgent_example" // String | Custom User-Agent (overrides device) (optional)
let output = "output_example" // String | Response format: json (parsed) or html (raw SERP) (optional) (default to .json)
let location = "location_example" // String | City-level geo-targeting (optional)
let lr = "lr_example" // String | Language restrict (e.g. lang_en) (optional)
let tbs = "tbs_example" // String | Time filter (e.g. qdr:d) (optional)
let safe = "safe_example" // String |  (optional) (default to "off")
let uule = "uule_example" // String | UULE encoded location (optional)
let filter = 987 // Int | Show omitted results (optional)
let nfpr = 987 // Int | Disable auto-correction (optional) (default to 0)
let cr = "cr_example" // String | Country restrict (optional)
let ludocid = "ludocid_example" // String | Google Place CID (optional)
let lsig = "lsig_example" // String | Knowledge Graph map ID (optional)
let kgmid = "kgmid_example" // String | Knowledge Graph entity ID (optional)
let si = "si_example" // String | Cached search params (optional)
let ibp = "ibp_example" // String | Layout control (optional)
let uds = "uds_example" // String | Google filter string (optional)
let aiOverview = true // Bool | Chase deferred AI Overview page_token with a follow-up fetch and merge the result. Adds ~1s and 1 credit when the SERP defers the overview. (optional) (default to false)

// Google web search
GoogleAPI.googleGoogleWebSearch(q: q, gl: gl, hl: hl, num: num, start: start, domain: domain, device: device, userAgent: userAgent, output: output, location: location, lr: lr, tbs: tbs, safe: safe, uule: uule, filter: filter, nfpr: nfpr, cr: cr, ludocid: ludocid, lsig: lsig, kgmid: kgmid, si: si, ibp: ibp, uds: uds, aiOverview: aiOverview) { (response, error) in
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
 **q** | **String** | Search query (supports Google operators) | 
 **gl** | **String** | Country code | [optional] [default to &quot;us&quot;]
 **hl** | **String** | Language code | [optional] [default to &quot;en&quot;]
 **num** | **Int** |  | [optional] [default to 10]
 **start** | **Int** | Page offset (0, 10, 20...) | [optional] [default to 0]
 **domain** | **String** | Google domain | [optional] [default to &quot;google.com&quot;]
 **device** | **String** | Device target: desktop, mobile, iphone, android, tablet | [optional] [default to .desktop]
 **userAgent** | **String** | Custom User-Agent (overrides device) | [optional] 
 **output** | **String** | Response format: json (parsed) or html (raw SERP) | [optional] [default to .json]
 **location** | **String** | City-level geo-targeting | [optional] 
 **lr** | **String** | Language restrict (e.g. lang_en) | [optional] 
 **tbs** | **String** | Time filter (e.g. qdr:d) | [optional] 
 **safe** | **String** |  | [optional] [default to &quot;off&quot;]
 **uule** | **String** | UULE encoded location | [optional] 
 **filter** | **Int** | Show omitted results | [optional] 
 **nfpr** | **Int** | Disable auto-correction | [optional] [default to 0]
 **cr** | **String** | Country restrict | [optional] 
 **ludocid** | **String** | Google Place CID | [optional] 
 **lsig** | **String** | Knowledge Graph map ID | [optional] 
 **kgmid** | **String** | Knowledge Graph entity ID | [optional] 
 **si** | **String** | Cached search params | [optional] 
 **ibp** | **String** | Layout control | [optional] 
 **uds** | **String** | Google filter string | [optional] 
 **aiOverview** | **Bool** | Chase deferred AI Overview page_token with a follow-up fetch and merge the result. Adds ~1s and 1 credit when the SERP defers the overview. | [optional] [default to false]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **googleHotelDetails**
```swift
    open class func googleHotelDetails(propertyToken: String, checkIn: String, checkOut: String, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Hotel details

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let propertyToken = "propertyToken_example" // String | Property token
let checkIn = "checkIn_example" // String | YYYY-MM-DD
let checkOut = "checkOut_example" // String | YYYY-MM-DD

// Hotel details
GoogleAPI.googleHotelDetails(propertyToken: propertyToken, checkIn: checkIn, checkOut: checkOut) { (response, error) in
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
 **propertyToken** | **String** | Property token | 
 **checkIn** | **String** | YYYY-MM-DD | 
 **checkOut** | **String** | YYYY-MM-DD | 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **googleImmersiveProductDetail**
```swift
    open class func googleImmersiveProductDetail(productId: String, q: String, gl: String? = nil, hl: String? = nil, catalogId: String? = nil, imageDocid: String? = nil, headlineOfferDocid: String? = nil, mid: String? = nil, includeOffers: Bool? = nil, includeVariants: Bool? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Immersive product detail

Get deep product details from Google's immersive product page.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let productId = "productId_example" // String | Google Shopping ``gpcid`` — the product_id returned on ``/shopping/search`` tiles. Scrapingdog-compatible.
let q = "q_example" // String | Original search query that surfaced the product. Required by Google's ``/async/oapv`` RPC.
let gl = "gl_example" // String | Country code (ISO 3166 alpha-2) (optional) (default to "us")
let hl = "hl_example" // String | Language code (optional) (default to "en")
let catalogId = "catalogId_example" // String | Optional ``catalogid`` from the Shopping tile (improves parity). (optional)
let imageDocid = "imageDocid_example" // String | Optional ``imageDocid`` for higher-fidelity images. (optional)
let headlineOfferDocid = "headlineOfferDocid_example" // String | Optional ``headlineOfferDocid`` to pin the featured seller. (optional)
let mid = "mid_example" // String | Optional Google Knowledge-Graph ``mid``. (optional)
let includeOffers = true // Bool | When true, fetch the full merchant-offer list via a secondary RPC (``/async/piu_ps``). Adds ~1 s. (optional) (default to false)
let includeVariants = true // Bool | When true, fetch size/colour variants via a secondary RPC (``/async/toy_v``). Adds ~1 s. (optional) (default to false)

// Immersive product detail
GoogleAPI.googleImmersiveProductDetail(productId: productId, q: q, gl: gl, hl: hl, catalogId: catalogId, imageDocid: imageDocid, headlineOfferDocid: headlineOfferDocid, mid: mid, includeOffers: includeOffers, includeVariants: includeVariants) { (response, error) in
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
 **productId** | **String** | Google Shopping &#x60;&#x60;gpcid&#x60;&#x60; — the product_id returned on &#x60;&#x60;/shopping/search&#x60;&#x60; tiles. Scrapingdog-compatible. | 
 **q** | **String** | Original search query that surfaced the product. Required by Google&#39;s &#x60;&#x60;/async/oapv&#x60;&#x60; RPC. | 
 **gl** | **String** | Country code (ISO 3166 alpha-2) | [optional] [default to &quot;us&quot;]
 **hl** | **String** | Language code | [optional] [default to &quot;en&quot;]
 **catalogId** | **String** | Optional &#x60;&#x60;catalogid&#x60;&#x60; from the Shopping tile (improves parity). | [optional] 
 **imageDocid** | **String** | Optional &#x60;&#x60;imageDocid&#x60;&#x60; for higher-fidelity images. | [optional] 
 **headlineOfferDocid** | **String** | Optional &#x60;&#x60;headlineOfferDocid&#x60;&#x60; to pin the featured seller. | [optional] 
 **mid** | **String** | Optional Google Knowledge-Graph &#x60;&#x60;mid&#x60;&#x60;. | [optional] 
 **includeOffers** | **Bool** | When true, fetch the full merchant-offer list via a secondary RPC (&#x60;&#x60;/async/piu_ps&#x60;&#x60;). Adds ~1 s. | [optional] [default to false]
 **includeVariants** | **Bool** | When true, fetch size/colour variants via a secondary RPC (&#x60;&#x60;/async/toy_v&#x60;&#x60;). Adds ~1 s. | [optional] [default to false]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **googleInterestByRegion**
```swift
    open class func googleInterestByRegion(q: String, geo: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Interest by region

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let q = "q_example" // String | Search term
let geo = "geo_example" // String |  (optional) (default to "")

// Interest by region
GoogleAPI.googleInterestByRegion(q: q, geo: geo) { (response, error) in
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
 **q** | **String** | Search term | 
 **geo** | **String** |  | [optional] [default to &quot;&quot;]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **googleInterestOverTime**
```swift
    open class func googleInterestOverTime(q: String, geo: String? = nil, date: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Interest over time

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let q = "q_example" // String | Search terms
let geo = "geo_example" // String |  (optional) (default to "")
let date = "date_example" // String |  (optional) (default to "today 12-m")

// Interest over time
GoogleAPI.googleInterestOverTime(q: q, geo: geo, date: date) { (response, error) in
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
 **q** | **String** | Search terms | 
 **geo** | **String** |  | [optional] [default to &quot;&quot;]
 **date** | **String** |  | [optional] [default to &quot;today 12-m&quot;]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **googleMultiSellerOffersByBarcode**
```swift
    open class func googleMultiSellerOffersByBarcode(barcode: String, gl: String? = nil, hl: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Multi-seller offers by barcode

Resolve a barcode to a product via Google web search, then return its Google Shopping seller offers (source + price per merchant).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let barcode = "barcode_example" // String | Product barcode — GTIN-8 / UPC-A / EAN-13 / GTIN-14
let gl = "gl_example" // String | Country code (ISO 3166 alpha-2) (optional)
let hl = "hl_example" // String | Language code (optional) (default to "en")

// Multi-seller offers by barcode
GoogleAPI.googleMultiSellerOffersByBarcode(barcode: barcode, gl: gl, hl: hl) { (response, error) in
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
 **barcode** | **String** | Product barcode — GTIN-8 / UPC-A / EAN-13 / GTIN-14 | 
 **gl** | **String** | Country code (ISO 3166 alpha-2) | [optional] 
 **hl** | **String** | Language code | [optional] [default to &quot;en&quot;]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **googleNewsByTopic**
```swift
    open class func googleNewsByTopic(topic: String, hl: String? = nil, gl: String? = nil, maxResults: Int? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

News by topic

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let topic = "topic_example" // String | Topic name
let hl = "hl_example" // String |  (optional) (default to "en")
let gl = "gl_example" // String |  (optional) (default to "US")
let maxResults = 987 // Int |  (optional) (default to 10)

// News by topic
GoogleAPI.googleNewsByTopic(topic: topic, hl: hl, gl: gl, maxResults: maxResults) { (response, error) in
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
 **topic** | **String** | Topic name | 
 **hl** | **String** |  | [optional] [default to &quot;en&quot;]
 **gl** | **String** |  | [optional] [default to &quot;US&quot;]
 **maxResults** | **Int** |  | [optional] [default to 10]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **googlePatentDetails**
```swift
    open class func googlePatentDetails(patentId: String, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Patent details

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let patentId = "patentId_example" // String | Patent number

// Patent details
GoogleAPI.googlePatentDetails(patentId: patentId) { (response, error) in
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
 **patentId** | **String** | Patent number | 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **googleRelatedTopicsQueries**
```swift
    open class func googleRelatedTopicsQueries(q: String, geo: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Related topics & queries

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let q = "q_example" // String | Search term
let geo = "geo_example" // String |  (optional) (default to "")

// Related topics & queries
GoogleAPI.googleRelatedTopicsQueries(q: q, geo: geo) { (response, error) in
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
 **q** | **String** | Search term | 
 **geo** | **String** |  | [optional] [default to &quot;&quot;]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **googleSearchGoogleImages**
```swift
    open class func googleSearchGoogleImages(q: String, gl: String? = nil, hl: String? = nil, tbs: String? = nil, imgsz: String? = nil, imgcolor: String? = nil, imgtype: String? = nil, safe: String? = nil, page: Int? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Search Google Images

Search Google Images for visual content.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let q = "q_example" // String | Image search query
let gl = "gl_example" // String | Country code (optional) (default to "us")
let hl = "hl_example" // String | Language code (optional) (default to "en")
let tbs = "tbs_example" // String | Time/filter string (e.g. qdr:d) (optional)
let imgsz = "imgsz_example" // String | Image size: l, m, i, xXl (optional)
let imgcolor = "imgcolor_example" // String | Image color filter (optional)
let imgtype = "imgtype_example" // String | Image type: face, photo, clipart (optional)
let safe = "safe_example" // String | Safe search (optional) (default to "off")
let page = 987 // Int | Page number (optional) (default to 0)

// Search Google Images
GoogleAPI.googleSearchGoogleImages(q: q, gl: gl, hl: hl, tbs: tbs, imgsz: imgsz, imgcolor: imgcolor, imgtype: imgtype, safe: safe, page: page) { (response, error) in
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
 **q** | **String** | Image search query | 
 **gl** | **String** | Country code | [optional] [default to &quot;us&quot;]
 **hl** | **String** | Language code | [optional] [default to &quot;en&quot;]
 **tbs** | **String** | Time/filter string (e.g. qdr:d) | [optional] 
 **imgsz** | **String** | Image size: l, m, i, xXl | [optional] 
 **imgcolor** | **String** | Image color filter | [optional] 
 **imgtype** | **String** | Image type: face, photo, clipart | [optional] 
 **safe** | **String** | Safe search | [optional] [default to &quot;off&quot;]
 **page** | **Int** | Page number | [optional] [default to 0]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **googleSearchGoogleJobs**
```swift
    open class func googleSearchGoogleJobs(q: String, location: String? = nil, gl: String? = nil, jobType: String? = nil, datePosted: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Search Google Jobs

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let q = "q_example" // String | Job title, keywords
let location = "location_example" // String |  (optional)
let gl = "gl_example" // String |  (optional) (default to "us")
let jobType = "jobType_example" // String |  (optional)
let datePosted = "datePosted_example" // String |  (optional)

// Search Google Jobs
GoogleAPI.googleSearchGoogleJobs(q: q, location: location, gl: gl, jobType: jobType, datePosted: datePosted) { (response, error) in
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
 **q** | **String** | Job title, keywords | 
 **location** | **String** |  | [optional] 
 **gl** | **String** |  | [optional] [default to &quot;us&quot;]
 **jobType** | **String** |  | [optional] 
 **datePosted** | **String** |  | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **googleSearchGoogleMapsPlaces**
```swift
    open class func googleSearchGoogleMapsPlaces(q: String, ll: String? = nil, gl: String? = nil, hl: String? = nil, start: Int? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Search Google Maps places

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let q = "q_example" // String | Search query
let ll = "ll_example" // String |  (optional)
let gl = "gl_example" // String |  (optional) (default to "us")
let hl = "hl_example" // String |  (optional) (default to "en")
let start = 987 // Int |  (optional) (default to 0)

// Search Google Maps places
GoogleAPI.googleSearchGoogleMapsPlaces(q: q, ll: ll, gl: gl, hl: hl, start: start) { (response, error) in
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
 **q** | **String** | Search query | 
 **ll** | **String** |  | [optional] 
 **gl** | **String** |  | [optional] [default to &quot;us&quot;]
 **hl** | **String** |  | [optional] [default to &quot;en&quot;]
 **start** | **Int** |  | [optional] [default to 0]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **googleSearchGoogleNews**
```swift
    open class func googleSearchGoogleNews(q: String, hl: String? = nil, gl: String? = nil, maxResults: Int? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Search Google News

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let q = "q_example" // String | Search query
let hl = "hl_example" // String |  (optional) (default to "en")
let gl = "gl_example" // String |  (optional) (default to "US")
let maxResults = 987 // Int |  (optional) (default to 10)

// Search Google News
GoogleAPI.googleSearchGoogleNews(q: q, hl: hl, gl: gl, maxResults: maxResults) { (response, error) in
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
 **q** | **String** | Search query | 
 **hl** | **String** |  | [optional] [default to &quot;en&quot;]
 **gl** | **String** |  | [optional] [default to &quot;US&quot;]
 **maxResults** | **Int** |  | [optional] [default to 10]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **googleSearchGoogleScholar**
```swift
    open class func googleSearchGoogleScholar(q: String, hl: String? = nil, asYlo: Int? = nil, asYhi: Int? = nil, asSdt: String? = nil, page: Int? = nil, num: Int? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Search Google Scholar

Search Google Scholar for scholarly articles.  Each result ships with its doc ``id``, ``type`` badge ([BOOK]/[PDF]/...), wrapped ``inline_links`` (versions + cited_by + related), PDF ``resources`` list, and structured ``authors`` (with ``author_id`` for profiled authors — pipe straight into ``/scholar/author``). Envelope carries ``scholar_results`` alias (Scrapingdog parity), ``related_searches``, and matched ``profiles`` cards.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let q = "q_example" // String | Search query for scholarly articles
let hl = "hl_example" // String | Language code (optional) (default to "en")
let asYlo = 987 // Int | Year from (e.g. 2020) (optional)
let asYhi = 987 // Int | Year to (e.g. 2024) (optional)
let asSdt = "asSdt_example" // String | Search type: 0=exclude patents, 7=include (optional) (default to "0")
let page = 987 // Int | Page number (0-based) (optional) (default to 0)
let num = 987 // Int | Results per page (max 20) (optional) (default to 10)

// Search Google Scholar
GoogleAPI.googleSearchGoogleScholar(q: q, hl: hl, asYlo: asYlo, asYhi: asYhi, asSdt: asSdt, page: page, num: num) { (response, error) in
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
 **q** | **String** | Search query for scholarly articles | 
 **hl** | **String** | Language code | [optional] [default to &quot;en&quot;]
 **asYlo** | **Int** | Year from (e.g. 2020) | [optional] 
 **asYhi** | **Int** | Year to (e.g. 2024) | [optional] 
 **asSdt** | **String** | Search type: 0&#x3D;exclude patents, 7&#x3D;include | [optional] [default to &quot;0&quot;]
 **page** | **Int** | Page number (0-based) | [optional] [default to 0]
 **num** | **Int** | Results per page (max 20) | [optional] [default to 10]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **googleSearchGoogleVideos**
```swift
    open class func googleSearchGoogleVideos(q: String, gl: String? = nil, hl: String? = nil, tbs: String? = nil, safe: String? = nil, page: Int? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Search Google Videos

Search Google for video results.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let q = "q_example" // String | Video search query
let gl = "gl_example" // String | Country code (optional) (default to "us")
let hl = "hl_example" // String | Language code (optional) (default to "en")
let tbs = "tbs_example" // String | Time filter (e.g. qdr:d) (optional)
let safe = "safe_example" // String | Safe search (optional) (default to "off")
let page = 987 // Int | Page number (optional) (default to 0)

// Search Google Videos
GoogleAPI.googleSearchGoogleVideos(q: q, gl: gl, hl: hl, tbs: tbs, safe: safe, page: page) { (response, error) in
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
 **q** | **String** | Video search query | 
 **gl** | **String** | Country code | [optional] [default to &quot;us&quot;]
 **hl** | **String** | Language code | [optional] [default to &quot;en&quot;]
 **tbs** | **String** | Time filter (e.g. qdr:d) | [optional] 
 **safe** | **String** | Safe search | [optional] [default to &quot;off&quot;]
 **page** | **Int** | Page number | [optional] [default to 0]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **googleSearchHotels**
```swift
    open class func googleSearchHotels(q: String, checkIn: String, checkOut: String, adults: Int? = nil, currency: String? = nil, gl: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Search hotels

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let q = "q_example" // String | Location or hotel name
let checkIn = "checkIn_example" // String | YYYY-MM-DD
let checkOut = "checkOut_example" // String | YYYY-MM-DD
let adults = 987 // Int |  (optional) (default to 2)
let currency = "currency_example" // String |  (optional) (default to "USD")
let gl = "gl_example" // String |  (optional) (default to "us")

// Search hotels
GoogleAPI.googleSearchHotels(q: q, checkIn: checkIn, checkOut: checkOut, adults: adults, currency: currency, gl: gl) { (response, error) in
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
 **q** | **String** | Location or hotel name | 
 **checkIn** | **String** | YYYY-MM-DD | 
 **checkOut** | **String** | YYYY-MM-DD | 
 **adults** | **Int** |  | [optional] [default to 2]
 **currency** | **String** |  | [optional] [default to &quot;USD&quot;]
 **gl** | **String** |  | [optional] [default to &quot;us&quot;]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **googleSearchPatents**
```swift
    open class func googleSearchPatents(q: String, page: Int? = nil, num: Int? = nil, sort: String? = nil, inventor: String? = nil, assignee: String? = nil, country: String? = nil, language: String? = nil, status: String? = nil, patentType: String? = nil, before: String? = nil, after: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Search patents

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let q = "q_example" // String | Search query (Boolean logic supported)
let page = 987 // Int |  (optional) (default to 0)
let num = 987 // Int |  (optional) (default to 10)
let sort = "sort_example" // String | 'new' or 'old' (optional)
let inventor = "inventor_example" // String | Inventor name(s) (optional)
let assignee = "assignee_example" // String | Assignee / company name(s) (optional)
let country = "country_example" // String | Country code (US, EP, WO, …) (optional)
let language = "language_example" // String | Patent language: ENGLISH, GERMAN, CHINESE, FRENCH, JAPANESE, KOREAN, SPANISH (optional)
let status = "status_example" // String | GRANT or APPLICATION (optional)
let patentType = "patentType_example" // String | PATENT or DESIGN (optional)
let before = "before_example" // String | Before date YYYYMMDD (optional)
let after = "after_example" // String | After date YYYYMMDD (optional)

// Search patents
GoogleAPI.googleSearchPatents(q: q, page: page, num: num, sort: sort, inventor: inventor, assignee: assignee, country: country, language: language, status: status, patentType: patentType, before: before, after: after) { (response, error) in
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
 **q** | **String** | Search query (Boolean logic supported) | 
 **page** | **Int** |  | [optional] [default to 0]
 **num** | **Int** |  | [optional] [default to 10]
 **sort** | **String** | &#39;new&#39; or &#39;old&#39; | [optional] 
 **inventor** | **String** | Inventor name(s) | [optional] 
 **assignee** | **String** | Assignee / company name(s) | [optional] 
 **country** | **String** | Country code (US, EP, WO, …) | [optional] 
 **language** | **String** | Patent language: ENGLISH, GERMAN, CHINESE, FRENCH, JAPANESE, KOREAN, SPANISH | [optional] 
 **status** | **String** | GRANT or APPLICATION | [optional] 
 **patentType** | **String** | PATENT or DESIGN | [optional] 
 **before** | **String** | Before date YYYYMMDD | [optional] 
 **after** | **String** | After date YYYYMMDD | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **googleSearchProducts**
```swift
    open class func googleSearchProducts(q: String, gl: String? = nil, minPrice: Int? = nil, maxPrice: Int? = nil, sortBy: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Search products

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let q = "q_example" // String | Product search query
let gl = "gl_example" // String |  (optional) (default to "us")
let minPrice = 987 // Int |  (optional)
let maxPrice = 987 // Int |  (optional)
let sortBy = "sortBy_example" // String |  (optional)

// Search products
GoogleAPI.googleSearchProducts(q: q, gl: gl, minPrice: minPrice, maxPrice: maxPrice, sortBy: sortBy) { (response, error) in
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
 **q** | **String** | Product search query | 
 **gl** | **String** |  | [optional] [default to &quot;us&quot;]
 **minPrice** | **Int** |  | [optional] 
 **maxPrice** | **Int** |  | [optional] 
 **sortBy** | **String** |  | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **googleSearchScholarAuthorProfiles**
```swift
    open class func googleSearchScholarAuthorProfiles(mauthors: String, hl: String? = nil, afterAuthor: String? = nil, beforeAuthor: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Search Scholar author profiles

Search Google Scholar for author profiles by name.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let mauthors = "mauthors_example" // String | Author name query (e.g. 'Geoffrey Hinton')
let hl = "hl_example" // String | Language code (optional) (default to "en")
let afterAuthor = "afterAuthor_example" // String | Pagination token (next page) (optional)
let beforeAuthor = "beforeAuthor_example" // String | Pagination token (previous page) (optional)

// Search Scholar author profiles
GoogleAPI.googleSearchScholarAuthorProfiles(mauthors: mauthors, hl: hl, afterAuthor: afterAuthor, beforeAuthor: beforeAuthor) { (response, error) in
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
 **mauthors** | **String** | Author name query (e.g. &#39;Geoffrey Hinton&#39;) | 
 **hl** | **String** | Language code | [optional] [default to &quot;en&quot;]
 **afterAuthor** | **String** | Pagination token (next page) | [optional] 
 **beforeAuthor** | **String** | Pagination token (previous page) | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **googleTrendingNews**
```swift
    open class func googleTrendingNews(hl: String? = nil, gl: String? = nil, maxResults: Int? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Trending news

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let hl = "hl_example" // String |  (optional) (default to "en")
let gl = "gl_example" // String |  (optional) (default to "US")
let maxResults = 987 // Int |  (optional) (default to 10)

// Trending news
GoogleAPI.googleTrendingNews(hl: hl, gl: gl, maxResults: maxResults) { (response, error) in
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
 **hl** | **String** |  | [optional] [default to &quot;en&quot;]
 **gl** | **String** |  | [optional] [default to &quot;US&quot;]
 **maxResults** | **Int** |  | [optional] [default to 10]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **googleTrendingSearches**
```swift
    open class func googleTrendingSearches(geo: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Trending searches

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let geo = "geo_example" // String |  (optional) (default to "US")

// Trending searches
GoogleAPI.googleTrendingSearches(geo: geo) { (response, error) in
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
 **geo** | **String** |  | [optional] [default to &quot;US&quot;]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **googleTrendsTopicAutocomplete**
```swift
    open class func googleTrendsTopicAutocomplete(q: String, hl: String? = nil, tz: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Trends topic autocomplete

Return categorized Knowledge Graph topic entities (mid, type) for a query.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let q = "q_example" // String | Query prefix to resolve into Trends topics
let hl = "hl_example" // String | Language code (optional) (default to "en-US")
let tz = "tz_example" // String | Timezone offset in minutes (optional) (default to "0")

// Trends topic autocomplete
GoogleAPI.googleTrendsTopicAutocomplete(q: q, hl: hl, tz: tz) { (response, error) in
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
 **q** | **String** | Query prefix to resolve into Trends topics | 
 **hl** | **String** | Language code | [optional] [default to &quot;en-US&quot;]
 **tz** | **String** | Timezone offset in minutes | [optional] [default to &quot;0&quot;]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

