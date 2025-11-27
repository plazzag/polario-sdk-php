# # DirectoryAdminPost200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**access** | [**\OpenAPI\Client\Model\ModelAccess**](ModelAccess.md) |  | [optional]
**access_edit_allowed** | **bool** |  | [optional]
**content_row_filter** | [**\OpenAPI\Client\Model\ModelSearch**](ModelSearch.md) | only reflects for dynamic directory (contentRowObjectType !&#x3D; null) | [optional]
**content_row_object_type** | [**\OpenAPI\Client\Model\ModelObjectType**](ModelObjectType.md) | null &#x3D; static directory | [optional]
**content_rows_count** | **int** | number of directory entries; access status will be ignored for counting; null &#x3D; not counted | [optional]
**create_accesses** | [**array<string,\OpenAPI\Client\Model\ModelOperationAccess>**](ModelOperationAccess.md) | property enums: &#x60;\&quot;CalendarEntry\&quot;&#x60; | [optional]
**description** | **string** |  | [optional]
**detail** | [**\OpenAPI\Client\Model\DirectoryResponseDetailModelPart**](DirectoryResponseDetailModelPart.md) |  | [optional]
**id** | **string** |  | [optional]
**is_system** | **bool** |  | [optional]
**items** | [**\OpenAPI\Client\Model\DirectorySwagResponseDirectoryItem[]**](DirectorySwagResponseDirectoryItem.md) |  | [optional]
**list_settings** | [**\OpenAPI\Client\Model\ModelDirectoryListSettings**](ModelDirectoryListSettings.md) |  | [optional]
**project_id** | **string** |  | [optional]
**selections** | [**\OpenAPI\Client\Model\SelectionAPIResponseAdmin[]**](SelectionAPIResponseAdmin.md) |  | [optional]
**title** | **string** | the localized name of the directory | [optional]
**type** | **string** |  | [optional]
**type_reference_id** | **string** |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
