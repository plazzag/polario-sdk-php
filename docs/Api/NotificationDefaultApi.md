# OpenAPI\Client\NotificationDefaultApi



All URIs are relative to https://custom.polario.de/api, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**notificationDefaultDelete()**](NotificationDefaultApi.md#notificationDefaultDelete) | **DELETE** /notification/default | Delete account notifications |
| [**notificationDefaultGet()**](NotificationDefaultApi.md#notificationDefaultGet) | **GET** /notification/default | Get all account notifications |
| [**notificationDefaultIdDelete()**](NotificationDefaultApi.md#notificationDefaultIdDelete) | **DELETE** /notification/default/{id} | Delete account notification |
| [**notificationDefaultIdGet()**](NotificationDefaultApi.md#notificationDefaultIdGet) | **GET** /notification/default/{id} | Get account notification |
| [**notificationDefaultIdPut()**](NotificationDefaultApi.md#notificationDefaultIdPut) | **PUT** /notification/default/{id} | Update account notification |
| [**notificationDefaultReadAllPut()**](NotificationDefaultApi.md#notificationDefaultReadAllPut) | **PUT** /notification/default/read-all | Read all account notifications |
| [**notificationDefaultReadPut()**](NotificationDefaultApi.md#notificationDefaultReadPut) | **PUT** /notification/default/read | Read account notifications |
| [**notificationDefaultSafariGet()**](NotificationDefaultApi.md#notificationDefaultSafariGet) | **GET** /notification/default/safari | Get safari settings |
| [**notificationDefaultUnreadPut()**](NotificationDefaultApi.md#notificationDefaultUnreadPut) | **PUT** /notification/default/unread | Unread account notifications |
| [**notificationDefaultVapidPublicGet()**](NotificationDefaultApi.md#notificationDefaultVapidPublicGet) | **GET** /notification/default/vapid/public | Get vapid public key |


## `notificationDefaultDelete()`

```php
notificationDefaultDelete($session, $request): \OpenAPI\Client\Model\ModelSwagStatusOk
```

Delete account notifications

This endpoint is for deleting account notifications. Request containing IDs of notifications with read confirmation will result 400.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\NotificationDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT
$request = array('request_example'); // string[] | ids of the notifications to delete

try {
    $result = $apiInstance->notificationDefaultDelete($session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NotificationDefaultApi->notificationDefaultDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **session** | **string**| JWT | |
| **request** | [**string[]**](../Model/string.md)| ids of the notifications to delete | |

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

## `notificationDefaultGet()`

```php
notificationDefaultGet($session, $cursor, $limit, $page, $accept_language): \OpenAPI\Client\Model\AccountnotificationAccountNotification[]
```

Get all account notifications

This endpoint returns all account notifications in default representation. If a limit is set, a cursor for this endpoint may be created to iterate over all account notifications.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\NotificationDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT
$cursor = 'cursor_example'; // string | id of the cursor used for pagination; required if page is set
$limit = 56; // int | amount of results per page (1 ... 100)
$page = 56; // int | current page index of the cursor used for pagination; required if cursor is set
$accept_language = 'accept_language_example'; // string | client language(s)

try {
    $result = $apiInstance->notificationDefaultGet($session, $cursor, $limit, $page, $accept_language);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NotificationDefaultApi->notificationDefaultGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **session** | **string**| JWT | |
| **cursor** | **string**| id of the cursor used for pagination; required if page is set | [optional] |
| **limit** | **int**| amount of results per page (1 ... 100) | [optional] |
| **page** | **int**| current page index of the cursor used for pagination; required if cursor is set | [optional] |
| **accept_language** | **string**| client language(s) | [optional] |

### Return type

[**\OpenAPI\Client\Model\AccountnotificationAccountNotification[]**](../Model/AccountnotificationAccountNotification.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `notificationDefaultIdDelete()`

```php
notificationDefaultIdDelete($id, $session): \OpenAPI\Client\Model\ModelSwagStatusOk
```

Delete account notification

This endpoint is for deleting account notification. Deleting unread notification with read confirmation will return 409.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\NotificationDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Notification ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->notificationDefaultIdDelete($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NotificationDefaultApi->notificationDefaultIdDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Notification ID | |
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

## `notificationDefaultIdGet()`

```php
notificationDefaultIdGet($id, $session, $accept_language): \OpenAPI\Client\Model\AccountnotificationAccountNotification
```

Get account notification

This endpoint is for fetching a specific account notification.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\NotificationDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Notification ID
$session = 'session_example'; // string | JWT
$accept_language = 'accept_language_example'; // string | client language(s)

try {
    $result = $apiInstance->notificationDefaultIdGet($id, $session, $accept_language);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NotificationDefaultApi->notificationDefaultIdGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Notification ID | |
| **session** | **string**| JWT | |
| **accept_language** | **string**| client language(s) | [optional] |

### Return type

[**\OpenAPI\Client\Model\AccountnotificationAccountNotification**](../Model/AccountnotificationAccountNotification.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `notificationDefaultIdPut()`

```php
notificationDefaultIdPut($id, $session, $request): \OpenAPI\Client\Model\NotificationPutAccountNotificationResponse
```

Update account notification

This endpoint is for updating account notification. Notifications with read confirmation cannot be marked as unread therefore 409 will be returned.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\NotificationDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Notification ID
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\NotificationPutAccountNotificationRequest(); // \OpenAPI\Client\Model\NotificationPutAccountNotificationRequest | notification to be updated

try {
    $result = $apiInstance->notificationDefaultIdPut($id, $session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NotificationDefaultApi->notificationDefaultIdPut: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Notification ID | |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\NotificationPutAccountNotificationRequest**](../Model/NotificationPutAccountNotificationRequest.md)| notification to be updated | |

### Return type

[**\OpenAPI\Client\Model\NotificationPutAccountNotificationResponse**](../Model/NotificationPutAccountNotificationResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `notificationDefaultReadAllPut()`

```php
notificationDefaultReadAllPut($session): string[]
```

Read all account notifications

This endpoint is for updating all account notifications to read. Only notifications without read confirmation will be marked as read.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\NotificationDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->notificationDefaultReadAllPut($session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NotificationDefaultApi->notificationDefaultReadAllPut: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **session** | **string**| JWT | |

### Return type

**string[]**

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `notificationDefaultReadPut()`

```php
notificationDefaultReadPut($session, $request): \OpenAPI\Client\Model\ModelSwagStatusOk
```

Read account notifications

This endpoint is for updating account notifications to read. Request containing IDs of notifications with read confirmation will result 400.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\NotificationDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT
$request = array('request_example'); // string[] | notification ids to be updated

try {
    $result = $apiInstance->notificationDefaultReadPut($session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NotificationDefaultApi->notificationDefaultReadPut: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **session** | **string**| JWT | |
| **request** | [**string[]**](../Model/string.md)| notification ids to be updated | |

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

## `notificationDefaultSafariGet()`

```php
notificationDefaultSafariGet($session): \OpenAPI\Client\Model\NotificationSafariSettings
```

Get safari settings

This endpoint returns the needed configuration for using browser push for Safari.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\NotificationDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->notificationDefaultSafariGet($session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NotificationDefaultApi->notificationDefaultSafariGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **session** | **string**| JWT | |

### Return type

[**\OpenAPI\Client\Model\NotificationSafariSettings**](../Model/NotificationSafariSettings.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `notificationDefaultUnreadPut()`

```php
notificationDefaultUnreadPut($session, $request): \OpenAPI\Client\Model\ModelSwagStatusOk
```

Unread account notifications

This endpoint is for updating account notifications to unread. Request containing IDs of notifications with read confirmation will result 400.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\NotificationDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT
$request = array('request_example'); // string[] | notification ids to be updated

try {
    $result = $apiInstance->notificationDefaultUnreadPut($session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NotificationDefaultApi->notificationDefaultUnreadPut: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **session** | **string**| JWT | |
| **request** | [**string[]**](../Model/string.md)| notification ids to be updated | |

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

## `notificationDefaultVapidPublicGet()`

```php
notificationDefaultVapidPublicGet($session): \OpenAPI\Client\Model\NotificationVAPIDPublicKeyResponse
```

Get vapid public key

This endpoint returns the vapid public key needed for using browser push for Chrome, Edge & Firefox.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\NotificationDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->notificationDefaultVapidPublicGet($session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NotificationDefaultApi->notificationDefaultVapidPublicGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **session** | **string**| JWT | |

### Return type

[**\OpenAPI\Client\Model\NotificationVAPIDPublicKeyResponse**](../Model/NotificationVAPIDPublicKeyResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
