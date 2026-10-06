# NaverAPI

All URIs are relative to *https://scrapebadger.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**naverNaverBlogSearch**](NaverAPI.md#navernaverblogsearch) | **GET** /v1/naver/blog | Naver blog search
[**naverNaverDatalabShoppingKeywordInsight**](NaverAPI.md#navernaverdatalabshoppingkeywordinsight) | **GET** /v1/naver/shopping/insight | Naver DataLab shopping keyword insight
[**naverNaverNewsSearch**](NaverAPI.md#navernavernewssearch) | **GET** /v1/naver/news | Naver news search
[**naverNaverPlaceDetail**](NaverAPI.md#navernaverplacedetail) | **GET** /v1/naver/place/{place_id} | Naver place detail
[**naverNaverPlaceLocalSearch**](NaverAPI.md#navernaverplacelocalsearch) | **GET** /v1/naver/local | Naver Place/Local search
[**naverNaverPlaceVisitorReviews**](NaverAPI.md#navernaverplacevisitorreviews) | **GET** /v1/naver/place/{place_id}/reviews | Naver place visitor reviews
[**naverNaverScraperHealthCheck**](NaverAPI.md#navernaverscraperhealthcheck) | **GET** /v1/naver/health | Naver scraper health check
[**naverNaverScraperHealthCheckHead**](NaverAPI.md#navernaverscraperhealthcheckhead) | **HEAD** /v1/naver/health | Naver scraper health check
[**naverNaverShoppingBestsellerRankings**](NaverAPI.md#navernavershoppingbestsellerrankings) | **GET** /v1/naver/shopping/bestsellers | Naver Shopping bestseller rankings
[**naverNaverShoppingCategoryReference**](NaverAPI.md#navernavershoppingcategoryreference) | **GET** /v1/naver/shopping/categories | Naver Shopping category reference
[**naverNaverShoppingTrendingKeywordRankings**](NaverAPI.md#navernavershoppingtrendingkeywordrankings) | **GET** /v1/naver/shopping/keywords | Naver Shopping trending keyword rankings
[**naverNaverWebSearch**](NaverAPI.md#navernaverwebsearch) | **GET** /v1/naver/search | Naver web search
[**naverSearchSuggestions**](NaverAPI.md#naversearchsuggestions) | **GET** /v1/naver/autocomplete | Search suggestions


# **naverNaverBlogSearch**
```swift
    open class func naverNaverBlogSearch(query: String, page: Int? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Naver blog search

Naver blog vertical — post title, blog name and real post URLs.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let query = "query_example" // String | 검색어
let page = 987 // Int |  (optional) (default to 1)

// Naver blog search
NaverAPI.naverNaverBlogSearch(query: query, page: page) { (response, error) in
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
 **query** | **String** | 검색어 | 
 **page** | **Int** |  | [optional] [default to 1]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **naverNaverDatalabShoppingKeywordInsight**
```swift
    open class func naverNaverDatalabShoppingKeywordInsight(categoryId: String, startDate: String, endDate: String, timeUnit: String? = nil, count: Int? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Naver DataLab shopping keyword insight

DataLab Shopping Insight — top search keywords in a category over a window.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let categoryId = "categoryId_example" // String | DataLab category id (cid), e.g. 50000000
let startDate = "startDate_example" // String | YYYY-MM-DD
let endDate = "endDate_example" // String | YYYY-MM-DD
let timeUnit = "timeUnit_example" // String | date | week | month (optional) (default to "date")
let count = 987 // Int | Keywords to return (optional) (default to 20)

// Naver DataLab shopping keyword insight
NaverAPI.naverNaverDatalabShoppingKeywordInsight(categoryId: categoryId, startDate: startDate, endDate: endDate, timeUnit: timeUnit, count: count) { (response, error) in
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
 **categoryId** | **String** | DataLab category id (cid), e.g. 50000000 | 
 **startDate** | **String** | YYYY-MM-DD | 
 **endDate** | **String** | YYYY-MM-DD | 
 **timeUnit** | **String** | date | week | month | [optional] [default to &quot;date&quot;]
 **count** | **Int** | Keywords to return | [optional] [default to 20]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **naverNaverNewsSearch**
```swift
    open class func naverNaverNewsSearch(query: String, page: Int? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Naver news search

Naver news vertical — publisher, age string and real article URLs.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let query = "query_example" // String | 검색어
let page = 987 // Int |  (optional) (default to 1)

// Naver news search
NaverAPI.naverNaverNewsSearch(query: query, page: page) { (response, error) in
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
 **query** | **String** | 검색어 | 
 **page** | **Int** |  | [optional] [default to 1]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **naverNaverPlaceDetail**
```swift
    open class func naverNaverPlaceDetail(placeId: String, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Naver place detail

Naver Place detail by place id.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let placeId = "placeId_example" // String | 

// Naver place detail
NaverAPI.naverNaverPlaceDetail(placeId: placeId) { (response, error) in
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
 **placeId** | **String** |  | 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **naverNaverPlaceLocalSearch**
```swift
    open class func naverNaverPlaceLocalSearch(query: String, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Naver Place/Local search

Naver Place/Local search — name, category, rating, hours status.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let query = "query_example" // String | Place query, e.g. '성남 카페'

// Naver Place/Local search
NaverAPI.naverNaverPlaceLocalSearch(query: query) { (response, error) in
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
 **query** | **String** | Place query, e.g. &#39;성남 카페&#39; | 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **naverNaverPlaceVisitorReviews**
```swift
    open class func naverNaverPlaceVisitorReviews(placeId: String, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Naver place visitor reviews

Visitor reviews for a Naver place — rating, body, reviewer, voted keywords, photos.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let placeId = "placeId_example" // String | 

// Naver place visitor reviews
NaverAPI.naverNaverPlaceVisitorReviews(placeId: placeId) { (response, error) in
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
 **placeId** | **String** |  | 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **naverNaverScraperHealthCheck**
```swift
    open class func naverNaverScraperHealthCheck(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Naver scraper health check

Check health of the Naver scraper service (accepts HEAD for UptimeRobot).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// Naver scraper health check
NaverAPI.naverNaverScraperHealthCheck() { (response, error) in
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

# **naverNaverScraperHealthCheckHead**
```swift
    open class func naverNaverScraperHealthCheckHead(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Naver scraper health check

Check health of the Naver scraper service (accepts HEAD for UptimeRobot).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// Naver scraper health check
NaverAPI.naverNaverScraperHealthCheckHead() { (response, error) in
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

# **naverNaverShoppingBestsellerRankings**
```swift
    open class func naverNaverShoppingBestsellerRankings(categoryId: String? = nil, ageType: String? = nil, sortType: String? = nil, periodType: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Naver Shopping bestseller rankings

Naver Shopping bestseller rankings — ranked products with price, review score, mall.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let categoryId = "categoryId_example" // String | Naver shopping category id, or ALL (optional) (default to "ALL")
let ageType = "ageType_example" // String | ALL | MEN_20 | WOMEN_20 | ... (optional) (default to "ALL")
let sortType = "sortType_example" // String | PRODUCT_CLICK | PRODUCT_BUY (optional) (default to "PRODUCT_CLICK")
let periodType = "periodType_example" // String | DAILY | WEEKLY (optional) (default to "DAILY")

// Naver Shopping bestseller rankings
NaverAPI.naverNaverShoppingBestsellerRankings(categoryId: categoryId, ageType: ageType, sortType: sortType, periodType: periodType) { (response, error) in
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
 **categoryId** | **String** | Naver shopping category id, or ALL | [optional] [default to &quot;ALL&quot;]
 **ageType** | **String** | ALL | MEN_20 | WOMEN_20 | ... | [optional] [default to &quot;ALL&quot;]
 **sortType** | **String** | PRODUCT_CLICK | PRODUCT_BUY | [optional] [default to &quot;PRODUCT_CLICK&quot;]
 **periodType** | **String** | DAILY | WEEKLY | [optional] [default to &quot;DAILY&quot;]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **naverNaverShoppingCategoryReference**
```swift
    open class func naverNaverShoppingCategoryReference(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Naver Shopping category reference

Naver Shopping top-level category ids (for bestsellers/keywords/insight). Free.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// Naver Shopping category reference
NaverAPI.naverNaverShoppingCategoryReference() { (response, error) in
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

# **naverNaverShoppingTrendingKeywordRankings**
```swift
    open class func naverNaverShoppingTrendingKeywordRankings(categoryId: String, ageType: String? = nil, sortType: String? = nil, periodType: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Naver Shopping trending keyword rankings

Trending Naver Shopping keywords for a category (snxbest keyword rankings).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let categoryId = "categoryId_example" // String | Naver shopping category id (see /shopping/categories)
let ageType = "ageType_example" // String | ALL | MEN_20 | WOMEN_20 | ... (optional) (default to "ALL")
let sortType = "sortType_example" // String |  (optional) (default to "KEYWORD_POPULAR")
let periodType = "periodType_example" // String | DAILY | WEEKLY (optional) (default to "WEEKLY")

// Naver Shopping trending keyword rankings
NaverAPI.naverNaverShoppingTrendingKeywordRankings(categoryId: categoryId, ageType: ageType, sortType: sortType, periodType: periodType) { (response, error) in
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
 **categoryId** | **String** | Naver shopping category id (see /shopping/categories) | 
 **ageType** | **String** | ALL | MEN_20 | WOMEN_20 | ... | [optional] [default to &quot;ALL&quot;]
 **sortType** | **String** |  | [optional] [default to &quot;KEYWORD_POPULAR&quot;]
 **periodType** | **String** | DAILY | WEEKLY | [optional] [default to &quot;WEEKLY&quot;]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **naverNaverWebSearch**
```swift
    open class func naverNaverWebSearch(query: String, page: Int? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Naver web search

Naver integrated SERP — organic results plus the inline Place pack.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let query = "query_example" // String | 검색어, e.g. '성남 카페'
let page = 987 // Int | Result page (optional) (default to 1)

// Naver web search
NaverAPI.naverNaverWebSearch(query: query, page: page) { (response, error) in
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
 **query** | **String** | 검색어, e.g. &#39;성남 카페&#39; | 
 **page** | **Int** | Result page | [optional] [default to 1]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **naverSearchSuggestions**
```swift
    open class func naverSearchSuggestions(query: String, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Search suggestions

Naver search-box suggestions.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let query = "query_example" // String | Partial search term

// Search suggestions
NaverAPI.naverSearchSuggestions(query: query) { (response, error) in
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
 **query** | **String** | Partial search term | 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

