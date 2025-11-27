# # IndexSwagIndexMetaMap

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**author** | **string** | only for Account and News | [optional]
**author_id** | **string** | only for MediaItem | [optional]
**booking_enabled** | **bool** | only for CalendarEntry | [optional]
**date_time** | [**\OpenAPI\Client\Model\ModelDateTime**](ModelDateTime.md) | only for CalendarEntry // Deprecated: will be removed in 6.0 | [optional]
**detail_disabled** | **bool** | only for CalendarEntry | [optional]
**field_primary** | **string** | only for DirectoryContentRow | [optional]
**field_secondary** | **string** | only for DirectoryContentRow | [optional]
**image_mask** | **string** | only for Directory, DirectoryContentRow | [optional]
**interaction** | **bool** | only for News, Page | [optional]
**keyword_ids** | **string[]** |  | [optional]
**linked_objects** | [**\OpenAPI\Client\Model\ModelObjectIdentification[]**](ModelObjectIdentification.md) | currently only Keywords, Locations and MediaImages are linked here | [optional]
**linked_project_ids** | **string[]** | only for News | [optional]
**media_id** | **string** | only for Account, ChatFeed, DirectoryContentRow, Location, News, Project, Stream | [optional]
**mime_type** | **string** | only for MediaItem | [optional]
**private** | **bool** | only for MediaItem | [optional]
**published_at** | **int** | only for CalendarEntry, News | [optional]
**size** | **int** | only for MediaItem | [optional]
**status** | **string** | only for News, Page, Project | [optional]
**teaser_text** | **string** | only for News | [optional]
**time_slot** | [**\OpenAPI\Client\Model\ModelTimeSlot**](ModelTimeSlot.md) | only for CalendarEntry | [optional]
**time_zone** | **string** | only for Project | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
