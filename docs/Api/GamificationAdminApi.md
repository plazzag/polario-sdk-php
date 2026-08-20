# OpenAPI\Client\GamificationAdminApi



All URIs are relative to https://custom.polario.de/api, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**reactionAdminGamificationBalanceGet()**](GamificationAdminApi.md#reactionAdminGamificationBalanceGet) | **GET** /reaction/admin/gamification/balance | Get gamification balance entry list |
| [**reactionAdminGamificationBalanceSearchPost()**](GamificationAdminApi.md#reactionAdminGamificationBalanceSearchPost) | **POST** /reaction/admin/gamification/balance/search | Create cursor gamification balance entries |
| [**reactionAdminGamificationEntryGet()**](GamificationAdminApi.md#reactionAdminGamificationEntryGet) | **GET** /reaction/admin/gamification/entry | Get leaderboard entry list |
| [**reactionAdminGamificationEntrySearchPost()**](GamificationAdminApi.md#reactionAdminGamificationEntrySearchPost) | **POST** /reaction/admin/gamification/entry/search | Create cursor leaderboard entries |
| [**reactionAdminGamificationLeaderboardIdAccountAccountIdBonusPost()**](GamificationAdminApi.md#reactionAdminGamificationLeaderboardIdAccountAccountIdBonusPost) | **POST** /reaction/admin/gamification/leaderboard/{id}/account/{accountId}/bonus | Add gamification bonus |
| [**reactionAdminGamificationLeaderboardIdAccountAccountIdResetPut()**](GamificationAdminApi.md#reactionAdminGamificationLeaderboardIdAccountAccountIdResetPut) | **PUT** /reaction/admin/gamification/leaderboard/{id}/account/{accountId}/reset | Reset account gamification balance |
| [**reactionAdminGamificationLeaderboardIdGet()**](GamificationAdminApi.md#reactionAdminGamificationLeaderboardIdGet) | **GET** /reaction/admin/gamification/leaderboard/{id} | Get leaderboard |
| [**reactionAdminGamificationLeaderboardIdPatch()**](GamificationAdminApi.md#reactionAdminGamificationLeaderboardIdPatch) | **PATCH** /reaction/admin/gamification/leaderboard/{id} | Update leaderboard |
| [**reactionAdminGamificationLeaderboardIdResetPut()**](GamificationAdminApi.md#reactionAdminGamificationLeaderboardIdResetPut) | **PUT** /reaction/admin/gamification/leaderboard/{id}/reset | Reset gamification balance |
| [**reactionAdminGamificationLeaderboardIdSyncPut()**](GamificationAdminApi.md#reactionAdminGamificationLeaderboardIdSyncPut) | **PUT** /reaction/admin/gamification/leaderboard/{id}/sync | Sync gamification balance |
| [**reactionAdminGamificationLeaderboardProjectProjectIdGet()**](GamificationAdminApi.md#reactionAdminGamificationLeaderboardProjectProjectIdGet) | **GET** /reaction/admin/gamification/leaderboard/project/{projectId} | Get leaderboard list for project |
| [**reactionAdminGamificationProjectProjectIdSettingsGet()**](GamificationAdminApi.md#reactionAdminGamificationProjectProjectIdSettingsGet) | **GET** /reaction/admin/gamification/project/{projectId}/settings | Get project settings |
| [**reactionAdminGamificationProjectProjectIdSettingsPut()**](GamificationAdminApi.md#reactionAdminGamificationProjectProjectIdSettingsPut) | **PUT** /reaction/admin/gamification/project/{projectId}/settings | Get project settings |
| [**reactionAdminGamificationRuleGet()**](GamificationAdminApi.md#reactionAdminGamificationRuleGet) | **GET** /reaction/admin/gamification/rule | Get gamification rule list |
| [**reactionAdminGamificationRuleIdDelete()**](GamificationAdminApi.md#reactionAdminGamificationRuleIdDelete) | **DELETE** /reaction/admin/gamification/rule/{id} | Delete gamification rule |
| [**reactionAdminGamificationRuleIdGet()**](GamificationAdminApi.md#reactionAdminGamificationRuleIdGet) | **GET** /reaction/admin/gamification/rule/{id} | Get gamification rule |
| [**reactionAdminGamificationRuleIdPatch()**](GamificationAdminApi.md#reactionAdminGamificationRuleIdPatch) | **PATCH** /reaction/admin/gamification/rule/{id} | Update gamification rule |
| [**reactionAdminGamificationRulePost()**](GamificationAdminApi.md#reactionAdminGamificationRulePost) | **POST** /reaction/admin/gamification/rule | Create gamification rule |
| [**reactionAdminGamificationRuleSearchPost()**](GamificationAdminApi.md#reactionAdminGamificationRuleSearchPost) | **POST** /reaction/admin/gamification/rule/search | Create cursor gamification rules |


## `reactionAdminGamificationBalanceGet()`

```php
reactionAdminGamificationBalanceGet($cursor, $page, $session, $limit): \OpenAPI\Client\Model\GamificationbalanceResponse[]
```

Get gamification balance entry list

This endpoint returns an array of all gamification balance entries for a cursor. The output is in administrative representation and filtered for the user permissions.  Cursor could be created here: POST /reaction/admin/gamification/balance/search  __Note:__ Gamification is a premium feature and requires a valid subscription.  _accessible without permission_

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\GamificationAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$cursor = 'cursor_example'; // string | id of the cursor used for pagination; required if page is set
$page = 56; // int | current page index of the cursor used for pagination; required if cursor is set
$session = 'session_example'; // string | JWT
$limit = 56; // int | amount of results per page (1 ... 100)

try {
    $result = $apiInstance->reactionAdminGamificationBalanceGet($cursor, $page, $session, $limit);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GamificationAdminApi->reactionAdminGamificationBalanceGet: ', $e->getMessage(), PHP_EOL;
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

[**\OpenAPI\Client\Model\GamificationbalanceResponse[]**](../Model/GamificationbalanceResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `reactionAdminGamificationBalanceSearchPost()`

```php
reactionAdminGamificationBalanceSearchPost($session, $request): \OpenAPI\Client\Model\ModelCursorResponse
```

Create cursor gamification balance entries

This endpoint returns a cursor for list gamification balance entries in admin representation with applied filter and sort options. In case of cursor response total will be 0 the status 204 with not content is returned instead.  __Note:__ Gamification is a premium feature and requires a valid subscription.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\GamificationAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\GamificationbalanceCursorRequest(); // \OpenAPI\Client\Model\GamificationbalanceCursorRequest | options to create cursor

try {
    $result = $apiInstance->reactionAdminGamificationBalanceSearchPost($session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GamificationAdminApi->reactionAdminGamificationBalanceSearchPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\GamificationbalanceCursorRequest**](../Model/GamificationbalanceCursorRequest.md)| options to create cursor | |

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

## `reactionAdminGamificationEntryGet()`

```php
reactionAdminGamificationEntryGet($cursor, $page, $session, $limit): \OpenAPI\Client\Model\GamificationleaderboardentryResponse[]
```

Get leaderboard entry list

This endpoint returns an array of all leaderboard entries for a cursor. The output is in administrative representation and filtered for the user permissions.  Cursor could be created here: POST /reaction/admin/gamification/entry/search  __Note:__ Gamification is a premium feature and requires a valid subscription.  _accessible without permission_

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\GamificationAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$cursor = 'cursor_example'; // string | id of the cursor used for pagination; required if page is set
$page = 56; // int | current page index of the cursor used for pagination; required if cursor is set
$session = 'session_example'; // string | JWT
$limit = 56; // int | amount of results per page (1 ... 100)

try {
    $result = $apiInstance->reactionAdminGamificationEntryGet($cursor, $page, $session, $limit);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GamificationAdminApi->reactionAdminGamificationEntryGet: ', $e->getMessage(), PHP_EOL;
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

## `reactionAdminGamificationEntrySearchPost()`

```php
reactionAdminGamificationEntrySearchPost($session, $request): \OpenAPI\Client\Model\ModelCursorResponse
```

Create cursor leaderboard entries

This endpoint returns a cursor for list leaderboard entries in admin representation with applied filter and sort options. In case of cursor response total will be 0 the status 204 with not content is returned instead.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\GamificationAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\GamificationleaderboardentryCursorRequestAdmin(); // \OpenAPI\Client\Model\GamificationleaderboardentryCursorRequestAdmin | options to create cursor

try {
    $result = $apiInstance->reactionAdminGamificationEntrySearchPost($session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GamificationAdminApi->reactionAdminGamificationEntrySearchPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\GamificationleaderboardentryCursorRequestAdmin**](../Model/GamificationleaderboardentryCursorRequestAdmin.md)| options to create cursor | |

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

## `reactionAdminGamificationLeaderboardIdAccountAccountIdBonusPost()`

```php
reactionAdminGamificationLeaderboardIdAccountAccountIdBonusPost($id, $account_id, $session, $request): \OpenAPI\Client\Model\GamificationleaderboardentryResponse
```

Add gamification bonus

This endpoint adds a bonus balance entry for an account. A negative bonus can be used as a penalty.  __Note:__ Gamification is a premium feature and requires a valid subscription.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\GamificationAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Leaderboard ID
$account_id = 'account_id_example'; // string | Account ID
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\GamificationbalancePostBonusRequest(); // \OpenAPI\Client\Model\GamificationbalancePostBonusRequest | Bonus data

try {
    $result = $apiInstance->reactionAdminGamificationLeaderboardIdAccountAccountIdBonusPost($id, $account_id, $session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GamificationAdminApi->reactionAdminGamificationLeaderboardIdAccountAccountIdBonusPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Leaderboard ID | |
| **account_id** | **string**| Account ID | |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\GamificationbalancePostBonusRequest**](../Model/GamificationbalancePostBonusRequest.md)| Bonus data | |

### Return type

[**\OpenAPI\Client\Model\GamificationleaderboardentryResponse**](../Model/GamificationleaderboardentryResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `reactionAdminGamificationLeaderboardIdAccountAccountIdResetPut()`

```php
reactionAdminGamificationLeaderboardIdAccountAccountIdResetPut($id, $account_id, $session): \OpenAPI\Client\Model\ModelSwagStatusOk
```

Reset account gamification balance

This endpoint removes all balance entries for a specific account in the given leaderboard and resets their score to 0.  __Note:__ Gamification is a premium feature and requires a valid subscription.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\GamificationAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Leaderboard ID
$account_id = 'account_id_example'; // string | Account ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->reactionAdminGamificationLeaderboardIdAccountAccountIdResetPut($id, $account_id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GamificationAdminApi->reactionAdminGamificationLeaderboardIdAccountAccountIdResetPut: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Leaderboard ID | |
| **account_id** | **string**| Account ID | |
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

## `reactionAdminGamificationLeaderboardIdGet()`

```php
reactionAdminGamificationLeaderboardIdGet($id, $session): \OpenAPI\Client\Model\GamificationleaderboardResponseAdmin
```

Get leaderboard

This endpoint returns a leaderboard in administrative representation by given id.  __Note:__ Gamification is a premium feature and requires a valid subscription.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\GamificationAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Leaderboard ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->reactionAdminGamificationLeaderboardIdGet($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GamificationAdminApi->reactionAdminGamificationLeaderboardIdGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Leaderboard ID | |
| **session** | **string**| JWT | |

### Return type

[**\OpenAPI\Client\Model\GamificationleaderboardResponseAdmin**](../Model/GamificationleaderboardResponseAdmin.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `reactionAdminGamificationLeaderboardIdPatch()`

```php
reactionAdminGamificationLeaderboardIdPatch($id, $session, $request): \OpenAPI\Client\Model\GamificationleaderboardResponseAdmin
```

Update leaderboard

This endpoint is for updating specific data of an existing leaderboard.  __Note:__ Gamification is a premium feature and requires a valid subscription.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\GamificationAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Leaderboard ID
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\GamificationleaderboardPatchRequest(); // \OpenAPI\Client\Model\GamificationleaderboardPatchRequest | leaderboard data to update

try {
    $result = $apiInstance->reactionAdminGamificationLeaderboardIdPatch($id, $session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GamificationAdminApi->reactionAdminGamificationLeaderboardIdPatch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Leaderboard ID | |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\GamificationleaderboardPatchRequest**](../Model/GamificationleaderboardPatchRequest.md)| leaderboard data to update | |

### Return type

[**\OpenAPI\Client\Model\GamificationleaderboardResponseAdmin**](../Model/GamificationleaderboardResponseAdmin.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `reactionAdminGamificationLeaderboardIdResetPut()`

```php
reactionAdminGamificationLeaderboardIdResetPut($id, $session): \OpenAPI\Client\Model\ModelSwagStatusOk
```

Reset gamification balance

This endpoint removes all balance entries for a specific leaderboard and resets score from all accounts to 0.  __Note:__ Gamification is a premium feature and requires a valid subscription.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\GamificationAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Leaderboard ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->reactionAdminGamificationLeaderboardIdResetPut($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GamificationAdminApi->reactionAdminGamificationLeaderboardIdResetPut: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Leaderboard ID | |
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

## `reactionAdminGamificationLeaderboardIdSyncPut()`

```php
reactionAdminGamificationLeaderboardIdSyncPut($id, $session)
```

Sync gamification balance

This endpoint syncs all balance entries for a specific leaderboard and sets correct scores and ranks of all accounts.  __Note:__ Gamification is a premium feature and requires a valid subscription.  _only accessible with permission_ : `\"Plazz\"`  _fully accessible with permission_ : `\"Plazz\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\GamificationAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Leaderboard ID
$session = 'session_example'; // string | JWT

try {
    $apiInstance->reactionAdminGamificationLeaderboardIdSyncPut($id, $session);
} catch (Exception $e) {
    echo 'Exception when calling GamificationAdminApi->reactionAdminGamificationLeaderboardIdSyncPut: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Leaderboard ID | |
| **session** | **string**| JWT | |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `reactionAdminGamificationLeaderboardProjectProjectIdGet()`

```php
reactionAdminGamificationLeaderboardProjectProjectIdGet($project_id, $session, $cursor, $limit, $page): \OpenAPI\Client\Model\GamificationleaderboardResponseAdmin[]
```

Get leaderboard list for project

This endpoint returns a list of all leaderboard for the requested project in administrative representation. If a limit is set, a cursor for this endpoint may be created to iterate over all leaderboards.  __Note:__ Gamification is a premium feature and requires a valid subscription.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\GamificationAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$project_id = 'project_id_example'; // string | Project ID
$session = 'session_example'; // string | JWT
$cursor = 'cursor_example'; // string | id of the cursor used for pagination; required if page is set
$limit = 56; // int | amount of results per page (1 ... 100)
$page = 56; // int | current page index of the cursor used for pagination; required if cursor is set

try {
    $result = $apiInstance->reactionAdminGamificationLeaderboardProjectProjectIdGet($project_id, $session, $cursor, $limit, $page);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GamificationAdminApi->reactionAdminGamificationLeaderboardProjectProjectIdGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **project_id** | **string**| Project ID | |
| **session** | **string**| JWT | |
| **cursor** | **string**| id of the cursor used for pagination; required if page is set | [optional] |
| **limit** | **int**| amount of results per page (1 ... 100) | [optional] |
| **page** | **int**| current page index of the cursor used for pagination; required if cursor is set | [optional] |

### Return type

[**\OpenAPI\Client\Model\GamificationleaderboardResponseAdmin[]**](../Model/GamificationleaderboardResponseAdmin.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `reactionAdminGamificationProjectProjectIdSettingsGet()`

```php
reactionAdminGamificationProjectProjectIdSettingsGet($project_id, $session): \OpenAPI\Client\Model\ModelProjectGamificationSettings
```

Get project settings

This endpoint returns the gamification settings in administrative representation by given project id.  __Note:__ Gamification is a premium feature and requires a valid subscription.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\GamificationAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$project_id = 'project_id_example'; // string | Project ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->reactionAdminGamificationProjectProjectIdSettingsGet($project_id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GamificationAdminApi->reactionAdminGamificationProjectProjectIdSettingsGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **project_id** | **string**| Project ID | |
| **session** | **string**| JWT | |

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

## `reactionAdminGamificationProjectProjectIdSettingsPut()`

```php
reactionAdminGamificationProjectProjectIdSettingsPut($project_id, $session, $request): \OpenAPI\Client\Model\ModelProjectGamificationSettings
```

Get project settings

This endpoint is for updating gamification settings of an existing project.  __Note:__ Gamification is a premium feature and requires a valid subscription.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\GamificationAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$project_id = 'project_id_example'; // string | Project ID
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\ModelProjectGamificationSettings(); // \OpenAPI\Client\Model\ModelProjectGamificationSettings | gamification settings

try {
    $result = $apiInstance->reactionAdminGamificationProjectProjectIdSettingsPut($project_id, $session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GamificationAdminApi->reactionAdminGamificationProjectProjectIdSettingsPut: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **project_id** | **string**| Project ID | |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\ModelProjectGamificationSettings**](../Model/ModelProjectGamificationSettings.md)| gamification settings | |

### Return type

[**\OpenAPI\Client\Model\ModelProjectGamificationSettings**](../Model/ModelProjectGamificationSettings.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `reactionAdminGamificationRuleGet()`

```php
reactionAdminGamificationRuleGet($session): \OpenAPI\Client\Model\GamificationruleResponse[]
```

Get gamification rule list

This endpoint returns an array of all gamification rules for a cursor. The output is in administrative representation and filtered for the user permissions.  Cursor could be created here: POST /reaction/admin/gamification/rule/search  _accessible without permission_

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\GamificationAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->reactionAdminGamificationRuleGet($session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GamificationAdminApi->reactionAdminGamificationRuleGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **session** | **string**| JWT | |

### Return type

[**\OpenAPI\Client\Model\GamificationruleResponse[]**](../Model/GamificationruleResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `reactionAdminGamificationRuleIdDelete()`

```php
reactionAdminGamificationRuleIdDelete($id, $session): \OpenAPI\Client\Model\ModelSwagStatusOk
```

Delete gamification rule

This endpoint deletes a gamification rule by given id.  __Note:__ Gamification is a premium feature and requires a valid subscription.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\GamificationAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Rule ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->reactionAdminGamificationRuleIdDelete($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GamificationAdminApi->reactionAdminGamificationRuleIdDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Rule ID | |
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

## `reactionAdminGamificationRuleIdGet()`

```php
reactionAdminGamificationRuleIdGet($id, $session): \OpenAPI\Client\Model\GamificationruleResponse
```

Get gamification rule

This endpoint returns a gamification rule by given id.  __Note:__ Gamification is a premium feature and requires a valid subscription.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\GamificationAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Rule ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->reactionAdminGamificationRuleIdGet($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GamificationAdminApi->reactionAdminGamificationRuleIdGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Rule ID | |
| **session** | **string**| JWT | |

### Return type

[**\OpenAPI\Client\Model\GamificationruleResponse**](../Model/GamificationruleResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `reactionAdminGamificationRuleIdPatch()`

```php
reactionAdminGamificationRuleIdPatch($id, $session, $request): \OpenAPI\Client\Model\GamificationruleResponse
```

Update gamification rule

This endpoint updates a gamification rule by given id.  __Note:__ Gamification is a premium feature and requires a valid subscription.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\GamificationAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Rule ID
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\GamificationrulePatchRequest(); // \OpenAPI\Client\Model\GamificationrulePatchRequest | rule data to be updated

try {
    $result = $apiInstance->reactionAdminGamificationRuleIdPatch($id, $session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GamificationAdminApi->reactionAdminGamificationRuleIdPatch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Rule ID | |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\GamificationrulePatchRequest**](../Model/GamificationrulePatchRequest.md)| rule data to be updated | [optional] |

### Return type

[**\OpenAPI\Client\Model\GamificationruleResponse**](../Model/GamificationruleResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `reactionAdminGamificationRulePost()`

```php
reactionAdminGamificationRulePost($session, $request): \OpenAPI\Client\Model\GamificationruleResponse
```

Create gamification rule

This endpoint creates a new gamification rule.  __Note:__ Gamification is a premium feature and requires a valid subscription.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\GamificationAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\GamificationrulePostRequest(); // \OpenAPI\Client\Model\GamificationrulePostRequest | Rule to create

try {
    $result = $apiInstance->reactionAdminGamificationRulePost($session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GamificationAdminApi->reactionAdminGamificationRulePost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\GamificationrulePostRequest**](../Model/GamificationrulePostRequest.md)| Rule to create | |

### Return type

[**\OpenAPI\Client\Model\GamificationruleResponse**](../Model/GamificationruleResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `reactionAdminGamificationRuleSearchPost()`

```php
reactionAdminGamificationRuleSearchPost($session, $request): \OpenAPI\Client\Model\ModelCursorResponse
```

Create cursor gamification rules

This endpoint returns a cursor for list gamification rules in admin representation with applied filter and sort options. In case of cursor response total will be 0 the status 204 with not content is returned instead.  __Note:__ Gamification is a premium feature and requires a valid subscription.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\GamificationAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\GamificationruleCursorRequest(); // \OpenAPI\Client\Model\GamificationruleCursorRequest | options to create cursor

try {
    $result = $apiInstance->reactionAdminGamificationRuleSearchPost($session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GamificationAdminApi->reactionAdminGamificationRuleSearchPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\GamificationruleCursorRequest**](../Model/GamificationruleCursorRequest.md)| options to create cursor | |

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
