# OpenAPI\Client\IndexDefaultApi



All URIs are relative to https://custom.polario.de/api, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**indexDefaultGet()**](IndexDefaultApi.md#indexDefaultGet) | **GET** /index/default | Get index items for cursor |
| [**indexDefaultObjectTypeObjectIdLinkedGet()**](IndexDefaultApi.md#indexDefaultObjectTypeObjectIdLinkedGet) | **GET** /index/default/{objectType}/{objectId}/linked | Get linked items |
| [**indexDefaultSearchPost()**](IndexDefaultApi.md#indexDefaultSearchPost) | **POST** /index/default/search | Create cursor |


## `indexDefaultGet()`

```php
indexDefaultGet($cursor, $page, $limit, $accept_language, $session): \OpenAPI\Client\Model\IndexAdminGet200ResponseInner[]
```

Get index items for cursor

This endpoint returns a list of all index items for a cursor in default representation.  Cursor could be created here: POST /index/default/search  _accessible without permission_

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\IndexDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$cursor = 'cursor_example'; // string | id of the cursor used for pagination; required if page is set
$page = 56; // int | current page index of the cursor used for pagination; required if cursor is set
$limit = 56; // int | amount of results per page (1 ... 100)
$accept_language = 'accept_language_example'; // string | client language(s)
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->indexDefaultGet($cursor, $page, $limit, $accept_language, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling IndexDefaultApi->indexDefaultGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **cursor** | **string**| id of the cursor used for pagination; required if page is set | |
| **page** | **int**| current page index of the cursor used for pagination; required if cursor is set | |
| **limit** | **int**| amount of results per page (1 ... 100) | [optional] |
| **accept_language** | **string**| client language(s) | [optional] |
| **session** | **string**| JWT | [optional] |

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

## `indexDefaultObjectTypeObjectIdLinkedGet()`

```php
indexDefaultObjectTypeObjectIdLinkedGet($object_type, $object_id, $cursor, $limit, $page, $accept_language, $session): \OpenAPI\Client\Model\IndexAdminGet200ResponseInner[]
```

Get linked items

This endpoint is for requesting all linked items for a specific object. If a limit is set, a cursor for this endpoint may be created to iterate over all linked items.  _accessible without permission_  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageGlobalMedia\"` `\"ManageProjects\"` (depending on requested object type)

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\IndexDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$object_type = 'object_type_example'; // string | object type
$object_id = 'object_id_example'; // string | object ID
$cursor = 'cursor_example'; // string | id of the cursor used for pagination; required if page is set
$limit = 56; // int | amount of results per page (1 ... 100)
$page = 56; // int | current page index of the cursor used for pagination; required if cursor is set
$accept_language = 'accept_language_example'; // string | client language(s)
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->indexDefaultObjectTypeObjectIdLinkedGet($object_type, $object_id, $cursor, $limit, $page, $accept_language, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling IndexDefaultApi->indexDefaultObjectTypeObjectIdLinkedGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **object_type** | **string**| object type | |
| **object_id** | **string**| object ID | |
| **cursor** | **string**| id of the cursor used for pagination; required if page is set | [optional] |
| **limit** | **int**| amount of results per page (1 ... 100) | [optional] |
| **page** | **int**| current page index of the cursor used for pagination; required if cursor is set | [optional] |
| **accept_language** | **string**| client language(s) | [optional] |
| **session** | **string**| JWT | [optional] |

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

## `indexDefaultSearchPost()`

```php
indexDefaultSearchPost($request, $accept_language, $session): \OpenAPI\Client\Model\ModelCursorResponse
```

Create cursor

This endpoint returns a cursor for list index items in default representation with applied filter and sort options. private items will not be part of the result. In case of cursor response total will be 0 the status 204 with not content is returned instead.  _accessible without permission_  _fully accessible with permission_ : `\"ManageAccounts\"` `\"ManageContent\"` `\"ManageGlobalMedia\"` `\"ManageProjects\"` (depending on requested object type)

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\IndexDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$request = new \OpenAPI\Client\Model\IndexCursorRequestDefault(); // \OpenAPI\Client\Model\IndexCursorRequestDefault | search criteria
$accept_language = 'accept_language_example'; // string | client language(s)
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->indexDefaultSearchPost($request, $accept_language, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling IndexDefaultApi->indexDefaultSearchPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **request** | [**\OpenAPI\Client\Model\IndexCursorRequestDefault**](../Model/IndexCursorRequestDefault.md)| search criteria | |
| **accept_language** | **string**| client language(s) | [optional] |
| **session** | **string**| JWT | [optional] |

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
