# LinkedInAPI

All URIs are relative to *https://scrapebadger.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**linkedinGetACompanySJobPostings**](LinkedInAPI.md#linkedingetacompanysjobpostings) | **GET** /v1/linkedin/companies/{company_id}/jobs | Get a company&#39;s job postings
[**linkedinGetACourse**](LinkedInAPI.md#linkedingetacourse) | **GET** /v1/linkedin/learning/{course_slug} | Get a course
[**linkedinGetAPublicArticle**](LinkedInAPI.md#linkedingetapublicarticle) | **GET** /v1/linkedin/articles/{article_slug} | Get a public article
[**linkedinGetAPublicPost**](LinkedInAPI.md#linkedingetapublicpost) | **GET** /v1/linkedin/posts/{post_slug} | Get a public post
[**linkedinGetCompany**](LinkedInAPI.md#linkedingetcompany) | **GET** /v1/linkedin/companies/{universal_name} | Get company
[**linkedinGetJobDetail**](LinkedInAPI.md#linkedingetjobdetail) | **GET** /v1/linkedin/jobs/{job_id} | Get job detail
[**linkedinGetPublicProfile**](LinkedInAPI.md#linkedingetpublicprofile) | **GET** /v1/linkedin/profiles/{public_id} | Get public profile
[**linkedinGetSchool**](LinkedInAPI.md#linkedingetschool) | **GET** /v1/linkedin/schools/{universal_name} | Get school
[**linkedinLinkedinScraperHealthCheck**](LinkedInAPI.md#linkedinlinkedinscraperhealthcheck) | **GET** /v1/linkedin/health | LinkedIn scraper health check
[**linkedinLinkedinScraperHealthCheckHead**](LinkedInAPI.md#linkedinlinkedinscraperhealthcheckhead) | **HEAD** /v1/linkedin/health | LinkedIn scraper health check
[**linkedinSearchLinkedinJobs**](LinkedInAPI.md#linkedinsearchlinkedinjobs) | **GET** /v1/linkedin/jobs/search | Search LinkedIn jobs
[**linkedinSuggestLocationGeoIds**](LinkedInAPI.md#linkedinsuggestlocationgeoids) | **GET** /v1/linkedin/geo/suggest | Suggest location geo ids


# **linkedinGetACompanySJobPostings**
```swift
    open class func linkedinGetACompanySJobPostings(companyId: String, start: Int? = nil, country: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get a company's job postings

Public job postings for a company (numeric company id from the company endpoint).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let companyId = "companyId_example" // String | 
let start = 987 // Int | Pagination offset (0, 25, 50, ...) (optional) (default to 0)
let country = "country_example" // String | Residential proxy country (optional) (default to "us")

// Get a company's job postings
LinkedInAPI.linkedinGetACompanySJobPostings(companyId: companyId, start: start, country: country) { (response, error) in
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
 **companyId** | **String** |  | 
 **start** | **Int** | Pagination offset (0, 25, 50, ...) | [optional] [default to 0]
 **country** | **String** | Residential proxy country | [optional] [default to &quot;us&quot;]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **linkedinGetACourse**
```swift
    open class func linkedinGetACourse(courseSlug: String, country: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get a course

A public LinkedIn Learning course — provider, workload, instructors, rating.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let courseSlug = "courseSlug_example" // String | 
let country = "country_example" // String | Residential proxy country (optional) (default to "us")

// Get a course
LinkedInAPI.linkedinGetACourse(courseSlug: courseSlug, country: country) { (response, error) in
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
 **courseSlug** | **String** |  | 
 **country** | **String** | Residential proxy country | [optional] [default to &quot;us&quot;]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **linkedinGetAPublicArticle**
```swift
    open class func linkedinGetAPublicArticle(articleSlug: String, country: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get a public article

A public Pulse article — title, body, author, reactions (JSON-LD).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let articleSlug = "articleSlug_example" // String | 
let country = "country_example" // String | Residential proxy country (optional) (default to "us")

// Get a public article
LinkedInAPI.linkedinGetAPublicArticle(articleSlug: articleSlug, country: country) { (response, error) in
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
 **articleSlug** | **String** |  | 
 **country** | **String** | Residential proxy country | [optional] [default to &quot;us&quot;]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **linkedinGetAPublicPost**
```swift
    open class func linkedinGetAPublicPost(postSlug: String, country: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get a public post

A public activity share — text, author, reactions, comments (JSON-LD).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let postSlug = "postSlug_example" // String | 
let country = "country_example" // String | Residential proxy country (optional) (default to "us")

// Get a public post
LinkedInAPI.linkedinGetAPublicPost(postSlug: postSlug, country: country) { (response, error) in
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
 **postSlug** | **String** |  | 
 **country** | **String** | Residential proxy country | [optional] [default to &quot;us&quot;]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **linkedinGetCompany**
```swift
    open class func linkedinGetCompany(universalName: String, country: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get company

Public company page — industry, size, HQ, followers, specialties (JSON-LD + SSR).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let universalName = "universalName_example" // String | 
let country = "country_example" // String | Residential proxy country (optional) (default to "us")

// Get company
LinkedInAPI.linkedinGetCompany(universalName: universalName, country: country) { (response, error) in
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
 **universalName** | **String** |  | 
 **country** | **String** | Residential proxy country | [optional] [default to &quot;us&quot;]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **linkedinGetJobDetail**
```swift
    open class func linkedinGetJobDetail(jobId: String, country: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get job detail

Full detail for one job posting (guest API, no login).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let jobId = "jobId_example" // String | 
let country = "country_example" // String | Residential proxy country (optional) (default to "us")

// Get job detail
LinkedInAPI.linkedinGetJobDetail(jobId: jobId, country: country) { (response, error) in
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
 **country** | **String** | Residential proxy country | [optional] [default to &quot;us&quot;]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **linkedinGetPublicProfile**
```swift
    open class func linkedinGetPublicProfile(publicId: String, country: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get public profile

Public profile by vanity id (the ``/in/{public_id}`` slug) — name, headline, location, about, experience, education (public JSON-LD + SSR subset).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let publicId = "publicId_example" // String | 
let country = "country_example" // String | Residential proxy country (optional) (default to "us")

// Get public profile
LinkedInAPI.linkedinGetPublicProfile(publicId: publicId, country: country) { (response, error) in
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
 **publicId** | **String** |  | 
 **country** | **String** | Residential proxy country | [optional] [default to &quot;us&quot;]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **linkedinGetSchool**
```swift
    open class func linkedinGetSchool(universalName: String, country: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Get school

Public school page — name, description, website, follower/alumni counts.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let universalName = "universalName_example" // String | 
let country = "country_example" // String | Residential proxy country (optional) (default to "us")

// Get school
LinkedInAPI.linkedinGetSchool(universalName: universalName, country: country) { (response, error) in
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
 **universalName** | **String** |  | 
 **country** | **String** | Residential proxy country | [optional] [default to &quot;us&quot;]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **linkedinLinkedinScraperHealthCheck**
```swift
    open class func linkedinLinkedinScraperHealthCheck(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

LinkedIn scraper health check

Check health of the LinkedIn scraper service (accepts HEAD).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// LinkedIn scraper health check
LinkedInAPI.linkedinLinkedinScraperHealthCheck() { (response, error) in
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

# **linkedinLinkedinScraperHealthCheckHead**
```swift
    open class func linkedinLinkedinScraperHealthCheckHead(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

LinkedIn scraper health check

Check health of the LinkedIn scraper service (accepts HEAD).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// LinkedIn scraper health check
LinkedInAPI.linkedinLinkedinScraperHealthCheckHead() { (response, error) in
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

# **linkedinSearchLinkedinJobs**
```swift
    open class func linkedinSearchLinkedinJobs(keywords: String? = nil, location: String? = nil, geoId: String? = nil, companyId: String? = nil, datePosted: String? = nil, experience: String? = nil, jobType: String? = nil, workplace: String? = nil, sort: String? = nil, start: Int? = nil, country: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Search LinkedIn jobs

Search public LinkedIn job postings (guest API, no login).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let keywords = "keywords_example" // String | Job title / keywords (optional)
let location = "location_example" // String | Location text, e.g. 'New York' (optional)
let geoId = "geoId_example" // String | LinkedIn numeric geo id (overrides location) (optional)
let companyId = "companyId_example" // String | Restrict to a company (numeric id) (optional)
let datePosted = "datePosted_example" // String | past_24h | past_week | past_month | any (optional)
let experience = "experience_example" // String | internship|entry|associate|mid_senior|director|executive (comma-separated) (optional)
let jobType = "jobType_example" // String | full_time|part_time|contract|temporary|internship|volunteer|other (optional)
let workplace = "workplace_example" // String | onsite|remote|hybrid (comma-separated) (optional)
let sort = "sort_example" // String | relevant | recent (optional)
let start = 987 // Int | Pagination offset (0, 25, 50, ...) (optional) (default to 0)
let country = "country_example" // String | Residential proxy country (optional) (default to "us")

// Search LinkedIn jobs
LinkedInAPI.linkedinSearchLinkedinJobs(keywords: keywords, location: location, geoId: geoId, companyId: companyId, datePosted: datePosted, experience: experience, jobType: jobType, workplace: workplace, sort: sort, start: start, country: country) { (response, error) in
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
 **keywords** | **String** | Job title / keywords | [optional] 
 **location** | **String** | Location text, e.g. &#39;New York&#39; | [optional] 
 **geoId** | **String** | LinkedIn numeric geo id (overrides location) | [optional] 
 **companyId** | **String** | Restrict to a company (numeric id) | [optional] 
 **datePosted** | **String** | past_24h | past_week | past_month | any | [optional] 
 **experience** | **String** | internship|entry|associate|mid_senior|director|executive (comma-separated) | [optional] 
 **jobType** | **String** | full_time|part_time|contract|temporary|internship|volunteer|other | [optional] 
 **workplace** | **String** | onsite|remote|hybrid (comma-separated) | [optional] 
 **sort** | **String** | relevant | recent | [optional] 
 **start** | **Int** | Pagination offset (0, 25, 50, ...) | [optional] [default to 0]
 **country** | **String** | Residential proxy country | [optional] [default to &quot;us&quot;]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **linkedinSuggestLocationGeoIds**
```swift
    open class func linkedinSuggestLocationGeoIds(query: String, type: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Suggest location geo ids

Resolve a name to LinkedIn ids (job-search ``geo_id`` / ``company_id`` helper).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let query = "query_example" // String | Location text, e.g. 'London'
let type = "type_example" // String | geo | company (optional) (default to "geo")

// Suggest location geo ids
LinkedInAPI.linkedinSuggestLocationGeoIds(query: query, type: type) { (response, error) in
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
 **query** | **String** | Location text, e.g. &#39;London&#39; | 
 **type** | **String** | geo | company | [optional] [default to &quot;geo&quot;]

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

