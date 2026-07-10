# OpenAPI\Client\LocationDefaultApi



All URIs are relative to https://custom.polario.de/api, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**locationDefaultGet()**](LocationDefaultApi.md#locationDefaultGet) | **GET** /location/default | Get location list |
| [**locationDefaultIdGet()**](LocationDefaultApi.md#locationDefaultIdGet) | **GET** /location/default/{id} | Get location |
| [**locationDefaultIdReservationPost()**](LocationDefaultApi.md#locationDefaultIdReservationPost) | **POST** /location/default/{id}/reservation | Create location reservation |
| [**locationDefaultPlaceConfigGet()**](LocationDefaultApi.md#locationDefaultPlaceConfigGet) | **GET** /location/default/place/config | Get places config |
| [**locationDefaultProjectIdGet()**](LocationDefaultApi.md#locationDefaultProjectIdGet) | **GET** /location/default/project/{id} | Get location list for project |
| [**locationDefaultReservationDelete()**](LocationDefaultApi.md#locationDefaultReservationDelete) | **DELETE** /location/default/reservation | Delete location reservation |
| [**locationDefaultSearchPost()**](LocationDefaultApi.md#locationDefaultSearchPost) | **POST** /location/default/search | Create cursor |


## `locationDefaultGet()`

```php
locationDefaultGet($cursor, $page, $limit, $accept_language, $session): \OpenAPI\Client\Model\LocationResponseDefault[]
```

Get location list

This endpoint returns an array of all locations for a cursor. The output is in default representation and filtered for the user permissions.  Cursor could be created here: POST /location/default/search  _accessible without permission_

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\LocationDefaultApi(
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
    $result = $apiInstance->locationDefaultGet($cursor, $page, $limit, $accept_language, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LocationDefaultApi->locationDefaultGet: ', $e->getMessage(), PHP_EOL;
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

[**\OpenAPI\Client\Model\LocationResponseDefault[]**](../Model/LocationResponseDefault.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `locationDefaultIdGet()`

```php
locationDefaultIdGet($id, $accept_language, $session): \OpenAPI\Client\Model\LocationResponseDefault
```

Get location

This endpoint returns a location in default representation by given id. If the requested language is not available it will fall back to the default language.  _accessible without permission_  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\LocationDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Location ID
$accept_language = 'accept_language_example'; // string | client language(s)
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->locationDefaultIdGet($id, $accept_language, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LocationDefaultApi->locationDefaultIdGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Location ID | |
| **accept_language** | **string**| client language(s) | [optional] |
| **session** | **string**| JWT | [optional] |

### Return type

[**\OpenAPI\Client\Model\LocationResponseDefault**](../Model/LocationResponseDefault.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `locationDefaultIdReservationPost()`

```php
locationDefaultIdReservationPost($id, $session, $request): \OpenAPI\Client\Model\LocationreservationResponse
```

Create location reservation

This endpoint is for creating a new location reservation. Calling this endpoint will remove already existing reservations. Only one reservation per user is permitted.  _accessible without permission_  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\LocationDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Location ID
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\LocationreservationRequest(); // \OpenAPI\Client\Model\LocationreservationRequest | Reservation to create

try {
    $result = $apiInstance->locationDefaultIdReservationPost($id, $session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LocationDefaultApi->locationDefaultIdReservationPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Location ID | |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\LocationreservationRequest**](../Model/LocationreservationRequest.md)| Reservation to create | |

### Return type

[**\OpenAPI\Client\Model\LocationreservationResponse**](../Model/LocationreservationResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `locationDefaultPlaceConfigGet()`

```php
locationDefaultPlaceConfigGet($session): \OpenAPI\Client\Model\PlaceConfigResponseDefault
```

Get places config

This endpoint returns config for places search. It provides the google places api key.  _accessible without permission_

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\LocationDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->locationDefaultPlaceConfigGet($session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LocationDefaultApi->locationDefaultPlaceConfigGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **session** | **string**| JWT | |

### Return type

[**\OpenAPI\Client\Model\PlaceConfigResponseDefault**](../Model/PlaceConfigResponseDefault.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `locationDefaultProjectIdGet()`

```php
locationDefaultProjectIdGet($id, $cursor, $limit, $page, $accept_language, $session): \OpenAPI\Client\Model\LocationResponseListDefault[]
```

Get location list for project

This endpoint returns a list of all locations for the requested project. If the requested language is not available it will fall back to the default language. If a limit is set, a cursor for this endpoint may be created to iterate over all locations.  _accessible without permission_  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\LocationDefaultApi(
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
    $result = $apiInstance->locationDefaultProjectIdGet($id, $cursor, $limit, $page, $accept_language, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LocationDefaultApi->locationDefaultProjectIdGet: ', $e->getMessage(), PHP_EOL;
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

[**\OpenAPI\Client\Model\LocationResponseListDefault[]**](../Model/LocationResponseListDefault.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `locationDefaultReservationDelete()`

```php
locationDefaultReservationDelete($session): \OpenAPI\Client\Model\ModelSwagStatusOk
```

Delete location reservation

This endpoint is for deleting location reservations for a user.  _accessible without permission_

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\LocationDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->locationDefaultReservationDelete($session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LocationDefaultApi->locationDefaultReservationDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
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

## `locationDefaultSearchPost()`

```php
locationDefaultSearchPost($request, $accept_language, $session): \OpenAPI\Client\Model\ModelCursorResponse
```

Create cursor

This endpoint returns a cursor for list locations in default representation with applied filter and sort options. In case of cursor response total will be 0 the status 204 with not content is returned instead.  _accessible without permission_  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\LocationDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$request = new \OpenAPI\Client\Model\LocationCursorRequestDefault(); // \OpenAPI\Client\Model\LocationCursorRequestDefault | options to create cursor
$accept_language = 'accept_language_example'; // string | client language(s)
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->locationDefaultSearchPost($request, $accept_language, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LocationDefaultApi->locationDefaultSearchPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **request** | [**\OpenAPI\Client\Model\LocationCursorRequestDefault**](../Model/LocationCursorRequestDefault.md)| options to create cursor | |
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
