# WallapopAPI

All URIs are relative to *https://scrapebadger.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**wallapopAutocomplete**](WallapopAPI.md#wallapopautocomplete) | **GET** /v1/wallapop/autocomplete | Autocomplete
[**wallapopGetListingDetail**](WallapopAPI.md#wallapopgetlistingdetail) | **GET** /v1/wallapop/items/{item_id} | Get listing detail
[**wallapopGetUserListings**](WallapopAPI.md#wallapopgetuserlistings) | **GET** /v1/wallapop/users/{user_id}/items | Get user listings
[**wallapopGetUserProfile**](WallapopAPI.md#wallapopgetuserprofile) | **GET** /v1/wallapop/users/{user_id} | Get user profile
[**wallapopGetUserReviews**](WallapopAPI.md#wallapopgetuserreviews) | **GET** /v1/wallapop/users/{user_id}/reviews | Get user reviews
[**wallapopListCategories**](WallapopAPI.md#wallapoplistcategories) | **GET** /v1/wallapop/categories | List categories
[**wallapopListFilterOptions**](WallapopAPI.md#wallapoplistfilteroptions) | **GET** /v1/wallapop/filters/{filter_id}/options | List filter options
[**wallapopListMarkets**](WallapopAPI.md#wallapoplistmarkets) | **GET** /v1/wallapop/markets | List markets
[**wallapopListSearchFilters**](WallapopAPI.md#wallapoplistsearchfilters) | **GET** /v1/wallapop/filters | List search filters
[**wallapopSearchListings**](WallapopAPI.md#wallapopsearchlistings) | **GET** /v1/wallapop/search | Search listings
[**wallapopWallapopScraperHealthCheck**](WallapopAPI.md#wallapopwallapopscraperhealthcheck) | **GET** /v1/wallapop/health | Wallapop scraper health check
[**wallapopWallapopScraperHealthCheckHead**](WallapopAPI.md#wallapopwallapopscraperhealthcheckhead) | **HEAD** /v1/wallapop/health | Wallapop scraper health check


# **wallapopAutocomplete**
```swift
    open class func wallapopAutocomplete(query: String, market: String? = nil, prefer: String? = nil, xCallbackURL: String? = nil, idempotencyKey: String? = nil, async: Bool? = nil, asyncWait: Int? = nil, callbackUrl: String? = nil, idempotencyKey2: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Autocomplete

Wallapop's search-box suggestions for a partial query.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let query = "query_example" // String | Partial search text, e.g. 'bici'
let market = "market_example" // String | Market: es (Spain), it (Italy), pt (Portugal) (optional) (default to "es")
let prefer = "prefer_example" // String | `respond-async[, wait=N]` (RFC 7240): run the call async. If it has not finished after `wait` seconds (0-120, default 25) the answer is `202` with a `request_id`; poll `GET /v1/requests/{request_id}`. Its `wait=` wins over `async_wait`; without one, `async_wait` sets the wait. (optional)
let xCallbackURL = "xCallbackURL_example" // String | An `https` URL that receives the signed `request.completed` webhook when the call finishes. Implies async: on its own (no `Prefer`, `async` or `async_wait`) the answer is an immediate `202`; with `Prefer: respond-async` or `async=true` the call still waits 25 s unless a wait is given. Wins over `callback_url`. (optional)
let idempotencyKey = "idempotencyKey_example" // String | 1-200 visible ASCII characters, per account, kept as long as the result (about 15 minutes). The same key on the same call returns that call's current state (`Idempotent-Replayed: true`) without running or billing it again; on a different call it is `409 idempotency_key_reused`. Applies to async calls only; on a synchronous call it is ignored. Wins over `idempotency_key`. (optional)
let async = true // Bool | Query form of `Prefer: respond-async`: `true` or `1` (also `yes`, `on`; `false`, `0`, `no`, `off` leave the call synchronous). Waits 25 s unless `async_wait` is given. Not sent to the scraper. (optional)
let asyncWait = 987 // Int | Seconds (0-120; values outside are clamped) to wait for the result before answering `202`. Implies async. Not sent to the scraper. (optional)
let callbackUrl = "callbackUrl_example" // String | Query form of `X-Callback-URL` (URL-encode it). Implies async; on its own the answer is an immediate `202` (wait 0). Not sent to the scraper. (optional)
let idempotencyKey2 = "idempotencyKey2_example" // String | Query form of `Idempotency-Key`. Not sent to the scraper. (optional)

// Autocomplete
WallapopAPI.wallapopAutocomplete(query: query, market: market, prefer: prefer, xCallbackURL: xCallbackURL, idempotencyKey: idempotencyKey, async: async, asyncWait: asyncWait, callbackUrl: callbackUrl, idempotencyKey2: idempotencyKey2) { (response, error) in
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
 **query** | **String** | Partial search text, e.g. &#39;bici&#39; | 
 **market** | **String** | Market: es (Spain), it (Italy), pt (Portugal) | [optional] [default to &quot;es&quot;]
 **prefer** | **String** | &#x60;respond-async[, wait&#x3D;N]&#x60; (RFC 7240): run the call async. If it has not finished after &#x60;wait&#x60; seconds (0-120, default 25) the answer is &#x60;202&#x60; with a &#x60;request_id&#x60;; poll &#x60;GET /v1/requests/{request_id}&#x60;. Its &#x60;wait&#x3D;&#x60; wins over &#x60;async_wait&#x60;; without one, &#x60;async_wait&#x60; sets the wait. | [optional] 
 **xCallbackURL** | **String** | An &#x60;https&#x60; URL that receives the signed &#x60;request.completed&#x60; webhook when the call finishes. Implies async: on its own (no &#x60;Prefer&#x60;, &#x60;async&#x60; or &#x60;async_wait&#x60;) the answer is an immediate &#x60;202&#x60;; with &#x60;Prefer: respond-async&#x60; or &#x60;async&#x3D;true&#x60; the call still waits 25 s unless a wait is given. Wins over &#x60;callback_url&#x60;. | [optional] 
 **idempotencyKey** | **String** | 1-200 visible ASCII characters, per account, kept as long as the result (about 15 minutes). The same key on the same call returns that call&#39;s current state (&#x60;Idempotent-Replayed: true&#x60;) without running or billing it again; on a different call it is &#x60;409 idempotency_key_reused&#x60;. Applies to async calls only; on a synchronous call it is ignored. Wins over &#x60;idempotency_key&#x60;. | [optional] 
 **async** | **Bool** | Query form of &#x60;Prefer: respond-async&#x60;: &#x60;true&#x60; or &#x60;1&#x60; (also &#x60;yes&#x60;, &#x60;on&#x60;; &#x60;false&#x60;, &#x60;0&#x60;, &#x60;no&#x60;, &#x60;off&#x60; leave the call synchronous). Waits 25 s unless &#x60;async_wait&#x60; is given. Not sent to the scraper. | [optional] 
 **asyncWait** | **Int** | Seconds (0-120; values outside are clamped) to wait for the result before answering &#x60;202&#x60;. Implies async. Not sent to the scraper. | [optional] 
 **callbackUrl** | **String** | Query form of &#x60;X-Callback-URL&#x60; (URL-encode it). Implies async; on its own the answer is an immediate &#x60;202&#x60; (wait 0). Not sent to the scraper. | [optional] 
 **idempotencyKey2** | **String** | Query form of &#x60;Idempotency-Key&#x60;. Not sent to the scraper. | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **wallapopGetListingDetail**
```swift
    open class func wallapopGetListingDetail(itemId: String, market: String? = nil, prefer: String? = nil, xCallbackURL: String? = nil, idempotencyKey: String? = nil, async: Bool? = nil, asyncWait: Int? = nil, callbackUrl: String? = nil, idempotencyKey2: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get listing detail

Full listing detail by id (e.g. nzxeknm5x562) or listing slug.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let itemId = "itemId_example" // String | 
let market = "market_example" // String | Market: es (Spain), it (Italy), pt (Portugal) (optional) (default to "es")
let prefer = "prefer_example" // String | `respond-async[, wait=N]` (RFC 7240): run the call async. If it has not finished after `wait` seconds (0-120, default 25) the answer is `202` with a `request_id`; poll `GET /v1/requests/{request_id}`. Its `wait=` wins over `async_wait`; without one, `async_wait` sets the wait. (optional)
let xCallbackURL = "xCallbackURL_example" // String | An `https` URL that receives the signed `request.completed` webhook when the call finishes. Implies async: on its own (no `Prefer`, `async` or `async_wait`) the answer is an immediate `202`; with `Prefer: respond-async` or `async=true` the call still waits 25 s unless a wait is given. Wins over `callback_url`. (optional)
let idempotencyKey = "idempotencyKey_example" // String | 1-200 visible ASCII characters, per account, kept as long as the result (about 15 minutes). The same key on the same call returns that call's current state (`Idempotent-Replayed: true`) without running or billing it again; on a different call it is `409 idempotency_key_reused`. Applies to async calls only; on a synchronous call it is ignored. Wins over `idempotency_key`. (optional)
let async = true // Bool | Query form of `Prefer: respond-async`: `true` or `1` (also `yes`, `on`; `false`, `0`, `no`, `off` leave the call synchronous). Waits 25 s unless `async_wait` is given. Not sent to the scraper. (optional)
let asyncWait = 987 // Int | Seconds (0-120; values outside are clamped) to wait for the result before answering `202`. Implies async. Not sent to the scraper. (optional)
let callbackUrl = "callbackUrl_example" // String | Query form of `X-Callback-URL` (URL-encode it). Implies async; on its own the answer is an immediate `202` (wait 0). Not sent to the scraper. (optional)
let idempotencyKey2 = "idempotencyKey2_example" // String | Query form of `Idempotency-Key`. Not sent to the scraper. (optional)

// Get listing detail
WallapopAPI.wallapopGetListingDetail(itemId: itemId, market: market, prefer: prefer, xCallbackURL: xCallbackURL, idempotencyKey: idempotencyKey, async: async, asyncWait: asyncWait, callbackUrl: callbackUrl, idempotencyKey2: idempotencyKey2) { (response, error) in
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
 **itemId** | **String** |  | 
 **market** | **String** | Market: es (Spain), it (Italy), pt (Portugal) | [optional] [default to &quot;es&quot;]
 **prefer** | **String** | &#x60;respond-async[, wait&#x3D;N]&#x60; (RFC 7240): run the call async. If it has not finished after &#x60;wait&#x60; seconds (0-120, default 25) the answer is &#x60;202&#x60; with a &#x60;request_id&#x60;; poll &#x60;GET /v1/requests/{request_id}&#x60;. Its &#x60;wait&#x3D;&#x60; wins over &#x60;async_wait&#x60;; without one, &#x60;async_wait&#x60; sets the wait. | [optional] 
 **xCallbackURL** | **String** | An &#x60;https&#x60; URL that receives the signed &#x60;request.completed&#x60; webhook when the call finishes. Implies async: on its own (no &#x60;Prefer&#x60;, &#x60;async&#x60; or &#x60;async_wait&#x60;) the answer is an immediate &#x60;202&#x60;; with &#x60;Prefer: respond-async&#x60; or &#x60;async&#x3D;true&#x60; the call still waits 25 s unless a wait is given. Wins over &#x60;callback_url&#x60;. | [optional] 
 **idempotencyKey** | **String** | 1-200 visible ASCII characters, per account, kept as long as the result (about 15 minutes). The same key on the same call returns that call&#39;s current state (&#x60;Idempotent-Replayed: true&#x60;) without running or billing it again; on a different call it is &#x60;409 idempotency_key_reused&#x60;. Applies to async calls only; on a synchronous call it is ignored. Wins over &#x60;idempotency_key&#x60;. | [optional] 
 **async** | **Bool** | Query form of &#x60;Prefer: respond-async&#x60;: &#x60;true&#x60; or &#x60;1&#x60; (also &#x60;yes&#x60;, &#x60;on&#x60;; &#x60;false&#x60;, &#x60;0&#x60;, &#x60;no&#x60;, &#x60;off&#x60; leave the call synchronous). Waits 25 s unless &#x60;async_wait&#x60; is given. Not sent to the scraper. | [optional] 
 **asyncWait** | **Int** | Seconds (0-120; values outside are clamped) to wait for the result before answering &#x60;202&#x60;. Implies async. Not sent to the scraper. | [optional] 
 **callbackUrl** | **String** | Query form of &#x60;X-Callback-URL&#x60; (URL-encode it). Implies async; on its own the answer is an immediate &#x60;202&#x60; (wait 0). Not sent to the scraper. | [optional] 
 **idempotencyKey2** | **String** | Query form of &#x60;Idempotency-Key&#x60;. Not sent to the scraper. | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **wallapopGetUserListings**
```swift
    open class func wallapopGetUserListings(userId: String, market: String? = nil, nextPage: String? = nil, prefer: String? = nil, xCallbackURL: String? = nil, idempotencyKey: String? = nil, async: Bool? = nil, asyncWait: Int? = nil, callbackUrl: String? = nil, idempotencyKey2: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get user listings

A seller's live listings, 40 per page.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let userId = "userId_example" // String | 
let market = "market_example" // String | Market: es (Spain), it (Italy), pt (Portugal) (optional) (default to "es")
let nextPage = "nextPage_example" // String | Cursor from the previous page's next_page (optional)
let prefer = "prefer_example" // String | `respond-async[, wait=N]` (RFC 7240): run the call async. If it has not finished after `wait` seconds (0-120, default 25) the answer is `202` with a `request_id`; poll `GET /v1/requests/{request_id}`. Its `wait=` wins over `async_wait`; without one, `async_wait` sets the wait. (optional)
let xCallbackURL = "xCallbackURL_example" // String | An `https` URL that receives the signed `request.completed` webhook when the call finishes. Implies async: on its own (no `Prefer`, `async` or `async_wait`) the answer is an immediate `202`; with `Prefer: respond-async` or `async=true` the call still waits 25 s unless a wait is given. Wins over `callback_url`. (optional)
let idempotencyKey = "idempotencyKey_example" // String | 1-200 visible ASCII characters, per account, kept as long as the result (about 15 minutes). The same key on the same call returns that call's current state (`Idempotent-Replayed: true`) without running or billing it again; on a different call it is `409 idempotency_key_reused`. Applies to async calls only; on a synchronous call it is ignored. Wins over `idempotency_key`. (optional)
let async = true // Bool | Query form of `Prefer: respond-async`: `true` or `1` (also `yes`, `on`; `false`, `0`, `no`, `off` leave the call synchronous). Waits 25 s unless `async_wait` is given. Not sent to the scraper. (optional)
let asyncWait = 987 // Int | Seconds (0-120; values outside are clamped) to wait for the result before answering `202`. Implies async. Not sent to the scraper. (optional)
let callbackUrl = "callbackUrl_example" // String | Query form of `X-Callback-URL` (URL-encode it). Implies async; on its own the answer is an immediate `202` (wait 0). Not sent to the scraper. (optional)
let idempotencyKey2 = "idempotencyKey2_example" // String | Query form of `Idempotency-Key`. Not sent to the scraper. (optional)

// Get user listings
WallapopAPI.wallapopGetUserListings(userId: userId, market: market, nextPage: nextPage, prefer: prefer, xCallbackURL: xCallbackURL, idempotencyKey: idempotencyKey, async: async, asyncWait: asyncWait, callbackUrl: callbackUrl, idempotencyKey2: idempotencyKey2) { (response, error) in
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
 **userId** | **String** |  | 
 **market** | **String** | Market: es (Spain), it (Italy), pt (Portugal) | [optional] [default to &quot;es&quot;]
 **nextPage** | **String** | Cursor from the previous page&#39;s next_page | [optional] 
 **prefer** | **String** | &#x60;respond-async[, wait&#x3D;N]&#x60; (RFC 7240): run the call async. If it has not finished after &#x60;wait&#x60; seconds (0-120, default 25) the answer is &#x60;202&#x60; with a &#x60;request_id&#x60;; poll &#x60;GET /v1/requests/{request_id}&#x60;. Its &#x60;wait&#x3D;&#x60; wins over &#x60;async_wait&#x60;; without one, &#x60;async_wait&#x60; sets the wait. | [optional] 
 **xCallbackURL** | **String** | An &#x60;https&#x60; URL that receives the signed &#x60;request.completed&#x60; webhook when the call finishes. Implies async: on its own (no &#x60;Prefer&#x60;, &#x60;async&#x60; or &#x60;async_wait&#x60;) the answer is an immediate &#x60;202&#x60;; with &#x60;Prefer: respond-async&#x60; or &#x60;async&#x3D;true&#x60; the call still waits 25 s unless a wait is given. Wins over &#x60;callback_url&#x60;. | [optional] 
 **idempotencyKey** | **String** | 1-200 visible ASCII characters, per account, kept as long as the result (about 15 minutes). The same key on the same call returns that call&#39;s current state (&#x60;Idempotent-Replayed: true&#x60;) without running or billing it again; on a different call it is &#x60;409 idempotency_key_reused&#x60;. Applies to async calls only; on a synchronous call it is ignored. Wins over &#x60;idempotency_key&#x60;. | [optional] 
 **async** | **Bool** | Query form of &#x60;Prefer: respond-async&#x60;: &#x60;true&#x60; or &#x60;1&#x60; (also &#x60;yes&#x60;, &#x60;on&#x60;; &#x60;false&#x60;, &#x60;0&#x60;, &#x60;no&#x60;, &#x60;off&#x60; leave the call synchronous). Waits 25 s unless &#x60;async_wait&#x60; is given. Not sent to the scraper. | [optional] 
 **asyncWait** | **Int** | Seconds (0-120; values outside are clamped) to wait for the result before answering &#x60;202&#x60;. Implies async. Not sent to the scraper. | [optional] 
 **callbackUrl** | **String** | Query form of &#x60;X-Callback-URL&#x60; (URL-encode it). Implies async; on its own the answer is an immediate &#x60;202&#x60; (wait 0). Not sent to the scraper. | [optional] 
 **idempotencyKey2** | **String** | Query form of &#x60;Idempotency-Key&#x60;. Not sent to the scraper. | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **wallapopGetUserProfile**
```swift
    open class func wallapopGetUserProfile(userId: String, market: String? = nil, prefer: String? = nil, xCallbackURL: String? = nil, idempotencyKey: String? = nil, async: Bool? = nil, asyncWait: Int? = nil, callbackUrl: String? = nil, idempotencyKey2: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get user profile

Seller profile with ratings, sales counters, response rate and verifications.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let userId = "userId_example" // String | 
let market = "market_example" // String | Market: es (Spain), it (Italy), pt (Portugal) (optional) (default to "es")
let prefer = "prefer_example" // String | `respond-async[, wait=N]` (RFC 7240): run the call async. If it has not finished after `wait` seconds (0-120, default 25) the answer is `202` with a `request_id`; poll `GET /v1/requests/{request_id}`. Its `wait=` wins over `async_wait`; without one, `async_wait` sets the wait. (optional)
let xCallbackURL = "xCallbackURL_example" // String | An `https` URL that receives the signed `request.completed` webhook when the call finishes. Implies async: on its own (no `Prefer`, `async` or `async_wait`) the answer is an immediate `202`; with `Prefer: respond-async` or `async=true` the call still waits 25 s unless a wait is given. Wins over `callback_url`. (optional)
let idempotencyKey = "idempotencyKey_example" // String | 1-200 visible ASCII characters, per account, kept as long as the result (about 15 minutes). The same key on the same call returns that call's current state (`Idempotent-Replayed: true`) without running or billing it again; on a different call it is `409 idempotency_key_reused`. Applies to async calls only; on a synchronous call it is ignored. Wins over `idempotency_key`. (optional)
let async = true // Bool | Query form of `Prefer: respond-async`: `true` or `1` (also `yes`, `on`; `false`, `0`, `no`, `off` leave the call synchronous). Waits 25 s unless `async_wait` is given. Not sent to the scraper. (optional)
let asyncWait = 987 // Int | Seconds (0-120; values outside are clamped) to wait for the result before answering `202`. Implies async. Not sent to the scraper. (optional)
let callbackUrl = "callbackUrl_example" // String | Query form of `X-Callback-URL` (URL-encode it). Implies async; on its own the answer is an immediate `202` (wait 0). Not sent to the scraper. (optional)
let idempotencyKey2 = "idempotencyKey2_example" // String | Query form of `Idempotency-Key`. Not sent to the scraper. (optional)

// Get user profile
WallapopAPI.wallapopGetUserProfile(userId: userId, market: market, prefer: prefer, xCallbackURL: xCallbackURL, idempotencyKey: idempotencyKey, async: async, asyncWait: asyncWait, callbackUrl: callbackUrl, idempotencyKey2: idempotencyKey2) { (response, error) in
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
 **userId** | **String** |  | 
 **market** | **String** | Market: es (Spain), it (Italy), pt (Portugal) | [optional] [default to &quot;es&quot;]
 **prefer** | **String** | &#x60;respond-async[, wait&#x3D;N]&#x60; (RFC 7240): run the call async. If it has not finished after &#x60;wait&#x60; seconds (0-120, default 25) the answer is &#x60;202&#x60; with a &#x60;request_id&#x60;; poll &#x60;GET /v1/requests/{request_id}&#x60;. Its &#x60;wait&#x3D;&#x60; wins over &#x60;async_wait&#x60;; without one, &#x60;async_wait&#x60; sets the wait. | [optional] 
 **xCallbackURL** | **String** | An &#x60;https&#x60; URL that receives the signed &#x60;request.completed&#x60; webhook when the call finishes. Implies async: on its own (no &#x60;Prefer&#x60;, &#x60;async&#x60; or &#x60;async_wait&#x60;) the answer is an immediate &#x60;202&#x60;; with &#x60;Prefer: respond-async&#x60; or &#x60;async&#x3D;true&#x60; the call still waits 25 s unless a wait is given. Wins over &#x60;callback_url&#x60;. | [optional] 
 **idempotencyKey** | **String** | 1-200 visible ASCII characters, per account, kept as long as the result (about 15 minutes). The same key on the same call returns that call&#39;s current state (&#x60;Idempotent-Replayed: true&#x60;) without running or billing it again; on a different call it is &#x60;409 idempotency_key_reused&#x60;. Applies to async calls only; on a synchronous call it is ignored. Wins over &#x60;idempotency_key&#x60;. | [optional] 
 **async** | **Bool** | Query form of &#x60;Prefer: respond-async&#x60;: &#x60;true&#x60; or &#x60;1&#x60; (also &#x60;yes&#x60;, &#x60;on&#x60;; &#x60;false&#x60;, &#x60;0&#x60;, &#x60;no&#x60;, &#x60;off&#x60; leave the call synchronous). Waits 25 s unless &#x60;async_wait&#x60; is given. Not sent to the scraper. | [optional] 
 **asyncWait** | **Int** | Seconds (0-120; values outside are clamped) to wait for the result before answering &#x60;202&#x60;. Implies async. Not sent to the scraper. | [optional] 
 **callbackUrl** | **String** | Query form of &#x60;X-Callback-URL&#x60; (URL-encode it). Implies async; on its own the answer is an immediate &#x60;202&#x60; (wait 0). Not sent to the scraper. | [optional] 
 **idempotencyKey2** | **String** | Query form of &#x60;Idempotency-Key&#x60;. Not sent to the scraper. | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **wallapopGetUserReviews**
```swift
    open class func wallapopGetUserReviews(userId: String, market: String? = nil, nextPage: String? = nil, prefer: String? = nil, xCallbackURL: String? = nil, idempotencyKey: String? = nil, async: Bool? = nil, asyncWait: Int? = nil, callbackUrl: String? = nil, idempotencyKey2: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get user reviews

Reviews a seller received, newest first, 40 per page.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let userId = "userId_example" // String | 
let market = "market_example" // String | Market: es (Spain), it (Italy), pt (Portugal) (optional) (default to "es")
let nextPage = "nextPage_example" // String | Cursor from the previous page's next_page (optional)
let prefer = "prefer_example" // String | `respond-async[, wait=N]` (RFC 7240): run the call async. If it has not finished after `wait` seconds (0-120, default 25) the answer is `202` with a `request_id`; poll `GET /v1/requests/{request_id}`. Its `wait=` wins over `async_wait`; without one, `async_wait` sets the wait. (optional)
let xCallbackURL = "xCallbackURL_example" // String | An `https` URL that receives the signed `request.completed` webhook when the call finishes. Implies async: on its own (no `Prefer`, `async` or `async_wait`) the answer is an immediate `202`; with `Prefer: respond-async` or `async=true` the call still waits 25 s unless a wait is given. Wins over `callback_url`. (optional)
let idempotencyKey = "idempotencyKey_example" // String | 1-200 visible ASCII characters, per account, kept as long as the result (about 15 minutes). The same key on the same call returns that call's current state (`Idempotent-Replayed: true`) without running or billing it again; on a different call it is `409 idempotency_key_reused`. Applies to async calls only; on a synchronous call it is ignored. Wins over `idempotency_key`. (optional)
let async = true // Bool | Query form of `Prefer: respond-async`: `true` or `1` (also `yes`, `on`; `false`, `0`, `no`, `off` leave the call synchronous). Waits 25 s unless `async_wait` is given. Not sent to the scraper. (optional)
let asyncWait = 987 // Int | Seconds (0-120; values outside are clamped) to wait for the result before answering `202`. Implies async. Not sent to the scraper. (optional)
let callbackUrl = "callbackUrl_example" // String | Query form of `X-Callback-URL` (URL-encode it). Implies async; on its own the answer is an immediate `202` (wait 0). Not sent to the scraper. (optional)
let idempotencyKey2 = "idempotencyKey2_example" // String | Query form of `Idempotency-Key`. Not sent to the scraper. (optional)

// Get user reviews
WallapopAPI.wallapopGetUserReviews(userId: userId, market: market, nextPage: nextPage, prefer: prefer, xCallbackURL: xCallbackURL, idempotencyKey: idempotencyKey, async: async, asyncWait: asyncWait, callbackUrl: callbackUrl, idempotencyKey2: idempotencyKey2) { (response, error) in
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
 **userId** | **String** |  | 
 **market** | **String** | Market: es (Spain), it (Italy), pt (Portugal) | [optional] [default to &quot;es&quot;]
 **nextPage** | **String** | Cursor from the previous page&#39;s next_page | [optional] 
 **prefer** | **String** | &#x60;respond-async[, wait&#x3D;N]&#x60; (RFC 7240): run the call async. If it has not finished after &#x60;wait&#x60; seconds (0-120, default 25) the answer is &#x60;202&#x60; with a &#x60;request_id&#x60;; poll &#x60;GET /v1/requests/{request_id}&#x60;. Its &#x60;wait&#x3D;&#x60; wins over &#x60;async_wait&#x60;; without one, &#x60;async_wait&#x60; sets the wait. | [optional] 
 **xCallbackURL** | **String** | An &#x60;https&#x60; URL that receives the signed &#x60;request.completed&#x60; webhook when the call finishes. Implies async: on its own (no &#x60;Prefer&#x60;, &#x60;async&#x60; or &#x60;async_wait&#x60;) the answer is an immediate &#x60;202&#x60;; with &#x60;Prefer: respond-async&#x60; or &#x60;async&#x3D;true&#x60; the call still waits 25 s unless a wait is given. Wins over &#x60;callback_url&#x60;. | [optional] 
 **idempotencyKey** | **String** | 1-200 visible ASCII characters, per account, kept as long as the result (about 15 minutes). The same key on the same call returns that call&#39;s current state (&#x60;Idempotent-Replayed: true&#x60;) without running or billing it again; on a different call it is &#x60;409 idempotency_key_reused&#x60;. Applies to async calls only; on a synchronous call it is ignored. Wins over &#x60;idempotency_key&#x60;. | [optional] 
 **async** | **Bool** | Query form of &#x60;Prefer: respond-async&#x60;: &#x60;true&#x60; or &#x60;1&#x60; (also &#x60;yes&#x60;, &#x60;on&#x60;; &#x60;false&#x60;, &#x60;0&#x60;, &#x60;no&#x60;, &#x60;off&#x60; leave the call synchronous). Waits 25 s unless &#x60;async_wait&#x60; is given. Not sent to the scraper. | [optional] 
 **asyncWait** | **Int** | Seconds (0-120; values outside are clamped) to wait for the result before answering &#x60;202&#x60;. Implies async. Not sent to the scraper. | [optional] 
 **callbackUrl** | **String** | Query form of &#x60;X-Callback-URL&#x60; (URL-encode it). Implies async; on its own the answer is an immediate &#x60;202&#x60; (wait 0). Not sent to the scraper. | [optional] 
 **idempotencyKey2** | **String** | Query form of &#x60;Idempotency-Key&#x60;. Not sent to the scraper. | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **wallapopListCategories**
```swift
    open class func wallapopListCategories(market: String? = nil, prefer: String? = nil, xCallbackURL: String? = nil, idempotencyKey: String? = nil, async: Bool? = nil, asyncWait: Int? = nil, callbackUrl: String? = nil, idempotencyKey2: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

List categories

The full category tree; top-level ids are the search category_id, nested subcategory ids go in subcategory_ids.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let market = "market_example" // String | Market: es (Spain), it (Italy), pt (Portugal) (optional) (default to "es")
let prefer = "prefer_example" // String | `respond-async[, wait=N]` (RFC 7240): run the call async. If it has not finished after `wait` seconds (0-120, default 25) the answer is `202` with a `request_id`; poll `GET /v1/requests/{request_id}`. Its `wait=` wins over `async_wait`; without one, `async_wait` sets the wait. (optional)
let xCallbackURL = "xCallbackURL_example" // String | An `https` URL that receives the signed `request.completed` webhook when the call finishes. Implies async: on its own (no `Prefer`, `async` or `async_wait`) the answer is an immediate `202`; with `Prefer: respond-async` or `async=true` the call still waits 25 s unless a wait is given. Wins over `callback_url`. (optional)
let idempotencyKey = "idempotencyKey_example" // String | 1-200 visible ASCII characters, per account, kept as long as the result (about 15 minutes). The same key on the same call returns that call's current state (`Idempotent-Replayed: true`) without running or billing it again; on a different call it is `409 idempotency_key_reused`. Applies to async calls only; on a synchronous call it is ignored. Wins over `idempotency_key`. (optional)
let async = true // Bool | Query form of `Prefer: respond-async`: `true` or `1` (also `yes`, `on`; `false`, `0`, `no`, `off` leave the call synchronous). Waits 25 s unless `async_wait` is given. Not sent to the scraper. (optional)
let asyncWait = 987 // Int | Seconds (0-120; values outside are clamped) to wait for the result before answering `202`. Implies async. Not sent to the scraper. (optional)
let callbackUrl = "callbackUrl_example" // String | Query form of `X-Callback-URL` (URL-encode it). Implies async; on its own the answer is an immediate `202` (wait 0). Not sent to the scraper. (optional)
let idempotencyKey2 = "idempotencyKey2_example" // String | Query form of `Idempotency-Key`. Not sent to the scraper. (optional)

// List categories
WallapopAPI.wallapopListCategories(market: market, prefer: prefer, xCallbackURL: xCallbackURL, idempotencyKey: idempotencyKey, async: async, asyncWait: asyncWait, callbackUrl: callbackUrl, idempotencyKey2: idempotencyKey2) { (response, error) in
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
 **market** | **String** | Market: es (Spain), it (Italy), pt (Portugal) | [optional] [default to &quot;es&quot;]
 **prefer** | **String** | &#x60;respond-async[, wait&#x3D;N]&#x60; (RFC 7240): run the call async. If it has not finished after &#x60;wait&#x60; seconds (0-120, default 25) the answer is &#x60;202&#x60; with a &#x60;request_id&#x60;; poll &#x60;GET /v1/requests/{request_id}&#x60;. Its &#x60;wait&#x3D;&#x60; wins over &#x60;async_wait&#x60;; without one, &#x60;async_wait&#x60; sets the wait. | [optional] 
 **xCallbackURL** | **String** | An &#x60;https&#x60; URL that receives the signed &#x60;request.completed&#x60; webhook when the call finishes. Implies async: on its own (no &#x60;Prefer&#x60;, &#x60;async&#x60; or &#x60;async_wait&#x60;) the answer is an immediate &#x60;202&#x60;; with &#x60;Prefer: respond-async&#x60; or &#x60;async&#x3D;true&#x60; the call still waits 25 s unless a wait is given. Wins over &#x60;callback_url&#x60;. | [optional] 
 **idempotencyKey** | **String** | 1-200 visible ASCII characters, per account, kept as long as the result (about 15 minutes). The same key on the same call returns that call&#39;s current state (&#x60;Idempotent-Replayed: true&#x60;) without running or billing it again; on a different call it is &#x60;409 idempotency_key_reused&#x60;. Applies to async calls only; on a synchronous call it is ignored. Wins over &#x60;idempotency_key&#x60;. | [optional] 
 **async** | **Bool** | Query form of &#x60;Prefer: respond-async&#x60;: &#x60;true&#x60; or &#x60;1&#x60; (also &#x60;yes&#x60;, &#x60;on&#x60;; &#x60;false&#x60;, &#x60;0&#x60;, &#x60;no&#x60;, &#x60;off&#x60; leave the call synchronous). Waits 25 s unless &#x60;async_wait&#x60; is given. Not sent to the scraper. | [optional] 
 **asyncWait** | **Int** | Seconds (0-120; values outside are clamped) to wait for the result before answering &#x60;202&#x60;. Implies async. Not sent to the scraper. | [optional] 
 **callbackUrl** | **String** | Query form of &#x60;X-Callback-URL&#x60; (URL-encode it). Implies async; on its own the answer is an immediate &#x60;202&#x60; (wait 0). Not sent to the scraper. | [optional] 
 **idempotencyKey2** | **String** | Query form of &#x60;Idempotency-Key&#x60;. Not sent to the scraper. | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **wallapopListFilterOptions**
```swift
    open class func wallapopListFilterOptions(filterId: String, categoryId: Int? = nil, subcategoryIds: String? = nil, query: String? = nil, market: String? = nil, prefer: String? = nil, xCallbackURL: String? = nil, idempotencyKey: String? = nil, async: Bool? = nil, asyncWait: Int? = nil, callbackUrl: String? = nil, idempotencyKey2: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

List filter options

Long option lists (e.g. brand, model) for filters flagged options_endpoint.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let filterId = "filterId_example" // String | 
let categoryId = 987 // Int | Category to scope options to (optional)
let subcategoryIds = "subcategoryIds_example" // String | Comma-separated subcategory ids (needs their category_id) (optional)
let query = "query_example" // String | Search text to scope options to (optional)
let market = "market_example" // String | Market: es (Spain), it (Italy), pt (Portugal) (optional) (default to "es")
let prefer = "prefer_example" // String | `respond-async[, wait=N]` (RFC 7240): run the call async. If it has not finished after `wait` seconds (0-120, default 25) the answer is `202` with a `request_id`; poll `GET /v1/requests/{request_id}`. Its `wait=` wins over `async_wait`; without one, `async_wait` sets the wait. (optional)
let xCallbackURL = "xCallbackURL_example" // String | An `https` URL that receives the signed `request.completed` webhook when the call finishes. Implies async: on its own (no `Prefer`, `async` or `async_wait`) the answer is an immediate `202`; with `Prefer: respond-async` or `async=true` the call still waits 25 s unless a wait is given. Wins over `callback_url`. (optional)
let idempotencyKey = "idempotencyKey_example" // String | 1-200 visible ASCII characters, per account, kept as long as the result (about 15 minutes). The same key on the same call returns that call's current state (`Idempotent-Replayed: true`) without running or billing it again; on a different call it is `409 idempotency_key_reused`. Applies to async calls only; on a synchronous call it is ignored. Wins over `idempotency_key`. (optional)
let async = true // Bool | Query form of `Prefer: respond-async`: `true` or `1` (also `yes`, `on`; `false`, `0`, `no`, `off` leave the call synchronous). Waits 25 s unless `async_wait` is given. Not sent to the scraper. (optional)
let asyncWait = 987 // Int | Seconds (0-120; values outside are clamped) to wait for the result before answering `202`. Implies async. Not sent to the scraper. (optional)
let callbackUrl = "callbackUrl_example" // String | Query form of `X-Callback-URL` (URL-encode it). Implies async; on its own the answer is an immediate `202` (wait 0). Not sent to the scraper. (optional)
let idempotencyKey2 = "idempotencyKey2_example" // String | Query form of `Idempotency-Key`. Not sent to the scraper. (optional)

// List filter options
WallapopAPI.wallapopListFilterOptions(filterId: filterId, categoryId: categoryId, subcategoryIds: subcategoryIds, query: query, market: market, prefer: prefer, xCallbackURL: xCallbackURL, idempotencyKey: idempotencyKey, async: async, asyncWait: asyncWait, callbackUrl: callbackUrl, idempotencyKey2: idempotencyKey2) { (response, error) in
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
 **filterId** | **String** |  | 
 **categoryId** | **Int** | Category to scope options to | [optional] 
 **subcategoryIds** | **String** | Comma-separated subcategory ids (needs their category_id) | [optional] 
 **query** | **String** | Search text to scope options to | [optional] 
 **market** | **String** | Market: es (Spain), it (Italy), pt (Portugal) | [optional] [default to &quot;es&quot;]
 **prefer** | **String** | &#x60;respond-async[, wait&#x3D;N]&#x60; (RFC 7240): run the call async. If it has not finished after &#x60;wait&#x60; seconds (0-120, default 25) the answer is &#x60;202&#x60; with a &#x60;request_id&#x60;; poll &#x60;GET /v1/requests/{request_id}&#x60;. Its &#x60;wait&#x3D;&#x60; wins over &#x60;async_wait&#x60;; without one, &#x60;async_wait&#x60; sets the wait. | [optional] 
 **xCallbackURL** | **String** | An &#x60;https&#x60; URL that receives the signed &#x60;request.completed&#x60; webhook when the call finishes. Implies async: on its own (no &#x60;Prefer&#x60;, &#x60;async&#x60; or &#x60;async_wait&#x60;) the answer is an immediate &#x60;202&#x60;; with &#x60;Prefer: respond-async&#x60; or &#x60;async&#x3D;true&#x60; the call still waits 25 s unless a wait is given. Wins over &#x60;callback_url&#x60;. | [optional] 
 **idempotencyKey** | **String** | 1-200 visible ASCII characters, per account, kept as long as the result (about 15 minutes). The same key on the same call returns that call&#39;s current state (&#x60;Idempotent-Replayed: true&#x60;) without running or billing it again; on a different call it is &#x60;409 idempotency_key_reused&#x60;. Applies to async calls only; on a synchronous call it is ignored. Wins over &#x60;idempotency_key&#x60;. | [optional] 
 **async** | **Bool** | Query form of &#x60;Prefer: respond-async&#x60;: &#x60;true&#x60; or &#x60;1&#x60; (also &#x60;yes&#x60;, &#x60;on&#x60;; &#x60;false&#x60;, &#x60;0&#x60;, &#x60;no&#x60;, &#x60;off&#x60; leave the call synchronous). Waits 25 s unless &#x60;async_wait&#x60; is given. Not sent to the scraper. | [optional] 
 **asyncWait** | **Int** | Seconds (0-120; values outside are clamped) to wait for the result before answering &#x60;202&#x60;. Implies async. Not sent to the scraper. | [optional] 
 **callbackUrl** | **String** | Query form of &#x60;X-Callback-URL&#x60; (URL-encode it). Implies async; on its own the answer is an immediate &#x60;202&#x60; (wait 0). Not sent to the scraper. | [optional] 
 **idempotencyKey2** | **String** | Query form of &#x60;Idempotency-Key&#x60;. Not sent to the scraper. | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **wallapopListMarkets**
```swift
    open class func wallapopListMarkets(prefer: String? = nil, xCallbackURL: String? = nil, idempotencyKey: String? = nil, async: Bool? = nil, asyncWait: Int? = nil, callbackUrl: String? = nil, idempotencyKey2: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

List markets

Supported Wallapop markets and their default search location.

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
WallapopAPI.wallapopListMarkets(prefer: prefer, xCallbackURL: xCallbackURL, idempotencyKey: idempotencyKey, async: async, asyncWait: asyncWait, callbackUrl: callbackUrl, idempotencyKey2: idempotencyKey2) { (response, error) in
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

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **wallapopListSearchFilters**
```swift
    open class func wallapopListSearchFilters(categoryId: Int? = nil, subcategoryIds: String? = nil, query: String? = nil, market: String? = nil, prefer: String? = nil, xCallbackURL: String? = nil, idempotencyKey: String? = nil, async: Bool? = nil, asyncWait: Int? = nil, callbackUrl: String? = nil, idempotencyKey2: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

List search filters

The filters Wallapop offers for a category or query, with option ids.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let categoryId = 987 // Int | Category the filters apply to (optional)
let subcategoryIds = "subcategoryIds_example" // String | Comma-separated subcategory ids (needs their category_id) (optional)
let query = "query_example" // String | Search text the filters apply to (optional)
let market = "market_example" // String | Market: es (Spain), it (Italy), pt (Portugal) (optional) (default to "es")
let prefer = "prefer_example" // String | `respond-async[, wait=N]` (RFC 7240): run the call async. If it has not finished after `wait` seconds (0-120, default 25) the answer is `202` with a `request_id`; poll `GET /v1/requests/{request_id}`. Its `wait=` wins over `async_wait`; without one, `async_wait` sets the wait. (optional)
let xCallbackURL = "xCallbackURL_example" // String | An `https` URL that receives the signed `request.completed` webhook when the call finishes. Implies async: on its own (no `Prefer`, `async` or `async_wait`) the answer is an immediate `202`; with `Prefer: respond-async` or `async=true` the call still waits 25 s unless a wait is given. Wins over `callback_url`. (optional)
let idempotencyKey = "idempotencyKey_example" // String | 1-200 visible ASCII characters, per account, kept as long as the result (about 15 minutes). The same key on the same call returns that call's current state (`Idempotent-Replayed: true`) without running or billing it again; on a different call it is `409 idempotency_key_reused`. Applies to async calls only; on a synchronous call it is ignored. Wins over `idempotency_key`. (optional)
let async = true // Bool | Query form of `Prefer: respond-async`: `true` or `1` (also `yes`, `on`; `false`, `0`, `no`, `off` leave the call synchronous). Waits 25 s unless `async_wait` is given. Not sent to the scraper. (optional)
let asyncWait = 987 // Int | Seconds (0-120; values outside are clamped) to wait for the result before answering `202`. Implies async. Not sent to the scraper. (optional)
let callbackUrl = "callbackUrl_example" // String | Query form of `X-Callback-URL` (URL-encode it). Implies async; on its own the answer is an immediate `202` (wait 0). Not sent to the scraper. (optional)
let idempotencyKey2 = "idempotencyKey2_example" // String | Query form of `Idempotency-Key`. Not sent to the scraper. (optional)

// List search filters
WallapopAPI.wallapopListSearchFilters(categoryId: categoryId, subcategoryIds: subcategoryIds, query: query, market: market, prefer: prefer, xCallbackURL: xCallbackURL, idempotencyKey: idempotencyKey, async: async, asyncWait: asyncWait, callbackUrl: callbackUrl, idempotencyKey2: idempotencyKey2) { (response, error) in
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
 **categoryId** | **Int** | Category the filters apply to | [optional] 
 **subcategoryIds** | **String** | Comma-separated subcategory ids (needs their category_id) | [optional] 
 **query** | **String** | Search text the filters apply to | [optional] 
 **market** | **String** | Market: es (Spain), it (Italy), pt (Portugal) | [optional] [default to &quot;es&quot;]
 **prefer** | **String** | &#x60;respond-async[, wait&#x3D;N]&#x60; (RFC 7240): run the call async. If it has not finished after &#x60;wait&#x60; seconds (0-120, default 25) the answer is &#x60;202&#x60; with a &#x60;request_id&#x60;; poll &#x60;GET /v1/requests/{request_id}&#x60;. Its &#x60;wait&#x3D;&#x60; wins over &#x60;async_wait&#x60;; without one, &#x60;async_wait&#x60; sets the wait. | [optional] 
 **xCallbackURL** | **String** | An &#x60;https&#x60; URL that receives the signed &#x60;request.completed&#x60; webhook when the call finishes. Implies async: on its own (no &#x60;Prefer&#x60;, &#x60;async&#x60; or &#x60;async_wait&#x60;) the answer is an immediate &#x60;202&#x60;; with &#x60;Prefer: respond-async&#x60; or &#x60;async&#x3D;true&#x60; the call still waits 25 s unless a wait is given. Wins over &#x60;callback_url&#x60;. | [optional] 
 **idempotencyKey** | **String** | 1-200 visible ASCII characters, per account, kept as long as the result (about 15 minutes). The same key on the same call returns that call&#39;s current state (&#x60;Idempotent-Replayed: true&#x60;) without running or billing it again; on a different call it is &#x60;409 idempotency_key_reused&#x60;. Applies to async calls only; on a synchronous call it is ignored. Wins over &#x60;idempotency_key&#x60;. | [optional] 
 **async** | **Bool** | Query form of &#x60;Prefer: respond-async&#x60;: &#x60;true&#x60; or &#x60;1&#x60; (also &#x60;yes&#x60;, &#x60;on&#x60;; &#x60;false&#x60;, &#x60;0&#x60;, &#x60;no&#x60;, &#x60;off&#x60; leave the call synchronous). Waits 25 s unless &#x60;async_wait&#x60; is given. Not sent to the scraper. | [optional] 
 **asyncWait** | **Int** | Seconds (0-120; values outside are clamped) to wait for the result before answering &#x60;202&#x60;. Implies async. Not sent to the scraper. | [optional] 
 **callbackUrl** | **String** | Query form of &#x60;X-Callback-URL&#x60; (URL-encode it). Implies async; on its own the answer is an immediate &#x60;202&#x60; (wait 0). Not sent to the scraper. | [optional] 
 **idempotencyKey2** | **String** | Query form of &#x60;Idempotency-Key&#x60;. Not sent to the scraper. | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **wallapopSearchListings**
```swift
    open class func wallapopSearchListings(query: String? = nil, market: String? = nil, latitude: Double? = nil, longitude: Double? = nil, distanceKm: Int? = nil, categoryId: Int? = nil, subcategoryIds: String? = nil, minPrice: Double? = nil, maxPrice: Double? = nil, condition: String? = nil, brand: String? = nil, model: String? = nil, color: String? = nil, timeFilter: TimeFilter_wallapopSearchListings? = nil, shippable: Bool? = nil, hasWarranty: Bool? = nil, refurbished: Bool? = nil, minYear: Int? = nil, maxYear: Int? = nil, minKm: Int? = nil, maxKm: Int? = nil, gearbox: Gearbox_wallapopSearchListings? = nil, minHorsepower: Int? = nil, maxHorsepower: Int? = nil, orderBy: OrderBy_wallapopSearchListings? = nil, nextPage: String? = nil, prefer: String? = nil, xCallbackURL: String? = nil, idempotencyKey: String? = nil, async: Bool? = nil, asyncWait: Int? = nil, callbackUrl: String? = nil, idempotencyKey2: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Search listings

Search Wallapop listings (40 per page). Needs a query, a category_id, subcategory_ids, or a combination.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let query = "query_example" // String | Search text, e.g. 'iphone 14' (optional)
let market = "market_example" // String | Market: es (Spain), it (Italy), pt (Portugal) (optional) (default to "es")
let latitude = 987 // Double | Search centre latitude (defaults to the market capital) (optional)
let longitude = 987 // Double | Search centre longitude (optional)
let distanceKm = 987 // Int | Search radius (optional)
let categoryId = 987 // Int | Category id from /categories (optional)
let subcategoryIds = "subcategoryIds_example" // String | Comma-separated subcategory ids from /categories (any level of the tree), e.g. 9447 (Smartphones) or 9447,10310 (optional)
let minPrice = 987 // Double | Minimum price (EUR) (optional)
let maxPrice = 987 // Double | Maximum price (EUR) (optional)
let condition = "condition_example" // String | Comma-separated: un_opened, in_box, new, as_good_as_new, good, fair, has_given_it_all (optional)
let brand = "brand_example" // String | Brand, e.g. Apple (optional)
let model = "model_example" // String | Model, e.g. iPhone 14 (optional)
let color = "color_example" // String | Colour id, e.g. black (optional)
let timeFilter = "timeFilter_example" // String | Only listings published within this window (optional)
let shippable = true // Bool | Only listings that ship (optional) (default to false)
let hasWarranty = true // Bool | Only listings with a warranty (optional) (default to false)
let refurbished = true // Bool | Only refurbished listings (optional) (default to false)
let minYear = 987 // Int | Cars: earliest model year (optional)
let maxYear = 987 // Int | Cars: latest model year (optional)
let minKm = 987 // Int | Cars: minimum mileage (optional)
let maxKm = 987 // Int | Cars: maximum mileage (optional)
let gearbox = "gearbox_example" // String | Cars (optional)
let minHorsepower = 987 // Int | Cars: minimum power (optional)
let maxHorsepower = 987 // Int | Cars: maximum power (optional)
let orderBy = "orderBy_example" // String | Sort order (optional) (default to .mostRelevance)
let nextPage = "nextPage_example" // String | Cursor from the previous page's next_page; other parameters are then ignored (optional)
let prefer = "prefer_example" // String | `respond-async[, wait=N]` (RFC 7240): run the call async. If it has not finished after `wait` seconds (0-120, default 25) the answer is `202` with a `request_id`; poll `GET /v1/requests/{request_id}`. Its `wait=` wins over `async_wait`; without one, `async_wait` sets the wait. (optional)
let xCallbackURL = "xCallbackURL_example" // String | An `https` URL that receives the signed `request.completed` webhook when the call finishes. Implies async: on its own (no `Prefer`, `async` or `async_wait`) the answer is an immediate `202`; with `Prefer: respond-async` or `async=true` the call still waits 25 s unless a wait is given. Wins over `callback_url`. (optional)
let idempotencyKey = "idempotencyKey_example" // String | 1-200 visible ASCII characters, per account, kept as long as the result (about 15 minutes). The same key on the same call returns that call's current state (`Idempotent-Replayed: true`) without running or billing it again; on a different call it is `409 idempotency_key_reused`. Applies to async calls only; on a synchronous call it is ignored. Wins over `idempotency_key`. (optional)
let async = true // Bool | Query form of `Prefer: respond-async`: `true` or `1` (also `yes`, `on`; `false`, `0`, `no`, `off` leave the call synchronous). Waits 25 s unless `async_wait` is given. Not sent to the scraper. (optional)
let asyncWait = 987 // Int | Seconds (0-120; values outside are clamped) to wait for the result before answering `202`. Implies async. Not sent to the scraper. (optional)
let callbackUrl = "callbackUrl_example" // String | Query form of `X-Callback-URL` (URL-encode it). Implies async; on its own the answer is an immediate `202` (wait 0). Not sent to the scraper. (optional)
let idempotencyKey2 = "idempotencyKey2_example" // String | Query form of `Idempotency-Key`. Not sent to the scraper. (optional)

// Search listings
WallapopAPI.wallapopSearchListings(query: query, market: market, latitude: latitude, longitude: longitude, distanceKm: distanceKm, categoryId: categoryId, subcategoryIds: subcategoryIds, minPrice: minPrice, maxPrice: maxPrice, condition: condition, brand: brand, model: model, color: color, timeFilter: timeFilter, shippable: shippable, hasWarranty: hasWarranty, refurbished: refurbished, minYear: minYear, maxYear: maxYear, minKm: minKm, maxKm: maxKm, gearbox: gearbox, minHorsepower: minHorsepower, maxHorsepower: maxHorsepower, orderBy: orderBy, nextPage: nextPage, prefer: prefer, xCallbackURL: xCallbackURL, idempotencyKey: idempotencyKey, async: async, asyncWait: asyncWait, callbackUrl: callbackUrl, idempotencyKey2: idempotencyKey2) { (response, error) in
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
 **query** | **String** | Search text, e.g. &#39;iphone 14&#39; | [optional] 
 **market** | **String** | Market: es (Spain), it (Italy), pt (Portugal) | [optional] [default to &quot;es&quot;]
 **latitude** | **Double** | Search centre latitude (defaults to the market capital) | [optional] 
 **longitude** | **Double** | Search centre longitude | [optional] 
 **distanceKm** | **Int** | Search radius | [optional] 
 **categoryId** | **Int** | Category id from /categories | [optional] 
 **subcategoryIds** | **String** | Comma-separated subcategory ids from /categories (any level of the tree), e.g. 9447 (Smartphones) or 9447,10310 | [optional] 
 **minPrice** | **Double** | Minimum price (EUR) | [optional] 
 **maxPrice** | **Double** | Maximum price (EUR) | [optional] 
 **condition** | **String** | Comma-separated: un_opened, in_box, new, as_good_as_new, good, fair, has_given_it_all | [optional] 
 **brand** | **String** | Brand, e.g. Apple | [optional] 
 **model** | **String** | Model, e.g. iPhone 14 | [optional] 
 **color** | **String** | Colour id, e.g. black | [optional] 
 **timeFilter** | **String** | Only listings published within this window | [optional] 
 **shippable** | **Bool** | Only listings that ship | [optional] [default to false]
 **hasWarranty** | **Bool** | Only listings with a warranty | [optional] [default to false]
 **refurbished** | **Bool** | Only refurbished listings | [optional] [default to false]
 **minYear** | **Int** | Cars: earliest model year | [optional] 
 **maxYear** | **Int** | Cars: latest model year | [optional] 
 **minKm** | **Int** | Cars: minimum mileage | [optional] 
 **maxKm** | **Int** | Cars: maximum mileage | [optional] 
 **gearbox** | **String** | Cars | [optional] 
 **minHorsepower** | **Int** | Cars: minimum power | [optional] 
 **maxHorsepower** | **Int** | Cars: maximum power | [optional] 
 **orderBy** | **String** | Sort order | [optional] [default to .mostRelevance]
 **nextPage** | **String** | Cursor from the previous page&#39;s next_page; other parameters are then ignored | [optional] 
 **prefer** | **String** | &#x60;respond-async[, wait&#x3D;N]&#x60; (RFC 7240): run the call async. If it has not finished after &#x60;wait&#x60; seconds (0-120, default 25) the answer is &#x60;202&#x60; with a &#x60;request_id&#x60;; poll &#x60;GET /v1/requests/{request_id}&#x60;. Its &#x60;wait&#x3D;&#x60; wins over &#x60;async_wait&#x60;; without one, &#x60;async_wait&#x60; sets the wait. | [optional] 
 **xCallbackURL** | **String** | An &#x60;https&#x60; URL that receives the signed &#x60;request.completed&#x60; webhook when the call finishes. Implies async: on its own (no &#x60;Prefer&#x60;, &#x60;async&#x60; or &#x60;async_wait&#x60;) the answer is an immediate &#x60;202&#x60;; with &#x60;Prefer: respond-async&#x60; or &#x60;async&#x3D;true&#x60; the call still waits 25 s unless a wait is given. Wins over &#x60;callback_url&#x60;. | [optional] 
 **idempotencyKey** | **String** | 1-200 visible ASCII characters, per account, kept as long as the result (about 15 minutes). The same key on the same call returns that call&#39;s current state (&#x60;Idempotent-Replayed: true&#x60;) without running or billing it again; on a different call it is &#x60;409 idempotency_key_reused&#x60;. Applies to async calls only; on a synchronous call it is ignored. Wins over &#x60;idempotency_key&#x60;. | [optional] 
 **async** | **Bool** | Query form of &#x60;Prefer: respond-async&#x60;: &#x60;true&#x60; or &#x60;1&#x60; (also &#x60;yes&#x60;, &#x60;on&#x60;; &#x60;false&#x60;, &#x60;0&#x60;, &#x60;no&#x60;, &#x60;off&#x60; leave the call synchronous). Waits 25 s unless &#x60;async_wait&#x60; is given. Not sent to the scraper. | [optional] 
 **asyncWait** | **Int** | Seconds (0-120; values outside are clamped) to wait for the result before answering &#x60;202&#x60;. Implies async. Not sent to the scraper. | [optional] 
 **callbackUrl** | **String** | Query form of &#x60;X-Callback-URL&#x60; (URL-encode it). Implies async; on its own the answer is an immediate &#x60;202&#x60; (wait 0). Not sent to the scraper. | [optional] 
 **idempotencyKey2** | **String** | Query form of &#x60;Idempotency-Key&#x60;. Not sent to the scraper. | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **wallapopWallapopScraperHealthCheck**
```swift
    open class func wallapopWallapopScraperHealthCheck(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Wallapop scraper health check

Check health of the Wallapop scraper service (accepts HEAD).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// Wallapop scraper health check
WallapopAPI.wallapopWallapopScraperHealthCheck() { (response, error) in
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

# **wallapopWallapopScraperHealthCheckHead**
```swift
    open class func wallapopWallapopScraperHealthCheckHead(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Wallapop scraper health check

Check health of the Wallapop scraper service (accepts HEAD).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// Wallapop scraper health check
WallapopAPI.wallapopWallapopScraperHealthCheckHead() { (response, error) in
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

