# OpenAPI\Client\EmailAdminApi



All URIs are relative to https://custom.polario.de/api, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**notificationAdminEmailIdDelete()**](EmailAdminApi.md#notificationAdminEmailIdDelete) | **DELETE** /notification/admin/email/{id} | Delete email |
| [**notificationAdminEmailIdGet()**](EmailAdminApi.md#notificationAdminEmailIdGet) | **GET** /notification/admin/email/{id} | Get email |
| [**notificationAdminEmailIdPatch()**](EmailAdminApi.md#notificationAdminEmailIdPatch) | **PATCH** /notification/admin/email/{id} | Update email |
| [**notificationAdminEmailPost()**](EmailAdminApi.md#notificationAdminEmailPost) | **POST** /notification/admin/email | Create email |
| [**notificationAdminEmailProjectIdGet()**](EmailAdminApi.md#notificationAdminEmailProjectIdGet) | **GET** /notification/admin/email/project/{id} | Get all project emails |
| [**notificationAdminEmailTestPost()**](EmailAdminApi.md#notificationAdminEmailTestPost) | **POST** /notification/admin/email/test | Test email content |


## `notificationAdminEmailIdDelete()`

```php
notificationAdminEmailIdDelete($id, $session): \OpenAPI\Client\Model\ModelSwagStatusOk
```

Delete email

This endpoint is for deleting an email with all localizations.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\EmailAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Email ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->notificationAdminEmailIdDelete($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EmailAdminApi->notificationAdminEmailIdDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Email ID | |
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

## `notificationAdminEmailIdGet()`

```php
notificationAdminEmailIdGet($id, $session): \OpenAPI\Client\Model\NotificationEmailResponseAdmin
```

Get email

This endpoint returns email in admin representation.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\EmailAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Email ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->notificationAdminEmailIdGet($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EmailAdminApi->notificationAdminEmailIdGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Email ID | |
| **session** | **string**| JWT | |

### Return type

[**\OpenAPI\Client\Model\NotificationEmailResponseAdmin**](../Model/NotificationEmailResponseAdmin.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `notificationAdminEmailIdPatch()`

```php
notificationAdminEmailIdPatch($id, $session, $request): \OpenAPI\Client\Model\NotificationEmailResponseAdmin
```

Update email

This endpoint is for updating email.  If the email is already published, it cannot be updated.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\EmailAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Email ID
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\NotificationPatchEmailRequest(); // \OpenAPI\Client\Model\NotificationPatchEmailRequest | email information to be updated

try {
    $result = $apiInstance->notificationAdminEmailIdPatch($id, $session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EmailAdminApi->notificationAdminEmailIdPatch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Email ID | |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\NotificationPatchEmailRequest**](../Model/NotificationPatchEmailRequest.md)| email information to be updated | |

### Return type

[**\OpenAPI\Client\Model\NotificationEmailResponseAdmin**](../Model/NotificationEmailResponseAdmin.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `notificationAdminEmailPost()`

```php
notificationAdminEmailPost($session, $request): \OpenAPI\Client\Model\NotificationEmailResponseAdmin
```

Create email

This endpoint is for creating a new email.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\EmailAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\NotificationPostEmailRequest(); // \OpenAPI\Client\Model\NotificationPostEmailRequest | email to create

try {
    $result = $apiInstance->notificationAdminEmailPost($session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EmailAdminApi->notificationAdminEmailPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\NotificationPostEmailRequest**](../Model/NotificationPostEmailRequest.md)| email to create | |

### Return type

[**\OpenAPI\Client\Model\NotificationEmailResponseAdmin**](../Model/NotificationEmailResponseAdmin.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `notificationAdminEmailProjectIdGet()`

```php
notificationAdminEmailProjectIdGet($id, $session, $cursor, $limit, $page): \OpenAPI\Client\Model\NotificationEmailResponseAdmin[]
```

Get all project emails

This endpoint returns all emails in admin representation for a project. If a limit is set, a cursor for this endpoint may be created to iterate over all emails.  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\EmailAdminApi(
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
    $result = $apiInstance->notificationAdminEmailProjectIdGet($id, $session, $cursor, $limit, $page);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EmailAdminApi->notificationAdminEmailProjectIdGet: ', $e->getMessage(), PHP_EOL;
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

[**\OpenAPI\Client\Model\NotificationEmailResponseAdmin[]**](../Model/NotificationEmailResponseAdmin.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `notificationAdminEmailTestPost()`

```php
notificationAdminEmailTestPost($session, $request, $accept_language): \OpenAPI\Client\Model\ModelSwagStatusOk
```

Test email content

This endpoint is for testing email data.  __Note:__ email will send without attachments if attachments exceed limit of 16MiB (16.7MB)  _only accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\EmailAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\NotificationTestEmailContentRequest(); // \OpenAPI\Client\Model\NotificationTestEmailContentRequest | email data to be tested
$accept_language = 'accept_language_example'; // string | client language(s)

try {
    $result = $apiInstance->notificationAdminEmailTestPost($session, $request, $accept_language);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EmailAdminApi->notificationAdminEmailTestPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\NotificationTestEmailContentRequest**](../Model/NotificationTestEmailContentRequest.md)| email data to be tested | |
| **accept_language** | **string**| client language(s) | [optional] |

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
