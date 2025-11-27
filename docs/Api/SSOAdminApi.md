# OpenAPI\Client\SSOAdminApi



All URIs are relative to https://custom.polario.de/api, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**authAdminSsoProviderGet()**](SSOAdminApi.md#authAdminSsoProviderGet) | **GET** /auth/admin/sso-provider | Get all sso provider |
| [**authAdminSsoProviderIdDelete()**](SSOAdminApi.md#authAdminSsoProviderIdDelete) | **DELETE** /auth/admin/sso-provider/{id} | Delete a sso provider |
| [**authAdminSsoProviderIdGet()**](SSOAdminApi.md#authAdminSsoProviderIdGet) | **GET** /auth/admin/sso-provider/{id} | Get a single sso provider |
| [**authAdminSsoProviderIdPut()**](SSOAdminApi.md#authAdminSsoProviderIdPut) | **PUT** /auth/admin/sso-provider/{id} | Update a sso provider |
| [**authAdminSsoProviderPost()**](SSOAdminApi.md#authAdminSsoProviderPost) | **POST** /auth/admin/sso-provider | Creates a sso provider |


## `authAdminSsoProviderGet()`

```php
authAdminSsoProviderGet($session, $cursor, $limit, $page): \OpenAPI\Client\Model\SsoProviderResponseAdmin[]
```

Get all sso provider

This endpoint returns all sso-provider with content in administrative representation. If a limit is set, a cursor for this endpoint may be created to iterate over all sso-provider.  _only accessible with permission_ : `\"ManageConfiguration\"`  _fully accessible with permission_ : `\"ManageConfiguration\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\SSOAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT
$cursor = 'cursor_example'; // string | id of the cursor used for pagination; required if page is set
$limit = 56; // int | amount of results per page (1 ... 100)
$page = 56; // int | current page index of the cursor used for pagination; required if cursor is set

try {
    $result = $apiInstance->authAdminSsoProviderGet($session, $cursor, $limit, $page);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SSOAdminApi->authAdminSsoProviderGet: ', $e->getMessage(), PHP_EOL;
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

[**\OpenAPI\Client\Model\SsoProviderResponseAdmin[]**](../Model/SsoProviderResponseAdmin.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `authAdminSsoProviderIdDelete()`

```php
authAdminSsoProviderIdDelete($id, $session): \OpenAPI\Client\Model\ModelSwagStatusOk
```

Delete a sso provider

This endpoint is for deleting a single sso provider with all localizations.  __Note:__ if isSystem = true the provider is not deletable, api call will result in a http 409  _only accessible with permission_ : `\"ManageConfiguration\"`  _fully accessible with permission_ : `\"ManageConfiguration\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\SSOAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Provider ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->authAdminSsoProviderIdDelete($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SSOAdminApi->authAdminSsoProviderIdDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Provider ID | |
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

## `authAdminSsoProviderIdGet()`

```php
authAdminSsoProviderIdGet($id, $session): \OpenAPI\Client\Model\SsoProviderResponseAdmin
```

Get a single sso provider

This endpoint returns a single sso-provider with content in administrative representation.  _only accessible with permission_ : `\"ManageConfiguration\"`  _fully accessible with permission_ : `\"ManageConfiguration\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\SSOAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Provider ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->authAdminSsoProviderIdGet($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SSOAdminApi->authAdminSsoProviderIdGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Provider ID | |
| **session** | **string**| JWT | |

### Return type

[**\OpenAPI\Client\Model\SsoProviderResponseAdmin**](../Model/SsoProviderResponseAdmin.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `authAdminSsoProviderIdPut()`

```php
authAdminSsoProviderIdPut($id, $session, $request): \OpenAPI\Client\Model\SsoProviderResponseAdmin
```

Update a sso provider

This endpoint updates a sso-provider.  __Note:__ if isSystem = true the provider is immutable, api call will result in a http 409  _only accessible with permission_ : `\"ManageConfiguration\"`  _fully accessible with permission_ : `\"ManageConfiguration\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\SSOAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Provider ID
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\SsoProviderRequest(); // \OpenAPI\Client\Model\SsoProviderRequest | sso provider to update

try {
    $result = $apiInstance->authAdminSsoProviderIdPut($id, $session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SSOAdminApi->authAdminSsoProviderIdPut: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Provider ID | |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\SsoProviderRequest**](../Model/SsoProviderRequest.md)| sso provider to update | |

### Return type

[**\OpenAPI\Client\Model\SsoProviderResponseAdmin**](../Model/SsoProviderResponseAdmin.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `authAdminSsoProviderPost()`

```php
authAdminSsoProviderPost($session, $request): \OpenAPI\Client\Model\SsoProviderResponseAdmin
```

Creates a sso provider

This endpoint creates a sso-provider.  _only accessible with permission_ : `\"ManageConfiguration\"`  _fully accessible with permission_ : `\"ManageConfiguration\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\SSOAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\SsoProviderRequest(); // \OpenAPI\Client\Model\SsoProviderRequest | sso provider to create

try {
    $result = $apiInstance->authAdminSsoProviderPost($session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SSOAdminApi->authAdminSsoProviderPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\SsoProviderRequest**](../Model/SsoProviderRequest.md)| sso provider to create | |

### Return type

[**\OpenAPI\Client\Model\SsoProviderResponseAdmin**](../Model/SsoProviderResponseAdmin.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
