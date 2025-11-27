# OpenAPI\Client\StreamDefaultApi



All URIs are relative to https://custom.polario.de/api, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**streamDefaultIdGet()**](StreamDefaultApi.md#streamDefaultIdGet) | **GET** /stream/default/{id} | Get stream |
| [**streamDefaultIdWatchGet()**](StreamDefaultApi.md#streamDefaultIdWatchGet) | **GET** /stream/default/{id}/watch | Get stream viewer count |
| [**streamDefaultIdWatchPut()**](StreamDefaultApi.md#streamDefaultIdWatchPut) | **PUT** /stream/default/{id}/watch | Set stream viewer |


## `streamDefaultIdGet()`

```php
streamDefaultIdGet($id, $session): \OpenAPI\Client\Model\StreamResponseDefault
```

Get stream

This endpoint returns a stream in default representation by given id.  _accessible without permission_  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\StreamDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Stream ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->streamDefaultIdGet($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StreamDefaultApi->streamDefaultIdGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Stream ID | |
| **session** | **string**| JWT | [optional] |

### Return type

[**\OpenAPI\Client\Model\StreamResponseDefault**](../Model/StreamResponseDefault.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `streamDefaultIdWatchGet()`

```php
streamDefaultIdWatchGet($id, $session): \OpenAPI\Client\Model\StreamResponseViewerCount
```

Get stream viewer count

This endpoint returns the amount of current viewers for a stream.  _accessible without permission_  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\StreamDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Stream ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->streamDefaultIdWatchGet($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StreamDefaultApi->streamDefaultIdWatchGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Stream ID | |
| **session** | **string**| JWT | [optional] |

### Return type

[**\OpenAPI\Client\Model\StreamResponseViewerCount**](../Model/StreamResponseViewerCount.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `streamDefaultIdWatchPut()`

```php
streamDefaultIdWatchPut($id, $user_identification, $session): \OpenAPI\Client\Model\StreamResponseViewerCount
```

Set stream viewer

This endpoint should be called periodically __(every 5 min)__ as long as a person is viewing a stream. It returns the amount of current viewers for a stream.  _accessible without permission_  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\StreamDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Stream ID
$user_identification = 'user_identification_example'; // string | uid to handle user specific content without session
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->streamDefaultIdWatchPut($id, $user_identification, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StreamDefaultApi->streamDefaultIdWatchPut: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Stream ID | |
| **user_identification** | **string**| uid to handle user specific content without session | [optional] |
| **session** | **string**| JWT | [optional] |

### Return type

[**\OpenAPI\Client\Model\StreamResponseViewerCount**](../Model/StreamResponseViewerCount.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
