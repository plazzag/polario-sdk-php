# # ModelDirectoryListSettings

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**allow_chat** | **bool** |  | [optional]
**field_header_image** | **string** | itemId // item must be Media with subtype Image -&gt; Image for header area of each list item | [optional]
**field_primary** | **string** | itemId // item must be PropertyCreator, TextBlock, TextDateTime, TextMail, TextNumber, TextPhone or TextPlainLine | [optional]
**field_secondary** | **string** | itemId // item must be PropertyCreator, TextDateTime, TextMail, TextNumber, TextPhone, TextPlainLine or null if fieldPrimary is TextBlock | [optional]
**headline_items** | **string[]** | items must be PropertyCreator, TextDateTime, TextNumber or TextPlainLine max 3 items | [optional]
**layout** | **string** | ColumnSingle and ColumnDouble are deprecated and will be removed in 6.0 | [optional]
**order** | **string** | for &#x60;\&quot;Custom\&quot;&#x60; property &#x60;sort\&quot; is used | [optional]
**order_with_highlights** | **bool** |  | [optional]
**share_entries** | **bool** |  | [optional]
**size** | **string** | Default: &#x60;\&quot;S\&quot;&#x60; | [optional]
**sort** | **array<string,string>[]** | only one property per entry allowed; property enums: &#x60;\&quot;createdAt\&quot;&#x60; &#x60;\&quot;id\&quot;&#x60; &#x60;\&quot;lastModified\&quot;&#x60; &#x60;\&quot;position\&quot;&#x60; or &#x60;\&quot;data.{{itemID}}\&quot;&#x60; of subtype TextDateTime, TextNumber or TextPlainLine; value enums: &#x60;\&quot;ASC\&quot;&#x60; &#x60;\&quot;DESC\&quot;&#x60; | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
