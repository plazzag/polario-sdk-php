# # ProjectPostRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**access** | [**\OpenAPI\Client\Model\ModelAccess**](ModelAccess.md) |  | [optional]
**create_accesses** | [**array<string,\OpenAPI\Client\Model\ModelOperationAccess>**](ModelOperationAccess.md) | property enums: &#x60;\&quot;AppointmentConfig\&quot;&#x60; &#x60;\&quot;Calendar\&quot;&#x60; &#x60;\&quot;CalendarTemplate\&quot;&#x60; &#x60;\&quot;ChatFeed\&quot;&#x60; &#x60;\&quot;Directory\&quot;&#x60; &#x60;\&quot;DirectoryTemplate\&quot;&#x60; &#x60;\&quot;Group\&quot;&#x60; &#x60;\&quot;Location\&quot;&#x60; &#x60;\&quot;LocationMap\&quot;&#x60; &#x60;\&quot;Media\&quot;&#x60; &#x60;\&quot;MediaFolder\&quot;&#x60; &#x60;\&quot;Menu\&quot;&#x60; &#x60;\&quot;News\&quot;&#x60; &#x60;\&quot;Notification\&quot;&#x60; &#x60;\&quot;Page\&quot;&#x60; &#x60;\&quot;Stream\&quot;&#x60;; see route description for additional information; Default for all property enums: &#x60;{\&quot;any\&quot;: \&quot;false\&quot;, \&quot;user\&quot;: \&quot;false\&quot;, \&quot;accounts\&quot;: {}, \&quot;groups\&quot;: {}}&#x60; | [optional]
**description** | **string** |  | [optional]
**featured** | **bool** |  | [optional]
**image** | **string** | currently not translatable | [optional]
**position** | **int** |  | [optional]
**scheme** | **string** | scheme id; Default: &#x60;null&#x60; | [optional]
**status** | **string** |  | [optional]
**time_zone** | **string** | IANA Time Zone | [optional]
**title** | **string** |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
