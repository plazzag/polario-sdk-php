# OpenAPI\Client\LegalAdminApi



All URIs are relative to https://custom.polario.de/api, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**configAdminLegalGet()**](LegalAdminApi.md#configAdminLegalGet) | **GET** /config/admin/legal | Get legal |
| [**configAdminLegalImprintGet()**](LegalAdminApi.md#configAdminLegalImprintGet) | **GET** /config/admin/legal/imprint | Get imprint |
| [**configAdminLegalImprintPut()**](LegalAdminApi.md#configAdminLegalImprintPut) | **PUT** /config/admin/legal/imprint | Update imprint |
| [**configAdminLegalPatch()**](LegalAdminApi.md#configAdminLegalPatch) | **PATCH** /config/admin/legal | Update legal |
| [**configAdminLegalPolicyGet()**](LegalAdminApi.md#configAdminLegalPolicyGet) | **GET** /config/admin/legal/policy | Get policy |
| [**configAdminLegalPolicyPut()**](LegalAdminApi.md#configAdminLegalPolicyPut) | **PUT** /config/admin/legal/policy | Update policy |
| [**configAdminLegalTermsGet()**](LegalAdminApi.md#configAdminLegalTermsGet) | **GET** /config/admin/legal/terms | Get terms |
| [**configAdminLegalTermsPut()**](LegalAdminApi.md#configAdminLegalTermsPut) | **PUT** /config/admin/legal/terms | Update terms |


## `configAdminLegalGet()`

```php
configAdminLegalGet($session, $if_modified_since): \OpenAPI\Client\Model\ConfigurationLegalResponseAdmin
```

Get legal

This endpoint returns the legal information in administrative representation. The If-Modified-Since header can be used for omitting the output if nothing has changed.  _accessible without permission_  _fully accessible with permission_ : `\"ManageConfiguration\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\LegalAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT
$if_modified_since = 56; // int | unix timestamp of the last sync

try {
    $result = $apiInstance->configAdminLegalGet($session, $if_modified_since);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LegalAdminApi->configAdminLegalGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **session** | **string**| JWT | |
| **if_modified_since** | **int**| unix timestamp of the last sync | [optional] |

### Return type

[**\OpenAPI\Client\Model\ConfigurationLegalResponseAdmin**](../Model/ConfigurationLegalResponseAdmin.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `configAdminLegalImprintGet()`

```php
configAdminLegalImprintGet($session, $if_modified_since): \OpenAPI\Client\Model\ConfigurationImprintResponse
```

Get imprint

This endpoint returns the imprint in administrative representation. The imprint is a html formatted string. The If-Modified-Since header can be used for omitting the output if nothing has changed.  _accessible without permission_  _fully accessible with permission_ : `\"ManageConfiguration\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\LegalAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT
$if_modified_since = 56; // int | unix timestamp of the last sync

try {
    $result = $apiInstance->configAdminLegalImprintGet($session, $if_modified_since);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LegalAdminApi->configAdminLegalImprintGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **session** | **string**| JWT | |
| **if_modified_since** | **int**| unix timestamp of the last sync | [optional] |

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

## `configAdminLegalImprintPut()`

```php
configAdminLegalImprintPut($session, $request): \OpenAPI\Client\Model\ConfigurationImprintResponse
```

Update imprint

This endpoint is for replacing the imprint. The imprint can be a html formatted string.  _only accessible with permission_ : `\"ManageConfiguration\"`  _fully accessible with permission_ : `\"ManageConfiguration\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\LegalAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\ConfigurationImprintRequestAdmin(); // \OpenAPI\Client\Model\ConfigurationImprintRequestAdmin | imprint to be replaced

try {
    $result = $apiInstance->configAdminLegalImprintPut($session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LegalAdminApi->configAdminLegalImprintPut: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\ConfigurationImprintRequestAdmin**](../Model/ConfigurationImprintRequestAdmin.md)| imprint to be replaced | [optional] |

### Return type

[**\OpenAPI\Client\Model\ConfigurationImprintResponse**](../Model/ConfigurationImprintResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `configAdminLegalPatch()`

```php
configAdminLegalPatch($session, $if_modified_since, $request): \OpenAPI\Client\Model\ConfigurationLegalResponseAdmin
```

Update legal

This endpoint is for updating specific data of the legal information. The If-Modified-Since header can be used for omitting the output if nothing has changed.  _only accessible with permission_ : `\"ManageConfiguration\"`  _fully accessible with permission_ : `\"ManageConfiguration\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\LegalAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT
$if_modified_since = 56; // int | unix timestamp of the last sync
$request = new \OpenAPI\Client\Model\ConfigurationLegalRequestAdmin(); // \OpenAPI\Client\Model\ConfigurationLegalRequestAdmin | legal information to be updated

try {
    $result = $apiInstance->configAdminLegalPatch($session, $if_modified_since, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LegalAdminApi->configAdminLegalPatch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **session** | **string**| JWT | |
| **if_modified_since** | **int**| unix timestamp of the last sync | [optional] |
| **request** | [**\OpenAPI\Client\Model\ConfigurationLegalRequestAdmin**](../Model/ConfigurationLegalRequestAdmin.md)| legal information to be updated | [optional] |

### Return type

[**\OpenAPI\Client\Model\ConfigurationLegalResponseAdmin**](../Model/ConfigurationLegalResponseAdmin.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `configAdminLegalPolicyGet()`

```php
configAdminLegalPolicyGet($session, $if_modified_since): \OpenAPI\Client\Model\ConfigurationPolicyResponse
```

Get policy

This endpoint returns the policy in administrative representation. The policy is a html formatted string. The If-Modified-Since header can be used for omitting the output if nothing has changed.  _accessible without permission_  _fully accessible with permission_ : `\"ManageConfiguration\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\LegalAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT
$if_modified_since = 56; // int | unix timestamp of the last sync

try {
    $result = $apiInstance->configAdminLegalPolicyGet($session, $if_modified_since);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LegalAdminApi->configAdminLegalPolicyGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **session** | **string**| JWT | |
| **if_modified_since** | **int**| unix timestamp of the last sync | [optional] |

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

## `configAdminLegalPolicyPut()`

```php
configAdminLegalPolicyPut($session, $request): \OpenAPI\Client\Model\ConfigurationPolicyResponse
```

Update policy

This endpoint is for replacing the policy. The policy can be a html formatted string.  _only accessible with permission_ : `\"ManageConfiguration\"`  _fully accessible with permission_ : `\"ManageConfiguration\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\LegalAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\ConfigurationPolicyRequestAdmin(); // \OpenAPI\Client\Model\ConfigurationPolicyRequestAdmin | policy to be replaced

try {
    $result = $apiInstance->configAdminLegalPolicyPut($session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LegalAdminApi->configAdminLegalPolicyPut: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\ConfigurationPolicyRequestAdmin**](../Model/ConfigurationPolicyRequestAdmin.md)| policy to be replaced | [optional] |

### Return type

[**\OpenAPI\Client\Model\ConfigurationPolicyResponse**](../Model/ConfigurationPolicyResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `configAdminLegalTermsGet()`

```php
configAdminLegalTermsGet($session, $if_modified_since): \OpenAPI\Client\Model\ConfigurationTermsResponse
```

Get terms

This endpoint returns the terms in administrative representation. The terms is a html formatted string. The If-Modified-Since header can be used for omitting the output if nothing has changed.  _accessible without permission_  _fully accessible with permission_ : `\"ManageConfiguration\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\LegalAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT
$if_modified_since = 56; // int | unix timestamp of the last sync

try {
    $result = $apiInstance->configAdminLegalTermsGet($session, $if_modified_since);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LegalAdminApi->configAdminLegalTermsGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **session** | **string**| JWT | |
| **if_modified_since** | **int**| unix timestamp of the last sync | [optional] |

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

## `configAdminLegalTermsPut()`

```php
configAdminLegalTermsPut($session, $request): \OpenAPI\Client\Model\ConfigurationTermsResponse
```

Update terms

This endpoint is for replacing the terms. The terms can be a html formatted string.  _only accessible with permission_ : `\"ManageConfiguration\"`  _fully accessible with permission_ : `\"ManageConfiguration\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\LegalAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\ConfigurationTermsRequestAdmin(); // \OpenAPI\Client\Model\ConfigurationTermsRequestAdmin | terms to be replaced

try {
    $result = $apiInstance->configAdminLegalTermsPut($session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LegalAdminApi->configAdminLegalTermsPut: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\ConfigurationTermsRequestAdmin**](../Model/ConfigurationTermsRequestAdmin.md)| terms to be replaced | [optional] |

### Return type

[**\OpenAPI\Client\Model\ConfigurationTermsResponse**](../Model/ConfigurationTermsResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
