# # AccountnotificationAccountNotification

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**attachments** | **string[]** | media ids; current implementation is limited for one attachment only and must be MediaTypeDocument; if attachments exceed 15MB they will be not attached in email notification; currently not translatable | [optional]
**content** | **string** |  | [optional]
**creator** | **string** | account id | [optional]
**id** | **string** |  | [optional]
**image** | **string** | media id; currently not translatable | [optional]
**is_pruned** | **bool** |  | [optional]
**is_read** | **bool** |  | [optional]
**linked_project_ids** | **string[]** |  | [optional]
**project_id** | **string** |  | [optional]
**published_at** | **int** |  | [optional]
**read_confirmation** | **bool** |  | [optional]
**read_confirmation_text** | **string** | currently not translatable | [optional]
**reference_id** | **string** | articleID for type News, sendbirdChannelURL for type Chat, sendbirdMessageID for type Mention, appointmentID for type Appointment | [optional]
**title** | **string** |  | [optional]
**translations** | [**\OpenAPI\Client\Model\ModelNotificationTranslation[]**](ModelNotificationTranslation.md) |  | [optional]
**type** | **string** |  | [optional]
**url** | **string** |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
