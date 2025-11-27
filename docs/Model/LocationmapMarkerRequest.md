# # LocationmapMarkerRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**background_color** | **string** | hexcolor or enum: &#x60;\&quot;backgroundPrimary\&quot;&#x60; &#x60;\&quot;backgroundSecondary\&quot;&#x60; &#x60;\&quot;backgroundTertiary\&quot;&#x60; &#x60;\&quot;border\&quot;&#x60; &#x60;\&quot;contrast\&quot;&#x60; &#x60;\&quot;error\&quot;&#x60; &#x60;\&quot;primary\&quot;&#x60; &#x60;\&quot;secondary\&quot;&#x60; &#x60;\&quot;success\&quot;&#x60; &#x60;\&quot;textPrimary\&quot;&#x60; &#x60;\&quot;textSecondary\&quot;&#x60; | [optional]
**background_color_dark** | **string** | hexcolor or enum: &#x60;\&quot;backgroundPrimary\&quot;&#x60; &#x60;\&quot;backgroundSecondary\&quot;&#x60; &#x60;\&quot;backgroundTertiary\&quot;&#x60; &#x60;\&quot;border\&quot;&#x60; &#x60;\&quot;contrast\&quot;&#x60; &#x60;\&quot;error\&quot;&#x60; &#x60;\&quot;primary\&quot;&#x60; &#x60;\&quot;secondary\&quot;&#x60; &#x60;\&quot;success\&quot;&#x60; &#x60;\&quot;textPrimary\&quot;&#x60; &#x60;\&quot;textSecondary\&quot;&#x60; | [optional]
**color** | **string** | icon or text color; hexcolor or enum: &#x60;\&quot;backgroundPrimary\&quot;&#x60; &#x60;\&quot;backgroundSecondary\&quot;&#x60; &#x60;\&quot;backgroundTertiary\&quot;&#x60; &#x60;\&quot;border\&quot;&#x60; &#x60;\&quot;contrast\&quot;&#x60; &#x60;\&quot;error\&quot;&#x60; &#x60;\&quot;primary\&quot;&#x60; &#x60;\&quot;secondary\&quot;&#x60; &#x60;\&quot;success\&quot;&#x60; &#x60;\&quot;textPrimary\&quot;&#x60; &#x60;\&quot;textSecondary\&quot;&#x60; | [optional]
**color_dark** | **string** | icon or text color; hexcolor or enum: &#x60;\&quot;backgroundPrimary\&quot;&#x60; &#x60;\&quot;backgroundSecondary\&quot;&#x60; &#x60;\&quot;backgroundTertiary\&quot;&#x60; &#x60;\&quot;border\&quot;&#x60; &#x60;\&quot;contrast\&quot;&#x60; &#x60;\&quot;error\&quot;&#x60; &#x60;\&quot;primary\&quot;&#x60; &#x60;\&quot;secondary\&quot;&#x60; &#x60;\&quot;success\&quot;&#x60; &#x60;\&quot;textPrimary\&quot;&#x60; &#x60;\&quot;textSecondary\&quot;&#x60; | [optional]
**coords** | [**\OpenAPI\Client\Model\ModelCoords**](ModelCoords.md) |  | [optional]
**deeplink** | [**\OpenAPI\Client\Model\DeeplinkRequest**](DeeplinkRequest.md) | must be null when url is set | [optional]
**icon** | **string** | media id | [optional]
**id** | **string** | new markers to create do not have an id on request | [optional]
**link_behavior** | **string** |  | [optional]
**order** | **int** | Default: &#x60;0&#x60; | [optional]
**text** | **string** | fallback if no icon is set | [optional]
**title** | **string** |  | [optional]
**url** | **string** | must be null when deeplink is set | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
