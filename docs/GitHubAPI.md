# GitHubAPI

All URIs are relative to *https://scrapebadger.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**githubGetProfile**](GitHubAPI.md#githubgetprofile) | **GET** /v1/github/profiles/{username} | Get profile
[**githubGetRepository**](GitHubAPI.md#githubgetrepository) | **GET** /v1/github/repositories/{owner}/{repo} | Get repository


# **githubGetProfile**
```swift
    open class func githubGetProfile(username: String, tab: Tab_githubGetProfile? = nil, year: Int? = nil, page: Int? = nil, nextPageToken: String? = nil, completion: @escaping (_ data: GitHubProfileResponse?, _ error: Error?) -> Void)
```

Get profile

Public user or organization profile, pins/popular repositories, README and contributions.  The overview preserves GitHub's public website sections, including organization-specific metadata. Compact displayed counts are approximate and marked with *_approximate. Unavailable or blocked data is an unbilled error, never an empty success.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let username = "username_example" // String | 
let tab = "tab_example" // String | Profile section; stars is available for users only (optional) (default to .overview)
let year = 987 // Int | Overview only: 1970 through the current UTC year; activity is December or current month (optional)
let page = 987 // Int | Repositories only: page number, 30 rows per page (optional)
let nextPageToken = "nextPageToken_example" // String | Stars only: previous pagination.next_page_token (optional)

// Get profile
GitHubAPI.githubGetProfile(username: username, tab: tab, year: year, page: page, nextPageToken: nextPageToken) { (response, error) in
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
 **tab** | **String** | Profile section; stars is available for users only | [optional] [default to .overview]
 **year** | **Int** | Overview only: 1970 through the current UTC year; activity is December or current month | [optional] 
 **page** | **Int** | Repositories only: page number, 30 rows per page | [optional] 
 **nextPageToken** | **String** | Stars only: previous pagination.next_page_token | [optional] 

### Return type

[**GitHubProfileResponse**](GitHubProfileResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **githubGetRepository**
```swift
    open class func githubGetRepository(owner: String, repo: String, completion: @escaping (_ data: GitHubRepositoryResponse?, _ error: Error?) -> Void)
```

Get repository

Public default-branch repository detail, native README, files and latest commit.  Use owner.login and name from a profile repository summary. Root file and contributor previews are not exhaustive recursive trees or membership lists. No GitHub token, market, ref, search or pagination parameter is accepted.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let owner = "owner_example" // String | 
let repo = "repo_example" // String | 

// Get repository
GitHubAPI.githubGetRepository(owner: owner, repo: repo) { (response, error) in
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
 **owner** | **String** |  | 
 **repo** | **String** |  | 

### Return type

[**GitHubRepositoryResponse**](GitHubRepositoryResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

