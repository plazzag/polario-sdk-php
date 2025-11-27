# OpenAPI\Client\ProjectAdminApi



All URIs are relative to https://custom.polario.de/api, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**projectAdminCopyGet()**](ProjectAdminApi.md#projectAdminCopyGet) | **GET** /project/admin/copy | Get project copy processes |
| [**projectAdminCopyIdGet()**](ProjectAdminApi.md#projectAdminCopyIdGet) | **GET** /project/admin/copy/{id} | Get project copy process |
| [**projectAdminGet()**](ProjectAdminApi.md#projectAdminGet) | **GET** /project/admin | Get project list |
| [**projectAdminIdAccessGet()**](ProjectAdminApi.md#projectAdminIdAccessGet) | **GET** /project/admin/{id}/access | Get project access configuration |
| [**projectAdminIdAccessPatch()**](ProjectAdminApi.md#projectAdminIdAccessPatch) | **PATCH** /project/admin/{id}/access | Update project access configuration |
| [**projectAdminIdCopyPost()**](ProjectAdminApi.md#projectAdminIdCopyPost) | **POST** /project/admin/{id}/copy | Duplicate project |
| [**projectAdminIdDelete()**](ProjectAdminApi.md#projectAdminIdDelete) | **DELETE** /project/admin/{id} | Delete project |
| [**projectAdminIdGet()**](ProjectAdminApi.md#projectAdminIdGet) | **GET** /project/admin/{id} | Get project |
| [**projectAdminIdPatch()**](ProjectAdminApi.md#projectAdminIdPatch) | **PATCH** /project/admin/{id} | Update project |
| [**projectAdminIdSettingsGet()**](ProjectAdminApi.md#projectAdminIdSettingsGet) | **GET** /project/admin/{id}/settings | Get project settings |
| [**projectAdminIdSettingsTrackingGet()**](ProjectAdminApi.md#projectAdminIdSettingsTrackingGet) | **GET** /project/admin/{id}/settings/tracking | Get project tracking settings |
| [**projectAdminIdSettingsTrackingPatch()**](ProjectAdminApi.md#projectAdminIdSettingsTrackingPatch) | **PATCH** /project/admin/{id}/settings/tracking | Update project tracking settings |
| [**projectAdminPost()**](ProjectAdminApi.md#projectAdminPost) | **POST** /project/admin | Create project |


## `projectAdminCopyGet()`

```php
projectAdminCopyGet($session, $cursor, $limit, $page): \OpenAPI\Client\Model\CopyprocessResponse[]
```

Get project copy processes

This endpoint returns an array of all project copy processes. The output is in administrative representation and filtered for the user permissions.  _only accessible with permission_ : `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\ProjectAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT
$cursor = 'cursor_example'; // string | id of the cursor used for pagination; required if page is set
$limit = 56; // int | amount of results per page (1 ... 100)
$page = 56; // int | current page index of the cursor used for pagination; required if cursor is set

try {
    $result = $apiInstance->projectAdminCopyGet($session, $cursor, $limit, $page);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProjectAdminApi->projectAdminCopyGet: ', $e->getMessage(), PHP_EOL;
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

[**\OpenAPI\Client\Model\CopyprocessResponse[]**](../Model/CopyprocessResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `projectAdminCopyIdGet()`

```php
projectAdminCopyIdGet($id, $session): \OpenAPI\Client\Model\CopyprocessResponse
```

Get project copy process

This endpoint returns a project copy process in administrative representation by given id.  _only accessible with permission_ : `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\ProjectAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Process ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->projectAdminCopyIdGet($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProjectAdminApi->projectAdminCopyIdGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Process ID | |
| **session** | **string**| JWT | |

### Return type

[**\OpenAPI\Client\Model\CopyprocessResponse**](../Model/CopyprocessResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `projectAdminGet()`

```php
projectAdminGet($session, $cursor, $limit, $page): \OpenAPI\Client\Model\ProjectResponseListAdmin[]
```

Get project list

This endpoint returns an array of all projects. The output is in administrative representation and filtered for the user permissions. If a limit is set, a cursor for this endpoint may be created to iterate over all projects.  _only accessible with permission_ : `\"ManageConfiguration\"` `\"ManageContent\"` `\"ManageProjects\"` `\"ViewAnalytics\"` `\"ViewGlobalAnalytics\"`  _fully accessible with permission_ : `\"ManageConfiguration\"` `\"ManageContent\"` `\"ManageProjects\"` `\"ViewAnalytics\"` `\"ViewGlobalAnalytics\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\ProjectAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT
$cursor = 'cursor_example'; // string | id of the cursor used for pagination; required if page is set
$limit = 56; // int | amount of results per page (1 ... 100)
$page = 56; // int | current page index of the cursor used for pagination; required if cursor is set

try {
    $result = $apiInstance->projectAdminGet($session, $cursor, $limit, $page);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProjectAdminApi->projectAdminGet: ', $e->getMessage(), PHP_EOL;
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

[**\OpenAPI\Client\Model\ProjectResponseListAdmin[]**](../Model/ProjectResponseListAdmin.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `projectAdminIdAccessGet()`

```php
projectAdminIdAccessGet($id, $session): \OpenAPI\Client\Model\AuthorizationAccessResponse
```

Get project access configuration

This endpoint returns the access configuration for the requested project.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\ProjectAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Project ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->projectAdminIdAccessGet($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProjectAdminApi->projectAdminIdAccessGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Project ID | |
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

## `projectAdminIdAccessPatch()`

```php
projectAdminIdAccessPatch($id, $session, $request): \OpenAPI\Client\Model\ModelAccess
```

Update project access configuration

This endpoint updates the access configuration for the requested project. Only the changes should be transmitted due this endpoint. Projects with status to be `\"Copying\"` cannot be manipulated, status 409 Conflict will be returned.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\ProjectAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Project ID
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\ModelAccess(); // \OpenAPI\Client\Model\ModelAccess | changed access rights

try {
    $result = $apiInstance->projectAdminIdAccessPatch($id, $session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProjectAdminApi->projectAdminIdAccessPatch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Project ID | |
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

## `projectAdminIdCopyPost()`

```php
projectAdminIdCopyPost($id, $session, $request): \OpenAPI\Client\Model\CopyprocessResponse
```

Duplicate project

This endpoint is for duplicating a project and returns the process status with its id.  _only accessible with permission_ : `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\ProjectAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Project ID
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\CopyprocessRequest(); // \OpenAPI\Client\Model\CopyprocessRequest | Copy config

try {
    $result = $apiInstance->projectAdminIdCopyPost($id, $session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProjectAdminApi->projectAdminIdCopyPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Project ID | |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\CopyprocessRequest**](../Model/CopyprocessRequest.md)| Copy config | |

### Return type

[**\OpenAPI\Client\Model\CopyprocessResponse**](../Model/CopyprocessResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `projectAdminIdDelete()`

```php
projectAdminIdDelete($id, $session): \OpenAPI\Client\Model\ModelSwagStatusOk
```

Delete project

This endpoint is for deleting a single project with all localizations. Projects with status to be `\"Copying\"` cannot be manipulated, status 409 Conflict will be returned.  _only accessible with permission_ : `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\ProjectAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Project ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->projectAdminIdDelete($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProjectAdminApi->projectAdminIdDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Project ID | |
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

## `projectAdminIdGet()`

```php
projectAdminIdGet($id, $session): \OpenAPI\Client\Model\ProjectResponseAdmin
```

Get project

This endpoint returns a localized project in administrative representation by given id.  _only accessible with permission_ : `\"ManageConfiguration\"` `\"ManageContent\"` `\"ManageProjects\"` `\"ViewAnalytics\"` `\"ViewGlobalAnalytics\"`  _fully accessible with permission_ : `\"ManageConfiguration\"` `\"ManageContent\"` `\"ManageProjects\"` `\"ViewAnalytics\"` `\"ViewGlobalAnalytics\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\ProjectAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Project ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->projectAdminIdGet($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProjectAdminApi->projectAdminIdGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Project ID | |
| **session** | **string**| JWT | |

### Return type

[**\OpenAPI\Client\Model\ProjectResponseAdmin**](../Model/ProjectResponseAdmin.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `projectAdminIdPatch()`

```php
projectAdminIdPatch($id, $session, $request): \OpenAPI\Client\Model\ProjectResponseAdmin
```

Update project

This endpoint is for updating specific data of an existing project. Projects with status to be `\"Copying\"` cannot be manipulated, status 409 Conflict will be returned.  ___createAccesses.AppointmentConfig.any___: must be false; true currently not supported  ___createAccesses.Calendar.any___: must be false; true currently not supported  ___createAccesses.CalendarTemplate.any___: must be false; true currently not supported  ___createAccesses.ChatFeed.any___: must be false; true currently not supported  ___createAccesses.Directory.any___: must be false; true currently not supported  ___createAccesses.DirectoryTemplate.any___: must be false; true currently not supported  ___createAccesses.Group.any___: must be false; true currently not supported  ___createAccesses.Location.any___: must be false; true currently not supported  ___createAccesses.LocationMap.any___: must be false; true currently not supported  ___createAccesses.Media.any___: must be false; true currently not supported  ___createAccesses.MediaFolder.any___: must be false; true currently not supported  ___createAccesses.Menu.any___: must be false; true currently not supported  ___createAccesses.News.any___: must be false; true currently not supported  ___createAccesses.Notification.any___: must be false; true currently not supported  ___createAccesses.Page.any___: must be false; true currently not supported  ___createAccesses.Stream.any___: must be false; true currently not supported  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\ProjectAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Project ID
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\ProjectPatchRequest(); // \OpenAPI\Client\Model\ProjectPatchRequest | project data to be updated

try {
    $result = $apiInstance->projectAdminIdPatch($id, $session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProjectAdminApi->projectAdminIdPatch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Project ID | |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\ProjectPatchRequest**](../Model/ProjectPatchRequest.md)| project data to be updated | [optional] |

### Return type

[**\OpenAPI\Client\Model\ProjectResponseAdmin**](../Model/ProjectResponseAdmin.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `projectAdminIdSettingsGet()`

```php
projectAdminIdSettingsGet($id, $session): \OpenAPI\Client\Model\ProjectResponseSettings
```

Get project settings

This endpoint returns the settings for the requested project.  _only accessible with permission_ : `\"ManageConfiguration\"`  _fully accessible with permission_ : `\"ManageConfiguration\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\ProjectAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Project ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->projectAdminIdSettingsGet($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProjectAdminApi->projectAdminIdSettingsGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Project ID | |
| **session** | **string**| JWT | |

### Return type

[**\OpenAPI\Client\Model\ProjectResponseSettings**](../Model/ProjectResponseSettings.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `projectAdminIdSettingsTrackingGet()`

```php
projectAdminIdSettingsTrackingGet($id, $session): \OpenAPI\Client\Model\ProjectResponseTracking
```

Get project tracking settings

This endpoint returns the tracking settings for the requested project.  _only accessible with permission_ : `\"ManageConfiguration\"` `\"ViewAnalytics\"` `\"ViewGlobalAnalytics\"`  _fully accessible with permission_ : `\"ManageConfiguration\"` `\"ViewAnalytics\"` `\"ViewGlobalAnalytics\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\ProjectAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Project ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->projectAdminIdSettingsTrackingGet($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProjectAdminApi->projectAdminIdSettingsTrackingGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Project ID | |
| **session** | **string**| JWT | |

### Return type

[**\OpenAPI\Client\Model\ProjectResponseTracking**](../Model/ProjectResponseTracking.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `projectAdminIdSettingsTrackingPatch()`

```php
projectAdminIdSettingsTrackingPatch($id, $session, $request): \OpenAPI\Client\Model\ProjectResponseTracking
```

Update project tracking settings

This endpoint is for updating the tracking settings of an existing project. Projects with status to be `\"Copying\"` cannot be manipulated, status 409 Conflict will be returned.  _only accessible with permission_ : `\"ManageConfiguration\"`  _fully accessible with permission_ : `\"ManageConfiguration\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\ProjectAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Project ID
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\ProjectPatchRequestTracking(); // \OpenAPI\Client\Model\ProjectPatchRequestTracking | project tracking data to be updated

try {
    $result = $apiInstance->projectAdminIdSettingsTrackingPatch($id, $session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProjectAdminApi->projectAdminIdSettingsTrackingPatch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Project ID | |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\ProjectPatchRequestTracking**](../Model/ProjectPatchRequestTracking.md)| project tracking data to be updated | [optional] |

### Return type

[**\OpenAPI\Client\Model\ProjectResponseTracking**](../Model/ProjectResponseTracking.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `projectAdminPost()`

```php
projectAdminPost($session, $request): \OpenAPI\Client\Model\ProjectResponseAdmin
```

Create project

This endpoint is for creating a new project.  ___createAccesses.AppointmentConfig.any___: must be false; true currently not supported  ___createAccesses.Calendar.any___: must be false; true currently not supported  ___createAccesses.CalendarTemplate.any___: must be false; true currently not supported  ___createAccesses.ChatFeed.any___: must be false; true currently not supported  ___createAccesses.Directory.any___: must be false; true currently not supported  ___createAccesses.DirectoryTemplate.any___: must be false; true currently not supported  ___createAccesses.Group.any___: must be false; true currently not supported  ___createAccesses.Location.any___: must be false; true currently not supported  ___createAccesses.LocationMap.any___: must be false; true currently not supported  ___createAccesses.Media.any___: must be false; true currently not supported  ___createAccesses.MediaFolder.any___: must be false; true currently not supported  ___createAccesses.Menu.any___: must be false; true currently not supported  ___createAccesses.News.any___: must be false; true currently not supported  ___createAccesses.Notification.any___: must be false; true currently not supported  ___createAccesses.Page.any___: must be false; true currently not supported  ___createAccesses.Stream.any___: must be false; true currently not supported  ___newsletter___ : is nullable -> null if newsletter is disabled for this project.  _only accessible with permission_ : `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\ProjectAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\ProjectPostRequest(); // \OpenAPI\Client\Model\ProjectPostRequest | Project to create

try {
    $result = $apiInstance->projectAdminPost($session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProjectAdminApi->projectAdminPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\ProjectPostRequest**](../Model/ProjectPostRequest.md)| Project to create | |

### Return type

[**\OpenAPI\Client\Model\ProjectResponseAdmin**](../Model/ProjectResponseAdmin.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
