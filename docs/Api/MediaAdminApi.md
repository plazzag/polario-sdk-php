# OpenAPI\Client\MediaAdminApi



All URIs are relative to https://custom.polario.de/api, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**configAdminMediaDefaultGet()**](MediaAdminApi.md#configAdminMediaDefaultGet) | **GET** /config/admin/media/default | Get factory default media configuration |
| [**configAdminMediaGet()**](MediaAdminApi.md#configAdminMediaGet) | **GET** /config/admin/media | Get media configuration |
| [**configAdminMediaPatch()**](MediaAdminApi.md#configAdminMediaPatch) | **PATCH** /config/admin/media | Update media configuration |
| [**mediaAdminFolderGet()**](MediaAdminApi.md#mediaAdminFolderGet) | **GET** /media/admin/folder | Get folder list |
| [**mediaAdminFolderIdDelete()**](MediaAdminApi.md#mediaAdminFolderIdDelete) | **DELETE** /media/admin/folder/{id} | Delete folder |
| [**mediaAdminFolderIdGet()**](MediaAdminApi.md#mediaAdminFolderIdGet) | **GET** /media/admin/folder/{id} | Get folder |
| [**mediaAdminFolderIdPatch()**](MediaAdminApi.md#mediaAdminFolderIdPatch) | **PATCH** /media/admin/folder/{id} | Update folder |
| [**mediaAdminFolderPost()**](MediaAdminApi.md#mediaAdminFolderPost) | **POST** /media/admin/folder | Create folder |
| [**mediaAdminGet()**](MediaAdminApi.md#mediaAdminGet) | **GET** /media/admin | Get media items list |
| [**mediaAdminIdAccessGet()**](MediaAdminApi.md#mediaAdminIdAccessGet) | **GET** /media/admin/{id}/access | Get media item access configuration |
| [**mediaAdminIdAccessPatch()**](MediaAdminApi.md#mediaAdminIdAccessPatch) | **PATCH** /media/admin/{id}/access | Update media item access configuration |
| [**mediaAdminIdDelete()**](MediaAdminApi.md#mediaAdminIdDelete) | **DELETE** /media/admin/{id} | Delete media item and file |
| [**mediaAdminIdDuplicatePost()**](MediaAdminApi.md#mediaAdminIdDuplicatePost) | **POST** /media/admin/{id}/duplicate | Duplicate media item and file |
| [**mediaAdminIdFileGet()**](MediaAdminApi.md#mediaAdminIdFileGet) | **GET** /media/admin/{id}/file | Get file |
| [**mediaAdminIdFilePut()**](MediaAdminApi.md#mediaAdminIdFilePut) | **PUT** /media/admin/{id}/file | Update file |
| [**mediaAdminIdGet()**](MediaAdminApi.md#mediaAdminIdGet) | **GET** /media/admin/{id} | Get media item |
| [**mediaAdminIdPatch()**](MediaAdminApi.md#mediaAdminIdPatch) | **PATCH** /media/admin/{id} | Update media item metadata |
| [**mediaAdminIdPermalinkGet()**](MediaAdminApi.md#mediaAdminIdPermalinkGet) | **GET** /media/admin/{id}/permalink | Get permalink |
| [**mediaAdminIdThumbnailGet()**](MediaAdminApi.md#mediaAdminIdThumbnailGet) | **GET** /media/admin/{id}/thumbnail | Get thumbnail |
| [**mediaAdminPost()**](MediaAdminApi.md#mediaAdminPost) | **POST** /media/admin | Upload file &amp; create media item |
| [**mediaAdminSearchPost()**](MediaAdminApi.md#mediaAdminSearchPost) | **POST** /media/admin/search | Create cursor |


## `configAdminMediaDefaultGet()`

```php
configAdminMediaDefaultGet($session): \OpenAPI\Client\Model\ConfigurationMediaConfigurationResponse
```

Get factory default media configuration

This endpoint returns the default media configuration. This can be used for reset settings to default value.  _accessible without permission_  _fully accessible with permission_ : `\"ManageConfiguration\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\MediaAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->configAdminMediaDefaultGet($session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MediaAdminApi->configAdminMediaDefaultGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **session** | **string**| JWT | |

### Return type

[**\OpenAPI\Client\Model\ConfigurationMediaConfigurationResponse**](../Model/ConfigurationMediaConfigurationResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `configAdminMediaGet()`

```php
configAdminMediaGet($session, $if_modified_since): \OpenAPI\Client\Model\ConfigurationMediaConfigurationResponse
```

Get media configuration

This endpoint returns the media configuration. The If-Modified-Since header can be used for omitting the output if nothing has changed.  _accessible without permission_  _fully accessible with permission_ : `\"ManageConfiguration\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\MediaAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT
$if_modified_since = 56; // int | unix timestamp of the last sync

try {
    $result = $apiInstance->configAdminMediaGet($session, $if_modified_since);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MediaAdminApi->configAdminMediaGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **session** | **string**| JWT | |
| **if_modified_since** | **int**| unix timestamp of the last sync | [optional] |

### Return type

[**\OpenAPI\Client\Model\ConfigurationMediaConfigurationResponse**](../Model/ConfigurationMediaConfigurationResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `configAdminMediaPatch()`

```php
configAdminMediaPatch($session, $if_modified_since, $request): \OpenAPI\Client\Model\ConfigurationMediaConfigurationResponse
```

Update media configuration

This endpoint is for updating the media configuration. The If-Modified-Since header can be used for omitting the request if nothing has changed.  _only accessible with permission_ : `\"ManageConfiguration\"`  _fully accessible with permission_ : `\"ManageConfiguration\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\MediaAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT
$if_modified_since = 56; // int | unix timestamp
$request = new \OpenAPI\Client\Model\ConfigurationMediaConfigurationRequestAdmin(); // \OpenAPI\Client\Model\ConfigurationMediaConfigurationRequestAdmin | media data to be updated

try {
    $result = $apiInstance->configAdminMediaPatch($session, $if_modified_since, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MediaAdminApi->configAdminMediaPatch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **session** | **string**| JWT | |
| **if_modified_since** | **int**| unix timestamp | [optional] |
| **request** | [**\OpenAPI\Client\Model\ConfigurationMediaConfigurationRequestAdmin**](../Model/ConfigurationMediaConfigurationRequestAdmin.md)| media data to be updated | [optional] |

### Return type

[**\OpenAPI\Client\Model\ConfigurationMediaConfigurationResponse**](../Model/ConfigurationMediaConfigurationResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `mediaAdminFolderGet()`

```php
mediaAdminFolderGet($session, $cursor, $limit, $page): \OpenAPI\Client\Model\FolderResponse[]
```

Get folder list

This endpoint returns all media folders. If a limit is set, a cursor for this endpoint may be created to iterate over all folders.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageGlobalMedia\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageGlobalMedia\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\MediaAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT
$cursor = 'cursor_example'; // string | id of the cursor used for pagination; required if page is set
$limit = 56; // int | amount of results per page (1 ... 100)
$page = 56; // int | current page index of the cursor used for pagination; required if cursor is set

try {
    $result = $apiInstance->mediaAdminFolderGet($session, $cursor, $limit, $page);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MediaAdminApi->mediaAdminFolderGet: ', $e->getMessage(), PHP_EOL;
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

[**\OpenAPI\Client\Model\FolderResponse[]**](../Model/FolderResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `mediaAdminFolderIdDelete()`

```php
mediaAdminFolderIdDelete($id, $session): \OpenAPI\Client\Model\ModelSwagStatusOk
```

Delete folder

This endpoint lets you delete a folder.  __Note:__ All media items within this folder will be deleted as well!  _only accessible with permission_ : `\"ManageContent\"` `\"ManageGlobalMedia\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageGlobalMedia\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\MediaAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Folder ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->mediaAdminFolderIdDelete($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MediaAdminApi->mediaAdminFolderIdDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Folder ID | |
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

## `mediaAdminFolderIdGet()`

```php
mediaAdminFolderIdGet($id, $session): \OpenAPI\Client\Model\FolderResponse
```

Get folder

This endpoint returns a media folder specified by the given id.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageGlobalMedia\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageGlobalMedia\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\MediaAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Folder ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->mediaAdminFolderIdGet($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MediaAdminApi->mediaAdminFolderIdGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Folder ID | |
| **session** | **string**| JWT | |

### Return type

[**\OpenAPI\Client\Model\FolderResponse**](../Model/FolderResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `mediaAdminFolderIdPatch()`

```php
mediaAdminFolderIdPatch($id, $session, $request): \OpenAPI\Client\Model\FolderResponse
```

Update folder

This endpoint is for updating specific data of an existing folder.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageGlobalMedia\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageGlobalMedia\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\MediaAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Folder ID
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\FolderPatchRequest(); // \OpenAPI\Client\Model\FolderPatchRequest | Folder data to update

try {
    $result = $apiInstance->mediaAdminFolderIdPatch($id, $session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MediaAdminApi->mediaAdminFolderIdPatch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Folder ID | |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\FolderPatchRequest**](../Model/FolderPatchRequest.md)| Folder data to update | |

### Return type

[**\OpenAPI\Client\Model\FolderResponse**](../Model/FolderResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `mediaAdminFolderPost()`

```php
mediaAdminFolderPost($session, $request): \OpenAPI\Client\Model\FolderResponse
```

Create folder

This endpoint creates a new media folder.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageGlobalMedia\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageGlobalMedia\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\MediaAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\FolderRequest(); // \OpenAPI\Client\Model\FolderRequest | Folder to create

try {
    $result = $apiInstance->mediaAdminFolderPost($session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MediaAdminApi->mediaAdminFolderPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\FolderRequest**](../Model/FolderRequest.md)| Folder to create | |

### Return type

[**\OpenAPI\Client\Model\FolderResponse**](../Model/FolderResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `mediaAdminGet()`

```php
mediaAdminGet($session, $cursor, $limit, $page): \OpenAPI\Client\Model\MediaResponseListAdmin[]
```

Get media items list

This endpoint list all media items in admin representation. The output is filtered for the user permissions. If a limit is set, a cursor for this endpoint may be created to iterate over all media items.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageGlobalMedia\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageGlobalMedia\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\MediaAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT
$cursor = 'cursor_example'; // string | id of the cursor used for pagination; required if page is set
$limit = 56; // int | amount of results per page (1 ... 100)
$page = 56; // int | current page index of the cursor used for pagination; required if cursor is set

try {
    $result = $apiInstance->mediaAdminGet($session, $cursor, $limit, $page);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MediaAdminApi->mediaAdminGet: ', $e->getMessage(), PHP_EOL;
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

[**\OpenAPI\Client\Model\MediaResponseListAdmin[]**](../Model/MediaResponseListAdmin.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `mediaAdminIdAccessGet()`

```php
mediaAdminIdAccessGet($id, $session): \OpenAPI\Client\Model\AuthorizationAccessResponse
```

Get media item access configuration

This endpoint returns the access configuration for the requested media item (file).  _only accessible with permission_ : `\"ManageContent\"` `\"ManageGlobalMedia\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageGlobalMedia\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\MediaAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | MediaItem ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->mediaAdminIdAccessGet($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MediaAdminApi->mediaAdminIdAccessGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| MediaItem ID | |
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

## `mediaAdminIdAccessPatch()`

```php
mediaAdminIdAccessPatch($id, $session, $request): \OpenAPI\Client\Model\ModelAccess
```

Update media item access configuration

This endpoint updates the access configuration for the requested media item (file). Only the changes should be transmitted due this endpoint.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageGlobalMedia\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageGlobalMedia\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\MediaAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | MediaItem ID
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\ModelAccess(); // \OpenAPI\Client\Model\ModelAccess | changed access rights

try {
    $result = $apiInstance->mediaAdminIdAccessPatch($id, $session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MediaAdminApi->mediaAdminIdAccessPatch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| MediaItem ID | |
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

## `mediaAdminIdDelete()`

```php
mediaAdminIdDelete($id, $session): \OpenAPI\Client\Model\ModelSwagStatusOk
```

Delete media item and file

This endpoint is for deleting a file (media item). Items of a readonly folder are not deletable.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageGlobalMedia\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageGlobalMedia\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\MediaAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Media ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->mediaAdminIdDelete($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MediaAdminApi->mediaAdminIdDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Media ID | |
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

## `mediaAdminIdDuplicatePost()`

```php
mediaAdminIdDuplicatePost($id, $session, $request): \OpenAPI\Client\Model\MediaResponseAdmin
```

Duplicate media item and file

This endpoint is for duplicating a file (media item). Only Media items that are not private could be duplicated.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageGlobalMedia\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageGlobalMedia\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\MediaAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Media ID
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\MediaDuplicationRequest(); // \OpenAPI\Client\Model\MediaDuplicationRequest | Duplication request

try {
    $result = $apiInstance->mediaAdminIdDuplicatePost($id, $session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MediaAdminApi->mediaAdminIdDuplicatePost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Media ID | |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\MediaDuplicationRequest**](../Model/MediaDuplicationRequest.md)| Duplication request | |

### Return type

[**\OpenAPI\Client\Model\MediaResponseAdmin**](../Model/MediaResponseAdmin.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `mediaAdminIdFileGet()`

```php
mediaAdminIdFileGet($id, $session)
```

Get file

This endpoint is for retrieving a media file directly.  The content type of the media file, will be the same as the file's MIME-Type. (E.g. when a jpg file was uploaded, the response will be an image/jpg)  Error messages are json encoded, as usual.  _Notice_: Do not use the `If-Modified-Since` header.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageGlobalMedia\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageGlobalMedia\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\MediaAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Media ID
$session = 'session_example'; // string | JWT

try {
    $apiInstance->mediaAdminIdFileGet($id, $session);
} catch (Exception $e) {
    echo 'Exception when calling MediaAdminApi->mediaAdminIdFileGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Media ID | |
| **session** | **string**| JWT | |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `*/*`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `mediaAdminIdFilePut()`

```php
mediaAdminIdFilePut($id, $session, $file): \OpenAPI\Client\Model\MediaResponseAdmin
```

Update file

This endpoint is for updating a specific file.  __Note:__ You can only update a file with a file of the same mime type. So, a png can not be updated with a jpeg file. The mime type and media type always stays the same.  __Supported Content-Types:__ * application/msword * application/pdf * application/vnd.ms-excel * application/vnd.ms-powerpoint * application/vnd.openxmlformats-officedocument.presentationml.presentation * application/vnd.openxmlformats-officedocument.spreadsheetml.sheet * application/vnd.openxmlformats-officedocument.wordprocessingml.document * image/jpeg * image/png * image/svg+xml * video/mp4  For uploading other formats uploadRestriction has to be deactivated here: PATCH /config/admin/media  _only accessible with permission_ : `\"ManageContent\"` `\"ManageGlobalMedia\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageGlobalMedia\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\MediaAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Media Item ID
$session = 'session_example'; // string | JWT
$file = 'file_example'; // string | The new file

try {
    $result = $apiInstance->mediaAdminIdFilePut($id, $session, $file);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MediaAdminApi->mediaAdminIdFilePut: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Media Item ID | |
| **session** | **string**| JWT | |
| **file** | **string**| The new file | |

### Return type

[**\OpenAPI\Client\Model\MediaResponseAdmin**](../Model/MediaResponseAdmin.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `multipart/form-data`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `mediaAdminIdGet()`

```php
mediaAdminIdGet($id, $session): \OpenAPI\Client\Model\MediaResponseAdmin
```

Get media item

This endpoint is for retrieving a media item with a signed url to the file in admin representation.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageGlobalMedia\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageGlobalMedia\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\MediaAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Media ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->mediaAdminIdGet($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MediaAdminApi->mediaAdminIdGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Media ID | |
| **session** | **string**| JWT | |

### Return type

[**\OpenAPI\Client\Model\MediaResponseAdmin**](../Model/MediaResponseAdmin.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `mediaAdminIdPatch()`

```php
mediaAdminIdPatch($id, $session, $request): \OpenAPI\Client\Model\MediaResponseAdmin
```

Update media item metadata

This endpoint offers the possibility to update the metadata of a given media item.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageGlobalMedia\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageGlobalMedia\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\MediaAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Media Item ID
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\MediaPatchRequestAdmin(); // \OpenAPI\Client\Model\MediaPatchRequestAdmin | media item data to update

try {
    $result = $apiInstance->mediaAdminIdPatch($id, $session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MediaAdminApi->mediaAdminIdPatch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Media Item ID | |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\MediaPatchRequestAdmin**](../Model/MediaPatchRequestAdmin.md)| media item data to update | |

### Return type

[**\OpenAPI\Client\Model\MediaResponseAdmin**](../Model/MediaResponseAdmin.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `mediaAdminIdPermalinkGet()`

```php
mediaAdminIdPermalinkGet($id, $session): \OpenAPI\Client\Model\MediaResponsePermalink[]
```

Get permalink

This endpoint is for retrieving the permalink of media file directly for _mediaType_ `\"MediaIcon\"` or `\"MediaImage\". A permalink could only be created for media items that are not private.  _only accessible with permission_ : `\"ManageGlobalMedia\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageGlobalMedia\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\MediaAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Media ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->mediaAdminIdPermalinkGet($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MediaAdminApi->mediaAdminIdPermalinkGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Media ID | |
| **session** | **string**| JWT | |

### Return type

[**\OpenAPI\Client\Model\MediaResponsePermalink[]**](../Model/MediaResponsePermalink.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `*/*`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `mediaAdminIdThumbnailGet()`

```php
mediaAdminIdThumbnailGet($id, $session)
```

Get thumbnail

This endpoint is for retrieving the thumbnail of media file directly.  The content type of the media file, will be the same as the file's MIME-Type. (E.g. when a jpg file was uploaded, the response will be an image/jpg)  Error messages are json encoded, as usual.  _Notice_: Do not use the `If-Modified-Since` header.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageGlobalMedia\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageGlobalMedia\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\MediaAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Media ID
$session = 'session_example'; // string | JWT

try {
    $apiInstance->mediaAdminIdThumbnailGet($id, $session);
} catch (Exception $e) {
    echo 'Exception when calling MediaAdminApi->mediaAdminIdThumbnailGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Media ID | |
| **session** | **string**| JWT | |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `*/*`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `mediaAdminPost()`

```php
mediaAdminPost($session, $alt_text, $file, $folder_id, $project_id, $title, $description, $private): \OpenAPI\Client\Model\MediaResponseAdmin
```

Upload file & create media item

This endpoint is for uploading a file.  __Supported Content-Types:__ * application/msword * application/pdf * application/vnd.ms-excel * application/vnd.ms-powerpoint * application/vnd.openxmlformats-officedocument.presentationml.presentation * application/vnd.openxmlformats-officedocument.spreadsheetml.sheet * application/vnd.openxmlformats-officedocument.wordprocessingml.document * image/jpeg * image/png * image/svg+xml * video/mp4  For uploading profile image the file should be PNG or JPEG.  For uploading other formats uploadRestriction has to be deactivated here: PATCH /config/admin/media  _only accessible with permission_ : `\"ManageContent\"` `\"ManageGlobalMedia\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageGlobalMedia\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\MediaAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT
$alt_text = 'alt_text_example'; // string | Alt text for the media file
$file = 'file_example'; // string | The actual file
$folder_id = 'folder_id_example'; // string | The ID of the folder the file should be stored in
$project_id = 'project_id_example'; // string | The ID of the project the file belongs in
$title = 'title_example'; // string | Title of the uploaded item
$description = 'description_example'; // string | The description of an uploaded item
$private = True; // bool | private files will not be shown in list files endpoint for admin users

try {
    $result = $apiInstance->mediaAdminPost($session, $alt_text, $file, $folder_id, $project_id, $title, $description, $private);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MediaAdminApi->mediaAdminPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **session** | **string**| JWT | |
| **alt_text** | **string**| Alt text for the media file | |
| **file** | **string**| The actual file | |
| **folder_id** | **string**| The ID of the folder the file should be stored in | |
| **project_id** | **string**| The ID of the project the file belongs in | |
| **title** | **string**| Title of the uploaded item | |
| **description** | **string**| The description of an uploaded item | [optional] |
| **private** | **bool**| private files will not be shown in list files endpoint for admin users | [optional] |

### Return type

[**\OpenAPI\Client\Model\MediaResponseAdmin**](../Model/MediaResponseAdmin.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `multipart/form-data`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `mediaAdminSearchPost()`

```php
mediaAdminSearchPost($session, $request): \OpenAPI\Client\Model\ModelCursorResponse
```

Create cursor

This endpoint returns a cursor for list media items in admin representation with applied filter and sort options. In case of cursor response total will be 0 the status 204 with not content is returned instead.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\MediaAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\MediaCursorRequestAdmin(); // \OpenAPI\Client\Model\MediaCursorRequestAdmin | options to create cursor

try {
    $result = $apiInstance->mediaAdminSearchPost($session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MediaAdminApi->mediaAdminSearchPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\MediaCursorRequestAdmin**](../Model/MediaCursorRequestAdmin.md)| options to create cursor | |

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
