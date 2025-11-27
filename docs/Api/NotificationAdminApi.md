# OpenAPI\Client\NotificationAdminApi



All URIs are relative to https://custom.polario.de/api, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**configAdminNotificationCertificateInfoPost()**](NotificationAdminApi.md#configAdminNotificationCertificateInfoPost) | **POST** /config/admin/notification/certificate/info | Get certificate info |
| [**configAdminNotificationGet()**](NotificationAdminApi.md#configAdminNotificationGet) | **GET** /config/admin/notification | Get notification configuration |
| [**configAdminNotificationIosCertificateCsrGet()**](NotificationAdminApi.md#configAdminNotificationIosCertificateCsrGet) | **GET** /config/admin/notification/ios-certificate/csr | Create iOS push CSR |
| [**configAdminNotificationIosCertificatePut()**](NotificationAdminApi.md#configAdminNotificationIosCertificatePut) | **PUT** /config/admin/notification/ios-certificate | Update iOS push certificate |
| [**configAdminNotificationPatch()**](NotificationAdminApi.md#configAdminNotificationPatch) | **PATCH** /config/admin/notification | Update notification configuration |
| [**configAdminNotificationSafariCertificateCsrGet()**](NotificationAdminApi.md#configAdminNotificationSafariCertificateCsrGet) | **GET** /config/admin/notification/safari-certificate/csr | Create Safari push CSR |
| [**configAdminNotificationSafariCertificatePut()**](NotificationAdminApi.md#configAdminNotificationSafariCertificatePut) | **PUT** /config/admin/notification/safari-certificate | Update Safari push certificate |
| [**notificationAdminIdDelete()**](NotificationAdminApi.md#notificationAdminIdDelete) | **DELETE** /notification/admin/{id} | Delete notification |
| [**notificationAdminIdGet()**](NotificationAdminApi.md#notificationAdminIdGet) | **GET** /notification/admin/{id} | Get notification |
| [**notificationAdminIdPatch()**](NotificationAdminApi.md#notificationAdminIdPatch) | **PATCH** /notification/admin/{id} | Update notification |
| [**notificationAdminPost()**](NotificationAdminApi.md#notificationAdminPost) | **POST** /notification/admin | Create notification |
| [**notificationAdminProjectIdGet()**](NotificationAdminApi.md#notificationAdminProjectIdGet) | **GET** /notification/admin/project/{id} | Get all project notifications |


## `configAdminNotificationCertificateInfoPost()`

```php
configAdminNotificationCertificateInfoPost($session, $file): \OpenAPI\Client\Model\ConfigurationCertificateInfoResponse
```

Get certificate info

This endpoint is retrieving information about a certificate. Certificate file must be provided in DER format.  _only accessible with permission_ : `\"ManageConfiguration\"`  _fully accessible with permission_ : `\"ManageConfiguration\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\NotificationAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT
$file = 'file_example'; // string | certificate

try {
    $result = $apiInstance->configAdminNotificationCertificateInfoPost($session, $file);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NotificationAdminApi->configAdminNotificationCertificateInfoPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **session** | **string**| JWT | |
| **file** | **string**| certificate | |

### Return type

[**\OpenAPI\Client\Model\ConfigurationCertificateInfoResponse**](../Model/ConfigurationCertificateInfoResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `multipart/form-data`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `configAdminNotificationGet()`

```php
configAdminNotificationGet($if_modified_since, $session): \OpenAPI\Client\Model\ConfigurationNotificationResponseAdmin
```

Get notification configuration

This endpoint returns the notification configuration. The If-Modified-Since header can be used for omitting the output if nothing has changed.  _accessible without permission_  _fully accessible with permission_ : `\"ManageConfiguration\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\NotificationAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$if_modified_since = 56; // int | unix timestamp of the last sync
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->configAdminNotificationGet($if_modified_since, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NotificationAdminApi->configAdminNotificationGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **if_modified_since** | **int**| unix timestamp of the last sync | [optional] |
| **session** | **string**| JWT | [optional] |

### Return type

[**\OpenAPI\Client\Model\ConfigurationNotificationResponseAdmin**](../Model/ConfigurationNotificationResponseAdmin.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `configAdminNotificationIosCertificateCsrGet()`

```php
configAdminNotificationIosCertificateCsrGet($session): \OpenAPI\Client\Model\ModelSwagStatusOk
```

Create iOS push CSR

This endpoint is for creating a new certificate signing request for ios push notifications.  _accessible without permission_  _fully accessible with permission_ : `\"ManageConfiguration\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\NotificationAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->configAdminNotificationIosCertificateCsrGet($session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NotificationAdminApi->configAdminNotificationIosCertificateCsrGet: ', $e->getMessage(), PHP_EOL;
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

## `configAdminNotificationIosCertificatePut()`

```php
configAdminNotificationIosCertificatePut($session, $file): \OpenAPI\Client\Model\ModelSwagStatusOk
```

Update iOS push certificate

This endpoint is for updating the ios push certificate. Certificate file must be provided in DER format.  _only accessible with permission_ : `\"ManageConfiguration\"`  _fully accessible with permission_ : `\"ManageConfiguration\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\NotificationAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT
$file = 'file_example'; // string | certificate

try {
    $result = $apiInstance->configAdminNotificationIosCertificatePut($session, $file);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NotificationAdminApi->configAdminNotificationIosCertificatePut: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **session** | **string**| JWT | |
| **file** | **string**| certificate | |

### Return type

[**\OpenAPI\Client\Model\ModelSwagStatusOk**](../Model/ModelSwagStatusOk.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `multipart/form-data`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `configAdminNotificationPatch()`

```php
configAdminNotificationPatch($session, $if_modified_since, $request): \OpenAPI\Client\Model\ConfigurationNotificationResponseAdmin
```

Update notification configuration

This endpoint is for updating the notification configuration. The If-Modified-Since header can be used for omitting the request if nothing has changed.  _only accessible with permission_ : `\"ManageConfiguration\"`  _fully accessible with permission_ : `\"ManageConfiguration\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\NotificationAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT
$if_modified_since = 56; // int | unix timestamp
$request = new \OpenAPI\Client\Model\ConfigurationNotificationRequestAdmin(); // \OpenAPI\Client\Model\ConfigurationNotificationRequestAdmin | notification data to be updated

try {
    $result = $apiInstance->configAdminNotificationPatch($session, $if_modified_since, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NotificationAdminApi->configAdminNotificationPatch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **session** | **string**| JWT | |
| **if_modified_since** | **int**| unix timestamp | [optional] |
| **request** | [**\OpenAPI\Client\Model\ConfigurationNotificationRequestAdmin**](../Model/ConfigurationNotificationRequestAdmin.md)| notification data to be updated | [optional] |

### Return type

[**\OpenAPI\Client\Model\ConfigurationNotificationResponseAdmin**](../Model/ConfigurationNotificationResponseAdmin.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `configAdminNotificationSafariCertificateCsrGet()`

```php
configAdminNotificationSafariCertificateCsrGet($session): \OpenAPI\Client\Model\ModelSwagStatusOk
```

Create Safari push CSR

This endpoint is for creating a new certificate signing request for safari push notifications.  _accessible without permission_  _fully accessible with permission_ : `\"ManageConfiguration\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\NotificationAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->configAdminNotificationSafariCertificateCsrGet($session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NotificationAdminApi->configAdminNotificationSafariCertificateCsrGet: ', $e->getMessage(), PHP_EOL;
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

## `configAdminNotificationSafariCertificatePut()`

```php
configAdminNotificationSafariCertificatePut($session, $file): \OpenAPI\Client\Model\ModelSwagStatusOk
```

Update Safari push certificate

This endpoint is for updating the safari push certificate. Certificate file must be provided in DER format.  _only accessible with permission_ : `\"ManageConfiguration\"`  _fully accessible with permission_ : `\"ManageConfiguration\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\NotificationAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT
$file = 'file_example'; // string | certificate

try {
    $result = $apiInstance->configAdminNotificationSafariCertificatePut($session, $file);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NotificationAdminApi->configAdminNotificationSafariCertificatePut: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **session** | **string**| JWT | |
| **file** | **string**| certificate | |

### Return type

[**\OpenAPI\Client\Model\ModelSwagStatusOk**](../Model/ModelSwagStatusOk.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `multipart/form-data`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `notificationAdminIdDelete()`

```php
notificationAdminIdDelete($id, $session): \OpenAPI\Client\Model\ModelSwagStatusOk
```

Delete notification

This endpoint is for deleting a notification with all localizations.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\NotificationAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Notification ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->notificationAdminIdDelete($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NotificationAdminApi->notificationAdminIdDelete: ', $e->getMessage(), PHP_EOL;
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

## `notificationAdminIdGet()`

```php
notificationAdminIdGet($id, $session): \OpenAPI\Client\Model\NotificationResponseAdmin
```

Get notification

This endpoint returns notification in admin representation.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\NotificationAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Notification ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->notificationAdminIdGet($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NotificationAdminApi->notificationAdminIdGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Notification ID | |
| **session** | **string**| JWT | |

### Return type

[**\OpenAPI\Client\Model\NotificationResponseAdmin**](../Model/NotificationResponseAdmin.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `notificationAdminIdPatch()`

```php
notificationAdminIdPatch($id, $session, $request): \OpenAPI\Client\Model\NotificationResponseAdmin
```

Update notification

This endpoint is for updating notification.  If ___readConfirmation___ is set to true the notification cannot be updated if it is already published.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\NotificationAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Notification ID
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\NotificationPatchNotificationRequest(); // \OpenAPI\Client\Model\NotificationPatchNotificationRequest | notification information to be updated

try {
    $result = $apiInstance->notificationAdminIdPatch($id, $session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NotificationAdminApi->notificationAdminIdPatch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Notification ID | |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\NotificationPatchNotificationRequest**](../Model/NotificationPatchNotificationRequest.md)| notification information to be updated | |

### Return type

[**\OpenAPI\Client\Model\NotificationResponseAdmin**](../Model/NotificationResponseAdmin.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `notificationAdminPost()`

```php
notificationAdminPost($session, $request): \OpenAPI\Client\Model\NotificationResponseAdmin
```

Create notification

This endpoint is for creating a new notification.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\NotificationAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\NotificationPostNotificationRequest(); // \OpenAPI\Client\Model\NotificationPostNotificationRequest | notification to create

try {
    $result = $apiInstance->notificationAdminPost($session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NotificationAdminApi->notificationAdminPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\NotificationPostNotificationRequest**](../Model/NotificationPostNotificationRequest.md)| notification to create | |

### Return type

[**\OpenAPI\Client\Model\NotificationResponseAdmin**](../Model/NotificationResponseAdmin.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `notificationAdminProjectIdGet()`

```php
notificationAdminProjectIdGet($id, $session, $cursor, $limit, $page): \OpenAPI\Client\Model\NotificationResponseAdmin[]
```

Get all project notifications

This endpoint returns all notifications in admin representation for a project. If a limit is set, a cursor for this endpoint may be created to iterate over all notifications.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\NotificationAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Project ID
$session = 'session_example'; // string | JWT
$cursor = 'cursor_example'; // string | id of the cursor used for pagination; required if page is set
$limit = 56; // int | amount of results per page (1 ... 100)
$page = 56; // int | current page index of the cursor used for pagination; required if cursor is set

try {
    $result = $apiInstance->notificationAdminProjectIdGet($id, $session, $cursor, $limit, $page);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NotificationAdminApi->notificationAdminProjectIdGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Project ID | |
| **session** | **string**| JWT | |
| **cursor** | **string**| id of the cursor used for pagination; required if page is set | [optional] |
| **limit** | **int**| amount of results per page (1 ... 100) | [optional] |
| **page** | **int**| current page index of the cursor used for pagination; required if cursor is set | [optional] |

### Return type

[**\OpenAPI\Client\Model\NotificationResponseAdmin[]**](../Model/NotificationResponseAdmin.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
