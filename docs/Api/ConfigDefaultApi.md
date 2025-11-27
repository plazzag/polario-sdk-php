# OpenAPI\Client\ConfigDefaultApi



All URIs are relative to https://custom.polario.de/api, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**configDefaultDesignGet()**](ConfigDefaultApi.md#configDefaultDesignGet) | **GET** /config/default/design | Get design |
| [**configDefaultDesignSchemeIdGet()**](ConfigDefaultApi.md#configDefaultDesignSchemeIdGet) | **GET** /config/default/design/scheme/{id} | Get scheme |
| [**configDefaultFeaturesGet()**](ConfigDefaultApi.md#configDefaultFeaturesGet) | **GET** /config/default/features | Get features |
| [**configDefaultPremiumGet()**](ConfigDefaultApi.md#configDefaultPremiumGet) | **GET** /config/default/premium | Get premium features |
| [**configDefaultSecurityGet()**](ConfigDefaultApi.md#configDefaultSecurityGet) | **GET** /config/default/security | Get security settings |


## `configDefaultDesignGet()`

```php
configDefaultDesignGet($if_modified_since, $session): \OpenAPI\Client\Model\ConfigurationDesignResponseDefault
```

Get design

This endpoint returns the design configuration in default representation. The If-Modified-Since header can be used for omitting the output if nothing has changed.  _accessible without permission_  _fully accessible with permission_ : `\"ManageConfiguration\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\ConfigDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$if_modified_since = 56; // int | unix timestamp of the last sync
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->configDefaultDesignGet($if_modified_since, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConfigDefaultApi->configDefaultDesignGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **if_modified_since** | **int**| unix timestamp of the last sync | [optional] |
| **session** | **string**| JWT | [optional] |

### Return type

[**\OpenAPI\Client\Model\ConfigurationDesignResponseDefault**](../Model/ConfigurationDesignResponseDefault.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `configDefaultDesignSchemeIdGet()`

```php
configDefaultDesignSchemeIdGet($id, $session, $if_modified_since): \OpenAPI\Client\Model\SchemeResponseDefault
```

Get scheme

This endpoint returns a scheme in default representation by given id. The _If-Modified-Since_ header can be used for omitting the output if nothing has changed.  _accessible without permission_  _fully accessible with permission_ : `\"ManageConfiguration\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\ConfigDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Scheme ID
$session = 'session_example'; // string | JWT
$if_modified_since = 56; // int | unix timestamp of the last sync

try {
    $result = $apiInstance->configDefaultDesignSchemeIdGet($id, $session, $if_modified_since);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConfigDefaultApi->configDefaultDesignSchemeIdGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Scheme ID | |
| **session** | **string**| JWT | [optional] |
| **if_modified_since** | **int**| unix timestamp of the last sync | [optional] |

### Return type

[**\OpenAPI\Client\Model\SchemeResponseDefault**](../Model/SchemeResponseDefault.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `configDefaultFeaturesGet()`

```php
configDefaultFeaturesGet($session): \OpenAPI\Client\Model\ConfigurationFeaturesResponseDefault
```

Get features

This endpoint returns the features configuration in default representation. The If-Modified-Since header can be used for omitting the output if nothing has changed.  _accessible without permission_  _fully accessible with permission_ : `\"ManageConfiguration\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\ConfigDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->configDefaultFeaturesGet($session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConfigDefaultApi->configDefaultFeaturesGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **session** | **string**| JWT | [optional] |

### Return type

[**\OpenAPI\Client\Model\ConfigurationFeaturesResponseDefault**](../Model/ConfigurationFeaturesResponseDefault.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `configDefaultPremiumGet()`

```php
configDefaultPremiumGet($session): \OpenAPI\Client\Model\ConfigurationPremiumResponseDefault
```

Get premium features

This endpoint returns the premium configuration in default representation.  _accessible without permission_  _fully accessible with permission_ : `\"Plazz\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\ConfigDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->configDefaultPremiumGet($session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConfigDefaultApi->configDefaultPremiumGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **session** | **string**| JWT | |

### Return type

[**\OpenAPI\Client\Model\ConfigurationPremiumResponseDefault**](../Model/ConfigurationPremiumResponseDefault.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `configDefaultSecurityGet()`

```php
configDefaultSecurityGet($if_modified_since, $session): \OpenAPI\Client\Model\ConfigurationSecurityResponseDefault
```

Get security settings

This endpoint returns the security configuration in default representation. The If-Modified-Since header can be used for omitting the output if nothing has changed.  _accessible without permission_  _fully accessible with permission_ : `\"ManageConfiguration\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\ConfigDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$if_modified_since = 56; // int | unix timestamp of the last sync
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->configDefaultSecurityGet($if_modified_since, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConfigDefaultApi->configDefaultSecurityGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **if_modified_since** | **int**| unix timestamp of the last sync | [optional] |
| **session** | **string**| JWT | [optional] |

### Return type

[**\OpenAPI\Client\Model\ConfigurationSecurityResponseDefault**](../Model/ConfigurationSecurityResponseDefault.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
