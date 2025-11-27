# OpenAPI\Client\CalendarAdminApi



All URIs are relative to https://custom.polario.de/api, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**calendarAdminEntryIdAccessGet()**](CalendarAdminApi.md#calendarAdminEntryIdAccessGet) | **GET** /calendar/admin/entry/{id}/access | Get calendar entry access configuration |
| [**calendarAdminEntryIdAccessPatch()**](CalendarAdminApi.md#calendarAdminEntryIdAccessPatch) | **PATCH** /calendar/admin/entry/{id}/access | Update calendar entry access configuration |
| [**calendarAdminEntryIdBookingAccountAccountIdDelete()**](CalendarAdminApi.md#calendarAdminEntryIdBookingAccountAccountIdDelete) | **DELETE** /calendar/admin/entry/{id}/booking/account/{accountId} | Delete booking |
| [**calendarAdminEntryIdBookingPost()**](CalendarAdminApi.md#calendarAdminEntryIdBookingPost) | **POST** /calendar/admin/entry/{id}/booking | Create booking |
| [**calendarAdminEntryIdDelete()**](CalendarAdminApi.md#calendarAdminEntryIdDelete) | **DELETE** /calendar/admin/entry/{id} | Delete calendar entry |
| [**calendarAdminEntryIdGet()**](CalendarAdminApi.md#calendarAdminEntryIdGet) | **GET** /calendar/admin/entry/{id} | Get calendar entry |
| [**calendarAdminEntryIdPut()**](CalendarAdminApi.md#calendarAdminEntryIdPut) | **PUT** /calendar/admin/entry/{id} | Update calendar entry |
| [**calendarAdminIdContentGet()**](CalendarAdminApi.md#calendarAdminIdContentGet) | **GET** /calendar/admin/{id}/content | Get calendar entries list for calendar |
| [**calendarAdminIdContentPost()**](CalendarAdminApi.md#calendarAdminIdContentPost) | **POST** /calendar/admin/{id}/content | Add calendar entries |
| [**calendarAdminIdDelete()**](CalendarAdminApi.md#calendarAdminIdDelete) | **DELETE** /calendar/admin/{id} | Delete calendar |
| [**calendarAdminIdDetailGet()**](CalendarAdminApi.md#calendarAdminIdDetailGet) | **GET** /calendar/admin/{id}/detail | Get calendar detail view |
| [**calendarAdminIdDetailPut()**](CalendarAdminApi.md#calendarAdminIdDetailPut) | **PUT** /calendar/admin/{id}/detail | Update calendar detail view |
| [**calendarAdminIdGet()**](CalendarAdminApi.md#calendarAdminIdGet) | **GET** /calendar/admin/{id} | Get calendar |
| [**calendarAdminIdItemsGet()**](CalendarAdminApi.md#calendarAdminIdItemsGet) | **GET** /calendar/admin/{id}/items | Get calendar detail view items |
| [**calendarAdminIdListSettingsGet()**](CalendarAdminApi.md#calendarAdminIdListSettingsGet) | **GET** /calendar/admin/{id}/list-settings | Get calendar list settings |
| [**calendarAdminIdListSettingsPut()**](CalendarAdminApi.md#calendarAdminIdListSettingsPut) | **PUT** /calendar/admin/{id}/list-settings | Update calendar list settings |
| [**calendarAdminIdPatch()**](CalendarAdminApi.md#calendarAdminIdPatch) | **PATCH** /calendar/admin/{id} | Update calendar info |
| [**calendarAdminIdSelectionsGet()**](CalendarAdminApi.md#calendarAdminIdSelectionsGet) | **GET** /calendar/admin/{id}/selections | Get calendar detail view selections |
| [**calendarAdminPost()**](CalendarAdminApi.md#calendarAdminPost) | **POST** /calendar/admin | Create calendar |
| [**calendarAdminProjectIdGet()**](CalendarAdminApi.md#calendarAdminProjectIdGet) | **GET** /calendar/admin/project/{id} | Get calendar list for project |
| [**calendarAdminSyncPut()**](CalendarAdminApi.md#calendarAdminSyncPut) | **PUT** /calendar/admin/sync | Sync operators for all calendar entries |
| [**calendarAdminTemplateGet()**](CalendarAdminApi.md#calendarAdminTemplateGet) | **GET** /calendar/admin/template | Get calendar template list |


## `calendarAdminEntryIdAccessGet()`

```php
calendarAdminEntryIdAccessGet($id, $session): \OpenAPI\Client\Model\AuthorizationAccessResponse
```

Get calendar entry access configuration

This endpoint returns the access configuration for the requested calendar entry. Calendars of `type` \"Appointment\" are readonly.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"` (not for \"Appointment\" calendars)

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\CalendarAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Entry ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->calendarAdminEntryIdAccessGet($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CalendarAdminApi->calendarAdminEntryIdAccessGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Entry ID | |
| **session** | **string**| JWT | |

### Return type

[**\OpenAPI\Client\Model\AuthorizationAccessResponse**](../Model/AuthorizationAccessResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `calendarAdminEntryIdAccessPatch()`

```php
calendarAdminEntryIdAccessPatch($id, $session, $request): \OpenAPI\Client\Model\ModelAccess
```

Update calendar entry access configuration

This endpoint updates the access configuration for the requested calendar entry. Only the changes should be transmitted due this endpoint. Calendars of `type` \"Appointment\" are readonly.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"` (not for \"Appointment\" calendars)

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\CalendarAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Entry ID
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\ModelAccess(); // \OpenAPI\Client\Model\ModelAccess | changed access rights

try {
    $result = $apiInstance->calendarAdminEntryIdAccessPatch($id, $session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CalendarAdminApi->calendarAdminEntryIdAccessPatch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Entry ID | |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\ModelAccess**](../Model/ModelAccess.md)| changed access rights | |

### Return type

[**\OpenAPI\Client\Model\ModelAccess**](../Model/ModelAccess.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `calendarAdminEntryIdBookingAccountAccountIdDelete()`

```php
calendarAdminEntryIdBookingAccountAccountIdDelete($id, $account_id, $session): \OpenAPI\Client\Model\ModelSwagStatusOk
```

Delete booking

This endpoint is for deleting a booking. Calendars of `type` \"Appointment\" are readonly.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"` (not for \"Appointment\" calendars)

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\CalendarAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Entry ID
$account_id = 'account_id_example'; // string | Account ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->calendarAdminEntryIdBookingAccountAccountIdDelete($id, $account_id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CalendarAdminApi->calendarAdminEntryIdBookingAccountAccountIdDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Entry ID | |
| **account_id** | **string**| Account ID | |
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

## `calendarAdminEntryIdBookingPost()`

```php
calendarAdminEntryIdBookingPost($id, $session, $request): \OpenAPI\Client\Model\BookingCalendarBookingResponseAdmin
```

Create booking

This endpoint is for creating calendar entry's booking in admin representation. Calendars of `type` \"Appointment\" are readonly.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"` (not for \"Appointment\" calendars)

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\CalendarAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Entry ID
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\BookingPostRequest(); // \OpenAPI\Client\Model\BookingPostRequest | booking to create

try {
    $result = $apiInstance->calendarAdminEntryIdBookingPost($id, $session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CalendarAdminApi->calendarAdminEntryIdBookingPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Entry ID | |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\BookingPostRequest**](../Model/BookingPostRequest.md)| booking to create | |

### Return type

[**\OpenAPI\Client\Model\BookingCalendarBookingResponseAdmin**](../Model/BookingCalendarBookingResponseAdmin.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `calendarAdminEntryIdDelete()`

```php
calendarAdminEntryIdDelete($id, $session): \OpenAPI\Client\Model\ModelSwagStatusOk
```

Delete calendar entry

This endpoint is for deleting a calendar entry. Calendars of `type` \"Appointment\" are readonly.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"` (not for \"Appointment\" calendars)

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\CalendarAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Entry ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->calendarAdminEntryIdDelete($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CalendarAdminApi->calendarAdminEntryIdDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Entry ID | |
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

## `calendarAdminEntryIdGet()`

```php
calendarAdminEntryIdGet($id, $session): \OpenAPI\Client\Model\CalendarAdminEntryIdGet200Response
```

Get calendar entry

This endpoint is for retrieving an entry of a calendar.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"` (not for \"Appointment\" calendars)

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\CalendarAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Entry ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->calendarAdminEntryIdGet($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CalendarAdminApi->calendarAdminEntryIdGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Entry ID | |
| **session** | **string**| JWT | |

### Return type

[**\OpenAPI\Client\Model\CalendarAdminEntryIdGet200Response**](../Model/CalendarAdminEntryIdGet200Response.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `calendarAdminEntryIdPut()`

```php
calendarAdminEntryIdPut($id, $session, $request): \OpenAPI\Client\Model\CalendarAdminEntryIdGet200Response
```

Update calendar entry

This endpoint is for updating a calendar entry. Calendars of `type` \"Appointment\" are readonly.  __Note:__ Widgets for tab type `WidgetPartyDirectory` must not have a `referenceId`  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"` (not for \"Appointment\" calendars)

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\CalendarAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Entry ID
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\ContentEntryRequest(); // \OpenAPI\Client\Model\ContentEntryRequest | calendar content entry to be replaced

try {
    $result = $apiInstance->calendarAdminEntryIdPut($id, $session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CalendarAdminApi->calendarAdminEntryIdPut: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Entry ID | |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\ContentEntryRequest**](../Model/ContentEntryRequest.md)| calendar content entry to be replaced | |

### Return type

[**\OpenAPI\Client\Model\CalendarAdminEntryIdGet200Response**](../Model/CalendarAdminEntryIdGet200Response.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `calendarAdminIdContentGet()`

```php
calendarAdminIdContentGet($id, $session, $cursor, $limit, $page): \OpenAPI\Client\Model\ContentEntryResponseListAdmin[]
```

Get calendar entries list for calendar

This endpoint is for retrieving all entries of the requested calendar in admin representation. The entries are sorted by `dateTime.dateStart:ASC` `dateTime.timeStart:ASC` `position:ASC`. If a limit is set, a cursor for this endpoint may be created to iterate over all calendar entries.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"` (not for \"Appointment\" calendars)

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\CalendarAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Calendar ID
$session = 'session_example'; // string | JWT
$cursor = 'cursor_example'; // string | id of the cursor used for pagination; required if page is set
$limit = 56; // int | amount of results per page (1 ... 100)
$page = 56; // int | current page index of the cursor used for pagination; required if cursor is set

try {
    $result = $apiInstance->calendarAdminIdContentGet($id, $session, $cursor, $limit, $page);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CalendarAdminApi->calendarAdminIdContentGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Calendar ID | |
| **session** | **string**| JWT | |
| **cursor** | **string**| id of the cursor used for pagination; required if page is set | [optional] |
| **limit** | **int**| amount of results per page (1 ... 100) | [optional] |
| **page** | **int**| current page index of the cursor used for pagination; required if cursor is set | [optional] |

### Return type

[**\OpenAPI\Client\Model\ContentEntryResponseListAdmin[]**](../Model/ContentEntryResponseListAdmin.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `calendarAdminIdContentPost()`

```php
calendarAdminIdContentPost($id, $session, $request): \OpenAPI\Client\Model\CalendarAdminIdContentPost200ResponseInner[]
```

Add calendar entries

This endpoint is for adding new entries to the requested calendar. Calendars of `type` \"Appointment\" are readonly. In case of response status is 205 the request was only executed partial. Use GET to receive the stored configuration.  __Note:__ Widgets for tab type `WidgetPartyDirectory` must not have a `referenceId`  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"` (not for \"Appointment\" calendars)

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\CalendarAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Calendar ID
$session = 'session_example'; // string | JWT
$request = array(new \OpenAPI\Client\Model\ContentEntryPostRequest()); // \OpenAPI\Client\Model\ContentEntryPostRequest[] | calendar content entries to create; max 100 elements are permitted per request

try {
    $result = $apiInstance->calendarAdminIdContentPost($id, $session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CalendarAdminApi->calendarAdminIdContentPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Calendar ID | |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\ContentEntryPostRequest[]**](../Model/ContentEntryPostRequest.md)| calendar content entries to create; max 100 elements are permitted per request | |

### Return type

[**\OpenAPI\Client\Model\CalendarAdminIdContentPost200ResponseInner[]**](../Model/CalendarAdminIdContentPost200ResponseInner.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `calendarAdminIdDelete()`

```php
calendarAdminIdDelete($id, $session): \OpenAPI\Client\Model\ModelSwagStatusOk
```

Delete calendar

This endpoint is for deleting a calendar with all localizations. Calendars of `type` \"Appointment\" are readonly.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"` (not for \"Appointment\" calendars)

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\CalendarAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Calendar ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->calendarAdminIdDelete($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CalendarAdminApi->calendarAdminIdDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Calendar ID | |
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

## `calendarAdminIdDetailGet()`

```php
calendarAdminIdDetailGet($id, $session): \OpenAPI\Client\Model\CalendarAdminIdDetailGet200Response
```

Get calendar detail view

This endpoint is for retrieving the detail config, items and selections of a calendar  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\CalendarAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Calendar ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->calendarAdminIdDetailGet($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CalendarAdminApi->calendarAdminIdDetailGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Calendar ID | |
| **session** | **string**| JWT | |

### Return type

[**\OpenAPI\Client\Model\CalendarAdminIdDetailGet200Response**](../Model/CalendarAdminIdDetailGet200Response.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `calendarAdminIdDetailPut()`

```php
calendarAdminIdDetailPut($id, $session, $request): \OpenAPI\Client\Model\CalendarAdminIdDetailGet200Response
```

Update calendar detail view

__Endpoint is returning 501 only at the moment!__  This endpoint is for updating the detail of an existing calendar. New Items need a client generated unique id for setting reference in detail. client generated id will be changed from server so item ids in response will differ! Calendars of `type` \"Appointment\" are readonly.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"` (not for \"Appointment\" calendars)

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\CalendarAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Calendar ID
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\CalendarPutDetailRequest(); // \OpenAPI\Client\Model\CalendarPutDetailRequest | detail to be updated

try {
    $result = $apiInstance->calendarAdminIdDetailPut($id, $session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CalendarAdminApi->calendarAdminIdDetailPut: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Calendar ID | |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\CalendarPutDetailRequest**](../Model/CalendarPutDetailRequest.md)| detail to be updated | |

### Return type

[**\OpenAPI\Client\Model\CalendarAdminIdDetailGet200Response**](../Model/CalendarAdminIdDetailGet200Response.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `calendarAdminIdGet()`

```php
calendarAdminIdGet($id, $session): \OpenAPI\Client\Model\CalendarAdminPost200Response
```

Get calendar

This endpoint is for retrieving one calendar in admin representation.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\CalendarAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Calendar ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->calendarAdminIdGet($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CalendarAdminApi->calendarAdminIdGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Calendar ID | |
| **session** | **string**| JWT | |

### Return type

[**\OpenAPI\Client\Model\CalendarAdminPost200Response**](../Model/CalendarAdminPost200Response.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `calendarAdminIdItemsGet()`

```php
calendarAdminIdItemsGet($id, $session): \OpenAPI\Client\Model\CalendarSwagResponseCalendarItem[]
```

Get calendar detail view items

This endpoint is for retrieving calendar items.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\CalendarAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Calendar ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->calendarAdminIdItemsGet($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CalendarAdminApi->calendarAdminIdItemsGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Calendar ID | |
| **session** | **string**| JWT | |

### Return type

[**\OpenAPI\Client\Model\CalendarSwagResponseCalendarItem[]**](../Model/CalendarSwagResponseCalendarItem.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `calendarAdminIdListSettingsGet()`

```php
calendarAdminIdListSettingsGet($id, $session): \OpenAPI\Client\Model\ModelCalendarListSettings
```

Get calendar list settings

This endpoint is for retrieving the list settings of a specific calendar  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\CalendarAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Calendar ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->calendarAdminIdListSettingsGet($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CalendarAdminApi->calendarAdminIdListSettingsGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Calendar ID | |
| **session** | **string**| JWT | [optional] |

### Return type

[**\OpenAPI\Client\Model\ModelCalendarListSettings**](../Model/ModelCalendarListSettings.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `calendarAdminIdListSettingsPut()`

```php
calendarAdminIdListSettingsPut($id, $session, $request): \OpenAPI\Client\Model\ModelCalendarListSettings
```

Update calendar list settings

This endpoint is for updating the list settings of an existing calendar. Calendars of `type` \"Appointment\" are readonly.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"` (not for \"Appointment\" calendars)

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\CalendarAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Calendar ID
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\ModelCalendarListSettings(); // \OpenAPI\Client\Model\ModelCalendarListSettings | list settings to be updated

try {
    $result = $apiInstance->calendarAdminIdListSettingsPut($id, $session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CalendarAdminApi->calendarAdminIdListSettingsPut: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Calendar ID | |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\ModelCalendarListSettings**](../Model/ModelCalendarListSettings.md)| list settings to be updated | |

### Return type

[**\OpenAPI\Client\Model\ModelCalendarListSettings**](../Model/ModelCalendarListSettings.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `calendarAdminIdPatch()`

```php
calendarAdminIdPatch($id, $session, $request): \OpenAPI\Client\Model\CalendarAdminPost200Response
```

Update calendar info

This endpoint is for updating the base info of an existing calendar. Calendars of `type` \"Appointment\" are readonly.  ___createAccesses.CalendarEntry.any___: must be false; true currently not supported  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"` (not for \"Appointment\" calendars)

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\CalendarAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Calendar ID
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\CalendarPatchRequest(); // \OpenAPI\Client\Model\CalendarPatchRequest | calendar information to be updated

try {
    $result = $apiInstance->calendarAdminIdPatch($id, $session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CalendarAdminApi->calendarAdminIdPatch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Calendar ID | |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\CalendarPatchRequest**](../Model/CalendarPatchRequest.md)| calendar information to be updated | |

### Return type

[**\OpenAPI\Client\Model\CalendarAdminPost200Response**](../Model/CalendarAdminPost200Response.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `calendarAdminIdSelectionsGet()`

```php
calendarAdminIdSelectionsGet($id, $session): \OpenAPI\Client\Model\SelectionAPIResponseAdmin[]
```

Get calendar detail view selections

This endpoint is for retrieving calendar selections.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\CalendarAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Calendar ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->calendarAdminIdSelectionsGet($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CalendarAdminApi->calendarAdminIdSelectionsGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Calendar ID | |
| **session** | **string**| JWT | |

### Return type

[**\OpenAPI\Client\Model\SelectionAPIResponseAdmin[]**](../Model/SelectionAPIResponseAdmin.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `calendarAdminPost()`

```php
calendarAdminPost($session, $request): \OpenAPI\Client\Model\CalendarAdminPost200Response
```

Create calendar

This endpoint is for creating a new calendar for chosen template.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\CalendarAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\CalendarPostRequest(); // \OpenAPI\Client\Model\CalendarPostRequest | calendar to create

try {
    $result = $apiInstance->calendarAdminPost($session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CalendarAdminApi->calendarAdminPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\CalendarPostRequest**](../Model/CalendarPostRequest.md)| calendar to create | |

### Return type

[**\OpenAPI\Client\Model\CalendarAdminPost200Response**](../Model/CalendarAdminPost200Response.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `calendarAdminProjectIdGet()`

```php
calendarAdminProjectIdGet($id, $session, $cursor, $limit, $page): \OpenAPI\Client\Model\CalendarAdminProjectIdGet200ResponseInner[]
```

Get calendar list for project

This endpoint is for retrieving all calendars of a project in admin representation. If a limit is set, a cursor for this endpoint may be created to iterate over all calendars.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\CalendarAdminApi(
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
    $result = $apiInstance->calendarAdminProjectIdGet($id, $session, $cursor, $limit, $page);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CalendarAdminApi->calendarAdminProjectIdGet: ', $e->getMessage(), PHP_EOL;
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

[**\OpenAPI\Client\Model\CalendarAdminProjectIdGet200ResponseInner[]**](../Model/CalendarAdminProjectIdGet200ResponseInner.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `calendarAdminSyncPut()`

```php
calendarAdminSyncPut($session): \OpenAPI\Client\Model\ModelSwagStatusOk
```

Sync operators for all calendar entries

This endpoint is sync operators for all chat feeds with sendbird. This endpoint should rarely be used because of its workload.  _only accessible with permission_ : `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\CalendarAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->calendarAdminSyncPut($session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CalendarAdminApi->calendarAdminSyncPut: ', $e->getMessage(), PHP_EOL;
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

## `calendarAdminTemplateGet()`

```php
calendarAdminTemplateGet($session, $cursor, $limit, $page): \OpenAPI\Client\Model\CalendarAdminTemplateGet200ResponseInner[]
```

Get calendar template list

This endpoint retrieving templates to enhance the creation of new calendars. If a limit is set, a cursor for this endpoint may be created to iterate over all templates.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\CalendarAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT
$cursor = 'cursor_example'; // string | id of the cursor used for pagination; required if page is set
$limit = 56; // int | amount of results per page (1 ... 100)
$page = 56; // int | current page index of the cursor used for pagination; required if cursor is set

try {
    $result = $apiInstance->calendarAdminTemplateGet($session, $cursor, $limit, $page);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CalendarAdminApi->calendarAdminTemplateGet: ', $e->getMessage(), PHP_EOL;
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

[**\OpenAPI\Client\Model\CalendarAdminTemplateGet200ResponseInner[]**](../Model/CalendarAdminTemplateGet200ResponseInner.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
