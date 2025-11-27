# OpenAPI\Client\DirectoryAdminApi



All URIs are relative to https://custom.polario.de/api, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**directoryAdminGet()**](DirectoryAdminApi.md#directoryAdminGet) | **GET** /directory/admin | Get directory list for cursor |
| [**directoryAdminIdContentGet()**](DirectoryAdminApi.md#directoryAdminIdContentGet) | **GET** /directory/admin/{id}/content | Get directory content rows list |
| [**directoryAdminIdContentPost()**](DirectoryAdminApi.md#directoryAdminIdContentPost) | **POST** /directory/admin/{id}/content | Add directory content rows |
| [**directoryAdminIdCopyPost()**](DirectoryAdminApi.md#directoryAdminIdCopyPost) | **POST** /directory/admin/{id}/copy | Copy directory |
| [**directoryAdminIdDelete()**](DirectoryAdminApi.md#directoryAdminIdDelete) | **DELETE** /directory/admin/{id} | Delete directory |
| [**directoryAdminIdDetailGet()**](DirectoryAdminApi.md#directoryAdminIdDetailGet) | **GET** /directory/admin/{id}/detail | Get directory detail view |
| [**directoryAdminIdDetailPut()**](DirectoryAdminApi.md#directoryAdminIdDetailPut) | **PUT** /directory/admin/{id}/detail | Update directory detail view |
| [**directoryAdminIdGet()**](DirectoryAdminApi.md#directoryAdminIdGet) | **GET** /directory/admin/{id} | Get directory |
| [**directoryAdminIdItemsGet()**](DirectoryAdminApi.md#directoryAdminIdItemsGet) | **GET** /directory/admin/{id}/items | Get directory detail view items |
| [**directoryAdminIdListSettingsGet()**](DirectoryAdminApi.md#directoryAdminIdListSettingsGet) | **GET** /directory/admin/{id}/list-settings | Get directory list settings |
| [**directoryAdminIdListSettingsPut()**](DirectoryAdminApi.md#directoryAdminIdListSettingsPut) | **PUT** /directory/admin/{id}/list-settings | Update directory list settings |
| [**directoryAdminIdPatch()**](DirectoryAdminApi.md#directoryAdminIdPatch) | **PATCH** /directory/admin/{id} | Update directory info |
| [**directoryAdminIdSelectionsGet()**](DirectoryAdminApi.md#directoryAdminIdSelectionsGet) | **GET** /directory/admin/{id}/selections | Get directory detail view selections |
| [**directoryAdminPost()**](DirectoryAdminApi.md#directoryAdminPost) | **POST** /directory/admin | Create directory |
| [**directoryAdminProjectIdGet()**](DirectoryAdminApi.md#directoryAdminProjectIdGet) | **GET** /directory/admin/project/{id} | Get directory list for project |
| [**directoryAdminRowIdAccessGet()**](DirectoryAdminApi.md#directoryAdminRowIdAccessGet) | **GET** /directory/admin/row/{id}/access | Get directory row access configuration |
| [**directoryAdminRowIdAccessPatch()**](DirectoryAdminApi.md#directoryAdminRowIdAccessPatch) | **PATCH** /directory/admin/row/{id}/access | Update directory row access configuration |
| [**directoryAdminRowIdDelete()**](DirectoryAdminApi.md#directoryAdminRowIdDelete) | **DELETE** /directory/admin/row/{id} | Delete directory content row |
| [**directoryAdminRowIdGet()**](DirectoryAdminApi.md#directoryAdminRowIdGet) | **GET** /directory/admin/row/{id} | Get directory content row |
| [**directoryAdminRowIdPut()**](DirectoryAdminApi.md#directoryAdminRowIdPut) | **PUT** /directory/admin/row/{id} | Update directory content row |
| [**directoryAdminSearchPost()**](DirectoryAdminApi.md#directoryAdminSearchPost) | **POST** /directory/admin/search | Create cursor |
| [**directoryAdminTemplateGet()**](DirectoryAdminApi.md#directoryAdminTemplateGet) | **GET** /directory/admin/template | Get directory template list |


## `directoryAdminGet()`

```php
directoryAdminGet($cursor, $page, $session, $limit): \OpenAPI\Client\Model\DirectoryAdminGet200ResponseInner[]
```

Get directory list for cursor

This endpoint is for retrieving all directories for the requested cursor in admin representation.  Cursor could be created here: POST /directory/admin/search  _accessible without permission_

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\DirectoryAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$cursor = 'cursor_example'; // string | id of the cursor used for pagination; required if page is set
$page = 56; // int | current page index of the cursor used for pagination; required if cursor is set
$session = 'session_example'; // string | JWT
$limit = 56; // int | amount of results per page (1 ... 100)

try {
    $result = $apiInstance->directoryAdminGet($cursor, $page, $session, $limit);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DirectoryAdminApi->directoryAdminGet: ', $e->getMessage(), PHP_EOL;
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

[**\OpenAPI\Client\Model\DirectoryAdminGet200ResponseInner[]**](../Model/DirectoryAdminGet200ResponseInner.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `directoryAdminIdContentGet()`

```php
directoryAdminIdContentGet($id, $session, $cursor, $limit, $page): \OpenAPI\Client\Model\ContentRowResponseAdmin[]
```

Get directory content rows list

This endpoint is for retrieving all content rows of the requested directory in admin representation. If directory has no items defined, output for dynamic directories will be empty. If a limit is set, a cursor for this endpoint may be created to iterate over all content rows.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\DirectoryAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Directory ID
$session = 'session_example'; // string | JWT
$cursor = 'cursor_example'; // string | id of the cursor used for pagination; required if page is set
$limit = 56; // int | amount of results per page (1 ... 100)
$page = 56; // int | current page index of the cursor used for pagination; required if cursor is set

try {
    $result = $apiInstance->directoryAdminIdContentGet($id, $session, $cursor, $limit, $page);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DirectoryAdminApi->directoryAdminIdContentGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Directory ID | |
| **session** | **string**| JWT | |
| **cursor** | **string**| id of the cursor used for pagination; required if page is set | [optional] |
| **limit** | **int**| amount of results per page (1 ... 100) | [optional] |
| **page** | **int**| current page index of the cursor used for pagination; required if cursor is set | [optional] |

### Return type

[**\OpenAPI\Client\Model\ContentRowResponseAdmin[]**](../Model/ContentRowResponseAdmin.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `directoryAdminIdContentPost()`

```php
directoryAdminIdContentPost($id, $session, $request): \OpenAPI\Client\Model\ContentRowResponseAdmin[]
```

Add directory content rows

This endpoint is for adding new content rows to the requested static directory. For dynamic directories no content can be added in this way. In case of response status is 205 the request was only executed partial. Use GET to receive the stored configuration.  __Note:__ rows for dynamic directory (contentRowObjectType != null) are not creatable here. Status 409 Conflict will be returned.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\DirectoryAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Directory ID
$session = 'session_example'; // string | JWT
$request = array(new \OpenAPI\Client\Model\ContentRowPostRequestAdmin()); // \OpenAPI\Client\Model\ContentRowPostRequestAdmin[] | directory content rows to create; max 100 elements are permitted per request

try {
    $result = $apiInstance->directoryAdminIdContentPost($id, $session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DirectoryAdminApi->directoryAdminIdContentPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Directory ID | |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\ContentRowPostRequestAdmin[]**](../Model/ContentRowPostRequestAdmin.md)| directory content rows to create; max 100 elements are permitted per request | |

### Return type

[**\OpenAPI\Client\Model\ContentRowResponseAdmin[]**](../Model/ContentRowResponseAdmin.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `directoryAdminIdCopyPost()`

```php
directoryAdminIdCopyPost($id, $session, $request): \OpenAPI\Client\Model\DirectoryAdminPost200Response
```

Copy directory

This endpoint is for coping a directory. In case of response status is 205 the request was performed correctly, but the server was not able to send the response data. Use GET to receive the stored configuration.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\DirectoryAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Directory ID
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\DirectoryCopyPostRequest(); // \OpenAPI\Client\Model\DirectoryCopyPostRequest | directory to be copied

try {
    $result = $apiInstance->directoryAdminIdCopyPost($id, $session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DirectoryAdminApi->directoryAdminIdCopyPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Directory ID | |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\DirectoryCopyPostRequest**](../Model/DirectoryCopyPostRequest.md)| directory to be copied | |

### Return type

[**\OpenAPI\Client\Model\DirectoryAdminPost200Response**](../Model/DirectoryAdminPost200Response.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `directoryAdminIdDelete()`

```php
directoryAdminIdDelete($id, $session): \OpenAPI\Client\Model\ModelSwagStatusOk
```

Delete directory

This endpoint is for deleting a directory with all localizations.  __Note:__ if isSystem = true the directory is not deletable, api call will result in a http 409  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\DirectoryAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Directory ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->directoryAdminIdDelete($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DirectoryAdminApi->directoryAdminIdDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Directory ID | |
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

## `directoryAdminIdDetailGet()`

```php
directoryAdminIdDetailGet($id, $session): \OpenAPI\Client\Model\DirectoryAdminIdDetailGet200Response
```

Get directory detail view

This endpoint is for retrieving the detail config, items and selections of a directory  __DateTime formats:__ * `\"DateOnly\"`: \"2006-01-02\" * `\"DateTime\"`: \"2006-01-02 15:04:05\" * `\"RFC822X\"`: \"02 Jan 06 15:04\" * `\"RFC1123X\"`: \"Mon, 02 Jan 2006 15:04\" * `\"RFC1123DateOnly\"`: \"Mon, 02 Jan 2006\" * `\"TimeOnlyX\"`: \"15:04\"  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\DirectoryAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Directory ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->directoryAdminIdDetailGet($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DirectoryAdminApi->directoryAdminIdDetailGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Directory ID | |
| **session** | **string**| JWT | |

### Return type

[**\OpenAPI\Client\Model\DirectoryAdminIdDetailGet200Response**](../Model/DirectoryAdminIdDetailGet200Response.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `directoryAdminIdDetailPut()`

```php
directoryAdminIdDetailPut($id, $session, $request): \OpenAPI\Client\Model\DirectoryAdminIdDetailGet200Response
```

Update directory detail view

This endpoint is for updating the detail of an existing directory. New Items need a client generated unique id for setting reference in detail. client generated id will be changed from server so item ids in response will differ!  __DateTime formats:__ * `\"DateOnly\"`: \"2006-01-02\" * `\"DateTime\"`: \"2006-01-02 15:04:05\" * `\"RFC822X\"`: \"02 Jan 06 15:04\" * `\"RFC1123X\"`: \"Mon, 02 Jan 2006 15:04\" * `\"RFC1123DateOnly\"`: \"Mon, 02 Jan 2006\" * `\"TimeOnlyX\"`: \"15:04\"  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\DirectoryAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Directory ID
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\DirectoryPutDetailRequest(); // \OpenAPI\Client\Model\DirectoryPutDetailRequest | detail to be updated

try {
    $result = $apiInstance->directoryAdminIdDetailPut($id, $session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DirectoryAdminApi->directoryAdminIdDetailPut: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Directory ID | |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\DirectoryPutDetailRequest**](../Model/DirectoryPutDetailRequest.md)| detail to be updated | |

### Return type

[**\OpenAPI\Client\Model\DirectoryAdminIdDetailGet200Response**](../Model/DirectoryAdminIdDetailGet200Response.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `directoryAdminIdGet()`

```php
directoryAdminIdGet($id, $session): \OpenAPI\Client\Model\DirectoryAdminPost200Response
```

Get directory

This endpoint returns a localized directory in administrative representation by given id.  __DateTime formats:__ * `\"DateOnly\"`: \"2006-01-02\" * `\"DateTime\"`: \"2006-01-02 15:04:05\" * `\"RFC822X\"`: \"02 Jan 06 15:04\" * `\"RFC1123X\"`: \"Mon, 02 Jan 2006 15:04\" * `\"RFC1123DateOnly\"`: \"Mon, 02 Jan 2006\" * `\"TimeOnlyX\"`: \"15:04\"  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\DirectoryAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Directory ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->directoryAdminIdGet($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DirectoryAdminApi->directoryAdminIdGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Directory ID | |
| **session** | **string**| JWT | |

### Return type

[**\OpenAPI\Client\Model\DirectoryAdminPost200Response**](../Model/DirectoryAdminPost200Response.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `directoryAdminIdItemsGet()`

```php
directoryAdminIdItemsGet($id, $session): \OpenAPI\Client\Model\DirectorySwagResponseDirectoryItem[]
```

Get directory detail view items

This endpoint is for retrieving directory items.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\DirectoryAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Directory ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->directoryAdminIdItemsGet($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DirectoryAdminApi->directoryAdminIdItemsGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Directory ID | |
| **session** | **string**| JWT | |

### Return type

[**\OpenAPI\Client\Model\DirectorySwagResponseDirectoryItem[]**](../Model/DirectorySwagResponseDirectoryItem.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `directoryAdminIdListSettingsGet()`

```php
directoryAdminIdListSettingsGet($id, $session): \OpenAPI\Client\Model\ModelDirectoryListSettings
```

Get directory list settings

This endpoint returns the list settings of a specific directory.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\DirectoryAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Directory ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->directoryAdminIdListSettingsGet($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DirectoryAdminApi->directoryAdminIdListSettingsGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Directory ID | |
| **session** | **string**| JWT | [optional] |

### Return type

[**\OpenAPI\Client\Model\ModelDirectoryListSettings**](../Model/ModelDirectoryListSettings.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `directoryAdminIdListSettingsPut()`

```php
directoryAdminIdListSettingsPut($id, $session, $request): \OpenAPI\Client\Model\ModelDirectoryListSettings
```

Update directory list settings

This endpoint is for updating the list settings of an existing directory.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\DirectoryAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Directory ID
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\ModelDirectoryListSettings(); // \OpenAPI\Client\Model\ModelDirectoryListSettings | list settings to be updated

try {
    $result = $apiInstance->directoryAdminIdListSettingsPut($id, $session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DirectoryAdminApi->directoryAdminIdListSettingsPut: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Directory ID | |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\ModelDirectoryListSettings**](../Model/ModelDirectoryListSettings.md)| list settings to be updated | |

### Return type

[**\OpenAPI\Client\Model\ModelDirectoryListSettings**](../Model/ModelDirectoryListSettings.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `directoryAdminIdPatch()`

```php
directoryAdminIdPatch($id, $session, $request): \OpenAPI\Client\Model\DirectoryAdminPost200Response
```

Update directory info

This endpoint is for updating the base info of an existing directory. System directories have limited patch support  __Supported objectTypes for contentRowFilter:__ * contentRowObjectType = `\"Account\"` supported objectTypes: `\"Group\"`  ___createAccesses.DirectoryContentRow.any___: must be false; true currently not supported  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\DirectoryAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Directory ID
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\DirectoryPatchRequest(); // \OpenAPI\Client\Model\DirectoryPatchRequest | directory information to be updated

try {
    $result = $apiInstance->directoryAdminIdPatch($id, $session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DirectoryAdminApi->directoryAdminIdPatch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Directory ID | |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\DirectoryPatchRequest**](../Model/DirectoryPatchRequest.md)| directory information to be updated | |

### Return type

[**\OpenAPI\Client\Model\DirectoryAdminPost200Response**](../Model/DirectoryAdminPost200Response.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `directoryAdminIdSelectionsGet()`

```php
directoryAdminIdSelectionsGet($id, $session): \OpenAPI\Client\Model\SelectionAPIResponseAdmin[]
```

Get directory detail view selections

This endpoint is for retrieving directory selections.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\DirectoryAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Directory ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->directoryAdminIdSelectionsGet($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DirectoryAdminApi->directoryAdminIdSelectionsGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Directory ID | |
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

## `directoryAdminPost()`

```php
directoryAdminPost($session, $request): \OpenAPI\Client\Model\DirectoryAdminPost200Response
```

Create directory

This endpoint is for creating a new directory for chosen template.  __Supported objectTypes for contentRowFilter:__ * contentRowObjectType = `\"Account\"` supported objectTypes: `\"Group\"`  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\DirectoryAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\DirectoryPostRequest(); // \OpenAPI\Client\Model\DirectoryPostRequest | directory to create

try {
    $result = $apiInstance->directoryAdminPost($session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DirectoryAdminApi->directoryAdminPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\DirectoryPostRequest**](../Model/DirectoryPostRequest.md)| directory to create | |

### Return type

[**\OpenAPI\Client\Model\DirectoryAdminPost200Response**](../Model/DirectoryAdminPost200Response.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `directoryAdminProjectIdGet()`

```php
directoryAdminProjectIdGet($id, $session, $cursor, $limit, $page): \OpenAPI\Client\Model\DirectoryAdminGet200ResponseInner[]
```

Get directory list for project

This endpoint is for retrieving all directories of a project in admin representation. If a limit is set, a cursor for this endpoint may be created to iterate over all directories.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\DirectoryAdminApi(
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
    $result = $apiInstance->directoryAdminProjectIdGet($id, $session, $cursor, $limit, $page);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DirectoryAdminApi->directoryAdminProjectIdGet: ', $e->getMessage(), PHP_EOL;
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

[**\OpenAPI\Client\Model\DirectoryAdminGet200ResponseInner[]**](../Model/DirectoryAdminGet200ResponseInner.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `directoryAdminRowIdAccessGet()`

```php
directoryAdminRowIdAccessGet($id, $session): \OpenAPI\Client\Model\AuthorizationAccessResponse
```

Get directory row access configuration

This endpoint returns the access configuration for the requested directory row.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\DirectoryAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Row ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->directoryAdminRowIdAccessGet($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DirectoryAdminApi->directoryAdminRowIdAccessGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Row ID | |
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

## `directoryAdminRowIdAccessPatch()`

```php
directoryAdminRowIdAccessPatch($id, $session, $request): \OpenAPI\Client\Model\ModelAccess
```

Update directory row access configuration

This endpoint updates the access configuration for the requested directory row. Only the changes should be transmitted due this endpoint.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\DirectoryAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Row ID
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\ModelAccess(); // \OpenAPI\Client\Model\ModelAccess | changed access rights

try {
    $result = $apiInstance->directoryAdminRowIdAccessPatch($id, $session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DirectoryAdminApi->directoryAdminRowIdAccessPatch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Row ID | |
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

## `directoryAdminRowIdDelete()`

```php
directoryAdminRowIdDelete($id, $session): \OpenAPI\Client\Model\ModelSwagStatusOk
```

Delete directory content row

This endpoint is for deleting a directory content row.  __Note:__ rows for dynamic directory (contentRowObjectType != null) are not deletable here. Status 409 Conflict will be returned.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\DirectoryAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Row ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->directoryAdminRowIdDelete($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DirectoryAdminApi->directoryAdminRowIdDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Row ID | |
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

## `directoryAdminRowIdGet()`

```php
directoryAdminRowIdGet($id, $session): \OpenAPI\Client\Model\ContentRowResponseAdmin
```

Get directory content row

This endpoint is for retrieving a content row of a directory.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\DirectoryAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Row ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->directoryAdminRowIdGet($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DirectoryAdminApi->directoryAdminRowIdGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Row ID | |
| **session** | **string**| JWT | |

### Return type

[**\OpenAPI\Client\Model\ContentRowResponseAdmin**](../Model/ContentRowResponseAdmin.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `directoryAdminRowIdPut()`

```php
directoryAdminRowIdPut($id, $session, $request): \OpenAPI\Client\Model\ContentRowResponseAdmin
```

Update directory content row

This endpoint is for updating a directory content row by row ID.  __Note:__ rows for dynamic directory (contentRowObjectType != null) are not changeable here. Status 409 Conflict will be returned.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\DirectoryAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Row ID
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\ContentRowRequestAdmin(); // \OpenAPI\Client\Model\ContentRowRequestAdmin | directory content row to be replaced

try {
    $result = $apiInstance->directoryAdminRowIdPut($id, $session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DirectoryAdminApi->directoryAdminRowIdPut: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Row ID | |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\ContentRowRequestAdmin**](../Model/ContentRowRequestAdmin.md)| directory content row to be replaced | |

### Return type

[**\OpenAPI\Client\Model\ContentRowResponseAdmin**](../Model/ContentRowResponseAdmin.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `directoryAdminSearchPost()`

```php
directoryAdminSearchPost($session, $request): \OpenAPI\Client\Model\ModelCursorResponse
```

Create cursor

This endpoint returns a cursor for list directories in admin representation with applied filter and sort options. In case of cursor response total will be 0 the status 204 with not content is returned instead.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\DirectoryAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\DirectoryCursorRequestAdmin(); // \OpenAPI\Client\Model\DirectoryCursorRequestAdmin | options to create cursor

try {
    $result = $apiInstance->directoryAdminSearchPost($session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DirectoryAdminApi->directoryAdminSearchPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\DirectoryCursorRequestAdmin**](../Model/DirectoryCursorRequestAdmin.md)| options to create cursor | |

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

## `directoryAdminTemplateGet()`

```php
directoryAdminTemplateGet($session, $cursor, $limit, $page): \OpenAPI\Client\Model\DirectoryAdminTemplateGet200ResponseInner[]
```

Get directory template list

This endpoint retrieving templates to enhance the creation of new directories. If a limit is set, a cursor for this endpoint may be created to iterate over all templates.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\DirectoryAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT
$cursor = 'cursor_example'; // string | id of the cursor used for pagination; required if page is set
$limit = 56; // int | amount of results per page (1 ... 100)
$page = 56; // int | current page index of the cursor used for pagination; required if cursor is set

try {
    $result = $apiInstance->directoryAdminTemplateGet($session, $cursor, $limit, $page);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DirectoryAdminApi->directoryAdminTemplateGet: ', $e->getMessage(), PHP_EOL;
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

[**\OpenAPI\Client\Model\DirectoryAdminTemplateGet200ResponseInner[]**](../Model/DirectoryAdminTemplateGet200ResponseInner.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
