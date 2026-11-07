# YelpBusiness

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**position** | **Int** | 1-based place in Yelp&#39;s organic order across pages (page 2 starts at 11): Yelp&#39;s own number where it numbers the results; services searches are unnumbered and keep Yelp&#39;s order. For ads, the slot order. | 
**isAd** | **Bool** |  | 
**id** | **String** | Yelp encrypted business ID. | 
**alias** | **String** | Business slug used in /biz/&lt;alias&gt;. | 
**name** | **String** |  | 
**url** | **String** |  | 
**rating** | **Double** |  | [optional] 
**reviewCount** | **Int** |  | [optional] 
**price** | **String** |  | [optional] 
**priceLevel** | **Int** |  | [optional] 
**categories** | [YelpCategory] |  | [optional] 
**neighborhoods** | **[String]** |  | [optional] 
**address** | **String** |  | [optional] 
**city** | **String** |  | [optional] 
**phone** | **String** |  | [optional] 
**timezone** | **String** |  | [optional] 
**openingHours** | [YelpHours] |  | [optional] 
**snippet** | **String** |  | [optional] 
**snippetType** | **String** |  | [optional] 
**highlights** | **[String]** |  | [optional] 
**tags** | **[String]** |  | [optional] 
**photos** | **[String]** |  | [optional] 
**alternateNames** | **[String]** |  | [optional] 
**isServiceAreaBusiness** | **Bool** |  | [optional] 
**isYelpGuaranteed** | **Bool** |  | [optional] 
**hasVerifiedLicense** | **Bool** |  | [optional] 
**adPlacement** | **String** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


