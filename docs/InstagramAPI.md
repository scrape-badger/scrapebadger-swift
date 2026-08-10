# InstagramAPI

All URIs are relative to *https://scrapebadger.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**instagramAboutThisAccount**](InstagramAPI.md#instagramaboutthisaccount) | **GET** /v1/instagram/users/{username}/about | About this account
[**instagramBlendedTopSearch**](InstagramAPI.md#instagramblendedtopsearch) | **GET** /v1/instagram/search/top | Blended top search
[**instagramGetActiveStories**](InstagramAPI.md#instagramgetactivestories) | **GET** /v1/instagram/users/{username}/stories | Get active stories
[**instagramGetAudioTrack**](InstagramAPI.md#instagramgetaudiotrack) | **GET** /v1/instagram/audio/{audio_id} | Get audio track
[**instagramGetComments**](InstagramAPI.md#instagramgetcomments) | **GET** /v1/instagram/media/{code}/comments | Get comments
[**instagramGetFollowers**](InstagramAPI.md#instagramgetfollowers) | **GET** /v1/instagram/users/{username}/followers | Get followers
[**instagramGetFollowing**](InstagramAPI.md#instagramgetfollowing) | **GET** /v1/instagram/users/{username}/following | Get following
[**instagramGetHashtagInfo**](InstagramAPI.md#instagramgethashtaginfo) | **GET** /v1/instagram/hashtags/{tag} | Get hashtag info
[**instagramGetHighlights**](InstagramAPI.md#instagramgethighlights) | **GET** /v1/instagram/users/{username}/highlights | Get highlights
[**instagramGetLikers**](InstagramAPI.md#instagramgetlikers) | **GET** /v1/instagram/media/{code}/likers | Get likers
[**instagramGetLocation**](InstagramAPI.md#instagramgetlocation) | **GET** /v1/instagram/locations/{location_pk} | Get location
[**instagramGetPostReelDetail**](InstagramAPI.md#instagramgetpostreeldetail) | **GET** /v1/instagram/media/{code} | Get post/reel detail
[**instagramGetProfile**](InstagramAPI.md#instagramgetprofile) | **GET** /v1/instagram/users/{username} | Get profile
[**instagramGetTaggedPosts**](InstagramAPI.md#instagramgettaggedposts) | **GET** /v1/instagram/users/{username}/tagged | Get tagged posts
[**instagramGetUserPosts**](InstagramAPI.md#instagramgetuserposts) | **GET** /v1/instagram/users/{username}/posts | Get user posts
[**instagramGetUserReels**](InstagramAPI.md#instagramgetuserreels) | **GET** /v1/instagram/users/{username}/reels | Get user reels
[**instagramHealth**](InstagramAPI.md#instagramhealth) | **GET** /v1/instagram/health | Health
[**instagramHealthHead**](InstagramAPI.md#instagramhealthhead) | **HEAD** /v1/instagram/health | Health
[**instagramRecentHashtagPosts**](InstagramAPI.md#instagramrecenthashtagposts) | **GET** /v1/instagram/hashtags/{tag}/recent | Recent hashtag posts
[**instagramRelatedProfiles**](InstagramAPI.md#instagramrelatedprofiles) | **GET** /v1/instagram/users/{username}/related | Related profiles
[**instagramSearchHashtags**](InstagramAPI.md#instagramsearchhashtags) | **GET** /v1/instagram/search/hashtags | Search hashtags
[**instagramSearchUsers**](InstagramAPI.md#instagramsearchusers) | **GET** /v1/instagram/search/users | Search users
[**instagramTopHashtagPosts**](InstagramAPI.md#instagramtophashtagposts) | **GET** /v1/instagram/hashtags/{tag}/top | Top hashtag posts


# **instagramAboutThisAccount**
```swift
    open class func instagramAboutThisAccount(username: String, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

About this account

Country, join date and former usernames.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let username = "username_example" // String | 

// About this account
InstagramAPI.instagramAboutThisAccount(username: username) { (response, error) in
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

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **instagramBlendedTopSearch**
```swift
    open class func instagramBlendedTopSearch(query: String, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Blended top search

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let query = "query_example" // String | 

// Blended top search
InstagramAPI.instagramBlendedTopSearch(query: query) { (response, error) in
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
 **query** | **String** |  | 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **instagramGetActiveStories**
```swift
    open class func instagramGetActiveStories(username: String, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get active stories

Active stories (account pool only).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let username = "username_example" // String | 

// Get active stories
InstagramAPI.instagramGetActiveStories(username: username) { (response, error) in
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

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **instagramGetAudioTrack**
```swift
    open class func instagramGetAudioTrack(audioId: String, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get audio track

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let audioId = "audioId_example" // String | 

// Get audio track
InstagramAPI.instagramGetAudioTrack(audioId: audioId) { (response, error) in
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
 **audioId** | **String** |  | 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **instagramGetComments**
```swift
    open class func instagramGetComments(code: String, amount: Int? = nil, cursor: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get comments

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let code = "code_example" // String | 
let amount = 987 // Int |  (optional) (default to 20)
let cursor = "cursor_example" // String |  (optional)

// Get comments
InstagramAPI.instagramGetComments(code: code, amount: amount, cursor: cursor) { (response, error) in
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
 **code** | **String** |  | 
 **amount** | **Int** |  | [optional] [default to 20]
 **cursor** | **String** |  | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **instagramGetFollowers**
```swift
    open class func instagramGetFollowers(username: String, amount: Int? = nil, cursor: String? = nil, order: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get followers

Followers list, paginated (account pool).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let username = "username_example" // String | 
let amount = 987 // Int |  (optional) (default to 50)
let cursor = "cursor_example" // String |  (optional)
let order = "order_example" // String | date_followed_latest | date_followed_earliest (optional)

// Get followers
InstagramAPI.instagramGetFollowers(username: username, amount: amount, cursor: cursor, order: order) { (response, error) in
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
 **amount** | **Int** |  | [optional] [default to 50]
 **cursor** | **String** |  | [optional] 
 **order** | **String** | date_followed_latest | date_followed_earliest | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **instagramGetFollowing**
```swift
    open class func instagramGetFollowing(username: String, amount: Int? = nil, cursor: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get following

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let username = "username_example" // String | 
let amount = 987 // Int |  (optional) (default to 50)
let cursor = "cursor_example" // String |  (optional)

// Get following
InstagramAPI.instagramGetFollowing(username: username, amount: amount, cursor: cursor) { (response, error) in
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
 **amount** | **Int** |  | [optional] [default to 50]
 **cursor** | **String** |  | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **instagramGetHashtagInfo**
```swift
    open class func instagramGetHashtagInfo(tag: String, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get hashtag info

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let tag = "tag_example" // String | 

// Get hashtag info
InstagramAPI.instagramGetHashtagInfo(tag: tag) { (response, error) in
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

# **instagramGetHighlights**
```swift
    open class func instagramGetHighlights(username: String, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get highlights

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let username = "username_example" // String | 

// Get highlights
InstagramAPI.instagramGetHighlights(username: username) { (response, error) in
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

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **instagramGetLikers**
```swift
    open class func instagramGetLikers(code: String, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get likers

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let code = "code_example" // String | 

// Get likers
InstagramAPI.instagramGetLikers(code: code) { (response, error) in
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
 **code** | **String** |  | 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **instagramGetLocation**
```swift
    open class func instagramGetLocation(locationPk: Int, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get location

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let locationPk = 987 // Int | 

// Get location
InstagramAPI.instagramGetLocation(locationPk: locationPk) { (response, error) in
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
 **locationPk** | **Int** |  | 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **instagramGetPostReelDetail**
```swift
    open class func instagramGetPostReelDetail(code: String, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get post/reel detail

Single post or reel: caption, media, counts, tags, location, carousel.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let code = "code_example" // String | 

// Get post/reel detail
InstagramAPI.instagramGetPostReelDetail(code: code) { (response, error) in
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
 **code** | **String** |  | 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **instagramGetProfile**
```swift
    open class func instagramGetProfile(username: String, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get profile

Full public profile: bio, counts, verification, business contact, links.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let username = "username_example" // String | 

// Get profile
InstagramAPI.instagramGetProfile(username: username) { (response, error) in
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

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **instagramGetTaggedPosts**
```swift
    open class func instagramGetTaggedPosts(username: String, amount: Int? = nil, cursor: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get tagged posts

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let username = "username_example" // String | 
let amount = 987 // Int |  (optional) (default to 20)
let cursor = "cursor_example" // String |  (optional)

// Get tagged posts
InstagramAPI.instagramGetTaggedPosts(username: username, amount: amount, cursor: cursor) { (response, error) in
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
 **amount** | **Int** |  | [optional] [default to 20]
 **cursor** | **String** |  | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **instagramGetUserPosts**
```swift
    open class func instagramGetUserPosts(username: String, amount: Int? = nil, cursor: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get user posts

Timeline posts, paginated.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let username = "username_example" // String | 
let amount = 987 // Int |  (optional) (default to 20)
let cursor = "cursor_example" // String |  (optional)

// Get user posts
InstagramAPI.instagramGetUserPosts(username: username, amount: amount, cursor: cursor) { (response, error) in
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
 **amount** | **Int** |  | [optional] [default to 20]
 **cursor** | **String** |  | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **instagramGetUserReels**
```swift
    open class func instagramGetUserReels(username: String, amount: Int? = nil, cursor: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get user reels

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let username = "username_example" // String | 
let amount = 987 // Int |  (optional) (default to 20)
let cursor = "cursor_example" // String |  (optional)

// Get user reels
InstagramAPI.instagramGetUserReels(username: username, amount: amount, cursor: cursor) { (response, error) in
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
 **amount** | **Int** |  | [optional] [default to 20]
 **cursor** | **String** |  | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **instagramHealth**
```swift
    open class func instagramHealth(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Health

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// Health
InstagramAPI.instagramHealth() { (response, error) in
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

# **instagramHealthHead**
```swift
    open class func instagramHealthHead(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Health

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// Health
InstagramAPI.instagramHealthHead() { (response, error) in
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

# **instagramRecentHashtagPosts**
```swift
    open class func instagramRecentHashtagPosts(tag: String, amount: Int? = nil, cursor: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Recent hashtag posts

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let tag = "tag_example" // String | 
let amount = 987 // Int |  (optional) (default to 20)
let cursor = "cursor_example" // String |  (optional)

// Recent hashtag posts
InstagramAPI.instagramRecentHashtagPosts(tag: tag, amount: amount, cursor: cursor) { (response, error) in
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
 **amount** | **Int** |  | [optional] [default to 20]
 **cursor** | **String** |  | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **instagramRelatedProfiles**
```swift
    open class func instagramRelatedProfiles(username: String, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Related profiles

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let username = "username_example" // String | 

// Related profiles
InstagramAPI.instagramRelatedProfiles(username: username) { (response, error) in
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

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **instagramSearchHashtags**
```swift
    open class func instagramSearchHashtags(query: String, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Search hashtags

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let query = "query_example" // String | 

// Search hashtags
InstagramAPI.instagramSearchHashtags(query: query) { (response, error) in
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
 **query** | **String** |  | 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **instagramSearchUsers**
```swift
    open class func instagramSearchUsers(query: String, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Search users

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let query = "query_example" // String | 

// Search users
InstagramAPI.instagramSearchUsers(query: query) { (response, error) in
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
 **query** | **String** |  | 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **instagramTopHashtagPosts**
```swift
    open class func instagramTopHashtagPosts(tag: String, amount: Int? = nil, cursor: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Top hashtag posts

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let tag = "tag_example" // String | 
let amount = 987 // Int |  (optional) (default to 20)
let cursor = "cursor_example" // String |  (optional)

// Top hashtag posts
InstagramAPI.instagramTopHashtagPosts(tag: tag, amount: amount, cursor: cursor) { (response, error) in
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
 **amount** | **Int** |  | [optional] [default to 20]
 **cursor** | **String** |  | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

