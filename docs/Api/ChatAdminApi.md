# OpenAPI\Client\ChatAdminApi



All URIs are relative to https://custom.polario.de/api, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**chatAdminChannelChannelURLDelete()**](ChatAdminApi.md#chatAdminChannelChannelURLDelete) | **DELETE** /chat/admin/channel/{channelURL} | delete a chat channel |
| [**chatAdminChannelGet()**](ChatAdminApi.md#chatAdminChannelGet) | **GET** /chat/admin/channel | Get list of chat channels |
| [**chatAdminFeedIdAccessGet()**](ChatAdminApi.md#chatAdminFeedIdAccessGet) | **GET** /chat/admin/feed/{id}/access | Get chat feed access configuration |
| [**chatAdminFeedIdAccessPatch()**](ChatAdminApi.md#chatAdminFeedIdAccessPatch) | **PATCH** /chat/admin/feed/{id}/access | Update chat feed access configuration |
| [**chatAdminFeedIdDelete()**](ChatAdminApi.md#chatAdminFeedIdDelete) | **DELETE** /chat/admin/feed/{id} | Delete chat feed |
| [**chatAdminFeedIdGet()**](ChatAdminApi.md#chatAdminFeedIdGet) | **GET** /chat/admin/feed/{id} | Get chat feed |
| [**chatAdminFeedIdPatch()**](ChatAdminApi.md#chatAdminFeedIdPatch) | **PATCH** /chat/admin/feed/{id} | Update chat feed |
| [**chatAdminFeedPost()**](ChatAdminApi.md#chatAdminFeedPost) | **POST** /chat/admin/feed | Create chat feed |
| [**chatAdminFeedProjectIdGet()**](ChatAdminApi.md#chatAdminFeedProjectIdGet) | **GET** /chat/admin/feed/project/{id} | Get chat feeds of project |
| [**chatAdminFeedSyncPut()**](ChatAdminApi.md#chatAdminFeedSyncPut) | **PUT** /chat/admin/feed/sync | Sync Operators for all chat feeds |


## `chatAdminChannelChannelURLDelete()`

```php
chatAdminChannelChannelURLDelete($channel_url, $session): \OpenAPI\Client\Model\ModelSwagStatusOk
```

delete a chat channel

This endpoint is for deleting a single chat channel.  _only accessible with admin role_

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\ChatAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$channel_url = 'channel_url_example'; // string | The Sendbird Channel ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->chatAdminChannelChannelURLDelete($channel_url, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ChatAdminApi->chatAdminChannelChannelURLDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **channel_url** | **string**| The Sendbird Channel ID | |
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

## `chatAdminChannelGet()`

```php
chatAdminChannelGet($session, $cursor, $limit, $page): \OpenAPI\Client\Model\ChannelChatChannelsResponse[]
```

Get list of chat channels

This endpoint is for getting list of all chat channels. If a limit is set, a cursor for this endpoint may be created to iterate over all chat channels.  _only accessible with admin role_

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\ChatAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT
$cursor = 'cursor_example'; // string | id of the cursor used for pagination; required if page is set
$limit = 56; // int | amount of results per page (1 ... 100)
$page = 56; // int | current page index of the cursor used for pagination; required if cursor is set

try {
    $result = $apiInstance->chatAdminChannelGet($session, $cursor, $limit, $page);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ChatAdminApi->chatAdminChannelGet: ', $e->getMessage(), PHP_EOL;
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

[**\OpenAPI\Client\Model\ChannelChatChannelsResponse[]**](../Model/ChannelChatChannelsResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `chatAdminFeedIdAccessGet()`

```php
chatAdminFeedIdAccessGet($id, $session): \OpenAPI\Client\Model\AuthorizationAccessResponse
```

Get chat feed access configuration

This endpoint returns the access configuration for the requested chat feed.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\ChatAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | ChatFeed ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->chatAdminFeedIdAccessGet($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ChatAdminApi->chatAdminFeedIdAccessGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| ChatFeed ID | |
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

## `chatAdminFeedIdAccessPatch()`

```php
chatAdminFeedIdAccessPatch($id, $session, $request): \OpenAPI\Client\Model\ModelAccess
```

Update chat feed access configuration

This endpoint updates the access configuration for the requested chat feed. Only the changes should be transmitted due this endpoint.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\ChatAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | ChatFeed ID
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\ModelAccess(); // \OpenAPI\Client\Model\ModelAccess | changed access rights

try {
    $result = $apiInstance->chatAdminFeedIdAccessPatch($id, $session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ChatAdminApi->chatAdminFeedIdAccessPatch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| ChatFeed ID | |
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

## `chatAdminFeedIdDelete()`

```php
chatAdminFeedIdDelete($id, $session): \OpenAPI\Client\Model\ModelSwagStatusOk
```

Delete chat feed

This endpoint is for deleting a single chat feed.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\ChatAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Form ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->chatAdminFeedIdDelete($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ChatAdminApi->chatAdminFeedIdDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Form ID | |
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

## `chatAdminFeedIdGet()`

```php
chatAdminFeedIdGet($id, $session): \OpenAPI\Client\Model\FeedResponseAdmin
```

Get chat feed

This endpoint is for retrieving a single chat feed in admin representation.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\ChatAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Chat Feed ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->chatAdminFeedIdGet($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ChatAdminApi->chatAdminFeedIdGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Chat Feed ID | |
| **session** | **string**| JWT | |

### Return type

[**\OpenAPI\Client\Model\FeedResponseAdmin**](../Model/FeedResponseAdmin.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `chatAdminFeedIdPatch()`

```php
chatAdminFeedIdPatch($id, $session, $request): \OpenAPI\Client\Model\FeedResponseAdmin
```

Update chat feed

This endpoint is for updating an existing chat feed  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\ChatAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Chat Feed ID
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\FeedPatchRequest(); // \OpenAPI\Client\Model\FeedPatchRequest | chat feed data to update

try {
    $result = $apiInstance->chatAdminFeedIdPatch($id, $session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ChatAdminApi->chatAdminFeedIdPatch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Chat Feed ID | |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\FeedPatchRequest**](../Model/FeedPatchRequest.md)| chat feed data to update | |

### Return type

[**\OpenAPI\Client\Model\FeedResponseAdmin**](../Model/FeedResponseAdmin.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `chatAdminFeedPost()`

```php
chatAdminFeedPost($session, $request): \OpenAPI\Client\Model\FeedResponseAdmin
```

Create chat feed

This endpoint is for creating a new chat feed.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\ChatAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\FeedPostRequest(); // \OpenAPI\Client\Model\FeedPostRequest | Chat-Feed to create

try {
    $result = $apiInstance->chatAdminFeedPost($session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ChatAdminApi->chatAdminFeedPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\FeedPostRequest**](../Model/FeedPostRequest.md)| Chat-Feed to create | |

### Return type

[**\OpenAPI\Client\Model\FeedResponseAdmin**](../Model/FeedResponseAdmin.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `chatAdminFeedProjectIdGet()`

```php
chatAdminFeedProjectIdGet($id, $session, $cursor, $limit, $page): \OpenAPI\Client\Model\FeedResponseListAdmin[]
```

Get chat feeds of project

This endpoint is for retrieving all chat feeds of a project in admin representation. If a limit is set, a cursor for this endpoint may be created to iterate over all chat feeds.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\ChatAdminApi(
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
    $result = $apiInstance->chatAdminFeedProjectIdGet($id, $session, $cursor, $limit, $page);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ChatAdminApi->chatAdminFeedProjectIdGet: ', $e->getMessage(), PHP_EOL;
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

[**\OpenAPI\Client\Model\FeedResponseListAdmin[]**](../Model/FeedResponseListAdmin.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `chatAdminFeedSyncPut()`

```php
chatAdminFeedSyncPut($session): \OpenAPI\Client\Model\ModelSwagStatusOk
```

Sync Operators for all chat feeds

This endpoint is sync operators for all chat feeds with sendbird. This endpoint should be rarely used, because of its workload.  _only accessible with permission_ : `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\ChatAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->chatAdminFeedSyncPut($session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ChatAdminApi->chatAdminFeedSyncPut: ', $e->getMessage(), PHP_EOL;
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
