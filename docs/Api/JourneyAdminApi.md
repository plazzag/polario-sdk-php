# OpenAPI\Client\JourneyAdminApi



All URIs are relative to https://custom.polario.de/api, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**reactionAdminJourneyIdAttendeeDelete()**](JourneyAdminApi.md#reactionAdminJourneyIdAttendeeDelete) | **DELETE** /reaction/admin/journey/{id}/attendee | Remove attendees |
| [**reactionAdminJourneyIdAttendeeGet()**](JourneyAdminApi.md#reactionAdminJourneyIdAttendeeGet) | **GET** /reaction/admin/journey/{id}/attendee | Get attendees |
| [**reactionAdminJourneyIdAttendeePatch()**](JourneyAdminApi.md#reactionAdminJourneyIdAttendeePatch) | **PATCH** /reaction/admin/journey/{id}/attendee | Update attendees |
| [**reactionAdminJourneyIdAttendeePost()**](JourneyAdminApi.md#reactionAdminJourneyIdAttendeePost) | **POST** /reaction/admin/journey/{id}/attendee | Add attendees |
| [**reactionAdminJourneyIdDelete()**](JourneyAdminApi.md#reactionAdminJourneyIdDelete) | **DELETE** /reaction/admin/journey/{id} | Delete journey |
| [**reactionAdminJourneyIdGet()**](JourneyAdminApi.md#reactionAdminJourneyIdGet) | **GET** /reaction/admin/journey/{id} | Get journey |
| [**reactionAdminJourneyIdPatch()**](JourneyAdminApi.md#reactionAdminJourneyIdPatch) | **PATCH** /reaction/admin/journey/{id} | Update journey |
| [**reactionAdminJourneyIdStagesGet()**](JourneyAdminApi.md#reactionAdminJourneyIdStagesGet) | **GET** /reaction/admin/journey/{id}/stages | Get stages |
| [**reactionAdminJourneyIdStagesPut()**](JourneyAdminApi.md#reactionAdminJourneyIdStagesPut) | **PUT** /reaction/admin/journey/{id}/stages | Update stages |
| [**reactionAdminJourneyPost()**](JourneyAdminApi.md#reactionAdminJourneyPost) | **POST** /reaction/admin/journey | Create journey |
| [**reactionAdminJourneyProjectIdGet()**](JourneyAdminApi.md#reactionAdminJourneyProjectIdGet) | **GET** /reaction/admin/journey/project/{id} | Get journey list for project |


## `reactionAdminJourneyIdAttendeeDelete()`

```php
reactionAdminJourneyIdAttendeeDelete($id, $session, $ids): \OpenAPI\Client\Model\ModelSwagStatusOk
```

Remove attendees

This endpoint is for removing journey processes. Note: when no query parameter is set, all attendees will be removed.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\JourneyAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Journey ID
$session = 'session_example'; // string | JWT
$ids = 'ids_example'; // string | account ids to be removed from journey

try {
    $result = $apiInstance->reactionAdminJourneyIdAttendeeDelete($id, $session, $ids);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling JourneyAdminApi->reactionAdminJourneyIdAttendeeDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Journey ID | |
| **session** | **string**| JWT | |
| **ids** | **string**| account ids to be removed from journey | [optional] |

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

## `reactionAdminJourneyIdAttendeeGet()`

```php
reactionAdminJourneyIdAttendeeGet($id, $session, $cursor, $limit, $page): \OpenAPI\Client\Model\JourneyprocessResponseAdmin[]
```

Get attendees

This endpoint is for retrieving attendees from journey processes.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\JourneyAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Journey ID
$session = 'session_example'; // string | JWT
$cursor = 'cursor_example'; // string | id of the cursor used for pagination; required if page is set
$limit = 56; // int | amount of results per page (1 ... 100)
$page = 56; // int | current page index of the cursor used for pagination; required if cursor is set

try {
    $result = $apiInstance->reactionAdminJourneyIdAttendeeGet($id, $session, $cursor, $limit, $page);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling JourneyAdminApi->reactionAdminJourneyIdAttendeeGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Journey ID | |
| **session** | **string**| JWT | |
| **cursor** | **string**| id of the cursor used for pagination; required if page is set | [optional] |
| **limit** | **int**| amount of results per page (1 ... 100) | [optional] |
| **page** | **int**| current page index of the cursor used for pagination; required if cursor is set | [optional] |

### Return type

[**\OpenAPI\Client\Model\JourneyprocessResponseAdmin[]**](../Model/JourneyprocessResponseAdmin.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `reactionAdminJourneyIdAttendeePatch()`

```php
reactionAdminJourneyIdAttendeePatch($id, $session, $request, $ids): \OpenAPI\Client\Model\ModelSwagStatusOk
```

Update attendees

This endpoint is for updating journey processes. Note: when no query parameter is set, all attendees will be updated.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\JourneyAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Journey ID
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\JourneyprocessPatchRequest(); // \OpenAPI\Client\Model\JourneyprocessPatchRequest | values to patch attendees for
$ids = 'ids_example'; // string | account ids to be updated

try {
    $result = $apiInstance->reactionAdminJourneyIdAttendeePatch($id, $session, $request, $ids);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling JourneyAdminApi->reactionAdminJourneyIdAttendeePatch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Journey ID | |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\JourneyprocessPatchRequest**](../Model/JourneyprocessPatchRequest.md)| values to patch attendees for | |
| **ids** | **string**| account ids to be updated | [optional] |

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

## `reactionAdminJourneyIdAttendeePost()`

```php
reactionAdminJourneyIdAttendeePost($id, $session, $request): \OpenAPI\Client\Model\JourneyprocessResponseAdmin[]
```

Add attendees

This endpoint is for creating new journey processes by adding attendees.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\JourneyAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Journey ID
$session = 'session_example'; // string | JWT
$request = array(new \OpenAPI\Client\Model\JourneyprocessPostEntry()); // \OpenAPI\Client\Model\JourneyprocessPostEntry[] | Attendees to create

try {
    $result = $apiInstance->reactionAdminJourneyIdAttendeePost($id, $session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling JourneyAdminApi->reactionAdminJourneyIdAttendeePost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Journey ID | |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\JourneyprocessPostEntry[]**](../Model/JourneyprocessPostEntry.md)| Attendees to create | |

### Return type

[**\OpenAPI\Client\Model\JourneyprocessResponseAdmin[]**](../Model/JourneyprocessResponseAdmin.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `reactionAdminJourneyIdDelete()`

```php
reactionAdminJourneyIdDelete($id, $session): \OpenAPI\Client\Model\ModelSwagStatusOk
```

Delete journey

This endpoint is for deleting a single journey with all localizations.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\JourneyAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Journey ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->reactionAdminJourneyIdDelete($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling JourneyAdminApi->reactionAdminJourneyIdDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Journey ID | |
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

## `reactionAdminJourneyIdGet()`

```php
reactionAdminJourneyIdGet($id, $session): \OpenAPI\Client\Model\JourneyResponseAdmin
```

Get journey

This endpoint returns a journey in administrative representation by given id.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\JourneyAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Journey ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->reactionAdminJourneyIdGet($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling JourneyAdminApi->reactionAdminJourneyIdGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Journey ID | |
| **session** | **string**| JWT | |

### Return type

[**\OpenAPI\Client\Model\JourneyResponseAdmin**](../Model/JourneyResponseAdmin.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `reactionAdminJourneyIdPatch()`

```php
reactionAdminJourneyIdPatch($id, $session, $request): \OpenAPI\Client\Model\JourneyResponseAdmin
```

Update journey

This endpoint is for updating specific data of an existing journey.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\JourneyAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Journey ID
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\JourneyPatchRequest(); // \OpenAPI\Client\Model\JourneyPatchRequest | journey data to be updated

try {
    $result = $apiInstance->reactionAdminJourneyIdPatch($id, $session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling JourneyAdminApi->reactionAdminJourneyIdPatch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Journey ID | |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\JourneyPatchRequest**](../Model/JourneyPatchRequest.md)| journey data to be updated | [optional] |

### Return type

[**\OpenAPI\Client\Model\JourneyResponseAdmin**](../Model/JourneyResponseAdmin.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `reactionAdminJourneyIdStagesGet()`

```php
reactionAdminJourneyIdStagesGet($id, $session): \OpenAPI\Client\Model\JourneyResponseStageAdmin[]
```

Get stages

This endpoint returns the stages for a journey object in administrative representation by given id.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\JourneyAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Journey ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->reactionAdminJourneyIdStagesGet($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling JourneyAdminApi->reactionAdminJourneyIdStagesGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Journey ID | |
| **session** | **string**| JWT | |

### Return type

[**\OpenAPI\Client\Model\JourneyResponseStageAdmin[]**](../Model/JourneyResponseStageAdmin.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `reactionAdminJourneyIdStagesPut()`

```php
reactionAdminJourneyIdStagesPut($id, $session, $request): \OpenAPI\Client\Model\JourneyResponseStageAdmin[]
```

Update stages

This endpoint updates the stages for a journey object in administrative representation by given id.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\JourneyAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Journey ID
$session = 'session_example'; // string | JWT
$request = array(new \OpenAPI\Client\Model\JourneyRequestStage()); // \OpenAPI\Client\Model\JourneyRequestStage[] | journey stages to be updated

try {
    $result = $apiInstance->reactionAdminJourneyIdStagesPut($id, $session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling JourneyAdminApi->reactionAdminJourneyIdStagesPut: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Journey ID | |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\JourneyRequestStage[]**](../Model/JourneyRequestStage.md)| journey stages to be updated | |

### Return type

[**\OpenAPI\Client\Model\JourneyResponseStageAdmin[]**](../Model/JourneyResponseStageAdmin.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `reactionAdminJourneyPost()`

```php
reactionAdminJourneyPost($session, $request): \OpenAPI\Client\Model\JourneyResponseAdmin
```

Create journey

This endpoint is for creating a new journey.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\JourneyAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\JourneyPostRequest(); // \OpenAPI\Client\Model\JourneyPostRequest | Journey to create

try {
    $result = $apiInstance->reactionAdminJourneyPost($session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling JourneyAdminApi->reactionAdminJourneyPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\JourneyPostRequest**](../Model/JourneyPostRequest.md)| Journey to create | |

### Return type

[**\OpenAPI\Client\Model\JourneyResponseAdmin**](../Model/JourneyResponseAdmin.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `reactionAdminJourneyProjectIdGet()`

```php
reactionAdminJourneyProjectIdGet($id, $session, $cursor, $limit, $page): \OpenAPI\Client\Model\JourneyResponseListAdmin[]
```

Get journey list for project

This endpoint returns a list of all journeys for the requested project without items in administrative representation. If a limit is set, a cursor for this endpoint may be created to iterate over all journeys.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\JourneyAdminApi(
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
    $result = $apiInstance->reactionAdminJourneyProjectIdGet($id, $session, $cursor, $limit, $page);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling JourneyAdminApi->reactionAdminJourneyProjectIdGet: ', $e->getMessage(), PHP_EOL;
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

[**\OpenAPI\Client\Model\JourneyResponseListAdmin[]**](../Model/JourneyResponseListAdmin.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
