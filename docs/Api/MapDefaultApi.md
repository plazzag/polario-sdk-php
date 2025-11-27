# OpenAPI\Client\MapDefaultApi



All URIs are relative to https://custom.polario.de/api, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**locationDefaultMapIdGet()**](MapDefaultApi.md#locationDefaultMapIdGet) | **GET** /location/default/map/{id} | Get map |


## `locationDefaultMapIdGet()`

```php
locationDefaultMapIdGet($id, $accept_language, $session): \OpenAPI\Client\Model\LocationmapResponseDefault
```

Get map

This endpoint returns a location map in default representation by given id. If the requested language is not available it will fall back to the default language.  _accessible without permission_  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\MapDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Map ID
$accept_language = 'accept_language_example'; // string | client language(s)
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->locationDefaultMapIdGet($id, $accept_language, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MapDefaultApi->locationDefaultMapIdGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Map ID | |
| **accept_language** | **string**| client language(s) | [optional] |
| **session** | **string**| JWT | [optional] |

### Return type

[**\OpenAPI\Client\Model\LocationmapResponseDefault**](../Model/LocationmapResponseDefault.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
