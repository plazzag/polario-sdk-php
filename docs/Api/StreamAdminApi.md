# OpenAPI\Client\StreamAdminApi



All URIs are relative to https://custom.polario.de/api, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**streamAdminIdAccessGet()**](StreamAdminApi.md#streamAdminIdAccessGet) | **GET** /stream/admin/{id}/access | Get stream access configuration |
| [**streamAdminIdAccessPatch()**](StreamAdminApi.md#streamAdminIdAccessPatch) | **PATCH** /stream/admin/{id}/access | Update stream access configuration |
| [**streamAdminIdDelete()**](StreamAdminApi.md#streamAdminIdDelete) | **DELETE** /stream/admin/{id} | Delete stream |
| [**streamAdminIdGet()**](StreamAdminApi.md#streamAdminIdGet) | **GET** /stream/admin/{id} | Get stream |
| [**streamAdminIdPatch()**](StreamAdminApi.md#streamAdminIdPatch) | **PATCH** /stream/admin/{id} | Update stream |
| [**streamAdminPost()**](StreamAdminApi.md#streamAdminPost) | **POST** /stream/admin | Create stream |
| [**streamAdminProjectIdGet()**](StreamAdminApi.md#streamAdminProjectIdGet) | **GET** /stream/admin/project/{id} | Get stream list for project |


## `streamAdminIdAccessGet()`

```php
streamAdminIdAccessGet($id, $session): \OpenAPI\Client\Model\AuthorizationAccessResponse
```

Get stream access configuration

This endpoint returns the access configuration for the requested stream.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\StreamAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Stream ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->streamAdminIdAccessGet($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StreamAdminApi->streamAdminIdAccessGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Stream ID | |
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

## `streamAdminIdAccessPatch()`

```php
streamAdminIdAccessPatch($id, $session, $request): \OpenAPI\Client\Model\ModelAccess
```

Update stream access configuration

This endpoint updates the access configuration for the requested stream. Only the changes should be transmitted due this endpoint.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\StreamAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Stream ID
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\ModelAccess(); // \OpenAPI\Client\Model\ModelAccess | changed access rights

try {
    $result = $apiInstance->streamAdminIdAccessPatch($id, $session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StreamAdminApi->streamAdminIdAccessPatch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Stream ID | |
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

## `streamAdminIdDelete()`

```php
streamAdminIdDelete($id, $session): \OpenAPI\Client\Model\ModelSwagStatusOk
```

Delete stream

This endpoint is for deleting a single stream.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\StreamAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Stream ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->streamAdminIdDelete($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StreamAdminApi->streamAdminIdDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Stream ID | |
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

## `streamAdminIdGet()`

```php
streamAdminIdGet($id, $session): \OpenAPI\Client\Model\StreamResponseAdmin
```

Get stream

This endpoint returns a stream in administrative representation by given id.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\StreamAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Stream ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->streamAdminIdGet($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StreamAdminApi->streamAdminIdGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Stream ID | |
| **session** | **string**| JWT | |

### Return type

[**\OpenAPI\Client\Model\StreamResponseAdmin**](../Model/StreamResponseAdmin.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `streamAdminIdPatch()`

```php
streamAdminIdPatch($id, $session, $request): \OpenAPI\Client\Model\StreamResponseAdmin
```

Update stream

This endpoint is for updating specific data of an existing stream.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\StreamAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Stream ID
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\StreamPatchRequest(); // \OpenAPI\Client\Model\StreamPatchRequest | stream data to be updated

try {
    $result = $apiInstance->streamAdminIdPatch($id, $session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StreamAdminApi->streamAdminIdPatch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Stream ID | |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\StreamPatchRequest**](../Model/StreamPatchRequest.md)| stream data to be updated | [optional] |

### Return type

[**\OpenAPI\Client\Model\StreamResponseAdmin**](../Model/StreamResponseAdmin.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `streamAdminPost()`

```php
streamAdminPost($session, $request): \OpenAPI\Client\Model\StreamResponseAdmin
```

Create stream

This endpoint is for creating a new stream.  Currently 3Q live streams are supported only due this endpoint.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\StreamAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\StreamPostRequest(); // \OpenAPI\Client\Model\StreamPostRequest | Stream to create

try {
    $result = $apiInstance->streamAdminPost($session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StreamAdminApi->streamAdminPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\StreamPostRequest**](../Model/StreamPostRequest.md)| Stream to create | |

### Return type

[**\OpenAPI\Client\Model\StreamResponseAdmin**](../Model/StreamResponseAdmin.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `streamAdminProjectIdGet()`

```php
streamAdminProjectIdGet($id, $session, $cursor, $limit, $page, $accept_language): \OpenAPI\Client\Model\StreamResponseListAdmin[]
```

Get stream list for project

This endpoint returns a list of all streams for the requested project without technical configuration parameters. If a limit is set, a cursor for this endpoint may be created to iterate over all streams.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\StreamAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Project ID
$session = 'session_example'; // string | JWT
$cursor = 'cursor_example'; // string | id of the cursor used for pagination; required if page is set
$limit = 56; // int | amount of results per page (1 ... 100)
$page = 56; // int | current page index of the cursor used for pagination; required if cursor is set
$accept_language = 'accept_language_example'; // string | client language(s)

try {
    $result = $apiInstance->streamAdminProjectIdGet($id, $session, $cursor, $limit, $page, $accept_language);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StreamAdminApi->streamAdminProjectIdGet: ', $e->getMessage(), PHP_EOL;
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
| **accept_language** | **string**| client language(s) | [optional] |

### Return type

[**\OpenAPI\Client\Model\StreamResponseListAdmin[]**](../Model/StreamResponseListAdmin.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
