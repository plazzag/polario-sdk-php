# OpenAPI\Client\NewsAdminApi



All URIs are relative to https://custom.polario.de/api, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**newsAdminGet()**](NewsAdminApi.md#newsAdminGet) | **GET** /news/admin | Get article list for cursor |
| [**newsAdminIdAccessGet()**](NewsAdminApi.md#newsAdminIdAccessGet) | **GET** /news/admin/{id}/access | Get article access configuration |
| [**newsAdminIdAccessPatch()**](NewsAdminApi.md#newsAdminIdAccessPatch) | **PATCH** /news/admin/{id}/access | Update article access configuration |
| [**newsAdminIdContentDesktopDelete()**](NewsAdminApi.md#newsAdminIdContentDesktopDelete) | **DELETE** /news/admin/{id}/content/desktop | Delete article desktop version |
| [**newsAdminIdContentDesktopGet()**](NewsAdminApi.md#newsAdminIdContentDesktopGet) | **GET** /news/admin/{id}/content/desktop | Get article desktop content |
| [**newsAdminIdContentDesktopPut()**](NewsAdminApi.md#newsAdminIdContentDesktopPut) | **PUT** /news/admin/{id}/content/desktop | Update article desktop content |
| [**newsAdminIdContentGet()**](NewsAdminApi.md#newsAdminIdContentGet) | **GET** /news/admin/{id}/content | Get article mobile content |
| [**newsAdminIdContentPut()**](NewsAdminApi.md#newsAdminIdContentPut) | **PUT** /news/admin/{id}/content | Update article mobile content |
| [**newsAdminIdDelete()**](NewsAdminApi.md#newsAdminIdDelete) | **DELETE** /news/admin/{id} | Delete article |
| [**newsAdminIdGet()**](NewsAdminApi.md#newsAdminIdGet) | **GET** /news/admin/{id} | Get article mobile |
| [**newsAdminIdPatch()**](NewsAdminApi.md#newsAdminIdPatch) | **PATCH** /news/admin/{id} | Update article info |
| [**newsAdminIdSettingsGet()**](NewsAdminApi.md#newsAdminIdSettingsGet) | **GET** /news/admin/{id}/settings | Get article settings |
| [**newsAdminIdSettingsPut()**](NewsAdminApi.md#newsAdminIdSettingsPut) | **PUT** /news/admin/{id}/settings | Update article settings |
| [**newsAdminPost()**](NewsAdminApi.md#newsAdminPost) | **POST** /news/admin | Create article |
| [**newsAdminPostCountProjectIdGet()**](NewsAdminApi.md#newsAdminPostCountProjectIdGet) | **GET** /news/admin/post-count/project/{id} | Get article post counts for project |
| [**newsAdminProjectIdGet()**](NewsAdminApi.md#newsAdminProjectIdGet) | **GET** /news/admin/project/{id} | Get article list for project |
| [**newsAdminSearchPost()**](NewsAdminApi.md#newsAdminSearchPost) | **POST** /news/admin/search | Create cursor |
| [**newsAdminSyncPut()**](NewsAdminApi.md#newsAdminSyncPut) | **PUT** /news/admin/sync | Sync Operators for all articles |


## `newsAdminGet()`

```php
newsAdminGet($cursor, $page, $session, $limit): \OpenAPI\Client\Model\NewsArticleResponseListAdmin[]
```

Get article list for cursor

This endpoint returns a list of all articles for a cursor without content in administrative representation.  Cursor could be created here: POST /news/admin/search  _accessible without permission_

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\NewsAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$cursor = 'cursor_example'; // string | id of the cursor used for pagination; required if page is set
$page = 56; // int | current page index of the cursor used for pagination; required if cursor is set
$session = 'session_example'; // string | JWT
$limit = 56; // int | amount of results per page (1 ... 100)

try {
    $result = $apiInstance->newsAdminGet($cursor, $page, $session, $limit);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NewsAdminApi->newsAdminGet: ', $e->getMessage(), PHP_EOL;
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

[**\OpenAPI\Client\Model\NewsArticleResponseListAdmin[]**](../Model/NewsArticleResponseListAdmin.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `newsAdminIdAccessGet()`

```php
newsAdminIdAccessGet($id, $session): \OpenAPI\Client\Model\AuthorizationAccessResponse
```

Get article access configuration

This endpoint returns the access configuration for the requested article.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\NewsAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Article ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->newsAdminIdAccessGet($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NewsAdminApi->newsAdminIdAccessGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Article ID | |
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

## `newsAdminIdAccessPatch()`

```php
newsAdminIdAccessPatch($id, $session, $request): \OpenAPI\Client\Model\ModelAccess
```

Update article access configuration

This endpoint updates the access configuration for the requested article. Only the changes should be transmitted due this endpoint.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\NewsAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Article ID
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\ModelAccess(); // \OpenAPI\Client\Model\ModelAccess | changed access rights

try {
    $result = $apiInstance->newsAdminIdAccessPatch($id, $session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NewsAdminApi->newsAdminIdAccessPatch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Article ID | |
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

## `newsAdminIdContentDesktopDelete()`

```php
newsAdminIdContentDesktopDelete($id, $session): \OpenAPI\Client\Model\ModelSwagStatusOk
```

Delete article desktop version

This endpoint will delete the desktop version of an article, but not the article itself. The Mobile Version will still exist.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\NewsAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Article ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->newsAdminIdContentDesktopDelete($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NewsAdminApi->newsAdminIdContentDesktopDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Article ID | |
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

## `newsAdminIdContentDesktopGet()`

```php
newsAdminIdContentDesktopGet($id, $session): \OpenAPI\Client\Model\NewsAdminIdContentGet200ResponseInner[]
```

Get article desktop content

This endpoint returns the localized desktop content of a specific article in administrative representation by given id.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\NewsAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Article ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->newsAdminIdContentDesktopGet($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NewsAdminApi->newsAdminIdContentDesktopGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Article ID | |
| **session** | **string**| JWT | |

### Return type

[**\OpenAPI\Client\Model\NewsAdminIdContentGet200ResponseInner[]**](../Model/NewsAdminIdContentGet200ResponseInner.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `newsAdminIdContentDesktopPut()`

```php
newsAdminIdContentDesktopPut($id, $session, $request): \OpenAPI\Client\Model\NewsAdminIdContentGet200ResponseInner[]
```

Update article desktop content

This endpoint is for creating or updating the desktop content of an existing article.  For storing mobile version use: PUT /news/admin/{id}/content  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\NewsAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Article ID
$session = 'session_example'; // string | JWT
$request = array(new \OpenAPI\Client\Model\NewsRequestSection()); // \OpenAPI\Client\Model\NewsRequestSection[] | desktop article content to update

try {
    $result = $apiInstance->newsAdminIdContentDesktopPut($id, $session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NewsAdminApi->newsAdminIdContentDesktopPut: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Article ID | |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\NewsRequestSection[]**](../Model/NewsRequestSection.md)| desktop article content to update | |

### Return type

[**\OpenAPI\Client\Model\NewsAdminIdContentGet200ResponseInner[]**](../Model/NewsAdminIdContentGet200ResponseInner.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `newsAdminIdContentGet()`

```php
newsAdminIdContentGet($id, $session): \OpenAPI\Client\Model\NewsAdminIdContentGet200ResponseInner[]
```

Get article mobile content

This endpoint returns the localized mobile content of a specific article in administrative representation by given id.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\NewsAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Article ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->newsAdminIdContentGet($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NewsAdminApi->newsAdminIdContentGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Article ID | |
| **session** | **string**| JWT | |

### Return type

[**\OpenAPI\Client\Model\NewsAdminIdContentGet200ResponseInner[]**](../Model/NewsAdminIdContentGet200ResponseInner.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `newsAdminIdContentPut()`

```php
newsAdminIdContentPut($id, $session, $request): \OpenAPI\Client\Model\NewsAdminIdContentGet200ResponseInner[]
```

Update article mobile content

This endpoint is for updating the mobile content of an existing article.  For storing desktop version use: PUT /news/admin/{id}/content/desktop  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\NewsAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Article ID
$session = 'session_example'; // string | JWT
$request = array(new \OpenAPI\Client\Model\NewsRequestSection()); // \OpenAPI\Client\Model\NewsRequestSection[] | standard article content to update

try {
    $result = $apiInstance->newsAdminIdContentPut($id, $session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NewsAdminApi->newsAdminIdContentPut: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Article ID | |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\NewsRequestSection[]**](../Model/NewsRequestSection.md)| standard article content to update | |

### Return type

[**\OpenAPI\Client\Model\NewsAdminIdContentGet200ResponseInner[]**](../Model/NewsAdminIdContentGet200ResponseInner.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `newsAdminIdDelete()`

```php
newsAdminIdDelete($id, $session): \OpenAPI\Client\Model\ModelSwagStatusOk
```

Delete article

This endpoint is for deleting a single article with all localizations.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\NewsAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Article ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->newsAdminIdDelete($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NewsAdminApi->newsAdminIdDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Article ID | |
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

## `newsAdminIdGet()`

```php
newsAdminIdGet($id, $session): \OpenAPI\Client\Model\NewsAdminPost200Response
```

Get article mobile

This endpoint returns a localized article in admin representation by given id.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\NewsAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Article ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->newsAdminIdGet($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NewsAdminApi->newsAdminIdGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Article ID | |
| **session** | **string**| JWT | |

### Return type

[**\OpenAPI\Client\Model\NewsAdminPost200Response**](../Model/NewsAdminPost200Response.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `newsAdminIdPatch()`

```php
newsAdminIdPatch($id, $session, $request): \OpenAPI\Client\Model\NewsAdminPost200Response
```

Update article info

This endpoint is for updating an article besides content and settings.  For storing content or settings use: PUT /news/admin/{id}/content AND PUT /news/admin/{id}/settings  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\NewsAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Article ID
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\NewsArticlePatchRequest(); // \OpenAPI\Client\Model\NewsArticlePatchRequest | article data to update

try {
    $result = $apiInstance->newsAdminIdPatch($id, $session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NewsAdminApi->newsAdminIdPatch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Article ID | |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\NewsArticlePatchRequest**](../Model/NewsArticlePatchRequest.md)| article data to update | |

### Return type

[**\OpenAPI\Client\Model\NewsAdminPost200Response**](../Model/NewsAdminPost200Response.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `newsAdminIdSettingsGet()`

```php
newsAdminIdSettingsGet($id, $session): \OpenAPI\Client\Model\ModelArticleSettings
```

Get article settings

This endpoint returns the settings of a specific article in administrative representation by given id.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\NewsAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Article ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->newsAdminIdSettingsGet($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NewsAdminApi->newsAdminIdSettingsGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Article ID | |
| **session** | **string**| JWT | |

### Return type

[**\OpenAPI\Client\Model\ModelArticleSettings**](../Model/ModelArticleSettings.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `newsAdminIdSettingsPut()`

```php
newsAdminIdSettingsPut($id, $session, $request): \OpenAPI\Client\Model\ModelArticleSettings
```

Update article settings

This endpoint updates the settings of a specific article and returns it.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\NewsAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Article ID
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\ModelArticleSettings(); // \OpenAPI\Client\Model\ModelArticleSettings | the settings of the article

try {
    $result = $apiInstance->newsAdminIdSettingsPut($id, $session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NewsAdminApi->newsAdminIdSettingsPut: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Article ID | |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\ModelArticleSettings**](../Model/ModelArticleSettings.md)| the settings of the article | |

### Return type

[**\OpenAPI\Client\Model\ModelArticleSettings**](../Model/ModelArticleSettings.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `newsAdminPost()`

```php
newsAdminPost($session, $request): \OpenAPI\Client\Model\NewsAdminPost200Response
```

Create article

This endpoint is for creating a new article. The article will be saves as standard (mobile) version.  For storing desktop version use: PUT /news/admin/{id}/content/desktop  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\NewsAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\NewsArticleRequest(); // \OpenAPI\Client\Model\NewsArticleRequest | standard article to create

try {
    $result = $apiInstance->newsAdminPost($session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NewsAdminApi->newsAdminPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\NewsArticleRequest**](../Model/NewsArticleRequest.md)| standard article to create | |

### Return type

[**\OpenAPI\Client\Model\NewsAdminPost200Response**](../Model/NewsAdminPost200Response.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `newsAdminPostCountProjectIdGet()`

```php
newsAdminPostCountProjectIdGet($id, $session, $cursor, $limit, $page): \OpenAPI\Client\Model\NewsArticlePostCountResponse[]
```

Get article post counts for project

This endpoint returns a list of post counts for all articles with social interaction activated of the requested project. If a limit is set, a cursor for this endpoint may be created to iterate over all article post counts.  _only accessible with permission_ : `\"ManageContent\" (counts also for linked projects)` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\" (counts also for linked projects)` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\NewsAdminApi(
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
    $result = $apiInstance->newsAdminPostCountProjectIdGet($id, $session, $cursor, $limit, $page);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NewsAdminApi->newsAdminPostCountProjectIdGet: ', $e->getMessage(), PHP_EOL;
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

[**\OpenAPI\Client\Model\NewsArticlePostCountResponse[]**](../Model/NewsArticlePostCountResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `newsAdminProjectIdGet()`

```php
newsAdminProjectIdGet($id, $session, $cursor, $limit, $page): \OpenAPI\Client\Model\NewsArticleResponseListAdmin[]
```

Get article list for project

This endpoint returns a list of all articles for the requested project without content in administrative representation. The entries are sorted by `publishedAt:DESC`. If a limit is set, a cursor for this endpoint may be created to iterate over all articles.  _only accessible with permission_ : `\"ManageContent\" (counts also for linked projects)` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\" (counts also for linked projects)` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\NewsAdminApi(
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
    $result = $apiInstance->newsAdminProjectIdGet($id, $session, $cursor, $limit, $page);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NewsAdminApi->newsAdminProjectIdGet: ', $e->getMessage(), PHP_EOL;
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

[**\OpenAPI\Client\Model\NewsArticleResponseListAdmin[]**](../Model/NewsArticleResponseListAdmin.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `newsAdminSearchPost()`

```php
newsAdminSearchPost($session, $request): \OpenAPI\Client\Model\ModelCursorResponse
```

Create cursor

This endpoint returns a cursor for list articles in admin representation with applied filter and sort options. In case of cursor response total will be 0 the status 204 with not content is returned instead.  _only accessible with permission_ : `\"ManageContent\" (counts also for linked projects)` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\" (counts also for linked projects)` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\NewsAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\NewsCursorRequestAdmin(); // \OpenAPI\Client\Model\NewsCursorRequestAdmin | options to create cursor

try {
    $result = $apiInstance->newsAdminSearchPost($session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NewsAdminApi->newsAdminSearchPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\NewsCursorRequestAdmin**](../Model/NewsCursorRequestAdmin.md)| options to create cursor | |

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

## `newsAdminSyncPut()`

```php
newsAdminSyncPut($session): \OpenAPI\Client\Model\ModelSwagStatusOk
```

Sync Operators for all articles

This endpoint is sync operators for all articles with sendbird. This endpoint should be rarely used, because of its workload. User must be Owner to call this endpoint.  _only accessible with permission_ : `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\NewsAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->newsAdminSyncPut($session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NewsAdminApi->newsAdminSyncPut: ', $e->getMessage(), PHP_EOL;
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
