# YouTubeAPI

All URIs are relative to *https://scrapebadger.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**youtubeBatchVideoDetail**](YouTubeAPI.md#youtubebatchvideodetail) | **POST** /v1/youtube/videos/batch | Batch video detail
[**youtubeChannelAbout**](YouTubeAPI.md#youtubechannelabout) | **GET** /v1/youtube/channels/{channel_id}/about | Channel about
[**youtubeChannelPlaylists**](YouTubeAPI.md#youtubechannelplaylists) | **GET** /v1/youtube/channels/{channel_id}/playlists | Channel playlists
[**youtubeChannelShorts**](YouTubeAPI.md#youtubechannelshorts) | **GET** /v1/youtube/channels/{channel_id}/shorts | Channel shorts
[**youtubeChannelStreams**](YouTubeAPI.md#youtubechannelstreams) | **GET** /v1/youtube/channels/{channel_id}/streams | Channel streams
[**youtubeChannelVideos**](YouTubeAPI.md#youtubechannelvideos) | **GET** /v1/youtube/channels/{channel_id}/videos | Channel videos
[**youtubeCommentReplies**](YouTubeAPI.md#youtubecommentreplies) | **GET** /v1/youtube/videos/{video_id}/comments/{comment_id}/replies | Comment replies
[**youtubeCommunityPostComments**](YouTubeAPI.md#youtubecommunitypostcomments) | **GET** /v1/youtube/posts/{post_id}/comments | Community post comments
[**youtubeCommunityPosts**](YouTubeAPI.md#youtubecommunityposts) | **GET** /v1/youtube/channels/{channel_id}/community | Community posts
[**youtubeContentRegions**](YouTubeAPI.md#youtubecontentregions) | **GET** /v1/youtube/regions | Content regions
[**youtubeGetACommunityPost**](YouTubeAPI.md#youtubegetacommunitypost) | **GET** /v1/youtube/posts/{post_id} | Get a community post
[**youtubeGetAMixRadioQueue**](YouTubeAPI.md#youtubegetamixradioqueue) | **GET** /v1/youtube/mixes/{playlist_id} | Get a mix / radio queue
[**youtubeGetAShort**](YouTubeAPI.md#youtubegetashort) | **GET** /v1/youtube/shorts/{video_id} | Get a Short
[**youtubeGetChannelDetail**](YouTubeAPI.md#youtubegetchanneldetail) | **GET** /v1/youtube/channels/{channel_id} | Get channel detail
[**youtubeGetPlaylistDetail**](YouTubeAPI.md#youtubegetplaylistdetail) | **GET** /v1/youtube/playlists/{playlist_id} | Get playlist detail
[**youtubeGetVideoDetail**](YouTubeAPI.md#youtubegetvideodetail) | **GET** /v1/youtube/videos/{video_id} | Get video detail
[**youtubeGuestHomeFeed**](YouTubeAPI.md#youtubeguesthomefeed) | **GET** /v1/youtube/home | Guest home feed
[**youtubeKeywordSuggestions**](YouTubeAPI.md#youtubekeywordsuggestions) | **GET** /v1/youtube/autocomplete | Keyword suggestions
[**youtubeListCaptionTracks**](YouTubeAPI.md#youtubelistcaptiontracks) | **GET** /v1/youtube/videos/{video_id}/captions | List caption tracks
[**youtubeLiveChatMessages**](YouTubeAPI.md#youtubelivechatmessages) | **GET** /v1/youtube/videos/{video_id}/live_chat | Live chat messages
[**youtubeOembedMetadata**](YouTubeAPI.md#youtubeoembedmetadata) | **GET** /v1/youtube/oembed | oEmbed metadata
[**youtubePlaylistItemsPage**](YouTubeAPI.md#youtubeplaylistitemspage) | **GET** /v1/youtube/playlists/{playlist_id}/items | Playlist items page
[**youtubeRelatedVideos**](YouTubeAPI.md#youtuberelatedvideos) | **GET** /v1/youtube/videos/{video_id}/related | Related videos
[**youtubeResolveHandleUrlToId**](YouTubeAPI.md#youtuberesolvehandleurltoid) | **GET** /v1/youtube/channels/resolve | Resolve handle/URL to id
[**youtubeSearchWithinAChannel**](YouTubeAPI.md#youtubesearchwithinachannel) | **GET** /v1/youtube/channels/{channel_id}/search | Search within a channel
[**youtubeSearchYoutube**](YouTubeAPI.md#youtubesearchyoutube) | **GET** /v1/youtube/search | Search YouTube
[**youtubeSearchYoutubeMusic**](YouTubeAPI.md#youtubesearchyoutubemusic) | **GET** /v1/youtube/music/search | Search YouTube Music
[**youtubeShortsBySound**](YouTubeAPI.md#youtubeshortsbysound) | **GET** /v1/youtube/shorts/by_sound/{sound_id} | Shorts by sound
[**youtubeStreamFormats**](YouTubeAPI.md#youtubestreamformats) | **GET** /v1/youtube/videos/{video_id}/streams | Stream formats
[**youtubeSubscriberCountFast**](YouTubeAPI.md#youtubesubscribercountfast) | **GET** /v1/youtube/channels/{channel_id}/subscriber_count | Subscriber count (fast)
[**youtubeSupportedMarkets**](YouTubeAPI.md#youtubesupportedmarkets) | **GET** /v1/youtube/markets | Supported markets
[**youtubeTrendingShorts**](YouTubeAPI.md#youtubetrendingshorts) | **GET** /v1/youtube/trending/shorts | Trending shorts
[**youtubeTrendingVideos**](YouTubeAPI.md#youtubetrendingvideos) | **GET** /v1/youtube/trending | Trending videos
[**youtubeUiLanguages**](YouTubeAPI.md#youtubeuilanguages) | **GET** /v1/youtube/languages | UI languages
[**youtubeVideoCategories**](YouTubeAPI.md#youtubevideocategories) | **GET** /v1/youtube/categories | Video categories
[**youtubeVideoComments**](YouTubeAPI.md#youtubevideocomments) | **GET** /v1/youtube/videos/{video_id}/comments | Video comments
[**youtubeVideoTranscript**](YouTubeAPI.md#youtubevideotranscript) | **GET** /v1/youtube/videos/{video_id}/transcript | Video transcript
[**youtubeVideosUnderAHashtag**](YouTubeAPI.md#youtubevideosunderahashtag) | **GET** /v1/youtube/hashtags/{tag} | Videos under a hashtag
[**youtubeYoutubeScraperHealthCheck**](YouTubeAPI.md#youtubeyoutubescraperhealthcheck) | **GET** /v1/youtube/health | YouTube scraper health check
[**youtubeYoutubeScraperHealthCheckHead**](YouTubeAPI.md#youtubeyoutubescraperhealthcheckhead) | **HEAD** /v1/youtube/health | YouTube scraper health check


# **youtubeBatchVideoDetail**
```swift
    open class func youtubeBatchVideoDetail(requestBody: [String: AnyCodable], completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Batch video detail

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let requestBody = "TODO" // [String: AnyCodable] | 

// Batch video detail
YouTubeAPI.youtubeBatchVideoDetail(requestBody: requestBody) { (response, error) in
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
 **requestBody** | [**[String: AnyCodable]**](AnyCodable.md) |  | 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **youtubeChannelAbout**
```swift
    open class func youtubeChannelAbout(channelId: String, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Channel about

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let channelId = "channelId_example" // String | 

// Channel about
YouTubeAPI.youtubeChannelAbout(channelId: channelId) { (response, error) in
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
 **channelId** | **String** |  | 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **youtubeChannelPlaylists**
```swift
    open class func youtubeChannelPlaylists(channelId: String, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Channel playlists

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let channelId = "channelId_example" // String | 

// Channel playlists
YouTubeAPI.youtubeChannelPlaylists(channelId: channelId) { (response, error) in
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
 **channelId** | **String** |  | 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **youtubeChannelShorts**
```swift
    open class func youtubeChannelShorts(channelId: String, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Channel shorts

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let channelId = "channelId_example" // String | 

// Channel shorts
YouTubeAPI.youtubeChannelShorts(channelId: channelId) { (response, error) in
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
 **channelId** | **String** |  | 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **youtubeChannelStreams**
```swift
    open class func youtubeChannelStreams(channelId: String, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Channel streams

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let channelId = "channelId_example" // String | 

// Channel streams
YouTubeAPI.youtubeChannelStreams(channelId: channelId) { (response, error) in
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
 **channelId** | **String** |  | 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **youtubeChannelVideos**
```swift
    open class func youtubeChannelVideos(channelId: String, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Channel videos

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let channelId = "channelId_example" // String | 

// Channel videos
YouTubeAPI.youtubeChannelVideos(channelId: channelId) { (response, error) in
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
 **channelId** | **String** |  | 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **youtubeCommentReplies**
```swift
    open class func youtubeCommentReplies(videoId: String, commentId: String, continuation: String, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Comment replies

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let videoId = "videoId_example" // String | 
let commentId = "commentId_example" // String | 
let continuation = "continuation_example" // String | Replies continuation token

// Comment replies
YouTubeAPI.youtubeCommentReplies(videoId: videoId, commentId: commentId, continuation: continuation) { (response, error) in
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
 **commentId** | **String** |  | 
 **continuation** | **String** | Replies continuation token | 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **youtubeCommunityPostComments**
```swift
    open class func youtubeCommunityPostComments(postId: String, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Community post comments

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let postId = "postId_example" // String | 

// Community post comments
YouTubeAPI.youtubeCommunityPostComments(postId: postId) { (response, error) in
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
 **postId** | **String** |  | 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **youtubeCommunityPosts**
```swift
    open class func youtubeCommunityPosts(channelId: String, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Community posts

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let channelId = "channelId_example" // String | 

// Community posts
YouTubeAPI.youtubeCommunityPosts(channelId: channelId) { (response, error) in
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
 **channelId** | **String** |  | 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **youtubeContentRegions**
```swift
    open class func youtubeContentRegions(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Content regions

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// Content regions
YouTubeAPI.youtubeContentRegions() { (response, error) in
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

# **youtubeGetACommunityPost**
```swift
    open class func youtubeGetACommunityPost(postId: String, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get a community post

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let postId = "postId_example" // String | 

// Get a community post
YouTubeAPI.youtubeGetACommunityPost(postId: postId) { (response, error) in
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
 **postId** | **String** |  | 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **youtubeGetAMixRadioQueue**
```swift
    open class func youtubeGetAMixRadioQueue(playlistId: String, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get a mix / radio queue

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let playlistId = "playlistId_example" // String | 

// Get a mix / radio queue
YouTubeAPI.youtubeGetAMixRadioQueue(playlistId: playlistId) { (response, error) in
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
 **playlistId** | **String** |  | 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **youtubeGetAShort**
```swift
    open class func youtubeGetAShort(videoId: String, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get a Short

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let videoId = "videoId_example" // String | 

// Get a Short
YouTubeAPI.youtubeGetAShort(videoId: videoId) { (response, error) in
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

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **youtubeGetChannelDetail**
```swift
    open class func youtubeGetChannelDetail(channelId: String, gl: String? = nil, hl: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get channel detail

Channel detail (accepts a UC id, @handle, or custom URL).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let channelId = "channelId_example" // String | 
let gl = "gl_example" // String |  (optional)
let hl = "hl_example" // String |  (optional)

// Get channel detail
YouTubeAPI.youtubeGetChannelDetail(channelId: channelId, gl: gl, hl: hl) { (response, error) in
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
 **channelId** | **String** |  | 
 **gl** | **String** |  | [optional] 
 **hl** | **String** |  | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **youtubeGetPlaylistDetail**
```swift
    open class func youtubeGetPlaylistDetail(playlistId: String, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get playlist detail

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let playlistId = "playlistId_example" // String | 

// Get playlist detail
YouTubeAPI.youtubeGetPlaylistDetail(playlistId: playlistId) { (response, error) in
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
 **playlistId** | **String** |  | 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **youtubeGetVideoDetail**
```swift
    open class func youtubeGetVideoDetail(videoId: String, gl: String? = nil, hl: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get video detail

Full video detail — merged player + next (likes, comments, chapters, related).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let videoId = "videoId_example" // String | 
let gl = "gl_example" // String |  (optional)
let hl = "hl_example" // String |  (optional)

// Get video detail
YouTubeAPI.youtubeGetVideoDetail(videoId: videoId, gl: gl, hl: hl) { (response, error) in
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
 **gl** | **String** |  | [optional] 
 **hl** | **String** |  | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **youtubeGuestHomeFeed**
```swift
    open class func youtubeGuestHomeFeed(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Guest home feed

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// Guest home feed
YouTubeAPI.youtubeGuestHomeFeed() { (response, error) in
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

# **youtubeKeywordSuggestions**
```swift
    open class func youtubeKeywordSuggestions(query: String, gl: String? = nil, hl: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Keyword suggestions

Return YouTube keyword autocomplete suggestions.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let query = "query_example" // String | Partial query prefix
let gl = "gl_example" // String |  (optional)
let hl = "hl_example" // String |  (optional)

// Keyword suggestions
YouTubeAPI.youtubeKeywordSuggestions(query: query, gl: gl, hl: hl) { (response, error) in
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
 **query** | **String** | Partial query prefix | 
 **gl** | **String** |  | [optional] 
 **hl** | **String** |  | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **youtubeListCaptionTracks**
```swift
    open class func youtubeListCaptionTracks(videoId: String, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

List caption tracks

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let videoId = "videoId_example" // String | 

// List caption tracks
YouTubeAPI.youtubeListCaptionTracks(videoId: videoId) { (response, error) in
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

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **youtubeLiveChatMessages**
```swift
    open class func youtubeLiveChatMessages(videoId: String, continuation: String? = nil, replay: Bool? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Live chat messages

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let videoId = "videoId_example" // String | 
let continuation = "continuation_example" // String |  (optional)
let replay = true // Bool |  (optional) (default to false)

// Live chat messages
YouTubeAPI.youtubeLiveChatMessages(videoId: videoId, continuation: continuation, replay: replay) { (response, error) in
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
 **continuation** | **String** |  | [optional] 
 **replay** | **Bool** |  | [optional] [default to false]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **youtubeOembedMetadata**
```swift
    open class func youtubeOembedMetadata(url: String, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

oEmbed metadata

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let url = "url_example" // String | A YouTube URL

// oEmbed metadata
YouTubeAPI.youtubeOembedMetadata(url: url) { (response, error) in
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
 **url** | **String** | A YouTube URL | 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **youtubePlaylistItemsPage**
```swift
    open class func youtubePlaylistItemsPage(playlistId: String, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Playlist items page

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let playlistId = "playlistId_example" // String | 

// Playlist items page
YouTubeAPI.youtubePlaylistItemsPage(playlistId: playlistId) { (response, error) in
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
 **playlistId** | **String** |  | 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **youtubeRelatedVideos**
```swift
    open class func youtubeRelatedVideos(videoId: String, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Related videos

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let videoId = "videoId_example" // String | 

// Related videos
YouTubeAPI.youtubeRelatedVideos(videoId: videoId) { (response, error) in
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

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **youtubeResolveHandleUrlToId**
```swift
    open class func youtubeResolveHandleUrlToId(handle: String? = nil, url: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Resolve handle/URL to id

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let handle = "handle_example" // String |  (optional)
let url = "url_example" // String |  (optional)

// Resolve handle/URL to id
YouTubeAPI.youtubeResolveHandleUrlToId(handle: handle, url: url) { (response, error) in
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
 **handle** | **String** |  | [optional] 
 **url** | **String** |  | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **youtubeSearchWithinAChannel**
```swift
    open class func youtubeSearchWithinAChannel(channelId: String, query: String, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Search within a channel

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let channelId = "channelId_example" // String | 
let query = "query_example" // String | Search keywords

// Search within a channel
YouTubeAPI.youtubeSearchWithinAChannel(channelId: channelId, query: query) { (response, error) in
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
 **channelId** | **String** |  | 
 **query** | **String** | Search keywords | 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **youtubeSearchYoutube**
```swift
    open class func youtubeSearchYoutube(query: String, type: String? = nil, sortBy: String? = nil, uploadDate: String? = nil, duration: String? = nil, features: String? = nil, gl: String? = nil, hl: String? = nil, continuation: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Search YouTube

Search videos / channels / playlists with the full filter matrix.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let query = "query_example" // String | Search keywords
let type = "type_example" // String | video|channel|playlist|movie|all (optional)
let sortBy = "sortBy_example" // String | relevance|date|views|rating (optional)
let uploadDate = "uploadDate_example" // String | hour|today|week|month|year (optional)
let duration = "duration_example" // String | short|medium|long (optional)
let features = "features_example" // String | hd,4k,360,vr180,3d,hdr,cc,subtitles,live (optional)
let gl = "gl_example" // String | Content region (US, GB, DE…) (optional)
let hl = "hl_example" // String | UI language (optional)
let continuation = "continuation_example" // String |  (optional)

// Search YouTube
YouTubeAPI.youtubeSearchYoutube(query: query, type: type, sortBy: sortBy, uploadDate: uploadDate, duration: duration, features: features, gl: gl, hl: hl, continuation: continuation) { (response, error) in
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
 **query** | **String** | Search keywords | 
 **type** | **String** | video|channel|playlist|movie|all | [optional] 
 **sortBy** | **String** | relevance|date|views|rating | [optional] 
 **uploadDate** | **String** | hour|today|week|month|year | [optional] 
 **duration** | **String** | short|medium|long | [optional] 
 **features** | **String** | hd,4k,360,vr180,3d,hdr,cc,subtitles,live | [optional] 
 **gl** | **String** | Content region (US, GB, DE…) | [optional] 
 **hl** | **String** | UI language | [optional] 
 **continuation** | **String** |  | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **youtubeSearchYoutubeMusic**
```swift
    open class func youtubeSearchYoutubeMusic(query: String, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Search YouTube Music

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let query = "query_example" // String | Search keywords

// Search YouTube Music
YouTubeAPI.youtubeSearchYoutubeMusic(query: query) { (response, error) in
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
 **query** | **String** | Search keywords | 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **youtubeShortsBySound**
```swift
    open class func youtubeShortsBySound(soundId: String, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Shorts by sound

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let soundId = "soundId_example" // String | 

// Shorts by sound
YouTubeAPI.youtubeShortsBySound(soundId: soundId) { (response, error) in
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
 **soundId** | **String** |  | 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **youtubeStreamFormats**
```swift
    open class func youtubeStreamFormats(videoId: String, client: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Stream formats

Stream/format metadata (best-effort; media URLs may be PO-token gated).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let videoId = "videoId_example" // String | 
let client = "client_example" // String | IOS|ANDROID|WEB (optional) (default to "IOS")

// Stream formats
YouTubeAPI.youtubeStreamFormats(videoId: videoId, client: client) { (response, error) in
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
 **client** | **String** | IOS|ANDROID|WEB | [optional] [default to &quot;IOS&quot;]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **youtubeSubscriberCountFast**
```swift
    open class func youtubeSubscriberCountFast(channelId: String, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Subscriber count (fast)

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let channelId = "channelId_example" // String | 

// Subscriber count (fast)
YouTubeAPI.youtubeSubscriberCountFast(channelId: channelId) { (response, error) in
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
 **channelId** | **String** |  | 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **youtubeSupportedMarkets**
```swift
    open class func youtubeSupportedMarkets(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Supported markets

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// Supported markets
YouTubeAPI.youtubeSupportedMarkets() { (response, error) in
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

# **youtubeTrendingShorts**
```swift
    open class func youtubeTrendingShorts(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Trending shorts

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// Trending shorts
YouTubeAPI.youtubeTrendingShorts() { (response, error) in
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

# **youtubeTrendingVideos**
```swift
    open class func youtubeTrendingVideos(gl: String? = nil, type: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Trending videos

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let gl = "gl_example" // String |  (optional)
let type = "type_example" // String | now|music|gaming|movies (optional) (default to "now")

// Trending videos
YouTubeAPI.youtubeTrendingVideos(gl: gl, type: type) { (response, error) in
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
 **gl** | **String** |  | [optional] 
 **type** | **String** | now|music|gaming|movies | [optional] [default to &quot;now&quot;]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **youtubeUiLanguages**
```swift
    open class func youtubeUiLanguages(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

UI languages

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// UI languages
YouTubeAPI.youtubeUiLanguages() { (response, error) in
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

# **youtubeVideoCategories**
```swift
    open class func youtubeVideoCategories(gl: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Video categories

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let gl = "gl_example" // String |  (optional) (default to "US")

// Video categories
YouTubeAPI.youtubeVideoCategories(gl: gl) { (response, error) in
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
 **gl** | **String** |  | [optional] [default to &quot;US&quot;]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **youtubeVideoComments**
```swift
    open class func youtubeVideoComments(videoId: String, sortBy: String? = nil, continuation: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Video comments

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let videoId = "videoId_example" // String | 
let sortBy = "sortBy_example" // String | top|newest (optional) (default to "top")
let continuation = "continuation_example" // String |  (optional)

// Video comments
YouTubeAPI.youtubeVideoComments(videoId: videoId, sortBy: sortBy, continuation: continuation) { (response, error) in
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
 **sortBy** | **String** | top|newest | [optional] [default to &quot;top&quot;]
 **continuation** | **String** |  | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **youtubeVideoTranscript**
```swift
    open class func youtubeVideoTranscript(videoId: String, language: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Video transcript

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let videoId = "videoId_example" // String | 
let language = "language_example" // String | BCP-47 language code (optional)

// Video transcript
YouTubeAPI.youtubeVideoTranscript(videoId: videoId, language: language) { (response, error) in
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
 **language** | **String** | BCP-47 language code | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **youtubeVideosUnderAHashtag**
```swift
    open class func youtubeVideosUnderAHashtag(tag: String, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Videos under a hashtag

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let tag = "tag_example" // String | 

// Videos under a hashtag
YouTubeAPI.youtubeVideosUnderAHashtag(tag: tag) { (response, error) in
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
 **tag** | **String** |  | 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **youtubeYoutubeScraperHealthCheck**
```swift
    open class func youtubeYoutubeScraperHealthCheck(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

YouTube scraper health check

Check health of the YouTube scraper service (accepts HEAD for UptimeRobot).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// YouTube scraper health check
YouTubeAPI.youtubeYoutubeScraperHealthCheck() { (response, error) in
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

# **youtubeYoutubeScraperHealthCheckHead**
```swift
    open class func youtubeYoutubeScraperHealthCheckHead(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

YouTube scraper health check

Check health of the YouTube scraper service (accepts HEAD for UptimeRobot).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// YouTube scraper health check
YouTubeAPI.youtubeYoutubeScraperHealthCheckHead() { (response, error) in
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

