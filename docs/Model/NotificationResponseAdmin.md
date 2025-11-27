# # NotificationResponseAdmin

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**attachments** | **string[]** | media ids; current implementation is limited for one attachment only and must be MediaTypeDocument; if attachments exceed 15MB they will be not attached in email notification; currently not translatable | [optional]
**content** | **string** |  | [optional]
**created_at** | **int** |  | [optional]
**creator** | **string** | account id | [optional]
**delete_count** | **int** | number of deleted notifications | [optional]
**id** | **string** |  | [optional]
**image** | **string** | media id; currently not translatable | [optional]
**is_published** | **bool** |  | [optional]
**project_id** | **string** |  | [optional]
**published_at** | **int** |  | [optional]
**read_confirmation** | **bool** |  | [optional]
**read_confirmation_text** | **string** | currently not translatable | [optional]
**read_count** | **int** | number of notifications marked as read | [optional]
**recipient_groups** | **string[]** | for empty array recipientGroups do not exist anymore and have to be set again | [optional]
**recipients_count** | **int** | number of recipients | [optional]
**time_zone** | **string** | IANA Time Zone | [optional]
**title** | **string** |  | [optional]
**type** | **string** |  | [optional]
**url** | **string** |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
