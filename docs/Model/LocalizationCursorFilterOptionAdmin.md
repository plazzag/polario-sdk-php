# # LocalizationCursorFilterOptionAdmin

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ids** | **string[]** |  | [optional]
**is_customized** | **bool[]** |  | [optional]
**is_deprecated** | **bool[]** |  | [optional]
**keys** | **string[]** |  | [optional]
**lang_codes** | **string[]** |  | [optional]
**search_string** | **string** | must be empty or have at least 3 characters; Default: &#x60;\&quot;\&quot;&#x60; LiveSearch: space separated groups of characters are treated as disjunctive regex group; WordSearch: exact match of whole words, for phrases wrap in escaped double quotes, exclude words by prepending \&quot;-\&quot; | [optional]
**search_type** | **string** | specifies how searchString should be interpreted; Default: &#x60;LiveSearch&#x60; | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
