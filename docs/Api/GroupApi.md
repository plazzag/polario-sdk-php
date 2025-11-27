# OpenAPI\Client\GroupApi



All URIs are relative to https://custom.polario.de/api, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**authGroupGet()**](GroupApi.md#authGroupGet) | **GET** /auth/group | Get group list |
| [**authGroupIdAccountDelete()**](GroupApi.md#authGroupIdAccountDelete) | **DELETE** /auth/group/{id}/account | remove accounts from group |
| [**authGroupIdAccountGet()**](GroupApi.md#authGroupIdAccountGet) | **GET** /auth/group/{id}/account | Get accounts of group |
| [**authGroupIdAccountPost()**](GroupApi.md#authGroupIdAccountPost) | **POST** /auth/group/{id}/account | add accounts to group |
| [**authGroupIdDelete()**](GroupApi.md#authGroupIdDelete) | **DELETE** /auth/group/{id} | Delete group |
| [**authGroupIdGet()**](GroupApi.md#authGroupIdGet) | **GET** /auth/group/{id} | Get group |
| [**authGroupIdPatch()**](GroupApi.md#authGroupIdPatch) | **PATCH** /auth/group/{id} | Update group |
| [**authGroupPost()**](GroupApi.md#authGroupPost) | **POST** /auth/group | Create group |
| [**authGroupProjectIdGet()**](GroupApi.md#authGroupProjectIdGet) | **GET** /auth/group/project/{id} | Get group list for project |


## `authGroupGet()`

```php
authGroupGet($session, $cursor, $limit, $page): \OpenAPI\Client\Model\GroupResponse[]
```

Get group list

This endpoint returns a list of all existing groups. If a limit is set, a cursor for this endpoint may be created to iterate over all groups.  _only accessible with permission_ : `\"ManageAccounts\"`  _fully accessible with permission_ : `\"ManageAccounts\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\GroupApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT
$cursor = 'cursor_example'; // string | id of the cursor used for pagination; required if page is set
$limit = 56; // int | amount of results per page (1 ... 100)
$page = 56; // int | current page index of the cursor used for pagination; required if cursor is set

try {
    $result = $apiInstance->authGroupGet($session, $cursor, $limit, $page);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GroupApi->authGroupGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
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

## `authGroupIdAccountDelete()`

```php
authGroupIdAccountDelete($id, $session, $request): string[]
```

remove accounts from group

This endpoint removes accounts from a specific group.  __Note:__ if isSystem = true the group is immutable, api call will result in a http 409  _only accessible with permission_ : `\"ManageAccounts\"`  _fully accessible with permission_ : `\"ManageAccounts\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\GroupApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Group ID
$session = 'session_example'; // string | JWT
$request = array('request_example'); // string[] | account ids

try {
    $result = $apiInstance->authGroupIdAccountDelete($id, $session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GroupApi->authGroupIdAccountDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Group ID | |
| **session** | **string**| JWT | |
| **request** | [**string[]**](../Model/string.md)| account ids | |

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

## `authGroupIdAccountGet()`

```php
authGroupIdAccountGet($id, $session): string[]
```

Get accounts of group

This endpoint returns all account ids for a specific group.  _only accessible with permission_ : `\"ManageAccounts\"` `\"ManageContent\"` `\"ManageGlobalMedia\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageAccounts\"` `\"ManageContent\"` `\"ManageGlobalMedia\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\GroupApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Group ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->authGroupIdAccountGet($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GroupApi->authGroupIdAccountGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Group ID | |
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

## `authGroupIdAccountPost()`

```php
authGroupIdAccountPost($id, $session, $request): string[]
```

add accounts to group

This endpoint adds accounts to a specific group.  __Note:__ if isSystem = true the group is immutable, api call will result in a http 409  _only accessible with permission_ : `\"ManageAccounts\"`  _fully accessible with permission_ : `\"ManageAccounts\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\GroupApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Group ID
$session = 'session_example'; // string | JWT
$request = array('request_example'); // string[] | account ids

try {
    $result = $apiInstance->authGroupIdAccountPost($id, $session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GroupApi->authGroupIdAccountPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Group ID | |
| **session** | **string**| JWT | |
| **request** | [**string[]**](../Model/string.md)| account ids | |

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

## `authGroupIdDelete()`

```php
authGroupIdDelete($id, $session): \OpenAPI\Client\Model\ModelSwagStatusOk
```

Delete group

This endpoint is for deleting a specific group. If a group has children, the child will remain at the place the deleted parent group was before.  __Note:__ if isSystem = true the group is immutable, api call will result in a http 409  _only accessible with permission_ : `\"ManageAccounts\"`  _fully accessible with permission_ : `\"ManageAccounts\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\GroupApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Group ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->authGroupIdDelete($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GroupApi->authGroupIdDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Group ID | |
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

## `authGroupIdGet()`

```php
authGroupIdGet($id, $session): \OpenAPI\Client\Model\GroupResponse
```

Get group

This endpoint returns group by given id with all additional information.  _only accessible with permission_ : `\"ManageAccounts\"` `\"ManageContent\"` `\"ManageGlobalMedia\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageAccounts\"` `\"ManageContent\"` `\"ManageGlobalMedia\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\GroupApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Group ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->authGroupIdGet($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GroupApi->authGroupIdGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Group ID | |
| **session** | **string**| JWT | |

### Return type

[**\OpenAPI\Client\Model\GroupResponse**](../Model/GroupResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `authGroupIdPatch()`

```php
authGroupIdPatch($id, $session, $request): \OpenAPI\Client\Model\GroupResponse
```

Update group

This endpoint is for updating a group.  __Note:__ if isSystem = true the group is immutable, api call will result in a http 409  _only accessible with permission_ : `\"ManageAccounts\"`  _fully accessible with permission_ : `\"ManageAccounts\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\GroupApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Group ID
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\GroupPatchRequest(); // \OpenAPI\Client\Model\GroupPatchRequest | group data to update

try {
    $result = $apiInstance->authGroupIdPatch($id, $session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GroupApi->authGroupIdPatch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Group ID | |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\GroupPatchRequest**](../Model/GroupPatchRequest.md)| group data to update | |

### Return type

[**\OpenAPI\Client\Model\GroupResponse**](../Model/GroupResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `authGroupPost()`

```php
authGroupPost($session, $request): \OpenAPI\Client\Model\GroupResponse
```

Create group

This endpoint is for creating a new group.  _only accessible with permission_ : `\"ManageAccounts\"`  _fully accessible with permission_ : `\"ManageAccounts\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\GroupApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\GroupPostRequest(); // \OpenAPI\Client\Model\GroupPostRequest | group data to create

try {
    $result = $apiInstance->authGroupPost($session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GroupApi->authGroupPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\GroupPostRequest**](../Model/GroupPostRequest.md)| group data to create | |

### Return type

[**\OpenAPI\Client\Model\GroupResponse**](../Model/GroupResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `authGroupProjectIdGet()`

```php
authGroupProjectIdGet($id, $session, $cursor, $limit, $page): \OpenAPI\Client\Model\GroupResponse[]
```

Get group list for project

This endpoint returns a list of all groups for the requested project. If a limit is set, a cursor for this endpoint may be created to iterate over all groups.  _only accessible with permission_ : `\"ManageAccounts\"` `\"ManageContent\"` `\"ManageGlobalMedia\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageAccounts\"` `\"ManageContent\"` `\"ManageGlobalMedia\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\GroupApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Project ID
$session = 'session_example'; // string | JWT
$cursor = 'cursor_example'; // string | id of the cursor used for pagination; required if page is set
$limit = 56; // int | amount of results per page (1 ... 100)
$page = 56; // int | current page index of the cursor used for pagination; required if cursor is set

try {
    $result = $apiInstance->authGroupProjectIdGet($id, $session, $cursor, $limit, $page);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GroupApi->authGroupProjectIdGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Project ID | |
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
