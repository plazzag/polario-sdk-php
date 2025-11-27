# # NotificationPatchNotificationRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**attachments** | **string[]** | media ids; current implementation is limited for one attachment only and must be MediaTypeDocument; if attachments exceed 15MB they will be not attached in email notification; currently not translatable | [optional]
**content** | **string** |  | [optional]
**image** | **string** | media id; currently not translatable | [optional]
**published_at** | **int** | 0 &#x3D; now | [optional]
**read_confirmation** | **bool** |  | [optional]
**read_confirmation_text** | **string** | currently not translatable | [optional]
**recipient_groups** | **string[]** | null &#x3D; sent to everyone; group ids must belong to provided project id | [optional]
**time_zone** | **string** | IANA Time Zone | [optional]
**title** | **string** |  | [optional]
**url** | **string** |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
