# FacebookAPI

All URIs are relative to *https://scrapebadger.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**facebookBrowseAMarketplaceCategory**](FacebookAPI.md#facebookbrowseamarketplacecategory) | **GET** /v1/facebook/marketplace/category/{category} | Browse a Marketplace category
[**facebookGetAMarketplaceItem**](FacebookAPI.md#facebookgetamarketplaceitem) | **GET** /v1/facebook/marketplace/item/{item_id} | Get a Marketplace item
[**facebookGetAnAd**](FacebookAPI.md#facebookgetanad) | **GET** /v1/facebook/ads/{ad_archive_id} | Get an ad
[**facebookGetGroupDetail**](FacebookAPI.md#facebookgetgroupdetail) | **GET** /v1/facebook/groups/{group_id} | Get group detail
[**facebookGetGroupPosts**](FacebookAPI.md#facebookgetgroupposts) | **GET** /v1/facebook/groups/{group_id}/posts | Get group posts
[**facebookGetPageDetail**](FacebookAPI.md#facebookgetpagedetail) | **GET** /v1/facebook/pages/{identifier} | Get page detail
[**facebookGetPagePosts**](FacebookAPI.md#facebookgetpageposts) | **GET** /v1/facebook/pages/{identifier}/posts | Get page posts
[**facebookGetPostComments**](FacebookAPI.md#facebookgetpostcomments) | **GET** /v1/facebook/posts/{post_id}/comments | Get post comments
[**facebookGetPostDetail**](FacebookAPI.md#facebookgetpostdetail) | **GET** /v1/facebook/posts/{post_id} | Get post detail
[**facebookGetProfileDetail**](FacebookAPI.md#facebookgetprofiledetail) | **GET** /v1/facebook/profiles/{identifier} | Get profile detail
[**facebookGetProfilePosts**](FacebookAPI.md#facebookgetprofileposts) | **GET** /v1/facebook/profiles/{identifier}/posts | Get profile posts
[**facebookListCategories**](FacebookAPI.md#facebooklistcategories) | **GET** /v1/facebook/marketplace/categories | List categories
[**facebookListLocations**](FacebookAPI.md#facebooklistlocations) | **GET** /v1/facebook/marketplace/locations | List locations
[**facebookSearchEvents**](FacebookAPI.md#facebooksearchevents) | **GET** /v1/facebook/search/events | Search events
[**facebookSearchEverything**](FacebookAPI.md#facebooksearcheverything) | **GET** /v1/facebook/search | Search everything
[**facebookSearchGroups**](FacebookAPI.md#facebooksearchgroups) | **GET** /v1/facebook/search/groups | Search groups
[**facebookSearchMarketplace**](FacebookAPI.md#facebooksearchmarketplace) | **GET** /v1/facebook/marketplace/search | Search Marketplace
[**facebookSearchPages**](FacebookAPI.md#facebooksearchpages) | **GET** /v1/facebook/search/pages | Search Pages
[**facebookSearchPeople**](FacebookAPI.md#facebooksearchpeople) | **GET** /v1/facebook/search/people | Search people
[**facebookSearchPlaces**](FacebookAPI.md#facebooksearchplaces) | **GET** /v1/facebook/search/places | Search places
[**facebookSearchPosts**](FacebookAPI.md#facebooksearchposts) | **GET** /v1/facebook/search/posts | Search posts
[**facebookSearchTheAdLibrary**](FacebookAPI.md#facebooksearchtheadlibrary) | **GET** /v1/facebook/ads/search | Search the Ad Library


# **facebookBrowseAMarketplaceCategory**
```swift
    open class func facebookBrowseAMarketplaceCategory(category: String, location: String? = nil, minPrice: Int? = nil, maxPrice: Int? = nil, sortBy: String? = nil, after: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Browse a Marketplace category

Browse Marketplace listings in a category (vehicles, electronics, ...).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let category = "category_example" // String | 
let location = "location_example" // String |  (optional) (default to "nyc")
let minPrice = 987 // Int |  (optional)
let maxPrice = 987 // Int |  (optional)
let sortBy = "sortBy_example" // String |  (optional)
let after = "after_example" // String |  (optional)

// Browse a Marketplace category
FacebookAPI.facebookBrowseAMarketplaceCategory(category: category, location: location, minPrice: minPrice, maxPrice: maxPrice, sortBy: sortBy, after: after) { (response, error) in
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
 **category** | **String** |  | 
 **location** | **String** |  | [optional] [default to &quot;nyc&quot;]
 **minPrice** | **Int** |  | [optional] 
 **maxPrice** | **Int** |  | [optional] 
 **sortBy** | **String** |  | [optional] 
 **after** | **String** |  | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **facebookGetAMarketplaceItem**
```swift
    open class func facebookGetAMarketplaceItem(itemId: String, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get a Marketplace item

Get full detail for a single Marketplace listing.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let itemId = "itemId_example" // String | 

// Get a Marketplace item
FacebookAPI.facebookGetAMarketplaceItem(itemId: itemId) { (response, error) in
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

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **facebookGetAnAd**
```swift
    open class func facebookGetAnAd(adArchiveId: String, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get an ad

Get a single Ad Library ad by its archive id.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let adArchiveId = "adArchiveId_example" // String | 

// Get an ad
FacebookAPI.facebookGetAnAd(adArchiveId: adArchiveId) { (response, error) in
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
 **adArchiveId** | **String** |  | 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **facebookGetGroupDetail**
```swift
    open class func facebookGetGroupDetail(groupId: String, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get group detail

Get a Facebook group's details.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let groupId = "groupId_example" // String | 

// Get group detail
FacebookAPI.facebookGetGroupDetail(groupId: groupId) { (response, error) in
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
 **groupId** | **String** |  | 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **facebookGetGroupPosts**
```swift
    open class func facebookGetGroupPosts(groupId: String, after: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get group posts

Get a Facebook group's post feed.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let groupId = "groupId_example" // String | 
let after = "after_example" // String |  (optional)

// Get group posts
FacebookAPI.facebookGetGroupPosts(groupId: groupId, after: after) { (response, error) in
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
 **groupId** | **String** |  | 
 **after** | **String** |  | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **facebookGetPageDetail**
```swift
    open class func facebookGetPageDetail(identifier: String, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get page detail

Get a Facebook Page's profile (name, category, followers, about).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let identifier = "identifier_example" // String | 

// Get page detail
FacebookAPI.facebookGetPageDetail(identifier: identifier) { (response, error) in
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
 **identifier** | **String** |  | 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **facebookGetPagePosts**
```swift
    open class func facebookGetPagePosts(identifier: String, after: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get page posts

Get a Facebook Page's timeline posts.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let identifier = "identifier_example" // String | 
let after = "after_example" // String |  (optional)

// Get page posts
FacebookAPI.facebookGetPagePosts(identifier: identifier, after: after) { (response, error) in
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
 **identifier** | **String** |  | 
 **after** | **String** |  | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **facebookGetPostComments**
```swift
    open class func facebookGetPostComments(postId: String, after: String? = nil, sort: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get post comments

Get a Facebook post's comment thread (paginated).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let postId = "postId_example" // String | 
let after = "after_example" // String |  (optional)
let sort = "sort_example" // String |  (optional) (default to "relevance")

// Get post comments
FacebookAPI.facebookGetPostComments(postId: postId, after: after, sort: sort) { (response, error) in
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
 **after** | **String** |  | [optional] 
 **sort** | **String** |  | [optional] [default to &quot;relevance&quot;]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **facebookGetPostDetail**
```swift
    open class func facebookGetPostDetail(postId: String, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get post detail

Get a Facebook post's detail plus its top comments.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let postId = "postId_example" // String | 

// Get post detail
FacebookAPI.facebookGetPostDetail(postId: postId) { (response, error) in
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

# **facebookGetProfileDetail**
```swift
    open class func facebookGetProfileDetail(identifier: String, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get profile detail

Get a Facebook profile's details.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let identifier = "identifier_example" // String | 

// Get profile detail
FacebookAPI.facebookGetProfileDetail(identifier: identifier) { (response, error) in
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
 **identifier** | **String** |  | 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **facebookGetProfilePosts**
```swift
    open class func facebookGetProfilePosts(identifier: String, after: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get profile posts

Get a Facebook profile's timeline posts.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let identifier = "identifier_example" // String | 
let after = "after_example" // String |  (optional)

// Get profile posts
FacebookAPI.facebookGetProfilePosts(identifier: identifier, after: after) { (response, error) in
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
 **identifier** | **String** |  | 
 **after** | **String** |  | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **facebookListCategories**
```swift
    open class func facebookListCategories(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

List categories

List Marketplace category slugs (free).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// List categories
FacebookAPI.facebookListCategories() { (response, error) in
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

# **facebookListLocations**
```swift
    open class func facebookListLocations(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

List locations

List common Marketplace location slugs (free).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// List locations
FacebookAPI.facebookListLocations() { (response, error) in
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

# **facebookSearchEvents**
```swift
    open class func facebookSearchEvents(q: String, after: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Search events

Search Facebook events.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let q = "q_example" // String | 
let after = "after_example" // String |  (optional)

// Search events
FacebookAPI.facebookSearchEvents(q: q, after: after) { (response, error) in
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
 **q** | **String** |  | 
 **after** | **String** |  | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **facebookSearchEverything**
```swift
    open class func facebookSearchEverything(q: String, after: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Search everything

Global Facebook search (top results across pages, people, groups, posts).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let q = "q_example" // String | Search query
let after = "after_example" // String |  (optional)

// Search everything
FacebookAPI.facebookSearchEverything(q: q, after: after) { (response, error) in
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
 **after** | **String** |  | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **facebookSearchGroups**
```swift
    open class func facebookSearchGroups(q: String, after: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Search groups

Search Facebook groups.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let q = "q_example" // String | 
let after = "after_example" // String |  (optional)

// Search groups
FacebookAPI.facebookSearchGroups(q: q, after: after) { (response, error) in
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
 **q** | **String** |  | 
 **after** | **String** |  | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **facebookSearchMarketplace**
```swift
    open class func facebookSearchMarketplace(query: String, location: String? = nil, minPrice: Int? = nil, maxPrice: Int? = nil, daysSinceListed: Int? = nil, sortBy: String? = nil, itemCondition: String? = nil, deliveryMethod: String? = nil, after: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Search Marketplace

Search Facebook Marketplace listings by keyword and location.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let query = "query_example" // String | Search keywords
let location = "location_example" // String | Marketplace location slug (optional) (default to "nyc")
let minPrice = 987 // Int |  (optional)
let maxPrice = 987 // Int |  (optional)
let daysSinceListed = 987 // Int |  (optional)
let sortBy = "sortBy_example" // String |  (optional)
let itemCondition = "itemCondition_example" // String |  (optional)
let deliveryMethod = "deliveryMethod_example" // String |  (optional)
let after = "after_example" // String |  (optional)

// Search Marketplace
FacebookAPI.facebookSearchMarketplace(query: query, location: location, minPrice: minPrice, maxPrice: maxPrice, daysSinceListed: daysSinceListed, sortBy: sortBy, itemCondition: itemCondition, deliveryMethod: deliveryMethod, after: after) { (response, error) in
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
 **location** | **String** | Marketplace location slug | [optional] [default to &quot;nyc&quot;]
 **minPrice** | **Int** |  | [optional] 
 **maxPrice** | **Int** |  | [optional] 
 **daysSinceListed** | **Int** |  | [optional] 
 **sortBy** | **String** |  | [optional] 
 **itemCondition** | **String** |  | [optional] 
 **deliveryMethod** | **String** |  | [optional] 
 **after** | **String** |  | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **facebookSearchPages**
```swift
    open class func facebookSearchPages(q: String, after: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Search Pages

Search Facebook Pages.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let q = "q_example" // String | 
let after = "after_example" // String |  (optional)

// Search Pages
FacebookAPI.facebookSearchPages(q: q, after: after) { (response, error) in
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
 **q** | **String** |  | 
 **after** | **String** |  | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **facebookSearchPeople**
```swift
    open class func facebookSearchPeople(q: String, after: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Search people

Search Facebook profiles.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let q = "q_example" // String | 
let after = "after_example" // String |  (optional)

// Search people
FacebookAPI.facebookSearchPeople(q: q, after: after) { (response, error) in
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
 **q** | **String** |  | 
 **after** | **String** |  | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **facebookSearchPlaces**
```swift
    open class func facebookSearchPlaces(q: String, after: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Search places

Search Facebook places.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let q = "q_example" // String | 
let after = "after_example" // String |  (optional)

// Search places
FacebookAPI.facebookSearchPlaces(q: q, after: after) { (response, error) in
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
 **q** | **String** |  | 
 **after** | **String** |  | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **facebookSearchPosts**
```swift
    open class func facebookSearchPosts(q: String, after: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Search posts

Search public Facebook posts.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let q = "q_example" // String | 
let after = "after_example" // String |  (optional)

// Search posts
FacebookAPI.facebookSearchPosts(q: q, after: after) { (response, error) in
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
 **q** | **String** |  | 
 **after** | **String** |  | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **facebookSearchTheAdLibrary**
```swift
    open class func facebookSearchTheAdLibrary(query: String, country: String? = nil, adType: String? = nil, activeStatus: String? = nil, after: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Search the Ad Library

Search the Facebook Ad Library.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let query = "query_example" // String | Advertiser or keyword
let country = "country_example" // String |  (optional) (default to "US")
let adType = "adType_example" // String |  (optional) (default to "all")
let activeStatus = "activeStatus_example" // String |  (optional) (default to "active")
let after = "after_example" // String |  (optional)

// Search the Ad Library
FacebookAPI.facebookSearchTheAdLibrary(query: query, country: country, adType: adType, activeStatus: activeStatus, after: after) { (response, error) in
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
 **query** | **String** | Advertiser or keyword | 
 **country** | **String** |  | [optional] [default to &quot;US&quot;]
 **adType** | **String** |  | [optional] [default to &quot;all&quot;]
 **activeStatus** | **String** |  | [optional] [default to &quot;active&quot;]
 **after** | **String** |  | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

