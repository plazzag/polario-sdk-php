# # DirectoryRequestItem

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**allow_multiple** | **int** | only for Media types; data.Options can hold max items specified here; -1 &#x3D; data.Options not limited; null &#x3D; only data.Value can be set: no gallery view; Default: &#x60;null&#x60; | [optional]
**auto_play** | **bool** | only for MediaVideo subtype | [optional]
**creator_name_pattern** | **string** | only for PropertyCreator subtype; \&quot;title\&quot;, \&quot;firstName\&quot; and \&quot;lastName\&quot; will be replaced with account profile values | [optional]
**date_time_format** | **string** | only for TextDateTime subtype | [optional]
**download** | **bool** | only for MediaDocument subtype | [optional]
**filter** | [**\OpenAPI\Client\Model\ModelSearch**](ModelSearch.md) | only for PropertyKeyword subtype | [optional]
**icon** | **string** | media id; Default: &#x60;null&#x60; | [optional]
**id** | **string** |  | [optional]
**link_behavior** | **string** | only for TextLink subtype | [optional]
**readonly** | **bool** | user can change value or not; no effect for directory contentRowObjectType &#x3D; Account | [optional]
**reference** | **string** | only in admin representation and only for directory contentRowObjectType &#x3D; Account and type is not Property; type must match with reference, subtype must not match with reference for type Text. | [optional]
**required** | **bool** | no effect for type &#x3D; Property and directory contentRowObjectType &#x3D; Account | [optional]
**selection_id** | **string** | only for Selection type | [optional]
**show_map** | **bool** | only for TextAddress subtype | [optional]
**show_title** | **bool** | Default: &#x60;true&#x60; | [optional]
**sub_type** | **string** | subtype must start with type for correct validation process; for directory contentRowObjectType &#x3D; Account only MediaImage,SelectionMultipleResponse,SelectionSingleResponse,TextBlock,TextLink,TextMail,TextPhone,TextPlainLine are available | [optional]
**title** | **string** | the localized name of a directory item. | [optional]
**type** | **string** | for directory contentRowObjectType &#x3D; Account only Text,Media,Selection are available | [optional]
**zoom_level** | **string** | only for TextAddress subtype | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
