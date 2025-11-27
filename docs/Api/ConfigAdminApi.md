# OpenAPI\Client\ConfigAdminApi



All URIs are relative to https://custom.polario.de/api, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**configAdminDesignCustomCssGet()**](ConfigAdminApi.md#configAdminDesignCustomCssGet) | **GET** /config/admin/design/custom-css | Get Custom CSS |
| [**configAdminDesignCustomCssPatch()**](ConfigAdminApi.md#configAdminDesignCustomCssPatch) | **PATCH** /config/admin/design/custom-css | Update Custom CSS |
| [**configAdminDesignDefaultGet()**](ConfigAdminApi.md#configAdminDesignDefaultGet) | **GET** /config/admin/design/default | Get factory default design |
| [**configAdminDesignGet()**](ConfigAdminApi.md#configAdminDesignGet) | **GET** /config/admin/design | Get design |
| [**configAdminDesignPatch()**](ConfigAdminApi.md#configAdminDesignPatch) | **PATCH** /config/admin/design | Update design |
| [**configAdminDesignSchemeGet()**](ConfigAdminApi.md#configAdminDesignSchemeGet) | **GET** /config/admin/design/scheme | Get schemes list |
| [**configAdminDesignSchemeIdDefaultGet()**](ConfigAdminApi.md#configAdminDesignSchemeIdDefaultGet) | **GET** /config/admin/design/scheme/{id}/default | Get factory default for system scheme |
| [**configAdminDesignSchemeIdDelete()**](ConfigAdminApi.md#configAdminDesignSchemeIdDelete) | **DELETE** /config/admin/design/scheme/{id} | Delete custom scheme |
| [**configAdminDesignSchemeIdGet()**](ConfigAdminApi.md#configAdminDesignSchemeIdGet) | **GET** /config/admin/design/scheme/{id} | Get scheme |
| [**configAdminDesignSchemeIdPatch()**](ConfigAdminApi.md#configAdminDesignSchemeIdPatch) | **PATCH** /config/admin/design/scheme/{id} | Update scheme |
| [**configAdminDesignSchemePost()**](ConfigAdminApi.md#configAdminDesignSchemePost) | **POST** /config/admin/design/scheme | Create custom scheme |
| [**configAdminFeaturesGet()**](ConfigAdminApi.md#configAdminFeaturesGet) | **GET** /config/admin/features | Get features |
| [**configAdminFeaturesPatch()**](ConfigAdminApi.md#configAdminFeaturesPatch) | **PATCH** /config/admin/features | Update features |
| [**configAdminKnowledgeBaseObjectTypeGet()**](ConfigAdminApi.md#configAdminKnowledgeBaseObjectTypeGet) | **GET** /config/admin/knowledge-base/{objectType} | Get knowledge base articles |
| [**configAdminPremiumGet()**](ConfigAdminApi.md#configAdminPremiumGet) | **GET** /config/admin/premium | Get premium features |
| [**configAdminPremiumPatch()**](ConfigAdminApi.md#configAdminPremiumPatch) | **PATCH** /config/admin/premium | Update premium features |
| [**configAdminSecurityDefaultGet()**](ConfigAdminApi.md#configAdminSecurityDefaultGet) | **GET** /config/admin/security/default | Get factory default security settings |
| [**configAdminSecurityGet()**](ConfigAdminApi.md#configAdminSecurityGet) | **GET** /config/admin/security | Get security settings |
| [**configAdminSecurityPatch()**](ConfigAdminApi.md#configAdminSecurityPatch) | **PATCH** /config/admin/security | Update security settings |


## `configAdminDesignCustomCssGet()`

```php
configAdminDesignCustomCssGet($session): \OpenAPI\Client\Model\ConfigurationDesignCustomCSSResponseAdmin
```

Get Custom CSS

This endpoint returns the custom css settings in admin representation.  _only accessible with permission_ : `\"Plazz\"`  _fully accessible with permission_ : `\"Plazz\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\ConfigAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->configAdminDesignCustomCssGet($session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConfigAdminApi->configAdminDesignCustomCssGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **session** | **string**| JWT | |

### Return type

[**\OpenAPI\Client\Model\ConfigurationDesignCustomCSSResponseAdmin**](../Model/ConfigurationDesignCustomCSSResponseAdmin.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `configAdminDesignCustomCssPatch()`

```php
configAdminDesignCustomCssPatch($session, $request): \OpenAPI\Client\Model\ConfigurationDesignCustomCSSResponseAdmin
```

Update Custom CSS

This endpoint updates the custom css settings in admin representation.  _only accessible with permission_ : `\"Plazz\"`  _fully accessible with permission_ : `\"Plazz\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\ConfigAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\ConfigurationDesignCustomCSSRequestAdmin(); // \OpenAPI\Client\Model\ConfigurationDesignCustomCSSRequestAdmin | custom css

try {
    $result = $apiInstance->configAdminDesignCustomCssPatch($session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConfigAdminApi->configAdminDesignCustomCssPatch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\ConfigurationDesignCustomCSSRequestAdmin**](../Model/ConfigurationDesignCustomCSSRequestAdmin.md)| custom css | [optional] |

### Return type

[**\OpenAPI\Client\Model\ConfigurationDesignCustomCSSResponseAdmin**](../Model/ConfigurationDesignCustomCSSResponseAdmin.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `configAdminDesignDefaultGet()`

```php
configAdminDesignDefaultGet($session): \OpenAPI\Client\Model\ConfigurationDesignResponseAdmin
```

Get factory default design

This endpoint returns the default design configuration in administrative representation. This can be used for reset settings to default value.  _accessible without permission_  _fully accessible with permission_ : `\"ManageConfiguration\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\ConfigAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->configAdminDesignDefaultGet($session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConfigAdminApi->configAdminDesignDefaultGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **session** | **string**| JWT | |

### Return type

[**\OpenAPI\Client\Model\ConfigurationDesignResponseAdmin**](../Model/ConfigurationDesignResponseAdmin.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `configAdminDesignGet()`

```php
configAdminDesignGet($session, $if_modified_since): \OpenAPI\Client\Model\ConfigurationDesignResponseAdmin
```

Get design

This endpoint returns the design configuration in administrative representation. The If-Modified-Since header can be used for omitting the output if nothing has changed.  _accessible without permission_  _fully accessible with permission_ : `\"ManageConfiguration\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\ConfigAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT
$if_modified_since = 56; // int | unix timestamp of the last sync

try {
    $result = $apiInstance->configAdminDesignGet($session, $if_modified_since);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConfigAdminApi->configAdminDesignGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **session** | **string**| JWT | |
| **if_modified_since** | **int**| unix timestamp of the last sync | [optional] |

### Return type

[**\OpenAPI\Client\Model\ConfigurationDesignResponseAdmin**](../Model/ConfigurationDesignResponseAdmin.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `configAdminDesignPatch()`

```php
configAdminDesignPatch($session, $if_modified_since, $request): \OpenAPI\Client\Model\ConfigurationDesignResponseAdmin
```

Update design

This endpoint is for updating specific data of the design configuration. The If-Modified-Since header can be used for omitting the request if nothing has changed.  _only accessible with permission_ : `\"ManageConfiguration\"`  _fully accessible with permission_ : `\"ManageConfiguration\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\ConfigAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT
$if_modified_since = 56; // int | unix timestamp
$request = new \OpenAPI\Client\Model\ConfigurationDesignRequestAdmin(); // \OpenAPI\Client\Model\ConfigurationDesignRequestAdmin | design data to be updated

try {
    $result = $apiInstance->configAdminDesignPatch($session, $if_modified_since, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConfigAdminApi->configAdminDesignPatch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **session** | **string**| JWT | |
| **if_modified_since** | **int**| unix timestamp | [optional] |
| **request** | [**\OpenAPI\Client\Model\ConfigurationDesignRequestAdmin**](../Model/ConfigurationDesignRequestAdmin.md)| design data to be updated | [optional] |

### Return type

[**\OpenAPI\Client\Model\ConfigurationDesignResponseAdmin**](../Model/ConfigurationDesignResponseAdmin.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `configAdminDesignSchemeGet()`

```php
configAdminDesignSchemeGet($session, $cursor, $limit, $page, $if_modified_since): \OpenAPI\Client\Model\SchemeResponseAdmin[]
```

Get schemes list

This endpoint returns an array of all scheme. The output is in administrative representation. The _If-Modified-Since_ header can be used for omitting the output if nothing has changed. If a limit is set, a cursor for this endpoint may be created to iterate over all schemes.  _accessible without permission_  _fully accessible with permission_ : `\"ManageConfiguration\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\ConfigAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT
$cursor = 'cursor_example'; // string | id of the cursor used for pagination; required if page is set
$limit = 56; // int | amount of results per page (1 ... 100)
$page = 56; // int | current page index of the cursor used for pagination; required if cursor is set
$if_modified_since = 56; // int | unix timestamp of the last sync

try {
    $result = $apiInstance->configAdminDesignSchemeGet($session, $cursor, $limit, $page, $if_modified_since);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConfigAdminApi->configAdminDesignSchemeGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **session** | **string**| JWT | |
| **cursor** | **string**| id of the cursor used for pagination; required if page is set | [optional] |
| **limit** | **int**| amount of results per page (1 ... 100) | [optional] |
| **page** | **int**| current page index of the cursor used for pagination; required if cursor is set | [optional] |
| **if_modified_since** | **int**| unix timestamp of the last sync | [optional] |

### Return type

[**\OpenAPI\Client\Model\SchemeResponseAdmin[]**](../Model/SchemeResponseAdmin.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `configAdminDesignSchemeIdDefaultGet()`

```php
configAdminDesignSchemeIdDefaultGet($id, $session): \OpenAPI\Client\Model\SchemeResponseAdmin
```

Get factory default for system scheme

This endpoint returns the default data of a system scheme in administrative representation by given id.  _accessible without permission_  _fully accessible with permission_ : `\"ManageConfiguration\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\ConfigAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Scheme ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->configAdminDesignSchemeIdDefaultGet($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConfigAdminApi->configAdminDesignSchemeIdDefaultGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Scheme ID | |
| **session** | **string**| JWT | |

### Return type

[**\OpenAPI\Client\Model\SchemeResponseAdmin**](../Model/SchemeResponseAdmin.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `configAdminDesignSchemeIdDelete()`

```php
configAdminDesignSchemeIdDelete($id, $session, $if_modified_since): \OpenAPI\Client\Model\ModelSwagStatusOk
```

Delete custom scheme

This endpoint is for deleting a single scheme. System schemes are not deletable. The _If-Modified-Since_ header can be used for omitting the request if nothing has changed.  _only accessible with permission_ : `\"ManageConfiguration\"`  _fully accessible with permission_ : `\"ManageConfiguration\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\ConfigAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Scheme ID
$session = 'session_example'; // string | JWT
$if_modified_since = 56; // int | unix timestamp of the last sync

try {
    $result = $apiInstance->configAdminDesignSchemeIdDelete($id, $session, $if_modified_since);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConfigAdminApi->configAdminDesignSchemeIdDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Scheme ID | |
| **session** | **string**| JWT | |
| **if_modified_since** | **int**| unix timestamp of the last sync | [optional] |

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

## `configAdminDesignSchemeIdGet()`

```php
configAdminDesignSchemeIdGet($id, $session, $if_modified_since): \OpenAPI\Client\Model\SchemeResponseAdmin
```

Get scheme

This endpoint returns a scheme in administrative representation by given id. The _If-Modified-Since_ header can be used for omitting the output if nothing has changed.  _accessible without permission_  _fully accessible with permission_ : `\"ManageConfiguration\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\ConfigAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Scheme ID
$session = 'session_example'; // string | JWT
$if_modified_since = 56; // int | unix timestamp of the last sync

try {
    $result = $apiInstance->configAdminDesignSchemeIdGet($id, $session, $if_modified_since);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConfigAdminApi->configAdminDesignSchemeIdGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Scheme ID | |
| **session** | **string**| JWT | |
| **if_modified_since** | **int**| unix timestamp of the last sync | [optional] |

### Return type

[**\OpenAPI\Client\Model\SchemeResponseAdmin**](../Model/SchemeResponseAdmin.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `configAdminDesignSchemeIdPatch()`

```php
configAdminDesignSchemeIdPatch($id, $session, $request, $if_modified_since): \OpenAPI\Client\Model\SchemeResponseAdmin
```

Update scheme

This endpoint is for updating specific data of an existing scheme. The title of system schemes is not editable. The _If-Modified-Since_ header can be used for omitting the request if nothing has changed.  _only accessible with permission_ : `\"ManageConfiguration\"`  _fully accessible with permission_ : `\"ManageConfiguration\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\ConfigAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Scheme ID
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\SchemeRequestAdmin(); // \OpenAPI\Client\Model\SchemeRequestAdmin | scheme to create
$if_modified_since = 56; // int | unix timestamp

try {
    $result = $apiInstance->configAdminDesignSchemeIdPatch($id, $session, $request, $if_modified_since);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConfigAdminApi->configAdminDesignSchemeIdPatch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Scheme ID | |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\SchemeRequestAdmin**](../Model/SchemeRequestAdmin.md)| scheme to create | |
| **if_modified_since** | **int**| unix timestamp | [optional] |

### Return type

[**\OpenAPI\Client\Model\SchemeResponseAdmin**](../Model/SchemeResponseAdmin.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `configAdminDesignSchemePost()`

```php
configAdminDesignSchemePost($session, $request): \OpenAPI\Client\Model\SchemeResponseAdmin
```

Create custom scheme

This endpoint is for creating a new scheme.  _only accessible with permission_ : `\"ManageConfiguration\"`  _fully accessible with permission_ : `\"ManageConfiguration\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\ConfigAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\SchemeRequestAdmin(); // \OpenAPI\Client\Model\SchemeRequestAdmin | scheme to create

try {
    $result = $apiInstance->configAdminDesignSchemePost($session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConfigAdminApi->configAdminDesignSchemePost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\SchemeRequestAdmin**](../Model/SchemeRequestAdmin.md)| scheme to create | |

### Return type

[**\OpenAPI\Client\Model\SchemeResponseAdmin**](../Model/SchemeResponseAdmin.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `configAdminFeaturesGet()`

```php
configAdminFeaturesGet($session): \OpenAPI\Client\Model\ConfigurationFeaturesResponseAdmin
```

Get features

This endpoint returns the features configuration in admin representation. The If-Modified-Since header can be used for omitting the output if nothing has changed.  _accessible without permission_  _fully accessible with permission_ : `\"ManageConfiguration\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\ConfigAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->configAdminFeaturesGet($session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConfigAdminApi->configAdminFeaturesGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **session** | **string**| JWT | |

### Return type

[**\OpenAPI\Client\Model\ConfigurationFeaturesResponseAdmin**](../Model/ConfigurationFeaturesResponseAdmin.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `configAdminFeaturesPatch()`

```php
configAdminFeaturesPatch($session, $request): \OpenAPI\Client\Model\ConfigurationPatchFeaturesResponseAdmin
```

Update features

This endpoint is for updating the features configuration. The If-Modified-Since header can be used for omitting the request if nothing has changed.  _only accessible with permission_ : `\"ManageConfiguration\"`  _fully accessible with permission_ : `\"ManageConfiguration\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\ConfigAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\ConfigurationPatchFeaturesRequestAdmin(); // \OpenAPI\Client\Model\ConfigurationPatchFeaturesRequestAdmin | features data to be updated

try {
    $result = $apiInstance->configAdminFeaturesPatch($session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConfigAdminApi->configAdminFeaturesPatch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\ConfigurationPatchFeaturesRequestAdmin**](../Model/ConfigurationPatchFeaturesRequestAdmin.md)| features data to be updated | [optional] |

### Return type

[**\OpenAPI\Client\Model\ConfigurationPatchFeaturesResponseAdmin**](../Model/ConfigurationPatchFeaturesResponseAdmin.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `configAdminKnowledgeBaseObjectTypeGet()`

```php
configAdminKnowledgeBaseObjectTypeGet($object_type, $session): array<string,\OpenAPI\Client\Model\KnowledgebaseFolder>
```

Get knowledge base articles

This endpoint returns all articles for a objectType in de and en  This keys of the object represents the language codes (de-DE|en-US).  _accessible without permission_

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\ConfigAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$object_type = 'object_type_example'; // string | objectType
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->configAdminKnowledgeBaseObjectTypeGet($object_type, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConfigAdminApi->configAdminKnowledgeBaseObjectTypeGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **object_type** | **string**| objectType | |
| **session** | **string**| JWT | |

### Return type

[**array<string,\OpenAPI\Client\Model\KnowledgebaseFolder>**](../Model/KnowledgebaseFolder.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `configAdminPremiumGet()`

```php
configAdminPremiumGet($session): \OpenAPI\Client\Model\ConfigurationPremiumResponseAdmin
```

Get premium features

This endpoint returns the premium configuration in admin representation.  _accessible without permission_  _fully accessible with permission_ : `\"Plazz\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\ConfigAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->configAdminPremiumGet($session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConfigAdminApi->configAdminPremiumGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **session** | **string**| JWT | |

### Return type

[**\OpenAPI\Client\Model\ConfigurationPremiumResponseAdmin**](../Model/ConfigurationPremiumResponseAdmin.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `configAdminPremiumPatch()`

```php
configAdminPremiumPatch($session, $request): \OpenAPI\Client\Model\ConfigurationPremiumResponseAdmin
```

Update premium features

This endpoint updates the premium configuration.  _only accessible with permission_ : `\"Plazz\"`  _fully accessible with permission_ : `\"Plazz\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\ConfigAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\ConfigurationPremiumRequest(); // \OpenAPI\Client\Model\ConfigurationPremiumRequest | premium configuration to be updated

try {
    $result = $apiInstance->configAdminPremiumPatch($session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConfigAdminApi->configAdminPremiumPatch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\ConfigurationPremiumRequest**](../Model/ConfigurationPremiumRequest.md)| premium configuration to be updated | [optional] |

### Return type

[**\OpenAPI\Client\Model\ConfigurationPremiumResponseAdmin**](../Model/ConfigurationPremiumResponseAdmin.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `configAdminSecurityDefaultGet()`

```php
configAdminSecurityDefaultGet($session): \OpenAPI\Client\Model\ConfigurationSecurityResponseAdmin
```

Get factory default security settings

This endpoint returns the default security configuration in administrative representation. This can be used for reset settings to default value.  _accessible without permission_  _fully accessible with permission_ : `\"ManageConfiguration\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\ConfigAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->configAdminSecurityDefaultGet($session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConfigAdminApi->configAdminSecurityDefaultGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **session** | **string**| JWT | |

### Return type

[**\OpenAPI\Client\Model\ConfigurationSecurityResponseAdmin**](../Model/ConfigurationSecurityResponseAdmin.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `configAdminSecurityGet()`

```php
configAdminSecurityGet($session, $if_modified_since): \OpenAPI\Client\Model\ConfigurationSecurityResponseAdmin
```

Get security settings

This endpoint returns the security configuration in administrative representation. This endpoint returns the security configuration in administrative representation. The If-Modified-Since header can be used for omitting the output if nothing has changed.  _accessible without permission_  _fully accessible with permission_ : `\"ManageConfiguration\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\ConfigAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT
$if_modified_since = 56; // int | unix timestamp of the last sync

try {
    $result = $apiInstance->configAdminSecurityGet($session, $if_modified_since);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConfigAdminApi->configAdminSecurityGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **session** | **string**| JWT | |
| **if_modified_since** | **int**| unix timestamp of the last sync | [optional] |

### Return type

[**\OpenAPI\Client\Model\ConfigurationSecurityResponseAdmin**](../Model/ConfigurationSecurityResponseAdmin.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `configAdminSecurityPatch()`

```php
configAdminSecurityPatch($session, $if_modified_since, $request): \OpenAPI\Client\Model\ConfigurationSecurityResponseAdmin
```

Update security settings

This endpoint is for updating specific data of the security configuration. The If-Modified-Since header can be used for omitting the request if nothing has changed.  _only accessible with permission_ : `\"ManageConfiguration\"`  _fully accessible with permission_ : `\"ManageConfiguration\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\ConfigAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT
$if_modified_since = 56; // int | unix timestamp
$request = new \OpenAPI\Client\Model\ConfigurationSecurityRequestAdmin(); // \OpenAPI\Client\Model\ConfigurationSecurityRequestAdmin | security data to be updated

try {
    $result = $apiInstance->configAdminSecurityPatch($session, $if_modified_since, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConfigAdminApi->configAdminSecurityPatch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **session** | **string**| JWT | |
| **if_modified_since** | **int**| unix timestamp | [optional] |
| **request** | [**\OpenAPI\Client\Model\ConfigurationSecurityRequestAdmin**](../Model/ConfigurationSecurityRequestAdmin.md)| security data to be updated | [optional] |

### Return type

[**\OpenAPI\Client\Model\ConfigurationSecurityResponseAdmin**](../Model/ConfigurationSecurityResponseAdmin.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
