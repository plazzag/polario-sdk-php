# OpenAPI\Client\SurveyAdminApi



All URIs are relative to https://custom.polario.de/api, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**reactionAdminSurveyIdAccessGet()**](SurveyAdminApi.md#reactionAdminSurveyIdAccessGet) | **GET** /reaction/admin/survey/{id}/access | Get survey access configuration |
| [**reactionAdminSurveyIdAccessPatch()**](SurveyAdminApi.md#reactionAdminSurveyIdAccessPatch) | **PATCH** /reaction/admin/survey/{id}/access | Update survey access configuration |
| [**reactionAdminSurveyIdAggregationGet()**](SurveyAdminApi.md#reactionAdminSurveyIdAggregationGet) | **GET** /reaction/admin/survey/{id}/aggregation | Get survey aggregation |
| [**reactionAdminSurveyIdAnswerGet()**](SurveyAdminApi.md#reactionAdminSurveyIdAnswerGet) | **GET** /reaction/admin/survey/{id}/answer | Get survey answers |
| [**reactionAdminSurveyIdAnswerSearchPost()**](SurveyAdminApi.md#reactionAdminSurveyIdAnswerSearchPost) | **POST** /reaction/admin/survey/{id}/answer/search | Create survey answers cursor |
| [**reactionAdminSurveyIdDelete()**](SurveyAdminApi.md#reactionAdminSurveyIdDelete) | **DELETE** /reaction/admin/survey/{id} | Delete survey |
| [**reactionAdminSurveyIdGet()**](SurveyAdminApi.md#reactionAdminSurveyIdGet) | **GET** /reaction/admin/survey/{id} | Get survey |
| [**reactionAdminSurveyIdItemsGet()**](SurveyAdminApi.md#reactionAdminSurveyIdItemsGet) | **GET** /reaction/admin/survey/{id}/items | Get items |
| [**reactionAdminSurveyIdItemsPut()**](SurveyAdminApi.md#reactionAdminSurveyIdItemsPut) | **PUT** /reaction/admin/survey/{id}/items | Update items |
| [**reactionAdminSurveyIdParticipationDelete()**](SurveyAdminApi.md#reactionAdminSurveyIdParticipationDelete) | **DELETE** /reaction/admin/survey/{id}/participation | Delete survey participations |
| [**reactionAdminSurveyIdParticipationGet()**](SurveyAdminApi.md#reactionAdminSurveyIdParticipationGet) | **GET** /reaction/admin/survey/{id}/participation | Get survey participations |
| [**reactionAdminSurveyIdParticipationSearchPost()**](SurveyAdminApi.md#reactionAdminSurveyIdParticipationSearchPost) | **POST** /reaction/admin/survey/{id}/participation/search | Create survey participation cursor |
| [**reactionAdminSurveyIdPatch()**](SurveyAdminApi.md#reactionAdminSurveyIdPatch) | **PATCH** /reaction/admin/survey/{id} | Update survey |
| [**reactionAdminSurveyPost()**](SurveyAdminApi.md#reactionAdminSurveyPost) | **POST** /reaction/admin/survey | Create survey |
| [**reactionAdminSurveyProjectIdGet()**](SurveyAdminApi.md#reactionAdminSurveyProjectIdGet) | **GET** /reaction/admin/survey/project/{id} | Get survey list for project |
| [**reactionAdminSurveySearchPost()**](SurveyAdminApi.md#reactionAdminSurveySearchPost) | **POST** /reaction/admin/survey/search | Create survey cursor |
| [**surveyAdminGet()**](SurveyAdminApi.md#surveyAdminGet) | **GET** /survey/admin | Get survey list |


## `reactionAdminSurveyIdAccessGet()`

```php
reactionAdminSurveyIdAccessGet($id, $session): \OpenAPI\Client\Model\AuthorizationAccessResponse
```

Get survey access configuration

This endpoint returns the access configuration for the requested survey.  __Note:__ Surveys is a premium feature and requires a valid subscription.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\SurveyAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Survey ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->reactionAdminSurveyIdAccessGet($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SurveyAdminApi->reactionAdminSurveyIdAccessGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Survey ID | |
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

## `reactionAdminSurveyIdAccessPatch()`

```php
reactionAdminSurveyIdAccessPatch($id, $session, $request): \OpenAPI\Client\Model\ModelAccess
```

Update survey access configuration

This endpoint updates the access configuration for the requested survey. Only the changes should be transmitted due this endpoint.  __Note:__ Surveys is a premium feature and requires a valid subscription.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\SurveyAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Survey ID
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\ModelAccess(); // \OpenAPI\Client\Model\ModelAccess | changed access rights

try {
    $result = $apiInstance->reactionAdminSurveyIdAccessPatch($id, $session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SurveyAdminApi->reactionAdminSurveyIdAccessPatch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Survey ID | |
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

## `reactionAdminSurveyIdAggregationGet()`

```php
reactionAdminSurveyIdAggregationGet($id, $session): array<string,array>
```

Get survey aggregation

This endpoint returns an aggregation for the given survey.  __Note:__ Surveys is a premium feature and requires a valid subscription.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\SurveyAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Survey ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->reactionAdminSurveyIdAggregationGet($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SurveyAdminApi->reactionAdminSurveyIdAggregationGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Survey ID | |
| **session** | **string**| JWT | |

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

## `reactionAdminSurveyIdAnswerGet()`

```php
reactionAdminSurveyIdAnswerGet($id, $session, $cursor, $limit, $page): \OpenAPI\Client\Model\SurveyanswerResponseAdmin[]
```

Get survey answers

This endpoint returns all answer records for the given survey.  __Note:__ Surveys is a premium feature and requires a valid subscription.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\SurveyAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Survey ID
$session = 'session_example'; // string | JWT
$cursor = 'cursor_example'; // string | id of the cursor used for pagination; required if page is set
$limit = 56; // int | amount of results per page (1 ... 100)
$page = 56; // int | current page index of the cursor used for pagination; required if cursor is set

try {
    $result = $apiInstance->reactionAdminSurveyIdAnswerGet($id, $session, $cursor, $limit, $page);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SurveyAdminApi->reactionAdminSurveyIdAnswerGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Survey ID | |
| **session** | **string**| JWT | |
| **cursor** | **string**| id of the cursor used for pagination; required if page is set | [optional] |
| **limit** | **int**| amount of results per page (1 ... 100) | [optional] |
| **page** | **int**| current page index of the cursor used for pagination; required if cursor is set | [optional] |

### Return type

[**\OpenAPI\Client\Model\SurveyanswerResponseAdmin[]**](../Model/SurveyanswerResponseAdmin.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `reactionAdminSurveyIdAnswerSearchPost()`

```php
reactionAdminSurveyIdAnswerSearchPost($id, $session, $request): \OpenAPI\Client\Model\ModelCursorResponse
```

Create survey answers cursor

This endpoint returns a cursor for list surveys in admin representation with applied filter and sort options. In case of cursor response total will be 0 the status 204 with not content is returned instead.  __Note:__ Surveys is a premium feature and requires a valid subscription.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\SurveyAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Survey ID
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\SurveyanswerCursorRequestAdmin(); // \OpenAPI\Client\Model\SurveyanswerCursorRequestAdmin | options to create cursor

try {
    $result = $apiInstance->reactionAdminSurveyIdAnswerSearchPost($id, $session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SurveyAdminApi->reactionAdminSurveyIdAnswerSearchPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Survey ID | |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\SurveyanswerCursorRequestAdmin**](../Model/SurveyanswerCursorRequestAdmin.md)| options to create cursor | |

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

## `reactionAdminSurveyIdDelete()`

```php
reactionAdminSurveyIdDelete($id, $session): \OpenAPI\Client\Model\ModelSwagStatusOk
```

Delete survey

This endpoint is for deleting a single survey with all localizations.  __Note:__ Surveys is a premium feature and requires a valid subscription.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\SurveyAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Survey ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->reactionAdminSurveyIdDelete($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SurveyAdminApi->reactionAdminSurveyIdDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Survey ID | |
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

## `reactionAdminSurveyIdGet()`

```php
reactionAdminSurveyIdGet($id, $session): \OpenAPI\Client\Model\SurveyResponseAdmin
```

Get survey

This endpoint returns a survey in administrative representation by given id.  __Note:__ Surveys is a premium feature and requires a valid subscription.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\SurveyAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Survey ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->reactionAdminSurveyIdGet($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SurveyAdminApi->reactionAdminSurveyIdGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Survey ID | |
| **session** | **string**| JWT | |

### Return type

[**\OpenAPI\Client\Model\SurveyResponseAdmin**](../Model/SurveyResponseAdmin.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `reactionAdminSurveyIdItemsGet()`

```php
reactionAdminSurveyIdItemsGet($id, $session): \OpenAPI\Client\Model\SurveyResponseItemAdmin[]
```

Get items

This endpoint retrieves the items for a survey object in administrative representation by given id.  __Note:__ Surveys is a premium feature and requires a valid subscription.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\SurveyAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Survey ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->reactionAdminSurveyIdItemsGet($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SurveyAdminApi->reactionAdminSurveyIdItemsGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Survey ID | |
| **session** | **string**| JWT | |

### Return type

[**\OpenAPI\Client\Model\SurveyResponseItemAdmin[]**](../Model/SurveyResponseItemAdmin.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `reactionAdminSurveyIdItemsPut()`

```php
reactionAdminSurveyIdItemsPut($id, $session, $request): \OpenAPI\Client\Model\SurveyResponseItemAdmin[]
```

Update items

This endpoint updates the items for a survey object in administrative representation by given id.  __Note:__ Surveys is a premium feature and requires a valid subscription.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\SurveyAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Survey ID
$session = 'session_example'; // string | JWT
$request = array(new \OpenAPI\Client\Model\SurveyRequestItem()); // \OpenAPI\Client\Model\SurveyRequestItem[] | survey items to be updated

try {
    $result = $apiInstance->reactionAdminSurveyIdItemsPut($id, $session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SurveyAdminApi->reactionAdminSurveyIdItemsPut: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Survey ID | |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\SurveyRequestItem[]**](../Model/SurveyRequestItem.md)| survey items to be updated | |

### Return type

[**\OpenAPI\Client\Model\SurveyResponseItemAdmin[]**](../Model/SurveyResponseItemAdmin.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `reactionAdminSurveyIdParticipationDelete()`

```php
reactionAdminSurveyIdParticipationDelete($id, $session): \OpenAPI\Client\Model\ModelSwagStatusOk
```

Delete survey participations

This endpoint returns deletes all participation records and answers for the given survey.  __Note:__ Surveys is a premium feature and requires a valid subscription.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\SurveyAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Survey ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->reactionAdminSurveyIdParticipationDelete($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SurveyAdminApi->reactionAdminSurveyIdParticipationDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Survey ID | |
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

## `reactionAdminSurveyIdParticipationGet()`

```php
reactionAdminSurveyIdParticipationGet($id, $session, $cursor, $limit, $page): \OpenAPI\Client\Model\SurveyparticipationResponseAdmin[]
```

Get survey participations

This endpoint returns all participation records for the given survey.  __Note:__ Surveys is a premium feature and requires a valid subscription.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\SurveyAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Survey ID
$session = 'session_example'; // string | JWT
$cursor = 'cursor_example'; // string | id of the cursor used for pagination; required if page is set
$limit = 56; // int | amount of results per page (1 ... 100)
$page = 56; // int | current page index of the cursor used for pagination; required if cursor is set

try {
    $result = $apiInstance->reactionAdminSurveyIdParticipationGet($id, $session, $cursor, $limit, $page);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SurveyAdminApi->reactionAdminSurveyIdParticipationGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Survey ID | |
| **session** | **string**| JWT | |
| **cursor** | **string**| id of the cursor used for pagination; required if page is set | [optional] |
| **limit** | **int**| amount of results per page (1 ... 100) | [optional] |
| **page** | **int**| current page index of the cursor used for pagination; required if cursor is set | [optional] |

### Return type

[**\OpenAPI\Client\Model\SurveyparticipationResponseAdmin[]**](../Model/SurveyparticipationResponseAdmin.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `reactionAdminSurveyIdParticipationSearchPost()`

```php
reactionAdminSurveyIdParticipationSearchPost($id, $session, $request): \OpenAPI\Client\Model\ModelCursorResponse
```

Create survey participation cursor

This endpoint returns a cursor for list surveys in admin representation with applied filter and sort options. In case of cursor response total will be 0 the status 204 with not content is returned instead.  __Note:__ Surveys is a premium feature and requires a valid subscription.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\SurveyAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Survey ID
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\SurveyparticipationCursorRequestAdmin(); // \OpenAPI\Client\Model\SurveyparticipationCursorRequestAdmin | options to create cursor

try {
    $result = $apiInstance->reactionAdminSurveyIdParticipationSearchPost($id, $session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SurveyAdminApi->reactionAdminSurveyIdParticipationSearchPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Survey ID | |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\SurveyparticipationCursorRequestAdmin**](../Model/SurveyparticipationCursorRequestAdmin.md)| options to create cursor | |

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

## `reactionAdminSurveyIdPatch()`

```php
reactionAdminSurveyIdPatch($id, $session, $request): \OpenAPI\Client\Model\SurveyResponseAdmin
```

Update survey

This endpoint is for updating specific data of an existing survey.  __Note:__ Surveys is a premium feature and requires a valid subscription.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\SurveyAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Survey ID
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\SurveyPatchRequest(); // \OpenAPI\Client\Model\SurveyPatchRequest | survey data to be updated

try {
    $result = $apiInstance->reactionAdminSurveyIdPatch($id, $session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SurveyAdminApi->reactionAdminSurveyIdPatch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Survey ID | |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\SurveyPatchRequest**](../Model/SurveyPatchRequest.md)| survey data to be updated | [optional] |

### Return type

[**\OpenAPI\Client\Model\SurveyResponseAdmin**](../Model/SurveyResponseAdmin.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `reactionAdminSurveyPost()`

```php
reactionAdminSurveyPost($session, $request): \OpenAPI\Client\Model\SurveyResponseAdmin
```

Create survey

This endpoint is for creating a new survey.  __Note:__ Surveys is a premium feature and requires a valid subscription.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\SurveyAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\SurveyPostRequest(); // \OpenAPI\Client\Model\SurveyPostRequest | Survey to create

try {
    $result = $apiInstance->reactionAdminSurveyPost($session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SurveyAdminApi->reactionAdminSurveyPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\SurveyPostRequest**](../Model/SurveyPostRequest.md)| Survey to create | |

### Return type

[**\OpenAPI\Client\Model\SurveyResponseAdmin**](../Model/SurveyResponseAdmin.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `reactionAdminSurveyProjectIdGet()`

```php
reactionAdminSurveyProjectIdGet($id, $session, $cursor, $limit, $page): \OpenAPI\Client\Model\SurveyResponseListAdmin[]
```

Get survey list for project

This endpoint returns a list of all surveys for the requested project without items in administrative representation. If a limit is set, a cursor for this endpoint may be created to iterate over all surveys.  __Note:__ Surveys is a premium feature and requires a valid subscription.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\SurveyAdminApi(
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
    $result = $apiInstance->reactionAdminSurveyProjectIdGet($id, $session, $cursor, $limit, $page);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SurveyAdminApi->reactionAdminSurveyProjectIdGet: ', $e->getMessage(), PHP_EOL;
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

[**\OpenAPI\Client\Model\SurveyResponseListAdmin[]**](../Model/SurveyResponseListAdmin.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `reactionAdminSurveySearchPost()`

```php
reactionAdminSurveySearchPost($session, $request): \OpenAPI\Client\Model\ModelCursorResponse
```

Create survey cursor

This endpoint returns a cursor for list surveys in admin representation with applied filter and sort options. In case of cursor response total will be 0 the status 204 with not content is returned instead.  __Note:__ Surveys is a premium feature and requires a valid subscription.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\SurveyAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\SurveyCursorRequestAdmin(); // \OpenAPI\Client\Model\SurveyCursorRequestAdmin | options to create cursor

try {
    $result = $apiInstance->reactionAdminSurveySearchPost($session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SurveyAdminApi->reactionAdminSurveySearchPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\SurveyCursorRequestAdmin**](../Model/SurveyCursorRequestAdmin.md)| options to create cursor | |

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

## `surveyAdminGet()`

```php
surveyAdminGet($cursor, $page, $session, $limit): \OpenAPI\Client\Model\SurveyResponseListAdmin[]
```

Get survey list

This endpoint returns an array of all surveys for a cursor. The output is in administrative representation and filtered for the user permissions.  Cursor could be created here: POST /reaction/admin/survey/search  __Note:__ Surveys is a premium feature and requires a valid subscription.  _accessible without permission_

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\SurveyAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$cursor = 'cursor_example'; // string | id of the cursor used for pagination; required if page is set
$page = 56; // int | current page index of the cursor used for pagination; required if cursor is set
$session = 'session_example'; // string | JWT
$limit = 56; // int | amount of results per page (1 ... 100)

try {
    $result = $apiInstance->surveyAdminGet($cursor, $page, $session, $limit);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SurveyAdminApi->surveyAdminGet: ', $e->getMessage(), PHP_EOL;
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

[**\OpenAPI\Client\Model\SurveyResponseListAdmin[]**](../Model/SurveyResponseListAdmin.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
