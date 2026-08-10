# TwitterAPI

All URIs are relative to *https://scrapebadger.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**twitterAdvancedTweetSearch**](TwitterAPI.md#twitteradvancedtweetsearch) | **GET** /v1/twitter/tweets/advanced_search | Advanced tweet search
[**twitterBatchGetUsersByIds**](TwitterAPI.md#twitterbatchgetusersbyids) | **GET** /v1/twitter/users/batch_by_ids | Batch get users by IDs
[**twitterBatchGetUsersByUsernames**](TwitterAPI.md#twitterbatchgetusersbyusernames) | **GET** /v1/twitter/users/batch_by_usernames | Batch get users by usernames
[**twitterConfigureWebhookOnAMonitor**](TwitterAPI.md#twitterconfigurewebhookonamonitor) | **POST** /v1/twitter/stream/webhooks | Configure webhook on a monitor
[**twitterCreateFilterRule**](TwitterAPI.md#twittercreatefilterrule) | **POST** /v1/twitter/stream/filter-rules | Create filter rule
[**twitterCreateStreamMonitor**](TwitterAPI.md#twittercreatestreammonitor) | **POST** /v1/twitter/stream/monitors | Create stream monitor
[**twitterDeleteFilterRule**](TwitterAPI.md#twitterdeletefilterrule) | **DELETE** /v1/twitter/stream/filter-rules/{rule_id} | Delete filter rule
[**twitterDeleteStreamMonitor**](TwitterAPI.md#twitterdeletestreammonitor) | **DELETE** /v1/twitter/stream/monitors/{monitor_id} | Delete stream monitor
[**twitterGetArticleById**](TwitterAPI.md#twittergetarticlebyid) | **GET** /v1/twitter/tweets/article/{article_id} | Get article by ID
[**twitterGetBroadcastDetails**](TwitterAPI.md#twittergetbroadcastdetails) | **GET** /v1/twitter/spaces/broadcast/{broadcast_id} | Get broadcast details
[**twitterGetCommunityDetails**](TwitterAPI.md#twittergetcommunitydetails) | **GET** /v1/twitter/communities/{community_id} | Get community details
[**twitterGetCommunityNotes**](TwitterAPI.md#twittergetcommunitynotes) | **GET** /v1/twitter/tweets/tweet/{tweet_id}/community_notes | Get community notes
[**twitterGetCommunityTweets**](TwitterAPI.md#twittergetcommunitytweets) | **GET** /v1/twitter/communities/{community_id}/tweets | Get community tweets
[**twitterGetFilterRule**](TwitterAPI.md#twittergetfilterrule) | **GET** /v1/twitter/stream/filter-rules/{rule_id} | Get filter rule
[**twitterGetFilterRulePerPollRates**](TwitterAPI.md#twittergetfilterruleperpollrates) | **GET** /v1/twitter/stream/filter-rules-pricing | Get filter rule per-poll rates
[**twitterGetListDetails**](TwitterAPI.md#twittergetlistdetails) | **GET** /v1/twitter/lists/{list_id}/detail | Get list details
[**twitterGetListTweets**](TwitterAPI.md#twittergetlisttweets) | **GET** /v1/twitter/lists/{list_id}/tweets | Get list tweets
[**twitterGetPlaceDetails**](TwitterAPI.md#twittergetplacedetails) | **GET** /v1/twitter/geo/places/{place_id} | Get place details
[**twitterGetSimilarTweets**](TwitterAPI.md#twittergetsimilartweets) | **GET** /v1/twitter/tweets/tweet/{tweet_id}/similar | Get similar tweets
[**twitterGetSpaceDetails**](TwitterAPI.md#twittergetspacedetails) | **GET** /v1/twitter/spaces/{space_id} | Get Space details
[**twitterGetStreamMonitor**](TwitterAPI.md#twittergetstreammonitor) | **GET** /v1/twitter/stream/monitors/{monitor_id} | Get stream monitor
[**twitterGetTrendingTopics**](TwitterAPI.md#twittergettrendingtopics) | **GET** /v1/twitter/trends/ | Get trending topics
[**twitterGetTrendsByLocation**](TwitterAPI.md#twittergettrendsbylocation) | **GET** /v1/twitter/trends/place/{woeid} | Get trends by location
[**twitterGetTweetDetails**](TwitterAPI.md#twittergettweetdetails) | **GET** /v1/twitter/tweets/tweet/{tweet_id} | Get tweet details
[**twitterGetTweetEditHistory**](TwitterAPI.md#twittergettweetedithistory) | **GET** /v1/twitter/tweets/tweet/{tweet_id}/edit_history | Get tweet edit history
[**twitterGetTweetFavoriters**](TwitterAPI.md#twittergettweetfavoriters) | **GET** /v1/twitter/tweets/tweet/{tweet_id}/favoriters | Get tweet favoriters
[**twitterGetTweetQuotes**](TwitterAPI.md#twittergettweetquotes) | **GET** /v1/twitter/tweets/tweet/{tweet_id}/quotes | Get tweet quotes
[**twitterGetTweetReplies**](TwitterAPI.md#twittergettweetreplies) | **GET** /v1/twitter/tweets/tweet/{tweet_id}/replies | Get tweet replies
[**twitterGetTweetRetweeters**](TwitterAPI.md#twittergettweetretweeters) | **GET** /v1/twitter/tweets/tweet/{tweet_id}/retweeters | Get tweet retweeters
[**twitterGetTweetsByIds**](TwitterAPI.md#twittergettweetsbyids) | **GET** /v1/twitter/tweets/ | Get tweets by IDs
[**twitterGetUserArticles**](TwitterAPI.md#twittergetuserarticles) | **GET** /v1/twitter/users/{user_id}/articles | Get user articles
[**twitterGetUserById**](TwitterAPI.md#twittergetuserbyid) | **GET** /v1/twitter/users/{user_id}/by_id | Get user by ID
[**twitterGetUserByUsername**](TwitterAPI.md#twittergetuserbyusername) | **GET** /v1/twitter/users/{username}/by_username | Get user by username
[**twitterGetUserFollowers**](TwitterAPI.md#twittergetuserfollowers) | **GET** /v1/twitter/users/{username}/followers | Get user followers
[**twitterGetUserFollowing**](TwitterAPI.md#twittergetuserfollowing) | **GET** /v1/twitter/users/{username}/followings | Get user following
[**twitterGetUserMentions**](TwitterAPI.md#twittergetusermentions) | **GET** /v1/twitter/users/{username}/mentions | Get user mentions
[**twitterGetUserSubscriptions**](TwitterAPI.md#twittergetusersubscriptions) | **GET** /v1/twitter/users/{user_id}/subscriptions | Get user subscriptions
[**twitterGetUserTweets**](TwitterAPI.md#twittergetusertweets) | **GET** /v1/twitter/users/{username}/latest_tweets | Get user tweets
[**twitterListBillingLogs**](TwitterAPI.md#twitterlistbillinglogs) | **GET** /v1/twitter/stream/billing-logs | List billing logs
[**twitterListDeliveryLogsForAFilterRule**](TwitterAPI.md#twitterlistdeliverylogsforafilterrule) | **GET** /v1/twitter/stream/filter-rules/{rule_id}/logs | List delivery logs for a filter rule
[**twitterListFilterRules**](TwitterAPI.md#twitterlistfilterrules) | **GET** /v1/twitter/stream/filter-rules | List filter rules
[**twitterListStreamMonitors**](TwitterAPI.md#twitterliststreammonitors) | **GET** /v1/twitter/stream/monitors | List stream monitors
[**twitterListTweetDeliveryLogs**](TwitterAPI.md#twitterlisttweetdeliverylogs) | **GET** /v1/twitter/stream/logs | List tweet delivery logs
[**twitterListWebhooks**](TwitterAPI.md#twitterlistwebhooks) | **GET** /v1/twitter/stream/webhooks | List webhooks
[**twitterRemoveWebhookFromMonitor**](TwitterAPI.md#twitterremovewebhookfrommonitor) | **DELETE** /v1/twitter/stream/webhooks/{webhook_id} | Remove webhook from monitor
[**twitterSearchCommunities**](TwitterAPI.md#twittersearchcommunities) | **GET** /v1/twitter/communities/search | Search communities
[**twitterSearchListTweets**](TwitterAPI.md#twittersearchlisttweets) | **GET** /v1/twitter/lists/{list_id}/search_tweets | Search list tweets
[**twitterSearchPlaces**](TwitterAPI.md#twittersearchplaces) | **GET** /v1/twitter/geo/search | Search places
[**twitterSearchUsers**](TwitterAPI.md#twittersearchusers) | **GET** /v1/twitter/users/search_users | Search users
[**twitterTestWebhookDelivery**](TwitterAPI.md#twittertestwebhookdelivery) | **POST** /v1/twitter/stream/webhooks/test | Test webhook delivery
[**twitterTwitterScraperHealthCheck**](TwitterAPI.md#twittertwitterscraperhealthcheck) | **GET** /v1/twitter/health | Twitter scraper health check
[**twitterTwitterScraperHealthCheckHead**](TwitterAPI.md#twittertwitterscraperhealthcheckhead) | **HEAD** /v1/twitter/health | Twitter scraper health check
[**twitterUpdateFilterRule**](TwitterAPI.md#twitterupdatefilterrule) | **PATCH** /v1/twitter/stream/filter-rules/{rule_id} | Update filter rule
[**twitterUpdateStreamMonitor**](TwitterAPI.md#twitterupdatestreammonitor) | **PATCH** /v1/twitter/stream/monitors/{monitor_id} | Update stream monitor
[**twitterValidateSearchQuery**](TwitterAPI.md#twittervalidatesearchquery) | **POST** /v1/twitter/stream/filter-rules/validate | Validate search query


# **twitterAdvancedTweetSearch**
```swift
    open class func twitterAdvancedTweetSearch(query: String, queryType: String? = nil, count: Int? = nil, cursor: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Advanced tweet search

Search tweets with advanced options.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let query = "query_example" // String | 
let queryType = "queryType_example" // String |  (optional)
let count = 987 // Int |  (optional)
let cursor = "cursor_example" // String |  (optional)

// Advanced tweet search
TwitterAPI.twitterAdvancedTweetSearch(query: query, queryType: queryType, count: count, cursor: cursor) { (response, error) in
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
 **queryType** | **String** |  | [optional] 
 **count** | **Int** |  | [optional] 
 **cursor** | **String** |  | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **twitterBatchGetUsersByIds**
```swift
    open class func twitterBatchGetUsersByIds(userIds: String, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Batch get users by IDs

Get multiple user profiles by their numeric IDs (comma-separated).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let userIds = "userIds_example" // String | 

// Batch get users by IDs
TwitterAPI.twitterBatchGetUsersByIds(userIds: userIds) { (response, error) in
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
 **userIds** | **String** |  | 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **twitterBatchGetUsersByUsernames**
```swift
    open class func twitterBatchGetUsersByUsernames(usernames: String, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Batch get users by usernames

Get multiple user profiles by their usernames (comma-separated).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let usernames = "usernames_example" // String | 

// Batch get users by usernames
TwitterAPI.twitterBatchGetUsersByUsernames(usernames: usernames) { (response, error) in
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
 **usernames** | **String** |  | 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **twitterConfigureWebhookOnAMonitor**
```swift
    open class func twitterConfigureWebhookOnAMonitor(webhookCreate: WebhookCreate, completion: @escaping (_ data: WebhookResponse?, _ error: Error?) -> Void)
```

Configure webhook on a monitor

Configure a webhook delivery URL on a stream monitor.  The secret is returned only once on creation. Subsequent calls show secret_set: bool. If monitor already has a webhook, delete it first (409 is returned).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let webhookCreate = WebhookCreate(monitorId: "monitorId_example", url: "url_example", secret: "secret_example") // WebhookCreate | 

// Configure webhook on a monitor
TwitterAPI.twitterConfigureWebhookOnAMonitor(webhookCreate: webhookCreate) { (response, error) in
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
 **webhookCreate** | [**WebhookCreate**](WebhookCreate.md) |  | 

### Return type

[**WebhookResponse**](WebhookResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **twitterCreateFilterRule**
```swift
    open class func twitterCreateFilterRule(filterRuleCreate: FilterRuleCreate, completion: @escaping (_ data: FilterRuleResponse?, _ error: Error?) -> Void)
```

Create filter rule

Create a new query-based tweet filter rule.  The rule starts in 'active' status immediately. Credits must be positive. The (api_key_id, tag) pair must be unique.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let filterRuleCreate = FilterRuleCreate(tag: "tag_example", query: "query_example", intervalSeconds: 123, maxResultsPerPoll: 123, webhookUrl: "webhookUrl_example", webhookSecret: "webhookSecret_example") // FilterRuleCreate | 

// Create filter rule
TwitterAPI.twitterCreateFilterRule(filterRuleCreate: filterRuleCreate) { (response, error) in
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
 **filterRuleCreate** | [**FilterRuleCreate**](FilterRuleCreate.md) |  | 

### Return type

[**FilterRuleResponse**](FilterRuleResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **twitterCreateStreamMonitor**
```swift
    open class func twitterCreateStreamMonitor(streamMonitorCreate: StreamMonitorCreate, completion: @escaping (_ data: StreamMonitorResponse?, _ error: Error?) -> Void)
```

Create stream monitor

Create a new stream monitor to watch Twitter accounts in real-time.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let streamMonitorCreate = StreamMonitorCreate(name: "name_example", usernames: ["usernames_example"], webhookUrl: "webhookUrl_example", webhookSecret: "webhookSecret_example", filterTypes: ["filterTypes_example"]) // StreamMonitorCreate | 

// Create stream monitor
TwitterAPI.twitterCreateStreamMonitor(streamMonitorCreate: streamMonitorCreate) { (response, error) in
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
 **streamMonitorCreate** | [**StreamMonitorCreate**](StreamMonitorCreate.md) |  | 

### Return type

[**StreamMonitorResponse**](StreamMonitorResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **twitterDeleteFilterRule**
```swift
    open class func twitterDeleteFilterRule(ruleId: String, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```

Delete filter rule

Delete a filter rule and all its logs.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let ruleId = "ruleId_example" // String | 

// Delete filter rule
TwitterAPI.twitterDeleteFilterRule(ruleId: ruleId) { (response, error) in
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
 **ruleId** | **String** |  | 

### Return type

Void (empty response body)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **twitterDeleteStreamMonitor**
```swift
    open class func twitterDeleteStreamMonitor(monitorId: String, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```

Delete stream monitor

Delete a stream monitor and all its logs.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let monitorId = "monitorId_example" // String | 

// Delete stream monitor
TwitterAPI.twitterDeleteStreamMonitor(monitorId: monitorId) { (response, error) in
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
 **monitorId** | **String** |  | 

### Return type

Void (empty response body)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **twitterGetArticleById**
```swift
    open class func twitterGetArticleById(articleId: String, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get article by ID

Get a long-form article by its ID.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let articleId = "articleId_example" // String | 

// Get article by ID
TwitterAPI.twitterGetArticleById(articleId: articleId) { (response, error) in
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
 **articleId** | **String** |  | 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **twitterGetBroadcastDetails**
```swift
    open class func twitterGetBroadcastDetails(broadcastId: String, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get broadcast details

Get details of a live video broadcast.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let broadcastId = "broadcastId_example" // String | 

// Get broadcast details
TwitterAPI.twitterGetBroadcastDetails(broadcastId: broadcastId) { (response, error) in
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
 **broadcastId** | **String** |  | 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **twitterGetCommunityDetails**
```swift
    open class func twitterGetCommunityDetails(communityId: String, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get community details

Get details of a specific community.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let communityId = "communityId_example" // String | 

// Get community details
TwitterAPI.twitterGetCommunityDetails(communityId: communityId) { (response, error) in
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
 **communityId** | **String** |  | 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **twitterGetCommunityNotes**
```swift
    open class func twitterGetCommunityNotes(tweetId: String, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get community notes

Get community notes (Birdwatch) for a specific tweet.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let tweetId = "tweetId_example" // String | 

// Get community notes
TwitterAPI.twitterGetCommunityNotes(tweetId: tweetId) { (response, error) in
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
 **tweetId** | **String** |  | 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **twitterGetCommunityTweets**
```swift
    open class func twitterGetCommunityTweets(communityId: String, tweetType: String? = nil, cursor: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get community tweets

Get tweets from a specific community.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let communityId = "communityId_example" // String | 
let tweetType = "tweetType_example" // String |  (optional)
let cursor = "cursor_example" // String |  (optional)

// Get community tweets
TwitterAPI.twitterGetCommunityTweets(communityId: communityId, tweetType: tweetType, cursor: cursor) { (response, error) in
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
 **communityId** | **String** |  | 
 **tweetType** | **String** |  | [optional] 
 **cursor** | **String** |  | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **twitterGetFilterRule**
```swift
    open class func twitterGetFilterRule(ruleId: String, completion: @escaping (_ data: FilterRuleResponse?, _ error: Error?) -> Void)
```

Get filter rule

Get a single filter rule by ID.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let ruleId = "ruleId_example" // String | 

// Get filter rule
TwitterAPI.twitterGetFilterRule(ruleId: ruleId) { (response, error) in
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
 **ruleId** | **String** |  | 

### Return type

[**FilterRuleResponse**](FilterRuleResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **twitterGetFilterRulePerPollRates**
```swift
    open class func twitterGetFilterRulePerPollRates(completion: @escaping (_ data: PortalApiRoutersV1TwitterFilterRulesFilterRulePricingResponse?, _ error: Error?) -> Void)
```

Get filter rule per-poll rates

Current per-poll rates (auth required — used by SDK + dashboard).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// Get filter rule per-poll rates
TwitterAPI.twitterGetFilterRulePerPollRates() { (response, error) in
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

[**PortalApiRoutersV1TwitterFilterRulesFilterRulePricingResponse**](PortalApiRoutersV1TwitterFilterRulesFilterRulePricingResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **twitterGetListDetails**
```swift
    open class func twitterGetListDetails(listId: String, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get list details

Get details of a specific list.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let listId = "listId_example" // String | 

// Get list details
TwitterAPI.twitterGetListDetails(listId: listId) { (response, error) in
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
 **listId** | **String** |  | 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **twitterGetListTweets**
```swift
    open class func twitterGetListTweets(listId: String, cursor: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get list tweets

Get tweets from a specific list.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let listId = "listId_example" // String | 
let cursor = "cursor_example" // String |  (optional)

// Get list tweets
TwitterAPI.twitterGetListTweets(listId: listId, cursor: cursor) { (response, error) in
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
 **listId** | **String** |  | 
 **cursor** | **String** |  | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **twitterGetPlaceDetails**
```swift
    open class func twitterGetPlaceDetails(placeId: String, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get place details

Get details of a specific place.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let placeId = "placeId_example" // String | 

// Get place details
TwitterAPI.twitterGetPlaceDetails(placeId: placeId) { (response, error) in
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

# **twitterGetSimilarTweets**
```swift
    open class func twitterGetSimilarTweets(tweetId: String, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get similar tweets

Get tweets similar to a specific tweet.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let tweetId = "tweetId_example" // String | 

// Get similar tweets
TwitterAPI.twitterGetSimilarTweets(tweetId: tweetId) { (response, error) in
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
 **tweetId** | **String** |  | 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **twitterGetSpaceDetails**
```swift
    open class func twitterGetSpaceDetails(spaceId: String, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get Space details

Get details of a Twitter Space.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let spaceId = "spaceId_example" // String | 

// Get Space details
TwitterAPI.twitterGetSpaceDetails(spaceId: spaceId) { (response, error) in
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
 **spaceId** | **String** |  | 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **twitterGetStreamMonitor**
```swift
    open class func twitterGetStreamMonitor(monitorId: String, completion: @escaping (_ data: StreamMonitorResponse?, _ error: Error?) -> Void)
```

Get stream monitor

Get a single stream monitor by ID.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let monitorId = "monitorId_example" // String | 

// Get stream monitor
TwitterAPI.twitterGetStreamMonitor(monitorId: monitorId) { (response, error) in
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
 **monitorId** | **String** |  | 

### Return type

[**StreamMonitorResponse**](StreamMonitorResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **twitterGetTrendingTopics**
```swift
    open class func twitterGetTrendingTopics(category: String? = nil, count: Int? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get trending topics

Get trending topics.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let category = "category_example" // String |  (optional)
let count = 987 // Int |  (optional)

// Get trending topics
TwitterAPI.twitterGetTrendingTopics(category: category, count: count) { (response, error) in
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
 **category** | **String** |  | [optional] 
 **count** | **Int** |  | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **twitterGetTrendsByLocation**
```swift
    open class func twitterGetTrendsByLocation(woeid: String, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get trends by location

Get trending topics for a specific location (WOEID).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let woeid = "woeid_example" // String | 

// Get trends by location
TwitterAPI.twitterGetTrendsByLocation(woeid: woeid) { (response, error) in
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
 **woeid** | **String** |  | 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **twitterGetTweetDetails**
```swift
    open class func twitterGetTweetDetails(tweetId: String, cursor: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get tweet details

Get detailed information about a specific tweet.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let tweetId = "tweetId_example" // String | 
let cursor = "cursor_example" // String |  (optional)

// Get tweet details
TwitterAPI.twitterGetTweetDetails(tweetId: tweetId, cursor: cursor) { (response, error) in
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
 **tweetId** | **String** |  | 
 **cursor** | **String** |  | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **twitterGetTweetEditHistory**
```swift
    open class func twitterGetTweetEditHistory(tweetId: String, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get tweet edit history

Get the edit history of a tweet.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let tweetId = "tweetId_example" // String | 

// Get tweet edit history
TwitterAPI.twitterGetTweetEditHistory(tweetId: tweetId) { (response, error) in
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
 **tweetId** | **String** |  | 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **twitterGetTweetFavoriters**
```swift
    open class func twitterGetTweetFavoriters(tweetId: String, cursor: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get tweet favoriters

Get users who favorited a specific tweet.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let tweetId = "tweetId_example" // String | 
let cursor = "cursor_example" // String |  (optional)

// Get tweet favoriters
TwitterAPI.twitterGetTweetFavoriters(tweetId: tweetId, cursor: cursor) { (response, error) in
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
 **tweetId** | **String** |  | 
 **cursor** | **String** |  | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **twitterGetTweetQuotes**
```swift
    open class func twitterGetTweetQuotes(tweetId: String, cursor: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get tweet quotes

Get tweets that quote a specific tweet.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let tweetId = "tweetId_example" // String | 
let cursor = "cursor_example" // String |  (optional)

// Get tweet quotes
TwitterAPI.twitterGetTweetQuotes(tweetId: tweetId, cursor: cursor) { (response, error) in
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
 **tweetId** | **String** |  | 
 **cursor** | **String** |  | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **twitterGetTweetReplies**
```swift
    open class func twitterGetTweetReplies(tweetId: String, cursor: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get tweet replies

Get replies to a specific tweet.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let tweetId = "tweetId_example" // String | 
let cursor = "cursor_example" // String |  (optional)

// Get tweet replies
TwitterAPI.twitterGetTweetReplies(tweetId: tweetId, cursor: cursor) { (response, error) in
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
 **tweetId** | **String** |  | 
 **cursor** | **String** |  | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **twitterGetTweetRetweeters**
```swift
    open class func twitterGetTweetRetweeters(tweetId: String, cursor: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get tweet retweeters

Get users who retweeted a specific tweet.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let tweetId = "tweetId_example" // String | 
let cursor = "cursor_example" // String |  (optional)

// Get tweet retweeters
TwitterAPI.twitterGetTweetRetweeters(tweetId: tweetId, cursor: cursor) { (response, error) in
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
 **tweetId** | **String** |  | 
 **cursor** | **String** |  | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **twitterGetTweetsByIds**
```swift
    open class func twitterGetTweetsByIds(tweets: String, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get tweets by IDs

Get multiple tweets by their IDs.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let tweets = "tweets_example" // String | 

// Get tweets by IDs
TwitterAPI.twitterGetTweetsByIds(tweets: tweets) { (response, error) in
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
 **tweets** | **String** |  | 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **twitterGetUserArticles**
```swift
    open class func twitterGetUserArticles(userId: String, cursor: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get user articles

Get long-form articles written by a user.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let userId = "userId_example" // String | 
let cursor = "cursor_example" // String |  (optional)

// Get user articles
TwitterAPI.twitterGetUserArticles(userId: userId, cursor: cursor) { (response, error) in
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
 **cursor** | **String** |  | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **twitterGetUserById**
```swift
    open class func twitterGetUserById(userId: String, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get user by ID

Get user profile by user ID.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let userId = "userId_example" // String | 

// Get user by ID
TwitterAPI.twitterGetUserById(userId: userId) { (response, error) in
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

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **twitterGetUserByUsername**
```swift
    open class func twitterGetUserByUsername(username: String, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get user by username

Get user profile by username.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let username = "username_example" // String | 

// Get user by username
TwitterAPI.twitterGetUserByUsername(username: username) { (response, error) in
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

# **twitterGetUserFollowers**
```swift
    open class func twitterGetUserFollowers(username: String, cursor: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get user followers

Get followers of a specific user.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let username = "username_example" // String | 
let cursor = "cursor_example" // String |  (optional)

// Get user followers
TwitterAPI.twitterGetUserFollowers(username: username, cursor: cursor) { (response, error) in
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
 **cursor** | **String** |  | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **twitterGetUserFollowing**
```swift
    open class func twitterGetUserFollowing(username: String, cursor: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get user following

Get users that a specific user is following.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let username = "username_example" // String | 
let cursor = "cursor_example" // String |  (optional)

// Get user following
TwitterAPI.twitterGetUserFollowing(username: username, cursor: cursor) { (response, error) in
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
 **cursor** | **String** |  | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **twitterGetUserMentions**
```swift
    open class func twitterGetUserMentions(username: String, count: Int? = nil, cursor: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get user mentions

Get tweets mentioning a specific user.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let username = "username_example" // String | 
let count = 987 // Int |  (optional)
let cursor = "cursor_example" // String |  (optional)

// Get user mentions
TwitterAPI.twitterGetUserMentions(username: username, count: count, cursor: cursor) { (response, error) in
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
 **count** | **Int** |  | [optional] 
 **cursor** | **String** |  | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **twitterGetUserSubscriptions**
```swift
    open class func twitterGetUserSubscriptions(userId: String, cursor: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get user subscriptions

Get subscriptions of a specific user.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let userId = "userId_example" // String | 
let cursor = "cursor_example" // String |  (optional)

// Get user subscriptions
TwitterAPI.twitterGetUserSubscriptions(userId: userId, cursor: cursor) { (response, error) in
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
 **cursor** | **String** |  | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **twitterGetUserTweets**
```swift
    open class func twitterGetUserTweets(username: String, cursor: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get user tweets

Get latest tweets from a specific user.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let username = "username_example" // String | 
let cursor = "cursor_example" // String |  (optional)

// Get user tweets
TwitterAPI.twitterGetUserTweets(username: username, cursor: cursor) { (response, error) in
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
 **cursor** | **String** |  | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **twitterListBillingLogs**
```swift
    open class func twitterListBillingLogs(monitorId: String? = nil, page: Int? = nil, pageSize: Int? = nil, completion: @escaping (_ data: BillingLogListResponse?, _ error: Error?) -> Void)
```

List billing logs

List billing activity logs for the authenticated API key's monitors.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let monitorId = "monitorId_example" // String |  (optional)
let page = 987 // Int |  (optional) (default to 1)
let pageSize = 987 // Int |  (optional) (default to 20)

// List billing logs
TwitterAPI.twitterListBillingLogs(monitorId: monitorId, page: page, pageSize: pageSize) { (response, error) in
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
 **monitorId** | **String** |  | [optional] 
 **page** | **Int** |  | [optional] [default to 1]
 **pageSize** | **Int** |  | [optional] [default to 20]

### Return type

[**BillingLogListResponse**](BillingLogListResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **twitterListDeliveryLogsForAFilterRule**
```swift
    open class func twitterListDeliveryLogsForAFilterRule(ruleId: String, deliveryStatus: String? = nil, authorUsername: String? = nil, page: Int? = nil, pageSize: Int? = nil, sort: Sort_twitterListDeliveryLogsForAFilterRule? = nil, completion: @escaping (_ data: FilterRuleDeliveryLogListResponse?, _ error: Error?) -> Void)
```

List delivery logs for a filter rule

List tweet delivery logs for a specific filter rule.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let ruleId = "ruleId_example" // String | 
let deliveryStatus = "deliveryStatus_example" // String |  (optional)
let authorUsername = "authorUsername_example" // String |  (optional)
let page = 987 // Int |  (optional) (default to 1)
let pageSize = 987 // Int |  (optional) (default to 20)
let sort = "sort_example" // String |  (optional) (default to .desc)

// List delivery logs for a filter rule
TwitterAPI.twitterListDeliveryLogsForAFilterRule(ruleId: ruleId, deliveryStatus: deliveryStatus, authorUsername: authorUsername, page: page, pageSize: pageSize, sort: sort) { (response, error) in
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
 **ruleId** | **String** |  | 
 **deliveryStatus** | **String** |  | [optional] 
 **authorUsername** | **String** |  | [optional] 
 **page** | **Int** |  | [optional] [default to 1]
 **pageSize** | **Int** |  | [optional] [default to 20]
 **sort** | **String** |  | [optional] [default to .desc]

### Return type

[**FilterRuleDeliveryLogListResponse**](FilterRuleDeliveryLogListResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **twitterListFilterRules**
```swift
    open class func twitterListFilterRules(status: String? = nil, page: Int? = nil, pageSize: Int? = nil, completion: @escaping (_ data: FilterRuleListResponse?, _ error: Error?) -> Void)
```

List filter rules

List all filter rules for the authenticated API key.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let status = "status_example" // String |  (optional)
let page = 987 // Int |  (optional) (default to 1)
let pageSize = 987 // Int |  (optional) (default to 20)

// List filter rules
TwitterAPI.twitterListFilterRules(status: status, page: page, pageSize: pageSize) { (response, error) in
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
 **status** | **String** |  | [optional] 
 **page** | **Int** |  | [optional] [default to 1]
 **pageSize** | **Int** |  | [optional] [default to 20]

### Return type

[**FilterRuleListResponse**](FilterRuleListResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **twitterListStreamMonitors**
```swift
    open class func twitterListStreamMonitors(status: String? = nil, page: Int? = nil, pageSize: Int? = nil, completion: @escaping (_ data: StreamMonitorListResponse?, _ error: Error?) -> Void)
```

List stream monitors

List all stream monitors for the authenticated API key.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let status = "status_example" // String |  (optional)
let page = 987 // Int |  (optional) (default to 1)
let pageSize = 987 // Int |  (optional) (default to 20)

// List stream monitors
TwitterAPI.twitterListStreamMonitors(status: status, page: page, pageSize: pageSize) { (response, error) in
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
 **status** | **String** |  | [optional] 
 **page** | **Int** |  | [optional] [default to 1]
 **pageSize** | **Int** |  | [optional] [default to 20]

### Return type

[**StreamMonitorListResponse**](StreamMonitorListResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **twitterListTweetDeliveryLogs**
```swift
    open class func twitterListTweetDeliveryLogs(monitorId: String? = nil, authorUsername: String? = nil, deliveryStatus: String? = nil, page: Int? = nil, pageSize: Int? = nil, sort: Sort_twitterListTweetDeliveryLogs? = nil, completion: @escaping (_ data: TweetDeliveryLogListResponse?, _ error: Error?) -> Void)
```

List tweet delivery logs

List tweet delivery logs for the authenticated API key's monitors.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let monitorId = "monitorId_example" // String |  (optional)
let authorUsername = "authorUsername_example" // String |  (optional)
let deliveryStatus = "deliveryStatus_example" // String |  (optional)
let page = 987 // Int |  (optional) (default to 1)
let pageSize = 987 // Int |  (optional) (default to 20)
let sort = "sort_example" // String |  (optional) (default to .desc)

// List tweet delivery logs
TwitterAPI.twitterListTweetDeliveryLogs(monitorId: monitorId, authorUsername: authorUsername, deliveryStatus: deliveryStatus, page: page, pageSize: pageSize, sort: sort) { (response, error) in
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
 **monitorId** | **String** |  | [optional] 
 **authorUsername** | **String** |  | [optional] 
 **deliveryStatus** | **String** |  | [optional] 
 **page** | **Int** |  | [optional] [default to 1]
 **pageSize** | **Int** |  | [optional] [default to 20]
 **sort** | **String** |  | [optional] [default to .desc]

### Return type

[**TweetDeliveryLogListResponse**](TweetDeliveryLogListResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **twitterListWebhooks**
```swift
    open class func twitterListWebhooks(monitorId: String? = nil, completion: @escaping (_ data: WebhookListResponse?, _ error: Error?) -> Void)
```

List webhooks

List all webhook-configured monitors for the authenticated API key.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let monitorId = "monitorId_example" // String |  (optional)

// List webhooks
TwitterAPI.twitterListWebhooks(monitorId: monitorId) { (response, error) in
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
 **monitorId** | **String** |  | [optional] 

### Return type

[**WebhookListResponse**](WebhookListResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **twitterRemoveWebhookFromMonitor**
```swift
    open class func twitterRemoveWebhookFromMonitor(webhookId: String, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```

Remove webhook from monitor

Remove webhook configuration from a monitor. webhook_id is the monitor_id.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let webhookId = "webhookId_example" // String | 

// Remove webhook from monitor
TwitterAPI.twitterRemoveWebhookFromMonitor(webhookId: webhookId) { (response, error) in
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
 **webhookId** | **String** |  | 

### Return type

Void (empty response body)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **twitterSearchCommunities**
```swift
    open class func twitterSearchCommunities(query: String, cursor: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Search communities

Search for communities by query.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let query = "query_example" // String | 
let cursor = "cursor_example" // String |  (optional)

// Search communities
TwitterAPI.twitterSearchCommunities(query: query, cursor: cursor) { (response, error) in
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
 **cursor** | **String** |  | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **twitterSearchListTweets**
```swift
    open class func twitterSearchListTweets(listId: String, query: String, cursor: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Search list tweets

Search tweets within a specific list.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let listId = "listId_example" // String | 
let query = "query_example" // String | 
let cursor = "cursor_example" // String |  (optional)

// Search list tweets
TwitterAPI.twitterSearchListTweets(listId: listId, query: query, cursor: cursor) { (response, error) in
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
 **listId** | **String** |  | 
 **query** | **String** |  | 
 **cursor** | **String** |  | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **twitterSearchPlaces**
```swift
    open class func twitterSearchPlaces(query: String? = nil, lat: Double? = nil, long: Double? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Search places

Search for places by query or coordinates.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let query = "query_example" // String |  (optional)
let lat = 987 // Double |  (optional)
let long = 987 // Double |  (optional)

// Search places
TwitterAPI.twitterSearchPlaces(query: query, lat: lat, long: long) { (response, error) in
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
 **query** | **String** |  | [optional] 
 **lat** | **Double** |  | [optional] 
 **long** | **Double** |  | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **twitterSearchUsers**
```swift
    open class func twitterSearchUsers(query: String, cursor: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Search users

Search for users by query.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let query = "query_example" // String | 
let cursor = "cursor_example" // String |  (optional)

// Search users
TwitterAPI.twitterSearchUsers(query: query, cursor: cursor) { (response, error) in
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
 **cursor** | **String** |  | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **twitterTestWebhookDelivery**
```swift
    open class func twitterTestWebhookDelivery(webhookTestRequest: WebhookTestRequest, completion: @escaping (_ data: WebhookTestResponse?, _ error: Error?) -> Void)
```

Test webhook delivery

Send a test payload to a monitor's webhook URL.  The test payload has type=\"test\" instead of type=\"tweet\". Makes a synchronous HTTP POST and returns the delivery result.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let webhookTestRequest = WebhookTestRequest(monitorId: "monitorId_example") // WebhookTestRequest | 

// Test webhook delivery
TwitterAPI.twitterTestWebhookDelivery(webhookTestRequest: webhookTestRequest) { (response, error) in
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
 **webhookTestRequest** | [**WebhookTestRequest**](WebhookTestRequest.md) |  | 

### Return type

[**WebhookTestResponse**](WebhookTestResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **twitterTwitterScraperHealthCheck**
```swift
    open class func twitterTwitterScraperHealthCheck(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Twitter scraper health check

Check health of the Twitter scraper service.  Accepts ``HEAD`` so external uptime checkers (UptimeRobot uses HEAD by default for HTTP monitors) don't get a 405 Method Not Allowed.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// Twitter scraper health check
TwitterAPI.twitterTwitterScraperHealthCheck() { (response, error) in
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

# **twitterTwitterScraperHealthCheckHead**
```swift
    open class func twitterTwitterScraperHealthCheckHead(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Twitter scraper health check

Check health of the Twitter scraper service.  Accepts ``HEAD`` so external uptime checkers (UptimeRobot uses HEAD by default for HTTP monitors) don't get a 405 Method Not Allowed.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// Twitter scraper health check
TwitterAPI.twitterTwitterScraperHealthCheckHead() { (response, error) in
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

# **twitterUpdateFilterRule**
```swift
    open class func twitterUpdateFilterRule(ruleId: String, filterRuleUpdate: FilterRuleUpdate, completion: @escaping (_ data: FilterRuleResponse?, _ error: Error?) -> Void)
```

Update filter rule

Partially update a filter rule.  Setting status='active' on a paused rule performs a credit check.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let ruleId = "ruleId_example" // String | 
let filterRuleUpdate = FilterRuleUpdate(tag: "tag_example", query: "query_example", intervalSeconds: 123, maxResultsPerPoll: 123, status: "status_example", webhookUrl: "webhookUrl_example", webhookSecret: "webhookSecret_example") // FilterRuleUpdate | 

// Update filter rule
TwitterAPI.twitterUpdateFilterRule(ruleId: ruleId, filterRuleUpdate: filterRuleUpdate) { (response, error) in
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
 **ruleId** | **String** |  | 
 **filterRuleUpdate** | [**FilterRuleUpdate**](FilterRuleUpdate.md) |  | 

### Return type

[**FilterRuleResponse**](FilterRuleResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **twitterUpdateStreamMonitor**
```swift
    open class func twitterUpdateStreamMonitor(monitorId: String, streamMonitorUpdate: StreamMonitorUpdate, completion: @escaping (_ data: StreamMonitorResponse?, _ error: Error?) -> Void)
```

Update stream monitor

Partially update a stream monitor.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let monitorId = "monitorId_example" // String | 
let streamMonitorUpdate = StreamMonitorUpdate(name: "name_example", usernames: ["usernames_example"], status: "status_example", webhookUrl: "webhookUrl_example", webhookSecret: "webhookSecret_example", filterTypes: ["filterTypes_example"]) // StreamMonitorUpdate | 

// Update stream monitor
TwitterAPI.twitterUpdateStreamMonitor(monitorId: monitorId, streamMonitorUpdate: streamMonitorUpdate) { (response, error) in
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
 **monitorId** | **String** |  | 
 **streamMonitorUpdate** | [**StreamMonitorUpdate**](StreamMonitorUpdate.md) |  | 

### Return type

[**StreamMonitorResponse**](StreamMonitorResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **twitterValidateSearchQuery**
```swift
    open class func twitterValidateSearchQuery(filterRuleValidateRequest: FilterRuleValidateRequest, completion: @escaping (_ data: FilterRuleValidateResponse?, _ error: Error?) -> Void)
```

Validate search query

Validate a Twitter search query string.  Performs basic structural validation without making a live Twitter request. Returns valid=True if the query passes syntax checks.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let filterRuleValidateRequest = FilterRuleValidateRequest(query: "query_example") // FilterRuleValidateRequest | 

// Validate search query
TwitterAPI.twitterValidateSearchQuery(filterRuleValidateRequest: filterRuleValidateRequest) { (response, error) in
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
 **filterRuleValidateRequest** | [**FilterRuleValidateRequest**](FilterRuleValidateRequest.md) |  | 

### Return type

[**FilterRuleValidateResponse**](FilterRuleValidateResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

