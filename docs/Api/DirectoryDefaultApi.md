# OpenAPI\Client\DirectoryDefaultApi



All URIs are relative to https://custom.polario.de/api, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**directoryDefaultIdContentGet()**](DirectoryDefaultApi.md#directoryDefaultIdContentGet) | **GET** /directory/default/{id}/content | Get directory content rows list |
| [**directoryDefaultIdGet()**](DirectoryDefaultApi.md#directoryDefaultIdGet) | **GET** /directory/default/{id} | Get directory |
| [**directoryDefaultIdRowPost()**](DirectoryDefaultApi.md#directoryDefaultIdRowPost) | **POST** /directory/default/{id}/row | Add directory content row |
| [**directoryDefaultRowIdDelete()**](DirectoryDefaultApi.md#directoryDefaultRowIdDelete) | **DELETE** /directory/default/row/{id} | Delete directory content row |
| [**directoryDefaultRowIdGet()**](DirectoryDefaultApi.md#directoryDefaultRowIdGet) | **GET** /directory/default/row/{id} | Get directory content row |
| [**directoryDefaultRowIdPut()**](DirectoryDefaultApi.md#directoryDefaultRowIdPut) | **PUT** /directory/default/row/{id} | Update directory content row |


## `directoryDefaultIdContentGet()`

```php
directoryDefaultIdContentGet($id, $cursor, $limit, $page, $accept_language, $session): \OpenAPI\Client\Model\ContentRowResponseDefault[]
```

Get directory content rows list

This endpoint is for retrieving all content rows of the requested directory in default representation. If directory has no items defined, output for dynamic directories will be empty. If the requested language is not available it will fall back to the default language. If a limit is set, a cursor for this endpoint may be created to iterate over all content rows.  _accessible without permission_  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\DirectoryDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Directory ID
$cursor = 'cursor_example'; // string | id of the cursor used for pagination; required if page is set
$limit = 56; // int | amount of results per page (1 ... 100)
$page = 56; // int | current page index of the cursor used for pagination; required if cursor is set
$accept_language = 'accept_language_example'; // string | client language(s)
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->directoryDefaultIdContentGet($id, $cursor, $limit, $page, $accept_language, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DirectoryDefaultApi->directoryDefaultIdContentGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Directory ID | |
| **cursor** | **string**| id of the cursor used for pagination; required if page is set | [optional] |
| **limit** | **int**| amount of results per page (1 ... 100) | [optional] |
| **page** | **int**| current page index of the cursor used for pagination; required if cursor is set | [optional] |
| **accept_language** | **string**| client language(s) | [optional] |
| **session** | **string**| JWT | [optional] |

### Return type

[**\OpenAPI\Client\Model\ContentRowResponseDefault[]**](../Model/ContentRowResponseDefault.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `directoryDefaultIdGet()`

```php
directoryDefaultIdGet($id, $accept_language, $session): \OpenAPI\Client\Model\DirectoryDefaultIdGet200Response
```

Get directory

This endpoint returns a localized directory in default user representation by given id. If the requested language is not available it will fall back to the default language.  __DateTime formats:__ * `\"DateOnly\"`: \"2006-01-02\" * `\"DateTime\"`: \"2006-01-02 15:04:05\" * `\"RFC822X\"`: \"02 Jan 06 15:04\" * `\"RFC1123X\"`: \"Mon, 02 Jan 2006 15:04\" * `\"RFC1123DateOnly\"`: \"Mon, 02 Jan 2006\" * `\"TimeOnlyX\"`: \"15:04\"  __Note:__ when the property `sort` does not have any elements than `order` will not be `\"Custom\"`  _accessible without permission_  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\DirectoryDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Directory ID
$accept_language = 'accept_language_example'; // string | client language(s)
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->directoryDefaultIdGet($id, $accept_language, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DirectoryDefaultApi->directoryDefaultIdGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Directory ID | |
| **accept_language** | **string**| client language(s) | [optional] |
| **session** | **string**| JWT | [optional] |

### Return type

[**\OpenAPI\Client\Model\DirectoryDefaultIdGet200Response**](../Model/DirectoryDefaultIdGet200Response.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `directoryDefaultIdRowPost()`

```php
directoryDefaultIdRowPost($id, $session, $request): \OpenAPI\Client\Model\ContentRowResponseDefault
```

Add directory content row

This endpoint is for adding new a new content row to the requested static directory. For dynamic directories no content can be added in this way.  __Note:__ rows for dynamic directory (contentRowObjectType != null) are not creatable here. Status 409 Conflict will be returned.  __Note:__  _data.translations_ will be always empty. Translation takes places async. Call GET /directory/default/row/{rowId} to check for translation later.  _accessible without permission_  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\DirectoryDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Directory ID
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\ContentRowRequestDefault(); // \OpenAPI\Client\Model\ContentRowRequestDefault | directory content row to create

try {
    $result = $apiInstance->directoryDefaultIdRowPost($id, $session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DirectoryDefaultApi->directoryDefaultIdRowPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Directory ID | |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\ContentRowRequestDefault**](../Model/ContentRowRequestDefault.md)| directory content row to create | |

### Return type

[**\OpenAPI\Client\Model\ContentRowResponseDefault**](../Model/ContentRowResponseDefault.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `directoryDefaultRowIdDelete()`

```php
directoryDefaultRowIdDelete($id, $session): \OpenAPI\Client\Model\ModelSwagStatusOk
```

Delete directory content row

This endpoint is for deleting a directory content row.  __Note:__ rows for dynamic directory (contentRowObjectType != null) are not deletable here. Status 409 Conflict will be returned.  _accessible without permission_  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\DirectoryDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Row ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->directoryDefaultRowIdDelete($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DirectoryDefaultApi->directoryDefaultRowIdDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Row ID | |
| **session** | **string**| JWT | [optional] |

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

## `directoryDefaultRowIdGet()`

```php
directoryDefaultRowIdGet($id, $accept_language, $session): \OpenAPI\Client\Model\ContentRowResponseDefault
```

Get directory content row

This endpoint is for retrieving a content row of a directory. If the requested language is not available it will fall back to the default language.  _accessible without permission_  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\DirectoryDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Row ID
$accept_language = 'accept_language_example'; // string | client language(s)
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->directoryDefaultRowIdGet($id, $accept_language, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DirectoryDefaultApi->directoryDefaultRowIdGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Row ID | |
| **accept_language** | **string**| client language(s) | [optional] |
| **session** | **string**| JWT | [optional] |

### Return type

[**\OpenAPI\Client\Model\ContentRowResponseDefault**](../Model/ContentRowResponseDefault.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `directoryDefaultRowIdPut()`

```php
directoryDefaultRowIdPut($id, $request, $accept_language, $session): \OpenAPI\Client\Model\ContentRowResponseDefault
```

Update directory content row

This endpoint is for updating a directory content row by row ID. If the requested language is not available it will fall back to the default language.  __Note:__ rows for dynamic directory (contentRowObjectType != null) are not changeable here. Status 409 Conflict will be returned.  __Note:__  _data.translations_ may not hold data. Translation takes places async. Call GET /directory/default/row/{id} to check for translation again later.  _accessible without permission_  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\DirectoryDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Row ID
$request = new \OpenAPI\Client\Model\ContentRowRequestDefault(); // \OpenAPI\Client\Model\ContentRowRequestDefault | directory content row to be replaced
$accept_language = 'accept_language_example'; // string | client language(s)
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->directoryDefaultRowIdPut($id, $request, $accept_language, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DirectoryDefaultApi->directoryDefaultRowIdPut: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Row ID | |
| **request** | [**\OpenAPI\Client\Model\ContentRowRequestDefault**](../Model/ContentRowRequestDefault.md)| directory content row to be replaced | |
| **accept_language** | **string**| client language(s) | [optional] |
| **session** | **string**| JWT | [optional] |

### Return type

[**\OpenAPI\Client\Model\ContentRowResponseDefault**](../Model/ContentRowResponseDefault.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
