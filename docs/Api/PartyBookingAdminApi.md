# OpenAPI\Client\PartyBookingAdminApi



All URIs are relative to https://custom.polario.de/api, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**partyAdminGet()**](PartyBookingAdminApi.md#partyAdminGet) | **GET** /party/admin | Get party list for cursor |
| [**partyAdminIdConfigPut()**](PartyBookingAdminApi.md#partyAdminIdConfigPut) | **PUT** /party/admin/{id}/config | Update party configuration |
| [**partyAdminIdDelete()**](PartyBookingAdminApi.md#partyAdminIdDelete) | **DELETE** /party/admin/{id} | Delete party |
| [**partyAdminIdGet()**](PartyBookingAdminApi.md#partyAdminIdGet) | **GET** /party/admin/{id} | Get party |
| [**partyAdminPost()**](PartyBookingAdminApi.md#partyAdminPost) | **POST** /party/admin | Create party |
| [**partyAdminSearchPost()**](PartyBookingAdminApi.md#partyAdminSearchPost) | **POST** /party/admin/search | Create cursor parties |


## `partyAdminGet()`

```php
partyAdminGet($cursor, $page, $session, $limit): \OpenAPI\Client\Model\PartyResponseAdmin[]
```

Get party list for cursor

This endpoint returns a list of all parties for a cursor in administrative representation.  Cursor could be created here: POST /party/admin/search  _accessible without permission_

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\PartyBookingAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$cursor = 'cursor_example'; // string | id of the cursor used for pagination; required if page is set
$page = 56; // int | current page index of the cursor used for pagination; required if cursor is set
$session = 'session_example'; // string | JWT
$limit = 56; // int | amount of results per page (1 ... 100)

try {
    $result = $apiInstance->partyAdminGet($cursor, $page, $session, $limit);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PartyBookingAdminApi->partyAdminGet: ', $e->getMessage(), PHP_EOL;
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

[**\OpenAPI\Client\Model\PartyResponseAdmin[]**](../Model/PartyResponseAdmin.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `partyAdminIdConfigPut()`

```php
partyAdminIdConfigPut($id, $session, $request): \OpenAPI\Client\Model\ModelPartyConfiguration
```

Update party configuration

This endpoint is for updating the configuration of a specific party.  _accessible without permission_  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\PartyBookingAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | party id
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\PartyRequestConfiguration(); // \OpenAPI\Client\Model\PartyRequestConfiguration | party configuration to update

try {
    $result = $apiInstance->partyAdminIdConfigPut($id, $session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PartyBookingAdminApi->partyAdminIdConfigPut: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| party id | |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\PartyRequestConfiguration**](../Model/PartyRequestConfiguration.md)| party configuration to update | |

### Return type

[**\OpenAPI\Client\Model\ModelPartyConfiguration**](../Model/ModelPartyConfiguration.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `partyAdminIdDelete()`

```php
partyAdminIdDelete($id, $session): \OpenAPI\Client\Model\ModelSwagStatusOk
```

Delete party

This endpoint is for deleting a single party.  _accessible without permission_  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\PartyBookingAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | party id
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->partyAdminIdDelete($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PartyBookingAdminApi->partyAdminIdDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| party id | |
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

## `partyAdminIdGet()`

```php
partyAdminIdGet($id, $session): \OpenAPI\Client\Model\PartyResponseAdmin
```

Get party

This endpoint returns a party in admin representation by given id.  _accessible without permission_  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\PartyBookingAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | party id
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->partyAdminIdGet($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PartyBookingAdminApi->partyAdminIdGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| party id | |
| **session** | **string**| JWT | |

### Return type

[**\OpenAPI\Client\Model\PartyResponseAdmin**](../Model/PartyResponseAdmin.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `partyAdminPost()`

```php
partyAdminPost($session, $request): \OpenAPI\Client\Model\PartyResponseAdmin
```

Create party

This endpoint is for creating a new party.  _accessible without permission_  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\PartyBookingAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\PartyRequestAdmin(); // \OpenAPI\Client\Model\PartyRequestAdmin | party to create

try {
    $result = $apiInstance->partyAdminPost($session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PartyBookingAdminApi->partyAdminPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\PartyRequestAdmin**](../Model/PartyRequestAdmin.md)| party to create | |

### Return type

[**\OpenAPI\Client\Model\PartyResponseAdmin**](../Model/PartyResponseAdmin.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `partyAdminSearchPost()`

```php
partyAdminSearchPost($session, $request): \OpenAPI\Client\Model\ModelCursorResponse
```

Create cursor parties

This endpoint returns a cursor for list parties in admin representation with applied filter and sort options. In case of cursor response total will be 0 the status 204 with not content is returned instead.  _accessible without permission_  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\PartyBookingAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\PartyCursorRequestAdmin(); // \OpenAPI\Client\Model\PartyCursorRequestAdmin | options to create cursor

try {
    $result = $apiInstance->partyAdminSearchPost($session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PartyBookingAdminApi->partyAdminSearchPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\PartyCursorRequestAdmin**](../Model/PartyCursorRequestAdmin.md)| options to create cursor | |

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
