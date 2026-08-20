# OpenAPI\Client\RecommendationApi



All URIs are relative to https://custom.polario.de/api, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**recommendationGet()**](RecommendationApi.md#recommendationGet) | **GET** /recommendation | Get recommendation list |
| [**recommendationObjectTypeGet()**](RecommendationApi.md#recommendationObjectTypeGet) | **GET** /recommendation/{objectType} | Get recommendation sorted |
| [**recommendationObjectTypeRandomGet()**](RecommendationApi.md#recommendationObjectTypeRandomGet) | **GET** /recommendation/{objectType}/random | Get recommendation random |
| [**recommendationObjectTypeRerollPost()**](RecommendationApi.md#recommendationObjectTypeRerollPost) | **POST** /recommendation/{objectType}/reroll | Reroll account matches |
| [**recommendationSearchPost()**](RecommendationApi.md#recommendationSearchPost) | **POST** /recommendation/search | Create cursor recommendations |


## `recommendationGet()`

```php
recommendationGet($cursor, $page, $session, $limit): \OpenAPI\Client\Model\RecommendationMatchResponse[]
```

Get recommendation list

This endpoint returns an array of all recommendations for a cursor.  Cursor could be created here: POST /recommendation/search  _accessible without permission_

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\RecommendationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$cursor = 'cursor_example'; // string | id of the cursor used for pagination; required if page is set
$page = 56; // int | current page index of the cursor used for pagination; required if cursor is set
$session = 'session_example'; // string | JWT
$limit = 56; // int | amount of results per page (1 ... 100)

try {
    $result = $apiInstance->recommendationGet($cursor, $page, $session, $limit);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RecommendationApi->recommendationGet: ', $e->getMessage(), PHP_EOL;
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

[**\OpenAPI\Client\Model\RecommendationMatchResponse[]**](../Model/RecommendationMatchResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `recommendationObjectTypeGet()`

```php
recommendationObjectTypeGet($object_type, $session): \OpenAPI\Client\Model\RecommendationMatchResponse[]
```

Get recommendation sorted

This endpoint returns sorted recommendations for the requesting account.  _accessible without permission_

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\RecommendationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$object_type = 'object_type_example'; // string | object type
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->recommendationObjectTypeGet($object_type, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RecommendationApi->recommendationObjectTypeGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **object_type** | **string**| object type | |
| **session** | **string**| JWT | |

### Return type

[**\OpenAPI\Client\Model\RecommendationMatchResponse[]**](../Model/RecommendationMatchResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `recommendationObjectTypeRandomGet()`

```php
recommendationObjectTypeRandomGet($object_type, $session): \OpenAPI\Client\Model\RecommendationMatchResponse[]
```

Get recommendation random

This endpoint returns random recommendations for the requesting account.  _accessible without permission_

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\RecommendationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$object_type = 'object_type_example'; // string | object type
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->recommendationObjectTypeRandomGet($object_type, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RecommendationApi->recommendationObjectTypeRandomGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **object_type** | **string**| object type | |
| **session** | **string**| JWT | |

### Return type

[**\OpenAPI\Client\Model\RecommendationMatchResponse[]**](../Model/RecommendationMatchResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `recommendationObjectTypeRerollPost()`

```php
recommendationObjectTypeRerollPost($object_type, $session, $request): \OpenAPI\Client\Model\RecommendationMatchResponse[]
```

Reroll account matches

This endpoint returns new recommendations for the requesting account.  _accessible without permission_

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\RecommendationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$object_type = 'object_type_example'; // string | object type
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\RecommendationRerollRequest(); // \OpenAPI\Client\Model\RecommendationRerollRequest | keep and change lists

try {
    $result = $apiInstance->recommendationObjectTypeRerollPost($object_type, $session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RecommendationApi->recommendationObjectTypeRerollPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **object_type** | **string**| object type | |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\RecommendationRerollRequest**](../Model/RecommendationRerollRequest.md)| keep and change lists | |

### Return type

[**\OpenAPI\Client\Model\RecommendationMatchResponse[]**](../Model/RecommendationMatchResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `recommendationSearchPost()`

```php
recommendationSearchPost($session, $request): \OpenAPI\Client\Model\ModelCursorResponse
```

Create cursor recommendations

This endpoint creates a cursor for list recommendations with applied filter and sort options. In case of cursor response total will be 0 the status 204 with no content is returned instead.  _accessible without permission_

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\RecommendationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\RecommendationCursorRequest(); // \OpenAPI\Client\Model\RecommendationCursorRequest | options to create cursor

try {
    $result = $apiInstance->recommendationSearchPost($session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RecommendationApi->recommendationSearchPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\RecommendationCursorRequest**](../Model/RecommendationCursorRequest.md)| options to create cursor | |

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
