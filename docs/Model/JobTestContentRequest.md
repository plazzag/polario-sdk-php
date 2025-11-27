# # JobTestContentRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**attachments** | **string[]** | media ids; currently not translatable | [optional]
**email_body** | **string** |  | [optional]
**email_reply_to** | **string** | currently not translatable | [optional]
**email_sender_name** | **string** | max 100 characters; currently not translatable | [optional]
**language** | **string** | if no language is selected the email will be sent for the default language of the system | [optional]
**preview_line** | **string** | max 90 characters | [optional]
**project_id** | **string** | must be null when &#x60;triggerEvent&#x60; is not null | [optional]
**recipients** | [**\OpenAPI\Client\Model\ModelNotificationRecipients**](ModelNotificationRecipients.md) |  | [optional]
**subject** | **string** | max 255 characters | [optional]
**trigger_cron_topic** | [**\OpenAPI\Client\Model\ModelMailTopic**](ModelMailTopic.md) | must be null when &#x60;triggerEvent&#x60; is not null; must be not null, when &#x60;triggerEvent&#x60; is null | [optional]
**trigger_event** | [**\OpenAPI\Client\Model\ModelMailEvent**](ModelMailEvent.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
