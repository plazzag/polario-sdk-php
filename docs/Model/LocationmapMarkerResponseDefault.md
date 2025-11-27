# # LocationmapMarkerResponseDefault

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**background_color** | **string** |  | [optional]
**background_color_dark** | **string** |  | [optional]
**color** | **string** | icon or text color | [optional]
**color_dark** | **string** | icon or text color | [optional]
**coords** | [**\OpenAPI\Client\Model\ModelCoords**](ModelCoords.md) |  | [optional]
**deeplink** | [**\OpenAPI\Client\Model\ModelDeeplinkObject**](ModelDeeplinkObject.md) | must be null when url is set | [optional]
**icon** | **string** | media id | [optional]
**id** | **string** |  | [optional]
**link_behavior** | **string** |  | [optional]
**order** | **int** |  | [optional]
**text** | **string** | fallback if no icon is set | [optional]
**title** | **string** |  | [optional]
**translations** | [**\OpenAPI\Client\Model\LocationmapMapMarkerTranslationResponse[]**](LocationmapMapMarkerTranslationResponse.md) |  | [optional]
**url** | **string** | must be null when deeplink is set | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
