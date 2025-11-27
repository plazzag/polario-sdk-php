# OpenAPI\Client\PageAdminApi



All URIs are relative to https://custom.polario.de/api, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**pageAdminIdAccessGet()**](PageAdminApi.md#pageAdminIdAccessGet) | **GET** /page/admin/{id}/access | Get page access configuration |
| [**pageAdminIdAccessPatch()**](PageAdminApi.md#pageAdminIdAccessPatch) | **PATCH** /page/admin/{id}/access | Update page access configuration |
| [**pageAdminIdContentDesktopDelete()**](PageAdminApi.md#pageAdminIdContentDesktopDelete) | **DELETE** /page/admin/{id}/content/desktop | Delete desktop content |
| [**pageAdminIdContentDesktopGet()**](PageAdminApi.md#pageAdminIdContentDesktopGet) | **GET** /page/admin/{id}/content/desktop | Get page desktop content |
| [**pageAdminIdContentDesktopPut()**](PageAdminApi.md#pageAdminIdContentDesktopPut) | **PUT** /page/admin/{id}/content/desktop | Update page desktop content |
| [**pageAdminIdContentGet()**](PageAdminApi.md#pageAdminIdContentGet) | **GET** /page/admin/{id}/content | Get page mobile content |
| [**pageAdminIdContentPut()**](PageAdminApi.md#pageAdminIdContentPut) | **PUT** /page/admin/{id}/content | Update page mobile content |
| [**pageAdminIdDelete()**](PageAdminApi.md#pageAdminIdDelete) | **DELETE** /page/admin/{id} | Delete page |
| [**pageAdminIdDesktopGet()**](PageAdminApi.md#pageAdminIdDesktopGet) | **GET** /page/admin/{id}/desktop | Get page desktop content |
| [**pageAdminIdGet()**](PageAdminApi.md#pageAdminIdGet) | **GET** /page/admin/{id} | Get page |
| [**pageAdminIdPatch()**](PageAdminApi.md#pageAdminIdPatch) | **PATCH** /page/admin/{id} | Update page |
| [**pageAdminIdSettingsGet()**](PageAdminApi.md#pageAdminIdSettingsGet) | **GET** /page/admin/{id}/settings | Get page settings |
| [**pageAdminIdSettingsPut()**](PageAdminApi.md#pageAdminIdSettingsPut) | **PUT** /page/admin/{id}/settings | Update page settings |
| [**pageAdminPost()**](PageAdminApi.md#pageAdminPost) | **POST** /page/admin | Create page |
| [**pageAdminPostCountProjectIdGet()**](PageAdminApi.md#pageAdminPostCountProjectIdGet) | **GET** /page/admin/post-count/project/{id} | Get page post counts for project |
| [**pageAdminProjectIdGet()**](PageAdminApi.md#pageAdminProjectIdGet) | **GET** /page/admin/project/{id} | Get page list for project |
| [**pageAdminSyncPut()**](PageAdminApi.md#pageAdminSyncPut) | **PUT** /page/admin/sync | Sync Operators for all pages |


## `pageAdminIdAccessGet()`

```php
pageAdminIdAccessGet($id, $session): \OpenAPI\Client\Model\AuthorizationAccessResponse
```

Get page access configuration

This endpoint returns the access configuration for the requested page.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\PageAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Page ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->pageAdminIdAccessGet($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PageAdminApi->pageAdminIdAccessGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Page ID | |
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

## `pageAdminIdAccessPatch()`

```php
pageAdminIdAccessPatch($id, $session, $request): \OpenAPI\Client\Model\ModelAccess
```

Update page access configuration

This endpoint updates the access configuration for the requested page. Only the changes should be transmitted due this endpoint.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\PageAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Page ID
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\ModelAccess(); // \OpenAPI\Client\Model\ModelAccess | changed access rights

try {
    $result = $apiInstance->pageAdminIdAccessPatch($id, $session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PageAdminApi->pageAdminIdAccessPatch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Page ID | |
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

## `pageAdminIdContentDesktopDelete()`

```php
pageAdminIdContentDesktopDelete($id, $session): \OpenAPI\Client\Model\ModelSwagStatusOk
```

Delete desktop content

This endpoint will delete the desktop version of a page, but not the page itself. The mobile version will still exist.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\PageAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Page ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->pageAdminIdContentDesktopDelete($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PageAdminApi->pageAdminIdContentDesktopDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Page ID | |
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

## `pageAdminIdContentDesktopGet()`

```php
pageAdminIdContentDesktopGet($id, $session): \OpenAPI\Client\Model\PageAdminIdContentGet200ResponseInner[]
```

Get page desktop content

This endpoint returns the localized mobile content of a specific page in administrative representation by given id.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\PageAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Page ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->pageAdminIdContentDesktopGet($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PageAdminApi->pageAdminIdContentDesktopGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Page ID | |
| **session** | **string**| JWT | |

### Return type

[**\OpenAPI\Client\Model\PageAdminIdContentGet200ResponseInner[]**](../Model/PageAdminIdContentGet200ResponseInner.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `pageAdminIdContentDesktopPut()`

```php
pageAdminIdContentDesktopPut($id, $session, $request): \OpenAPI\Client\Model\PageAdminIdContentGet200ResponseInner[]
```

Update page desktop content

This endpoint is for creating or updating the desktop content of an existing page.  For storing mobile version use: PUT /page/admin/{id}/content  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\PageAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Page ID
$session = 'session_example'; // string | JWT
$request = array(new \OpenAPI\Client\Model\PageRequestSection()); // \OpenAPI\Client\Model\PageRequestSection[] | desktop page content to update

try {
    $result = $apiInstance->pageAdminIdContentDesktopPut($id, $session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PageAdminApi->pageAdminIdContentDesktopPut: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Page ID | |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\PageRequestSection[]**](../Model/PageRequestSection.md)| desktop page content to update | |

### Return type

[**\OpenAPI\Client\Model\PageAdminIdContentGet200ResponseInner[]**](../Model/PageAdminIdContentGet200ResponseInner.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `pageAdminIdContentGet()`

```php
pageAdminIdContentGet($id, $session): \OpenAPI\Client\Model\PageAdminIdContentGet200ResponseInner[]
```

Get page mobile content

This endpoint returns the localized mobile content of a specific page in administrative representation by given id.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\PageAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Page ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->pageAdminIdContentGet($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PageAdminApi->pageAdminIdContentGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Page ID | |
| **session** | **string**| JWT | |

### Return type

[**\OpenAPI\Client\Model\PageAdminIdContentGet200ResponseInner[]**](../Model/PageAdminIdContentGet200ResponseInner.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `pageAdminIdContentPut()`

```php
pageAdminIdContentPut($id, $session, $request): \OpenAPI\Client\Model\PageAdminIdContentGet200ResponseInner[]
```

Update page mobile content

This endpoint is for updating the mobile content of an existing page.  For storing desktop version use: PUT /page/admin/{id}/content/desktop  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\PageAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Page ID
$session = 'session_example'; // string | JWT
$request = array(new \OpenAPI\Client\Model\PageRequestSection()); // \OpenAPI\Client\Model\PageRequestSection[] | standard page content to update

try {
    $result = $apiInstance->pageAdminIdContentPut($id, $session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PageAdminApi->pageAdminIdContentPut: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Page ID | |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\PageRequestSection[]**](../Model/PageRequestSection.md)| standard page content to update | |

### Return type

[**\OpenAPI\Client\Model\PageAdminIdContentGet200ResponseInner[]**](../Model/PageAdminIdContentGet200ResponseInner.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `pageAdminIdDelete()`

```php
pageAdminIdDelete($id, $session): \OpenAPI\Client\Model\ModelSwagStatusOk
```

Delete page

This endpoint is for deleting a single page with all localizations.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\PageAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Page ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->pageAdminIdDelete($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PageAdminApi->pageAdminIdDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Page ID | |
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

## `pageAdminIdDesktopGet()`

```php
pageAdminIdDesktopGet($id, $session): \OpenAPI\Client\Model\PageAdminPost200Response
```

Get page desktop content

This endpoint returns the localized desktop version of page if it exists in admin representation by given id. If the requested language is not available it will fall back to the default language.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\PageAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Page ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->pageAdminIdDesktopGet($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PageAdminApi->pageAdminIdDesktopGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Page ID | |
| **session** | **string**| JWT | |

### Return type

[**\OpenAPI\Client\Model\PageAdminPost200Response**](../Model/PageAdminPost200Response.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `pageAdminIdGet()`

```php
pageAdminIdGet($id, $session): \OpenAPI\Client\Model\PageAdminPost200Response
```

Get page

This endpoint returns a localized page in administrative representation by given id.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\PageAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Page ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->pageAdminIdGet($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PageAdminApi->pageAdminIdGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Page ID | |
| **session** | **string**| JWT | |

### Return type

[**\OpenAPI\Client\Model\PageAdminPost200Response**](../Model/PageAdminPost200Response.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `pageAdminIdPatch()`

```php
pageAdminIdPatch($id, $session, $request): \OpenAPI\Client\Model\PageAdminPost200Response
```

Update page

This endpoint is for updating the page besides content and settings.  For storing content or settings use: PUT /page/admin/{id}/content AND PUT /page/admin/{id}/settings  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\PageAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Page ID
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\PagePatchRequest(); // \OpenAPI\Client\Model\PagePatchRequest | page data to update

try {
    $result = $apiInstance->pageAdminIdPatch($id, $session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PageAdminApi->pageAdminIdPatch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Page ID | |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\PagePatchRequest**](../Model/PagePatchRequest.md)| page data to update | |

### Return type

[**\OpenAPI\Client\Model\PageAdminPost200Response**](../Model/PageAdminPost200Response.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `pageAdminIdSettingsGet()`

```php
pageAdminIdSettingsGet($id, $session): \OpenAPI\Client\Model\ModelPageSettings
```

Get page settings

This endpoint returns the settings of a specific page in administrative representation by given id.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\PageAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Page ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->pageAdminIdSettingsGet($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PageAdminApi->pageAdminIdSettingsGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Page ID | |
| **session** | **string**| JWT | |

### Return type

[**\OpenAPI\Client\Model\ModelPageSettings**](../Model/ModelPageSettings.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `pageAdminIdSettingsPut()`

```php
pageAdminIdSettingsPut($id, $session, $request): \OpenAPI\Client\Model\ModelPageSettings[]
```

Update page settings

This endpoint updates the settings of a specific page returns it.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\PageAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Page ID
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\ModelPageSettings(); // \OpenAPI\Client\Model\ModelPageSettings | the settings of the page

try {
    $result = $apiInstance->pageAdminIdSettingsPut($id, $session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PageAdminApi->pageAdminIdSettingsPut: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Page ID | |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\ModelPageSettings**](../Model/ModelPageSettings.md)| the settings of the page | |

### Return type

[**\OpenAPI\Client\Model\ModelPageSettings[]**](../Model/ModelPageSettings.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `pageAdminPost()`

```php
pageAdminPost($session, $request): \OpenAPI\Client\Model\PageAdminPost200Response
```

Create page

This endpoint is for creating a new page. The page will be saves as standard (mobile) version.  For storing desktop version use: PUT /page/admin/{id}/content/desktop  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\PageAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\PageRequest(); // \OpenAPI\Client\Model\PageRequest | standard page to create

try {
    $result = $apiInstance->pageAdminPost($session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PageAdminApi->pageAdminPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\PageRequest**](../Model/PageRequest.md)| standard page to create | |

### Return type

[**\OpenAPI\Client\Model\PageAdminPost200Response**](../Model/PageAdminPost200Response.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `pageAdminPostCountProjectIdGet()`

```php
pageAdminPostCountProjectIdGet($id, $session, $cursor, $limit, $page): \OpenAPI\Client\Model\PagePostCountResponse[]
```

Get page post counts for project

This endpoint returns a list of post counts for all pages with social interaction activated of the requested project. If a limit is set, a cursor for this endpoint may be created to iterate over all post counts.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\PageAdminApi(
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
    $result = $apiInstance->pageAdminPostCountProjectIdGet($id, $session, $cursor, $limit, $page);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PageAdminApi->pageAdminPostCountProjectIdGet: ', $e->getMessage(), PHP_EOL;
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

[**\OpenAPI\Client\Model\PagePostCountResponse[]**](../Model/PagePostCountResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `pageAdminProjectIdGet()`

```php
pageAdminProjectIdGet($id, $session, $cursor, $limit, $page): \OpenAPI\Client\Model\PageResponseListAdmin[]
```

Get page list for project

This endpoint returns a list of all pages for the requested project without content in administrative representation. If a limit is set, a cursor for this endpoint may be created to iterate over all pages.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\PageAdminApi(
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
    $result = $apiInstance->pageAdminProjectIdGet($id, $session, $cursor, $limit, $page);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PageAdminApi->pageAdminProjectIdGet: ', $e->getMessage(), PHP_EOL;
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

[**\OpenAPI\Client\Model\PageResponseListAdmin[]**](../Model/PageResponseListAdmin.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `pageAdminSyncPut()`

```php
pageAdminSyncPut($session): \OpenAPI\Client\Model\ModelSwagStatusOk
```

Sync Operators for all pages

This endpoint is sync operators for all pages with sendbird. This endpoint should be rarely used, because of its workload.  _only accessible with permission_ : `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\PageAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->pageAdminSyncPut($session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PageAdminApi->pageAdminSyncPut: ', $e->getMessage(), PHP_EOL;
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
