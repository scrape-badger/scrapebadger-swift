# YelpSearchResponse

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**market** | **String** |  | 
**query** | **String** |  | 
**location** | **String** |  | 
**locationResolved** | [**YelpResolvedLocation**](YelpResolvedLocation.md) |  | 
**didYouMean** | **String** |  | [optional] 
**queryMatched** | **Bool** | False when Yelp could not place the query; results are then Yelp&#39;s broader ranking for the location, as Yelp shows them. | 
**totalResults** | **Int** | Yelp&#39;s reported total; at most 110 are browsable. | 
**page** | **Int** |  | 
**pageSize** | **Int** |  | 
**totalPages** | **Int** |  | 
**hasNextPage** | **Bool** |  | 
**nextPage** | **Int** |  | [optional] 
**results** | [YelpBusiness] |  | 
**ads** | [YelpBusiness] |  | 
**filters** | [String: YelpFilterGroup] |  | 
**relatedSearches** | [YelpLink] |  | 
**sourceUrl** | **String** |  | 
**fetchedAt** | **String** |  | 
**fetchedUtc** | **Double** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


