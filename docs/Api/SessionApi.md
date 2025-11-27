# OpenAPI\Client\SessionApi



All URIs are relative to https://custom.polario.de/api, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**authLoginPost()**](SessionApi.md#authLoginPost) | **POST** /auth/login | Login |
| [**authLogoutGet()**](SessionApi.md#authLogoutGet) | **GET** /auth/logout | Logout |
| [**authSessionPost()**](SessionApi.md#authSessionPost) | **POST** /auth/session | Refresh |


## `authLoginPost()`

```php
authLoginPost($request, $platform): \OpenAPI\Client\Model\AuthLoginResponse
```

Login

This endpoint provides the login with a salted challenge response authentication mechanism (SCRAM). This endpoint is for the final message of the SCRAM challenge. The platform must match the platform from the first message. See RFC 5802 for detail SCRAM definition.  To perform this action call SCRAM First first: POST /auth/auth  _accessible without permission_

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\SessionApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$request = new \OpenAPI\Client\Model\AuthLoginRequest(); // \OpenAPI\Client\Model\AuthLoginRequest | Clients Final Message
$platform = 'platform_example'; // string | The client platform

try {
    $result = $apiInstance->authLoginPost($request, $platform);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SessionApi->authLoginPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **request** | [**\OpenAPI\Client\Model\AuthLoginRequest**](../Model/AuthLoginRequest.md)| Clients Final Message | |
| **platform** | **string**| The client platform | [optional] |

### Return type

[**\OpenAPI\Client\Model\AuthLoginResponse**](../Model/AuthLoginResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `authLogoutGet()`

```php
authLogoutGet($session): \OpenAPI\Client\Model\ModelSwagStatusOk
```

Logout

This endpoint finish current session and invalidates the refresh token for this session.  _accessible without permission_

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\SessionApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->authLogoutGet($session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SessionApi->authLogoutGet: ', $e->getMessage(), PHP_EOL;
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

## `authSessionPost()`

```php
authSessionPost($request): \OpenAPI\Client\Model\AuthRefreshResponse
```

Refresh

This endpoint refreshes a JWT with given refresh token and return it in the response header. If refresh token is invalid it will return 416 Requested Range Not Satisfiable.  _accessible without permission_

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\SessionApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$request = new \OpenAPI\Client\Model\AuthRefreshRequest(); // \OpenAPI\Client\Model\AuthRefreshRequest | refresh token

try {
    $result = $apiInstance->authSessionPost($request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SessionApi->authSessionPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **request** | [**\OpenAPI\Client\Model\AuthRefreshRequest**](../Model/AuthRefreshRequest.md)| refresh token | |

### Return type

[**\OpenAPI\Client\Model\AuthRefreshResponse**](../Model/AuthRefreshResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
