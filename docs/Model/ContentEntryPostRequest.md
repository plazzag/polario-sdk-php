# # ContentEntryPostRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**access** | [**\OpenAPI\Client\Model\ModelAccess**](ModelAccess.md) |  | [optional]
**booking_enabled** | **bool** | bookingEnabled can only be true if externalId is not null; Default: &#x60;false&#x60; | [optional]
**data_set** | [**array<string,\OpenAPI\Client\Model\ContentEntryValueRequest>**](ContentEntryValueRequest.md) |  | [optional]
**end** | **int** |  | [optional]
**external_id** | **string** | externalParty must be set if externalId is set; Default: &#x60;null&#x60; | [optional]
**external_party** | **string** | Default: &#x60;null&#x60; | [optional]
**id** | **string** |  | [optional]
**keyword_ids** | **string[]** |  | [optional]
**parent_id** | **string** |  | [optional]
**position** | **int** |  | [optional]
**published_at** | **int** |  | [optional]
**start** | **int** |  | [optional]
**tabs** | [**\OpenAPI\Client\Model\ContentEntryTabRequest[]**](ContentEntryTabRequest.md) |  | [optional]
**time_zone** | **string** | IANA Time Zone | [optional]
**title** | **string** |  | [optional]
**widgets** | [**array<string,\OpenAPI\Client\Model\ContentbuilderRequestItem>**](ContentbuilderRequestItem.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
