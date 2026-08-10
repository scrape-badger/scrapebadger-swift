# RedditAPI

All URIs are relative to *https://scrapebadger.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**redditGetCrossPosts**](RedditAPI.md#redditgetcrossposts) | **GET** /v1/reddit/posts/{post_id}/duplicates | Get cross-posts
[**redditGetPostComments**](RedditAPI.md#redditgetpostcomments) | **GET** /v1/reddit/posts/{post_id}/comments | Get post comments
[**redditGetPostDetail**](RedditAPI.md#redditgetpostdetail) | **GET** /v1/reddit/posts/{post_id} | Get post detail
[**redditGetPostsByDomain**](RedditAPI.md#redditgetpostsbydomain) | **GET** /v1/reddit/domains/{domain}/posts | Get posts by domain
[**redditGetSubredditInfo**](RedditAPI.md#redditgetsubredditinfo) | **GET** /v1/reddit/subreddits/{subreddit} | Get subreddit info
[**redditGetSubredditPosts**](RedditAPI.md#redditgetsubredditposts) | **GET** /v1/reddit/subreddits/{subreddit}/posts | Get subreddit posts
[**redditGetSubredditRules**](RedditAPI.md#redditgetsubredditrules) | **GET** /v1/reddit/subreddits/{subreddit}/rules | Get subreddit rules
[**redditGetTrendingPosts**](RedditAPI.md#redditgettrendingposts) | **GET** /v1/reddit/posts/trending | Get trending posts
[**redditGetUserProfile**](RedditAPI.md#redditgetuserprofile) | **GET** /v1/reddit/users/{username} | Get user profile
[**redditGetUserSComments**](RedditAPI.md#redditgetuserscomments) | **GET** /v1/reddit/users/{username}/comments | Get user&#39;s comments
[**redditGetUserSModeratedSubreddits**](RedditAPI.md#redditgetusersmoderatedsubreddits) | **GET** /v1/reddit/users/{username}/moderated | Get user&#39;s moderated subreddits
[**redditGetUserSPosts**](RedditAPI.md#redditgetusersposts) | **GET** /v1/reddit/users/{username}/posts | Get user&#39;s posts
[**redditGetUserSTrophies**](RedditAPI.md#redditgetuserstrophies) | **GET** /v1/reddit/users/{username}/trophies | Get user&#39;s trophies
[**redditGetWikiPageContent**](RedditAPI.md#redditgetwikipagecontent) | **GET** /v1/reddit/subreddits/{subreddit}/wiki/{page} | Get wiki page content
[**redditListWikiPages**](RedditAPI.md#redditlistwikipages) | **GET** /v1/reddit/subreddits/{subreddit}/wiki | List wiki pages
[**redditNewSubreddits**](RedditAPI.md#redditnewsubreddits) | **GET** /v1/reddit/subreddits/new | New subreddits
[**redditPopularSubreddits**](RedditAPI.md#redditpopularsubreddits) | **GET** /v1/reddit/subreddits/popular | Popular subreddits
[**redditRedditScraperHealthCheck**](RedditAPI.md#redditredditscraperhealthcheck) | **GET** /v1/reddit/health | Reddit scraper health check
[**redditRedditScraperHealthCheckHead**](RedditAPI.md#redditredditscraperhealthcheckhead) | **HEAD** /v1/reddit/health | Reddit scraper health check
[**redditSearchRedditPosts**](RedditAPI.md#redditsearchredditposts) | **GET** /v1/reddit/search/posts | Search Reddit posts
[**redditSearchSubreddits**](RedditAPI.md#redditsearchsubreddits) | **GET** /v1/reddit/search/subreddits | Search subreddits
[**redditSearchUsers**](RedditAPI.md#redditsearchusers) | **GET** /v1/reddit/search/users | Search users


# **redditGetCrossPosts**
```swift
    open class func redditGetCrossPosts(postId: String, limit: Int? = nil, after: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get cross-posts

Get cross-posts and duplicates of a Reddit post.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let postId = "postId_example" // String | 
let limit = 987 // Int |  (optional) (default to 25)
let after = "after_example" // String |  (optional)

// Get cross-posts
RedditAPI.redditGetCrossPosts(postId: postId, limit: limit, after: after) { (response, error) in
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
 **limit** | **Int** |  | [optional] [default to 25]
 **after** | **String** |  | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **redditGetPostComments**
```swift
    open class func redditGetPostComments(postId: String, sort: String? = nil, limit: Int? = nil, depth: Int? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get post comments

Get comment tree for a Reddit post.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let postId = "postId_example" // String | 
let sort = "sort_example" // String | Sort: confidence, top, new, controversial, old, qa (optional) (default to "confidence")
let limit = 987 // Int |  (optional) (default to 25)
let depth = 987 // Int |  (optional)

// Get post comments
RedditAPI.redditGetPostComments(postId: postId, sort: sort, limit: limit, depth: depth) { (response, error) in
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
 **sort** | **String** | Sort: confidence, top, new, controversial, old, qa | [optional] [default to &quot;confidence&quot;]
 **limit** | **Int** |  | [optional] [default to 25]
 **depth** | **Int** |  | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **redditGetPostDetail**
```swift
    open class func redditGetPostDetail(postId: String, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get post detail

Get detailed information about a Reddit post.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let postId = "postId_example" // String | 

// Get post detail
RedditAPI.redditGetPostDetail(postId: postId) { (response, error) in
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

# **redditGetPostsByDomain**
```swift
    open class func redditGetPostsByDomain(domain: String, sort: String? = nil, t: String? = nil, limit: Int? = nil, after: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get posts by domain

Get Reddit posts linking to a specific domain.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let domain = "domain_example" // String | 
let sort = "sort_example" // String |  (optional) (default to "hot")
let t = "t_example" // String |  (optional) (default to "all")
let limit = 987 // Int |  (optional) (default to 25)
let after = "after_example" // String |  (optional)

// Get posts by domain
RedditAPI.redditGetPostsByDomain(domain: domain, sort: sort, t: t, limit: limit, after: after) { (response, error) in
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
 **domain** | **String** |  | 
 **sort** | **String** |  | [optional] [default to &quot;hot&quot;]
 **t** | **String** |  | [optional] [default to &quot;all&quot;]
 **limit** | **Int** |  | [optional] [default to 25]
 **after** | **String** |  | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **redditGetSubredditInfo**
```swift
    open class func redditGetSubredditInfo(subreddit: String, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get subreddit info

Get detailed information about a subreddit.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let subreddit = "subreddit_example" // String | 

// Get subreddit info
RedditAPI.redditGetSubredditInfo(subreddit: subreddit) { (response, error) in
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
 **subreddit** | **String** |  | 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **redditGetSubredditPosts**
```swift
    open class func redditGetSubredditPosts(subreddit: String, sort: String? = nil, t: String? = nil, limit: Int? = nil, after: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get subreddit posts

Get posts from a subreddit with sorting options.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let subreddit = "subreddit_example" // String | 
let sort = "sort_example" // String | Sort: hot, new, top, rising, controversial (optional) (default to "hot")
let t = "t_example" // String | Time filter (optional) (default to "all")
let limit = 987 // Int |  (optional) (default to 25)
let after = "after_example" // String |  (optional)

// Get subreddit posts
RedditAPI.redditGetSubredditPosts(subreddit: subreddit, sort: sort, t: t, limit: limit, after: after) { (response, error) in
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
 **subreddit** | **String** |  | 
 **sort** | **String** | Sort: hot, new, top, rising, controversial | [optional] [default to &quot;hot&quot;]
 **t** | **String** | Time filter | [optional] [default to &quot;all&quot;]
 **limit** | **Int** |  | [optional] [default to 25]
 **after** | **String** |  | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **redditGetSubredditRules**
```swift
    open class func redditGetSubredditRules(subreddit: String, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get subreddit rules

Get the rules of a subreddit.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let subreddit = "subreddit_example" // String | 

// Get subreddit rules
RedditAPI.redditGetSubredditRules(subreddit: subreddit) { (response, error) in
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
 **subreddit** | **String** |  | 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **redditGetTrendingPosts**
```swift
    open class func redditGetTrendingPosts(sort: String? = nil, t: String? = nil, limit: Int? = nil, after: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get trending posts

Get trending posts from Reddit's front page.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let sort = "sort_example" // String | Sort: hot, new, top, rising, controversial, best (optional) (default to "hot")
let t = "t_example" // String | Time filter (optional) (default to "day")
let limit = 987 // Int |  (optional) (default to 25)
let after = "after_example" // String |  (optional)

// Get trending posts
RedditAPI.redditGetTrendingPosts(sort: sort, t: t, limit: limit, after: after) { (response, error) in
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
 **sort** | **String** | Sort: hot, new, top, rising, controversial, best | [optional] [default to &quot;hot&quot;]
 **t** | **String** | Time filter | [optional] [default to &quot;day&quot;]
 **limit** | **Int** |  | [optional] [default to 25]
 **after** | **String** |  | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **redditGetUserProfile**
```swift
    open class func redditGetUserProfile(username: String, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get user profile

Get a Reddit user's profile.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let username = "username_example" // String | 

// Get user profile
RedditAPI.redditGetUserProfile(username: username) { (response, error) in
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

# **redditGetUserSComments**
```swift
    open class func redditGetUserSComments(username: String, sort: String? = nil, t: String? = nil, limit: Int? = nil, after: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get user's comments

Get comments by a Reddit user.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let username = "username_example" // String | 
let sort = "sort_example" // String |  (optional) (default to "new")
let t = "t_example" // String |  (optional) (default to "all")
let limit = 987 // Int |  (optional) (default to 25)
let after = "after_example" // String |  (optional)

// Get user's comments
RedditAPI.redditGetUserSComments(username: username, sort: sort, t: t, limit: limit, after: after) { (response, error) in
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
 **sort** | **String** |  | [optional] [default to &quot;new&quot;]
 **t** | **String** |  | [optional] [default to &quot;all&quot;]
 **limit** | **Int** |  | [optional] [default to 25]
 **after** | **String** |  | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **redditGetUserSModeratedSubreddits**
```swift
    open class func redditGetUserSModeratedSubreddits(username: String, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get user's moderated subreddits

Get subreddits moderated by a user.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let username = "username_example" // String | 

// Get user's moderated subreddits
RedditAPI.redditGetUserSModeratedSubreddits(username: username) { (response, error) in
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

# **redditGetUserSPosts**
```swift
    open class func redditGetUserSPosts(username: String, sort: String? = nil, t: String? = nil, limit: Int? = nil, after: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get user's posts

Get posts submitted by a Reddit user.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let username = "username_example" // String | 
let sort = "sort_example" // String |  (optional) (default to "new")
let t = "t_example" // String |  (optional) (default to "all")
let limit = 987 // Int |  (optional) (default to 25)
let after = "after_example" // String |  (optional)

// Get user's posts
RedditAPI.redditGetUserSPosts(username: username, sort: sort, t: t, limit: limit, after: after) { (response, error) in
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
 **sort** | **String** |  | [optional] [default to &quot;new&quot;]
 **t** | **String** |  | [optional] [default to &quot;all&quot;]
 **limit** | **Int** |  | [optional] [default to 25]
 **after** | **String** |  | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **redditGetUserSTrophies**
```swift
    open class func redditGetUserSTrophies(username: String, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get user's trophies

Get a user's trophy case.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let username = "username_example" // String | 

// Get user's trophies
RedditAPI.redditGetUserSTrophies(username: username) { (response, error) in
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

# **redditGetWikiPageContent**
```swift
    open class func redditGetWikiPageContent(subreddit: String, page: String, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get wiki page content

Get the content of a specific wiki page.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let subreddit = "subreddit_example" // String | 
let page = "page_example" // String | 

// Get wiki page content
RedditAPI.redditGetWikiPageContent(subreddit: subreddit, page: page) { (response, error) in
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
 **subreddit** | **String** |  | 
 **page** | **String** |  | 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **redditListWikiPages**
```swift
    open class func redditListWikiPages(subreddit: String, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

List wiki pages

List all wiki pages in a subreddit.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let subreddit = "subreddit_example" // String | 

// List wiki pages
RedditAPI.redditListWikiPages(subreddit: subreddit) { (response, error) in
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
 **subreddit** | **String** |  | 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **redditNewSubreddits**
```swift
    open class func redditNewSubreddits(limit: Int? = nil, after: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

New subreddits

Get recently created subreddits.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let limit = 987 // Int |  (optional) (default to 25)
let after = "after_example" // String |  (optional)

// New subreddits
RedditAPI.redditNewSubreddits(limit: limit, after: after) { (response, error) in
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
 **limit** | **Int** |  | [optional] [default to 25]
 **after** | **String** |  | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **redditPopularSubreddits**
```swift
    open class func redditPopularSubreddits(limit: Int? = nil, after: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Popular subreddits

Get popular subreddits by subscriber count.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let limit = 987 // Int |  (optional) (default to 25)
let after = "after_example" // String |  (optional)

// Popular subreddits
RedditAPI.redditPopularSubreddits(limit: limit, after: after) { (response, error) in
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
 **limit** | **Int** |  | [optional] [default to 25]
 **after** | **String** |  | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **redditRedditScraperHealthCheck**
```swift
    open class func redditRedditScraperHealthCheck(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Reddit scraper health check

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// Reddit scraper health check
RedditAPI.redditRedditScraperHealthCheck() { (response, error) in
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

# **redditRedditScraperHealthCheckHead**
```swift
    open class func redditRedditScraperHealthCheckHead(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Reddit scraper health check

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// Reddit scraper health check
RedditAPI.redditRedditScraperHealthCheckHead() { (response, error) in
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

# **redditSearchRedditPosts**
```swift
    open class func redditSearchRedditPosts(q: String, subreddit: String? = nil, sort: String? = nil, t: String? = nil, limit: Int? = nil, after: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Search Reddit posts

Search Reddit posts globally or within a subreddit.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let q = "q_example" // String | Search query
let subreddit = "subreddit_example" // String | Restrict to subreddit (optional)
let sort = "sort_example" // String | Sort: relevance, hot, top, new, comments (optional) (default to "relevance")
let t = "t_example" // String | Time: hour, day, week, month, year, all (optional) (default to "all")
let limit = 987 // Int |  (optional) (default to 25)
let after = "after_example" // String |  (optional)

// Search Reddit posts
RedditAPI.redditSearchRedditPosts(q: q, subreddit: subreddit, sort: sort, t: t, limit: limit, after: after) { (response, error) in
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
 **subreddit** | **String** | Restrict to subreddit | [optional] 
 **sort** | **String** | Sort: relevance, hot, top, new, comments | [optional] [default to &quot;relevance&quot;]
 **t** | **String** | Time: hour, day, week, month, year, all | [optional] [default to &quot;all&quot;]
 **limit** | **Int** |  | [optional] [default to 25]
 **after** | **String** |  | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **redditSearchSubreddits**
```swift
    open class func redditSearchSubreddits(q: String, limit: Int? = nil, after: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Search subreddits

Search for subreddits by keyword.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let q = "q_example" // String | Search query
let limit = 987 // Int |  (optional) (default to 25)
let after = "after_example" // String |  (optional)

// Search subreddits
RedditAPI.redditSearchSubreddits(q: q, limit: limit, after: after) { (response, error) in
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
 **limit** | **Int** |  | [optional] [default to 25]
 **after** | **String** |  | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **redditSearchUsers**
```swift
    open class func redditSearchUsers(q: String, limit: Int? = nil, after: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Search users

Search for Reddit users.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let q = "q_example" // String | Search query
let limit = 987 // Int |  (optional) (default to 25)
let after = "after_example" // String |  (optional)

// Search users
RedditAPI.redditSearchUsers(q: q, limit: limit, after: after) { (response, error) in
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
 **limit** | **Int** |  | [optional] [default to 25]
 **after** | **String** |  | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

