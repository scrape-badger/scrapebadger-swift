# RufusAPI

All URIs are relative to *https://scrapebadger.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**rufusAmazonRufusScraperHealthCheck**](RufusAPI.md#rufusamazonrufusscraperhealthcheck) | **GET** /v1/rufus/health | Amazon Rufus scraper health check
[**rufusAmazonRufusScraperHealthCheckHead**](RufusAPI.md#rufusamazonrufusscraperhealthcheckhead) | **HEAD** /v1/rufus/health | Amazon Rufus scraper health check
[**rufusAskAmazonRufusAQuestion**](RufusAPI.md#rufusaskamazonrufusaquestion) | **GET** /v1/rufus/ask | Ask Amazon Rufus a question
[**rufusAskAmazonRufusAQuestionPost**](RufusAPI.md#rufusaskamazonrufusaquestionpost) | **POST** /v1/rufus/ask | Ask Amazon Rufus a question (POST)
[**rufusListAmazonRufusModels**](RufusAPI.md#rufuslistamazonrufusmodels) | **GET** /v1/rufus/models | List Amazon Rufus models


# **rufusAmazonRufusScraperHealthCheck**
```swift
    open class func rufusAmazonRufusScraperHealthCheck(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Amazon Rufus scraper health check

Check health of the Amazon service that serves Rufus (accepts HEAD).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// Amazon Rufus scraper health check
RufusAPI.rufusAmazonRufusScraperHealthCheck() { (response, error) in
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

# **rufusAmazonRufusScraperHealthCheckHead**
```swift
    open class func rufusAmazonRufusScraperHealthCheckHead(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Amazon Rufus scraper health check

Check health of the Amazon service that serves Rufus (accepts HEAD).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// Amazon Rufus scraper health check
RufusAPI.rufusAmazonRufusScraperHealthCheckHead() { (response, error) in
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

# **rufusAskAmazonRufusAQuestion**
```swift
    open class func rufusAskAmazonRufusAQuestion(prompt: String, asin: String? = nil, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Ask Amazon Rufus a question

Ask Alexa for Shopping (Rufus) and get its answer and product cards.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let prompt = "prompt_example" // String | The shopping question to ask (max 4000 characters).
let asin = "asin_example" // String | Optional product ASIN whose page should provide the shopping context. (optional)

// Ask Amazon Rufus a question
RufusAPI.rufusAskAmazonRufusAQuestion(prompt: prompt, asin: asin) { (response, error) in
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
 **prompt** | **String** | The shopping question to ask (max 4000 characters). | 
 **asin** | **String** | Optional product ASIN whose page should provide the shopping context. | [optional] 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **rufusAskAmazonRufusAQuestionPost**
```swift
    open class func rufusAskAmazonRufusAQuestionPost(rufusAskRequest: RufusAskRequest, completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

Ask Amazon Rufus a question (POST)

POST form of `/ask`, accepting prompt and optional asin in the JSON body.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger

let rufusAskRequest = RufusAskRequest(prompt: "prompt_example", asin: "asin_example") // RufusAskRequest | 

// Ask Amazon Rufus a question (POST)
RufusAPI.rufusAskAmazonRufusAQuestionPost(rufusAskRequest: rufusAskRequest) { (response, error) in
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
 **rufusAskRequest** | [**RufusAskRequest**](RufusAskRequest.md) |  | 

### Return type

**AnyCodable**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **rufusListAmazonRufusModels**
```swift
    open class func rufusListAmazonRufusModels(completion: @escaping (_ data: AnyCodable?, _ error: Error?) -> Void)
```

List Amazon Rufus models

List the Amazon shopping assistant surface exposed by this API.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import ScrapeBadger


// List Amazon Rufus models
RufusAPI.rufusListAmazonRufusModels() { (response, error) in
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

