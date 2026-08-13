# TikTokAPI

All URIs are relative to *https://scrapebadger.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**tiktokGeneralSearch**](TikTokAPI.md#tiktokgeneralsearch) | **GET** /v1/tiktok/search | General search
[**tiktokGetCommentReplies**](TikTokAPI.md#tiktokgetcommentreplies) | **GET** /v1/tiktok/comments/{comment_id}/replies | Get comment replies
[**tiktokGetComments**](TikTokAPI.md#tiktokgetcomments) | **GET** /v1/tiktok/videos/{video_id}/comments | Get comments
[**tiktokGetFollowersDeprecated**](TikTokAPI.md#tiktokgetfollowersdeprecated) | **GET** /v1/tiktok/users/{username}/followers | Get followers (deprecated)
[**tiktokGetFollowingDeprecated**](TikTokAPI.md#tiktokgetfollowingdeprecated) | **GET** /v1/tiktok/users/{username}/following | Get following (deprecated)
[**tiktokGetHashtagDetail**](TikTokAPI.md#tiktokgethashtagdetail) | **GET** /v1/tiktok/hashtags/{name} | Get hashtag detail
[**tiktokGetHashtagVideos**](TikTokAPI.md#tiktokgethashtagvideos) | **GET** /v1/tiktok/hashtags/{name}/videos | Get hashtag videos
[**tiktokGetLikedVideosDeprecated**](TikTokAPI.md#tiktokgetlikedvideosdeprecated) | **GET** /v1/tiktok/users/{username}/liked | Get liked videos (deprecated)
[**tiktokGetMusicSoundDetail**](TikTokAPI.md#tiktokgetmusicsounddetail) | **GET** /v1/tiktok/music/{music_id} | Get music/sound detail
[**tiktokGetMusicVideos**](TikTokAPI.md#tiktokgetmusicvideos) | **GET** /v1/tiktok/music/{music_id}/videos | Get music videos
[**tiktokGetOembedMetadata**](TikTokAPI.md#tiktokgetoembedmetadata) | **GET** /v1/tiktok/oembed | Get oEmbed metadata
[**tiktokGetRelatedVideos**](TikTokAPI.md#tiktokgetrelatedvideos) | **GET** /v1/tiktok/videos/{video_id}/related | Get related videos
[**tiktokGetReposts**](TikTokAPI.md#tiktokgetreposts) | **GET** /v1/tiktok/users/{username}/reposts | Get reposts
[**tiktokGetTiktokAdDetail**](TikTokAPI.md#tiktokgettiktokaddetail) | **GET** /v1/tiktok/ads/{ad_id} | Get TikTok ad detail
[**tiktokGetTranscript**](TikTokAPI.md#tiktokgettranscript) | **GET** /v1/tiktok/videos/{video_id}/transcript | Get transcript
[**tiktokGetUserProfile**](TikTokAPI.md#tiktokgetuserprofile) | **GET** /v1/tiktok/users/{username} | Get user profile
[**tiktokGetUserVideos**](TikTokAPI.md#tiktokgetuservideos) | **GET** /v1/tiktok/users/{username}/videos | Get user videos
[**tiktokGetVideoDetail**](TikTokAPI.md#tiktokgetvideodetail) | **GET** /v1/tiktok/videos/{video_id} | Get video detail
[**tiktokHealthCheck**](TikTokAPI.md#tiktokhealthcheck) | **GET** /v1/tiktok/health | Health check
[**tiktokHealthCheckHead**](TikTokAPI.md#tiktokhealthcheckhead) | **HEAD** /v1/tiktok/health | Health check
[**tiktokListRegions**](TikTokAPI.md#tiktoklistregions) | **GET** /v1/tiktok/regions | List regions
[**tiktokSearchHashtags**](TikTokAPI.md#tiktoksearchhashtags) | **GET** /v1/tiktok/search/hashtags | Search hashtags
[**tiktokSearchTheTiktokAdLibrary**](TikTokAPI.md#tiktoksearchthetiktokadlibrary) | **GET** /v1/tiktok/ads/search | Search the TikTok Ad Library
[**tiktokSearchTiktokAdvertisers**](TikTokAPI.md#tiktoksearchtiktokadvertisers) | **GET** /v1/tiktok/ads/advertisers | Search TikTok advertisers
[**tiktokSearchUsers**](TikTokAPI.md#tiktoksearchusers) | **GET** /v1/tiktok/search/users | Search users
[**tiktokSearchVideos**](TikTokAPI.md#tiktoksearchvideos) | **GET** /v1/tiktok/search/videos | Search videos
[**tiktokTrendingHashtags**](TikTokAPI.md#tiktoktrendinghashtags) | **GET** /v1/tiktok/trending/hashtags | Trending hashtags
[**tiktokTrendingSongs**](TikTokAPI.md#tiktoktrendingsongs) | **GET** /v1/tiktok/trending/songs | Trending songs
[**tiktokTrendingVideos**](TikTokAPI.md#tiktoktrendingvideos) | **GET** /v1/tiktok/trending/videos | Trending videos


# **tiktokGeneralSearch**
```swift
    open class func tiktokGeneralSearch(query: String, region: String? = nil, count: Int? = nil, cursor: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

General search

General TikTok search — video results from the Top feed.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let query = "query_example" // String | Search keyword
let region = "region_example" // String |  (optional) (default to "US")
let count = 987 // Int |  (optional) (default to 20)
let cursor = "cursor_example" // String | Composite pagination cursor (offset.search_id) from a prior page's pagination.cursor (optional)

// General search
TikTokAPI.tiktokGeneralSearch(query: query, region: region, count: count, cursor: cursor) { (response, error) in
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
 **query** | **String** | Search keyword | 
 **region** | **String** |  | [optional] [default to &quot;US&quot;]
 **count** | **Int** |  | [optional] [default to 20]
 **cursor** | **String** | Composite pagination cursor (offset.search_id) from a prior page&#39;s pagination.cursor | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **tiktokGetCommentReplies**
```swift
    open class func tiktokGetCommentReplies(commentId: String, videoId: String, region: String? = nil, count: Int? = nil, cursor: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get comment replies

Get replies to a TikTok comment (best-effort).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let commentId = "commentId_example" // String | 
let videoId = "videoId_example" // String | Parent video id
let region = "region_example" // String |  (optional) (default to "US")
let count = 987 // Int |  (optional) (default to 20)
let cursor = "cursor_example" // String | Pagination cursor from a prior page's pagination.cursor (optional)

// Get comment replies
TikTokAPI.tiktokGetCommentReplies(commentId: commentId, videoId: videoId, region: region, count: count, cursor: cursor) { (response, error) in
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
 **commentId** | **String** |  | 
 **videoId** | **String** | Parent video id | 
 **region** | **String** |  | [optional] [default to &quot;US&quot;]
 **count** | **Int** |  | [optional] [default to 20]
 **cursor** | **String** | Pagination cursor from a prior page&#39;s pagination.cursor | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **tiktokGetComments**
```swift
    open class func tiktokGetComments(videoId: String, region: String? = nil, count: Int? = nil, cursor: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get comments

Get top-level comments on a TikTok video.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let videoId = "videoId_example" // String | 
let region = "region_example" // String |  (optional) (default to "US")
let count = 987 // Int |  (optional) (default to 20)
let cursor = "cursor_example" // String | Pagination cursor from a prior page's pagination.cursor (optional)

// Get comments
TikTokAPI.tiktokGetComments(videoId: videoId, region: region, count: count, cursor: cursor) { (response, error) in
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
 **videoId** | **String** |  | 
 **region** | **String** |  | [optional] [default to &quot;US&quot;]
 **count** | **Int** |  | [optional] [default to 20]
 **cursor** | **String** | Pagination cursor from a prior page&#39;s pagination.cursor | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **tiktokGetFollowersDeprecated**
```swift
    open class func tiktokGetFollowersDeprecated(username: String, region: String? = nil, count: Int? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get followers (deprecated)

DEPRECATED — TikTok followers require an authenticated account session. Returns HTTP 410.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let username = "username_example" // String | 
let region = "region_example" // String |  (optional) (default to "US")
let count = 987 // Int |  (optional) (default to 30)

// Get followers (deprecated)
TikTokAPI.tiktokGetFollowersDeprecated(username: username, region: region, count: count) { (response, error) in
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
 **username** | **String** |  | 
 **region** | **String** |  | [optional] [default to &quot;US&quot;]
 **count** | **Int** |  | [optional] [default to 30]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **tiktokGetFollowingDeprecated**
```swift
    open class func tiktokGetFollowingDeprecated(username: String, region: String? = nil, count: Int? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get following (deprecated)

DEPRECATED — TikTok following requires an authenticated account session. Returns HTTP 410.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let username = "username_example" // String | 
let region = "region_example" // String |  (optional) (default to "US")
let count = 987 // Int |  (optional) (default to 30)

// Get following (deprecated)
TikTokAPI.tiktokGetFollowingDeprecated(username: username, region: region, count: count) { (response, error) in
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
 **username** | **String** |  | 
 **region** | **String** |  | [optional] [default to &quot;US&quot;]
 **count** | **Int** |  | [optional] [default to 30]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **tiktokGetHashtagDetail**
```swift
    open class func tiktokGetHashtagDetail(name: String, region: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get hashtag detail

Get TikTok hashtag/challenge detail.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let name = "name_example" // String | 
let region = "region_example" // String |  (optional) (default to "US")

// Get hashtag detail
TikTokAPI.tiktokGetHashtagDetail(name: name, region: region) { (response, error) in
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
 **name** | **String** |  | 
 **region** | **String** |  | [optional] [default to &quot;US&quot;]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **tiktokGetHashtagVideos**
```swift
    open class func tiktokGetHashtagVideos(name: String, region: String? = nil, count: Int? = nil, cursor: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get hashtag videos

Get videos tagged with a TikTok hashtag.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let name = "name_example" // String | 
let region = "region_example" // String |  (optional) (default to "US")
let count = 987 // Int |  (optional) (default to 30)
let cursor = "cursor_example" // String | Pagination cursor from a prior page's pagination.cursor (optional)

// Get hashtag videos
TikTokAPI.tiktokGetHashtagVideos(name: name, region: region, count: count, cursor: cursor) { (response, error) in
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
 **name** | **String** |  | 
 **region** | **String** |  | [optional] [default to &quot;US&quot;]
 **count** | **Int** |  | [optional] [default to 30]
 **cursor** | **String** | Pagination cursor from a prior page&#39;s pagination.cursor | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **tiktokGetLikedVideosDeprecated**
```swift
    open class func tiktokGetLikedVideosDeprecated(username: String, region: String? = nil, count: Int? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get liked videos (deprecated)

DEPRECATED — TikTok liked videos require an authenticated account session. Returns HTTP 410.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let username = "username_example" // String | 
let region = "region_example" // String |  (optional) (default to "US")
let count = 987 // Int |  (optional) (default to 30)

// Get liked videos (deprecated)
TikTokAPI.tiktokGetLikedVideosDeprecated(username: username, region: region, count: count) { (response, error) in
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
 **username** | **String** |  | 
 **region** | **String** |  | [optional] [default to &quot;US&quot;]
 **count** | **Int** |  | [optional] [default to 30]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **tiktokGetMusicSoundDetail**
```swift
    open class func tiktokGetMusicSoundDetail(musicId: String, region: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get music/sound detail

Get TikTok sound/music detail.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let musicId = "musicId_example" // String | 
let region = "region_example" // String |  (optional) (default to "US")

// Get music/sound detail
TikTokAPI.tiktokGetMusicSoundDetail(musicId: musicId, region: region) { (response, error) in
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
 **musicId** | **String** |  | 
 **region** | **String** |  | [optional] [default to &quot;US&quot;]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **tiktokGetMusicVideos**
```swift
    open class func tiktokGetMusicVideos(musicId: String, region: String? = nil, count: Int? = nil, cursor: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get music videos

Get videos using a given TikTok sound.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let musicId = "musicId_example" // String | 
let region = "region_example" // String |  (optional) (default to "US")
let count = 987 // Int |  (optional) (default to 30)
let cursor = "cursor_example" // String | Pagination cursor from a prior page's pagination.cursor (optional)

// Get music videos
TikTokAPI.tiktokGetMusicVideos(musicId: musicId, region: region, count: count, cursor: cursor) { (response, error) in
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
 **musicId** | **String** |  | 
 **region** | **String** |  | [optional] [default to &quot;US&quot;]
 **count** | **Int** |  | [optional] [default to 30]
 **cursor** | **String** | Pagination cursor from a prior page&#39;s pagination.cursor | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **tiktokGetOembedMetadata**
```swift
    open class func tiktokGetOembedMetadata(url: String, region: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get oEmbed metadata

Get cheap unauthenticated oEmbed metadata for a TikTok URL.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let url = "url_example" // String | Full TikTok video or profile URL
let region = "region_example" // String |  (optional) (default to "US")

// Get oEmbed metadata
TikTokAPI.tiktokGetOembedMetadata(url: url, region: region) { (response, error) in
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
 **url** | **String** | Full TikTok video or profile URL | 
 **region** | **String** |  | [optional] [default to &quot;US&quot;]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **tiktokGetRelatedVideos**
```swift
    open class func tiktokGetRelatedVideos(videoId: String, region: String? = nil, count: Int? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get related videos

Get TikTok's related videos for a given video.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let videoId = "videoId_example" // String | 
let region = "region_example" // String |  (optional) (default to "US")
let count = 987 // Int |  (optional) (default to 16)

// Get related videos
TikTokAPI.tiktokGetRelatedVideos(videoId: videoId, region: region, count: count) { (response, error) in
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
 **videoId** | **String** |  | 
 **region** | **String** |  | [optional] [default to &quot;US&quot;]
 **count** | **Int** |  | [optional] [default to 16]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **tiktokGetReposts**
```swift
    open class func tiktokGetReposts(username: String, region: String? = nil, count: Int? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get reposts

Get videos a TikTok user has reposted.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let username = "username_example" // String | 
let region = "region_example" // String |  (optional) (default to "US")
let count = 987 // Int |  (optional) (default to 30)

// Get reposts
TikTokAPI.tiktokGetReposts(username: username, region: region, count: count) { (response, error) in
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
 **username** | **String** |  | 
 **region** | **String** |  | [optional] [default to &quot;US&quot;]
 **count** | **Int** |  | [optional] [default to 30]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **tiktokGetTiktokAdDetail**
```swift
    open class func tiktokGetTiktokAdDetail(adId: String, region: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get TikTok ad detail

Get a single ad's advertiser, creatives, and targeting/impression breakdown.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let adId = "adId_example" // String | 
let region = "region_example" // String | EU region code (the Ad Library is EU-only) (optional) (default to "DE")

// Get TikTok ad detail
TikTokAPI.tiktokGetTiktokAdDetail(adId: adId, region: region) { (response, error) in
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
 **adId** | **String** |  | 
 **region** | **String** | EU region code (the Ad Library is EU-only) | [optional] [default to &quot;DE&quot;]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **tiktokGetTranscript**
```swift
    open class func tiktokGetTranscript(videoId: String, region: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get transcript

Get subtitle/caption tracks for a TikTok video.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let videoId = "videoId_example" // String | 
let region = "region_example" // String |  (optional) (default to "US")

// Get transcript
TikTokAPI.tiktokGetTranscript(videoId: videoId, region: region) { (response, error) in
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
 **videoId** | **String** |  | 
 **region** | **String** |  | [optional] [default to &quot;US&quot;]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **tiktokGetUserProfile**
```swift
    open class func tiktokGetUserProfile(username: String, region: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get user profile

Get a TikTok user's full profile.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let username = "username_example" // String | 
let region = "region_example" // String | Content region (ISO 3166-1 alpha-2) (optional) (default to "US")

// Get user profile
TikTokAPI.tiktokGetUserProfile(username: username, region: region) { (response, error) in
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
 **username** | **String** |  | 
 **region** | **String** | Content region (ISO 3166-1 alpha-2) | [optional] [default to &quot;US&quot;]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **tiktokGetUserVideos**
```swift
    open class func tiktokGetUserVideos(username: String, region: String? = nil, count: Int? = nil, cursor: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get user videos

Get a TikTok user's posted videos.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let username = "username_example" // String | 
let region = "region_example" // String |  (optional) (default to "US")
let count = 987 // Int |  (optional) (default to 30)
let cursor = "cursor_example" // String | Pagination cursor from a prior page's `pagination.cursor` (signer path only). (optional)

// Get user videos
TikTokAPI.tiktokGetUserVideos(username: username, region: region, count: count, cursor: cursor) { (response, error) in
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
 **username** | **String** |  | 
 **region** | **String** |  | [optional] [default to &quot;US&quot;]
 **count** | **Int** |  | [optional] [default to 30]
 **cursor** | **String** | Pagination cursor from a prior page&#39;s &#x60;pagination.cursor&#x60; (signer path only). | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **tiktokGetVideoDetail**
```swift
    open class func tiktokGetVideoDetail(videoId: String, region: String? = nil, username: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get video detail

Get full metadata for a single TikTok video/post.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let videoId = "videoId_example" // String | 
let region = "region_example" // String |  (optional) (default to "US")
let username = "username_example" // String | Author handle (skips oEmbed lookup) (optional)

// Get video detail
TikTokAPI.tiktokGetVideoDetail(videoId: videoId, region: region, username: username) { (response, error) in
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
 **videoId** | **String** |  | 
 **region** | **String** |  | [optional] [default to &quot;US&quot;]
 **username** | **String** | Author handle (skips oEmbed lookup) | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **tiktokHealthCheck**
```swift
    open class func tiktokHealthCheck(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Health check

Check health of the TikTok scraper service.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// Health check
TikTokAPI.tiktokHealthCheck() { (response, error) in
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

# **tiktokHealthCheckHead**
```swift
    open class func tiktokHealthCheckHead(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Health check

Check health of the TikTok scraper service.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// Health check
TikTokAPI.tiktokHealthCheckHead() { (response, error) in
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

# **tiktokListRegions**
```swift
    open class func tiktokListRegions(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

List regions

List supported TikTok content regions.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// List regions
TikTokAPI.tiktokListRegions() { (response, error) in
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

# **tiktokSearchHashtags**
```swift
    open class func tiktokSearchHashtags(query: String, region: String? = nil, count: Int? = nil, cursor: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Search hashtags

Search TikTok hashtags by keyword.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let query = "query_example" // String | Search keyword
let region = "region_example" // String |  (optional) (default to "US")
let count = 987 // Int |  (optional) (default to 20)
let cursor = "cursor_example" // String | Composite pagination cursor (offset.search_id) from a prior page's pagination.cursor (optional)

// Search hashtags
TikTokAPI.tiktokSearchHashtags(query: query, region: region, count: count, cursor: cursor) { (response, error) in
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
 **query** | **String** | Search keyword | 
 **region** | **String** |  | [optional] [default to &quot;US&quot;]
 **count** | **Int** |  | [optional] [default to 20]
 **cursor** | **String** | Composite pagination cursor (offset.search_id) from a prior page&#39;s pagination.cursor | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **tiktokSearchTheTiktokAdLibrary**
```swift
    open class func tiktokSearchTheTiktokAdLibrary(query: String? = nil, advertiserId: String? = nil, region: String? = nil, days: Int? = nil, sort: String? = nil, offset: Int? = nil, searchId: String? = nil, count: Int? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Search the TikTok Ad Library

Search TikTok's Commercial Content Library (ad transparency) by keyword or advertiser.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let query = "query_example" // String | Keyword (ignored when advertiser_id is set) (optional) (default to "")
let advertiserId = "advertiserId_example" // String | Advertiser business id(s) for advertiser search (optional) (default to "")
let region = "region_example" // String | EU region code (the Ad Library is EU-only) (optional) (default to "DE")
let days = 987 // Int |  (optional) (default to 30)
let sort = "sort_example" // String |  (optional) (default to "last_shown_date,desc")
let offset = 987 // Int |  (optional) (default to 0)
let searchId = "searchId_example" // String |  (optional) (default to "")
let count = 987 // Int |  (optional) (default to 20)

// Search the TikTok Ad Library
TikTokAPI.tiktokSearchTheTiktokAdLibrary(query: query, advertiserId: advertiserId, region: region, days: days, sort: sort, offset: offset, searchId: searchId, count: count) { (response, error) in
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
 **query** | **String** | Keyword (ignored when advertiser_id is set) | [optional] [default to &quot;&quot;]
 **advertiserId** | **String** | Advertiser business id(s) for advertiser search | [optional] [default to &quot;&quot;]
 **region** | **String** | EU region code (the Ad Library is EU-only) | [optional] [default to &quot;DE&quot;]
 **days** | **Int** |  | [optional] [default to 30]
 **sort** | **String** |  | [optional] [default to &quot;last_shown_date,desc&quot;]
 **offset** | **Int** |  | [optional] [default to 0]
 **searchId** | **String** |  | [optional] [default to &quot;&quot;]
 **count** | **Int** |  | [optional] [default to 20]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **tiktokSearchTiktokAdvertisers**
```swift
    open class func tiktokSearchTiktokAdvertisers(query: String, region: String? = nil, count: Int? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Search TikTok advertisers

Look up TikTok advertiser business ids by name (feeds ads/search?advertiser_id=).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let query = "query_example" // String | Advertiser name (or partial) to look up
let region = "region_example" // String | EU region code (the Ad Library is EU-only) (optional) (default to "DE")
let count = 987 // Int |  (optional) (default to 10)

// Search TikTok advertisers
TikTokAPI.tiktokSearchTiktokAdvertisers(query: query, region: region, count: count) { (response, error) in
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
 **query** | **String** | Advertiser name (or partial) to look up | 
 **region** | **String** | EU region code (the Ad Library is EU-only) | [optional] [default to &quot;DE&quot;]
 **count** | **Int** |  | [optional] [default to 10]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **tiktokSearchUsers**
```swift
    open class func tiktokSearchUsers(query: String, region: String? = nil, count: Int? = nil, cursor: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Search users

Search TikTok users by keyword.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let query = "query_example" // String | Search keyword
let region = "region_example" // String |  (optional) (default to "US")
let count = 987 // Int |  (optional) (default to 20)
let cursor = "cursor_example" // String | Composite pagination cursor (offset.search_id) from a prior page's pagination.cursor (optional)

// Search users
TikTokAPI.tiktokSearchUsers(query: query, region: region, count: count, cursor: cursor) { (response, error) in
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
 **query** | **String** | Search keyword | 
 **region** | **String** |  | [optional] [default to &quot;US&quot;]
 **count** | **Int** |  | [optional] [default to 20]
 **cursor** | **String** | Composite pagination cursor (offset.search_id) from a prior page&#39;s pagination.cursor | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **tiktokSearchVideos**
```swift
    open class func tiktokSearchVideos(query: String, region: String? = nil, count: Int? = nil, cursor: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Search videos

Search TikTok videos by keyword.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let query = "query_example" // String | Search keyword
let region = "region_example" // String |  (optional) (default to "US")
let count = 987 // Int |  (optional) (default to 20)
let cursor = "cursor_example" // String | Composite pagination cursor (offset.search_id) from a prior page's pagination.cursor (optional)

// Search videos
TikTokAPI.tiktokSearchVideos(query: query, region: region, count: count, cursor: cursor) { (response, error) in
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
 **query** | **String** | Search keyword | 
 **region** | **String** |  | [optional] [default to &quot;US&quot;]
 **count** | **Int** |  | [optional] [default to 20]
 **cursor** | **String** | Composite pagination cursor (offset.search_id) from a prior page&#39;s pagination.cursor | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **tiktokTrendingHashtags**
```swift
    open class func tiktokTrendingHashtags(region: String? = nil, period: Int? = nil, count: Int? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Trending hashtags

Get trending hashtags (mobile Discover surface — view_count + creators).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let region = "region_example" // String |  (optional) (default to "US")
let period = 987 // Int |  (optional) (default to 7)
let count = 987 // Int |  (optional) (default to 20)

// Trending hashtags
TikTokAPI.tiktokTrendingHashtags(region: region, period: period, count: count) { (response, error) in
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
 **region** | **String** |  | [optional] [default to &quot;US&quot;]
 **period** | **Int** |  | [optional] [default to 7]
 **count** | **Int** |  | [optional] [default to 20]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **tiktokTrendingSongs**
```swift
    open class func tiktokTrendingSongs(region: String? = nil, period: Int? = nil, count: Int? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Trending songs

Get trending songs/sounds (mobile hot-music feed — ranked by usage).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let region = "region_example" // String |  (optional) (default to "US")
let period = 987 // Int |  (optional) (default to 7)
let count = 987 // Int |  (optional) (default to 20)

// Trending songs
TikTokAPI.tiktokTrendingSongs(region: region, period: period, count: count) { (response, error) in
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
 **region** | **String** |  | [optional] [default to &quot;US&quot;]
 **period** | **Int** |  | [optional] [default to 7]
 **count** | **Int** |  | [optional] [default to 20]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **tiktokTrendingVideos**
```swift
    open class func tiktokTrendingVideos(region: String? = nil, count: Int? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Trending videos

Get trending videos from the TikTok Explore feed.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let region = "region_example" // String |  (optional) (default to "US")
let count = 987 // Int |  (optional) (default to 20)

// Trending videos
TikTokAPI.tiktokTrendingVideos(region: region, count: count) { (response, error) in
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
 **region** | **String** |  | [optional] [default to &quot;US&quot;]
 **count** | **Int** |  | [optional] [default to 20]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

