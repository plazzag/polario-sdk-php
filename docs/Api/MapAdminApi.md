# OpenAPI\Client\MapAdminApi



All URIs are relative to https://custom.polario.de/api, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**locationAdminMapIdAccessGet()**](MapAdminApi.md#locationAdminMapIdAccessGet) | **GET** /location/admin/map/{id}/access | Get map access configuration |
| [**locationAdminMapIdAccessPatch()**](MapAdminApi.md#locationAdminMapIdAccessPatch) | **PATCH** /location/admin/map/{id}/access | Update map access configuration |
| [**locationAdminMapIdDelete()**](MapAdminApi.md#locationAdminMapIdDelete) | **DELETE** /location/admin/map/{id} | Delete map |
| [**locationAdminMapIdGet()**](MapAdminApi.md#locationAdminMapIdGet) | **GET** /location/admin/map/{id} | Get map |
| [**locationAdminMapIdPatch()**](MapAdminApi.md#locationAdminMapIdPatch) | **PATCH** /location/admin/map/{id} | Update map |
| [**locationAdminMapPost()**](MapAdminApi.md#locationAdminMapPost) | **POST** /location/admin/map | Create map |
| [**locationAdminMapProjectIdGet()**](MapAdminApi.md#locationAdminMapProjectIdGet) | **GET** /location/admin/map/project/{id} | Get map list for project |


## `locationAdminMapIdAccessGet()`

```php
locationAdminMapIdAccessGet($id, $session): \OpenAPI\Client\Model\AuthorizationAccessResponse
```

Get map access configuration

This endpoint returns the access configuration for the requested location map.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\MapAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Map ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->locationAdminMapIdAccessGet($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MapAdminApi->locationAdminMapIdAccessGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Map ID | |
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

## `locationAdminMapIdAccessPatch()`

```php
locationAdminMapIdAccessPatch($id, $session, $request): \OpenAPI\Client\Model\ModelAccess
```

Update map access configuration

This endpoint updates the access configuration for the requested location map. Only the changes should be transmitted due this endpoint.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\MapAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Map ID
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\ModelAccess(); // \OpenAPI\Client\Model\ModelAccess | changed access rights

try {
    $result = $apiInstance->locationAdminMapIdAccessPatch($id, $session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MapAdminApi->locationAdminMapIdAccessPatch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Map ID | |
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

## `locationAdminMapIdDelete()`

```php
locationAdminMapIdDelete($id, $session): \OpenAPI\Client\Model\ModelSwagStatusOk
```

Delete map

This endpoint is for deleting a single location map.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\MapAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Map ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->locationAdminMapIdDelete($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MapAdminApi->locationAdminMapIdDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Map ID | |
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

## `locationAdminMapIdGet()`

```php
locationAdminMapIdGet($id, $session): \OpenAPI\Client\Model\LocationmapResponseAdmin
```

Get map

This endpoint returns a location map in administrative representation by given id.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\MapAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Map ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->locationAdminMapIdGet($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MapAdminApi->locationAdminMapIdGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Map ID | |
| **session** | **string**| JWT | |

### Return type

[**\OpenAPI\Client\Model\LocationmapResponseAdmin**](../Model/LocationmapResponseAdmin.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `locationAdminMapIdPatch()`

```php
locationAdminMapIdPatch($id, $session, $request): \OpenAPI\Client\Model\LocationmapResponseAdmin
```

Update map

This endpoint is for updating specific data of an existing location map.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\MapAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | nMap ID
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\LocationmapPatchRequest(); // \OpenAPI\Client\Model\LocationmapPatchRequest | map data to be updated

try {
    $result = $apiInstance->locationAdminMapIdPatch($id, $session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MapAdminApi->locationAdminMapIdPatch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| nMap ID | |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\LocationmapPatchRequest**](../Model/LocationmapPatchRequest.md)| map data to be updated | [optional] |

### Return type

[**\OpenAPI\Client\Model\LocationmapResponseAdmin**](../Model/LocationmapResponseAdmin.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `locationAdminMapPost()`

```php
locationAdminMapPost($session, $request): \OpenAPI\Client\Model\LocationmapResponseAdmin
```

Create map

This endpoint is for creating a new location map.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\MapAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\LocationmapRequestAdmin(); // \OpenAPI\Client\Model\LocationmapRequestAdmin | Map to create

try {
    $result = $apiInstance->locationAdminMapPost($session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MapAdminApi->locationAdminMapPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\LocationmapRequestAdmin**](../Model/LocationmapRequestAdmin.md)| Map to create | |

### Return type

[**\OpenAPI\Client\Model\LocationmapResponseAdmin**](../Model/LocationmapResponseAdmin.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `locationAdminMapProjectIdGet()`

```php
locationAdminMapProjectIdGet($id, $session, $cursor, $limit, $page): \OpenAPI\Client\Model\LocationmapResponseListAdmin[]
```

Get map list for project

This endpoint returns a list of all location maps for the requested project. If a limit is set, a cursor for this endpoint may be created to iterate over all maps.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\MapAdminApi(
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
    $result = $apiInstance->locationAdminMapProjectIdGet($id, $session, $cursor, $limit, $page);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MapAdminApi->locationAdminMapProjectIdGet: ', $e->getMessage(), PHP_EOL;
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

[**\OpenAPI\Client\Model\LocationmapResponseListAdmin[]**](../Model/LocationmapResponseListAdmin.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
