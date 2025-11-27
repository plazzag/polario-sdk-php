# OpenAPI\Client\PermissionApi



All URIs are relative to https://custom.polario.de/api, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**authPermissionGet()**](PermissionApi.md#authPermissionGet) | **GET** /auth/permission | List permissions |
| [**authPermissionPermissionGet()**](PermissionApi.md#authPermissionPermissionGet) | **GET** /auth/permission/{permission} | Check permission existence |


## `authPermissionGet()`

```php
authPermissionGet($session, $accept_language): \OpenAPI\Client\Model\AuthSwagPermissionsAssociated
```

List permissions

This endpoint returns all available permissions for association with localization.  _only accessible with permission_ : `\"ManageAccounts\"` `\"ManageGlobalRoles\"`  _fully accessible with permission_ : `\"ManageAccounts\"` `\"ManageGlobalRoles\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\PermissionApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT
$accept_language = 'accept_language_example'; // string | client language(s)

try {
    $result = $apiInstance->authPermissionGet($session, $accept_language);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PermissionApi->authPermissionGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **session** | **string**| JWT | |
| **accept_language** | **string**| client language(s) | [optional] |

### Return type

[**\OpenAPI\Client\Model\AuthSwagPermissionsAssociated**](../Model/AuthSwagPermissionsAssociated.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `authPermissionPermissionGet()`

```php
authPermissionPermissionGet($permission, $session): \OpenAPI\Client\Model\AuthorizationPermissionResponse
```

Check permission existence

This endpoint checks if a given user or any has the desired permission  In case of response status is 403 the user does not have the requested permission.  _accessible without permission_

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\PermissionApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$permission = 'permission_example'; // string | The permission to check
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->authPermissionPermissionGet($permission, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PermissionApi->authPermissionPermissionGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **permission** | **string**| The permission to check | |
| **session** | **string**| JWT | |

### Return type

[**\OpenAPI\Client\Model\AuthorizationPermissionResponse**](../Model/AuthorizationPermissionResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
