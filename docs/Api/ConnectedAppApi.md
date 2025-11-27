# OpenAPI\Client\ConnectedAppApi



All URIs are relative to https://custom.polario.de/api, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**authConnectedAppGet()**](ConnectedAppApi.md#authConnectedAppGet) | **GET** /auth/connected-app | get connected apps list |
| [**authConnectedAppIdDelete()**](ConnectedAppApi.md#authConnectedAppIdDelete) | **DELETE** /auth/connected-app/{id} | Delete connected app |
| [**authConnectedAppIdGet()**](ConnectedAppApi.md#authConnectedAppIdGet) | **GET** /auth/connected-app/{id} | get connected app |
| [**authConnectedAppIdPatch()**](ConnectedAppApi.md#authConnectedAppIdPatch) | **PATCH** /auth/connected-app/{id} | Update connected app |
| [**authConnectedAppIdSecretDelete()**](ConnectedAppApi.md#authConnectedAppIdSecretDelete) | **DELETE** /auth/connected-app/{id}/secret | Remove secret |
| [**authConnectedAppIdSecretPost()**](ConnectedAppApi.md#authConnectedAppIdSecretPost) | **POST** /auth/connected-app/{id}/secret | Add secret |
| [**authConnectedAppIdSessionPost()**](ConnectedAppApi.md#authConnectedAppIdSessionPost) | **POST** /auth/connected-app/{id}/session | Create session |
| [**authConnectedAppPost()**](ConnectedAppApi.md#authConnectedAppPost) | **POST** /auth/connected-app | Create connected app |


## `authConnectedAppGet()`

```php
authConnectedAppGet($session): \OpenAPI\Client\Model\ConnectedappResponseList[]
```

get connected apps list

This endpoint is for retrieving all existing connected apps, which are currently stored in db.  _only accessible with permission_ : `\"ManageApps\"`  _fully accessible with permission_ : `\"ManageApps\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\ConnectedAppApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->authConnectedAppGet($session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConnectedAppApi->authConnectedAppGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **session** | **string**| JWT | |

### Return type

[**\OpenAPI\Client\Model\ConnectedappResponseList[]**](../Model/ConnectedappResponseList.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `authConnectedAppIdDelete()`

```php
authConnectedAppIdDelete($id, $session): \OpenAPI\Client\Model\ModelSwagStatusOk
```

Delete connected app

Deletes a connected app by given id and removes the roles from the linked robot account.  _only accessible with permission_ : `\"ManageApps\"`  _fully accessible with permission_ : `\"ManageApps\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\ConnectedAppApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Connected App ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->authConnectedAppIdDelete($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConnectedAppApi->authConnectedAppIdDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Connected App ID | |
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

## `authConnectedAppIdGet()`

```php
authConnectedAppIdGet($id, $session): \OpenAPI\Client\Model\ConnectedappResponse
```

get connected app

This endpoint is for retrieving one connected app, which is currently stored in db.  _only accessible with permission_ : `\"ManageApps\"`  _fully accessible with permission_ : `\"ManageApps\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\ConnectedAppApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Connected App ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->authConnectedAppIdGet($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConnectedAppApi->authConnectedAppIdGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Connected App ID | |
| **session** | **string**| JWT | |

### Return type

[**\OpenAPI\Client\Model\ConnectedappResponse**](../Model/ConnectedappResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `authConnectedAppIdPatch()`

```php
authConnectedAppIdPatch($id, $session, $request): \OpenAPI\Client\Model\ConnectedappResponse
```

Update connected app

This endpoint updates the requested connected App. It also updates the linked technical account for the connected app. Only the changes should be transmitted due this endpoint.  _only accessible with permission_ : `\"ManageApps\"`  _fully accessible with permission_ : `\"ManageApps\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\ConnectedAppApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Connected App ID
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\ConnectedappRequest(); // \OpenAPI\Client\Model\ConnectedappRequest | changed connected app

try {
    $result = $apiInstance->authConnectedAppIdPatch($id, $session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConnectedAppApi->authConnectedAppIdPatch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Connected App ID | |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\ConnectedappRequest**](../Model/ConnectedappRequest.md)| changed connected app | |

### Return type

[**\OpenAPI\Client\Model\ConnectedappResponse**](../Model/ConnectedappResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `authConnectedAppIdSecretDelete()`

```php
authConnectedAppIdSecretDelete($id, $session, $request): \OpenAPI\Client\Model\ModelSwagStatusOk
```

Remove secret

Deletes a secret by given of a connected app  _only accessible with permission_ : `\"ManageApps\"`  _fully accessible with permission_ : `\"ManageApps\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\ConnectedAppApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Connected App ID
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\ConnectedappSecretRequest(); // \OpenAPI\Client\Model\ConnectedappSecretRequest | secret to be removed

try {
    $result = $apiInstance->authConnectedAppIdSecretDelete($id, $session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConnectedAppApi->authConnectedAppIdSecretDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Connected App ID | |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\ConnectedappSecretRequest**](../Model/ConnectedappSecretRequest.md)| secret to be removed | |

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

## `authConnectedAppIdSecretPost()`

```php
authConnectedAppIdSecretPost($id, $session, $request): \OpenAPI\Client\Model\ConnectedappSecretResponse
```

Add secret

This endpoint updates the requested connected App to add a new secret.  _only accessible with permission_ : `\"ManageApps\"`  _fully accessible with permission_ : `\"ManageApps\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\ConnectedAppApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Connected App ID
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\ConnectedappAddSecretRequest(); // \OpenAPI\Client\Model\ConnectedappAddSecretRequest | expiration timestamp for secret

try {
    $result = $apiInstance->authConnectedAppIdSecretPost($id, $session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConnectedAppApi->authConnectedAppIdSecretPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Connected App ID | |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\ConnectedappAddSecretRequest**](../Model/ConnectedappAddSecretRequest.md)| expiration timestamp for secret | |

### Return type

[**\OpenAPI\Client\Model\ConnectedappSecretResponse**](../Model/ConnectedappSecretResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `authConnectedAppIdSessionPost()`

```php
authConnectedAppIdSessionPost($id, $secret): \OpenAPI\Client\Model\ModelSwagStatusOk
```

Create session

This endpoint creates a session for a connected app  _accessible without permission_

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\ConnectedAppApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Connected App ID
$secret = 'secret_example'; // string | connected app token

try {
    $result = $apiInstance->authConnectedAppIdSessionPost($id, $secret);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConnectedAppApi->authConnectedAppIdSessionPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Connected App ID | |
| **secret** | **string**| connected app token | |

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

## `authConnectedAppPost()`

```php
authConnectedAppPost($session, $request): \OpenAPI\Client\Model\ConnectedappResponse
```

Create connected app

This endpoint is for creating a new connected app. It also creates a new technical account that will be linked with the connected app. You are only allowed to add roles that have permissions you already own through your roles. If you have `\"ManageGlobalRoles\"` you are allowed to add all roles.  _only accessible with permission_ : `\"ManageApps\"`  _fully accessible with permission_ : `\"ManageApps\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\ConnectedAppApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\ConnectedappRequest(); // \OpenAPI\Client\Model\ConnectedappRequest | Connected app to create

try {
    $result = $apiInstance->authConnectedAppPost($session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConnectedAppApi->authConnectedAppPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\ConnectedappRequest**](../Model/ConnectedappRequest.md)| Connected app to create | |

### Return type

[**\OpenAPI\Client\Model\ConnectedappResponse**](../Model/ConnectedappResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
