# OpenAPI\Client\ShippingAdminApi



All URIs are relative to https://custom.polario.de/api, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**shippingAdminAccountGet()**](ShippingAdminApi.md#shippingAdminAccountGet) | **GET** /shipping/admin/Account | Get accounts shipping list |
| [**shippingAdminAccountIdGet()**](ShippingAdminApi.md#shippingAdminAccountIdGet) | **GET** /shipping/admin/Account/{id} | Get account shipping |
| [**shippingAdminAccountIdPost()**](ShippingAdminApi.md#shippingAdminAccountIdPost) | **POST** /shipping/admin/Account/{id} | Add account shipping data |
| [**shippingAdminAccountIdPut()**](ShippingAdminApi.md#shippingAdminAccountIdPut) | **PUT** /shipping/admin/Account/{id} | Start account shipping process |
| [**shippingAdminAccountPost()**](ShippingAdminApi.md#shippingAdminAccountPost) | **POST** /shipping/admin/Account | Create account shipping |
| [**shippingAdminIdGet()**](ShippingAdminApi.md#shippingAdminIdGet) | **GET** /shipping/admin/{id} | Get shipping |


## `shippingAdminAccountGet()`

```php
shippingAdminAccountGet($session, $cursor, $limit, $page): \OpenAPI\Client\Model\ShippingResponseAdmin[]
```

Get accounts shipping list

This endpoint returns a list of all account shipping in admin representation. If a limit is set, a cursor for this endpoint may be created to iterate over all account shipping's.  _only accessible with permission_ : `\"ManageAccounts\"`  _fully accessible with permission_ : `\"ManageAccounts\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\ShippingAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT
$cursor = 'cursor_example'; // string | id of the cursor used for pagination; required if page is set
$limit = 56; // int | amount of results per page (1 ... 100)
$page = 56; // int | current page index of the cursor used for pagination; required if cursor is set

try {
    $result = $apiInstance->shippingAdminAccountGet($session, $cursor, $limit, $page);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ShippingAdminApi->shippingAdminAccountGet: ', $e->getMessage(), PHP_EOL;
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

[**\OpenAPI\Client\Model\ShippingResponseAdmin[]**](../Model/ShippingResponseAdmin.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `shippingAdminAccountIdGet()`

```php
shippingAdminAccountIdGet($id, $session): \OpenAPI\Client\Model\ShippingResponseAdmin
```

Get account shipping

This endpoint returns an account shipping in admin representation by given id.  _only accessible with permission_ : `\"ManageAccounts\"`  _fully accessible with permission_ : `\"ManageAccounts\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\ShippingAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Shipping ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->shippingAdminAccountIdGet($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ShippingAdminApi->shippingAdminAccountIdGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Shipping ID | |
| **session** | **string**| JWT | |

### Return type

[**\OpenAPI\Client\Model\ShippingResponseAdmin**](../Model/ShippingResponseAdmin.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `shippingAdminAccountIdPost()`

```php
shippingAdminAccountIdPost($id, $session, $request): \OpenAPI\Client\Model\ModelShipAccountData[]
```

Add account shipping data

This endpoint is for adding new account shipping data.  __Note:__ This endpoint does not prevent sending not permitted `null` values for `\"image\"` `\"title\"` `\"ssoIdentity\"` and `\"ssoProviderId\"`. `null` values will be ignored in that case.  _only accessible with permission_ : `\"ManageAccounts\"`  _fully accessible with permission_ : `\"ManageAccounts\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\ShippingAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Shipping ID
$session = 'session_example'; // string | JWT
$request = array(new \OpenAPI\Client\Model\ModelShipAccountData()); // \OpenAPI\Client\Model\ModelShipAccountData[] | account data to ship; max 100 elements are permitted per request

try {
    $result = $apiInstance->shippingAdminAccountIdPost($id, $session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ShippingAdminApi->shippingAdminAccountIdPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Shipping ID | |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\ModelShipAccountData[]**](../Model/ModelShipAccountData.md)| account data to ship; max 100 elements are permitted per request | |

### Return type

[**\OpenAPI\Client\Model\ModelShipAccountData[]**](../Model/ModelShipAccountData.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `shippingAdminAccountIdPut()`

```php
shippingAdminAccountIdPut($id, $session): \OpenAPI\Client\Model\ModelSwagStatusOk
```

Start account shipping process

This endpoint is for starting the process of an account shipping. To start the processing there must be at least one data chunk.  _only accessible with permission_ : `\"ManageAccounts\"`  _fully accessible with permission_ : `\"ManageAccounts\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\ShippingAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Shipping ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->shippingAdminAccountIdPut($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ShippingAdminApi->shippingAdminAccountIdPut: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Shipping ID | |
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

## `shippingAdminAccountPost()`

```php
shippingAdminAccountPost($session, $request): \OpenAPI\Client\Model\ShippingResponseAdmin
```

Create account shipping

This endpoint is for creating a new account shipping. The current system state will be used for the data to be imported. Further changes on projects or groups will not affect that shipping.  _only accessible with permission_ : `\"ManageAccounts\"`  _fully accessible with permission_ : `\"ManageAccounts\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\ShippingAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\ShippingRequestBaseAdmin(); // \OpenAPI\Client\Model\ShippingRequestBaseAdmin | shipping config

try {
    $result = $apiInstance->shippingAdminAccountPost($session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ShippingAdminApi->shippingAdminAccountPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\ShippingRequestBaseAdmin**](../Model/ShippingRequestBaseAdmin.md)| shipping config | |

### Return type

[**\OpenAPI\Client\Model\ShippingResponseAdmin**](../Model/ShippingResponseAdmin.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `shippingAdminIdGet()`

```php
shippingAdminIdGet($id, $session): \OpenAPI\Client\Model\ShippingResponseAdmin
```

Get shipping

This endpoint returns a shipping in admin representation by given id.  _only accessible with permission_ : `\"ManageAccounts\"`  _fully accessible with permission_ : `\"ManageAccounts\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\ShippingAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Shipping ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->shippingAdminIdGet($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ShippingAdminApi->shippingAdminIdGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Shipping ID | |
| **session** | **string**| JWT | |

### Return type

[**\OpenAPI\Client\Model\ShippingResponseAdmin**](../Model/ShippingResponseAdmin.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
