# OpenAPI\Client\MediaDefaultApi



All URIs are relative to https://custom.polario.de/api, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**configDefaultMediaGet()**](MediaDefaultApi.md#configDefaultMediaGet) | **GET** /config/default/media | Get media configuration |
| [**mediaDefaultDownloadGet()**](MediaDefaultApi.md#mediaDefaultDownloadGet) | **GET** /media/default/download | Download media items |
| [**mediaDefaultDownloadIdGet()**](MediaDefaultApi.md#mediaDefaultDownloadIdGet) | **GET** /media/default/download/{id} | Get download status |
| [**mediaDefaultFolderIdContentGet()**](MediaDefaultApi.md#mediaDefaultFolderIdContentGet) | **GET** /media/default/folder/{id}/content | Get media items list of folder |
| [**mediaDefaultGet()**](MediaDefaultApi.md#mediaDefaultGet) | **GET** /media/default | Get media items list |
| [**mediaDefaultIdDelete()**](MediaDefaultApi.md#mediaDefaultIdDelete) | **DELETE** /media/default/{id} | Delete media item and file |
| [**mediaDefaultIdFileGet()**](MediaDefaultApi.md#mediaDefaultIdFileGet) | **GET** /media/default/{id}/file | Get file |
| [**mediaDefaultIdFilePut()**](MediaDefaultApi.md#mediaDefaultIdFilePut) | **PUT** /media/default/{id}/file | Update file |
| [**mediaDefaultIdGet()**](MediaDefaultApi.md#mediaDefaultIdGet) | **GET** /media/default/{id} | Get media item |
| [**mediaDefaultIdPatch()**](MediaDefaultApi.md#mediaDefaultIdPatch) | **PATCH** /media/default/{id} | Update media item metadata |
| [**mediaDefaultIdThumbnailGet()**](MediaDefaultApi.md#mediaDefaultIdThumbnailGet) | **GET** /media/default/{id}/thumbnail | Get thumbnail |
| [**mediaDefaultIdsGet()**](MediaDefaultApi.md#mediaDefaultIdsGet) | **GET** /media/default/ids | Get media item ids |
| [**mediaDefaultPost()**](MediaDefaultApi.md#mediaDefaultPost) | **POST** /media/default | Upload file &amp; create media item |
| [**mediaDefaultSearchPost()**](MediaDefaultApi.md#mediaDefaultSearchPost) | **POST** /media/default/search | Create cursor |


## `configDefaultMediaGet()`

```php
configDefaultMediaGet($if_modified_since, $session): \OpenAPI\Client\Model\ConfigurationMediaConfigurationResponse
```

Get media configuration

This endpoint returns the media configuration. The If-Modified-Since header can be used for omitting the output if nothing has changed.  _accessible without permission_  _fully accessible with permission_ : `\"ManageConfiguration\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\MediaDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$if_modified_since = 56; // int | unix timestamp of the last sync
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->configDefaultMediaGet($if_modified_since, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MediaDefaultApi->configDefaultMediaGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **if_modified_since** | **int**| unix timestamp of the last sync | [optional] |
| **session** | **string**| JWT | [optional] |

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

## `mediaDefaultDownloadGet()`

```php
mediaDefaultDownloadGet($ids, $session): \OpenAPI\Client\Model\DownloadrequestResponse
```

Download media items

This endpoint is for downloading multiple documents. Once started, the request is collection the files and put them into a zip file. The url to download the zip file from will be in the response after processing and available on calling this endpoint GET /media/default/download/{id}  The download will automatically fail after 2h. After 2h downloads are released to be cleaned up.  The provided ids are interpreted as filter, so invalid or not accessible ids will be ignored.  _accessible without permission_  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageGlobalMedia\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\MediaDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$ids = 'ids_example'; // string | ids to download
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->mediaDefaultDownloadGet($ids, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MediaDefaultApi->mediaDefaultDownloadGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **ids** | **string**| ids to download | |
| **session** | **string**| JWT | |

### Return type

[**\OpenAPI\Client\Model\DownloadrequestResponse**](../Model/DownloadrequestResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `mediaDefaultDownloadIdGet()`

```php
mediaDefaultDownloadIdGet($id, $session): \OpenAPI\Client\Model\DownloadrequestResponse
```

Get download status

This endpoint returns the information for a requested download  _accessible without permission_

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\MediaDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Download ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->mediaDefaultDownloadIdGet($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MediaDefaultApi->mediaDefaultDownloadIdGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Download ID | |
| **session** | **string**| JWT | [optional] |

### Return type

[**\OpenAPI\Client\Model\DownloadrequestResponse**](../Model/DownloadrequestResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `mediaDefaultFolderIdContentGet()`

```php
mediaDefaultFolderIdContentGet($id, $cursor, $limit, $page, $accept_language, $session): \OpenAPI\Client\Model\MediaResponseListDefault[]
```

Get media items list of folder

This endpoint list all media items in default representation for the requested folder id. The output is filtered for the user permissions. If the requested language is not available it will fall back to the default language. If a limit is set, a cursor for this endpoint may be created to iterate over all media items.  _accessible without permission_  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageGlobalMedia\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\MediaDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Folder ID
$cursor = 'cursor_example'; // string | id of the cursor used for pagination; required if page is set
$limit = 56; // int | amount of results per page (1 ... 100)
$page = 56; // int | current page index of the cursor used for pagination; required if cursor is set
$accept_language = 'accept_language_example'; // string | client language(s)
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->mediaDefaultFolderIdContentGet($id, $cursor, $limit, $page, $accept_language, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MediaDefaultApi->mediaDefaultFolderIdContentGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Folder ID | |
| **cursor** | **string**| id of the cursor used for pagination; required if page is set | [optional] |
| **limit** | **int**| amount of results per page (1 ... 100) | [optional] |
| **page** | **int**| current page index of the cursor used for pagination; required if cursor is set | [optional] |
| **accept_language** | **string**| client language(s) | [optional] |
| **session** | **string**| JWT | [optional] |

### Return type

[**\OpenAPI\Client\Model\MediaResponseListDefault[]**](../Model/MediaResponseListDefault.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `mediaDefaultGet()`

```php
mediaDefaultGet($cursor, $limit, $page, $accept_language, $session): \OpenAPI\Client\Model\MediaResponseListDefault[]
```

Get media items list

This endpoint list all media items in default representation. The output is filtered for the user permissions. If the requested language is not available it will fall back to the default language. If a limit is set, a cursor for this endpoint may be created to iterate over all media items.  _accessible without permission_  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageGlobalMedia\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\MediaDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$cursor = 'cursor_example'; // string | id of the cursor used for pagination; required if page is set
$limit = 56; // int | amount of results per page (1 ... 100)
$page = 56; // int | current page index of the cursor used for pagination; required if cursor is set
$accept_language = 'accept_language_example'; // string | client language(s)
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->mediaDefaultGet($cursor, $limit, $page, $accept_language, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MediaDefaultApi->mediaDefaultGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **cursor** | **string**| id of the cursor used for pagination; required if page is set | [optional] |
| **limit** | **int**| amount of results per page (1 ... 100) | [optional] |
| **page** | **int**| current page index of the cursor used for pagination; required if cursor is set | [optional] |
| **accept_language** | **string**| client language(s) | [optional] |
| **session** | **string**| JWT | [optional] |

### Return type

[**\OpenAPI\Client\Model\MediaResponseListDefault[]**](../Model/MediaResponseListDefault.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `mediaDefaultIdDelete()`

```php
mediaDefaultIdDelete($id, $session): \OpenAPI\Client\Model\ModelSwagStatusOk
```

Delete media item and file

This endpoint is for deleting a file (media item). Items of a readonly folder are not deletable.  _accessible without permission_  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageGlobalMedia\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\MediaDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Media ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->mediaDefaultIdDelete($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MediaDefaultApi->mediaDefaultIdDelete: ', $e->getMessage(), PHP_EOL;
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

## `mediaDefaultIdFileGet()`

```php
mediaDefaultIdFileGet($id, $session)
```

Get file

This endpoint is for retrieving a media file directly.  The content type of the media file, will be the same as the file's MIME-Type. (E.g. when a jpg file was uploaded, the response will be an image/jpg)  Error messages are json encoded, as usual.  _Notice_: Do not use the `If-Modified-Since` header.  _accessible without permission_  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageGlobalMedia\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\MediaDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Media ID
$session = 'session_example'; // string | JWT

try {
    $apiInstance->mediaDefaultIdFileGet($id, $session);
} catch (Exception $e) {
    echo 'Exception when calling MediaDefaultApi->mediaDefaultIdFileGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Media ID | |
| **session** | **string**| JWT | [optional] |

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

## `mediaDefaultIdFilePut()`

```php
mediaDefaultIdFilePut($id, $session, $file, $accept_language): \OpenAPI\Client\Model\ModelSwagStatusOk
```

Update file

This endpoint is for updating a specific file.  __Note:__ You can only update a file with a file of the same mime type. So, a png can not be updated with a jpeg file. The mime type and media type always stays the same.  __Supported Content-Types:__ * application/msword * application/pdf * application/vnd.ms-excel * application/vnd.ms-powerpoint * application/vnd.openxmlformats-officedocument.presentationml.presentation * application/vnd.openxmlformats-officedocument.spreadsheetml.sheet * application/vnd.openxmlformats-officedocument.wordprocessingml.document * image/jpeg * image/png * image/svg+xml * video/mp4  For uploading other formats uploadRestriction has to be deactivated here: PATCH /config/admin/media If the requested language is not available it will fall back to the default language.  _accessible without permission_  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageGlobalMedia\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\MediaDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Media Item ID
$session = 'session_example'; // string | JWT
$file = 'file_example'; // string | The new file
$accept_language = 'accept_language_example'; // string | client language(s)

try {
    $result = $apiInstance->mediaDefaultIdFilePut($id, $session, $file, $accept_language);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MediaDefaultApi->mediaDefaultIdFilePut: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Media Item ID | |
| **session** | **string**| JWT | |
| **file** | **string**| The new file | |
| **accept_language** | **string**| client language(s) | [optional] |

### Return type

[**\OpenAPI\Client\Model\ModelSwagStatusOk**](../Model/ModelSwagStatusOk.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `multipart/form-data`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `mediaDefaultIdGet()`

```php
mediaDefaultIdGet($id, $accept_language, $session): \OpenAPI\Client\Model\MediaResponseDefault
```

Get media item

This endpoint is for retrieving a media item with a signed url to the file in default representation. If the requested language is not available it will fall back to the default language.  _accessible without permission_  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageGlobalMedia\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\MediaDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Media ID
$accept_language = 'accept_language_example'; // string | client language(s)
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->mediaDefaultIdGet($id, $accept_language, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MediaDefaultApi->mediaDefaultIdGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Media ID | |
| **accept_language** | **string**| client language(s) | [optional] |
| **session** | **string**| JWT | [optional] |

### Return type

[**\OpenAPI\Client\Model\MediaResponseDefault**](../Model/MediaResponseDefault.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `mediaDefaultIdPatch()`

```php
mediaDefaultIdPatch($id, $session, $request, $accept_language): \OpenAPI\Client\Model\MediaResponseDefault
```

Update media item metadata

This endpoint offers the possibility to update the metadata of a given media item. If the requested language is not available it will fall back to the default language.  _accessible without permission_  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageGlobalMedia\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\MediaDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Media Item ID
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\MediaPatchRequestDefault(); // \OpenAPI\Client\Model\MediaPatchRequestDefault | media item data to update
$accept_language = 'accept_language_example'; // string | client language(s)

try {
    $result = $apiInstance->mediaDefaultIdPatch($id, $session, $request, $accept_language);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MediaDefaultApi->mediaDefaultIdPatch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Media Item ID | |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\MediaPatchRequestDefault**](../Model/MediaPatchRequestDefault.md)| media item data to update | |
| **accept_language** | **string**| client language(s) | [optional] |

### Return type

[**\OpenAPI\Client\Model\MediaResponseDefault**](../Model/MediaResponseDefault.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `mediaDefaultIdThumbnailGet()`

```php
mediaDefaultIdThumbnailGet($id, $session)
```

Get thumbnail

This endpoint is for retrieving the thumbnail of media file directly.  The content type of the media file, will be the same as the file's MIME-Type. (E.g. when a jpg file was uploaded, the response will be an image/jpg)  Error messages are json encoded, as usual.  _Notice_: Do not use the `If-Modified-Since` header.  _accessible without permission_  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageGlobalMedia\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\MediaDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Media ID
$session = 'session_example'; // string | JWT

try {
    $apiInstance->mediaDefaultIdThumbnailGet($id, $session);
} catch (Exception $e) {
    echo 'Exception when calling MediaDefaultApi->mediaDefaultIdThumbnailGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Media ID | |
| **session** | **string**| JWT | [optional] |

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

## `mediaDefaultIdsGet()`

```php
mediaDefaultIdsGet($session): string[]
```

Get media item ids

This endpoint returns ids of all media items.  _accessible without permission_  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageGlobalMedia\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\MediaDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->mediaDefaultIdsGet($session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MediaDefaultApi->mediaDefaultIdsGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **session** | **string**| JWT | [optional] |

### Return type

**string[]**

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `mediaDefaultPost()`

```php
mediaDefaultPost($session, $alt_text, $file, $folder_id, $project_id, $title, $accept_language, $private): \OpenAPI\Client\Model\MediaResponseDefault
```

Upload file & create media item

This endpoint is for uploading a file.  __Supported Content-Types:__ * application/msword * application/pdf * application/vnd.ms-excel * application/vnd.ms-powerpoint * application/vnd.openxmlformats-officedocument.presentationml.presentation * application/vnd.openxmlformats-officedocument.spreadsheetml.sheet * application/vnd.openxmlformats-officedocument.wordprocessingml.document * image/jpeg * image/png * image/svg+xml * video/mp4  For uploading profile image the file should be PNG or JPEG.  For uploading other formats uploadRestriction has to be deactivated here: PATCH /config/admin/media If the requested language is not available it will fall back to the default language.  __Note:__  _data.translations_ will be always empty. Translation takes places async. Call GET /media/default//{mediaId} to check for translation later.  _accessible without permission_  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageGlobalMedia\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\MediaDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT
$alt_text = 'alt_text_example'; // string | Alt text for the media file
$file = 'file_example'; // string | The actual file
$folder_id = 'folder_id_example'; // string | The ID of the folder the file should be stored in or null string
$project_id = 'project_id_example'; // string | The ID of the project the file belongs in or null string
$title = 'title_example'; // string | Title of the uploaded item
$accept_language = 'accept_language_example'; // string | client language(s)
$private = True; // bool | private files will not be shown in list files endpoint for admin users

try {
    $result = $apiInstance->mediaDefaultPost($session, $alt_text, $file, $folder_id, $project_id, $title, $accept_language, $private);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MediaDefaultApi->mediaDefaultPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **session** | **string**| JWT | |
| **alt_text** | **string**| Alt text for the media file | |
| **file** | **string**| The actual file | |
| **folder_id** | **string**| The ID of the folder the file should be stored in or null string | |
| **project_id** | **string**| The ID of the project the file belongs in or null string | |
| **title** | **string**| Title of the uploaded item | |
| **accept_language** | **string**| client language(s) | [optional] |
| **private** | **bool**| private files will not be shown in list files endpoint for admin users | [optional] |

### Return type

[**\OpenAPI\Client\Model\MediaResponseDefault**](../Model/MediaResponseDefault.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `multipart/form-data`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `mediaDefaultSearchPost()`

```php
mediaDefaultSearchPost($request, $accept_language, $session): \OpenAPI\Client\Model\ModelCursorResponse
```

Create cursor

This endpoint returns a cursor for list medias in default representation with applied filter and sort options. In case of cursor response total will be 0 the status 204 with not content is returned instead.  _accessible without permission_  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\MediaDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$request = new \OpenAPI\Client\Model\MediaCursorRequestDefault(); // \OpenAPI\Client\Model\MediaCursorRequestDefault | options to create cursor
$accept_language = 'accept_language_example'; // string | client language(s)
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->mediaDefaultSearchPost($request, $accept_language, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MediaDefaultApi->mediaDefaultSearchPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **request** | [**\OpenAPI\Client\Model\MediaCursorRequestDefault**](../Model/MediaCursorRequestDefault.md)| options to create cursor | |
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
