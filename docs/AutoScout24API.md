# AutoScout24API

All URIs are relative to *https://scrapebadger.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**autoscout24CheckAutoscout24Health**](AutoScout24API.md#autoscout24checkautoscout24health) | **GET** /v1/autoscout24/health | Check AutoScout24 health
[**autoscout24GetListing**](AutoScout24API.md#autoscout24getlisting) | **GET** /v1/autoscout24/listing | Get listing
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

# **autoscout24GetListing**
```swift
    open class func autoscout24GetListing(url: String? = nil, listingId: String? = nil, market: Market_autoscout24GetListing? = nil, prefer: String? = nil, xCallbackURL: String? = nil, idempotencyKey: String? = nil, async: Bool? = nil, asyncWait: Int? = nil, callbackUrl: String? = nil, idempotencyKey2: String? = nil, completion: @escaping (_ data: AutoScout24ListingResponse?, _ error: Error?) -> Void)
```

Get listing

Full public vehicle specifications, equipment, photos, price and seller data.  Exactly one of url or listing_id is required. Supported markets match /markets. Successful detail costs 10 credits; removed or missing listings return an unbilled 404. Invalid inputs return 422 and source failures 503.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let url = "url_example" // String | Full HTTPS listing URL from search results. Supply url or listing_id, not both. (optional)
let listingId = "listingId_example" // String | Listing UUID from search results; requires no SEO slug. (optional)
let market = "market_example" // String | Inferred from URL, otherwise de. Explicit market must match the URL host. (optional)
let prefer = "prefer_example" // String | `respond-async[, wait=N]` (RFC 7240): run the call async. If it has not finished after `wait` seconds (0-120, default 25) the answer is `202` with a `request_id`; poll `GET /v1/requests/{request_id}`. Its `wait=` wins over `async_wait`; without one, `async_wait` sets the wait. (optional)
let xCallbackURL = "xCallbackURL_example" // String | An `https` URL that receives the signed `request.completed` webhook when the call finishes. Implies async: on its own (no `Prefer`, `async` or `async_wait`) the answer is an immediate `202`; with `Prefer: respond-async` or `async=true` the call still waits 25 s unless a wait is given. Wins over `callback_url`. (optional)
let idempotencyKey = "idempotencyKey_example" // String | 1-200 visible ASCII characters, per account, kept as long as the result (about 15 minutes). The same key on the same call returns that call's current state (`Idempotent-Replayed: true`) without running or billing it again; on a different call it is `409 idempotency_key_reused`. Applies to async calls only; on a synchronous call it is ignored. Wins over `idempotency_key`. (optional)
let async = true // Bool | Query form of `Prefer: respond-async`: `true` or `1` (also `yes`, `on`; `false`, `0`, `no`, `off` leave the call synchronous). Waits 25 s unless `async_wait` is given. Not sent to the scraper. (optional)
let asyncWait = 987 // Int | Seconds (0-120; values outside are clamped) to wait for the result before answering `202`. Implies async. Not sent to the scraper. (optional)
let callbackUrl = "callbackUrl_example" // String | Query form of `X-Callback-URL` (URL-encode it). Implies async; on its own the answer is an immediate `202` (wait 0). Not sent to the scraper. (optional)
let idempotencyKey2 = "idempotencyKey2_example" // String | Query form of `Idempotency-Key`. Not sent to the scraper. (optional)

// Get listing
AutoScout24API.autoscout24GetListing(url: url, listingId: listingId, market: market, prefer: prefer, xCallbackURL: xCallbackURL, idempotencyKey: idempotencyKey, async: async, asyncWait: asyncWait, callbackUrl: callbackUrl, idempotencyKey2: idempotencyKey2) { (response, error) in
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
 **url** | **String** | Full HTTPS listing URL from search results. Supply url or listing_id, not both. | [optional] 
 **listingId** | **String** | Listing UUID from search results; requires no SEO slug. | [optional] 
 **market** | **String** | Inferred from URL, otherwise de. Explicit market must match the URL host. | [optional] 
 **prefer** | **String** | &#x60;respond-async[, wait&#x3D;N]&#x60; (RFC 7240): run the call async. If it has not finished after &#x60;wait&#x60; seconds (0-120, default 25) the answer is &#x60;202&#x60; with a &#x60;request_id&#x60;; poll &#x60;GET /v1/requests/{request_id}&#x60;. Its &#x60;wait&#x3D;&#x60; wins over &#x60;async_wait&#x60;; without one, &#x60;async_wait&#x60; sets the wait. | [optional] 
 **xCallbackURL** | **String** | An &#x60;https&#x60; URL that receives the signed &#x60;request.completed&#x60; webhook when the call finishes. Implies async: on its own (no &#x60;Prefer&#x60;, &#x60;async&#x60; or &#x60;async_wait&#x60;) the answer is an immediate &#x60;202&#x60;; with &#x60;Prefer: respond-async&#x60; or &#x60;async&#x3D;true&#x60; the call still waits 25 s unless a wait is given. Wins over &#x60;callback_url&#x60;. | [optional] 
 **idempotencyKey** | **String** | 1-200 visible ASCII characters, per account, kept as long as the result (about 15 minutes). The same key on the same call returns that call&#39;s current state (&#x60;Idempotent-Replayed: true&#x60;) without running or billing it again; on a different call it is &#x60;409 idempotency_key_reused&#x60;. Applies to async calls only; on a synchronous call it is ignored. Wins over &#x60;idempotency_key&#x60;. | [optional] 
 **async** | **Bool** | Query form of &#x60;Prefer: respond-async&#x60;: &#x60;true&#x60; or &#x60;1&#x60; (also &#x60;yes&#x60;, &#x60;on&#x60;; &#x60;false&#x60;, &#x60;0&#x60;, &#x60;no&#x60;, &#x60;off&#x60; leave the call synchronous). Waits 25 s unless &#x60;async_wait&#x60; is given. Not sent to the scraper. | [optional] 
 **asyncWait** | **Int** | Seconds (0-120; values outside are clamped) to wait for the result before answering &#x60;202&#x60;. Implies async. Not sent to the scraper. | [optional] 
 **callbackUrl** | **String** | Query form of &#x60;X-Callback-URL&#x60; (URL-encode it). Implies async; on its own the answer is an immediate &#x60;202&#x60; (wait 0). Not sent to the scraper. | [optional] 
 **idempotencyKey2** | **String** | Query form of &#x60;Idempotency-Key&#x60;. Not sent to the scraper. | [optional] 

### Return type

[**AutoScout24ListingResponse**](AutoScout24ListingResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **autoscout24ListMarkets**
```swift
    open class func autoscout24ListMarkets(prefer: String? = nil, xCallbackURL: String? = nil, idempotencyKey: String? = nil, async: Bool? = nil, asyncWait: Int? = nil, callbackUrl: String? = nil, idempotencyKey2: String? = nil, completion: @escaping (_ data: AutoScout24MarketsResponse?, _ error: Error?) -> Void)
```

List markets

Verified marketplaces, domains, languages and currency. Free reference endpoint.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let prefer = "prefer_example" // String | `respond-async[, wait=N]` (RFC 7240): run the call async. If it has not finished after `wait` seconds (0-120, default 25) the answer is `202` with a `request_id`; poll `GET /v1/requests/{request_id}`. Its `wait=` wins over `async_wait`; without one, `async_wait` sets the wait. (optional)
let xCallbackURL = "xCallbackURL_example" // String | An `https` URL that receives the signed `request.completed` webhook when the call finishes. Implies async: on its own (no `Prefer`, `async` or `async_wait`) the answer is an immediate `202`; with `Prefer: respond-async` or `async=true` the call still waits 25 s unless a wait is given. Wins over `callback_url`. (optional)
let idempotencyKey = "idempotencyKey_example" // String | 1-200 visible ASCII characters, per account, kept as long as the result (about 15 minutes). The same key on the same call returns that call's current state (`Idempotent-Replayed: true`) without running or billing it again; on a different call it is `409 idempotency_key_reused`. Applies to async calls only; on a synchronous call it is ignored. Wins over `idempotency_key`. (optional)
let async = true // Bool | Query form of `Prefer: respond-async`: `true` or `1` (also `yes`, `on`; `false`, `0`, `no`, `off` leave the call synchronous). Waits 25 s unless `async_wait` is given. Not sent to the scraper. (optional)
let asyncWait = 987 // Int | Seconds (0-120; values outside are clamped) to wait for the result before answering `202`. Implies async. Not sent to the scraper. (optional)
let callbackUrl = "callbackUrl_example" // String | Query form of `X-Callback-URL` (URL-encode it). Implies async; on its own the answer is an immediate `202` (wait 0). Not sent to the scraper. (optional)
let idempotencyKey2 = "idempotencyKey2_example" // String | Query form of `Idempotency-Key`. Not sent to the scraper. (optional)

// List markets
AutoScout24API.autoscout24ListMarkets(prefer: prefer, xCallbackURL: xCallbackURL, idempotencyKey: idempotencyKey, async: async, asyncWait: asyncWait, callbackUrl: callbackUrl, idempotencyKey2: idempotencyKey2) { (response, error) in
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
 **prefer** | **String** | &#x60;respond-async[, wait&#x3D;N]&#x60; (RFC 7240): run the call async. If it has not finished after &#x60;wait&#x60; seconds (0-120, default 25) the answer is &#x60;202&#x60; with a &#x60;request_id&#x60;; poll &#x60;GET /v1/requests/{request_id}&#x60;. Its &#x60;wait&#x3D;&#x60; wins over &#x60;async_wait&#x60;; without one, &#x60;async_wait&#x60; sets the wait. | [optional] 
 **xCallbackURL** | **String** | An &#x60;https&#x60; URL that receives the signed &#x60;request.completed&#x60; webhook when the call finishes. Implies async: on its own (no &#x60;Prefer&#x60;, &#x60;async&#x60; or &#x60;async_wait&#x60;) the answer is an immediate &#x60;202&#x60;; with &#x60;Prefer: respond-async&#x60; or &#x60;async&#x3D;true&#x60; the call still waits 25 s unless a wait is given. Wins over &#x60;callback_url&#x60;. | [optional] 
 **idempotencyKey** | **String** | 1-200 visible ASCII characters, per account, kept as long as the result (about 15 minutes). The same key on the same call returns that call&#39;s current state (&#x60;Idempotent-Replayed: true&#x60;) without running or billing it again; on a different call it is &#x60;409 idempotency_key_reused&#x60;. Applies to async calls only; on a synchronous call it is ignored. Wins over &#x60;idempotency_key&#x60;. | [optional] 
 **async** | **Bool** | Query form of &#x60;Prefer: respond-async&#x60;: &#x60;true&#x60; or &#x60;1&#x60; (also &#x60;yes&#x60;, &#x60;on&#x60;; &#x60;false&#x60;, &#x60;0&#x60;, &#x60;no&#x60;, &#x60;off&#x60; leave the call synchronous). Waits 25 s unless &#x60;async_wait&#x60; is given. Not sent to the scraper. | [optional] 
 **asyncWait** | **Int** | Seconds (0-120; values outside are clamped) to wait for the result before answering &#x60;202&#x60;. Implies async. Not sent to the scraper. | [optional] 
 **callbackUrl** | **String** | Query form of &#x60;X-Callback-URL&#x60; (URL-encode it). Implies async; on its own the answer is an immediate &#x60;202&#x60; (wait 0). Not sent to the scraper. | [optional] 
 **idempotencyKey2** | **String** | Query form of &#x60;Idempotency-Key&#x60;. Not sent to the scraper. | [optional] 

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
    open class func autoscout24ListSearchFilters(market: Market_autoscout24ListSearchFilters? = nil, make: String? = nil, prefer: String? = nil, xCallbackURL: String? = nil, idempotencyKey: String? = nil, async: Bool? = nil, asyncWait: Int? = nil, callbackUrl: String? = nil, idempotencyKey2: String? = nil, completion: @escaping (_ data: AutoScout24FiltersResponse?, _ error: Error?) -> Void)
```

List search filters

Current native make, model and vehicle filter options. Set make for its models.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let market = "market_example" // String |  (optional) (default to .de)
let make = "make_example" // String |  (optional)
let prefer = "prefer_example" // String | `respond-async[, wait=N]` (RFC 7240): run the call async. If it has not finished after `wait` seconds (0-120, default 25) the answer is `202` with a `request_id`; poll `GET /v1/requests/{request_id}`. Its `wait=` wins over `async_wait`; without one, `async_wait` sets the wait. (optional)
let xCallbackURL = "xCallbackURL_example" // String | An `https` URL that receives the signed `request.completed` webhook when the call finishes. Implies async: on its own (no `Prefer`, `async` or `async_wait`) the answer is an immediate `202`; with `Prefer: respond-async` or `async=true` the call still waits 25 s unless a wait is given. Wins over `callback_url`. (optional)
let idempotencyKey = "idempotencyKey_example" // String | 1-200 visible ASCII characters, per account, kept as long as the result (about 15 minutes). The same key on the same call returns that call's current state (`Idempotent-Replayed: true`) without running or billing it again; on a different call it is `409 idempotency_key_reused`. Applies to async calls only; on a synchronous call it is ignored. Wins over `idempotency_key`. (optional)
let async = true // Bool | Query form of `Prefer: respond-async`: `true` or `1` (also `yes`, `on`; `false`, `0`, `no`, `off` leave the call synchronous). Waits 25 s unless `async_wait` is given. Not sent to the scraper. (optional)
let asyncWait = 987 // Int | Seconds (0-120; values outside are clamped) to wait for the result before answering `202`. Implies async. Not sent to the scraper. (optional)
let callbackUrl = "callbackUrl_example" // String | Query form of `X-Callback-URL` (URL-encode it). Implies async; on its own the answer is an immediate `202` (wait 0). Not sent to the scraper. (optional)
let idempotencyKey2 = "idempotencyKey2_example" // String | Query form of `Idempotency-Key`. Not sent to the scraper. (optional)

// List search filters
AutoScout24API.autoscout24ListSearchFilters(market: market, make: make, prefer: prefer, xCallbackURL: xCallbackURL, idempotencyKey: idempotencyKey, async: async, asyncWait: asyncWait, callbackUrl: callbackUrl, idempotencyKey2: idempotencyKey2) { (response, error) in
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
 **prefer** | **String** | &#x60;respond-async[, wait&#x3D;N]&#x60; (RFC 7240): run the call async. If it has not finished after &#x60;wait&#x60; seconds (0-120, default 25) the answer is &#x60;202&#x60; with a &#x60;request_id&#x60;; poll &#x60;GET /v1/requests/{request_id}&#x60;. Its &#x60;wait&#x3D;&#x60; wins over &#x60;async_wait&#x60;; without one, &#x60;async_wait&#x60; sets the wait. | [optional] 
 **xCallbackURL** | **String** | An &#x60;https&#x60; URL that receives the signed &#x60;request.completed&#x60; webhook when the call finishes. Implies async: on its own (no &#x60;Prefer&#x60;, &#x60;async&#x60; or &#x60;async_wait&#x60;) the answer is an immediate &#x60;202&#x60;; with &#x60;Prefer: respond-async&#x60; or &#x60;async&#x3D;true&#x60; the call still waits 25 s unless a wait is given. Wins over &#x60;callback_url&#x60;. | [optional] 
 **idempotencyKey** | **String** | 1-200 visible ASCII characters, per account, kept as long as the result (about 15 minutes). The same key on the same call returns that call&#39;s current state (&#x60;Idempotent-Replayed: true&#x60;) without running or billing it again; on a different call it is &#x60;409 idempotency_key_reused&#x60;. Applies to async calls only; on a synchronous call it is ignored. Wins over &#x60;idempotency_key&#x60;. | [optional] 
 **async** | **Bool** | Query form of &#x60;Prefer: respond-async&#x60;: &#x60;true&#x60; or &#x60;1&#x60; (also &#x60;yes&#x60;, &#x60;on&#x60;; &#x60;false&#x60;, &#x60;0&#x60;, &#x60;no&#x60;, &#x60;off&#x60; leave the call synchronous). Waits 25 s unless &#x60;async_wait&#x60; is given. Not sent to the scraper. | [optional] 
 **asyncWait** | **Int** | Seconds (0-120; values outside are clamped) to wait for the result before answering &#x60;202&#x60;. Implies async. Not sent to the scraper. | [optional] 
 **callbackUrl** | **String** | Query form of &#x60;X-Callback-URL&#x60; (URL-encode it). Implies async; on its own the answer is an immediate &#x60;202&#x60; (wait 0). Not sent to the scraper. | [optional] 
 **idempotencyKey2** | **String** | Query form of &#x60;Idempotency-Key&#x60;. Not sent to the scraper. | [optional] 

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
    open class func autoscout24SearchVehicles(market: Market_autoscout24SearchVehicles? = nil, make: String? = nil, model: String? = nil, priceMin: Int? = nil, priceMax: Int? = nil, mileageMin: Int? = nil, mileageMax: Int? = nil, yearMin: Int? = nil, yearMax: Int? = nil, powerMin: Int? = nil, powerMax: Int? = nil, fuelType: FuelType_autoscout24SearchVehicles? = nil, transmission: Transmission_autoscout24SearchVehicles? = nil, bodyType: BodyType_autoscout24SearchVehicles? = nil, sellerType: SellerType_autoscout24SearchVehicles? = nil, condition: Condition_autoscout24SearchVehicles? = nil, zip: String? = nil, radius: Int? = nil, sortBy: SortBy_autoscout24SearchVehicles? = nil, page: Int? = nil, prefer: String? = nil, xCallbackURL: String? = nil, idempotencyKey: String? = nil, async: Bool? = nil, asyncWait: Int? = nil, callbackUrl: String? = nil, idempotencyKey2: String? = nil, completion: @escaping (_ data: AutoScout24SearchResponse?, _ error: Error?) -> Void)
```

Search vehicles

Search live vehicle cards, seller/location information and current filter taxonomy.  Browsing is capped at 200 pages (normally 20 cards each). Narrow the query to reach more inventory. Empty results cost zero credits. Pass a result's url or id to /listing for its full specifications and equipment.

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
let prefer = "prefer_example" // String | `respond-async[, wait=N]` (RFC 7240): run the call async. If it has not finished after `wait` seconds (0-120, default 25) the answer is `202` with a `request_id`; poll `GET /v1/requests/{request_id}`. Its `wait=` wins over `async_wait`; without one, `async_wait` sets the wait. (optional)
let xCallbackURL = "xCallbackURL_example" // String | An `https` URL that receives the signed `request.completed` webhook when the call finishes. Implies async: on its own (no `Prefer`, `async` or `async_wait`) the answer is an immediate `202`; with `Prefer: respond-async` or `async=true` the call still waits 25 s unless a wait is given. Wins over `callback_url`. (optional)
let idempotencyKey = "idempotencyKey_example" // String | 1-200 visible ASCII characters, per account, kept as long as the result (about 15 minutes). The same key on the same call returns that call's current state (`Idempotent-Replayed: true`) without running or billing it again; on a different call it is `409 idempotency_key_reused`. Applies to async calls only; on a synchronous call it is ignored. Wins over `idempotency_key`. (optional)
let async = true // Bool | Query form of `Prefer: respond-async`: `true` or `1` (also `yes`, `on`; `false`, `0`, `no`, `off` leave the call synchronous). Waits 25 s unless `async_wait` is given. Not sent to the scraper. (optional)
let asyncWait = 987 // Int | Seconds (0-120; values outside are clamped) to wait for the result before answering `202`. Implies async. Not sent to the scraper. (optional)
let callbackUrl = "callbackUrl_example" // String | Query form of `X-Callback-URL` (URL-encode it). Implies async; on its own the answer is an immediate `202` (wait 0). Not sent to the scraper. (optional)
let idempotencyKey2 = "idempotencyKey2_example" // String | Query form of `Idempotency-Key`. Not sent to the scraper. (optional)

// Search vehicles
AutoScout24API.autoscout24SearchVehicles(market: market, make: make, model: model, priceMin: priceMin, priceMax: priceMax, mileageMin: mileageMin, mileageMax: mileageMax, yearMin: yearMin, yearMax: yearMax, powerMin: powerMin, powerMax: powerMax, fuelType: fuelType, transmission: transmission, bodyType: bodyType, sellerType: sellerType, condition: condition, zip: zip, radius: radius, sortBy: sortBy, page: page, prefer: prefer, xCallbackURL: xCallbackURL, idempotencyKey: idempotencyKey, async: async, asyncWait: asyncWait, callbackUrl: callbackUrl, idempotencyKey2: idempotencyKey2) { (response, error) in
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
 **prefer** | **String** | &#x60;respond-async[, wait&#x3D;N]&#x60; (RFC 7240): run the call async. If it has not finished after &#x60;wait&#x60; seconds (0-120, default 25) the answer is &#x60;202&#x60; with a &#x60;request_id&#x60;; poll &#x60;GET /v1/requests/{request_id}&#x60;. Its &#x60;wait&#x3D;&#x60; wins over &#x60;async_wait&#x60;; without one, &#x60;async_wait&#x60; sets the wait. | [optional] 
 **xCallbackURL** | **String** | An &#x60;https&#x60; URL that receives the signed &#x60;request.completed&#x60; webhook when the call finishes. Implies async: on its own (no &#x60;Prefer&#x60;, &#x60;async&#x60; or &#x60;async_wait&#x60;) the answer is an immediate &#x60;202&#x60;; with &#x60;Prefer: respond-async&#x60; or &#x60;async&#x3D;true&#x60; the call still waits 25 s unless a wait is given. Wins over &#x60;callback_url&#x60;. | [optional] 
 **idempotencyKey** | **String** | 1-200 visible ASCII characters, per account, kept as long as the result (about 15 minutes). The same key on the same call returns that call&#39;s current state (&#x60;Idempotent-Replayed: true&#x60;) without running or billing it again; on a different call it is &#x60;409 idempotency_key_reused&#x60;. Applies to async calls only; on a synchronous call it is ignored. Wins over &#x60;idempotency_key&#x60;. | [optional] 
 **async** | **Bool** | Query form of &#x60;Prefer: respond-async&#x60;: &#x60;true&#x60; or &#x60;1&#x60; (also &#x60;yes&#x60;, &#x60;on&#x60;; &#x60;false&#x60;, &#x60;0&#x60;, &#x60;no&#x60;, &#x60;off&#x60; leave the call synchronous). Waits 25 s unless &#x60;async_wait&#x60; is given. Not sent to the scraper. | [optional] 
 **asyncWait** | **Int** | Seconds (0-120; values outside are clamped) to wait for the result before answering &#x60;202&#x60;. Implies async. Not sent to the scraper. | [optional] 
 **callbackUrl** | **String** | Query form of &#x60;X-Callback-URL&#x60; (URL-encode it). Implies async; on its own the answer is an immediate &#x60;202&#x60; (wait 0). Not sent to the scraper. | [optional] 
 **idempotencyKey2** | **String** | Query form of &#x60;Idempotency-Key&#x60;. Not sent to the scraper. | [optional] 

### Return type

[**AutoScout24SearchResponse**](AutoScout24SearchResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

