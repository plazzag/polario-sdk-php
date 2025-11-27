# # MenuRequestItem

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**access** | [**\OpenAPI\Client\Model\ModelAccess**](ModelAccess.md) | not editable for Profile, Support, Imprint, Settings and LeaveProject type | [optional]
**applied_filter** | [**\OpenAPI\Client\Model\ContentbuilderRequestItemAppliedFilter**](ContentbuilderRequestItemAppliedFilter.md) | only for Link type and deeplink.objectType &#x3D; Calendar | [optional]
**children** | [**\OpenAPI\Client\Model\MenuRequestItem[]**](MenuRequestItem.md) | only for Folder type | [optional]
**deeplink** | [**\OpenAPI\Client\Model\DeeplinkRequest**](DeeplinkRequest.md) | only for Image, Link, Support and Imprint type; must be null when url is set | [optional]
**icon** | **string** | media id only for ChatFeed, Folder, Gallery, IndexSearch, Link, News, Support, Imprint, Settings and LeaveProject type | [optional]
**id** | **string** | new items to create do not have an id (null) | [optional]
**image** | **string** | media id only for Image type | [optional]
**link_behavior** | **string** | only for Image, Link, Support, Imprint and Settings type; Has no effect if the url matches with the web app | [optional]
**platforms** | **string[]** | platforms menu item should be visible for | [optional]
**reference_ids** | **string[]** | only for ChatFeed and Gallery type | [optional]
**search** | [**\OpenAPI\Client\Model\ModelSearch**](ModelSearch.md) | only for IndexSearch and News type | [optional]
**separator_type** | **string** | only for Separator type | [optional]
**size** | **string** | only for Gap type | [optional]
**text** | **string** | only for ChatFeed, Folder, Gallery, IndexSearch, Link, News, Separator, Support, Imprint, Settings and LeaveProject type | [optional]
**text_orientation** | **string** | only for Separator type | [optional]
**type** | **string** |  | [optional]
**url** | **string** | only for Image, Link, Support, Imprint and Settings type; must be null if deeplink is set | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
