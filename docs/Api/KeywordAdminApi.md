# OpenAPI\Client\KeywordAdminApi



All URIs are relative to https://custom.polario.de/api, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**keywordAdminCategoryGet()**](KeywordAdminApi.md#keywordAdminCategoryGet) | **GET** /keyword/admin/category | Get keyword category list |
| [**keywordAdminCategoryIdDelete()**](KeywordAdminApi.md#keywordAdminCategoryIdDelete) | **DELETE** /keyword/admin/category/{id} | Delete keyword category |
| [**keywordAdminCategoryIdGet()**](KeywordAdminApi.md#keywordAdminCategoryIdGet) | **GET** /keyword/admin/category/{id} | Get keyword category |
| [**keywordAdminCategoryIdPatch()**](KeywordAdminApi.md#keywordAdminCategoryIdPatch) | **PATCH** /keyword/admin/category/{id} | Update keyword category |
| [**keywordAdminCategoryPost()**](KeywordAdminApi.md#keywordAdminCategoryPost) | **POST** /keyword/admin/category | Create keyword category |
| [**keywordAdminGet()**](KeywordAdminApi.md#keywordAdminGet) | **GET** /keyword/admin | Get keyword list |
| [**keywordAdminIdDelete()**](KeywordAdminApi.md#keywordAdminIdDelete) | **DELETE** /keyword/admin/{id} | Delete keyword |
| [**keywordAdminIdGet()**](KeywordAdminApi.md#keywordAdminIdGet) | **GET** /keyword/admin/{id} | Get keyword |
| [**keywordAdminIdPatch()**](KeywordAdminApi.md#keywordAdminIdPatch) | **PATCH** /keyword/admin/{id} | Update keyword |
| [**keywordAdminPost()**](KeywordAdminApi.md#keywordAdminPost) | **POST** /keyword/admin | Create keyword |


## `keywordAdminCategoryGet()`

```php
keywordAdminCategoryGet($session, $cursor, $limit, $page): \OpenAPI\Client\Model\KeywordcategoryResponseAdmin[]
```

Get keyword category list

This endpoint returns a list of all keyword categories in admin representation.  _accessible without permission_  _fully accessible with permission_ : `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\KeywordAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT
$cursor = 'cursor_example'; // string | id of the cursor used for pagination; required if page is set
$limit = 56; // int | amount of results per page (1 ... 100); by default no limit (no pagination headers) currently; only allowed if cursor is not set
$page = 56; // int | current page index of the cursor used for pagination; required if cursor is set

try {
    $result = $apiInstance->keywordAdminCategoryGet($session, $cursor, $limit, $page);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling KeywordAdminApi->keywordAdminCategoryGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **session** | **string**| JWT | |
| **cursor** | **string**| id of the cursor used for pagination; required if page is set | [optional] |
| **limit** | **int**| amount of results per page (1 ... 100); by default no limit (no pagination headers) currently; only allowed if cursor is not set | [optional] |
| **page** | **int**| current page index of the cursor used for pagination; required if cursor is set | [optional] |

### Return type

[**\OpenAPI\Client\Model\KeywordcategoryResponseAdmin[]**](../Model/KeywordcategoryResponseAdmin.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `keywordAdminCategoryIdDelete()`

```php
keywordAdminCategoryIdDelete($id, $session): \OpenAPI\Client\Model\ModelSwagStatusOk
```

Delete keyword category

This endpoint is for deleting a single keyword category Remove all references in keywords, do not delete keywords  _accessible without permission_  _fully accessible with permission_ : `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\KeywordAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Category ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->keywordAdminCategoryIdDelete($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling KeywordAdminApi->keywordAdminCategoryIdDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Category ID | |
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

## `keywordAdminCategoryIdGet()`

```php
keywordAdminCategoryIdGet($id, $session): \OpenAPI\Client\Model\KeywordcategoryResponseAdmin
```

Get keyword category

This endpoint returns a localized keyword category by given id in admin representation.  _accessible without permission_  _fully accessible with permission_ : `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\KeywordAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Category ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->keywordAdminCategoryIdGet($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling KeywordAdminApi->keywordAdminCategoryIdGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Category ID | |
| **session** | **string**| JWT | |

### Return type

[**\OpenAPI\Client\Model\KeywordcategoryResponseAdmin**](../Model/KeywordcategoryResponseAdmin.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `keywordAdminCategoryIdPatch()`

```php
keywordAdminCategoryIdPatch($id, $session, $request): \OpenAPI\Client\Model\KeywordcategoryResponseAdmin
```

Update keyword category

This endpoint is for updating keyword category.  _accessible without permission_  _fully accessible with permission_ : `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\KeywordAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Category ID
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\KeywordcategoryRequest(); // \OpenAPI\Client\Model\KeywordcategoryRequest | keyword category information to be updated

try {
    $result = $apiInstance->keywordAdminCategoryIdPatch($id, $session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling KeywordAdminApi->keywordAdminCategoryIdPatch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Category ID | |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\KeywordcategoryRequest**](../Model/KeywordcategoryRequest.md)| keyword category information to be updated | |

### Return type

[**\OpenAPI\Client\Model\KeywordcategoryResponseAdmin**](../Model/KeywordcategoryResponseAdmin.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `keywordAdminCategoryPost()`

```php
keywordAdminCategoryPost($session, $request): \OpenAPI\Client\Model\KeywordcategoryResponseAdmin
```

Create keyword category

This endpoint is for creating a new keyword category.  _accessible without permission_  _fully accessible with permission_ : `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\KeywordAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\KeywordcategoryRequest(); // \OpenAPI\Client\Model\KeywordcategoryRequest | keyword category to create

try {
    $result = $apiInstance->keywordAdminCategoryPost($session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling KeywordAdminApi->keywordAdminCategoryPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\KeywordcategoryRequest**](../Model/KeywordcategoryRequest.md)| keyword category to create | |

### Return type

[**\OpenAPI\Client\Model\KeywordcategoryResponseAdmin**](../Model/KeywordcategoryResponseAdmin.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `keywordAdminGet()`

```php
keywordAdminGet($session, $cursor, $limit, $page): \OpenAPI\Client\Model\KeywordResponseAdmin[]
```

Get keyword list

This endpoint returns a list of all keywords in admin representation. If a limit is set, a cursor for this endpoint may be created to iterate over all keywords.  _accessible without permission_  _fully accessible with permission_ : `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\KeywordAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT
$cursor = 'cursor_example'; // string | id of the cursor used for pagination; required if page is set
$limit = 56; // int | amount of results per page (1 ... 100)
$page = 56; // int | current page index of the cursor used for pagination; required if cursor is set

try {
    $result = $apiInstance->keywordAdminGet($session, $cursor, $limit, $page);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling KeywordAdminApi->keywordAdminGet: ', $e->getMessage(), PHP_EOL;
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

[**\OpenAPI\Client\Model\KeywordResponseAdmin[]**](../Model/KeywordResponseAdmin.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `keywordAdminIdDelete()`

```php
keywordAdminIdDelete($id, $session): \OpenAPI\Client\Model\ModelSwagStatusOk
```

Delete keyword

This endpoint is for deleting a single keyword.  _accessible without permission_  _fully accessible with permission_ : `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\KeywordAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Keyword ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->keywordAdminIdDelete($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling KeywordAdminApi->keywordAdminIdDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Keyword ID | |
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

## `keywordAdminIdGet()`

```php
keywordAdminIdGet($id, $session): \OpenAPI\Client\Model\KeywordResponseAdmin
```

Get keyword

This endpoint returns a localized keyword by given id in admin representation.  _accessible without permission_  _fully accessible with permission_ : `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\KeywordAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Keyword ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->keywordAdminIdGet($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling KeywordAdminApi->keywordAdminIdGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Keyword ID | |
| **session** | **string**| JWT | |

### Return type

[**\OpenAPI\Client\Model\KeywordResponseAdmin**](../Model/KeywordResponseAdmin.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `keywordAdminIdPatch()`

```php
keywordAdminIdPatch($id, $session, $request): \OpenAPI\Client\Model\KeywordResponseAdmin
```

Update keyword

This endpoint is for updating keyword.  _accessible without permission_  _fully accessible with permission_ : `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\KeywordAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Keyword ID
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\KeywordPatchRequest(); // \OpenAPI\Client\Model\KeywordPatchRequest | keyword information to be updated

try {
    $result = $apiInstance->keywordAdminIdPatch($id, $session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling KeywordAdminApi->keywordAdminIdPatch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Keyword ID | |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\KeywordPatchRequest**](../Model/KeywordPatchRequest.md)| keyword information to be updated | |

### Return type

[**\OpenAPI\Client\Model\KeywordResponseAdmin**](../Model/KeywordResponseAdmin.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `keywordAdminPost()`

```php
keywordAdminPost($session, $request): \OpenAPI\Client\Model\KeywordResponseAdmin
```

Create keyword

This endpoint is for creating a new keyword.  _accessible without permission_  _fully accessible with permission_ : `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\KeywordAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\KeywordRequest(); // \OpenAPI\Client\Model\KeywordRequest | keyword to create

try {
    $result = $apiInstance->keywordAdminPost($session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling KeywordAdminApi->keywordAdminPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\KeywordRequest**](../Model/KeywordRequest.md)| keyword to create | |

### Return type

[**\OpenAPI\Client\Model\KeywordResponseAdmin**](../Model/KeywordResponseAdmin.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
