# # ContentEntryValueRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**address** | [**\OpenAPI\Client\Model\ModelAddress**](ModelAddress.md) | only for TextAddress subtype | [optional]
**deeplink** | [**\OpenAPI\Client\Model\DeeplinkRequest**](DeeplinkRequest.md) | only for MediaImage subtype; must be null when url is set; Default: &#x60;null&#x60; | [optional]
**item_id** | **string** |  | [optional]
**link_behavior** | **string** | only for MediaImage subtype; Default: &#x60;null&#x60; | [optional]
**options** | **string[]** | only for Selection types and ModuleDirectoryContentRows and ModuleLocations subtype // array of ids | [optional]
**url** | **string** | only for MediaImage subtype; must be null when deeplink is set; Default: &#x60;null&#x60; | [optional]
**value** | **string** | only for Media types and ModuleDirectory, ModuleStream, TextPlainLine, TextBlock, TextLink, TextMail and TextPhone subtype // For subtype TextBlock it is a html formatted string, following tags are allowed to use: &#x60;\&quot;em\&quot;&#x60; &#x60;\&quot;i\&quot;&#x60; &#x60;\&quot;strong\&quot;&#x60; &#x60;\&quot;b\&quot;&#x60; &#x60;\&quot;u\&quot;&#x60; &#x60;\&quot;ul\&quot;&#x60; &#x60;\&quot;li\&quot;&#x60; &#x60;\&quot;ol\&quot;&#x60; &#x60;\&quot;a\&quot;&#x60; &#x60;\&quot;p\&quot;&#x60; | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
