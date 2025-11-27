# # NotificationPatchEmailRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**attachments** | **string[]** | media ids; currently not translatable | [optional]
**email_body** | **string** |  | [optional]
**email_editor_config** | **string** |  | [optional]
**email_reply_to** | **string** | currently not translatable | [optional]
**email_sender_name** | **string** | max 100 characters; currently not translatable | [optional]
**preview_line** | **string** | max 90 characters | [optional]
**published_at** | **int** | 0 &#x3D; now | [optional]
**recipient_groups** | **string[]** | null &#x3D; sent to everyone; group ids must belong to provided project id | [optional]
**subject** | **string** | max 255 characters | [optional]
**time_zone** | **string** | IANA Time Zone | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
