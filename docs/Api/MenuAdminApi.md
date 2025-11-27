# OpenAPI\Client\MenuAdminApi



All URIs are relative to https://custom.polario.de/api, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**menuAdminProjectIdAccessGet()**](MenuAdminApi.md#menuAdminProjectIdAccessGet) | **GET** /menu/admin/project/{id}/access | Get menu access configuration |
| [**menuAdminProjectIdAccessPatch()**](MenuAdminApi.md#menuAdminProjectIdAccessPatch) | **PATCH** /menu/admin/project/{id}/access | Update menu access configuration |
| [**menuAdminProjectIdContentGet()**](MenuAdminApi.md#menuAdminProjectIdContentGet) | **GET** /menu/admin/project/{id}/content | Get menu content |
| [**menuAdminProjectIdContentPut()**](MenuAdminApi.md#menuAdminProjectIdContentPut) | **PUT** /menu/admin/project/{id}/content | Update menu content |
| [**menuAdminProjectIdGet()**](MenuAdminApi.md#menuAdminProjectIdGet) | **GET** /menu/admin/project/{id} | Get menu for project |
| [**menuAdminProjectIdPost()**](MenuAdminApi.md#menuAdminProjectIdPost) | **POST** /menu/admin/project/{id} | Create menu for project |
| [**menuAdminProjectIdSettingsGet()**](MenuAdminApi.md#menuAdminProjectIdSettingsGet) | **GET** /menu/admin/project/{id}/settings | Get menu settings |
| [**menuAdminProjectIdSettingsPut()**](MenuAdminApi.md#menuAdminProjectIdSettingsPut) | **PUT** /menu/admin/project/{id}/settings | Update menu settings |


## `menuAdminProjectIdAccessGet()`

```php
menuAdminProjectIdAccessGet($id, $session): \OpenAPI\Client\Model\AuthorizationAccessResponse
```

Get menu access configuration

This endpoint returns the access configuration for the requested menu.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\MenuAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Menu ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->menuAdminProjectIdAccessGet($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MenuAdminApi->menuAdminProjectIdAccessGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Menu ID | |
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

## `menuAdminProjectIdAccessPatch()`

```php
menuAdminProjectIdAccessPatch($id, $session, $request): \OpenAPI\Client\Model\ModelAccess
```

Update menu access configuration

This endpoint updates the access configuration for the requested menu. Only the changes should be transmitted due this endpoint.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\MenuAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Menu ID
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\ModelAccess(); // \OpenAPI\Client\Model\ModelAccess | changed access rights

try {
    $result = $apiInstance->menuAdminProjectIdAccessPatch($id, $session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MenuAdminApi->menuAdminProjectIdAccessPatch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Menu ID | |
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

## `menuAdminProjectIdContentGet()`

```php
menuAdminProjectIdContentGet($id, $session): \OpenAPI\Client\Model\MenuSwagMenuItemAdmin[]
```

Get menu content

This endpoint returns the content of the menu for a specific project. The output is in administrative representation.  ___search.objectTypes___: enums limited to: `\"Calendar\"` `\"CalendarEntry\"` `\"ChatFeed\"` `\"Directory\"` `\"DirectoryContentRow\"` `\"Location\"` `\"LocationMap\"` `\"MediaAudio\"` `\"MediaDocument\"` `\"MediaFolder\"` `\"MediaIcon\"` `\"MediaImage\"` `\"MediaOther\"` `\"MediaVideo\"` `\"News\"` `\"Page\"` `\"Project\"` `\"Stream\"`  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\MenuAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Project ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->menuAdminProjectIdContentGet($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MenuAdminApi->menuAdminProjectIdContentGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Project ID | |
| **session** | **string**| JWT | |

### Return type

[**\OpenAPI\Client\Model\MenuSwagMenuItemAdmin[]**](../Model/MenuSwagMenuItemAdmin.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `menuAdminProjectIdContentPut()`

```php
menuAdminProjectIdContentPut($id, $session, $request): \OpenAPI\Client\Model\MenuSwagMenuItemAdmin[]
```

Update menu content

This endpoint updates the content of a menu and returns it.  ___search.objectTypes___: enums limited to: `\"Calendar\"` `\"CalendarEntry\"` `\"ChatFeed\"` `\"Directory\"` `\"DirectoryContentRow\"` `\"Location\"` `\"LocationMap\"` `\"MediaAudio\"` `\"MediaDocument\"` `\"MediaFolder\"` `\"MediaIcon\"` `\"MediaImage\"` `\"MediaOther\"` `\"MediaVideo\"` `\"News\"` `\"Page\"` `\"Project\"` `\"Stream\"`  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\MenuAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Project ID
$session = 'session_example'; // string | JWT
$request = array(new \OpenAPI\Client\Model\MenuRequestItem()); // \OpenAPI\Client\Model\MenuRequestItem[] | the content of the menu

try {
    $result = $apiInstance->menuAdminProjectIdContentPut($id, $session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MenuAdminApi->menuAdminProjectIdContentPut: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Project ID | |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\MenuRequestItem[]**](../Model/MenuRequestItem.md)| the content of the menu | |

### Return type

[**\OpenAPI\Client\Model\MenuSwagMenuItemAdmin[]**](../Model/MenuSwagMenuItemAdmin.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `menuAdminProjectIdGet()`

```php
menuAdminProjectIdGet($id, $session): \OpenAPI\Client\Model\MenuAdminProjectIdGet200Response
```

Get menu for project

This endpoint returns the menu for a specific project. The output is in administrative representation.  ___content.search.objectTypes___: enums limited to: `\"Calendar\"` `\"CalendarEntry\"` `\"ChatFeed\"` `\"Directory\"` `\"DirectoryContentRow\"` `\"Location\"` `\"LocationMap\"` `\"MediaAudio\"` `\"MediaDocument\"` `\"MediaFolder\"` `\"MediaIcon\"` `\"MediaImage\"` `\"MediaOther\"` `\"MediaVideo\"` `\"News\"` `\"Page\"` `\"Project\"` `\"Stream\"`  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\MenuAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Project ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->menuAdminProjectIdGet($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MenuAdminApi->menuAdminProjectIdGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Project ID | |
| **session** | **string**| JWT | |

### Return type

[**\OpenAPI\Client\Model\MenuAdminProjectIdGet200Response**](../Model/MenuAdminProjectIdGet200Response.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `menuAdminProjectIdPost()`

```php
menuAdminProjectIdPost($id, $session, $request): \OpenAPI\Client\Model\MenuAdminProjectIdGet200Response
```

Create menu for project

This endpoint is for creating a new menu for a specific project. In case of response status is 409 the menu already exist.  ___content.search.objectTypes___: enums limited to: `\"Calendar\"` `\"CalendarEntry\"` `\"ChatFeed\"` `\"Directory\"` `\"DirectoryContentRow\"` `\"Location\"` `\"LocationMap\"` `\"MediaAudio\"` `\"MediaDocument\"` `\"MediaFolder\"` `\"MediaIcon\"` `\"MediaImage\"` `\"MediaOther\"` `\"MediaVideo\"` `\"News\"` `\"Page\"` `\"Project\"` `\"Stream\"`  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\MenuAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Project ID
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\MenuRequest(); // \OpenAPI\Client\Model\MenuRequest | the settings and content of the menu

try {
    $result = $apiInstance->menuAdminProjectIdPost($id, $session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MenuAdminApi->menuAdminProjectIdPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Project ID | |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\MenuRequest**](../Model/MenuRequest.md)| the settings and content of the menu | |

### Return type

[**\OpenAPI\Client\Model\MenuAdminProjectIdGet200Response**](../Model/MenuAdminProjectIdGet200Response.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `menuAdminProjectIdSettingsGet()`

```php
menuAdminProjectIdSettingsGet($id, $session): \OpenAPI\Client\Model\MenuResponseSettingsAdmin
```

Get menu settings

This endpoint returns the settings of the menu for a specific project. The output is in administrative representation.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\MenuAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Project ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->menuAdminProjectIdSettingsGet($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MenuAdminApi->menuAdminProjectIdSettingsGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Project ID | |
| **session** | **string**| JWT | |

### Return type

[**\OpenAPI\Client\Model\MenuResponseSettingsAdmin**](../Model/MenuResponseSettingsAdmin.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `menuAdminProjectIdSettingsPut()`

```php
menuAdminProjectIdSettingsPut($id, $session, $request): \OpenAPI\Client\Model\MenuResponseSettingsAdmin[]
```

Update menu settings

This endpoint updates the settings of a menu and returns it.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\MenuAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Project ID
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\MenuRequestSettings(); // \OpenAPI\Client\Model\MenuRequestSettings | the settings of the menu

try {
    $result = $apiInstance->menuAdminProjectIdSettingsPut($id, $session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MenuAdminApi->menuAdminProjectIdSettingsPut: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Project ID | |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\MenuRequestSettings**](../Model/MenuRequestSettings.md)| the settings of the menu | |

### Return type

[**\OpenAPI\Client\Model\MenuResponseSettingsAdmin[]**](../Model/MenuResponseSettingsAdmin.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
