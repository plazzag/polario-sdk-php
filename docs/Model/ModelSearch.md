# # ModelSearch

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**keyword_ids** | **string[]** | filter for objects with at least one of the provided keywords; use empty array for no keyword filter | [optional]
**object_ids** | **string[]** | filter for objects for provided objectIds; if array is set objectTypes must contain exactly one entry; objectIds must belong to object type set in objectTypes; private items will not be part of the result; use empty array for no type filter | [optional]
**object_types** | **string[]** | filter for objects of provided objectTypes; objectType Group is not indexed; use empty array for no type filter | [optional]
**project_ids** | **string[]** | filter for project available objects; use empty array for no project filter, global objects are always supplied | [optional]
**reference_ids** | **string[]** | filter for objects with at least one of the provided referenceIDs (parents); if array is set objectTypes must contain exactly one of the following entries: CalendarEntry, DirectoryContentRow; use empty array for no type filter | OR filter | [optional]
**search_string** | **string** | filter for objects with provided text; can be empty when either keywordIds, objectIds, objectTypes, projectIds or referenceIds is not empty, else must have min 3 characters; LiveSearch: space separated groups of characters are treated as disjunctive regex group; WordSearch: exact match of whole words, for phrases wrap in escaped double quotes, exclude words by prepending \&quot;-\&quot; | [optional]
**search_type** | **string** | specifies how searchString should be interpreted; use LiveSearch if searchString is empty. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
