# OpenAPI\Client\PartyAdminApi



All URIs are relative to https://custom.polario.de/api, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**partyAdminGet()**](PartyAdminApi.md#partyAdminGet) | **GET** /party/admin | Get party list for cursor |
| [**partyAdminIdConfigPut()**](PartyAdminApi.md#partyAdminIdConfigPut) | **PUT** /party/admin/{id}/config | Update party configuration |
| [**partyAdminIdDelete()**](PartyAdminApi.md#partyAdminIdDelete) | **DELETE** /party/admin/{id} | Delete party |
| [**partyAdminIdGet()**](PartyAdminApi.md#partyAdminIdGet) | **GET** /party/admin/{id} | Get party |
| [**partyAdminIdReactionPost()**](PartyAdminApi.md#partyAdminIdReactionPost) | **POST** /party/admin/{id}/reaction | Create reaction |
| [**partyAdminPost()**](PartyAdminApi.md#partyAdminPost) | **POST** /party/admin | Create party |
| [**partyAdminReactionGet()**](PartyAdminApi.md#partyAdminReactionGet) | **GET** /party/admin/reaction | Get reaction list for cursor |
| [**partyAdminReactionIdDelete()**](PartyAdminApi.md#partyAdminReactionIdDelete) | **DELETE** /party/admin/reaction/{id} | Delete reaction |
| [**partyAdminReactionIdPut()**](PartyAdminApi.md#partyAdminReactionIdPut) | **PUT** /party/admin/reaction/{id} | Update reaction |
| [**partyAdminReactionSearchPost()**](PartyAdminApi.md#partyAdminReactionSearchPost) | **POST** /party/admin/reaction/search | Create cursor |
| [**partyAdminSearchPost()**](PartyAdminApi.md#partyAdminSearchPost) | **POST** /party/admin/search | Create cursor |


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



$apiInstance = new OpenAPI\Client\Api\PartyAdminApi(
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
    echo 'Exception when calling PartyAdminApi->partyAdminGet: ', $e->getMessage(), PHP_EOL;
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



$apiInstance = new OpenAPI\Client\Api\PartyAdminApi(
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
    echo 'Exception when calling PartyAdminApi->partyAdminIdConfigPut: ', $e->getMessage(), PHP_EOL;
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



$apiInstance = new OpenAPI\Client\Api\PartyAdminApi(
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
    echo 'Exception when calling PartyAdminApi->partyAdminIdDelete: ', $e->getMessage(), PHP_EOL;
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



$apiInstance = new OpenAPI\Client\Api\PartyAdminApi(
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
    echo 'Exception when calling PartyAdminApi->partyAdminIdGet: ', $e->getMessage(), PHP_EOL;
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

## `partyAdminIdReactionPost()`

```php
partyAdminIdReactionPost($id, $session, $request): \OpenAPI\Client\Model\ReactionResponseAdmin
```

Create reaction

This endpoint is for creating a new reaction.  _only accessible with permission_ : `\"ManageAccounts\"`  _fully accessible with permission_ : `\"ManageAccounts\"` + `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\PartyAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | party id
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\ReactionRequestAdmin(); // \OpenAPI\Client\Model\ReactionRequestAdmin | reaction to create

try {
    $result = $apiInstance->partyAdminIdReactionPost($id, $session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PartyAdminApi->partyAdminIdReactionPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| party id | |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\ReactionRequestAdmin**](../Model/ReactionRequestAdmin.md)| reaction to create | |

### Return type

[**\OpenAPI\Client\Model\ReactionResponseAdmin**](../Model/ReactionResponseAdmin.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
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



$apiInstance = new OpenAPI\Client\Api\PartyAdminApi(
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
    echo 'Exception when calling PartyAdminApi->partyAdminPost: ', $e->getMessage(), PHP_EOL;
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

## `partyAdminReactionGet()`

```php
partyAdminReactionGet($cursor, $page, $session, $limit): \OpenAPI\Client\Model\ReactionResponseAdmin[]
```

Get reaction list for cursor

This endpoint returns a list of all reactions for a cursor in administrative representation.  Cursor could be created here: POST /party/admin/reaction/search  _accessible without permission_

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\PartyAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$cursor = 'cursor_example'; // string | id of the cursor used for pagination; required if page is set
$page = 56; // int | current page index of the cursor used for pagination; required if cursor is set
$session = 'session_example'; // string | JWT
$limit = 56; // int | amount of results per page (1 ... 100)

try {
    $result = $apiInstance->partyAdminReactionGet($cursor, $page, $session, $limit);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PartyAdminApi->partyAdminReactionGet: ', $e->getMessage(), PHP_EOL;
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

[**\OpenAPI\Client\Model\ReactionResponseAdmin[]**](../Model/ReactionResponseAdmin.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `partyAdminReactionIdDelete()`

```php
partyAdminReactionIdDelete($id, $session): \OpenAPI\Client\Model\ModelSwagStatusOk
```

Delete reaction

This endpoint is for deleting a single reaction.  _only accessible with permission_ : `\"ManageAccounts\"`  _fully accessible with permission_ : `\"ManageAccounts\"` + `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\PartyAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | reaction id
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->partyAdminReactionIdDelete($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PartyAdminApi->partyAdminReactionIdDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| reaction id | |
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

## `partyAdminReactionIdPut()`

```php
partyAdminReactionIdPut($id, $session, $request): \OpenAPI\Client\Model\ReactionResponseAdmin
```

Update reaction

This endpoint is for updating a specific reaction.  _only accessible with permission_ : `\"ManageAccounts\"`  _fully accessible with permission_ : `\"ManageAccounts\"` + `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\PartyAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | reaction id
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\ReactionRequest(); // \OpenAPI\Client\Model\ReactionRequest | reaction to update

try {
    $result = $apiInstance->partyAdminReactionIdPut($id, $session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PartyAdminApi->partyAdminReactionIdPut: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| reaction id | |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\ReactionRequest**](../Model/ReactionRequest.md)| reaction to update | |

### Return type

[**\OpenAPI\Client\Model\ReactionResponseAdmin**](../Model/ReactionResponseAdmin.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `partyAdminReactionSearchPost()`

```php
partyAdminReactionSearchPost($session, $request): \OpenAPI\Client\Model\ModelCursorResponse
```

Create cursor

This endpoint returns a cursor for list reactions in admin representation with applied filter and sort options. In case of cursor response total will be 0 the status 204 with not content is returned instead.  _only accessible with permission_ : `\"ManageAccounts\"`  _fully accessible with permission_ : `\"ManageAccounts\"` + `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\PartyAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\GitPlazzNetReposSandmannBackendServicesPartyReactionCursorRequestAdmin(); // \OpenAPI\Client\Model\GitPlazzNetReposSandmannBackendServicesPartyReactionCursorRequestAdmin | options to create cursor

try {
    $result = $apiInstance->partyAdminReactionSearchPost($session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PartyAdminApi->partyAdminReactionSearchPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\GitPlazzNetReposSandmannBackendServicesPartyReactionCursorRequestAdmin**](../Model/GitPlazzNetReposSandmannBackendServicesPartyReactionCursorRequestAdmin.md)| options to create cursor | |

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

## `partyAdminSearchPost()`

```php
partyAdminSearchPost($session, $request): \OpenAPI\Client\Model\ModelCursorResponse
```

Create cursor

This endpoint returns a cursor for list parties in admin representation with applied filter and sort options. In case of cursor response total will be 0 the status 204 with not content is returned instead.  _accessible without permission_  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\PartyAdminApi(
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
    echo 'Exception when calling PartyAdminApi->partyAdminSearchPost: ', $e->getMessage(), PHP_EOL;
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
