# OpenAPI\Client\PartyDefaultApi



All URIs are relative to https://custom.polario.de/api, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**partyDefaultGet()**](PartyDefaultApi.md#partyDefaultGet) | **GET** /party/default | Get party list for cursor |
| [**partyDefaultIdReactionGet()**](PartyDefaultApi.md#partyDefaultIdReactionGet) | **GET** /party/default/{id}/reaction | Get reaction |
| [**partyDefaultIdReactionPut()**](PartyDefaultApi.md#partyDefaultIdReactionPut) | **PUT** /party/default/{id}/reaction | Set reaction |
| [**partyDefaultObjectTypeObjectIdGet()**](PartyDefaultApi.md#partyDefaultObjectTypeObjectIdGet) | **GET** /party/default/{objectType}/{objectId} | Get party |
| [**partyDefaultObjectTypeReferenceObjectIdGet()**](PartyDefaultApi.md#partyDefaultObjectTypeReferenceObjectIdGet) | **GET** /party/default/{objectType}/reference/{objectId} | Get parties for reference |
| [**partyDefaultReactionGet()**](PartyDefaultApi.md#partyDefaultReactionGet) | **GET** /party/default/reaction | Get reaction list for cursor |
| [**partyDefaultReactionSearchPost()**](PartyDefaultApi.md#partyDefaultReactionSearchPost) | **POST** /party/default/reaction/search | Create cursor |
| [**partyDefaultSearchPost()**](PartyDefaultApi.md#partyDefaultSearchPost) | **POST** /party/default/search | Create cursor |


## `partyDefaultGet()`

```php
partyDefaultGet($cursor, $page, $session, $limit): \OpenAPI\Client\Model\PartyResponseDefault[]
```

Get party list for cursor

This endpoint returns a list of all parties for a cursor in default representation.  Cursor could be created here: POST /party/default/search  _accessible without permission_

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\PartyDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$cursor = 'cursor_example'; // string | id of the cursor used for pagination; required if page is set
$page = 56; // int | current page index of the cursor used for pagination; required if cursor is set
$session = 'session_example'; // string | JWT
$limit = 56; // int | amount of results per page (1 ... 100)

try {
    $result = $apiInstance->partyDefaultGet($cursor, $page, $session, $limit);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PartyDefaultApi->partyDefaultGet: ', $e->getMessage(), PHP_EOL;
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

[**\OpenAPI\Client\Model\PartyResponseDefault[]**](../Model/PartyResponseDefault.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `partyDefaultIdReactionGet()`

```php
partyDefaultIdReactionGet($id, $session): \OpenAPI\Client\Model\GitPlazzNetReposSandmannBackendServicesPartyReactionResponseDefault
```

Get reaction

This endpoint returns the reaction for the own account for given party id.  _accessible without permission_  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\PartyDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | party id
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->partyDefaultIdReactionGet($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PartyDefaultApi->partyDefaultIdReactionGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| party id | |
| **session** | **string**| JWT | |

### Return type

[**\OpenAPI\Client\Model\GitPlazzNetReposSandmannBackendServicesPartyReactionResponseDefault**](../Model/GitPlazzNetReposSandmannBackendServicesPartyReactionResponseDefault.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `partyDefaultIdReactionPut()`

```php
partyDefaultIdReactionPut($id, $session, $request): \OpenAPI\Client\Model\ModelSwagStatusOk
```

Set reaction

This endpoint updates the reaction for the own account for given party id.  _accessible without permission_  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\PartyDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | party id
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\ReactionRequest(); // \OpenAPI\Client\Model\ReactionRequest | reaction

try {
    $result = $apiInstance->partyDefaultIdReactionPut($id, $session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PartyDefaultApi->partyDefaultIdReactionPut: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| party id | |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\ReactionRequest**](../Model/ReactionRequest.md)| reaction | |

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

## `partyDefaultObjectTypeObjectIdGet()`

```php
partyDefaultObjectTypeObjectIdGet($object_type, $object_id, $session): \OpenAPI\Client\Model\PartyResponseDefault
```

Get party

This endpoint returns a party in default representation by given id.  __Note:__ for objectType `CalendarEntry` _config.bookingSlots.dateEnd_ and _config.bookingSlots.timeEnd_ will not be null  _accessible without permission_  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\PartyDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$object_type = 'object_type_example'; // string | object type
$object_id = 'object_id_example'; // string | object id
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->partyDefaultObjectTypeObjectIdGet($object_type, $object_id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PartyDefaultApi->partyDefaultObjectTypeObjectIdGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **object_type** | **string**| object type | |
| **object_id** | **string**| object id | |
| **session** | **string**| JWT | |

### Return type

[**\OpenAPI\Client\Model\PartyResponseDefault**](../Model/PartyResponseDefault.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `partyDefaultObjectTypeReferenceObjectIdGet()`

```php
partyDefaultObjectTypeReferenceObjectIdGet($object_type, $object_id, $session, $cursor, $limit, $page): \OpenAPI\Client\Model\PartyResponseDefault[]
```

Get parties for reference

This endpoint returns all parties for the provided reference in default representation. If the limit is set, a cursor for this endpoint may be created to iterate over all locations.  __Note:__ for objectType `CalendarEntry` _config.bookingSlots.dateEnd_ and _config.bookingSlots.timeEnd_ will not be null; objectId is calendarId (referenceId)  _accessible without permission_  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\PartyDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$object_type = 'object_type_example'; // string | object type
$object_id = 'object_id_example'; // string | reference id
$session = 'session_example'; // string | JWT
$cursor = 'cursor_example'; // string | id of the cursor used for pagination; required if page is set
$limit = 56; // int | amount of results per page (1 ... 100)
$page = 56; // int | current page index of the cursor used for pagination; required if cursor is set

try {
    $result = $apiInstance->partyDefaultObjectTypeReferenceObjectIdGet($object_type, $object_id, $session, $cursor, $limit, $page);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PartyDefaultApi->partyDefaultObjectTypeReferenceObjectIdGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **object_type** | **string**| object type | |
| **object_id** | **string**| reference id | |
| **session** | **string**| JWT | |
| **cursor** | **string**| id of the cursor used for pagination; required if page is set | [optional] |
| **limit** | **int**| amount of results per page (1 ... 100) | [optional] |
| **page** | **int**| current page index of the cursor used for pagination; required if cursor is set | [optional] |

### Return type

[**\OpenAPI\Client\Model\PartyResponseDefault[]**](../Model/PartyResponseDefault.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `partyDefaultReactionGet()`

```php
partyDefaultReactionGet($cursor, $page, $session, $limit): \OpenAPI\Client\Model\GitPlazzNetReposSandmannBackendServicesPartyReactionResponseDefault[]
```

Get reaction list for cursor

This endpoint returns a list of all reactions for a cursor in default representation.  Cursor could be created here: POST /party/default/reaction/search  _accessible without permission_

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\PartyDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$cursor = 'cursor_example'; // string | id of the cursor used for pagination; required if page is set
$page = 56; // int | current page index of the cursor used for pagination; required if cursor is set
$session = 'session_example'; // string | JWT
$limit = 56; // int | amount of results per page (1 ... 100)

try {
    $result = $apiInstance->partyDefaultReactionGet($cursor, $page, $session, $limit);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PartyDefaultApi->partyDefaultReactionGet: ', $e->getMessage(), PHP_EOL;
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

[**\OpenAPI\Client\Model\GitPlazzNetReposSandmannBackendServicesPartyReactionResponseDefault[]**](../Model/GitPlazzNetReposSandmannBackendServicesPartyReactionResponseDefault.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `partyDefaultReactionSearchPost()`

```php
partyDefaultReactionSearchPost($session, $request): \OpenAPI\Client\Model\ModelCursorResponse
```

Create cursor

This endpoint returns a cursor for list reactions in default representation with applied filter and sort options. In case of cursor response total will be 0 the status 204 with not content is returned instead.  _only accessible with permission_ : `\"ManageAccounts\"`  _fully accessible with permission_ : `\"ManageAccounts\"` + `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\PartyDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\GitPlazzNetReposSandmannBackendServicesPartyReactionCursorRequestDefault(); // \OpenAPI\Client\Model\GitPlazzNetReposSandmannBackendServicesPartyReactionCursorRequestDefault | options to create cursor

try {
    $result = $apiInstance->partyDefaultReactionSearchPost($session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PartyDefaultApi->partyDefaultReactionSearchPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\GitPlazzNetReposSandmannBackendServicesPartyReactionCursorRequestDefault**](../Model/GitPlazzNetReposSandmannBackendServicesPartyReactionCursorRequestDefault.md)| options to create cursor | |

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

## `partyDefaultSearchPost()`

```php
partyDefaultSearchPost($session, $request): \OpenAPI\Client\Model\ModelCursorResponse
```

Create cursor

This endpoint returns a cursor for list parties in default representation with applied filter and sort options. In case of cursor response total will be 0 the status 204 with not content is returned instead.  _accessible without permission_  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\PartyDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\PartyCursorRequestDefault(); // \OpenAPI\Client\Model\PartyCursorRequestDefault | options to create cursor

try {
    $result = $apiInstance->partyDefaultSearchPost($session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PartyDefaultApi->partyDefaultSearchPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\PartyCursorRequestDefault**](../Model/PartyCursorRequestDefault.md)| options to create cursor | |

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
