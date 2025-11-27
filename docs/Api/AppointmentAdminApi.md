# OpenAPI\Client\AppointmentAdminApi



All URIs are relative to https://custom.polario.de/api, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**calendarAdminAppointmentConfigIdDelete()**](AppointmentAdminApi.md#calendarAdminAppointmentConfigIdDelete) | **DELETE** /calendar/admin/appointment/config/{id} | Delete appointment config |
| [**calendarAdminAppointmentConfigIdGet()**](AppointmentAdminApi.md#calendarAdminAppointmentConfigIdGet) | **GET** /calendar/admin/appointment/config/{id} | Get appointment config |
| [**calendarAdminAppointmentConfigIdPatch()**](AppointmentAdminApi.md#calendarAdminAppointmentConfigIdPatch) | **PATCH** /calendar/admin/appointment/config/{id} | Update appointment config |
| [**calendarAdminAppointmentConfigPost()**](AppointmentAdminApi.md#calendarAdminAppointmentConfigPost) | **POST** /calendar/admin/appointment/config | Create appointment config |
| [**calendarAdminAppointmentConfigProjectIdGet()**](AppointmentAdminApi.md#calendarAdminAppointmentConfigProjectIdGet) | **GET** /calendar/admin/appointment/config/project/{id} | Get appointment config list for project |


## `calendarAdminAppointmentConfigIdDelete()`

```php
calendarAdminAppointmentConfigIdDelete($id, $session): \OpenAPI\Client\Model\ModelSwagStatusOk
```

Delete appointment config

This endpoint is for deleting an appointment configuration.  __Note:__ Appointments is a premium feature and requires a valid subscription.  _only accessible with permission_ :  `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ :  `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\AppointmentAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Appointment config ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->calendarAdminAppointmentConfigIdDelete($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AppointmentAdminApi->calendarAdminAppointmentConfigIdDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Appointment config ID | |
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

## `calendarAdminAppointmentConfigIdGet()`

```php
calendarAdminAppointmentConfigIdGet($id, $session): \OpenAPI\Client\Model\AppointmentConfigResponse
```

Get appointment config

This endpoint is for retrieving one appointment configuration.  __Note:__ Appointments is a premium feature and requires a valid subscription.  _only accessible with permission_ :  `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ :  `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\AppointmentAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Appointment config ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->calendarAdminAppointmentConfigIdGet($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AppointmentAdminApi->calendarAdminAppointmentConfigIdGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Appointment config ID | |
| **session** | **string**| JWT | |

### Return type

[**\OpenAPI\Client\Model\AppointmentConfigResponse**](../Model/AppointmentConfigResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `calendarAdminAppointmentConfigIdPatch()`

```php
calendarAdminAppointmentConfigIdPatch($id, $session, $request): \OpenAPI\Client\Model\AppointmentConfigResponse
```

Update appointment config

This endpoint is for updating an existing appointment configuration.  __Note:__ Appointments is a premium feature and requires a valid subscription.  _only accessible with permission_ :  `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ :  `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\AppointmentAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Appointment config ID
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\AppointmentConfigPatchRequest(); // \OpenAPI\Client\Model\AppointmentConfigPatchRequest | appointment config to create

try {
    $result = $apiInstance->calendarAdminAppointmentConfigIdPatch($id, $session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AppointmentAdminApi->calendarAdminAppointmentConfigIdPatch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Appointment config ID | |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\AppointmentConfigPatchRequest**](../Model/AppointmentConfigPatchRequest.md)| appointment config to create | |

### Return type

[**\OpenAPI\Client\Model\AppointmentConfigResponse**](../Model/AppointmentConfigResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `calendarAdminAppointmentConfigPost()`

```php
calendarAdminAppointmentConfigPost($session, $request): \OpenAPI\Client\Model\AppointmentConfigResponse
```

Create appointment config

This endpoint is for creating a new appointment configuration.  __Note:__ Appointments is a premium feature and requires a valid subscription.  _only accessible with permission_ :  `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ :  `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\AppointmentAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\AppointmentConfigPostRequest(); // \OpenAPI\Client\Model\AppointmentConfigPostRequest | appointment config to create

try {
    $result = $apiInstance->calendarAdminAppointmentConfigPost($session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AppointmentAdminApi->calendarAdminAppointmentConfigPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\AppointmentConfigPostRequest**](../Model/AppointmentConfigPostRequest.md)| appointment config to create | |

### Return type

[**\OpenAPI\Client\Model\AppointmentConfigResponse**](../Model/AppointmentConfigResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `calendarAdminAppointmentConfigProjectIdGet()`

```php
calendarAdminAppointmentConfigProjectIdGet($id, $session): \OpenAPI\Client\Model\AppointmentConfigResponse[]
```

Get appointment config list for project

This endpoint is for retrieving all appointment configurations for the requested project. If a limit is set, a cursor for this endpoint may be created to iterate over all calendars.  __Note:__ Appointments is a premium feature and requires a valid subscription.  _only accessible with permission_ :  `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ :  `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\AppointmentAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | project ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->calendarAdminAppointmentConfigProjectIdGet($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AppointmentAdminApi->calendarAdminAppointmentConfigProjectIdGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| project ID | |
| **session** | **string**| JWT | |

### Return type

[**\OpenAPI\Client\Model\AppointmentConfigResponse[]**](../Model/AppointmentConfigResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
