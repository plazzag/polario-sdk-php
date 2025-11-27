# # NewsArticleRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**access** | [**\OpenAPI\Client\Model\ModelAccess**](ModelAccess.md) |  | [optional]
**archived_at** | **int** | must be null for status &#x60;\&quot;Archived\&quot;&#x60;; If not null must be must greater than &#x60;publishedAt&#x60; and in future for status &#x60;\&quot;Draft\&quot;&#x60; and &#x60;\&quot;Published\&quot;&#x60;; Default: &#x60;null&#x60; | [optional]
**author** | **string** |  | [optional]
**content** | [**\OpenAPI\Client\Model\NewsRequestSection[]**](NewsRequestSection.md) |  | [optional]
**header_image** | **string** |  | [optional]
**keyword_ids** | **string[]** |  | [optional]
**linked_project_ids** | **string[]** | Default: &#x60;[]&#x60; | [optional]
**project_id** | **string** |  | [optional]
**published_at** | **int** | must be null for status &#x60;\&quot;Published\&quot;&#x60;; If not null must be in future for status &#x60;\&quot;Draft\&quot;&#x60; and in past for status &#x60;\&quot;Archived\&quot;&#x60; | [optional]
**send_notification** | **bool** | Default: &#x60;true&#x60; | [optional]
**settings** | [**\OpenAPI\Client\Model\ModelArticleSettings**](ModelArticleSettings.md) |  | [optional]
**status** | **string** |  | [optional]
**teaser_text** | **string** |  | [optional]
**time_zone** | **string** | IANA Time Zone | [optional]
**title** | **string** |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
