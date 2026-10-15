# OpenAPI\Client\GamificationDefaultApi



All URIs are relative to https://custom.polario.de/api, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**reactionDefaultGamificationActionPost()**](GamificationDefaultApi.md#reactionDefaultGamificationActionPost) | **POST** /reaction/default/gamification/action | Score gamification action |
| [**reactionDefaultGamificationEntryGet()**](GamificationDefaultApi.md#reactionDefaultGamificationEntryGet) | **GET** /reaction/default/gamification/entry | Get leaderboard entry list |
| [**reactionDefaultGamificationEntrySearchPost()**](GamificationDefaultApi.md#reactionDefaultGamificationEntrySearchPost) | **POST** /reaction/default/gamification/entry/search | Create cursor leaderboard entries |
| [**reactionDefaultGamificationLeaderboardIdAccountAccountIdGet()**](GamificationDefaultApi.md#reactionDefaultGamificationLeaderboardIdAccountAccountIdGet) | **GET** /reaction/default/gamification/leaderboard/{id}/account/{accountId} | Get leaderboard entry for own account |
| [**reactionDefaultGamificationLeaderboardIdGet()**](GamificationDefaultApi.md#reactionDefaultGamificationLeaderboardIdGet) | **GET** /reaction/default/gamification/leaderboard/{id} | Get leaderboard |
| [**reactionDefaultGamificationLeaderboardProjectProjectIdGet()**](GamificationDefaultApi.md#reactionDefaultGamificationLeaderboardProjectProjectIdGet) | **GET** /reaction/default/gamification/leaderboard/project/{projectId} | Get leaderboard list for project |
| [**reactionDefaultGamificationProjectProjectIdSettingsGet()**](GamificationDefaultApi.md#reactionDefaultGamificationProjectProjectIdSettingsGet) | **GET** /reaction/default/gamification/project/{projectId}/settings | Get project settings |


## `reactionDefaultGamificationActionPost()`

```php
reactionDefaultGamificationActionPost($session, $request): \OpenAPI\Client\Model\GamificationActionResponse
```

Score gamification action

This endpoint scores a gamification action for the requesting account. Project-related actions score only in their related projects, including linked projects for news. Actions without a project score across all projects. Actions do not score while gamification is disabled or paused for the project.  __Note:__ Gamification is a premium feature and requires a valid subscription.  _accessible without permission_

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\GamificationDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\GamificationActionRequest(); // \OpenAPI\Client\Model\GamificationActionRequest | Action to score

try {
    $result = $apiInstance->reactionDefaultGamificationActionPost($session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GamificationDefaultApi->reactionDefaultGamificationActionPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\GamificationActionRequest**](../Model/GamificationActionRequest.md)| Action to score | |

### Return type

[**\OpenAPI\Client\Model\GamificationActionResponse**](../Model/GamificationActionResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `reactionDefaultGamificationEntryGet()`

```php
reactionDefaultGamificationEntryGet($cursor, $page, $session, $limit): \OpenAPI\Client\Model\GamificationleaderboardentryResponse[]
```

Get leaderboard entry list

This endpoint returns an array of leaderboard entries for a cursor. The output is in default representation and filtered for the user permissions.  Cursor could be created here: POST /reaction/default/gamification/entry/search  __Note:__ Gamification is a premium feature and requires a valid subscription.  _accessible without permission_

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\GamificationDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$cursor = 'cursor_example'; // string | id of the cursor used for pagination; required if page is set
$page = 56; // int | current page index of the cursor used for pagination; required if cursor is set
$session = 'session_example'; // string | JWT
$limit = 56; // int | amount of results per page (1 ... 100)

try {
    $result = $apiInstance->reactionDefaultGamificationEntryGet($cursor, $page, $session, $limit);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GamificationDefaultApi->reactionDefaultGamificationEntryGet: ', $e->getMessage(), PHP_EOL;
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

[**\OpenAPI\Client\Model\GamificationleaderboardentryResponse[]**](../Model/GamificationleaderboardentryResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `reactionDefaultGamificationEntrySearchPost()`

```php
reactionDefaultGamificationEntrySearchPost($session, $request): \OpenAPI\Client\Model\PaginationCursorResponse
```

Create cursor leaderboard entries

This endpoint returns a cursor for list leaderboard entries in default representation with applied filter and sort options. In case of cursor response total will be 0 the status 204 with not content is returned instead.  __Note:__ Gamification is a premium feature and requires a valid subscription.  _accessible without permission_

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\GamificationDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\GamificationleaderboardentryCursorRequestDefault(); // \OpenAPI\Client\Model\GamificationleaderboardentryCursorRequestDefault | options to create cursor

try {
    $result = $apiInstance->reactionDefaultGamificationEntrySearchPost($session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GamificationDefaultApi->reactionDefaultGamificationEntrySearchPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\GamificationleaderboardentryCursorRequestDefault**](../Model/GamificationleaderboardentryCursorRequestDefault.md)| options to create cursor | |

### Return type

[**\OpenAPI\Client\Model\PaginationCursorResponse**](../Model/PaginationCursorResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `reactionDefaultGamificationLeaderboardIdAccountAccountIdGet()`

```php
reactionDefaultGamificationLeaderboardIdAccountAccountIdGet($id, $account_id, $session): \OpenAPI\Client\Model\GamificationleaderboardentryResponse
```

Get leaderboard entry for own account

This endpoint returns the leaderboard entry for the authenticated account in the given leaderboard.  __Note:__ Gamification is a premium feature and requires a valid subscription.  _accessible without permission_ (can only be used for the own account. Session must match requested account id.)

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\GamificationDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Leaderboard ID
$account_id = 'account_id_example'; // string | Account ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->reactionDefaultGamificationLeaderboardIdAccountAccountIdGet($id, $account_id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GamificationDefaultApi->reactionDefaultGamificationLeaderboardIdAccountAccountIdGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Leaderboard ID | |
| **account_id** | **string**| Account ID | |
| **session** | **string**| JWT | |

### Return type

[**\OpenAPI\Client\Model\GamificationleaderboardentryResponse**](../Model/GamificationleaderboardentryResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `reactionDefaultGamificationLeaderboardIdGet()`

```php
reactionDefaultGamificationLeaderboardIdGet($id, $session): \OpenAPI\Client\Model\GamificationleaderboardResponseDefault
```

Get leaderboard

This endpoint returns a leaderboard in default representation by given id.  __Note:__ Gamification is a premium feature and requires a valid subscription.  _accessible without permission_  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\GamificationDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Leaderboard ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->reactionDefaultGamificationLeaderboardIdGet($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GamificationDefaultApi->reactionDefaultGamificationLeaderboardIdGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Leaderboard ID | |
| **session** | **string**| JWT | [optional] |

### Return type

[**\OpenAPI\Client\Model\GamificationleaderboardResponseDefault**](../Model/GamificationleaderboardResponseDefault.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `reactionDefaultGamificationLeaderboardProjectProjectIdGet()`

```php
reactionDefaultGamificationLeaderboardProjectProjectIdGet($project_id, $cursor, $limit, $page, $session): \OpenAPI\Client\Model\GamificationleaderboardResponseDefault[]
```

Get leaderboard list for project

This endpoint returns a list of all leaderboard for the requested project in default representation. If a limit is set, a cursor for this endpoint may be created to iterate over all leaderboards.  __Note:__ Gamification is a premium feature and requires a valid subscription.  _accessible without permission_  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\GamificationDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$project_id = 'project_id_example'; // string | Project ID
$cursor = 'cursor_example'; // string | id of the cursor used for pagination; required if page is set
$limit = 56; // int | amount of results per page (1 ... 100)
$page = 56; // int | current page index of the cursor used for pagination; required if cursor is set
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->reactionDefaultGamificationLeaderboardProjectProjectIdGet($project_id, $cursor, $limit, $page, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GamificationDefaultApi->reactionDefaultGamificationLeaderboardProjectProjectIdGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **project_id** | **string**| Project ID | |
| **cursor** | **string**| id of the cursor used for pagination; required if page is set | [optional] |
| **limit** | **int**| amount of results per page (1 ... 100) | [optional] |
| **page** | **int**| current page index of the cursor used for pagination; required if cursor is set | [optional] |
| **session** | **string**| JWT | [optional] |

### Return type

[**\OpenAPI\Client\Model\GamificationleaderboardResponseDefault[]**](../Model/GamificationleaderboardResponseDefault.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `reactionDefaultGamificationProjectProjectIdSettingsGet()`

```php
reactionDefaultGamificationProjectProjectIdSettingsGet($project_id, $session): \OpenAPI\Client\Model\ModelProjectGamificationSettings
```

Get project settings

This endpoint returns the gamification settings in default representation by given project id.  __Note:__ Gamification is a premium feature and requires a valid subscription.  _accessible without permission_  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\GamificationDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$project_id = 'project_id_example'; // string | Project ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->reactionDefaultGamificationProjectProjectIdSettingsGet($project_id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GamificationDefaultApi->reactionDefaultGamificationProjectProjectIdSettingsGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **project_id** | **string**| Project ID | |
| **session** | **string**| JWT | [optional] |

### Return type

[**\OpenAPI\Client\Model\ModelProjectGamificationSettings**](../Model/ModelProjectGamificationSettings.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
