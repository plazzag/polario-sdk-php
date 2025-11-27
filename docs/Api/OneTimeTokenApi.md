# OpenAPI\Client\OneTimeTokenApi



All URIs are relative to https://custom.polario.de/api, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**authOttValidatePost()**](OneTimeTokenApi.md#authOttValidatePost) | **POST** /auth/ott/validate | Validate one time token |


## `authOttValidatePost()`

```php
authOttValidatePost($request, $platform): \OpenAPI\Client\Model\ModelSwagStatusOk
```

Validate one time token

This endpoint validates given one time token. The one time token must also match the platform. Only if provided token is valid it returns 200.  _accessible without permission_

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\OneTimeTokenApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$request = new \OpenAPI\Client\Model\AuthOttValidateRequest(); // \OpenAPI\Client\Model\AuthOttValidateRequest | one time token
$platform = 'platform_example'; // string | The client platform

try {
    $result = $apiInstance->authOttValidatePost($request, $platform);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OneTimeTokenApi->authOttValidatePost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **request** | [**\OpenAPI\Client\Model\AuthOttValidateRequest**](../Model/AuthOttValidateRequest.md)| one time token | |
| **platform** | **string**| The client platform | [optional] |

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
