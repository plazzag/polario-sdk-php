# # ModelNotificationTranslation

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**attachments** | **string[]** | media ids; current implementation is limited for one attachment only and must be MediaTypeDocument; if attachments exceed 15MB they will be not attached in email notification; currently not translatable | [optional]
**content** | **string** |  | [optional]
**email_localization** | [**\OpenAPI\Client\Model\ModelNotificationJobLocalization**](ModelNotificationJobLocalization.md) |  | [optional]
**image** | **string** | media id; currently not translatable | [optional]
**lang_key** | **string** |  | [optional]
**read_confirmation_text** | **string** | currently not translatable | [optional]
**title** | **string** |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
