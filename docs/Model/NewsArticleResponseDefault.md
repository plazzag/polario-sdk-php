# # NewsArticleResponseDefault

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**author** | **string** |  | [optional]
**channel_id** | **string** | the id for sendbird social feed group chat or null if no channel is present or interaction is disabled | [optional]
**content** | [**\OpenAPI\Client\Model\NewsResponseSectionDefault[]**](NewsResponseSectionDefault.md) |  | [optional]
**content_representation** | [**\OpenAPI\Client\Model\NewsPlatform**](NewsPlatform.md) | a web article can contain a 4 column layout | [optional]
**created_at** | **int** |  | [optional]
**has_desktop** | **bool** | indicator if an article has a desktop representation | [optional]
**header_image** | **string** |  | [optional]
**id** | **string** |  | [optional]
**keyword_ids** | **string[]** |  | [optional]
**last_modified** | **int** |  | [optional]
**linked_project_ids** | **string[]** |  | [optional]
**project_id** | **string** | the project id the article belongs to | [optional]
**published_at** | **int** |  | [optional]
**settings** | [**\OpenAPI\Client\Model\NewsResponseSettingsDefault**](NewsResponseSettingsDefault.md) |  | [optional]
**status** | **string** |  | [optional]
**teaser_text** | **string** |  | [optional]
**time_zone** | **string** | IANA Time Zone | [optional]
**title** | **string** |  | [optional]
**translations** | [**\OpenAPI\Client\Model\NewsArticleTranslationResponse[]**](NewsArticleTranslationResponse.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
