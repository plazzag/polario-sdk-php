# # JobResponseListAdmin

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**enabled** | **bool** | false, when trigger event could currently not be triggered regarding config, etc. | [optional]
**id** | **string** |  | [optional]
**is_system** | **bool** |  | [optional]
**preview_line** | **string** |  | [optional]
**project_id** | **string** |  | [optional]
**recipients** | [**\OpenAPI\Client\Model\ModelNotificationRecipients**](ModelNotificationRecipients.md) |  | [optional]
**status** | **string** |  | [optional]
**subject** | **string** |  | [optional]
**title** | **string** |  | [optional]
**trigger_cron** | **string** | format: &#x60;\&quot;* * * * *\&quot;&#x60; | [optional]
**trigger_cron_topic** | [**\OpenAPI\Client\Model\ModelMailTopic**](ModelMailTopic.md) |  | [optional]
**trigger_event** | [**\OpenAPI\Client\Model\ModelMailEvent**](ModelMailEvent.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
