# OpenAPI\Client\AdminAreaApi



All URIs are relative to https://custom.polario.de/api, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**newsDefaultIdPreviewDesktopGet()**](AdminAreaApi.md#newsDefaultIdPreviewDesktopGet) | **GET** /news/default/{id}/preview/desktop | Get article preview desktop |
| [**newsDefaultIdPreviewGet()**](AdminAreaApi.md#newsDefaultIdPreviewGet) | **GET** /news/default/{id}/preview | Get article preview mobile |
| [**newsDefaultPreviewSearchPost()**](AdminAreaApi.md#newsDefaultPreviewSearchPost) | **POST** /news/default/preview/search | Create cursor |
| [**newsDefaultProjectIdPreviewGet()**](AdminAreaApi.md#newsDefaultProjectIdPreviewGet) | **GET** /news/default/project/{id}/preview | Get article list preview for project |
| [**newsDefaultProjectIdPreviewIdsGet()**](AdminAreaApi.md#newsDefaultProjectIdPreviewIdsGet) | **GET** /news/default/project/{id}/preview/ids | Get article preview ids for project |
| [**pageDefaultIdPreviewDesktopGet()**](AdminAreaApi.md#pageDefaultIdPreviewDesktopGet) | **GET** /page/default/{id}/preview/desktop | Get page preview desktop |
| [**pageDefaultIdPreviewGet()**](AdminAreaApi.md#pageDefaultIdPreviewGet) | **GET** /page/default/{id}/preview | Get page preview mobile |
| [**pageDefaultProjectIdPreviewGet()**](AdminAreaApi.md#pageDefaultProjectIdPreviewGet) | **GET** /page/default/project/{id}/preview | Get page list preview for project |


## `newsDefaultIdPreviewDesktopGet()`

```php
newsDefaultIdPreviewDesktopGet($id, $session, $accept_language): \OpenAPI\Client\Model\NewsDefaultIdGet200Response
```

Get article preview desktop

This endpoint returns a localized article preview for desktop in default user representation by given id.  For published view use: GET /news/default/{id}/desktop  If there is no specific desktop version of the article the standard (mobile) version of the article will be selected.  _only accessible with permission_ : `\"AccessPreview\"` `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\AdminAreaApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Article ID
$session = 'session_example'; // string | JWT
$accept_language = 'accept_language_example'; // string | client language(s)

try {
    $result = $apiInstance->newsDefaultIdPreviewDesktopGet($id, $session, $accept_language);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AdminAreaApi->newsDefaultIdPreviewDesktopGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Article ID | |
| **session** | **string**| JWT | |
| **accept_language** | **string**| client language(s) | [optional] |

### Return type

[**\OpenAPI\Client\Model\NewsDefaultIdGet200Response**](../Model/NewsDefaultIdGet200Response.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `newsDefaultIdPreviewGet()`

```php
newsDefaultIdPreviewGet($id, $session, $accept_language): \OpenAPI\Client\Model\NewsDefaultIdGet200Response
```

Get article preview mobile

This endpoint returns a localized article in default user representation by given id.  For published view use: GET /news/default/{id}  _only accessible with permission_ : `\"AccessPreview\"` `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\AdminAreaApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Article ID
$session = 'session_example'; // string | JWT
$accept_language = 'accept_language_example'; // string | client language(s)

try {
    $result = $apiInstance->newsDefaultIdPreviewGet($id, $session, $accept_language);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AdminAreaApi->newsDefaultIdPreviewGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Article ID | |
| **session** | **string**| JWT | |
| **accept_language** | **string**| client language(s) | [optional] |

### Return type

[**\OpenAPI\Client\Model\NewsDefaultIdGet200Response**](../Model/NewsDefaultIdGet200Response.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `newsDefaultPreviewSearchPost()`

```php
newsDefaultPreviewSearchPost($request, $accept_language, $session): \OpenAPI\Client\Model\ModelCursorResponse
```

Create cursor

This endpoint returns a cursor for preview list articles in default representation with applied filter and sort options. In case of cursor response total will be 0 the status 204 with not content is returned instead.  For published list cursor use: GET /news/default/search  _only accessible with permission_ : `\"AccessPreview\" (counts also for linked projects)` `\"ManageContent\" (counts also for linked projects)` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\" (counts also for linked projects)` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\AdminAreaApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$request = new \OpenAPI\Client\Model\NewsPostCursorPreviewDefault(); // \OpenAPI\Client\Model\NewsPostCursorPreviewDefault | options to create cursor
$accept_language = 'accept_language_example'; // string | client language(s)
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->newsDefaultPreviewSearchPost($request, $accept_language, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AdminAreaApi->newsDefaultPreviewSearchPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **request** | [**\OpenAPI\Client\Model\NewsPostCursorPreviewDefault**](../Model/NewsPostCursorPreviewDefault.md)| options to create cursor | |
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

## `newsDefaultProjectIdPreviewGet()`

```php
newsDefaultProjectIdPreviewGet($id, $session, $cursor, $limit, $page, $accept_language): \OpenAPI\Client\Model\NewsArticleResponseListDefault[]
```

Get article list preview for project

This endpoint returns a list of all articles for the requested project without content in default representation. The entries are sorted by `publishedAt:DESC`. If a limit is set, a cursor for this endpoint may be created to iterate over all articles.  For published view list use: GET /news/default/project/{id}  _only accessible with permission_ : `\"AccessPreview\" (counts also for linked projects)` `\"ManageContent\" (counts also for linked projects)` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\" (counts also for linked projects)` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\AdminAreaApi(
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
    $result = $apiInstance->newsDefaultProjectIdPreviewGet($id, $session, $cursor, $limit, $page, $accept_language);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AdminAreaApi->newsDefaultProjectIdPreviewGet: ', $e->getMessage(), PHP_EOL;
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

[**\OpenAPI\Client\Model\NewsArticleResponseListDefault[]**](../Model/NewsArticleResponseListDefault.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `newsDefaultProjectIdPreviewIdsGet()`

```php
newsDefaultProjectIdPreviewIdsGet($id, $session, $accept_language): string[]
```

Get article preview ids for project

This endpoint returns a list of all articles for the requested project without content in default representation. The entries are sorted by `publishedAt:DESC`.  For published list ids use: GET /news/default/project/{id}/ids  _only accessible with permission_ : `\"AccessPreview\" (counts also for linked projects)` `\"ManageContent\" (counts also for linked projects)` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\" (counts also for linked projects)` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\AdminAreaApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Project ID
$session = 'session_example'; // string | JWT
$accept_language = 'accept_language_example'; // string | client language(s)

try {
    $result = $apiInstance->newsDefaultProjectIdPreviewIdsGet($id, $session, $accept_language);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AdminAreaApi->newsDefaultProjectIdPreviewIdsGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Project ID | |
| **session** | **string**| JWT | |
| **accept_language** | **string**| client language(s) | [optional] |

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

## `pageDefaultIdPreviewDesktopGet()`

```php
pageDefaultIdPreviewDesktopGet($id, $session, $accept_language): \OpenAPI\Client\Model\PageDefaultIdGet200Response
```

Get page preview desktop

This endpoint returns a localized page preview for desktop in default user representation by given id.  For published view use: GET /page/default/{id}/desktop  If there is no specific desktop version of the page the standard (mobile) version of the page will be selected. If the requested language is not available it will fall back to the default language.  _only accessible with permission_ : `\"AccessPreview\"` `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\AdminAreaApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Page ID
$session = 'session_example'; // string | JWT
$accept_language = 'accept_language_example'; // string | client language(s)

try {
    $result = $apiInstance->pageDefaultIdPreviewDesktopGet($id, $session, $accept_language);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AdminAreaApi->pageDefaultIdPreviewDesktopGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Page ID | |
| **session** | **string**| JWT | |
| **accept_language** | **string**| client language(s) | [optional] |

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

## `pageDefaultIdPreviewGet()`

```php
pageDefaultIdPreviewGet($id, $session, $accept_language): \OpenAPI\Client\Model\PageDefaultIdGet200Response
```

Get page preview mobile

This endpoint returns a localized page in default user representation by given id.  For published view use: GET /page/default/{id}  If the requested language is not available it will fall back to the default language.  _only accessible with permission_ : `\"AccessPreview\"` `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\AdminAreaApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Page ID
$session = 'session_example'; // string | JWT
$accept_language = 'accept_language_example'; // string | client language(s)

try {
    $result = $apiInstance->pageDefaultIdPreviewGet($id, $session, $accept_language);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AdminAreaApi->pageDefaultIdPreviewGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Page ID | |
| **session** | **string**| JWT | |
| **accept_language** | **string**| client language(s) | [optional] |

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

## `pageDefaultProjectIdPreviewGet()`

```php
pageDefaultProjectIdPreviewGet($id, $session, $cursor, $limit, $page, $accept_language): \OpenAPI\Client\Model\PageResponseListDefault[]
```

Get page list preview for project

This endpoint returns a list of all pages for the requested project without content in default representation. If a limit is set, a cursor for this endpoint may be created to iterate over all pages.  If the requested language is not available it will fall back to the default language.  _only accessible with permission_ : `\"AccessPreview\"` `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\AdminAreaApi(
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
    $result = $apiInstance->pageDefaultProjectIdPreviewGet($id, $session, $cursor, $limit, $page, $accept_language);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AdminAreaApi->pageDefaultProjectIdPreviewGet: ', $e->getMessage(), PHP_EOL;
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

[**\OpenAPI\Client\Model\PageResponseListDefault[]**](../Model/PageResponseListDefault.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
