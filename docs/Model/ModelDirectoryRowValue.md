# # ModelDirectoryRowValue

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**address** | [**\OpenAPI\Client\Model\ModelAddress**](ModelAddress.md) | only for TextAddress subtype | [optional]
**item_id** | **string** |  | [optional]
**number** | **float** | only for TextNumber subtype | [optional]
**options** | **string[]** | only for Selection and Media types and ModuleDirectoryContentRows and ModuleLocations subtype // array of ids; for Media it holds additional media ids (value holds default one) | [optional]
**timestamp** | **int** | only for TextDateTime subtype | [optional]
**translations** | [**\OpenAPI\Client\Model\ModelDirectoryRowValueTranslation[]**](ModelDirectoryRowValueTranslation.md) |  | [optional]
**value** | **string** | only for Media types and ModuleDirectory, ModuleStream, TextPlainLine, TextBlock, TextLink, TextMail and TextPhone subtype // For subtype TextBlock it is a html formatted string, following tags are allowed to use: &#x60;\&quot;em\&quot;&#x60; &#x60;\&quot;i\&quot;&#x60; &#x60;\&quot;strong\&quot;&#x60; &#x60;\&quot;b\&quot;&#x60; &#x60;\&quot;u\&quot;&#x60; &#x60;\&quot;ul\&quot;&#x60; &#x60;\&quot;li\&quot;&#x60; &#x60;\&quot;ol\&quot;&#x60; &#x60;\&quot;a\&quot;&#x60; &#x60;\&quot;p\&quot;&#x60; | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
