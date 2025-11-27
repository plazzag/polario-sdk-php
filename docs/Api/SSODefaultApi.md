# OpenAPI\Client\SSODefaultApi



All URIs are relative to https://custom.polario.de/api, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**authDefaultSsoProviderGet()**](SSODefaultApi.md#authDefaultSsoProviderGet) | **GET** /auth/default/sso-provider | Get all published sso provider |
| [**authSaml2IdGet()**](SSODefaultApi.md#authSaml2IdGet) | **GET** /auth/Saml2/{id} | Start a saml2 auth flow |
| [**authSaml2IdMetadataGet()**](SSODefaultApi.md#authSaml2IdMetadataGet) | **GET** /auth/Saml2/{id}/metadata | Generates a metadata.xml file |
| [**authSaml2IdResponsePost()**](SSODefaultApi.md#authSaml2IdResponsePost) | **POST** /auth/Saml2/{id}/response | Response endpoint of saml2 auth flow |
| [**authSsoCodePost()**](SSODefaultApi.md#authSsoCodePost) | **POST** /auth/sso-code | Create a session based on sso auth code |


## `authDefaultSsoProviderGet()`

```php
authDefaultSsoProviderGet($cursor, $limit, $page, $accept_language): \OpenAPI\Client\Model\SsoProviderResponseDefault[]
```

Get all published sso provider

This endpoint returns all sso-provider with content in default representation. If a limit is set, a cursor for this endpoint may be created to iterate over all sso-provider.  _accessible without permission_

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\SSODefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$cursor = 'cursor_example'; // string | id of the cursor used for pagination; required if page is set
$limit = 56; // int | amount of results per page (1 ... 100)
$page = 56; // int | current page index of the cursor used for pagination; required if cursor is set
$accept_language = 'accept_language_example'; // string | client language(s)

try {
    $result = $apiInstance->authDefaultSsoProviderGet($cursor, $limit, $page, $accept_language);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SSODefaultApi->authDefaultSsoProviderGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **cursor** | **string**| id of the cursor used for pagination; required if page is set | [optional] |
| **limit** | **int**| amount of results per page (1 ... 100) | [optional] |
| **page** | **int**| current page index of the cursor used for pagination; required if cursor is set | [optional] |
| **accept_language** | **string**| client language(s) | [optional] |

### Return type

[**\OpenAPI\Client\Model\SsoProviderResponseDefault[]**](../Model/SsoProviderResponseDefault.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `authSaml2IdGet()`

```php
authSaml2IdGet($origin, $id)
```

Start a saml2 auth flow

This endpoint redirects the user to the idp login mask.  __Note:__ This endpoint has to be opened directly in browser location, not called via ajax  _accessible without permission_

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\SSODefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$origin = 'origin_example'; // string | the requesting platform (Ios|Android|Web|Cms)
$id = 'id_example'; // string | Provider ID

try {
    $apiInstance->authSaml2IdGet($origin, $id);
} catch (Exception $e) {
    echo 'Exception when calling SSODefaultApi->authSaml2IdGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **origin** | **string**| the requesting platform (Ios|Android|Web|Cms) | |
| **id** | **string**| Provider ID | |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `authSaml2IdMetadataGet()`

```php
authSaml2IdMetadataGet($id)
```

Generates a metadata.xml file

This endpoint is for providing the metadata for saml provider in xml.  __Note:__ This endpoint has to be opened directly in browser location, not called via ajax  _accessible without permission_

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\SSODefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Provider ID

try {
    $apiInstance->authSaml2IdMetadataGet($id);
} catch (Exception $e) {
    echo 'Exception when calling SSODefaultApi->authSaml2IdMetadataGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Provider ID | |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `text/xml`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `authSaml2IdResponsePost()`

```php
authSaml2IdResponsePost($id)
```

Response endpoint of saml2 auth flow

This endpoint processes a saml2 response and redirects the user to the frontend.  __Note:__ This endpoint should only be called from the identity provider  Redirect Path: /{app|cms}/auth/code/{code} -> for Ios with custom url scheme  _accessible without permission_

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\SSODefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Provider ID

try {
    $apiInstance->authSaml2IdResponsePost($id);
} catch (Exception $e) {
    echo 'Exception when calling SSODefaultApi->authSaml2IdResponsePost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Provider ID | |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `authSsoCodePost()`

```php
authSsoCodePost($request, $platform): \OpenAPI\Client\Model\AuthLoginResponse
```

Create a session based on sso auth code

This endpoint creates a new session and refresh token based on auth code. The auth code can only be redeemed once! The _Platform_ header must match origin from sso process.  The __signature__ will be empty  _accessible without permission_

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\SSODefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$request = new \OpenAPI\Client\Model\SsoCodeRequest(); // \OpenAPI\Client\Model\SsoCodeRequest | sso auth code to redeem
$platform = 'platform_example'; // string | The client platform

try {
    $result = $apiInstance->authSsoCodePost($request, $platform);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SSODefaultApi->authSsoCodePost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **request** | [**\OpenAPI\Client\Model\SsoCodeRequest**](../Model/SsoCodeRequest.md)| sso auth code to redeem | |
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
