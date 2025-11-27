# OpenAPI\Client\AccountApi



All URIs are relative to https://custom.polario.de/api, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**authAccountAnalyticsAccountSettingsGet()**](AccountApi.md#authAccountAnalyticsAccountSettingsGet) | **GET** /auth/account/analytics/account-settings | Get account settings analytics for cursor |
| [**authAccountAnalyticsAccountSettingsSearchPost()**](AccountApi.md#authAccountAnalyticsAccountSettingsSearchPost) | **POST** /auth/account/analytics/account-settings/search | Create account settings analytics cursor |
| [**authAccountColorGet()**](AccountApi.md#authAccountColorGet) | **GET** /auth/account/color | account colors |
| [**authAccountDelete()**](AccountApi.md#authAccountDelete) | **DELETE** /auth/account | Delete accounts |
| [**authAccountDeleteOwnPost()**](AccountApi.md#authAccountDeleteOwnPost) | **POST** /auth/account/delete-own | Delete own |
| [**authAccountGet()**](AccountApi.md#authAccountGet) | **GET** /auth/account | Get accounts |
| [**authAccountIdAccessGet()**](AccountApi.md#authAccountIdAccessGet) | **GET** /auth/account/{id}/access | Get account access configuration |
| [**authAccountIdAccessPatch()**](AccountApi.md#authAccountIdAccessPatch) | **PATCH** /auth/account/{id}/access | Update account access configuration |
| [**authAccountIdCredentialsPatch()**](AccountApi.md#authAccountIdCredentialsPatch) | **PATCH** /auth/account/{id}/credentials | Update account credentials |
| [**authAccountIdDelete()**](AccountApi.md#authAccountIdDelete) | **DELETE** /auth/account/{id} | Delete account |
| [**authAccountIdDeviceDeviceIdLogoutGet()**](AccountApi.md#authAccountIdDeviceDeviceIdLogoutGet) | **GET** /auth/account/{id}/device/{deviceId}/logout | Logout device |
| [**authAccountIdDeviceGet()**](AccountApi.md#authAccountIdDeviceGet) | **GET** /auth/account/{id}/device | Get account devices |
| [**authAccountIdGet()**](AccountApi.md#authAccountIdGet) | **GET** /auth/account/{id} | Get account |
| [**authAccountIdGroupProjectProjectIdGet()**](AccountApi.md#authAccountIdGroupProjectProjectIdGet) | **GET** /auth/account/{id}/group/project/{projectId} | Get group list for account for project |
| [**authAccountIdGroupProjectProjectIdPut()**](AccountApi.md#authAccountIdGroupProjectProjectIdPut) | **PUT** /auth/account/{id}/group/project/{projectId} | Update account groups membership for project |
| [**authAccountIdPermissionGet()**](AccountApi.md#authAccountIdPermissionGet) | **GET** /auth/account/{id}/permission | Get account permissions |
| [**authAccountIdProfileGet()**](AccountApi.md#authAccountIdProfileGet) | **GET** /auth/account/{id}/profile | Get account profile |
| [**authAccountIdProfilePatch()**](AccountApi.md#authAccountIdProfilePatch) | **PATCH** /auth/account/{id}/profile | Update account profile |
| [**authAccountIdProjectProjectIdVisitPut()**](AccountApi.md#authAccountIdProjectProjectIdVisitPut) | **PUT** /auth/account/{id}/project/{projectId}/visit | Account entered project first time |
| [**authAccountIdPushDelete()**](AccountApi.md#authAccountIdPushDelete) | **DELETE** /auth/account/{id}/push | Remove push token |
| [**authAccountIdPushGet()**](AccountApi.md#authAccountIdPushGet) | **GET** /auth/account/{id}/push | Get push token |
| [**authAccountIdPushPut()**](AccountApi.md#authAccountIdPushPut) | **PUT** /auth/account/{id}/push | Set push token |
| [**authAccountIdRolesGet()**](AccountApi.md#authAccountIdRolesGet) | **GET** /auth/account/{id}/roles | Get roles of an account |
| [**authAccountIdRolesPut()**](AccountApi.md#authAccountIdRolesPut) | **PUT** /auth/account/{id}/roles | Update the roles of an account |
| [**authAccountIdSettingsGet()**](AccountApi.md#authAccountIdSettingsGet) | **GET** /auth/account/{id}/settings | Get account settings |
| [**authAccountIdSettingsNotificationGet()**](AccountApi.md#authAccountIdSettingsNotificationGet) | **GET** /auth/account/{id}/settings/notification | Get account notification settings |
| [**authAccountIdSettingsNotificationPatch()**](AccountApi.md#authAccountIdSettingsNotificationPatch) | **PATCH** /auth/account/{id}/settings/notification | Update account notification settings |
| [**authAccountIdSettingsProjectProjectIdGet()**](AccountApi.md#authAccountIdSettingsProjectProjectIdGet) | **GET** /auth/account/{id}/settings/project/{projectId} | Get account project settings |
| [**authAccountIdSettingsProjectProjectIdPatch()**](AccountApi.md#authAccountIdSettingsProjectProjectIdPatch) | **PATCH** /auth/account/{id}/settings/project/{projectId} | Update account project settings |
| [**authAccountIdSettingsTrackingGet()**](AccountApi.md#authAccountIdSettingsTrackingGet) | **GET** /auth/account/{id}/settings/tracking | Get account tracking settings |
| [**authAccountIdSettingsTrackingPut()**](AccountApi.md#authAccountIdSettingsTrackingPut) | **PUT** /auth/account/{id}/settings/tracking | Update account tracking settings |
| [**authAccountIdSettingsVisibilityGet()**](AccountApi.md#authAccountIdSettingsVisibilityGet) | **GET** /auth/account/{id}/settings/visibility | Get account visibility settings |
| [**authAccountIdSettingsVisibilityPatch()**](AccountApi.md#authAccountIdSettingsVisibilityPatch) | **PATCH** /auth/account/{id}/settings/visibility | Update account visibility settings |
| [**authAccountMetaGet()**](AccountApi.md#authAccountMetaGet) | **GET** /auth/account-meta | Get meta item setup |
| [**authAccountMetaPut()**](AccountApi.md#authAccountMetaPut) | **PUT** /auth/account-meta | Update meta item setup |
| [**authAccountPost()**](AccountApi.md#authAccountPost) | **POST** /auth/account | Create account |
| [**authAccountProjectProjectIdIdGet()**](AccountApi.md#authAccountProjectProjectIdIdGet) | **GET** /auth/account/project/{projectId}/id | Get project account ids |
| [**authAccountProjectProjectIdStatsGet()**](AccountApi.md#authAccountProjectProjectIdStatsGet) | **GET** /auth/account/project/{projectId}/stats | Get project accounts statistics |
| [**authAccountProjectProjectIdStatsRecordGet()**](AccountApi.md#authAccountProjectProjectIdStatsRecordGet) | **GET** /auth/account/project/{projectId}/stats/record | Get project accounts statistic records |
| [**authAccountSearchPost()**](AccountApi.md#authAccountSearchPost) | **POST** /auth/account/search | Search accounts |
| [**authAccountStatsGet()**](AccountApi.md#authAccountStatsGet) | **GET** /auth/account/stats | Get accounts statistics |
| [**authAccountStatsRecordGet()**](AccountApi.md#authAccountStatsRecordGet) | **GET** /auth/account/stats/record | Get accounts statistic records |
| [**authEmailPost()**](AccountApi.md#authEmailPost) | **POST** /auth/email | Change email first |
| [**authEmailPut()**](AccountApi.md#authEmailPut) | **PUT** /auth/email | Change email final |
| [**authPasswordChangePost()**](AccountApi.md#authPasswordChangePost) | **POST** /auth/password/change | Request password change |
| [**authPasswordPut()**](AccountApi.md#authPasswordPut) | **PUT** /auth/password | Change Password |
| [**authPasswordRecoverPost()**](AccountApi.md#authPasswordRecoverPost) | **POST** /auth/password/recover | Recover Password |
| [**authRegisterPost()**](AccountApi.md#authRegisterPost) | **POST** /auth/register | Registration |


## `authAccountAnalyticsAccountSettingsGet()`

```php
authAccountAnalyticsAccountSettingsGet($cursor, $page, $session, $limit): \OpenAPI\Client\Model\AnalyticsAccountSettingsRecord[]
```

Get account settings analytics for cursor

This endpoint returns a list of all accounts settings analytics snapshot records for a cursor in administrative representation.  Cursor could be created here: POST /auth/account/analytics/account-settings/search  _accessible without permission_

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$cursor = 'cursor_example'; // string | id of the cursor used for pagination; required if page is set
$page = 56; // int | current page index of the cursor used for pagination; required if cursor is set
$session = 'session_example'; // string | JWT
$limit = 56; // int | amount of results per page (1 ... 100)

try {
    $result = $apiInstance->authAccountAnalyticsAccountSettingsGet($cursor, $page, $session, $limit);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->authAccountAnalyticsAccountSettingsGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **cursor** | **string**| id of the cursor used for pagination; required if page is set | |
| **page** | **int**| current page index of the cursor used for pagination; required if cursor is set | |
| **session** | **string**| JWT | |
| **limit** | **int**| amount of results per page (1 ... 100) | [optional] |

### Return type

[**\OpenAPI\Client\Model\AnalyticsAccountSettingsRecord[]**](../Model/AnalyticsAccountSettingsRecord.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `authAccountAnalyticsAccountSettingsSearchPost()`

```php
authAccountAnalyticsAccountSettingsSearchPost($session, $request): \OpenAPI\Client\Model\ModelCursorResponse
```

Create account settings analytics cursor

This endpoint returns a cursor for list account settings snapshot records with applied filter and sort options. In case of cursor response total will be 0 the status 204 with not content is returned instead.  _only accessible with permission_ : `\"ManageAccounts\"` `\"ManageConfiguration\"` `\"ManageContent\"` `\"ManageProjects\"` `\"ViewAnalytics\"` `\"ViewGlobalAnalytics\"`  _fully accessible with permission_ : `\"ManageAccounts\"` `\"ManageConfiguration\"` `\"ManageContent\"` `\"ManageProjects\"` `\"ViewAnalytics\"` `\"ViewGlobalAnalytics\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\AnalyticsCursorRequest(); // \OpenAPI\Client\Model\AnalyticsCursorRequest | options to create cursor

try {
    $result = $apiInstance->authAccountAnalyticsAccountSettingsSearchPost($session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->authAccountAnalyticsAccountSettingsSearchPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\AnalyticsCursorRequest**](../Model/AnalyticsCursorRequest.md)| options to create cursor | |

### Return type

[**\OpenAPI\Client\Model\ModelCursorResponse**](../Model/ModelCursorResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `authAccountColorGet()`

```php
authAccountColorGet($session): \OpenAPI\Client\Model\ModelAccountProfileColor[]
```

account colors

This endpoint is for requesting available account profile colors.  _accessible without permission_

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->authAccountColorGet($session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->authAccountColorGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **session** | **string**| JWT | |

### Return type

[**\OpenAPI\Client\Model\ModelAccountProfileColor[]**](../Model/ModelAccountProfileColor.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `authAccountDelete()`

```php
authAccountDelete($ids, $session): \OpenAPI\Client\Model\ModelSwagStatusOk
```

Delete accounts

This endpoint is for deleting multiple accounts from the system.  _only accessible with permission_ : `\"ManageAccounts\"`  _fully accessible with permission_ : `\"ManageAccounts\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$ids = 'ids_example'; // string | ids to delete
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->authAccountDelete($ids, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->authAccountDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **ids** | **string**| ids to delete | |
| **session** | **string**| JWT | |

### Return type

[**\OpenAPI\Client\Model\ModelSwagStatusOk**](../Model/ModelSwagStatusOk.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `authAccountDeleteOwnPost()`

```php
authAccountDeleteOwnPost($request, $platform): \OpenAPI\Client\Model\AuthServerSignatureResponse
```

Delete own

This endpoint is for deleting an account with the correct password. This endpoint uses the final message of the SCRAM challenge to validate the password. The Platform must match the Platform from the first message. See RFC 5802 for detail SCRAM definition.  To perform this action call SCRAM First first: POST /auth/auth  _accessible without permission_

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$request = new \OpenAPI\Client\Model\AuthScramFinalRequest(); // \OpenAPI\Client\Model\AuthScramFinalRequest | Clients Final Message
$platform = 'platform_example'; // string | The client platform

try {
    $result = $apiInstance->authAccountDeleteOwnPost($request, $platform);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->authAccountDeleteOwnPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **request** | [**\OpenAPI\Client\Model\AuthScramFinalRequest**](../Model/AuthScramFinalRequest.md)| Clients Final Message | |
| **platform** | **string**| The client platform | [optional] |

### Return type

[**\OpenAPI\Client\Model\AuthServerSignatureResponse**](../Model/AuthServerSignatureResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `authAccountGet()`

```php
authAccountGet($session, $cursor, $limit, $page, $accept_language, $platform): \OpenAPI\Client\Model\AccountResponse[]
```

Get accounts

This endpoint is for requesting account list of the system. If a limit is set, a cursor for this endpoint may be created to iterate over all accounts. If _Platform_ header is `\"Cms\"` _Accept-Language_ header will be ignored.  _only accessible with permission_ : `\"ManageAccounts\"`  _fully accessible with permission_ : `\"ManageAccounts\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT
$cursor = 'cursor_example'; // string | id of the cursor used for pagination; required if page is set
$limit = 56; // int | amount of results per page (1 ... 100)
$page = 56; // int | current page index of the cursor used for pagination; required if cursor is set
$accept_language = 'accept_language_example'; // string | client language(s)
$platform = 'platform_example'; // string | The client platform

try {
    $result = $apiInstance->authAccountGet($session, $cursor, $limit, $page, $accept_language, $platform);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->authAccountGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **session** | **string**| JWT | |
| **cursor** | **string**| id of the cursor used for pagination; required if page is set | [optional] |
| **limit** | **int**| amount of results per page (1 ... 100) | [optional] |
| **page** | **int**| current page index of the cursor used for pagination; required if cursor is set | [optional] |
| **accept_language** | **string**| client language(s) | [optional] |
| **platform** | **string**| The client platform | [optional] |

### Return type

[**\OpenAPI\Client\Model\AccountResponse[]**](../Model/AccountResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `authAccountIdAccessGet()`

```php
authAccountIdAccessGet($id, $session): \OpenAPI\Client\Model\AuthorizationAccessResponse
```

Get account access configuration

This endpoint returns the access configuration for the requested account.  _only accessible with permission_ : `\"ManageAccounts\"`  _fully accessible with permission_ : `\"ManageAccounts\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Account ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->authAccountIdAccessGet($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->authAccountIdAccessGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Account ID | |
| **session** | **string**| JWT | |

### Return type

[**\OpenAPI\Client\Model\AuthorizationAccessResponse**](../Model/AuthorizationAccessResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `authAccountIdAccessPatch()`

```php
authAccountIdAccessPatch($id, $session, $request): \OpenAPI\Client\Model\ModelAccess
```

Update account access configuration

This endpoint updates the access configuration for the requested account. Only the changes should be transmitted due this endpoint.  _only accessible with permission_ : `\"ManageAccounts\"`  _fully accessible with permission_ : `\"ManageAccounts\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Account ID
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\ModelAccess(); // \OpenAPI\Client\Model\ModelAccess | changed access rights

try {
    $result = $apiInstance->authAccountIdAccessPatch($id, $session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->authAccountIdAccessPatch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Account ID | |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\ModelAccess**](../Model/ModelAccess.md)| changed access rights | |

### Return type

[**\OpenAPI\Client\Model\ModelAccess**](../Model/ModelAccess.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `authAccountIdCredentialsPatch()`

```php
authAccountIdCredentialsPatch($id, $session, $request): \OpenAPI\Client\Model\ModelSwagStatusOk
```

Update account credentials

This endpoint is for updating account credential information without the SCRAM flow. Credentials cannot be changed for an accounts that is linked to a sso provider. If an email address is provided, a password must also be provided. (Because of SCRAM the email address can only be changed by providing a password.) User has to login again after credentials change.  _only accessible with permission_ : `\"ManageAccounts\"`  _fully accessible with permission_ : `\"ManageAccounts\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Account ID
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\AccountPatchCredentialsRequest(); // \OpenAPI\Client\Model\AccountPatchCredentialsRequest | new credentials

try {
    $result = $apiInstance->authAccountIdCredentialsPatch($id, $session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->authAccountIdCredentialsPatch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Account ID | |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\AccountPatchCredentialsRequest**](../Model/AccountPatchCredentialsRequest.md)| new credentials | |

### Return type

[**\OpenAPI\Client\Model\ModelSwagStatusOk**](../Model/ModelSwagStatusOk.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `authAccountIdDelete()`

```php
authAccountIdDelete($id, $session): \OpenAPI\Client\Model\ModelSwagStatusOk
```

Delete account

This endpoint is for deleting a single account.  For deletion of own account via frontend see: POST /auth/account/delete-own  _only accessible with permission_ : `\"ManageAccounts\"`  _fully accessible with permission_ : `\"ManageAccounts\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Account ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->authAccountIdDelete($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->authAccountIdDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Account ID | |
| **session** | **string**| JWT | |

### Return type

[**\OpenAPI\Client\Model\ModelSwagStatusOk**](../Model/ModelSwagStatusOk.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `authAccountIdDeviceDeviceIdLogoutGet()`

```php
authAccountIdDeviceDeviceIdLogoutGet($id, $device_id, $session): \OpenAPI\Client\Model\ModelSwagStatusOk
```

Logout device

This endpoint is for account device logout.  _accessible without permission_ (can only be used for the own account. Session must match requested account id.)

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Account ID
$device_id = 'device_id_example'; // string | Device ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->authAccountIdDeviceDeviceIdLogoutGet($id, $device_id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->authAccountIdDeviceDeviceIdLogoutGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Account ID | |
| **device_id** | **string**| Device ID | |
| **session** | **string**| JWT | |

### Return type

[**\OpenAPI\Client\Model\ModelSwagStatusOk**](../Model/ModelSwagStatusOk.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `authAccountIdDeviceGet()`

```php
authAccountIdDeviceGet($id, $session, $platform): \OpenAPI\Client\Model\ModelAccountDevice[]
```

Get account devices

This endpoint is for requesting account devices. The _Platform_ header is for filtering devices for the correct product (App|Cms).  _accessible without permission_ (can only be used for the own account. Session must match requested account id.)

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Account ID
$session = 'session_example'; // string | JWT
$platform = 'platform_example'; // string | The client platform

try {
    $result = $apiInstance->authAccountIdDeviceGet($id, $session, $platform);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->authAccountIdDeviceGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Account ID | |
| **session** | **string**| JWT | |
| **platform** | **string**| The client platform | [optional] |

### Return type

[**\OpenAPI\Client\Model\ModelAccountDevice[]**](../Model/ModelAccountDevice.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `authAccountIdGet()`

```php
authAccountIdGet($id, $session, $accept_language, $platform): \OpenAPI\Client\Model\AccountResponse
```

Get account

This endpoint returns the requested account. If _Platform_ header is `\"Cms\"` _Accept-Language_ header will be ignored.  _accessible without permission_ (can only be used for the own account. Session must match requested account id.)  _fully accessible with permission_ : `\"ManageAccounts\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Account ID
$session = 'session_example'; // string | JWT
$accept_language = 'accept_language_example'; // string | client language(s)
$platform = 'platform_example'; // string | The client platform

try {
    $result = $apiInstance->authAccountIdGet($id, $session, $accept_language, $platform);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->authAccountIdGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Account ID | |
| **session** | **string**| JWT | |
| **accept_language** | **string**| client language(s) | [optional] |
| **platform** | **string**| The client platform | [optional] |

### Return type

[**\OpenAPI\Client\Model\AccountResponse**](../Model/AccountResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `authAccountIdGroupProjectProjectIdGet()`

```php
authAccountIdGroupProjectProjectIdGet($id, $project_id, $session, $cursor, $limit, $page): \OpenAPI\Client\Model\GroupResponse[]
```

Get group list for account for project

This endpoint returns a list of all groups for the requested account and project. If a limit is set, a cursor for this endpoint may be created to iterate over all groups.  _only accessible with permission_ : `\"ManageAccounts\"`  _fully accessible with permission_ : `\"ManageAccounts\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Account ID
$project_id = 'project_id_example'; // string | Project ID
$session = 'session_example'; // string | JWT
$cursor = 'cursor_example'; // string | id of the cursor used for pagination; required if page is set
$limit = 56; // int | amount of results per page (1 ... 100)
$page = 56; // int | current page index of the cursor used for pagination; required if cursor is set

try {
    $result = $apiInstance->authAccountIdGroupProjectProjectIdGet($id, $project_id, $session, $cursor, $limit, $page);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->authAccountIdGroupProjectProjectIdGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Account ID | |
| **project_id** | **string**| Project ID | |
| **session** | **string**| JWT | |
| **cursor** | **string**| id of the cursor used for pagination; required if page is set | [optional] |
| **limit** | **int**| amount of results per page (1 ... 100) | [optional] |
| **page** | **int**| current page index of the cursor used for pagination; required if cursor is set | [optional] |

### Return type

[**\OpenAPI\Client\Model\GroupResponse[]**](../Model/GroupResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `authAccountIdGroupProjectProjectIdPut()`

```php
authAccountIdGroupProjectProjectIdPut($id, $project_id, $session, $request): string[]
```

Update account groups membership for project

This endpoint is for updating the group membership of an account for a specific project. In case of response status is 205 the request was only executed partial. Use GET to receive the stored configuration.  _only accessible with permission_ : `\"ManageAccounts\"`  _fully accessible with permission_ : `\"ManageAccounts\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Account ID
$project_id = 'project_id_example'; // string | Project ID
$session = 'session_example'; // string | JWT
$request = array('request_example'); // string[] | group ids

try {
    $result = $apiInstance->authAccountIdGroupProjectProjectIdPut($id, $project_id, $session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->authAccountIdGroupProjectProjectIdPut: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Account ID | |
| **project_id** | **string**| Project ID | |
| **session** | **string**| JWT | |
| **request** | [**string[]**](../Model/string.md)| group ids | |

### Return type

**string[]**

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `authAccountIdPermissionGet()`

```php
authAccountIdPermissionGet($id, $session, $accept_language): array<string,\OpenAPI\Client\Model\AuthorizationPermissionResponse>
```

Get account permissions

This endpoint returns all permissions the user own.  ___property___: enums: `\"AccessPreview\"` `\"ManageAccounts\"` `\"ManageCheckIns\"` `\"ManageConfiguration\"` `\"ManageContent\"` `\"ManageGlobalMedia\"` `\"ManageGlobalRoles\"` `\"ManagePosts\"` `\"ManageProjects\"` `\"ViewAnalytics\"` `\"ViewGlobalAnalytics\"`  _accessible without permission_ (can only be used for the own account. Session must match requested account id.)

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Account ID
$session = 'session_example'; // string | JWT
$accept_language = 'accept_language_example'; // string | client language(s)

try {
    $result = $apiInstance->authAccountIdPermissionGet($id, $session, $accept_language);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->authAccountIdPermissionGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Account ID | |
| **session** | **string**| JWT | |
| **accept_language** | **string**| client language(s) | [optional] |

### Return type

[**array<string,\OpenAPI\Client\Model\AuthorizationPermissionResponse>**](../Model/AuthorizationPermissionResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `authAccountIdProfileGet()`

```php
authAccountIdProfileGet($id, $session, $accept_language, $platform): \OpenAPI\Client\Model\AccountProfileResponse
```

Get account profile

This endpoint is for requesting account profile information. If _Platform_ header is `\"Cms\"` _Accept-Language_ header will be ignored.  _accessible without permission_  _fully accessible with permission_ : `\"ManageAccounts\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Account ID
$session = 'session_example'; // string | JWT
$accept_language = 'accept_language_example'; // string | client language(s)
$platform = 'platform_example'; // string | The client platform

try {
    $result = $apiInstance->authAccountIdProfileGet($id, $session, $accept_language, $platform);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->authAccountIdProfileGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Account ID | |
| **session** | **string**| JWT | |
| **accept_language** | **string**| client language(s) | [optional] |
| **platform** | **string**| The client platform | [optional] |

### Return type

[**\OpenAPI\Client\Model\AccountProfileResponse**](../Model/AccountProfileResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `authAccountIdProfilePatch()`

```php
authAccountIdProfilePatch($id, $session, $request, $accept_language, $platform): \OpenAPI\Client\Model\AccountProfileResponse
```

Update account profile

This endpoint is for updating account profile information. Read only items can only be patched with cms session. If _Platform_ header is `\"Cms\"` _Accept-Language_ header will be ignored.  __Note:__  _meta.translations_ may not hold data. Translation takes places async. Call GET /auth/account/{id}/profile to check for translation again later.  _accessible without permission_  _fully accessible with permission_ : `\"ManageAccounts\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Account ID
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\AccountPatchProfileRequest(); // \OpenAPI\Client\Model\AccountPatchProfileRequest | account profile
$accept_language = 'accept_language_example'; // string | client language(s)
$platform = 'platform_example'; // string | The client platform

try {
    $result = $apiInstance->authAccountIdProfilePatch($id, $session, $request, $accept_language, $platform);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->authAccountIdProfilePatch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Account ID | |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\AccountPatchProfileRequest**](../Model/AccountPatchProfileRequest.md)| account profile | |
| **accept_language** | **string**| client language(s) | [optional] |
| **platform** | **string**| The client platform | [optional] |

### Return type

[**\OpenAPI\Client\Model\AccountProfileResponse**](../Model/AccountProfileResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `authAccountIdProjectProjectIdVisitPut()`

```php
authAccountIdProjectProjectIdVisitPut($id, $project_id, $session): \OpenAPI\Client\Model\ModelSwagStatusOk
```

Account entered project first time

This endpoint is for announcing that an account has entered a project for the first time. It will enable the notification settings for the entered project.  _accessible without permission_ (can only be used for the own account. Session must match requested account id.)

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Account ID of JWT
$project_id = 'project_id_example'; // string | Project ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->authAccountIdProjectProjectIdVisitPut($id, $project_id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->authAccountIdProjectProjectIdVisitPut: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Account ID of JWT | |
| **project_id** | **string**| Project ID | |
| **session** | **string**| JWT | |

### Return type

[**\OpenAPI\Client\Model\ModelSwagStatusOk**](../Model/ModelSwagStatusOk.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `authAccountIdPushDelete()`

```php
authAccountIdPushDelete($id, $session): \OpenAPI\Client\Model\ModelSwagStatusOk
```

Remove push token

This endpoint is for removing account device push token. Session is linked to a device.  _accessible without permission_ (can only be used for the own account. Session must match requested account id.)

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Account ID of JWT
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->authAccountIdPushDelete($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->authAccountIdPushDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Account ID of JWT | |
| **session** | **string**| JWT | |

### Return type

[**\OpenAPI\Client\Model\ModelSwagStatusOk**](../Model/ModelSwagStatusOk.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `authAccountIdPushGet()`

```php
authAccountIdPushGet($id, $session): \OpenAPI\Client\Model\AuthPushTokenResponse
```

Get push token

This endpoint is for requesting account device push token. Session is linked to a device.  _accessible without permission_ (can only be used for the own account. Session must match requested account id.)

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Account ID of JWT
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->authAccountIdPushGet($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->authAccountIdPushGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Account ID of JWT | |
| **session** | **string**| JWT | |

### Return type

[**\OpenAPI\Client\Model\AuthPushTokenResponse**](../Model/AuthPushTokenResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `authAccountIdPushPut()`

```php
authAccountIdPushPut($id, $session, $request, $accept_language): \OpenAPI\Client\Model\ModelSwagStatusOk
```

Set push token

This endpoint is for setting account device push token. Session is linked to a device. The _Accept-Language_ header is used to select the language for sending the push notification. If no language is selected, it will be sent for the default language of the system.  _accessible without permission_ (can only be used for the own account. Session must match requested account id.)

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Account ID of JWT
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\AuthPushTokenRequest(); // \OpenAPI\Client\Model\AuthPushTokenRequest | device push values
$accept_language = 'accept_language_example'; // string | client language(s)

try {
    $result = $apiInstance->authAccountIdPushPut($id, $session, $request, $accept_language);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->authAccountIdPushPut: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Account ID of JWT | |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\AuthPushTokenRequest**](../Model/AuthPushTokenRequest.md)| device push values | |
| **accept_language** | **string**| client language(s) | [optional] |

### Return type

[**\OpenAPI\Client\Model\ModelSwagStatusOk**](../Model/ModelSwagStatusOk.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `authAccountIdRolesGet()`

```php
authAccountIdRolesGet($id, $session): \OpenAPI\Client\Model\ModelAccountRole[]
```

Get roles of an account

This endpoint is for retrieving the roles of a given account  _only accessible with permission_ : `\"ManageAccounts\"`  _fully accessible with permission_ : `\"ManageAccounts\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Account ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->authAccountIdRolesGet($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->authAccountIdRolesGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Account ID | |
| **session** | **string**| JWT | |

### Return type

[**\OpenAPI\Client\Model\ModelAccountRole[]**](../Model/ModelAccountRole.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `authAccountIdRolesPut()`

```php
authAccountIdRolesPut($id, $session, $request): \OpenAPI\Client\Model\ModelAccountRole[]
```

Update the roles of an account

This endpoint is for updating the roles of an account. You are only allowed to add and remove roles that have permissions you already own through your roles. If you have `\"ManageGlobalRoles\"` you are allowed to add and remove all roles. If a user already own a role, that user can keep this role with this request, even if you do not own the permissions of that role. You are not allowed to add or remove roles that have permissions you don't own but user own them from other role.  _only accessible with permission_ : `\"ManageAccounts\"`  _fully accessible with permission_ : `\"ManageAccounts\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Account ID
$session = 'session_example'; // string | JWT
$request = array(new \OpenAPI\Client\Model\ModelAccountRole()); // \OpenAPI\Client\Model\ModelAccountRole[] | the new account roles

try {
    $result = $apiInstance->authAccountIdRolesPut($id, $session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->authAccountIdRolesPut: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Account ID | |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\ModelAccountRole[]**](../Model/ModelAccountRole.md)| the new account roles | |

### Return type

[**\OpenAPI\Client\Model\ModelAccountRole[]**](../Model/ModelAccountRole.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `authAccountIdSettingsGet()`

```php
authAccountIdSettingsGet($id, $session): \OpenAPI\Client\Model\AccountSettingsResponse
```

Get account settings

This endpoint is for requesting account settings.  _accessible without permission_ (can only be used for the own account. Session must match requested account id.)  _fully accessible with permission_ : `\"ManageAccounts\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Account ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->authAccountIdSettingsGet($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->authAccountIdSettingsGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Account ID | |
| **session** | **string**| JWT | |

### Return type

[**\OpenAPI\Client\Model\AccountSettingsResponse**](../Model/AccountSettingsResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `authAccountIdSettingsNotificationGet()`

```php
authAccountIdSettingsNotificationGet($id, $session): \OpenAPI\Client\Model\ModelAccountNotificationSettings
```

Get account notification settings

This endpoint is for requesting account notification settings.  _accessible without permission_ (can only be used for the own account. Session must match requested account id.)  _fully accessible with permission_ : `\"ManageAccounts\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Account ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->authAccountIdSettingsNotificationGet($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->authAccountIdSettingsNotificationGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Account ID | |
| **session** | **string**| JWT | |

### Return type

[**\OpenAPI\Client\Model\ModelAccountNotificationSettings**](../Model/ModelAccountNotificationSettings.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `authAccountIdSettingsNotificationPatch()`

```php
authAccountIdSettingsNotificationPatch($id, $session, $request): \OpenAPI\Client\Model\ModelAccountNotificationSettings[]
```

Update account notification settings

This endpoint updates the account notification settings. In case of response status is 205 the request was only executed partial. Use GET to receive the stored configuration.  _accessible without permission_ (can only be used for the own account. Session must match requested account id.)  _fully accessible with permission_ : `\"ManageAccounts\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Account ID
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\ModelAccountNotificationSettings(); // \OpenAPI\Client\Model\ModelAccountNotificationSettings | account notification settings

try {
    $result = $apiInstance->authAccountIdSettingsNotificationPatch($id, $session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->authAccountIdSettingsNotificationPatch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Account ID | |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\ModelAccountNotificationSettings**](../Model/ModelAccountNotificationSettings.md)| account notification settings | |

### Return type

[**\OpenAPI\Client\Model\ModelAccountNotificationSettings[]**](../Model/ModelAccountNotificationSettings.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `authAccountIdSettingsProjectProjectIdGet()`

```php
authAccountIdSettingsProjectProjectIdGet($id, $project_id, $session): \OpenAPI\Client\Model\ModelAccountProjectSettings
```

Get account project settings

This endpoint is for requesting account project settings for the requested project.  _accessible without permission_ (can only be used for the own account. Session must match requested account id.)  _fully accessible with permission_ : `\"ManageAccounts\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Account ID
$project_id = 'project_id_example'; // string | Project ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->authAccountIdSettingsProjectProjectIdGet($id, $project_id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->authAccountIdSettingsProjectProjectIdGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Account ID | |
| **project_id** | **string**| Project ID | |
| **session** | **string**| JWT | |

### Return type

[**\OpenAPI\Client\Model\ModelAccountProjectSettings**](../Model/ModelAccountProjectSettings.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `authAccountIdSettingsProjectProjectIdPatch()`

```php
authAccountIdSettingsProjectProjectIdPatch($id, $project_id, $session, $request): \OpenAPI\Client\Model\ModelAccountProjectSettings[]
```

Update account project settings

This endpoint updates the account project settings for the requested project.  _accessible without permission_ (can only be used for the own account. Session must match requested account id.)  _fully accessible with permission_ : `\"ManageAccounts\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Account ID
$project_id = 'project_id_example'; // string | Project ID
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\AccountProjectSettingsRequest(); // \OpenAPI\Client\Model\AccountProjectSettingsRequest | account project settings

try {
    $result = $apiInstance->authAccountIdSettingsProjectProjectIdPatch($id, $project_id, $session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->authAccountIdSettingsProjectProjectIdPatch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Account ID | |
| **project_id** | **string**| Project ID | |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\AccountProjectSettingsRequest**](../Model/AccountProjectSettingsRequest.md)| account project settings | |

### Return type

[**\OpenAPI\Client\Model\ModelAccountProjectSettings[]**](../Model/ModelAccountProjectSettings.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `authAccountIdSettingsTrackingGet()`

```php
authAccountIdSettingsTrackingGet($id, $session): \OpenAPI\Client\Model\AccountTrackingResponse
```

Get account tracking settings

This endpoint is for requesting account tracking settings.  _accessible without permission_ (can only be used for the own account. Session must match requested account id.)  _fully accessible with permission_ : `\"ManageAccounts\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Account ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->authAccountIdSettingsTrackingGet($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->authAccountIdSettingsTrackingGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Account ID | |
| **session** | **string**| JWT | |

### Return type

[**\OpenAPI\Client\Model\AccountTrackingResponse**](../Model/AccountTrackingResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `authAccountIdSettingsTrackingPut()`

```php
authAccountIdSettingsTrackingPut($id, $session, $request): \OpenAPI\Client\Model\AccountTrackingResponse
```

Update account tracking settings

This endpoint is for updating account tracking settings.  _accessible without permission_ (can only be used for the own account. Session must match requested account id.)  _fully accessible with permission_ : `\"ManageAccounts\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Account ID
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\AccountTrackingRequest(); // \OpenAPI\Client\Model\AccountTrackingRequest | account tracking settings

try {
    $result = $apiInstance->authAccountIdSettingsTrackingPut($id, $session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->authAccountIdSettingsTrackingPut: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Account ID | |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\AccountTrackingRequest**](../Model/AccountTrackingRequest.md)| account tracking settings | |

### Return type

[**\OpenAPI\Client\Model\AccountTrackingResponse**](../Model/AccountTrackingResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `authAccountIdSettingsVisibilityGet()`

```php
authAccountIdSettingsVisibilityGet($id, $session): \OpenAPI\Client\Model\AccountVisibilitySettingsResponse
```

Get account visibility settings

This endpoint is for requesting account visibility settings.  _accessible without permission_ (can only be used for the own account. Session must match requested account id.)  _fully accessible with permission_ : `\"ManageAccounts\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Account ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->authAccountIdSettingsVisibilityGet($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->authAccountIdSettingsVisibilityGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Account ID | |
| **session** | **string**| JWT | |

### Return type

[**\OpenAPI\Client\Model\AccountVisibilitySettingsResponse**](../Model/AccountVisibilitySettingsResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `authAccountIdSettingsVisibilityPatch()`

```php
authAccountIdSettingsVisibilityPatch($id, $session, $request): \OpenAPI\Client\Model\AccountVisibilitySettingsResponse
```

Update account visibility settings

This endpoint is for updating account visibility settings. In order to enable the chat, the account should have first or last name set. After enabling the chat the refresh session endpoint must be called to get also a sendbird session token.  __Note:__ In exceptional cases the user has to login again.  _accessible without permission_ (can only be used for the own account. Session must match requested account id.)  _fully accessible with permission_ : `\"ManageAccounts\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Account ID
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\AccountVisibilitySettingsRequest(); // \OpenAPI\Client\Model\AccountVisibilitySettingsRequest | account visibility settings

try {
    $result = $apiInstance->authAccountIdSettingsVisibilityPatch($id, $session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->authAccountIdSettingsVisibilityPatch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Account ID | |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\AccountVisibilitySettingsRequest**](../Model/AccountVisibilitySettingsRequest.md)| account visibility settings | |

### Return type

[**\OpenAPI\Client\Model\AccountVisibilitySettingsResponse**](../Model/AccountVisibilitySettingsResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `authAccountMetaGet()`

```php
authAccountMetaGet($session, $accept_language, $platform): \OpenAPI\Client\Model\AuthAccountMetaGet200Response
```

Get meta item setup

This endpoint is for retrieving the meta item configuration for accounts. If _Platform_ is `\"Cms\"` _Accept-Language_ header will be ignored. If _Platform_ is not `\"Cms\"` _selections.options.design_ values are hexcolors only.  _accessible without permission_

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT
$accept_language = 'accept_language_example'; // string | client language(s)
$platform = 'platform_example'; // string | The client platform

try {
    $result = $apiInstance->authAccountMetaGet($session, $accept_language, $platform);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->authAccountMetaGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **session** | **string**| JWT | |
| **accept_language** | **string**| client language(s) | [optional] |
| **platform** | **string**| The client platform | [optional] |

### Return type

[**\OpenAPI\Client\Model\AuthAccountMetaGet200Response**](../Model/AuthAccountMetaGet200Response.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `authAccountMetaPut()`

```php
authAccountMetaPut($session, $request): \OpenAPI\Client\Model\AuthAccountMetaGet200Response
```

Update meta item setup

This endpoint is for updating the meta item configuration for accounts  _only accessible with permission_ : `\"ManageConfiguration\"`  _fully accessible with permission_ : `\"ManageConfiguration\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\AccountPutMetaRequest(); // \OpenAPI\Client\Model\AccountPutMetaRequest | new meta configuration

try {
    $result = $apiInstance->authAccountMetaPut($session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->authAccountMetaPut: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\AccountPutMetaRequest**](../Model/AccountPutMetaRequest.md)| new meta configuration | |

### Return type

[**\OpenAPI\Client\Model\AuthAccountMetaGet200Response**](../Model/AuthAccountMetaGet200Response.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `authAccountPost()`

```php
authAccountPost($session, $request, $accept_language): \OpenAPI\Client\Model\AccountResponse
```

Create account

This endpoint is for creating a new account. An email can be sent to the account owner to inform about the new account. If no password is provided, an email with a set password token will be sent to the account owner. You are only allowed to add roles that have permissions you already own through your roles. If you have `\"ManageGlobalRoles\"` you are allowed to add all roles. The _Accept-Language_ header is used to select the language for sending the email. If no language is selected, the email will be sent for the default language of the system.  _only accessible with permission_ : `\"ManageAccounts\"`  _fully accessible with permission_ : `\"ManageAccounts\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\AccountCreateRequest(); // \OpenAPI\Client\Model\AccountCreateRequest | Account to create
$accept_language = 'accept_language_example'; // string | client language(s)

try {
    $result = $apiInstance->authAccountPost($session, $request, $accept_language);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->authAccountPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\AccountCreateRequest**](../Model/AccountCreateRequest.md)| Account to create | |
| **accept_language** | **string**| client language(s) | [optional] |

### Return type

[**\OpenAPI\Client\Model\AccountResponse**](../Model/AccountResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `authAccountProjectProjectIdIdGet()`

```php
authAccountProjectProjectIdIdGet($project_id, $session): string[]
```

Get project account ids

This endpoint is for requesting account ids of a project  _only accessible with permission_ : `\"ManageAccounts\"` `\"ManageConfiguration\"` `\"ManageContent\"` `\"ManageProjects\"` `\"ViewAnalytics\"` `\"ViewGlobalAnalytics\"`  _fully accessible with permission_ : `\"ManageAccounts\"` `\"ManageConfiguration\"` `\"ManageContent\"` `\"ManageProjects\"` `\"ViewAnalytics\"` `\"ViewGlobalAnalytics\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$project_id = 'project_id_example'; // string | Project ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->authAccountProjectProjectIdIdGet($project_id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->authAccountProjectProjectIdIdGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **project_id** | **string**| Project ID | |
| **session** | **string**| JWT | |

### Return type

**string[]**

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `authAccountProjectProjectIdStatsGet()`

```php
authAccountProjectProjectIdStatsGet($project_id, $session): \OpenAPI\Client\Model\AccountProjectStatsResponse[]
```

Get project accounts statistics

This endpoint is for requesting accounts statistics of a project Only accounts that have access and entered the project once are considered.  _only accessible with permission_ : `\"ManageAccounts\"` `\"ManageConfiguration\"` `\"ManageContent\"` `\"ManageProjects\"` `\"ViewAnalytics\"` `\"ViewGlobalAnalytics\"`  _fully accessible with permission_ : `\"ManageAccounts\"` `\"ManageConfiguration\"` `\"ManageContent\"` `\"ManageProjects\"` `\"ViewAnalytics\"` `\"ViewGlobalAnalytics\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$project_id = 'project_id_example'; // string | Project ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->authAccountProjectProjectIdStatsGet($project_id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->authAccountProjectProjectIdStatsGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **project_id** | **string**| Project ID | |
| **session** | **string**| JWT | |

### Return type

[**\OpenAPI\Client\Model\AccountProjectStatsResponse[]**](../Model/AccountProjectStatsResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `authAccountProjectProjectIdStatsRecordGet()`

```php
authAccountProjectProjectIdStatsRecordGet($project_id, $session): array<string,\OpenAPI\Client\Model\AccountProjectStatsRecordResponse>
```

Get project accounts statistic records

This endpoint is for requesting accounts statistic records of a project. Only accounts that have access and entered the project once are considered.  _only accessible with permission_ : `\"ManageAccounts\"` `\"ManageConfiguration\"` `\"ManageContent\"` `\"ManageProjects\"` `\"ViewAnalytics\"` `\"ViewGlobalAnalytics\"`  _fully accessible with permission_ : `\"ManageAccounts\"` `\"ManageConfiguration\"` `\"ManageContent\"` `\"ManageProjects\"` `\"ViewAnalytics\"` `\"ViewGlobalAnalytics\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$project_id = 'project_id_example'; // string | Project ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->authAccountProjectProjectIdStatsRecordGet($project_id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->authAccountProjectProjectIdStatsRecordGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **project_id** | **string**| Project ID | |
| **session** | **string**| JWT | |

### Return type

[**array<string,\OpenAPI\Client\Model\AccountProjectStatsRecordResponse>**](../Model/AccountProjectStatsRecordResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `authAccountSearchPost()`

```php
authAccountSearchPost($session, $request, $accept_language, $platform): \OpenAPI\Client\Model\AccountResponse[]
```

Search accounts

This endpoint is for requesting account list with a search If _Platform_ header is `\"Cms\"` _Accept-Language_ header will be ignored.  _only accessible with permission_ : `\"ManageAccounts\"`  _fully accessible with permission_ : `\"ManageAccounts\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\AccountSearch(); // \OpenAPI\Client\Model\AccountSearch | search
$accept_language = 'accept_language_example'; // string | client language(s)
$platform = 'platform_example'; // string | The client platform

try {
    $result = $apiInstance->authAccountSearchPost($session, $request, $accept_language, $platform);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->authAccountSearchPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\AccountSearch**](../Model/AccountSearch.md)| search | |
| **accept_language** | **string**| client language(s) | [optional] |
| **platform** | **string**| The client platform | [optional] |

### Return type

[**\OpenAPI\Client\Model\AccountResponse[]**](../Model/AccountResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `authAccountStatsGet()`

```php
authAccountStatsGet($session): \OpenAPI\Client\Model\AccountStatsResponse[]
```

Get accounts statistics

This endpoint is for requesting accounts statistics.  _only accessible with permission_ : `\"ManageAccounts\"` `\"ManageConfiguration\"` `\"ManageProjects\"` `\"ViewGlobalAnalytics\"`  _fully accessible with permission_ : `\"ManageAccounts\"` `\"ManageConfiguration\"` `\"ManageProjects\"` `\"ViewGlobalAnalytics\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->authAccountStatsGet($session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->authAccountStatsGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **session** | **string**| JWT | |

### Return type

[**\OpenAPI\Client\Model\AccountStatsResponse[]**](../Model/AccountStatsResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `authAccountStatsRecordGet()`

```php
authAccountStatsRecordGet($session): array<string,\OpenAPI\Client\Model\ModelAccountStatsRecord>
```

Get accounts statistic records

This endpoint is for requesting accounts statistic records.  _only accessible with permission_ : `\"ManageAccounts\"` `\"ManageConfiguration\"` `\"ManageProjects\"` `\"ViewGlobalAnalytics\"`  _fully accessible with permission_ : `\"ManageAccounts\"` `\"ManageConfiguration\"` `\"ManageProjects\"` `\"ViewGlobalAnalytics\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->authAccountStatsRecordGet($session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->authAccountStatsRecordGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **session** | **string**| JWT | |

### Return type

[**array<string,\OpenAPI\Client\Model\ModelAccountStatsRecord>**](../Model/ModelAccountStatsRecord.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `authEmailPost()`

```php
authEmailPost($session, $request, $accept_language, $platform): \OpenAPI\Client\Model\ModelSwagStatusOk
```

Change email first

This endpoint should be requested first for changing the current email address for an account. The email cannot be changed for an accounts that is linked to a sso provider. A link with a confirmation token is sent to the new email address. This token must be redeemed to save the change. The _Platform_ header is for creating the correct token link send to the requested new email address. The token should be redeemed on PUT /auth/email This function is safe against enumeration attacks, so it is not possible to get information about already used emails in the system. If there already is an account for the requested mail, the address cannot be changed for the current account The _Accept-Language_ header is used to select the language for sending the email. If no language is selected, the email will be sent for the default language of the system.  _accessible without permission_

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\AuthEmailChangeFirstRequest(); // \OpenAPI\Client\Model\AuthEmailChangeFirstRequest | requested mail change
$accept_language = 'accept_language_example'; // string | client language(s)
$platform = 'platform_example'; // string | The client platform

try {
    $result = $apiInstance->authEmailPost($session, $request, $accept_language, $platform);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->authEmailPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\AuthEmailChangeFirstRequest**](../Model/AuthEmailChangeFirstRequest.md)| requested mail change | |
| **accept_language** | **string**| client language(s) | [optional] |
| **platform** | **string**| The client platform | [optional] |

### Return type

[**\OpenAPI\Client\Model\ModelSwagStatusOk**](../Model/ModelSwagStatusOk.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `authEmailPut()`

```php
authEmailPut($request, $accept_language, $platform): \OpenAPI\Client\Model\AuthEmailChangeResponse
```

Change email final

This endpoint should be requested for redeeming the token to finish the email address change. For this action a one time token is needed. The email cannot be changed for an accounts that is linked to a sso provider. After a successful change of the email address all session and refresh tokens will be invalidated and a notification is sent to the old email address of the account. The _Accept-Language_ header is used to select the language for sending the email. If no language is selected, the email will be sent for the default language of the system. On success this endpoint provides a new refresh token and new session in the 200 response. In case of response status is 205 login has to be performed again.  _accessible without permission_

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$request = new \OpenAPI\Client\Model\AuthEmailChangeRedeemTokenRequest(); // \OpenAPI\Client\Model\AuthEmailChangeRedeemTokenRequest | email change token
$accept_language = 'accept_language_example'; // string | client language(s)
$platform = 'platform_example'; // string | The client platform

try {
    $result = $apiInstance->authEmailPut($request, $accept_language, $platform);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->authEmailPut: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **request** | [**\OpenAPI\Client\Model\AuthEmailChangeRedeemTokenRequest**](../Model/AuthEmailChangeRedeemTokenRequest.md)| email change token | |
| **accept_language** | **string**| client language(s) | [optional] |
| **platform** | **string**| The client platform | [optional] |

### Return type

[**\OpenAPI\Client\Model\AuthEmailChangeResponse**](../Model/AuthEmailChangeResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `authPasswordChangePost()`

```php
authPasswordChangePost($request, $platform): \OpenAPI\Client\Model\AuthPasswordChangeTokenResponse
```

Request password change

This endpoint is for requesting a one time token to change the password of an account. The password cannot be changed for an accounts that is linked to a sso provider. This endpoint uses the final message of the SCRAM challenge to validate the old password. The Platform must match the Platform from the first message. See RFC 5802 for detail SCRAM definition.  To perform this action call SCRAM First first: POST /auth/auth  _accessible without permission_

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$request = new \OpenAPI\Client\Model\AuthScramFinalRequest(); // \OpenAPI\Client\Model\AuthScramFinalRequest | Clients Final Message
$platform = 'platform_example'; // string | The client platform

try {
    $result = $apiInstance->authPasswordChangePost($request, $platform);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->authPasswordChangePost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **request** | [**\OpenAPI\Client\Model\AuthScramFinalRequest**](../Model/AuthScramFinalRequest.md)| Clients Final Message | |
| **platform** | **string**| The client platform | [optional] |

### Return type

[**\OpenAPI\Client\Model\AuthPasswordChangeTokenResponse**](../Model/AuthPasswordChangeTokenResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `authPasswordPut()`

```php
authPasswordPut($request, $platform): \OpenAPI\Client\Model\AuthPasswordChangeResponse
```

Change Password

This endpoint is for replacing old password with new one. For this action a one time token is needed. The token can be created with a new account registration, a password recover action or changing password request. The new password must be supplied in plain text to check if it matches the password security guidelines. If the new password does not match the guidelines the reason can be found in the 400 response message. After a successful change of the password every session and refresh token for this user will be invalidated. On success this endpoint provides a new refresh token and new session in the 200 response. In case of response status is 205 login has to be performed again.  __Error messages:__ * Error.Token.Invalid * Error.Password.NoLower * Error.Password.TooShort * Error.Password.NoNumber * Error.Password.NotDictionarySafe * Error.Password.NoSpecial * Error.Password.NoUpper * Error.Password.UsedBefore  _accessible without permission_

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$request = new \OpenAPI\Client\Model\AuthPasswordChangeRequest(); // \OpenAPI\Client\Model\AuthPasswordChangeRequest | password change
$platform = 'platform_example'; // string | The client platform

try {
    $result = $apiInstance->authPasswordPut($request, $platform);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->authPasswordPut: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **request** | [**\OpenAPI\Client\Model\AuthPasswordChangeRequest**](../Model/AuthPasswordChangeRequest.md)| password change | |
| **platform** | **string**| The client platform | [optional] |

### Return type

[**\OpenAPI\Client\Model\AuthPasswordChangeResponse**](../Model/AuthPasswordChangeResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `authPasswordRecoverPost()`

```php
authPasswordRecoverPost($request, $accept_language, $platform): \OpenAPI\Client\Model\ModelSwagStatusOk
```

Recover Password

This endpoint is for recovering password for given email. It always returns 200 if the request body is correct. If there is an existing account for the given email address, an email will be sent to this address with a token link. The _Platform_ header is used for setting the interface the recovering link should lead. The _Accept-Language_ header is used to select the language for sending the email. If no language is selected, the email will be sent for the default language of the system.  _accessible without permission_

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$request = new \OpenAPI\Client\Model\AuthPasswordRecoverRequest(); // \OpenAPI\Client\Model\AuthPasswordRecoverRequest | password recover
$accept_language = 'accept_language_example'; // string | client language(s)
$platform = 'platform_example'; // string | The client platform

try {
    $result = $apiInstance->authPasswordRecoverPost($request, $accept_language, $platform);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->authPasswordRecoverPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **request** | [**\OpenAPI\Client\Model\AuthPasswordRecoverRequest**](../Model/AuthPasswordRecoverRequest.md)| password recover | |
| **accept_language** | **string**| client language(s) | [optional] |
| **platform** | **string**| The client platform | [optional] |

### Return type

[**\OpenAPI\Client\Model\ModelSwagStatusOk**](../Model/ModelSwagStatusOk.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `authRegisterPost()`

```php
authRegisterPost($request, $accept_language): \OpenAPI\Client\Model\ModelSwagStatusOk
```

Registration

This endpoint is used for registration of an account with a valid email address. An email with registration token will be sent to the given address. If there already is an account for that email address, a password forgotten link will be sent to the user instead. The received one time token can be redeemed for setting password: PUT /auth/password If registration is disabled in the security configuration this endpoint is also disabled. The _Accept-Language_ header is used to select the language for sending the email. If no language is selected, the email will be sent for the default language of the system.  _accessible without permission_

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$request = new \OpenAPI\Client\Model\AccountRegistrationRequest(); // \OpenAPI\Client\Model\AccountRegistrationRequest | email address
$accept_language = 'accept_language_example'; // string | client language(s)

try {
    $result = $apiInstance->authRegisterPost($request, $accept_language);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->authRegisterPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **request** | [**\OpenAPI\Client\Model\AccountRegistrationRequest**](../Model/AccountRegistrationRequest.md)| email address | |
| **accept_language** | **string**| client language(s) | [optional] |

### Return type

[**\OpenAPI\Client\Model\ModelSwagStatusOk**](../Model/ModelSwagStatusOk.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
