# # ModelShipAccountData

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**access_read** | **string** | Default for new accounts: &#x60;\&quot;Any\&quot;&#x60; | [optional]
**add_to_groups** | **string[]** | group titles must match regex /^([^,\\s]|[^,\\s][^,]*[^,\\s])$/ | [optional]
**email** | **string** |  | [optional]
**first_name** | **string** |  | [optional]
**image** | **string** | use empty string for removing image | [optional]
**last_name** | **string** |  | [optional]
**mail_language** | **string** | format: IETF BCP 47; for null the email will be sent for the default language of the system | [optional]
**meta** | [**\OpenAPI\Client\Model\ModelAccountMetaData[]**](ModelAccountMetaData.md) |  | [optional]
**own_access** | [**\OpenAPI\Client\Model\ModelOperation**](ModelOperation.md) | Delete (includes) Write (includes) Read | [optional]
**password** | **string** | must be empty if sso is set | [optional]
**product** | **string** | Default: &#x60;\&quot;App\&quot;&#x60; | [optional]
**salutation** | **string** |  | [optional]
**send_mail** | **bool** | Default: &#x60;false&#x60; | [optional]
**sso_identity** | **string** | must be empty if password is set; must be set if ssoProviderId is set; use empty string for removing ssoIdentity | [optional]
**sso_provider_id** | **string** | must be empty if password is set; must be set if ssoIdentity is set; use empty string for removing ssoProviderId | [optional]
**title** | **string** | use empty string for removing title | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
