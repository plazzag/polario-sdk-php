# # JobResponseAdmin

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**attachments** | **string[]** | media ids; currently not translatable | [optional]
**email_body** | **string** |  | [optional]
**email_editor_config** | **string** |  | [optional]
**email_reply_to** | **string** | currently not translatable | [optional]
**email_sender_address** | **string** |  | [optional]
**email_sender_name** | **string** | max 100 characters; currently not translatable | [optional]
**enabled** | **bool** | false, when trigger event could currently not be triggered regarding config, etc. | [optional]
**id** | **string** |  | [optional]
**is_customized** | **bool** |  | [optional]
**is_system** | **bool** |  | [optional]
**preview_line** | **string** | max 90 characters | [optional]
**project_id** | **string** |  | [optional]
**recipients** | [**\OpenAPI\Client\Model\ModelNotificationRecipients**](ModelNotificationRecipients.md) |  | [optional]
**status** | **string** |  | [optional]
**subject** | **string** | max 255 characters | [optional]
**title** | **string** |  | [optional]
**trigger_cron** | **string** | format: &#x60;\&quot;* * * * *\&quot;&#x60; | [optional]
**trigger_cron_topic** | [**\OpenAPI\Client\Model\ModelMailTopic**](ModelMailTopic.md) |  | [optional]
**trigger_event** | [**\OpenAPI\Client\Model\ModelMailEvent**](ModelMailEvent.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
