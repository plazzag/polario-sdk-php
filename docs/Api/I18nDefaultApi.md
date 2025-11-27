# OpenAPI\Client\I18nDefaultApi



All URIs are relative to https://custom.polario.de/api, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**configDefaultLanguageGet()**](I18nDefaultApi.md#configDefaultLanguageGet) | **GET** /config/default/language | Get languages |
| [**configDefaultLocalizationGet()**](I18nDefaultApi.md#configDefaultLocalizationGet) | **GET** /config/default/localization | Get localizations |


## `configDefaultLanguageGet()`

```php
configDefaultLanguageGet($session): \OpenAPI\Client\Model\LanguageResponseDefault[]
```

Get languages

This endpoint returns all published languages in default representation.  _accessible without permission_  _fully accessible with permission_ : `\"ManageConfiguration\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\I18nDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->configDefaultLanguageGet($session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling I18nDefaultApi->configDefaultLanguageGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **session** | **string**| JWT | [optional] |

### Return type

[**\OpenAPI\Client\Model\LanguageResponseDefault[]**](../Model/LanguageResponseDefault.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `configDefaultLocalizationGet()`

```php
configDefaultLocalizationGet($accept_language, $session): array<string,string>
```

Get localizations

This endpoint returns all localizations either in provided or default language in default representation.  _accessible without permission_  _fully accessible with permission_ : `\"ManageConfiguration\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\I18nDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$accept_language = 'accept_language_example'; // string | client language(s)
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->configDefaultLocalizationGet($accept_language, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling I18nDefaultApi->configDefaultLocalizationGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **accept_language** | **string**| client language(s) | [optional] |
| **session** | **string**| JWT | [optional] |

### Return type

**array<string,string>**

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
