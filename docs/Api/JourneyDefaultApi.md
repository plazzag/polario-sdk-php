# OpenAPI\Client\JourneyDefaultApi



All URIs are relative to https://custom.polario.de/api, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**reactionDefaultJourneyGet()**](JourneyDefaultApi.md#reactionDefaultJourneyGet) | **GET** /reaction/default/journey | Get journey processes list for cursor |
| [**reactionDefaultJourneyIdGet()**](JourneyDefaultApi.md#reactionDefaultJourneyIdGet) | **GET** /reaction/default/journey/{id} | Get journey |
| [**reactionDefaultJourneyIdProcessGet()**](JourneyDefaultApi.md#reactionDefaultJourneyIdProcessGet) | **GET** /reaction/default/journey/{id}/process | Get journey process |
| [**reactionDefaultJourneyIdStageStageIdPatch()**](JourneyDefaultApi.md#reactionDefaultJourneyIdStageStageIdPatch) | **PATCH** /reaction/default/journey/{id}/stage/{stageId} | Update stage status |
| [**reactionDefaultJourneySearchPost()**](JourneyDefaultApi.md#reactionDefaultJourneySearchPost) | **POST** /reaction/default/journey/search | Create cursor |
| [**reactionDefaultJourneyStatsGet()**](JourneyDefaultApi.md#reactionDefaultJourneyStatsGet) | **GET** /reaction/default/journey/stats | Get journey stats |


## `reactionDefaultJourneyGet()`

```php
reactionDefaultJourneyGet($session, $cursor, $page, $limit, $accept_language): \OpenAPI\Client\Model\JourneyprocessResponseListDefault[]
```

Get journey processes list for cursor

This endpoint returns a list of all journey processes for account without content in default representation.  Cursor could be created here: POST /reaction/default/journey/search  _accessible without permission_

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\JourneyDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT
$cursor = 'cursor_example'; // string | id of the cursor used for pagination; required if page is set
$page = 56; // int | current page index of the cursor used for pagination; required if cursor is set
$limit = 56; // int | amount of results per page (1 ... 100)
$accept_language = 'accept_language_example'; // string | client language(s)

try {
    $result = $apiInstance->reactionDefaultJourneyGet($session, $cursor, $page, $limit, $accept_language);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling JourneyDefaultApi->reactionDefaultJourneyGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **session** | **string**| JWT | |
| **cursor** | **string**| id of the cursor used for pagination; required if page is set | [optional] |
| **page** | **int**| current page index of the cursor used for pagination; required if cursor is set | [optional] |
| **limit** | **int**| amount of results per page (1 ... 100) | [optional] |
| **accept_language** | **string**| client language(s) | [optional] |

### Return type

[**\OpenAPI\Client\Model\JourneyprocessResponseListDefault[]**](../Model/JourneyprocessResponseListDefault.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `reactionDefaultJourneyIdGet()`

```php
reactionDefaultJourneyIdGet($id, $session, $accept_language): \OpenAPI\Client\Model\JourneyResponseDefault
```

Get journey

This endpoint returns a journey in default representation by given id. If the requested language is not available it will fall back to the default language.  _accessible without permission_

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\JourneyDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Journey ID
$session = 'session_example'; // string | JWT
$accept_language = 'accept_language_example'; // string | client language(s)

try {
    $result = $apiInstance->reactionDefaultJourneyIdGet($id, $session, $accept_language);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling JourneyDefaultApi->reactionDefaultJourneyIdGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Journey ID | |
| **session** | **string**| JWT | |
| **accept_language** | **string**| client language(s) | [optional] |

### Return type

[**\OpenAPI\Client\Model\JourneyResponseDefault**](../Model/JourneyResponseDefault.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `reactionDefaultJourneyIdProcessGet()`

```php
reactionDefaultJourneyIdProcessGet($id, $session, $accept_language): \OpenAPI\Client\Model\JourneyprocessResponseDefault
```

Get journey process

This endpoint returns a journey process in default representation by given journey id. If the requested language is not available it will fall back to the default language.  _accessible without permission_

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\JourneyDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Journey ID
$session = 'session_example'; // string | JWT
$accept_language = 'accept_language_example'; // string | client language(s)

try {
    $result = $apiInstance->reactionDefaultJourneyIdProcessGet($id, $session, $accept_language);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling JourneyDefaultApi->reactionDefaultJourneyIdProcessGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Journey ID | |
| **session** | **string**| JWT | |
| **accept_language** | **string**| client language(s) | [optional] |

### Return type

[**\OpenAPI\Client\Model\JourneyprocessResponseDefault**](../Model/JourneyprocessResponseDefault.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `reactionDefaultJourneyIdStageStageIdPatch()`

```php
reactionDefaultJourneyIdStageStageIdPatch($id, $stage_id, $session, $request, $accept_language): \OpenAPI\Client\Model\JourneyprocessResponseDefault
```

Update stage status

This endpoint is for updating the status of a stage for an own journey process. If the requested language is not available it will fall back to the default language.  _accessible without permission_

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\JourneyDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Journey ID
$stage_id = 'stage_id_example'; // string | Stage ID
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\JourneyprocessPatchStageStatus(); // \OpenAPI\Client\Model\JourneyprocessPatchStageStatus | stage status information
$accept_language = 'accept_language_example'; // string | client language(s)

try {
    $result = $apiInstance->reactionDefaultJourneyIdStageStageIdPatch($id, $stage_id, $session, $request, $accept_language);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling JourneyDefaultApi->reactionDefaultJourneyIdStageStageIdPatch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Journey ID | |
| **stage_id** | **string**| Stage ID | |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\JourneyprocessPatchStageStatus**](../Model/JourneyprocessPatchStageStatus.md)| stage status information | |
| **accept_language** | **string**| client language(s) | [optional] |

### Return type

[**\OpenAPI\Client\Model\JourneyprocessResponseDefault**](../Model/JourneyprocessResponseDefault.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `reactionDefaultJourneySearchPost()`

```php
reactionDefaultJourneySearchPost($session, $request): \OpenAPI\Client\Model\ModelCursorResponse
```

Create cursor

This endpoint returns a cursor for list own journeys in default representation with applied filter and sort options. In case of cursor response total will be 0 the status 204 with not content is returned instead.  _accessible without permission_

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\JourneyDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\JourneyprocessCursorRequestDefault(); // \OpenAPI\Client\Model\JourneyprocessCursorRequestDefault | options to create cursor

try {
    $result = $apiInstance->reactionDefaultJourneySearchPost($session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling JourneyDefaultApi->reactionDefaultJourneySearchPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\JourneyprocessCursorRequestDefault**](../Model/JourneyprocessCursorRequestDefault.md)| options to create cursor | |

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

## `reactionDefaultJourneyStatsGet()`

```php
reactionDefaultJourneyStatsGet($session): \OpenAPI\Client\Model\JourneyResponseStatsDefault
```

Get journey stats

This endpoint returns aggregated statistics for journeys of the authenticated account.  _accessible without permission_

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\JourneyDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->reactionDefaultJourneyStatsGet($session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling JourneyDefaultApi->reactionDefaultJourneyStatsGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **session** | **string**| JWT | |

### Return type

[**\OpenAPI\Client\Model\JourneyResponseStatsDefault**](../Model/JourneyResponseStatsDefault.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
