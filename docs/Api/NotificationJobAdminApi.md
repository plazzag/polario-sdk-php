# OpenAPI\Client\NotificationJobAdminApi



All URIs are relative to https://custom.polario.de/api, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**notificationAdminJobGet()**](NotificationJobAdminApi.md#notificationAdminJobGet) | **GET** /notification/admin/job | Get job list for project |
| [**notificationAdminJobIdDefaultGet()**](NotificationJobAdminApi.md#notificationAdminJobIdDefaultGet) | **GET** /notification/admin/job/{id}/default | Get default job |
| [**notificationAdminJobIdDelete()**](NotificationJobAdminApi.md#notificationAdminJobIdDelete) | **DELETE** /notification/admin/job/{id} | Delete Notification Job |
| [**notificationAdminJobIdGet()**](NotificationJobAdminApi.md#notificationAdminJobIdGet) | **GET** /notification/admin/job/{id} | Get job |
| [**notificationAdminJobIdPatch()**](NotificationJobAdminApi.md#notificationAdminJobIdPatch) | **PATCH** /notification/admin/job/{id} | Update job |
| [**notificationAdminJobPost()**](NotificationJobAdminApi.md#notificationAdminJobPost) | **POST** /notification/admin/job | Create job |
| [**notificationAdminJobTestPost()**](NotificationJobAdminApi.md#notificationAdminJobTestPost) | **POST** /notification/admin/job/test | Test job content |


## `notificationAdminJobGet()`

```php
notificationAdminJobGet($session, $cursor, $limit, $page, $accept_language): \OpenAPI\Client\Model\JobResponseListAdmin[]
```

Get job list for project

This endpoint returns a list of all jobs. If a limit is set, a cursor for this endpoint may be created to iterate over all jobs.  _only accessible with permission_ : `\"ManageConfiguration\"`  _fully accessible with permission_ : `\"ManageConfiguration\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\NotificationJobAdminApi(
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
    $result = $apiInstance->notificationAdminJobGet($session, $cursor, $limit, $page, $accept_language);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NotificationJobAdminApi->notificationAdminJobGet: ', $e->getMessage(), PHP_EOL;
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

[**\OpenAPI\Client\Model\JobResponseListAdmin[]**](../Model/JobResponseListAdmin.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `notificationAdminJobIdDefaultGet()`

```php
notificationAdminJobIdDefaultGet($id, $session): \OpenAPI\Client\Model\JobResponseAdmin
```

Get default job

This endpoint returns the default job in administrative representation by given id.  _only accessible with permission_ : `\"ManageConfiguration\"`  _fully accessible with permission_ : `\"ManageConfiguration\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\NotificationJobAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Job ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->notificationAdminJobIdDefaultGet($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NotificationJobAdminApi->notificationAdminJobIdDefaultGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Job ID | |
| **session** | **string**| JWT | |

### Return type

[**\OpenAPI\Client\Model\JobResponseAdmin**](../Model/JobResponseAdmin.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `notificationAdminJobIdDelete()`

```php
notificationAdminJobIdDelete($id, $session): \OpenAPI\Client\Model\ModelSwagStatusOk
```

Delete Notification Job

This endpoint is for deleting a single Notification Job.  _only accessible with permission_ : `\"ManageConfiguration\"`  _fully accessible with permission_ : `\"ManageConfiguration\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\NotificationJobAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Job ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->notificationAdminJobIdDelete($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NotificationJobAdminApi->notificationAdminJobIdDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Job ID | |
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

## `notificationAdminJobIdGet()`

```php
notificationAdminJobIdGet($id, $session): \OpenAPI\Client\Model\JobResponseAdmin
```

Get job

This endpoint returns a job in administrative representation by given id.  _only accessible with permission_ : `\"ManageConfiguration\"`  _fully accessible with permission_ : `\"ManageConfiguration\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\NotificationJobAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Job ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->notificationAdminJobIdGet($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NotificationJobAdminApi->notificationAdminJobIdGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Job ID | |
| **session** | **string**| JWT | |

### Return type

[**\OpenAPI\Client\Model\JobResponseAdmin**](../Model/JobResponseAdmin.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `notificationAdminJobIdPatch()`

```php
notificationAdminJobIdPatch($id, $session, $request): \OpenAPI\Client\Model\JobResponseAdmin
```

Update job

This endpoint is for updating specific data of an existing job. In case of response status is 205 the request was only executed partial. Use GET to receive the stored configuration.  __Note:__ email will send without attachments if attachments exceed limit of 16MiB (16.7MB)  _only accessible with permission_ : `\"ManageConfiguration\"`  _fully accessible with permission_ : `\"ManageConfiguration\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\NotificationJobAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Job ID
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\JobPatchRequest(); // \OpenAPI\Client\Model\JobPatchRequest | job data to be updated

try {
    $result = $apiInstance->notificationAdminJobIdPatch($id, $session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NotificationJobAdminApi->notificationAdminJobIdPatch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Job ID | |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\JobPatchRequest**](../Model/JobPatchRequest.md)| job data to be updated | |

### Return type

[**\OpenAPI\Client\Model\JobResponseAdmin**](../Model/JobResponseAdmin.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `notificationAdminJobPost()`

```php
notificationAdminJobPost($session, $request): \OpenAPI\Client\Model\JobResponseAdmin
```

Create job

This endpoint is for creating a notification job. In case of response status is 205 the request was performed, but the request data could not be created. Use GET to receive the stored notification job data.  _only accessible with permission_ : `\"ManageConfiguration\"`  _fully accessible with permission_ : `\"ManageConfiguration\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\NotificationJobAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\JobRequestAdmin(); // \OpenAPI\Client\Model\JobRequestAdmin | job to create

try {
    $result = $apiInstance->notificationAdminJobPost($session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NotificationJobAdminApi->notificationAdminJobPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\JobRequestAdmin**](../Model/JobRequestAdmin.md)| job to create | |

### Return type

[**\OpenAPI\Client\Model\JobResponseAdmin**](../Model/JobResponseAdmin.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `notificationAdminJobTestPost()`

```php
notificationAdminJobTestPost($session, $request, $accept_language): \OpenAPI\Client\Model\ModelSwagStatusOk
```

Test job content

This endpoint is for testing job data.  __Note:__ email will send without attachments if attachments exceed limit of 16MiB (16.7MB)  _only accessible with permission_ : `\"ManageConfiguration\"`  _fully accessible with permission_ : `\"ManageConfiguration\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\NotificationJobAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\JobTestContentRequest(); // \OpenAPI\Client\Model\JobTestContentRequest | job data to be tested
$accept_language = 'accept_language_example'; // string | client language(s)

try {
    $result = $apiInstance->notificationAdminJobTestPost($session, $request, $accept_language);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NotificationJobAdminApi->notificationAdminJobTestPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\JobTestContentRequest**](../Model/JobTestContentRequest.md)| job data to be tested | |
| **accept_language** | **string**| client language(s) | [optional] |

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
