# OpenAPI\Client\I18nAdminApi



All URIs are relative to https://custom.polario.de/api, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**configAdminLanguageDefaultPut()**](I18nAdminApi.md#configAdminLanguageDefaultPut) | **PUT** /config/admin/language/default | Update default language |
| [**configAdminLanguageGet()**](I18nAdminApi.md#configAdminLanguageGet) | **GET** /config/admin/language | Get languages |
| [**configAdminLanguageIdGet()**](I18nAdminApi.md#configAdminLanguageIdGet) | **GET** /config/admin/language/{id} | Get language |
| [**configAdminLanguageIdLocalizationDefaultPut()**](I18nAdminApi.md#configAdminLanguageIdLocalizationDefaultPut) | **PUT** /config/admin/language/{id}/localization/default | Reset localizations |
| [**configAdminLanguageIdLocalizationGet()**](I18nAdminApi.md#configAdminLanguageIdLocalizationGet) | **GET** /config/admin/language/{id}/localization | Get localizations of language |
| [**configAdminLanguageIdPatch()**](I18nAdminApi.md#configAdminLanguageIdPatch) | **PATCH** /config/admin/language/{id} | Update language |
| [**configAdminLocalizationGet()**](I18nAdminApi.md#configAdminLocalizationGet) | **GET** /config/admin/localization | Get localizations for cursor |
| [**configAdminLocalizationGlossaryGet()**](I18nAdminApi.md#configAdminLocalizationGlossaryGet) | **GET** /config/admin/localization/glossary | Get glossary |
| [**configAdminLocalizationGlossaryIdDelete()**](I18nAdminApi.md#configAdminLocalizationGlossaryIdDelete) | **DELETE** /config/admin/localization/glossary/{id} | Delete glossary entry |
| [**configAdminLocalizationGlossaryIdGet()**](I18nAdminApi.md#configAdminLocalizationGlossaryIdGet) | **GET** /config/admin/localization/glossary/{id} | Get glossary entry |
| [**configAdminLocalizationGlossaryIdPut()**](I18nAdminApi.md#configAdminLocalizationGlossaryIdPut) | **PUT** /config/admin/localization/glossary/{id} | Update glossary entry |
| [**configAdminLocalizationGlossaryPost()**](I18nAdminApi.md#configAdminLocalizationGlossaryPost) | **POST** /config/admin/localization/glossary | Create glossary entry |
| [**configAdminLocalizationIdDefaultPut()**](I18nAdminApi.md#configAdminLocalizationIdDefaultPut) | **PUT** /config/admin/localization/{id}/default | Reset localization |
| [**configAdminLocalizationIdGet()**](I18nAdminApi.md#configAdminLocalizationIdGet) | **GET** /config/admin/localization/{id} | Get localization |
| [**configAdminLocalizationIdPatch()**](I18nAdminApi.md#configAdminLocalizationIdPatch) | **PATCH** /config/admin/localization/{id} | Update localization |
| [**configAdminLocalizationKeysGet()**](I18nAdminApi.md#configAdminLocalizationKeysGet) | **GET** /config/admin/localization/keys | Get localization keys |
| [**configAdminLocalizationSearchPost()**](I18nAdminApi.md#configAdminLocalizationSearchPost) | **POST** /config/admin/localization/search | Create cursor |


## `configAdminLanguageDefaultPut()`

```php
configAdminLanguageDefaultPut($session, $request): \OpenAPI\Client\Model\ModelSwagStatusOk
```

Update default language

This endpoint updates the default language in the system. The default language will be published automatically. If auto translation is disabled, the current default language will be set to Draft.  _only accessible with permission_ : `\"ManageConfiguration\"`  _fully accessible with permission_ : `\"ManageConfiguration\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\I18nAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\LanguagePutDefaultRequest(); // \OpenAPI\Client\Model\LanguagePutDefaultRequest | configuration for default language

try {
    $result = $apiInstance->configAdminLanguageDefaultPut($session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling I18nAdminApi->configAdminLanguageDefaultPut: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\LanguagePutDefaultRequest**](../Model/LanguagePutDefaultRequest.md)| configuration for default language | |

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

## `configAdminLanguageGet()`

```php
configAdminLanguageGet($session): \OpenAPI\Client\Model\LanguageResponseAdmin[]
```

Get languages

This endpoint returns all available languages in administrative representation.  _only accessible with permission_ : `\"ManageConfiguration\"`  _fully accessible with permission_ : `\"ManageConfiguration\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\I18nAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->configAdminLanguageGet($session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling I18nAdminApi->configAdminLanguageGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **session** | **string**| JWT | |

### Return type

[**\OpenAPI\Client\Model\LanguageResponseAdmin[]**](../Model/LanguageResponseAdmin.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `configAdminLanguageIdGet()`

```php
configAdminLanguageIdGet($id, $session): \OpenAPI\Client\Model\LanguageResponseAdmin
```

Get language

This endpoint returns a language in administrative representation by given id.  _only accessible with permission_ : `\"ManageConfiguration\"`  _fully accessible with permission_ : `\"ManageConfiguration\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\I18nAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Language code in format: IETF BCP 47
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->configAdminLanguageIdGet($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling I18nAdminApi->configAdminLanguageIdGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Language code in format: IETF BCP 47 | |
| **session** | **string**| JWT | |

### Return type

[**\OpenAPI\Client\Model\LanguageResponseAdmin**](../Model/LanguageResponseAdmin.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `configAdminLanguageIdLocalizationDefaultPut()`

```php
configAdminLanguageIdLocalizationDefaultPut($id, $session): \OpenAPI\Client\Model\LocalizationResponseAdmin[]
```

Reset localizations

This endpoint updates all localizations in the system for the provided language to the default value if the localization is customized and not deprecated.  _only accessible with permission_ : `\"ManageConfiguration\"`  _fully accessible with permission_ : `\"ManageConfiguration\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\I18nAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Language code in format: IETF BCP 47
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->configAdminLanguageIdLocalizationDefaultPut($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling I18nAdminApi->configAdminLanguageIdLocalizationDefaultPut: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Language code in format: IETF BCP 47 | |
| **session** | **string**| JWT | |

### Return type

[**\OpenAPI\Client\Model\LocalizationResponseAdmin[]**](../Model/LocalizationResponseAdmin.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `configAdminLanguageIdLocalizationGet()`

```php
configAdminLanguageIdLocalizationGet($id, $session): \OpenAPI\Client\Model\LocalizationResponseAdmin[]
```

Get localizations of language

This endpoint returns a localizations in administrative representation by given language.  _only accessible with permission_ : `\"ManageConfiguration\"`  _fully accessible with permission_ : `\"ManageConfiguration\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\I18nAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Language code in format: IETF BCP 47
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->configAdminLanguageIdLocalizationGet($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling I18nAdminApi->configAdminLanguageIdLocalizationGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Language code in format: IETF BCP 47 | |
| **session** | **string**| JWT | |

### Return type

[**\OpenAPI\Client\Model\LocalizationResponseAdmin[]**](../Model/LocalizationResponseAdmin.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `configAdminLanguageIdPatch()`

```php
configAdminLanguageIdPatch($id, $session, $request): \OpenAPI\Client\Model\LanguageResponseAdmin
```

Update language

This endpoint updates a language in the system by given id. The default language must be published. Status of languages could only be changed if auto translation is activated. To switch the default language, use the following endpoint: PUT /config/admin/language/default  _only accessible with permission_ : `\"ManageConfiguration\"`  _fully accessible with permission_ : `\"ManageConfiguration\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\I18nAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Language code in format: IETF BCP 47
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\LanguagePatchRequest(); // \OpenAPI\Client\Model\LanguagePatchRequest | language data to be updated

try {
    $result = $apiInstance->configAdminLanguageIdPatch($id, $session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling I18nAdminApi->configAdminLanguageIdPatch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Language code in format: IETF BCP 47 | |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\LanguagePatchRequest**](../Model/LanguagePatchRequest.md)| language data to be updated | [optional] |

### Return type

[**\OpenAPI\Client\Model\LanguageResponseAdmin**](../Model/LanguageResponseAdmin.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `configAdminLocalizationGet()`

```php
configAdminLocalizationGet($cursor, $page, $session, $limit): \OpenAPI\Client\Model\LocalizationResponseAdmin[]
```

Get localizations for cursor

This endpoint returns a list of all localizations for a cursor in administrative representation.  Cursor could be created here: POST /config/admin/localization/search  _accessible without permission_

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\I18nAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$cursor = 'cursor_example'; // string | id of the cursor used for pagination; required if page is set
$page = 56; // int | current page index of the cursor used for pagination; required if cursor is set
$session = 'session_example'; // string | JWT
$limit = 56; // int | amount of results per page (1 ... 100)

try {
    $result = $apiInstance->configAdminLocalizationGet($cursor, $page, $session, $limit);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling I18nAdminApi->configAdminLocalizationGet: ', $e->getMessage(), PHP_EOL;
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

[**\OpenAPI\Client\Model\LocalizationResponseAdmin[]**](../Model/LocalizationResponseAdmin.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `configAdminLocalizationGlossaryGet()`

```php
configAdminLocalizationGlossaryGet($session): \OpenAPI\Client\Model\TranslationGlossaryEntry[]
```

Get glossary

This endpoint returns all glossary entries.  _only accessible with permission_ : `\"ManageConfiguration\"`  _fully accessible with permission_ : `\"ManageConfiguration\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\I18nAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->configAdminLocalizationGlossaryGet($session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling I18nAdminApi->configAdminLocalizationGlossaryGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **session** | **string**| JWT | |

### Return type

[**\OpenAPI\Client\Model\TranslationGlossaryEntry[]**](../Model/TranslationGlossaryEntry.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `configAdminLocalizationGlossaryIdDelete()`

```php
configAdminLocalizationGlossaryIdDelete($id, $session): \OpenAPI\Client\Model\ModelSwagStatusOk
```

Delete glossary entry

This endpoint deletes a single glossary entry for provided id.  _only accessible with permission_ : `\"ManageConfiguration\"`  _fully accessible with permission_ : `\"ManageConfiguration\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\I18nAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Entry ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->configAdminLocalizationGlossaryIdDelete($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling I18nAdminApi->configAdminLocalizationGlossaryIdDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Entry ID | |
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

## `configAdminLocalizationGlossaryIdGet()`

```php
configAdminLocalizationGlossaryIdGet($id, $session): \OpenAPI\Client\Model\TranslationGlossaryEntry
```

Get glossary entry

This endpoint returns a single glossary entry for provided id.  _only accessible with permission_ : `\"ManageConfiguration\"`  _fully accessible with permission_ : `\"ManageConfiguration\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\I18nAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Entry ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->configAdminLocalizationGlossaryIdGet($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling I18nAdminApi->configAdminLocalizationGlossaryIdGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Entry ID | |
| **session** | **string**| JWT | |

### Return type

[**\OpenAPI\Client\Model\TranslationGlossaryEntry**](../Model/TranslationGlossaryEntry.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `configAdminLocalizationGlossaryIdPut()`

```php
configAdminLocalizationGlossaryIdPut($id, $session, $request): \OpenAPI\Client\Model\TranslationGlossaryEntry
```

Update glossary entry

This endpoint updates a single glossary entry.  _only accessible with permission_ : `\"ManageConfiguration\"`  _fully accessible with permission_ : `\"ManageConfiguration\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\I18nAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Entry ID
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\LocalizationGlossaryEntryRequest(); // \OpenAPI\Client\Model\LocalizationGlossaryEntryRequest | Entry to be updated

try {
    $result = $apiInstance->configAdminLocalizationGlossaryIdPut($id, $session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling I18nAdminApi->configAdminLocalizationGlossaryIdPut: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Entry ID | |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\LocalizationGlossaryEntryRequest**](../Model/LocalizationGlossaryEntryRequest.md)| Entry to be updated | |

### Return type

[**\OpenAPI\Client\Model\TranslationGlossaryEntry**](../Model/TranslationGlossaryEntry.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `configAdminLocalizationGlossaryPost()`

```php
configAdminLocalizationGlossaryPost($session, $request): \OpenAPI\Client\Model\TranslationGlossaryEntry
```

Create glossary entry

This endpoint creates a single glossary entry.  _only accessible with permission_ : `\"ManageConfiguration\"`  _fully accessible with permission_ : `\"ManageConfiguration\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\I18nAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\LocalizationGlossaryEntryRequest(); // \OpenAPI\Client\Model\LocalizationGlossaryEntryRequest | Entry to be created

try {
    $result = $apiInstance->configAdminLocalizationGlossaryPost($session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling I18nAdminApi->configAdminLocalizationGlossaryPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\LocalizationGlossaryEntryRequest**](../Model/LocalizationGlossaryEntryRequest.md)| Entry to be created | |

### Return type

[**\OpenAPI\Client\Model\TranslationGlossaryEntry**](../Model/TranslationGlossaryEntry.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `configAdminLocalizationIdDefaultPut()`

```php
configAdminLocalizationIdDefaultPut($id, $session): \OpenAPI\Client\Model\LocalizationResponseAdmin
```

Reset localization

This endpoint updates a localization in the system to the default value if the localization is customized and not deprecated. It will send status 409 if localization is deprecated.  _only accessible with permission_ : `\"ManageConfiguration\"`  _fully accessible with permission_ : `\"ManageConfiguration\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\I18nAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Localization ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->configAdminLocalizationIdDefaultPut($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling I18nAdminApi->configAdminLocalizationIdDefaultPut: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Localization ID | |
| **session** | **string**| JWT | |

### Return type

[**\OpenAPI\Client\Model\LocalizationResponseAdmin**](../Model/LocalizationResponseAdmin.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `configAdminLocalizationIdGet()`

```php
configAdminLocalizationIdGet($id, $session): \OpenAPI\Client\Model\LocalizationResponseAdmin
```

Get localization

This endpoint returns a localization in administrative representation by given id.  _only accessible with permission_ : `\"ManageConfiguration\"`  _fully accessible with permission_ : `\"ManageConfiguration\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\I18nAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Localization ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->configAdminLocalizationIdGet($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling I18nAdminApi->configAdminLocalizationIdGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Localization ID | |
| **session** | **string**| JWT | |

### Return type

[**\OpenAPI\Client\Model\LocalizationResponseAdmin**](../Model/LocalizationResponseAdmin.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `configAdminLocalizationIdPatch()`

```php
configAdminLocalizationIdPatch($id, $session, $request): \OpenAPI\Client\Model\LocalizationResponseAdmin
```

Update localization

This endpoint updates a localization in the system by given id.  _only accessible with permission_ : `\"ManageConfiguration\"`  _fully accessible with permission_ : `\"ManageConfiguration\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\I18nAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Localization ID
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\LocalizationPatchLocalizationRequest(); // \OpenAPI\Client\Model\LocalizationPatchLocalizationRequest | localization data to be updated

try {
    $result = $apiInstance->configAdminLocalizationIdPatch($id, $session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling I18nAdminApi->configAdminLocalizationIdPatch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Localization ID | |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\LocalizationPatchLocalizationRequest**](../Model/LocalizationPatchLocalizationRequest.md)| localization data to be updated | [optional] |

### Return type

[**\OpenAPI\Client\Model\LocalizationResponseAdmin**](../Model/LocalizationResponseAdmin.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `configAdminLocalizationKeysGet()`

```php
configAdminLocalizationKeysGet($session, $cursor, $page, $limit): string[]
```

Get localization keys

This endpoint returns a list of localization keys.  Cursor could be created here: POST /config/admin/localization/search  _accessible without permission_

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\I18nAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT
$cursor = 'cursor_example'; // string | id of the cursor used for pagination; required if page is set
$page = 56; // int | current page index of the cursor used for pagination; required if cursor is set
$limit = 56; // int | amount of results per page (1 ... 100)

try {
    $result = $apiInstance->configAdminLocalizationKeysGet($session, $cursor, $page, $limit);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling I18nAdminApi->configAdminLocalizationKeysGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **session** | **string**| JWT | |
| **cursor** | **string**| id of the cursor used for pagination; required if page is set | [optional] |
| **page** | **int**| current page index of the cursor used for pagination; required if cursor is set | [optional] |
| **limit** | **int**| amount of results per page (1 ... 100) | [optional] |

### Return type

**string[]**

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `configAdminLocalizationSearchPost()`

```php
configAdminLocalizationSearchPost($session, $request): \OpenAPI\Client\Model\ModelCursorResponse
```

Create cursor

This endpoint returns a cursor for list localizations in admin representation with applied filter and sort options. In case of cursor response total will be 0 the status 204 with not content is returned instead.  _only accessible with permission_ : `\"ManageConfiguration\"`  _fully accessible with permission_ : `\"ManageConfiguration\"`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\I18nAdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\LocalizationCursorRequestAdmin(); // \OpenAPI\Client\Model\LocalizationCursorRequestAdmin | options to create cursor

try {
    $result = $apiInstance->configAdminLocalizationSearchPost($session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling I18nAdminApi->configAdminLocalizationSearchPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\LocalizationCursorRequestAdmin**](../Model/LocalizationCursorRequestAdmin.md)| options to create cursor | |

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
