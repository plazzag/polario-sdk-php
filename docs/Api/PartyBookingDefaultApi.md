# OpenAPI\Client\PartyBookingDefaultApi



All URIs are relative to https://custom.polario.de/api, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**partyDefaultGet()**](PartyBookingDefaultApi.md#partyDefaultGet) | **GET** /party/default | Get party list for cursor |
| [**partyDefaultObjectTypeObjectIdGet()**](PartyBookingDefaultApi.md#partyDefaultObjectTypeObjectIdGet) | **GET** /party/default/{objectType}/{objectId} | Get party |
| [**partyDefaultObjectTypeReferenceObjectIdGet()**](PartyBookingDefaultApi.md#partyDefaultObjectTypeReferenceObjectIdGet) | **GET** /party/default/{objectType}/reference/{objectId} | Get parties for reference |
| [**partyDefaultSearchPost()**](PartyBookingDefaultApi.md#partyDefaultSearchPost) | **POST** /party/default/search | Create cursor parties |


## `partyDefaultGet()`

```php
partyDefaultGet($cursor, $page, $session, $limit): \OpenAPI\Client\Model\PartyResponseDefault[]
```

Get party list for cursor

This endpoint returns a list of all parties for a cursor in default representation.  Cursor could be created here: POST /party/default/search  _accessible without permission_

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\PartyBookingDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$cursor = 'cursor_example'; // string | id of the cursor used for pagination; required if page is set
$page = 56; // int | current page index of the cursor used for pagination; required if cursor is set
$session = 'session_example'; // string | JWT
$limit = 56; // int | amount of results per page (1 ... 100)

try {
    $result = $apiInstance->partyDefaultGet($cursor, $page, $session, $limit);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PartyBookingDefaultApi->partyDefaultGet: ', $e->getMessage(), PHP_EOL;
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

[**\OpenAPI\Client\Model\PartyResponseDefault[]**](../Model/PartyResponseDefault.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `partyDefaultObjectTypeObjectIdGet()`

```php
partyDefaultObjectTypeObjectIdGet($object_type, $object_id, $session): \OpenAPI\Client\Model\PartyResponseDefault
```

Get party

This endpoint returns a party in default representation by given id.  __Note:__ for objectType `CalendarEntry` _config.bookingSlots.dateEnd_ and _config.bookingSlots.timeEnd_ will not be null  _accessible without permission_  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\PartyBookingDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$object_type = 'object_type_example'; // string | object type
$object_id = 'object_id_example'; // string | object id
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->partyDefaultObjectTypeObjectIdGet($object_type, $object_id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PartyBookingDefaultApi->partyDefaultObjectTypeObjectIdGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **object_type** | **string**| object type | |
| **object_id** | **string**| object id | |
| **session** | **string**| JWT | |

### Return type

[**\OpenAPI\Client\Model\PartyResponseDefault**](../Model/PartyResponseDefault.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `partyDefaultObjectTypeReferenceObjectIdGet()`

```php
partyDefaultObjectTypeReferenceObjectIdGet($object_type, $object_id, $session, $cursor, $limit, $page): \OpenAPI\Client\Model\PartyResponseDefault[]
```

Get parties for reference

This endpoint returns all parties for the provided reference in default representation. If the limit is set, a cursor for this endpoint may be created to iterate over all locations.  __Note:__ for objectType `CalendarEntry` _config.bookingSlots.dateEnd_ and _config.bookingSlots.timeEnd_ will not be null; objectId is calendarId (referenceId)  _accessible without permission_  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\PartyBookingDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$object_type = 'object_type_example'; // string | object type
$object_id = 'object_id_example'; // string | reference id
$session = 'session_example'; // string | JWT
$cursor = 'cursor_example'; // string | id of the cursor used for pagination; required if page is set
$limit = 56; // int | amount of results per page (1 ... 100)
$page = 56; // int | current page index of the cursor used for pagination; required if cursor is set

try {
    $result = $apiInstance->partyDefaultObjectTypeReferenceObjectIdGet($object_type, $object_id, $session, $cursor, $limit, $page);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PartyBookingDefaultApi->partyDefaultObjectTypeReferenceObjectIdGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **object_type** | **string**| object type | |
| **object_id** | **string**| reference id | |
| **session** | **string**| JWT | |
| **cursor** | **string**| id of the cursor used for pagination; required if page is set | [optional] |
| **limit** | **int**| amount of results per page (1 ... 100) | [optional] |
| **page** | **int**| current page index of the cursor used for pagination; required if cursor is set | [optional] |

### Return type

[**\OpenAPI\Client\Model\PartyResponseDefault[]**](../Model/PartyResponseDefault.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `partyDefaultSearchPost()`

```php
partyDefaultSearchPost($session, $request): \OpenAPI\Client\Model\ModelCursorResponse
```

Create cursor parties

This endpoint returns a cursor for list parties in default representation with applied filter and sort options. In case of cursor response total will be 0 the status 204 with not content is returned instead.  _accessible without permission_  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\PartyBookingDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\PartyCursorRequestDefault(); // \OpenAPI\Client\Model\PartyCursorRequestDefault | options to create cursor

try {
    $result = $apiInstance->partyDefaultSearchPost($session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PartyBookingDefaultApi->partyDefaultSearchPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\PartyCursorRequestDefault**](../Model/PartyCursorRequestDefault.md)| options to create cursor | |

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
