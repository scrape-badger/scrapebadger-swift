# WebAPI

All URIs are relative to *https://scrapebadger.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**webDetectAntiBotAndCaptchaSystems**](WebAPI.md#webdetectantibotandcaptchasystems) | **POST** /v1/web/detect | Detect anti-bot and CAPTCHA systems
[**webExtractStructuredData**](WebAPI.md#webextractstructureddata) | **POST** /v1/web/extract | Extract structured data
[**webPollAnAutoUnblockDiscoveryJob**](WebAPI.md#webpollanautounblockdiscoveryjob) | **GET** /v1/web/unblock/{job_id} | Poll an auto-unblock discovery job
[**webScrapeAUrl**](WebAPI.md#webscrapeaurl) | **POST** /v1/web/scrape | Scrape a URL
[**webTakeAScreenshot**](WebAPI.md#webtakeascreenshot) | **POST** /v1/web/screenshot | Take a screenshot
[**webWebScraperHealthCheck**](WebAPI.md#webwebscraperhealthcheck) | **GET** /v1/web/health | Web scraper health check
[**webWebScraperHealthCheckHead**](WebAPI.md#webwebscraperhealthcheckhead) | **HEAD** /v1/web/health | Web scraper health check


# **webDetectAntiBotAndCaptchaSystems**
```swift
    open class func webDetectAntiBotAndCaptchaSystems(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Detect anti-bot and CAPTCHA systems

Detect which anti-bot and CAPTCHA systems are present on a URL.  Uses rnet to fetch the page and identify DataDome, Cloudflare, Akamai, Kasada, Amazon WAF, reCAPTCHA, hCaptcha, GeeTest, and more. Cost: 1 credit.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// Detect anti-bot and CAPTCHA systems
WebAPI.webDetectAntiBotAndCaptchaSystems() { (response, error) in
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

# **webExtractStructuredData**
```swift
    open class func webExtractStructuredData(extractRequest: ExtractRequest, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Extract structured data

Scrape a URL and extract fields with CSS/XPath selectors and/or AI.  ``extract_rules`` maps a field to a selector and returns ``data``; ``ai_extract_rules`` (field -> description) and ``ai_query`` return ``ai_extraction``. Billed as a scrape, plus the AI extraction credits when AI is asked for and succeeds.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let extractRequest = ExtractRequest(url: "url_example", waitFor: "waitFor_example", country: "country_example", proxyTier: "proxyTier_example", extractRules: "TODO", aiExtractRules: "TODO", aiQuery: "aiQuery_example", renderJs: false) // ExtractRequest | 

// Extract structured data
WebAPI.webExtractStructuredData(extractRequest: extractRequest) { (response, error) in
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
 **extractRequest** | [**ExtractRequest**](ExtractRequest.md) |  | 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **webPollAnAutoUnblockDiscoveryJob**
```swift
    open class func webPollAnAutoUnblockDiscoveryJob(jobId: String, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Poll an auto-unblock discovery job

Return the status + progress narration for an auto-unblock job.  Polled by the playground loader. ``job_id`` is an unguessable UUID handed out in the ``202 unblocking`` envelope and acts as a capability token, so any authenticated caller holding it can read the job (this is what lets several users share one discovery run's loader).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let jobId = "jobId_example" // String | 

// Poll an auto-unblock discovery job
WebAPI.webPollAnAutoUnblockDiscoveryJob(jobId: jobId) { (response, error) in
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
 **jobId** | **String** |  | 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **webScrapeAUrl**
```swift
    open class func webScrapeAUrl(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Scrape a URL

Scrape a URL and return its content.  The Generic Web Scraping API is fully user-driven: callers pick their own request parameters (engine, proxy tier, country, JS rendering, …). A blocked target surfaces the raw 422 ``blocking_page_detected`` so the caller can tune parameters themselves — we do NOT auto-trigger host discovery. Curated per-origin overrides (which the dedicated scraper APIs depend on) still apply.  One exception, added for SB-001083/SCR-64: a plain ``google.com/search`` web-SERP fetch is served by the dedicated Google scraper, whose rotation loop is built for SearchGuard. Same request shape, same response shape, billed at what it actually cost — the caller sees only a better hit rate. ``serp_adapter`` fails closed, so any request carrying a parameter it does not recognise as route-or-cost takes the generic path unchanged, and the user-driven contract above still holds.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// Scrape a URL
WebAPI.webScrapeAUrl() { (response, error) in
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

# **webTakeAScreenshot**
```swift
    open class func webTakeAScreenshot(screenshotRequest: ScreenshotRequest, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Take a screenshot

Render a URL in the browser engine and return a PNG screenshot.  ``screenshot`` is the PNG, base64-encoded. ``width``/``height`` set the viewport; ``full_page`` captures the whole scrollable page. Billed as a browser scrape (plus the proxy tier); a page that loads without a screenshot is a 502 and costs nothing.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let screenshotRequest = ScreenshotRequest(url: "url_example", waitFor: "waitFor_example", country: "country_example", proxyTier: "proxyTier_example", fullPage: false, width: 123, height: 123) // ScreenshotRequest | 

// Take a screenshot
WebAPI.webTakeAScreenshot(screenshotRequest: screenshotRequest) { (response, error) in
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
 **screenshotRequest** | [**ScreenshotRequest**](ScreenshotRequest.md) |  | 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **webWebScraperHealthCheck**
```swift
    open class func webWebScraperHealthCheck(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Web scraper health check

Check health of the web scraper service.  Bypasses the proxy abstraction because web-scraper exposes ``/health`` at the root (no ``/api/v1`` prefix, unlike the other scraper services).  Accepts ``HEAD`` so external uptime checkers (UptimeRobot uses HEAD by default for HTTP monitors) don't get a 405 Method Not Allowed.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// Web scraper health check
WebAPI.webWebScraperHealthCheck() { (response, error) in
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

# **webWebScraperHealthCheckHead**
```swift
    open class func webWebScraperHealthCheckHead(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Web scraper health check

Check health of the web scraper service.  Bypasses the proxy abstraction because web-scraper exposes ``/health`` at the root (no ``/api/v1`` prefix, unlike the other scraper services).  Accepts ``HEAD`` so external uptime checkers (UptimeRobot uses HEAD by default for HTTP monitors) don't get a 405 Method Not Allowed.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// Web scraper health check
WebAPI.webWebScraperHealthCheckHead() { (response, error) in
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

