# OpenAPI\Client\CalendarDefaultApi



All URIs are relative to https://custom.polario.de/api, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**calendarDefaultEntryGet()**](CalendarDefaultApi.md#calendarDefaultEntryGet) | **GET** /calendar/default/entry | Get calendar entries list for cursor |
| [**calendarDefaultEntryIdBookingGet()**](CalendarDefaultApi.md#calendarDefaultEntryIdBookingGet) | **GET** /calendar/default/entry/{id}/booking | Get booking |
| [**calendarDefaultEntryIdGet()**](CalendarDefaultApi.md#calendarDefaultEntryIdGet) | **GET** /calendar/default/entry/{id} | Get calendar entry |
| [**calendarDefaultEntrySearchPost()**](CalendarDefaultApi.md#calendarDefaultEntrySearchPost) | **POST** /calendar/default/entry/search | Create entry cursor |
| [**calendarDefaultIdContentGet()**](CalendarDefaultApi.md#calendarDefaultIdContentGet) | **GET** /calendar/default/{id}/content | Get calendar entries list for calendar |
| [**calendarDefaultIdGet()**](CalendarDefaultApi.md#calendarDefaultIdGet) | **GET** /calendar/default/{id} | Get calendar |
| [**calendarDefaultMyCalendarContentGet()**](CalendarDefaultApi.md#calendarDefaultMyCalendarContentGet) | **GET** /calendar/default/my-calendar/content | Get calendar entries list for my calendar |
| [**calendarDefaultMyCalendarGet()**](CalendarDefaultApi.md#calendarDefaultMyCalendarGet) | **GET** /calendar/default/my-calendar | Get my calendar |


## `calendarDefaultEntryGet()`

```php
calendarDefaultEntryGet($cursor, $page, $limit, $accept_language, $session): \OpenAPI\Client\Model\ContentEntryResponseListDefault[]
```

Get calendar entries list for cursor

This endpoint is for retrieving all entries for the requested cursor in default representation.  Cursor could be created here: POST /calendar/default/entry/search  _accessible without permission_

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\CalendarDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$cursor = 'cursor_example'; // string | id of the cursor used for pagination; required if page is set
$page = 56; // int | current page index of the cursor used for pagination; required if cursor is set
$limit = 56; // int | amount of results per page (1 ... 100)
$accept_language = 'accept_language_example'; // string | client language(s)
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->calendarDefaultEntryGet($cursor, $page, $limit, $accept_language, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CalendarDefaultApi->calendarDefaultEntryGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **cursor** | **string**| id of the cursor used for pagination; required if page is set | |
| **page** | **int**| current page index of the cursor used for pagination; required if cursor is set | |
| **limit** | **int**| amount of results per page (1 ... 100) | [optional] |
| **accept_language** | **string**| client language(s) | [optional] |
| **session** | **string**| JWT | [optional] |

### Return type

[**\OpenAPI\Client\Model\ContentEntryResponseListDefault[]**](../Model/ContentEntryResponseListDefault.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `calendarDefaultEntryIdBookingGet()`

```php
calendarDefaultEntryIdBookingGet($id, $session): \OpenAPI\Client\Model\BookingCalendarBookingResponseDefault
```

Get booking

This endpoint is for retrieving calendar entry's booking in default representation.  _accessible without permission_ (can only be used for the own account. Session must match requested account id.)

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\CalendarDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Entry ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->calendarDefaultEntryIdBookingGet($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CalendarDefaultApi->calendarDefaultEntryIdBookingGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Entry ID | |
| **session** | **string**| JWT | |

### Return type

[**\OpenAPI\Client\Model\BookingCalendarBookingResponseDefault**](../Model/BookingCalendarBookingResponseDefault.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `calendarDefaultEntryIdGet()`

```php
calendarDefaultEntryIdGet($id, $accept_language, $session): \OpenAPI\Client\Model\CalendarDefaultEntryIdGet200Response
```

Get calendar entry

This endpoint is for retrieving an entry of a calendar.  _accessible without permission_  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"` (not for \"Appointment\" calendars)

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\CalendarDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Entry ID
$accept_language = 'accept_language_example'; // string | client language(s)
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->calendarDefaultEntryIdGet($id, $accept_language, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CalendarDefaultApi->calendarDefaultEntryIdGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Entry ID | |
| **accept_language** | **string**| client language(s) | [optional] |
| **session** | **string**| JWT | [optional] |

### Return type

[**\OpenAPI\Client\Model\CalendarDefaultEntryIdGet200Response**](../Model/CalendarDefaultEntryIdGet200Response.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `calendarDefaultEntrySearchPost()`

```php
calendarDefaultEntrySearchPost($request, $accept_language, $session): \OpenAPI\Client\Model\ModelCursorResponse
```

Create entry cursor

This endpoint returns a cursor for list published calendar entries in default representation with applied filter and sort options. In case of cursor response total will be 0 the status 204 with not content is returned instead.  _accessible without permission_

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\CalendarDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$request = new \OpenAPI\Client\Model\GitPlazzNetReposSandmannBackendServicesCalendarContentCursorFilterOptionDefault(); // \OpenAPI\Client\Model\GitPlazzNetReposSandmannBackendServicesCalendarContentCursorFilterOptionDefault | options to create cursor
$accept_language = 'accept_language_example'; // string | client language(s)
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->calendarDefaultEntrySearchPost($request, $accept_language, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CalendarDefaultApi->calendarDefaultEntrySearchPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **request** | [**\OpenAPI\Client\Model\GitPlazzNetReposSandmannBackendServicesCalendarContentCursorFilterOptionDefault**](../Model/GitPlazzNetReposSandmannBackendServicesCalendarContentCursorFilterOptionDefault.md)| options to create cursor | |
| **accept_language** | **string**| client language(s) | [optional] |
| **session** | **string**| JWT | [optional] |

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

## `calendarDefaultIdContentGet()`

```php
calendarDefaultIdContentGet($id, $cursor, $limit, $page, $accept_language, $session): \OpenAPI\Client\Model\ContentDeprecatedEntryResponseListDefault[]
```

Get calendar entries list for calendar

This endpoint is for retrieving all entries of the requested calendar in default representation. The entries are sorted by `dateTime.dateStart:ASC` `dateTime.timeStart:ASC` `position:ASC`. If a limit is set, a cursor for this endpoint may be created to iterate over all calendar entries.  _accessible without permission_

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\CalendarDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Calendar ID
$cursor = 'cursor_example'; // string | id of the cursor used for pagination; required if page is set
$limit = 56; // int | amount of results per page (1 ... 100)
$page = 56; // int | current page index of the cursor used for pagination; required if cursor is set
$accept_language = 'accept_language_example'; // string | client language(s)
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->calendarDefaultIdContentGet($id, $cursor, $limit, $page, $accept_language, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CalendarDefaultApi->calendarDefaultIdContentGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Calendar ID | |
| **cursor** | **string**| id of the cursor used for pagination; required if page is set | [optional] |
| **limit** | **int**| amount of results per page (1 ... 100) | [optional] |
| **page** | **int**| current page index of the cursor used for pagination; required if cursor is set | [optional] |
| **accept_language** | **string**| client language(s) | [optional] |
| **session** | **string**| JWT | [optional] |

### Return type

[**\OpenAPI\Client\Model\ContentDeprecatedEntryResponseListDefault[]**](../Model/ContentDeprecatedEntryResponseListDefault.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `calendarDefaultIdGet()`

```php
calendarDefaultIdGet($id, $accept_language, $session): \OpenAPI\Client\Model\CalendarDefaultIdGet200Response
```

Get calendar

This endpoint is for retrieving one calendar in default representation. If the requested language is not available it will fall back to the default language.  _accessible without permission_  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\CalendarDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Calendar ID
$accept_language = 'accept_language_example'; // string | client language(s)
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->calendarDefaultIdGet($id, $accept_language, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CalendarDefaultApi->calendarDefaultIdGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Calendar ID | |
| **accept_language** | **string**| client language(s) | [optional] |
| **session** | **string**| JWT | [optional] |

### Return type

[**\OpenAPI\Client\Model\CalendarDefaultIdGet200Response**](../Model/CalendarDefaultIdGet200Response.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `calendarDefaultMyCalendarContentGet()`

```php
calendarDefaultMyCalendarContentGet($session, $cursor, $limit, $page, $accept_language): \OpenAPI\Client\Model\ContentDeprecatedEntryResponseListDefault[]
```

Get calendar entries list for my calendar

This endpoint is for retrieving all entries of my calendar in default representation. The entries are sorted by `dateTime.dateStart:ASC` `dateTime.timeStart:ASC` `position:ASC`. If a limit is set, a cursor for this endpoint may be created to iterate over all calendar entries.  _accessible without permission_

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\CalendarDefaultApi(
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
    $result = $apiInstance->calendarDefaultMyCalendarContentGet($session, $cursor, $limit, $page, $accept_language);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CalendarDefaultApi->calendarDefaultMyCalendarContentGet: ', $e->getMessage(), PHP_EOL;
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

[**\OpenAPI\Client\Model\ContentDeprecatedEntryResponseListDefault[]**](../Model/ContentDeprecatedEntryResponseListDefault.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `calendarDefaultMyCalendarGet()`

```php
calendarDefaultMyCalendarGet($session): \OpenAPI\Client\Model\CalendarResponseDefault
```

Get my calendar

This endpoint is for retrieving my calendar in default representation.  _accessible without permission_

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\CalendarDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->calendarDefaultMyCalendarGet($session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CalendarDefaultApi->calendarDefaultMyCalendarGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **session** | **string**| JWT | |

### Return type

[**\OpenAPI\Client\Model\CalendarResponseDefault**](../Model/CalendarResponseDefault.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
