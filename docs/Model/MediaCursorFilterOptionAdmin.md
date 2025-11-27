# # MediaCursorFilterOptionAdmin

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**folder_ids** | **string[]** | filter values can hold null to be filtered for global elements as well. | [optional]
**ids** | **string[]** |  | [optional]
**media_types** | **string[]** |  | [optional]
**mime_type** | **string[]** |  | [optional]
**project_ids** | **string[]** | global objects are always supplied | [optional]
**search_string** | **string** | must be empty or have at least 3 characters; Default: &#x60;\&quot;\&quot;&#x60; LiveSearch: space separated groups of characters are treated as disjunctive regex group; WordSearch: exact match of whole words, for phrases wrap in escaped double quotes, exclude words by prepending \&quot;-\&quot; | [optional]
**search_type** | **string** | specifies how searchString should be interpreted; Default: &#x60;LiveSearch&#x60; | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
