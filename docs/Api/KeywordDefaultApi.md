# OpenAPI\Client\KeywordDefaultApi



All URIs are relative to https://custom.polario.de/api, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**keywordDefaultCategoryGet()**](KeywordDefaultApi.md#keywordDefaultCategoryGet) | **GET** /keyword/default/category | Get keyword category list |
| [**keywordDefaultCategoryIdGet()**](KeywordDefaultApi.md#keywordDefaultCategoryIdGet) | **GET** /keyword/default/category/{id} | Get keyword category |
| [**keywordDefaultGet()**](KeywordDefaultApi.md#keywordDefaultGet) | **GET** /keyword/default | Get keyword list |


## `keywordDefaultCategoryGet()`

```php
keywordDefaultCategoryGet($cursor, $limit, $page): \OpenAPI\Client\Model\KeywordcategoryResponseDefault[]
```

Get keyword category list

This endpoint returns a list of all keyword categories in default representation.  _accessible without permission_

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\KeywordDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$cursor = 'cursor_example'; // string | id of the cursor used for pagination; required if page is set
$limit = 56; // int | amount of results per page (1 ... 100); by default no limit (no pagination headers) currently; only allowed if cursor is not set
$page = 56; // int | current page index of the cursor used for pagination; required if cursor is set

try {
    $result = $apiInstance->keywordDefaultCategoryGet($cursor, $limit, $page);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling KeywordDefaultApi->keywordDefaultCategoryGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **cursor** | **string**| id of the cursor used for pagination; required if page is set | [optional] |
| **limit** | **int**| amount of results per page (1 ... 100); by default no limit (no pagination headers) currently; only allowed if cursor is not set | [optional] |
| **page** | **int**| current page index of the cursor used for pagination; required if cursor is set | [optional] |

### Return type

[**\OpenAPI\Client\Model\KeywordcategoryResponseDefault[]**](../Model/KeywordcategoryResponseDefault.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `keywordDefaultCategoryIdGet()`

```php
keywordDefaultCategoryIdGet($id): \OpenAPI\Client\Model\KeywordcategoryResponseDefault
```

Get keyword category

This endpoint returns a localized keyword category by given id in default representation.  _accessible without permission_

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\KeywordDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Category ID

try {
    $result = $apiInstance->keywordDefaultCategoryIdGet($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling KeywordDefaultApi->keywordDefaultCategoryIdGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Category ID | |

### Return type

[**\OpenAPI\Client\Model\KeywordcategoryResponseDefault**](../Model/KeywordcategoryResponseDefault.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `keywordDefaultGet()`

```php
keywordDefaultGet($cursor, $limit, $page, $accept_language, $session): \OpenAPI\Client\Model\KeywordResponseDefault[]
```

Get keyword list

This endpoint returns a list of all keywords in default representation. If the requested language is not available it will fall back to the default language. If a limit is set, a cursor for this endpoint may be created to iterate over all keywords.  _accessible without permission_

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\KeywordDefaultApi(
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
    $result = $apiInstance->keywordDefaultGet($cursor, $limit, $page, $accept_language, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling KeywordDefaultApi->keywordDefaultGet: ', $e->getMessage(), PHP_EOL;
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

[**\OpenAPI\Client\Model\KeywordResponseDefault[]**](../Model/KeywordResponseDefault.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
