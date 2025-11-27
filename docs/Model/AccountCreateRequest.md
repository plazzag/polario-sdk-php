# # AccountCreateRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**access** | [**\OpenAPI\Client\Model\ModelAccess**](ModelAccess.md) |  | [optional]
**email** | **string** |  | [optional]
**first_name** | **string** |  | [optional]
**image** | **string** |  | [optional]
**keyword_ids** | **string[]** | Default: &#x60;[]&#x60; | [optional]
**last_name** | **string** |  | [optional]
**meta** | [**\OpenAPI\Client\Model\ModelAccountMetaData[]**](ModelAccountMetaData.md) |  | [optional]
**own_access** | [**\OpenAPI\Client\Model\ModelOperation**](ModelOperation.md) | Delete (includes) Write (includes) Read | [optional]
**password** | **string** | must be empty if sso is set | [optional]
**product** | **string** |  | [optional]
**roles** | [**\OpenAPI\Client\Model\ModelAccountRole[]**](ModelAccountRole.md) | Default: &#x60;[]&#x60; | [optional]
**salutation** | **string** |  | [optional]
**send_mail** | **bool** |  | [optional]
**sso_identity** | **string** | must be empty if password is set; must be set if ssoProviderId is set | [optional]
**sso_provider_id** | **string** | must be empty if password is set; must be set if ssoIdentity is set | [optional]
**title** | **string** |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
