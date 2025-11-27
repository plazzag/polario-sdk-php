# OpenAPI\Client\IndexAdminApi



All URIs are relative to https://custom.polario.de/api, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**indexAdminGet()**](IndexAdminApi.md#indexAdminGet) | **GET** /index/admin | Get index items for cursor |
| [**indexAdminObjectTypeObjectIdGet()**](IndexAdminApi.md#indexAdminObjectTypeObjectIdGet) | **GET** /index/admin/{objectType}/{objectId} | Get index |
| [**indexAdminObjectTypeObjectIdLinkedGet()**](IndexAdminApi.md#indexAdminObjectTypeObjectIdLinkedGet) | **GET** /index/admin/{objectType}/{objectId}/linked | Get linked items |
| [**indexAdminSearchPost()**](IndexAdminApi.md#indexAdminSearchPost) | **POST** /index/admin/search | Create cursor |


## `indexAdminGet()`

```php
indexAdminGet($cursor, $page, $session, $limit): \OpenAPI\Client\Model\IndexAdminGet200ResponseInner[]
```

Get index items for cursor

This endpoint returns a list of all index items for a cursor in administrative representation.  Cursor could be created here: POST /index/admin/search  _accessible without permission_

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\IndexAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$cursor = 'cursor_example'; // string | id of the cursor used for pagination; required if page is set
$page = 56; // int | current page index of the cursor used for pagination; required if cursor is set
$session = 'session_example'; // string | JWT
$limit = 56; // int | amount of results per page (1 ... 100)

try {
    $result = $apiInstance->indexAdminGet($cursor, $page, $session, $limit);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling IndexAdminApi->indexAdminGet: ', $e->getMessage(), PHP_EOL;
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

[**\OpenAPI\Client\Model\IndexAdminGet200ResponseInner[]**](../Model/IndexAdminGet200ResponseInner.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `indexAdminObjectTypeObjectIdGet()`

```php
indexAdminObjectTypeObjectIdGet($object_type, $object_id, $session): \OpenAPI\Client\Model\IndexAdminObjectTypeObjectIdGet200Response
```

Get index

This endpoint is for requesting a specific index items.  _accessible without permission_  _fully accessible with permission_ : `\"ManageAccounts\"` `\"ManageContent\"` `\"ManageGlobalMedia\"` `\"ManageProjects\"` (depending on requested object type)

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\IndexAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$object_type = 'object_type_example'; // string | object type
$object_id = 'object_id_example'; // string | object ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->indexAdminObjectTypeObjectIdGet($object_type, $object_id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling IndexAdminApi->indexAdminObjectTypeObjectIdGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **object_type** | **string**| object type | |
| **object_id** | **string**| object ID | |
| **session** | **string**| JWT | |

### Return type

[**\OpenAPI\Client\Model\IndexAdminObjectTypeObjectIdGet200Response**](../Model/IndexAdminObjectTypeObjectIdGet200Response.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `indexAdminObjectTypeObjectIdLinkedGet()`

```php
indexAdminObjectTypeObjectIdLinkedGet($object_type, $object_id, $session, $cursor, $limit, $page): \OpenAPI\Client\Model\IndexAdminGet200ResponseInner[]
```

Get linked items

This endpoint is for requesting all linked items for a specific object. If a limit is set, a cursor for this endpoint may be created to iterate over all linked items.  _accessible without permission_  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageGlobalMedia\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\IndexAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$object_type = 'object_type_example'; // string | object type
$object_id = 'object_id_example'; // string | object ID
$session = 'session_example'; // string | JWT
$cursor = 'cursor_example'; // string | id of the cursor used for pagination; required if page is set
$limit = 56; // int | amount of results per page (1 ... 100)
$page = 56; // int | current page index of the cursor used for pagination; required if cursor is set

try {
    $result = $apiInstance->indexAdminObjectTypeObjectIdLinkedGet($object_type, $object_id, $session, $cursor, $limit, $page);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling IndexAdminApi->indexAdminObjectTypeObjectIdLinkedGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **object_type** | **string**| object type | |
| **object_id** | **string**| object ID | |
| **session** | **string**| JWT | |
| **cursor** | **string**| id of the cursor used for pagination; required if page is set | [optional] |
| **limit** | **int**| amount of results per page (1 ... 100) | [optional] |
| **page** | **int**| current page index of the cursor used for pagination; required if cursor is set | [optional] |

### Return type

[**\OpenAPI\Client\Model\IndexAdminGet200ResponseInner[]**](../Model/IndexAdminGet200ResponseInner.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `indexAdminSearchPost()`

```php
indexAdminSearchPost($session, $request): \OpenAPI\Client\Model\ModelCursorResponse
```

Create cursor

This endpoint returns a cursor for list index items in admin representation with applied filter and sort options. private items will not be part of the result. In case of cursor response total will be 0 the status 204 with not content is returned instead.  _accessible without permission_  _fully accessible with permission_ : `\"ManageAccounts\"` `\"ManageContent\"` `\"ManageGlobalMedia\"` `\"ManageProjects\"` (depending on requested object type)

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\IndexAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\IndexCursorRequestAdmin(); // \OpenAPI\Client\Model\IndexCursorRequestAdmin | search criteria to create cursor

try {
    $result = $apiInstance->indexAdminSearchPost($session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling IndexAdminApi->indexAdminSearchPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\IndexCursorRequestAdmin**](../Model/IndexCursorRequestAdmin.md)| search criteria to create cursor | |

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
