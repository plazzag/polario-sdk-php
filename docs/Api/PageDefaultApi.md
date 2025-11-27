# OpenAPI\Client\PageDefaultApi



All URIs are relative to https://custom.polario.de/api, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**pageDefaultIdDesktopGet()**](PageDefaultApi.md#pageDefaultIdDesktopGet) | **GET** /page/default/{id}/desktop | Get page desktop content |
| [**pageDefaultIdGet()**](PageDefaultApi.md#pageDefaultIdGet) | **GET** /page/default/{id} | Get page |
| [**pageDefaultPostCountIdGet()**](PageDefaultApi.md#pageDefaultPostCountIdGet) | **GET** /page/default/post-count/{id} | Get page post count |
| [**pageDefaultPostCountProjectIdGet()**](PageDefaultApi.md#pageDefaultPostCountProjectIdGet) | **GET** /page/default/post-count/project/{id} | Get page post counts for project |


## `pageDefaultIdDesktopGet()`

```php
pageDefaultIdDesktopGet($id, $accept_language, $session): \OpenAPI\Client\Model\PageDefaultIdGet200Response
```

Get page desktop content

This endpoint returns a localized page for desktop in default user representation by given id. If there is no specific desktop version of the page the standard (mobile) version of the page will be selected.  For preview use: GET /page/default/{id}/preview/desktop  If the requested language is not available it will fall back to the default language.  _accessible without permission_  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\PageDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Page ID
$accept_language = 'accept_language_example'; // string | client language(s)
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->pageDefaultIdDesktopGet($id, $accept_language, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PageDefaultApi->pageDefaultIdDesktopGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Page ID | |
| **accept_language** | **string**| client language(s) | [optional] |
| **session** | **string**| JWT | [optional] |

### Return type

[**\OpenAPI\Client\Model\PageDefaultIdGet200Response**](../Model/PageDefaultIdGet200Response.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `pageDefaultIdGet()`

```php
pageDefaultIdGet($id, $accept_language, $session): \OpenAPI\Client\Model\PageDefaultIdGet200Response
```

Get page

This endpoint returns a localized page in default user representation by given id.  For preview use: GET /page/default/{id}/preview  If the requested language is not available it will fall back to the default language.  _accessible without permission_  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\PageDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Page ID
$accept_language = 'accept_language_example'; // string | client language(s)
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->pageDefaultIdGet($id, $accept_language, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PageDefaultApi->pageDefaultIdGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Page ID | |
| **accept_language** | **string**| client language(s) | [optional] |
| **session** | **string**| JWT | [optional] |

### Return type

[**\OpenAPI\Client\Model\PageDefaultIdGet200Response**](../Model/PageDefaultIdGet200Response.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `pageDefaultPostCountIdGet()`

```php
pageDefaultPostCountIdGet($id, $session): \OpenAPI\Client\Model\PagePostCountResponse
```

Get page post count

This endpoint returns the post count of the requested page.  _accessible without permission_  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\PageDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Page ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->pageDefaultPostCountIdGet($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PageDefaultApi->pageDefaultPostCountIdGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Page ID | |
| **session** | **string**| JWT | |

### Return type

[**\OpenAPI\Client\Model\PagePostCountResponse**](../Model/PagePostCountResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `pageDefaultPostCountProjectIdGet()`

```php
pageDefaultPostCountProjectIdGet($id, $session, $cursor, $limit, $page): \OpenAPI\Client\Model\PagePostCountResponse[]
```

Get page post counts for project

This endpoint returns a list of post counts for all published pages with social interaction activated of the requested project. If a limit is set, a cursor for this endpoint may be created to iterate over all post counts.  _accessible without permission_  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\PageDefaultApi(
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
    $result = $apiInstance->pageDefaultPostCountProjectIdGet($id, $session, $cursor, $limit, $page);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PageDefaultApi->pageDefaultPostCountProjectIdGet: ', $e->getMessage(), PHP_EOL;
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

[**\OpenAPI\Client\Model\PagePostCountResponse[]**](../Model/PagePostCountResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
