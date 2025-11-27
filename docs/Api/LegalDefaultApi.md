# OpenAPI\Client\LegalDefaultApi



All URIs are relative to https://custom.polario.de/api, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**configDefaultLegalGet()**](LegalDefaultApi.md#configDefaultLegalGet) | **GET** /config/default/legal | Get legal |
| [**configDefaultLegalImprintGet()**](LegalDefaultApi.md#configDefaultLegalImprintGet) | **GET** /config/default/legal/imprint | Get imprint |
| [**configDefaultLegalPolicyGet()**](LegalDefaultApi.md#configDefaultLegalPolicyGet) | **GET** /config/default/legal/policy | Get policy |
| [**configDefaultLegalTermsGet()**](LegalDefaultApi.md#configDefaultLegalTermsGet) | **GET** /config/default/legal/terms | Get terms |
| [**configDefaultLegalTrackingGet()**](LegalDefaultApi.md#configDefaultLegalTrackingGet) | **GET** /config/default/legal/tracking | Get tracking legal |


## `configDefaultLegalGet()`

```php
configDefaultLegalGet($if_modified_since, $session): \OpenAPI\Client\Model\ConfigurationLegalResponseDefault
```

Get legal

This endpoint returns the legal information in default representation. The If-Modified-Since header can be used for omitting the output if nothing has changed.  _accessible without permission_  _fully accessible with permission_ : `\"ManageConfiguration\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\LegalDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$if_modified_since = 56; // int | unix timestamp of the last sync
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->configDefaultLegalGet($if_modified_since, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LegalDefaultApi->configDefaultLegalGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **if_modified_since** | **int**| unix timestamp of the last sync | [optional] |
| **session** | **string**| JWT | [optional] |

### Return type

[**\OpenAPI\Client\Model\ConfigurationLegalResponseDefault**](../Model/ConfigurationLegalResponseDefault.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `configDefaultLegalImprintGet()`

```php
configDefaultLegalImprintGet($if_modified_since, $session): \OpenAPI\Client\Model\ConfigurationImprintResponse
```

Get imprint

This endpoint returns the imprint in default representation. The imprint is a html formatted string. The If-Modified-Since header can be used for omitting the output if nothing has changed.  _accessible without permission_  _fully accessible with permission_ : `\"ManageConfiguration\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\LegalDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$if_modified_since = 56; // int | unix timestamp of the last sync
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->configDefaultLegalImprintGet($if_modified_since, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LegalDefaultApi->configDefaultLegalImprintGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **if_modified_since** | **int**| unix timestamp of the last sync | [optional] |
| **session** | **string**| JWT | [optional] |

### Return type

[**\OpenAPI\Client\Model\ConfigurationImprintResponse**](../Model/ConfigurationImprintResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `configDefaultLegalPolicyGet()`

```php
configDefaultLegalPolicyGet($if_modified_since, $session): \OpenAPI\Client\Model\ConfigurationPolicyResponse
```

Get policy

This endpoint returns the policy in default representation. The policy is a html formatted string. The If-Modified-Since header can be used for omitting the output if nothing has changed.  _accessible without permission_  _fully accessible with permission_ : `\"ManageConfiguration\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\LegalDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$if_modified_since = 56; // int | unix timestamp of the last sync
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->configDefaultLegalPolicyGet($if_modified_since, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LegalDefaultApi->configDefaultLegalPolicyGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **if_modified_since** | **int**| unix timestamp of the last sync | [optional] |
| **session** | **string**| JWT | [optional] |

### Return type

[**\OpenAPI\Client\Model\ConfigurationPolicyResponse**](../Model/ConfigurationPolicyResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `configDefaultLegalTermsGet()`

```php
configDefaultLegalTermsGet($if_modified_since, $session): \OpenAPI\Client\Model\ConfigurationTermsResponse
```

Get terms

This endpoint returns the terms in default representation. The terms is a html formatted string. The If-Modified-Since header can be used for omitting the output if nothing has changed.  _accessible without permission_  _fully accessible with permission_ : `\"ManageConfiguration\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\LegalDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$if_modified_since = 56; // int | unix timestamp of the last sync
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->configDefaultLegalTermsGet($if_modified_since, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LegalDefaultApi->configDefaultLegalTermsGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **if_modified_since** | **int**| unix timestamp of the last sync | [optional] |
| **session** | **string**| JWT | [optional] |

### Return type

[**\OpenAPI\Client\Model\ConfigurationTermsResponse**](../Model/ConfigurationTermsResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `configDefaultLegalTrackingGet()`

```php
configDefaultLegalTrackingGet($session): \OpenAPI\Client\Model\ConfigurationTrackingLegalResponse
```

Get tracking legal

This endpoint returns the tracking legal information in default representation. The tracking legal information is a html formatted string.  _accessible without permission_  _fully accessible with permission_ : `\"ManageConfiguration\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\LegalDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->configDefaultLegalTrackingGet($session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LegalDefaultApi->configDefaultLegalTrackingGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **session** | **string**| JWT | [optional] |

### Return type

[**\OpenAPI\Client\Model\ConfigurationTrackingLegalResponse**](../Model/ConfigurationTrackingLegalResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
