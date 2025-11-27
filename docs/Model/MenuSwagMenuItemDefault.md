# # MenuSwagMenuItemDefault

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**applied_filter** | [**\OpenAPI\Client\Model\ContentbuilderSwagResponseItemAppliedFilter**](ContentbuilderSwagResponseItemAppliedFilter.md) | only for Link type and deeplink.objectType &#x3D; Calendar | [optional]
**children** | [**\OpenAPI\Client\Model\MenuSwagMenuItemDefault[]**](MenuSwagMenuItemDefault.md) | only for Folder type | [optional]
**deeplink** | [**\OpenAPI\Client\Model\ModelDeeplinkObject**](ModelDeeplinkObject.md) | only for Image, Link, Support and Imprint type | [optional]
**icon** | **string** | media id only for ChatFeed, Folder, Gallery, IndexSearch, Link, News, Support, Imprint, Settings and LeaveProject type | [optional]
**id** | **string** |  | [optional]
**image** | **string** | media id only for Image type | [optional]
**link_behavior** | **string** | only for Image, Link, Support, Imprint and Settings type; Has no effect if the url matches with the web app | [optional]
**reference_ids** | **string[]** | only for ChatFeed and Gallery type | [optional]
**search** | [**\OpenAPI\Client\Model\ModelSearch**](ModelSearch.md) | only for IndexSearch type and News type | [optional]
**separator_type** | **string** | only for Separator type | [optional]
**size** | **string** | only for Gap type | [optional]
**text** | **string** | only for ChatFeed, Folder, Gallery, IndexSearch, Link, News, Separator, Support, Imprint, Settings and LeaveProject type | [optional]
**text_orientation** | **string** | only for Separator type | [optional]
**translations** | [**\OpenAPI\Client\Model\MenuItemTranslationResponse[]**](MenuItemTranslationResponse.md) | only for ChatFeed, Folder, Gallery, IndexSearch, Link, News, Separator, Support, Imprint, Settings and LeaveProject type | [optional]
**type** | **string** |  | [optional]
**url** | **string** | only for ChatFeed, Gallery, Image, IndexSearch, Link, News, Support, Imprint and Settings type; if deeplink is set url has value of deeplink.deeplinkUrl | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
