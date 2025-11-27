# OpenAPI\Client\ProjectApi



All URIs are relative to https://custom.polario.de/api, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**projectDefaultIdGuestVisitPut()**](ProjectApi.md#projectDefaultIdGuestVisitPut) | **PUT** /project/default/{id}/guest-visit | guest visit |


## `projectDefaultIdGuestVisitPut()`

```php
projectDefaultIdGuestVisitPut($id, $request): \OpenAPI\Client\Model\ModelSwagStatusOk
```

guest visit

This endpoint is for tracking guest account.  _accessible without permission_

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\ProjectApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Project ID
$request = new \OpenAPI\Client\Model\GuestvisitRequest(); // \OpenAPI\Client\Model\GuestvisitRequest | device id

try {
    $result = $apiInstance->projectDefaultIdGuestVisitPut($id, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProjectApi->projectDefaultIdGuestVisitPut: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Project ID | |
| **request** | [**\OpenAPI\Client\Model\GuestvisitRequest**](../Model/GuestvisitRequest.md)| device id | |

### Return type

[**\OpenAPI\Client\Model\ModelSwagStatusOk**](../Model/ModelSwagStatusOk.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
