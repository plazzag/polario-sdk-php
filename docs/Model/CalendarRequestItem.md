# # CalendarRequestItem

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**auto_play** | **bool** | only for MediaVideo subtype | [optional]
**download** | **bool** | only for MediaDocument subtype | [optional]
**filter** | [**\OpenAPI\Client\Model\ModelSearch**](ModelSearch.md) | only for PropertyKeyword subtype | [optional]
**icon** | **string** | media id; Default: &#x60;null&#x60; | [optional]
**id** | **string** |  | [optional]
**link_behavior** | **string** | only for TextLink subtype | [optional]
**readonly** | **bool** | user can change value or not | [optional]
**reference_id** | **string** | only for Selection type | [optional]
**required** | **bool** | no effect for type &#x3D; Property | [optional]
**show_map** | **bool** | only for TextAddress subtype | [optional]
**show_title** | **bool** | Default: &#x60;true&#x60; | [optional]
**sub_type** | **string** | subtype must start with type for correct validation process | [optional]
**title** | **string** | the localized name of a calendar item. | [optional]
**type** | **string** |  | [optional]
**zoom_level** | **string** | only for TextAddress subtype | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
