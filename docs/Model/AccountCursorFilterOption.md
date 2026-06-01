# AccountCursorFilterOption

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**emails** | **string[]** |  | [optional]
**ids** | **string[]** |  | [optional]
**keyword_ids** | **string[]** |  | [optional]
**roles** | **string[]** |  | [optional]
**search_language** | **string** | specifies the language the search string should be interpreted in | [optional]
**search_string** | **string** | must be empty or have at least 3 characters; Default: &#x60;\&quot;\&quot;&#x60; LiveSearch: space separated groups of characters are treated as disjunctive regex group; WordSearch: exact match of whole words, for phrases wrap in escaped double quotes, exclude words by prepending \&quot;-\&quot; | [optional]
**search_type** | **string** | specifies how searchString should be interpreted; Default: &#x60;LiveSearch&#x60; | [optional]
**sso_provider_ids** | **string[]** |  | [optional]
**trackings** | **string[]** |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
