# # NewsArticlePatchRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**archived_at** | **int** | not editable for status &#x60;\&quot;Archived\&quot;&#x60;; If not null must be must greater than &#x60;publishedAt&#x60; and in future for status &#x60;\&quot;Draft\&quot;&#x60; and &#x60;\&quot;Published\&quot;&#x60; | [optional]
**author** | **string** |  | [optional]
**header_image** | **string** |  | [optional]
**keyword_ids** | **string[]** |  | [optional]
**linked_project_ids** | **string[]** |  | [optional]
**published_at** | **int** | not editable for status &#x60;\&quot;Published\&quot;&#x60;; If not null must be in future for status &#x60;\&quot;Draft\&quot;&#x60; and in past for status &#x60;\&quot;Archived\&quot;&#x60; | [optional]
**send_notification** | **bool** | value can not be changed for published or archived news | [optional]
**status** | **string** |  | [optional]
**teaser_text** | **string** |  | [optional]
**time_zone** | **string** | IANA Time Zone | [optional]
**title** | **string** |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
