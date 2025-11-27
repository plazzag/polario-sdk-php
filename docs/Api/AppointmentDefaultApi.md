# OpenAPI\Client\AppointmentDefaultApi



All URIs are relative to https://custom.polario.de/api, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**calendarDefaultAppointmentGet()**](AppointmentDefaultApi.md#calendarDefaultAppointmentGet) | **GET** /calendar/default/appointment | Get appointment list for cursor |
| [**calendarDefaultAppointmentIdGet()**](AppointmentDefaultApi.md#calendarDefaultAppointmentIdGet) | **GET** /calendar/default/appointment/{id} | Get appointment |
| [**calendarDefaultAppointmentPost()**](AppointmentDefaultApi.md#calendarDefaultAppointmentPost) | **POST** /calendar/default/appointment | Create appointment |
| [**calendarDefaultAppointmentSearchPost()**](AppointmentDefaultApi.md#calendarDefaultAppointmentSearchPost) | **POST** /calendar/default/appointment/search | Create cursor |
| [**calendarDefaultAppointmentSlotAllGet()**](AppointmentDefaultApi.md#calendarDefaultAppointmentSlotAllGet) | **GET** /calendar/default/appointment/slot/all | Get all appointment slot options |
| [**calendarDefaultAppointmentSlotSearchPost()**](AppointmentDefaultApi.md#calendarDefaultAppointmentSlotSearchPost) | **POST** /calendar/default/appointment/slot/search | Get possible appointment slot options |


## `calendarDefaultAppointmentGet()`

```php
calendarDefaultAppointmentGet($cursor, $page, $session, $limit): \OpenAPI\Client\Model\AppointmentResponse[]
```

Get appointment list for cursor

This endpoint is for retrieving all appointments for the requested cursor in default representation.  Cursor could be created here: POST /calendar/default/appointment/search  _accessible without permission_

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\AppointmentDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$cursor = 'cursor_example'; // string | id of the cursor used for pagination; required if page is set
$page = 56; // int | current page index of the cursor used for pagination; required if cursor is set
$session = 'session_example'; // string | JWT
$limit = 56; // int | amount of results per page (1 ... 100)

try {
    $result = $apiInstance->calendarDefaultAppointmentGet($cursor, $page, $session, $limit);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AppointmentDefaultApi->calendarDefaultAppointmentGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **cursor** | **string**| id of the cursor used for pagination; required if page is set | |
| **page** | **int**| current page index of the cursor used for pagination; required if cursor is set | |
| **session** | **string**| JWT | |
| **limit** | **int**| amount of results per page (1 ... 100) | [optional] |

### Return type

[**\OpenAPI\Client\Model\AppointmentResponse[]**](../Model/AppointmentResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `calendarDefaultAppointmentIdGet()`

```php
calendarDefaultAppointmentIdGet($id, $session): \OpenAPI\Client\Model\AppointmentResponse
```

Get appointment

This endpoint is for retrieving one appointment for requested id.  _accessible without permission_

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\AppointmentDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Appointment config ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->calendarDefaultAppointmentIdGet($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AppointmentDefaultApi->calendarDefaultAppointmentIdGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Appointment config ID | |
| **session** | **string**| JWT | |

### Return type

[**\OpenAPI\Client\Model\AppointmentResponse**](../Model/AppointmentResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `calendarDefaultAppointmentPost()`

```php
calendarDefaultAppointmentPost($session, $request): \OpenAPI\Client\Model\AppointmentResponse
```

Create appointment

This endpoint is for creating a new appointment.  __Note:__ Appointments is a premium feature and requires a valid subscription.  _accessible without permission_

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\AppointmentDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\AppointmentPostRequest(); // \OpenAPI\Client\Model\AppointmentPostRequest | appointment to create

try {
    $result = $apiInstance->calendarDefaultAppointmentPost($session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AppointmentDefaultApi->calendarDefaultAppointmentPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\AppointmentPostRequest**](../Model/AppointmentPostRequest.md)| appointment to create | |

### Return type

[**\OpenAPI\Client\Model\AppointmentResponse**](../Model/AppointmentResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `calendarDefaultAppointmentSearchPost()`

```php
calendarDefaultAppointmentSearchPost($session, $request): \OpenAPI\Client\Model\ModelCursorResponse
```

Create cursor

This endpoint returns a cursor for list appointments in default representation with applied filter and sort options. In case of cursor response total will be 0 the status 204 with not content is returned instead.  _accessible without permission_

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\AppointmentDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\AppointmentCursorRequestDefault(); // \OpenAPI\Client\Model\AppointmentCursorRequestDefault | options to create cursor

try {
    $result = $apiInstance->calendarDefaultAppointmentSearchPost($session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AppointmentDefaultApi->calendarDefaultAppointmentSearchPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\AppointmentCursorRequestDefault**](../Model/AppointmentCursorRequestDefault.md)| options to create cursor | |

### Return type

[**\OpenAPI\Client\Model\ModelCursorResponse**](../Model/ModelCursorResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `calendarDefaultAppointmentSlotAllGet()`

```php
calendarDefaultAppointmentSlotAllGet($session): \OpenAPI\Client\Model\AppointmentAllSlotsResponse
```

Get all appointment slot options

This endpoint is for retrieving all appointment slot options.  _accessible without permission_

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\AppointmentDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->calendarDefaultAppointmentSlotAllGet($session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AppointmentDefaultApi->calendarDefaultAppointmentSlotAllGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **session** | **string**| JWT | |

### Return type

[**\OpenAPI\Client\Model\AppointmentAllSlotsResponse**](../Model/AppointmentAllSlotsResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `calendarDefaultAppointmentSlotSearchPost()`

```php
calendarDefaultAppointmentSlotSearchPost($session, $request): \OpenAPI\Client\Model\AppointmentAvailableSlotsResponse
```

Get possible appointment slot options

This endpoint is for retrieving all possible appointment slot options for requested search. It only applies restrictions but ignores occupied and blocked meeting options as long as it's allowed to create such \"conflicts\". All values that were returned could be selected to create an appointment.  _accessible without permission_

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\AppointmentDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\AppointmentSlotSearchRequest(); // \OpenAPI\Client\Model\AppointmentSlotSearchRequest | appointment slot search query

try {
    $result = $apiInstance->calendarDefaultAppointmentSlotSearchPost($session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AppointmentDefaultApi->calendarDefaultAppointmentSlotSearchPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\AppointmentSlotSearchRequest**](../Model/AppointmentSlotSearchRequest.md)| appointment slot search query | |

### Return type

[**\OpenAPI\Client\Model\AppointmentAvailableSlotsResponse**](../Model/AppointmentAvailableSlotsResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
