# OpenAPI\Client\AuthApi



All URIs are relative to https://custom.polario.de/api, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**authAuthPost()**](AuthApi.md#authAuthPost) | **POST** /auth/auth | SCRAM First |


## `authAuthPost()`

```php
authAuthPost($request, $platform): \OpenAPI\Client\Model\AuthAuthenticationResponse
```

SCRAM First

This endpoint provides the first message of a salted challenge response authentication mechanism (SCRAM). This challenge is used to validate the users password. It is used to perform login or change password with old password. The _Platform_ header is for creating session use range. See RFC 5802 for detail SCRAM definition.  _accessible without permission_

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\AuthApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$request = new \OpenAPI\Client\Model\AuthAuthenticationRequest(); // \OpenAPI\Client\Model\AuthAuthenticationRequest | Clients First Message
$platform = 'platform_example'; // string | The client platform

try {
    $result = $apiInstance->authAuthPost($request, $platform);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AuthApi->authAuthPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **request** | [**\OpenAPI\Client\Model\AuthAuthenticationRequest**](../Model/AuthAuthenticationRequest.md)| Clients First Message | |
| **platform** | **string**| The client platform | [optional] |

### Return type

[**\OpenAPI\Client\Model\AuthAuthenticationResponse**](../Model/AuthAuthenticationResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
