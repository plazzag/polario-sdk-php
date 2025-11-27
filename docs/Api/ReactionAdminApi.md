# OpenAPI\Client\ReactionAdminApi



All URIs are relative to https://custom.polario.de/api, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**reactionAdminObjectTypeGet()**](ReactionAdminApi.md#reactionAdminObjectTypeGet) | **GET** /reaction/admin/{objectType} | Get reactions of type |
| [**reactionAdminObjectTypeSearchPost()**](ReactionAdminApi.md#reactionAdminObjectTypeSearchPost) | **POST** /reaction/admin/{objectType}/search | Create cursor |


## `reactionAdminObjectTypeGet()`

```php
reactionAdminObjectTypeGet($object_type, $session, $cursor, $limit, $page): \OpenAPI\Client\Model\ReactionResponseListAdmin[]
```

Get reactions of type

Currently the objects of type page and news are supported. If a limit is set, a cursor for this endpoint may be created to iterate over all reactions.  _accessible without permission_  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageGlobalMedia\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\ReactionAdminApi(
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
    $result = $apiInstance->reactionAdminObjectTypeGet($object_type, $session, $cursor, $limit, $page);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReactionAdminApi->reactionAdminObjectTypeGet: ', $e->getMessage(), PHP_EOL;
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

[**\OpenAPI\Client\Model\ReactionResponseListAdmin[]**](../Model/ReactionResponseListAdmin.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `reactionAdminObjectTypeSearchPost()`

```php
reactionAdminObjectTypeSearchPost($object_type, $session, $request): \OpenAPI\Client\Model\ModelCursorResponse
```

Create cursor

This endpoint returns a cursor for list reactions in admin representation with applied filter. In case of cursor response total will be 0 the status 204 with not content is returned instead.  _accessible without permission_  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\ReactionAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$object_type = 'object_type_example'; // string | object type
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\ReactionCursorObjectIDsRequest(); // \OpenAPI\Client\Model\ReactionCursorObjectIDsRequest | options to create cursor

try {
    $result = $apiInstance->reactionAdminObjectTypeSearchPost($object_type, $session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReactionAdminApi->reactionAdminObjectTypeSearchPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **object_type** | **string**| object type | |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\ReactionCursorObjectIDsRequest**](../Model/ReactionCursorObjectIDsRequest.md)| options to create cursor | |

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
