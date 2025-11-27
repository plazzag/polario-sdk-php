# OpenAPI\Client\MenuDefaultApi



All URIs are relative to https://custom.polario.de/api, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**menuDefaultProjectIdGet()**](MenuDefaultApi.md#menuDefaultProjectIdGet) | **GET** /menu/default/project/{id} | Get menu for project |


## `menuDefaultProjectIdGet()`

```php
menuDefaultProjectIdGet($id, $accept_language, $platform, $session): \OpenAPI\Client\Model\MenuDefaultProjectIdGet200Response
```

Get menu for project

This endpoint returns the menu for a specific project. The output is in default representation. The _Platform_ header is for filtering menu items for the correct platform. If the requested language is not available it will fall back to the default language.  ___content.search.objectTypes___: enums limited to: `\"Calendar\"` `\"CalendarEntry\"` `\"ChatFeed\"` `\"Directory\"` `\"DirectoryContentRow\"` `\"Location\"` `\"LocationMap\"` `\"MediaAudio\"` `\"MediaDocument\"` `\"MediaFolder\"` `\"MediaIcon\"` `\"MediaImage\"` `\"MediaOther\"` `\"MediaVideo\"` `\"News\"` `\"Page\"` `\"Project\"` `\"Stream\"`  _accessible without permission_  _fully accessible with permission_ : `\"ManageContent\"` `\"ManageProjects\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\MenuDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Project ID
$accept_language = 'accept_language_example'; // string | client language(s)
$platform = 'platform_example'; // string | The client platform
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->menuDefaultProjectIdGet($id, $accept_language, $platform, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MenuDefaultApi->menuDefaultProjectIdGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Project ID | |
| **accept_language** | **string**| client language(s) | [optional] |
| **platform** | **string**| The client platform | [optional] |
| **session** | **string**| JWT | [optional] |

### Return type

[**\OpenAPI\Client\Model\MenuDefaultProjectIdGet200Response**](../Model/MenuDefaultProjectIdGet200Response.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
