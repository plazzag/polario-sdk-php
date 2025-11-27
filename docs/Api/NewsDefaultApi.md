# OpenAPI\Client\NewsDefaultApi



All URIs are relative to https://custom.polario.de/api, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**newsDefaultGet()**](NewsDefaultApi.md#newsDefaultGet) | **GET** /news/default | Get published article list for cursor |
| [**newsDefaultIdDesktopGet()**](NewsDefaultApi.md#newsDefaultIdDesktopGet) | **GET** /news/default/{id}/desktop | Get article desktop |
| [**newsDefaultIdGet()**](NewsDefaultApi.md#newsDefaultIdGet) | **GET** /news/default/{id} | Get article mobile |
| [**newsDefaultPostCountIdGet()**](NewsDefaultApi.md#newsDefaultPostCountIdGet) | **GET** /news/default/post-count/{id} | Get article post count |
| [**newsDefaultPostCountProjectIdGet()**](NewsDefaultApi.md#newsDefaultPostCountProjectIdGet) | **GET** /news/default/post-count/project/{id} | Get article post counts for project |
| [**newsDefaultProjectIdGet()**](NewsDefaultApi.md#newsDefaultProjectIdGet) | **GET** /news/default/project/{id} | Get published article list for project |
| [**newsDefaultProjectIdIdsGet()**](NewsDefaultApi.md#newsDefaultProjectIdIdsGet) | **GET** /news/default/project/{id}/ids | Get published article ids for project |
| [**newsDefaultSearchPost()**](NewsDefaultApi.md#newsDefaultSearchPost) | **POST** /news/default/search | Create cursor |


## `newsDefaultGet()`

```php
newsDefaultGet($cursor, $page, $limit, $accept_language, $session): \OpenAPI\Client\Model\NewsArticleResponseListDefault[]
```

Get published article list for cursor

This endpoint returns a list of all articles for a cursor without content in default representation.  Cursor could be created for published view here: POST /news/default/search  Cursor could be created for preview view here: POST /news/default/preview/search  _accessible without permission_

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\NewsDefaultApi(
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
    $result = $apiInstance->newsDefaultGet($cursor, $page, $limit, $accept_language, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NewsDefaultApi->newsDefaultGet: ', $e->getMessage(), PHP_EOL;
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

[**\OpenAPI\Client\Model\NewsArticleResponseListDefault[]**](../Model/NewsArticleResponseListDefault.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `newsDefaultIdDesktopGet()`

```php
newsDefaultIdDesktopGet($id, $accept_language, $session): \OpenAPI\Client\Model\NewsDefaultIdGet200Response
```

Get article desktop

This endpoint returns a localized article for desktop in default user representation by given id. If there is no specific desktop version of the article the standard (mobile) version of the article will be selected.  For preview use: GET /news/default/{id}/preview/desktop  _accessible without permission_  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\NewsDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Article ID
$accept_language = 'accept_language_example'; // string | client language(s)
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->newsDefaultIdDesktopGet($id, $accept_language, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NewsDefaultApi->newsDefaultIdDesktopGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Article ID | |
| **accept_language** | **string**| client language(s) | [optional] |
| **session** | **string**| JWT | [optional] |

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

## `newsDefaultIdGet()`

```php
newsDefaultIdGet($id, $accept_language, $session): \OpenAPI\Client\Model\NewsDefaultIdGet200Response
```

Get article mobile

This endpoint returns a localized article in default user representation by given id.  For preview use: GET /news/default/{id}/preview  _accessible without permission_  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\NewsDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Article ID
$accept_language = 'accept_language_example'; // string | client language(s)
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->newsDefaultIdGet($id, $accept_language, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NewsDefaultApi->newsDefaultIdGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Article ID | |
| **accept_language** | **string**| client language(s) | [optional] |
| **session** | **string**| JWT | [optional] |

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

## `newsDefaultPostCountIdGet()`

```php
newsDefaultPostCountIdGet($id, $session): \OpenAPI\Client\Model\NewsArticlePostCountResponse
```

Get article post count

This endpoint returns the post count of the requested article.  _accessible without permission_  _fully accessible with permission_ : `\"ManageContent\" (counts also for linked projects)` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\NewsDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Article ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->newsDefaultPostCountIdGet($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NewsDefaultApi->newsDefaultPostCountIdGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Article ID | |
| **session** | **string**| JWT | |

### Return type

[**\OpenAPI\Client\Model\NewsArticlePostCountResponse**](../Model/NewsArticlePostCountResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `newsDefaultPostCountProjectIdGet()`

```php
newsDefaultPostCountProjectIdGet($id, $session, $cursor, $limit, $page): \OpenAPI\Client\Model\NewsArticlePostCountResponse[]
```

Get article post counts for project

This endpoint returns a list of post counts for all published articles with social interaction activated of the requested project. If a limit is set, a cursor for this endpoint may be created to iterate over all article post counts.  _accessible without permission_  _fully accessible with permission_ : `\"ManageContent\" (counts also for linked projects)` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\NewsDefaultApi(
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
    $result = $apiInstance->newsDefaultPostCountProjectIdGet($id, $session, $cursor, $limit, $page);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NewsDefaultApi->newsDefaultPostCountProjectIdGet: ', $e->getMessage(), PHP_EOL;
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

[**\OpenAPI\Client\Model\NewsArticlePostCountResponse[]**](../Model/NewsArticlePostCountResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `newsDefaultProjectIdGet()`

```php
newsDefaultProjectIdGet($id, $cursor, $limit, $page, $accept_language, $session): \OpenAPI\Client\Model\NewsArticleResponseListDefault[]
```

Get published article list for project

This endpoint returns a list of all published articles for the requested project without content in default representation. The entries are sorted by `publishedAt:DESC`. If a limit is set, a cursor for this endpoint may be created to iterate over all articles.  For preview list use: GET /news/default/project/{id}/preview  _accessible without permission_  _fully accessible with permission_ : `\"ManageContent\" (counts also for linked projects)` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\NewsDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Project ID
$cursor = 'cursor_example'; // string | id of the cursor used for pagination; required if page is set
$limit = 56; // int | amount of results per page (1 ... 100)
$page = 56; // int | current page index of the cursor used for pagination; required if cursor is set
$accept_language = 'accept_language_example'; // string | client language(s)
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->newsDefaultProjectIdGet($id, $cursor, $limit, $page, $accept_language, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NewsDefaultApi->newsDefaultProjectIdGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Project ID | |
| **cursor** | **string**| id of the cursor used for pagination; required if page is set | [optional] |
| **limit** | **int**| amount of results per page (1 ... 100) | [optional] |
| **page** | **int**| current page index of the cursor used for pagination; required if cursor is set | [optional] |
| **accept_language** | **string**| client language(s) | [optional] |
| **session** | **string**| JWT | [optional] |

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

## `newsDefaultProjectIdIdsGet()`

```php
newsDefaultProjectIdIdsGet($id, $session): string[]
```

Get published article ids for project

This endpoint returns ids of all published articles for the requested project. The entries are sorted by `publishedAt:DESC`.  For preview list ids use: GET /news/default/project/{id}/preview/ids  _accessible without permission_  _fully accessible with permission_ : `\"ManageContent\" (counts also for linked projects)` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\NewsDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Project ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->newsDefaultProjectIdIdsGet($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NewsDefaultApi->newsDefaultProjectIdIdsGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Project ID | |
| **session** | **string**| JWT | [optional] |

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

## `newsDefaultSearchPost()`

```php
newsDefaultSearchPost($request, $accept_language, $session): \OpenAPI\Client\Model\ModelCursorResponse
```

Create cursor

This endpoint returns a cursor for list published articles in default representation with applied filter and sort options. In case of cursor response total will be 0 the status 204 with not content is returned instead.  For preview list cursor use: GET /news/default/preview/search  _accessible without permission_  _fully accessible with permission_ : `\"ManageContent\" (counts also for linked projects)` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\NewsDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$request = new \OpenAPI\Client\Model\NewsCursorRequestDefault(); // \OpenAPI\Client\Model\NewsCursorRequestDefault | options to create cursor
$accept_language = 'accept_language_example'; // string | client language(s)
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->newsDefaultSearchPost($request, $accept_language, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NewsDefaultApi->newsDefaultSearchPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **request** | [**\OpenAPI\Client\Model\NewsCursorRequestDefault**](../Model/NewsCursorRequestDefault.md)| options to create cursor | |
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
