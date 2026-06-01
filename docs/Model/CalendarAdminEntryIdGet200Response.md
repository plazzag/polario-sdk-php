# CalendarAdminEntryIdGet200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**access** | [**\OpenAPI\Client\Model\ModelAccess**](ModelAccess.md) | part 1 from authorization.AccessResponse | [optional]
**access_edit_allowed** | **bool** | part 2 from authorization.AccessResponse | [optional]
**booking_enabled** | **bool** |  | [optional]
**calendar_id** | **string** |  | [optional]
**data_set** | [**array<string,\OpenAPI\Client\Model\ContentEntryValueResponse>**](ContentEntryValueResponse.md) |  | [optional]
**date_time** | [**\OpenAPI\Client\Model\ContentEntryDateTimeResponse**](ContentEntryDateTimeResponse.md) | applies to the project time zone | [optional]
**detail_disabled** | **bool** |  | [optional]
**end** | **int** |  | [optional]
**external_id** | **string** |  | [optional]
**external_party** | **string** |  | [optional]
**id** | **string** |  | [optional]
**is_appointment** | **bool** |  | [optional]
**keyword_ids** | **string[]** |  | [optional]
**parent_id** | **string** |  | [optional]
**position** | **int** |  | [optional]
**project_id** | **string** |  | [optional]
**published_at** | **int** |  | [optional]
**rating_enabled** | **bool** |  | [optional]
**rating_result** | **int[]** | [0,0,0,0,0] &#x3D; [Amount1StarRatings, Amount2StarRatings, ...], redundant data SSOT is model.Rating | [optional]
**start** | **int** |  | [optional]
**tabs** | [**\OpenAPI\Client\Model\ContentEntryTabResponse[]**](ContentEntryTabResponse.md) |  | [optional]
**time_zone** | **string** | IANA Time Zone | [optional]
**title** | **string** |  | [optional]
**translations** | [**\OpenAPI\Client\Model\ContentEntryTranslation[]**](ContentEntryTranslation.md) |  | [optional]
**widgets** | [**array<string,\OpenAPI\Client\Model\ContentbuilderSwagResponseItemAdmin>**](ContentbuilderSwagResponseItemAdmin.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
