# OpenAPI\Client\RoleApi



All URIs are relative to https://custom.polario.de/api, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**authRoleAllowedToSetGet()**](RoleApi.md#authRoleAllowedToSetGet) | **GET** /auth/role/allowed-to-set | Get roles allowed assigning |
| [**authRoleGet()**](RoleApi.md#authRoleGet) | **GET** /auth/role | Get roles |
| [**authRoleIdDelete()**](RoleApi.md#authRoleIdDelete) | **DELETE** /auth/role/{id} | Delete role |
| [**authRoleIdGet()**](RoleApi.md#authRoleIdGet) | **GET** /auth/role/{id} | Get role |
| [**authRoleIdPatch()**](RoleApi.md#authRoleIdPatch) | **PATCH** /auth/role/{id} | Update role |
| [**authRolePost()**](RoleApi.md#authRolePost) | **POST** /auth/role | Create role |


## `authRoleAllowedToSetGet()`

```php
authRoleAllowedToSetGet($session): \OpenAPI\Client\Model\ModelAccountRole[]
```

Get roles allowed assigning

This endpoint list all roles that could be assigned to other accounts the requested account is allowed for. projectID = null indicates that it is a global role or that the role can be assigned for all projects.  _only accessible with permission_ : `\"ManageAccounts\"`  _fully accessible with permission_ : `\"ManageAccounts\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\RoleApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->authRoleAllowedToSetGet($session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RoleApi->authRoleAllowedToSetGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
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

## `authRoleGet()`

```php
authRoleGet($session, $accept_language): \OpenAPI\Client\Model\RoleResponse[]
```

Get roles

This endpoint returns all roles of the system (filtered by permissions)  _only accessible with permission_ : `\"ManageAccounts\"` `\"ManageGlobalRoles\"`  _fully accessible with permission_ : `\"ManageAccounts\"` `\"ManageGlobalRoles\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\RoleApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT
$accept_language = 'accept_language_example'; // string | client language(s)

try {
    $result = $apiInstance->authRoleGet($session, $accept_language);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RoleApi->authRoleGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **session** | **string**| JWT | |
| **accept_language** | **string**| client language(s) | [optional] |

### Return type

[**\OpenAPI\Client\Model\RoleResponse[]**](../Model/RoleResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `authRoleIdDelete()`

```php
authRoleIdDelete($id, $session): \OpenAPI\Client\Model\ModelSwagStatusOk
```

Delete role

This endpoint is for deleting a specific role.  _only accessible with permission_ : `\"ManageGlobalRoles\"`  _fully accessible with permission_ : `\"ManageGlobalRoles\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\RoleApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Role ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->authRoleIdDelete($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RoleApi->authRoleIdDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Role ID | |
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

## `authRoleIdGet()`

```php
authRoleIdGet($id, $session, $accept_language): \OpenAPI\Client\Model\RoleResponse
```

Get role

This endpoint returns role by given id with all additional information.  _only accessible with permission_ : `\"ManageAccounts\"` `\"ManageGlobalRoles\"`  _fully accessible with permission_ : `\"ManageAccounts\"` `\"ManageGlobalRoles\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\RoleApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Role ID
$session = 'session_example'; // string | JWT
$accept_language = 'accept_language_example'; // string | client language(s)

try {
    $result = $apiInstance->authRoleIdGet($id, $session, $accept_language);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RoleApi->authRoleIdGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Role ID | |
| **session** | **string**| JWT | |
| **accept_language** | **string**| client language(s) | [optional] |

### Return type

[**\OpenAPI\Client\Model\RoleResponse**](../Model/RoleResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `authRoleIdPatch()`

```php
authRoleIdPatch($id, $session, $request, $accept_language): \OpenAPI\Client\Model\RoleResponse
```

Update role

This endpoint is for updating a role. Project based roles can only contain project permissions and global roles can only contain global permissions. If Accept-Language is not provided, the localization is changed for the default language.  __Global Permissions:__ `\"ManageAccounts\"` `\"ManageConfiguration\"` `\"ManageGlobalMedia\"` `\"ManageGlobalRoles\"` `\"ManageProjects\"` `\"ViewGlobalAnalytics\"`  __Project Permissions:__ `\"AccessPreview\"` `\"ManageCheckIns\"` `\"ManageContent\"` `\"ManagePosts\"` `\"ViewAnalytics\"`  _only accessible with permission_ : `\"ManageGlobalRoles\"`  _fully accessible with permission_ : `\"ManageGlobalRoles\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\RoleApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Role ID
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\RolePatchRequest(); // \OpenAPI\Client\Model\RolePatchRequest | role data to update
$accept_language = 'accept_language_example'; // string | client language(s)

try {
    $result = $apiInstance->authRoleIdPatch($id, $session, $request, $accept_language);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RoleApi->authRoleIdPatch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Role ID | |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\RolePatchRequest**](../Model/RolePatchRequest.md)| role data to update | |
| **accept_language** | **string**| client language(s) | [optional] |

### Return type

[**\OpenAPI\Client\Model\RoleResponse**](../Model/RoleResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `authRolePost()`

```php
authRolePost($session, $request, $accept_language): \OpenAPI\Client\Model\RoleResponse
```

Create role

This endpoint is for creating a new role. Project based roles can only contain project permissions and global roles can only contain global permissions. If Accept-Language is not the same as the default language, the provided localization will be also stored for the default language  __Global Permissions:__ `\"ManageAccounts\"` `\"ManageConfiguration\"` `\"ManageGlobalMedia\"` `\"ManageGlobalRoles\"` `\"ManageProjects\"` `\"ViewGlobalAnalytics\"`  __Project Permissions:__ `\"AccessPreview\"` `\"ManageCheckIns\"` `\"ManageContent\"` `\"ManagePosts\"` `\"ViewAnalytics\"`  __Note:__ There is a maximum of 256 roles. You cannot create more than that. Status code 409 will be sent in that case.  _only accessible with permission_ : `\"ManageGlobalRoles\"`  _fully accessible with permission_ : `\"ManageGlobalRoles\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\RoleApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\RolePostRequest(); // \OpenAPI\Client\Model\RolePostRequest | role data to create
$accept_language = 'accept_language_example'; // string | client language(s)

try {
    $result = $apiInstance->authRolePost($session, $request, $accept_language);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RoleApi->authRolePost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\RolePostRequest**](../Model/RolePostRequest.md)| role data to create | |
| **accept_language** | **string**| client language(s) | [optional] |

### Return type

[**\OpenAPI\Client\Model\RoleResponse**](../Model/RoleResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
