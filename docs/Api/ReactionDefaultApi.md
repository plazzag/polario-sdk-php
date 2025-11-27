# OpenAPI\Client\ReactionDefaultApi



All URIs are relative to https://custom.polario.de/api, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**reactionDefaultBookmarkGet()**](ReactionDefaultApi.md#reactionDefaultBookmarkGet) | **GET** /reaction/default/bookmark | Get bookmarks for current user |
| [**reactionDefaultBookmarkObjectTypeGet()**](ReactionDefaultApi.md#reactionDefaultBookmarkObjectTypeGet) | **GET** /reaction/default/bookmark/{objectType} | Get bookmarks for object type |
| [**reactionDefaultBookmarkObjectTypeObjectIdDelete()**](ReactionDefaultApi.md#reactionDefaultBookmarkObjectTypeObjectIdDelete) | **DELETE** /reaction/default/bookmark/{objectType}/{objectId} | Delete a bookmark |
| [**reactionDefaultBookmarkObjectTypeObjectIdGet()**](ReactionDefaultApi.md#reactionDefaultBookmarkObjectTypeObjectIdGet) | **GET** /reaction/default/bookmark/{objectType}/{objectId} | Get bookmark of object for your account |
| [**reactionDefaultBookmarkObjectTypeObjectIdPost()**](ReactionDefaultApi.md#reactionDefaultBookmarkObjectTypeObjectIdPost) | **POST** /reaction/default/bookmark/{objectType}/{objectId} | Create a bookmark |
| [**reactionDefaultObjectTypeGet()**](ReactionDefaultApi.md#reactionDefaultObjectTypeGet) | **GET** /reaction/default/{objectType} | Get reactions of type |
| [**reactionDefaultObjectTypeObjectIdDelete()**](ReactionDefaultApi.md#reactionDefaultObjectTypeObjectIdDelete) | **DELETE** /reaction/default/{objectType}/{objectId} | Delete your reaction |
| [**reactionDefaultObjectTypeObjectIdGet()**](ReactionDefaultApi.md#reactionDefaultObjectTypeObjectIdGet) | **GET** /reaction/default/{objectType}/{objectId} | Get reactions of object |
| [**reactionDefaultObjectTypeObjectIdPost()**](ReactionDefaultApi.md#reactionDefaultObjectTypeObjectIdPost) | **POST** /reaction/default/{objectType}/{objectId} | Create or update your reaction |
| [**reactionDefaultObjectTypeSearchPost()**](ReactionDefaultApi.md#reactionDefaultObjectTypeSearchPost) | **POST** /reaction/default/{objectType}/search | Create cursor |


## `reactionDefaultBookmarkGet()`

```php
reactionDefaultBookmarkGet($session, $cursor, $limit, $page): \OpenAPI\Client\Model\BookmarkResponse[]
```

Get bookmarks for current user

This endpoint is for retrieving all bookmarks of the own account. If a limit is set, a cursor for this endpoint may be created to iterate over all bookmarks.  _accessible without permission_

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\ReactionDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT
$cursor = 'cursor_example'; // string | id of the cursor used for pagination; required if page is set
$limit = 56; // int | amount of results per page (1 ... 100)
$page = 56; // int | current page index of the cursor used for pagination; required if cursor is set

try {
    $result = $apiInstance->reactionDefaultBookmarkGet($session, $cursor, $limit, $page);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReactionDefaultApi->reactionDefaultBookmarkGet: ', $e->getMessage(), PHP_EOL;
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

[**\OpenAPI\Client\Model\BookmarkResponse[]**](../Model/BookmarkResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `reactionDefaultBookmarkObjectTypeGet()`

```php
reactionDefaultBookmarkObjectTypeGet($object_type, $session, $cursor, $limit, $page): \OpenAPI\Client\Model\BookmarkResponse[]
```

Get bookmarks for object type

Bookmarks are not available for rows of dynamic directory entries. If a limit is set, a cursor for this endpoint may be created to iterate over all bookmarks.  _accessible without permission_

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\ReactionDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$object_type = 'object_type_example'; // string | object type
$session = 'session_example'; // string | JWT
$cursor = 'cursor_example'; // string | id of the cursor used for pagination; required if page is set
$limit = 56; // int | amount of results per page (1 ... 100)
$page = 56; // int | current page index of the cursor used for pagination; required if cursor is set

try {
    $result = $apiInstance->reactionDefaultBookmarkObjectTypeGet($object_type, $session, $cursor, $limit, $page);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReactionDefaultApi->reactionDefaultBookmarkObjectTypeGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **object_type** | **string**| object type | |
| **session** | **string**| JWT | |
| **cursor** | **string**| id of the cursor used for pagination; required if page is set | [optional] |
| **limit** | **int**| amount of results per page (1 ... 100) | [optional] |
| **page** | **int**| current page index of the cursor used for pagination; required if cursor is set | [optional] |

### Return type

[**\OpenAPI\Client\Model\BookmarkResponse[]**](../Model/BookmarkResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `reactionDefaultBookmarkObjectTypeObjectIdDelete()`

```php
reactionDefaultBookmarkObjectTypeObjectIdDelete($object_type, $object_id, $session): \OpenAPI\Client\Model\ModelSwagStatusOk
```

Delete a bookmark

This endpoint is for deleting a bookmark from the system  _accessible without permission_

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\ReactionDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$object_type = 'object_type_example'; // string | object type
$object_id = 'object_id_example'; // string | object ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->reactionDefaultBookmarkObjectTypeObjectIdDelete($object_type, $object_id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReactionDefaultApi->reactionDefaultBookmarkObjectTypeObjectIdDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **object_type** | **string**| object type | |
| **object_id** | **string**| object ID | |
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

## `reactionDefaultBookmarkObjectTypeObjectIdGet()`

```php
reactionDefaultBookmarkObjectTypeObjectIdGet($object_type, $object_id, $session): \OpenAPI\Client\Model\BookmarkResponse
```

Get bookmark of object for your account

This endpoint is for retrieving the bookmark status for the requested object. Bookmarks are not available for rows of dynamic directory entries.  _accessible without permission_

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\ReactionDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$object_type = 'object_type_example'; // string | object type
$object_id = 'object_id_example'; // string | object ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->reactionDefaultBookmarkObjectTypeObjectIdGet($object_type, $object_id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReactionDefaultApi->reactionDefaultBookmarkObjectTypeObjectIdGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **object_type** | **string**| object type | |
| **object_id** | **string**| object ID | |
| **session** | **string**| JWT | |

### Return type

[**\OpenAPI\Client\Model\BookmarkResponse**](../Model/BookmarkResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `reactionDefaultBookmarkObjectTypeObjectIdPost()`

```php
reactionDefaultBookmarkObjectTypeObjectIdPost($object_type, $object_id, $session): \OpenAPI\Client\Model\BookmarkResponse
```

Create a bookmark

This endpoint is for creating a bookmark. Bookmarks are not available for rows of dynamic directory entries.  _accessible without permission_  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"` `\"ManageGlobalMedia\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\ReactionDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$object_type = 'object_type_example'; // string | object type
$object_id = 'object_id_example'; // string | object ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->reactionDefaultBookmarkObjectTypeObjectIdPost($object_type, $object_id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReactionDefaultApi->reactionDefaultBookmarkObjectTypeObjectIdPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **object_type** | **string**| object type | |
| **object_id** | **string**| object ID | |
| **session** | **string**| JWT | |

### Return type

[**\OpenAPI\Client\Model\BookmarkResponse**](../Model/BookmarkResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `reactionDefaultObjectTypeGet()`

```php
reactionDefaultObjectTypeGet($object_type, $session, $cursor, $limit, $page): array<string,array>
```

Get reactions of type

Currently the objects of type page and news are supported. If a limit is set, a cursor for this endpoint may be created to iterate over all reactions.  _accessible without permission_  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageGlobalMedia\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\ReactionDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$object_type = 'object_type_example'; // string | object type
$session = 'session_example'; // string | JWT
$cursor = 'cursor_example'; // string | id of the cursor used for pagination; required if page is set
$limit = 56; // int | amount of results per page (1 ... 100)
$page = 56; // int | current page index of the cursor used for pagination; required if cursor is set

try {
    $result = $apiInstance->reactionDefaultObjectTypeGet($object_type, $session, $cursor, $limit, $page);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReactionDefaultApi->reactionDefaultObjectTypeGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **object_type** | **string**| object type | |
| **session** | **string**| JWT | |
| **cursor** | **string**| id of the cursor used for pagination; required if page is set | [optional] |
| **limit** | **int**| amount of results per page (1 ... 100) | [optional] |
| **page** | **int**| current page index of the cursor used for pagination; required if cursor is set | [optional] |

### Return type

**array<string,array>**

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `reactionDefaultObjectTypeObjectIdDelete()`

```php
reactionDefaultObjectTypeObjectIdDelete($object_type, $object_id, $session): \OpenAPI\Client\Model\GitPlazzNetReposSandmannBackendServicesReactionReactionResponseDefault
```

Delete your reaction

This endpoint is for deleting your reaction of a system object. This is only possible if the interaction on this object is allowed. Currently the objects of type page and news are supported.  _accessible without permission_

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\ReactionDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$object_type = 'object_type_example'; // string | object type
$object_id = 'object_id_example'; // string | object ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->reactionDefaultObjectTypeObjectIdDelete($object_type, $object_id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReactionDefaultApi->reactionDefaultObjectTypeObjectIdDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **object_type** | **string**| object type | |
| **object_id** | **string**| object ID | |
| **session** | **string**| JWT | |

### Return type

[**\OpenAPI\Client\Model\GitPlazzNetReposSandmannBackendServicesReactionReactionResponseDefault**](../Model/GitPlazzNetReposSandmannBackendServicesReactionReactionResponseDefault.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `reactionDefaultObjectTypeObjectIdGet()`

```php
reactionDefaultObjectTypeObjectIdGet($object_type, $object_id, $session): \OpenAPI\Client\Model\GitPlazzNetReposSandmannBackendServicesReactionReactionResponseDefault
```

Get reactions of object

This is only possible if the interaction on this object is allowed. Currently the objects of type page and news are supported.  _accessible without permission_  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\ReactionDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$object_type = 'object_type_example'; // string | object type
$object_id = 'object_id_example'; // string | object ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->reactionDefaultObjectTypeObjectIdGet($object_type, $object_id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReactionDefaultApi->reactionDefaultObjectTypeObjectIdGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **object_type** | **string**| object type | |
| **object_id** | **string**| object ID | |
| **session** | **string**| JWT | |

### Return type

[**\OpenAPI\Client\Model\GitPlazzNetReposSandmannBackendServicesReactionReactionResponseDefault**](../Model/GitPlazzNetReposSandmannBackendServicesReactionReactionResponseDefault.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `reactionDefaultObjectTypeObjectIdPost()`

```php
reactionDefaultObjectTypeObjectIdPost($object_type, $object_id, $session, $request): \OpenAPI\Client\Model\GitPlazzNetReposSandmannBackendServicesReactionReactionResponseDefault
```

Create or update your reaction

This endpoint is for creating or updating your reaction of a system object. This is only possible if the interaction on this object is allowed. Currently the objects of type Page and News are supported.  _accessible without permission_  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\ReactionDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$object_type = 'object_type_example'; // string | object type
$object_id = 'object_id_example'; // string | object ID
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\ReactionPostReactionRequest(); // \OpenAPI\Client\Model\ReactionPostReactionRequest | the configuration of your reaction

try {
    $result = $apiInstance->reactionDefaultObjectTypeObjectIdPost($object_type, $object_id, $session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReactionDefaultApi->reactionDefaultObjectTypeObjectIdPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **object_type** | **string**| object type | |
| **object_id** | **string**| object ID | |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\ReactionPostReactionRequest**](../Model/ReactionPostReactionRequest.md)| the configuration of your reaction | |

### Return type

[**\OpenAPI\Client\Model\GitPlazzNetReposSandmannBackendServicesReactionReactionResponseDefault**](../Model/GitPlazzNetReposSandmannBackendServicesReactionReactionResponseDefault.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `reactionDefaultObjectTypeSearchPost()`

```php
reactionDefaultObjectTypeSearchPost($object_type, $request, $session): \OpenAPI\Client\Model\ModelCursorResponse
```

Create cursor

This endpoint returns a cursor for list reactions in default representation with applied filter. In case of cursor response total will be 0 the status 204 with not content is returned instead.  _accessible without permission_  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\ReactionDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$object_type = 'object_type_example'; // string | object type
$request = new \OpenAPI\Client\Model\ReactionCursorObjectIDsRequest(); // \OpenAPI\Client\Model\ReactionCursorObjectIDsRequest | options to create cursor
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->reactionDefaultObjectTypeSearchPost($object_type, $request, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReactionDefaultApi->reactionDefaultObjectTypeSearchPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **object_type** | **string**| object type | |
| **request** | [**\OpenAPI\Client\Model\ReactionCursorObjectIDsRequest**](../Model/ReactionCursorObjectIDsRequest.md)| options to create cursor | |
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
