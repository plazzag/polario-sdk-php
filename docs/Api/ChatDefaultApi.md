# OpenAPI\Client\ChatDefaultApi



All URIs are relative to https://custom.polario.de/api, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**chatDefaultChannelChannelURLInvitePost()**](ChatDefaultApi.md#chatDefaultChannelChannelURLInvitePost) | **POST** /chat/default/channel/{channelURL}/invite | invite users to protected chat channel |
| [**chatDefaultChannelChannelURLJoinPost()**](ChatDefaultApi.md#chatDefaultChannelChannelURLJoinPost) | **POST** /chat/default/channel/{channelURL}/join | request join for protected chat channel |
| [**chatDefaultChannelChannelURLRequestGet()**](ChatDefaultApi.md#chatDefaultChannelChannelURLRequestGet) | **GET** /chat/default/channel/{channelURL}/request | get requests for chat channel |
| [**chatDefaultChannelChannelURLRequestIdGet()**](ChatDefaultApi.md#chatDefaultChannelChannelURLRequestIdGet) | **GET** /chat/default/channel/{channelURL}/request/{id} | get request of account for chat channel |
| [**chatDefaultChannelChannelURLRequestIdPost()**](ChatDefaultApi.md#chatDefaultChannelChannelURLRequestIdPost) | **POST** /chat/default/channel/{channelURL}/request/{id} | process join request for protected chat channel |
| [**chatDefaultChannelRequestGet()**](ChatDefaultApi.md#chatDefaultChannelRequestGet) | **GET** /chat/default/channel/request | get requests for all chat channels for requesting account |
| [**chatDefaultChannelRequestPost()**](ChatDefaultApi.md#chatDefaultChannelRequestPost) | **POST** /chat/default/channel/request | get requests for chat channels |
| [**chatDefaultFeedIdGet()**](ChatDefaultApi.md#chatDefaultFeedIdGet) | **GET** /chat/default/feed/{id} | Get chat feed |
| [**chatDefaultFeedIdJoinPost()**](ChatDefaultApi.md#chatDefaultFeedIdJoinPost) | **POST** /chat/default/feed/{id}/join | Join chat feed |
| [**chatDefaultFeedProjectIdGet()**](ChatDefaultApi.md#chatDefaultFeedProjectIdGet) | **GET** /chat/default/feed/project/{id} | Get chat feeds of project |


## `chatDefaultChannelChannelURLInvitePost()`

```php
chatDefaultChannelChannelURLInvitePost($channel_url, $session, $request): \OpenAPI\Client\Model\ModelSwagStatusOk
```

invite users to protected chat channel

This endpoint is for inviting users to a protected chat channel In case of response status is 205 the request was only executed partial.  __Note:__ Only operators of the provided sendbird channel can call this endpoint  _accessible without permission_

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\ChatDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$channel_url = 'channel_url_example'; // string | The Sendbird Channel URL
$session = 'session_example'; // string | JWT
$request = array('request_example'); // string[] | Account IDs

try {
    $result = $apiInstance->chatDefaultChannelChannelURLInvitePost($channel_url, $session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ChatDefaultApi->chatDefaultChannelChannelURLInvitePost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **channel_url** | **string**| The Sendbird Channel URL | |
| **session** | **string**| JWT | |
| **request** | [**string[]**](../Model/string.md)| Account IDs | |

### Return type

[**\OpenAPI\Client\Model\ModelSwagStatusOk**](../Model/ModelSwagStatusOk.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `chatDefaultChannelChannelURLJoinPost()`

```php
chatDefaultChannelChannelURLJoinPost($channel_url, $session): \OpenAPI\Client\Model\ModelSwagStatusOk
```

request join for protected chat channel

This endpoint is for joining a protected chat channel  If user is already a member of the channel a http 200 is returned without creating a request.  _accessible without permission_

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\ChatDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$channel_url = 'channel_url_example'; // string | The Sendbird Channel URL
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->chatDefaultChannelChannelURLJoinPost($channel_url, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ChatDefaultApi->chatDefaultChannelChannelURLJoinPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **channel_url** | **string**| The Sendbird Channel URL | |
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

## `chatDefaultChannelChannelURLRequestGet()`

```php
chatDefaultChannelChannelURLRequestGet($channel_url, $session): \OpenAPI\Client\Model\ChannelChatChannelJoinRequestResponse[]
```

get requests for chat channel

This endpoint returns all requests for the requested channel.  __Note:__ Only operators of the provided sendbird channel can call this endpoint  _accessible without permission_

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\ChatDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$channel_url = 'channel_url_example'; // string | The Sendbird Channel URL
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->chatDefaultChannelChannelURLRequestGet($channel_url, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ChatDefaultApi->chatDefaultChannelChannelURLRequestGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **channel_url** | **string**| The Sendbird Channel URL | |
| **session** | **string**| JWT | |

### Return type

[**\OpenAPI\Client\Model\ChannelChatChannelJoinRequestResponse[]**](../Model/ChannelChatChannelJoinRequestResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `chatDefaultChannelChannelURLRequestIdGet()`

```php
chatDefaultChannelChannelURLRequestIdGet($channel_url, $id, $session): \OpenAPI\Client\Model\ChannelChatChannelJoinRequestResponse
```

get request of account for chat channel

This endpoint returns the request of an account for a chat channel.  __Note:__ Only operators of the provided sendbird channel and the requesting accountID can call this endpoint  _accessible without permission_

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\ChatDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$channel_url = 'channel_url_example'; // string | The Sendbird Channel URL
$id = 'id_example'; // string | The ID of the account which should be processed
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->chatDefaultChannelChannelURLRequestIdGet($channel_url, $id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ChatDefaultApi->chatDefaultChannelChannelURLRequestIdGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **channel_url** | **string**| The Sendbird Channel URL | |
| **id** | **string**| The ID of the account which should be processed | |
| **session** | **string**| JWT | |

### Return type

[**\OpenAPI\Client\Model\ChannelChatChannelJoinRequestResponse**](../Model/ChannelChatChannelJoinRequestResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `chatDefaultChannelChannelURLRequestIdPost()`

```php
chatDefaultChannelChannelURLRequestIdPost($channel_url, $id, $session, $request): \OpenAPI\Client\Model\ModelSwagStatusOk
```

process join request for protected chat channel

This endpoint is for processing a joining request for a protected chat channel  __Note:__ Only operators of the provided sendbird channel can call this endpoint  _accessible without permission_

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\ChatDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$channel_url = 'channel_url_example'; // string | The Sendbird Channel URL
$id = 'id_example'; // string | The ID of the account which should be processed
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\ChannelChatChannelRequest(); // \OpenAPI\Client\Model\ChannelChatChannelRequest | action to be performed

try {
    $result = $apiInstance->chatDefaultChannelChannelURLRequestIdPost($channel_url, $id, $session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ChatDefaultApi->chatDefaultChannelChannelURLRequestIdPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **channel_url** | **string**| The Sendbird Channel URL | |
| **id** | **string**| The ID of the account which should be processed | |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\ChannelChatChannelRequest**](../Model/ChannelChatChannelRequest.md)| action to be performed | |

### Return type

[**\OpenAPI\Client\Model\ModelSwagStatusOk**](../Model/ModelSwagStatusOk.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `chatDefaultChannelRequestGet()`

```php
chatDefaultChannelRequestGet($session, $cursor, $limit, $page): \OpenAPI\Client\Model\ChannelChatChannelJoinRequestResponse[]
```

get requests for all chat channels for requesting account

This endpoint returns all pending requests for all channels for the current user. If a limit is set, a cursor for this endpoint may be created to iterate over all pending requests.  _accessible without permission_

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\ChatDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT
$cursor = 'cursor_example'; // string | id of the cursor used for pagination; required if page is set
$limit = 56; // int | amount of results per page (1 ... 100)
$page = 56; // int | current page index of the cursor used for pagination; required if cursor is set

try {
    $result = $apiInstance->chatDefaultChannelRequestGet($session, $cursor, $limit, $page);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ChatDefaultApi->chatDefaultChannelRequestGet: ', $e->getMessage(), PHP_EOL;
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

[**\OpenAPI\Client\Model\ChannelChatChannelJoinRequestResponse[]**](../Model/ChannelChatChannelJoinRequestResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `chatDefaultChannelRequestPost()`

```php
chatDefaultChannelRequestPost($session, $request): \OpenAPI\Client\Model\ChannelChatChannelJoinRequestResponse[]
```

get requests for chat channels

This endpoint returns all requests for the requested channels.  __Note:__ Only operators of the provided sendbird channels can call this endpoint  _accessible without permission_

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\ChatDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\ChannelChatChannelRequestListRequest(); // \OpenAPI\Client\Model\ChannelChatChannelRequestListRequest | channelURLs

try {
    $result = $apiInstance->chatDefaultChannelRequestPost($session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ChatDefaultApi->chatDefaultChannelRequestPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\ChannelChatChannelRequestListRequest**](../Model/ChannelChatChannelRequestListRequest.md)| channelURLs | |

### Return type

[**\OpenAPI\Client\Model\ChannelChatChannelJoinRequestResponse[]**](../Model/ChannelChatChannelJoinRequestResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `chatDefaultFeedIdGet()`

```php
chatDefaultFeedIdGet($id, $accept_language, $session): \OpenAPI\Client\Model\FeedResponseDefault
```

Get chat feed

This endpoint is for retrieving a single chat feed in default representation. If the requested language is not available it will fall back to the default language.  _accessible without permission_  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\ChatDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Chat Feed ID
$accept_language = 'accept_language_example'; // string | client language(s)
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->chatDefaultFeedIdGet($id, $accept_language, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ChatDefaultApi->chatDefaultFeedIdGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Chat Feed ID | |
| **accept_language** | **string**| client language(s) | [optional] |
| **session** | **string**| JWT | [optional] |

### Return type

[**\OpenAPI\Client\Model\FeedResponseDefault**](../Model/FeedResponseDefault.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `chatDefaultFeedIdJoinPost()`

```php
chatDefaultFeedIdJoinPost($id, $session): \OpenAPI\Client\Model\ModelSwagStatusOk
```

Join chat feed

This endpoint is for joining a chat feed.  _accessible without permission_  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\ChatDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Chat Feed ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->chatDefaultFeedIdJoinPost($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ChatDefaultApi->chatDefaultFeedIdJoinPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Chat Feed ID | |
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

## `chatDefaultFeedProjectIdGet()`

```php
chatDefaultFeedProjectIdGet($id, $cursor, $limit, $page, $accept_language, $session): \OpenAPI\Client\Model\FeedResponseDefault[]
```

Get chat feeds of project

This endpoint is for retrieving all chat feeds of a project in default representation. If the requested language is not available it will fall back to the default language. If a limit is set, a cursor for this endpoint may be created to iterate over all chat feeds.  _accessible without permission_  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\ChatDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Project ID
$cursor = 'cursor_example'; // string | id of the cursor used for pagination; required if page is set
$limit = 56; // int | amount of results per page (1 ... 100)
$page = 56; // int | current page index of the cursor used for pagination; required if cursor is set
$accept_language = 'accept_language_example'; // string | client language(s)
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->chatDefaultFeedProjectIdGet($id, $cursor, $limit, $page, $accept_language, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ChatDefaultApi->chatDefaultFeedProjectIdGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Project ID | |
| **cursor** | **string**| id of the cursor used for pagination; required if page is set | [optional] |
| **limit** | **int**| amount of results per page (1 ... 100) | [optional] |
| **page** | **int**| current page index of the cursor used for pagination; required if cursor is set | [optional] |
| **accept_language** | **string**| client language(s) | [optional] |
| **session** | **string**| JWT | [optional] |

### Return type

[**\OpenAPI\Client\Model\FeedResponseDefault[]**](../Model/FeedResponseDefault.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
