# OpenAPI\Client\WebhookApi



All URIs are relative to https://custom.polario.de/api, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**webhookGet()**](WebhookApi.md#webhookGet) | **GET** /webhook | Get all webhooks |
| [**webhookIdCallPost()**](WebhookApi.md#webhookIdCallPost) | **POST** /webhook/{id}/call | Call webhook |
| [**webhookIdDelete()**](WebhookApi.md#webhookIdDelete) | **DELETE** /webhook/{id} | Delete webhook |
| [**webhookIdGet()**](WebhookApi.md#webhookIdGet) | **GET** /webhook/{id} | Get webhook |
| [**webhookIdLogsGet()**](WebhookApi.md#webhookIdLogsGet) | **GET** /webhook/{id}/logs | Get webhook logs |
| [**webhookIdPatch()**](WebhookApi.md#webhookIdPatch) | **PATCH** /webhook/{id} | Update webhook |
| [**webhookPost()**](WebhookApi.md#webhookPost) | **POST** /webhook | Create webhook |


## `webhookGet()`

```php
webhookGet($session, $cursor, $limit, $page): \OpenAPI\Client\Model\WebhookResponse[]
```

Get all webhooks

This endpoint returns all webhooks. If a limit is set, a cursor for this endpoint may be created to iterate over all webhooks.  _only accessible with permission_ : `\"ManageConfiguration\"`  _fully accessible with permission_ : `\"ManageConfiguration\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\WebhookApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT
$cursor = 'cursor_example'; // string | id of the cursor used for pagination; required if page is set
$limit = 56; // int | amount of results per page (1 ... 100)
$page = 56; // int | current page index of the cursor used for pagination; required if cursor is set

try {
    $result = $apiInstance->webhookGet($session, $cursor, $limit, $page);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WebhookApi->webhookGet: ', $e->getMessage(), PHP_EOL;
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

[**\OpenAPI\Client\Model\WebhookResponse[]**](../Model/WebhookResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `webhookIdCallPost()`

```php
webhookIdCallPost($id, $session, $request): \OpenAPI\Client\Model\ModelWebhookRequestLogMessage
```

Call webhook

This endpoint triggers a demo call to webhook by given ID  _only accessible with permission_ : `\"ManageConfiguration\"`  _fully accessible with permission_ : `\"ManageConfiguration\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\WebhookApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Webhook ID
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\WebhookCallRequest(); // \OpenAPI\Client\Model\WebhookCallRequest | webhook action to be called

try {
    $result = $apiInstance->webhookIdCallPost($id, $session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WebhookApi->webhookIdCallPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Webhook ID | |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\WebhookCallRequest**](../Model/WebhookCallRequest.md)| webhook action to be called | |

### Return type

[**\OpenAPI\Client\Model\ModelWebhookRequestLogMessage**](../Model/ModelWebhookRequestLogMessage.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `webhookIdDelete()`

```php
webhookIdDelete($id, $session): \OpenAPI\Client\Model\ModelSwagStatusOk
```

Delete webhook

This endpoint is for deleting a single webhook.  _only accessible with permission_ : `\"ManageConfiguration\"`  _fully accessible with permission_ : `\"ManageConfiguration\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\WebhookApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Webhook ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->webhookIdDelete($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WebhookApi->webhookIdDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Webhook ID | |
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

## `webhookIdGet()`

```php
webhookIdGet($id, $session): \OpenAPI\Client\Model\WebhookResponse
```

Get webhook

This endpoint returns a webhook by given id.  _only accessible with permission_ : `\"ManageConfiguration\"`  _fully accessible with permission_ : `\"ManageConfiguration\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\WebhookApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Webhook ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->webhookIdGet($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WebhookApi->webhookIdGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Webhook ID | |
| **session** | **string**| JWT | |

### Return type

[**\OpenAPI\Client\Model\WebhookResponse**](../Model/WebhookResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `webhookIdLogsGet()`

```php
webhookIdLogsGet($id, $session, $cursor, $limit, $page): \OpenAPI\Client\Model\ModelWebhookRequestLogMessage[]
```

Get webhook logs

This endpoint returns the logs of a webhook by given id. If a limit is set, a cursor for this endpoint may be created to iterate over all webhook logs.  _only accessible with permission_ : `\"ManageConfiguration\"`  _fully accessible with permission_ : `\"ManageConfiguration\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\WebhookApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Webhook ID
$session = 'session_example'; // string | JWT
$cursor = 'cursor_example'; // string | id of the cursor used for pagination; required if page is set
$limit = 56; // int | amount of results per page (1 ... 100)
$page = 56; // int | current page index of the cursor used for pagination; required if cursor is set

try {
    $result = $apiInstance->webhookIdLogsGet($id, $session, $cursor, $limit, $page);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WebhookApi->webhookIdLogsGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Webhook ID | |
| **session** | **string**| JWT | |
| **cursor** | **string**| id of the cursor used for pagination; required if page is set | [optional] |
| **limit** | **int**| amount of results per page (1 ... 100) | [optional] |
| **page** | **int**| current page index of the cursor used for pagination; required if cursor is set | [optional] |

### Return type

[**\OpenAPI\Client\Model\ModelWebhookRequestLogMessage[]**](../Model/ModelWebhookRequestLogMessage.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `webhookIdPatch()`

```php
webhookIdPatch($id, $session, $request): \OpenAPI\Client\Model\WebhookResponse
```

Update webhook

This endpoint updates a webhook by given id.  _only accessible with permission_ : `\"ManageConfiguration\"`  _fully accessible with permission_ : `\"ManageConfiguration\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\WebhookApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Webhook ID
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\WebhookRequest(); // \OpenAPI\Client\Model\WebhookRequest | webhook information to be updated

try {
    $result = $apiInstance->webhookIdPatch($id, $session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WebhookApi->webhookIdPatch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Webhook ID | |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\WebhookRequest**](../Model/WebhookRequest.md)| webhook information to be updated | |

### Return type

[**\OpenAPI\Client\Model\WebhookResponse**](../Model/WebhookResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `webhookPost()`

```php
webhookPost($session, $request): \OpenAPI\Client\Model\WebhookResponse
```

Create webhook

This endpoint creates a new webhook.  _only accessible with permission_ : `\"ManageConfiguration\"`  _fully accessible with permission_ : `\"ManageConfiguration\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\WebhookApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\WebhookRequest(); // \OpenAPI\Client\Model\WebhookRequest | webhook to create

try {
    $result = $apiInstance->webhookPost($session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WebhookApi->webhookPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\WebhookRequest**](../Model/WebhookRequest.md)| webhook to create | |

### Return type

[**\OpenAPI\Client\Model\WebhookResponse**](../Model/WebhookResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
