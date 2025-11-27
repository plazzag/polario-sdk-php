# OpenAPI\Client\ProjectDefaultApi



All URIs are relative to https://custom.polario.de/api, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**projectDefaultGet()**](ProjectDefaultApi.md#projectDefaultGet) | **GET** /project/default | Get published project list |
| [**projectDefaultIdGet()**](ProjectDefaultApi.md#projectDefaultIdGet) | **GET** /project/default/{id} | Get project |


## `projectDefaultGet()`

```php
projectDefaultGet($cursor, $limit, $page, $accept_language, $session): \OpenAPI\Client\Model\ProjectResponseDefault[]
```

Get published project list

This endpoint returns an array of all published projects. The output is in default representation and filtered for the user permissions. If a limit is set, a cursor for this endpoint may be created to iterate over all projects.  _accessible without permission_  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\ProjectDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$cursor = 'cursor_example'; // string | id of the cursor used for pagination; required if page is set
$limit = 56; // int | amount of results per page (1 ... 100)
$page = 56; // int | current page index of the cursor used for pagination; required if cursor is set
$accept_language = 'accept_language_example'; // string | client language(s)
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->projectDefaultGet($cursor, $limit, $page, $accept_language, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProjectDefaultApi->projectDefaultGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **cursor** | **string**| id of the cursor used for pagination; required if page is set | [optional] |
| **limit** | **int**| amount of results per page (1 ... 100) | [optional] |
| **page** | **int**| current page index of the cursor used for pagination; required if cursor is set | [optional] |
| **accept_language** | **string**| client language(s) | [optional] |
| **session** | **string**| JWT | [optional] |

### Return type

[**\OpenAPI\Client\Model\ProjectResponseDefault[]**](../Model/ProjectResponseDefault.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `projectDefaultIdGet()`

```php
projectDefaultIdGet($id, $accept_language, $session): \OpenAPI\Client\Model\ProjectResponseDefault
```

Get project

This endpoint returns a localized project in default representation by given id. If the requested language is not available it will fall back to the default language.  _accessible without permission_  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\ProjectDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Project ID
$accept_language = 'accept_language_example'; // string | client language(s)
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->projectDefaultIdGet($id, $accept_language, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProjectDefaultApi->projectDefaultIdGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Project ID | |
| **accept_language** | **string**| client language(s) | [optional] |
| **session** | **string**| JWT | [optional] |

### Return type

[**\OpenAPI\Client\Model\ProjectResponseDefault**](../Model/ProjectResponseDefault.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
