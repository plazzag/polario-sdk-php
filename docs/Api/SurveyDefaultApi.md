# OpenAPI\Client\SurveyDefaultApi



All URIs are relative to https://custom.polario.de/api, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**reactionDefaultSurveyIdGet()**](SurveyDefaultApi.md#reactionDefaultSurveyIdGet) | **GET** /reaction/default/survey/{id} | Get survey |
| [**reactionDefaultSurveyIdParticipationGet()**](SurveyDefaultApi.md#reactionDefaultSurveyIdParticipationGet) | **GET** /reaction/default/survey/{id}/participation | Get own survey participations |
| [**reactionDefaultSurveyIdParticipationPost()**](SurveyDefaultApi.md#reactionDefaultSurveyIdParticipationPost) | **POST** /reaction/default/survey/{id}/participation | Submit survey participation |


## `reactionDefaultSurveyIdGet()`

```php
reactionDefaultSurveyIdGet($id, $session, $accept_language): \OpenAPI\Client\Model\SurveyResponseDefault
```

Get survey

This endpoint returns a published survey in default representation by given id. Only published surveys accessible to the user are returned.  __Note:__ Surveys is a premium feature and requires a valid subscription.  _accessible without permission_

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\SurveyDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Survey ID
$session = 'session_example'; // string | JWT
$accept_language = 'accept_language_example'; // string | client language(s)

try {
    $result = $apiInstance->reactionDefaultSurveyIdGet($id, $session, $accept_language);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SurveyDefaultApi->reactionDefaultSurveyIdGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Survey ID | |
| **session** | **string**| JWT | |
| **accept_language** | **string**| client language(s) | [optional] |

### Return type

[**\OpenAPI\Client\Model\SurveyResponseDefault**](../Model/SurveyResponseDefault.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `reactionDefaultSurveyIdParticipationGet()`

```php
reactionDefaultSurveyIdParticipationGet($id, $session): \OpenAPI\Client\Model\SurveyparticipationResponseDefault[]
```

Get own survey participations

This endpoint returns the calling user's own participation records for the given survey. For property `participationMode` is `\"Single\"` this returns at most one result; for `\"Multiple\"` it may return several.  __Note:__ Surveys is a premium feature and requires a valid subscription.  _accessible without permission_

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\SurveyDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Survey ID
$session = 'session_example'; // string | JWT

try {
    $result = $apiInstance->reactionDefaultSurveyIdParticipationGet($id, $session);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SurveyDefaultApi->reactionDefaultSurveyIdParticipationGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Survey ID | |
| **session** | **string**| JWT | |

### Return type

[**\OpenAPI\Client\Model\SurveyparticipationResponseDefault[]**](../Model/SurveyparticipationResponseDefault.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `reactionDefaultSurveyIdParticipationPost()`

```php
reactionDefaultSurveyIdParticipationPost($id, $session, $request): \OpenAPI\Client\Model\SurveyparticipationResponseDefault
```

Submit survey participation

This endpoint submits answers for a published survey the user has access to. For surveys with property `participationMode` is `\"Single\"`, only one submission per user is allowed. Contingent limits on items and options are enforced on a best-effort basis.  ___answers.property___ is item id  __Note:__ Surveys is a premium feature and requires a valid subscription.  _accessible without permission_

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\SurveyDefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | Survey ID
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\SurveyparticipationPostRequest(); // \OpenAPI\Client\Model\SurveyparticipationPostRequest | Participation answers

try {
    $result = $apiInstance->reactionDefaultSurveyIdParticipationPost($id, $session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SurveyDefaultApi->reactionDefaultSurveyIdParticipationPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Survey ID | |
| **session** | **string**| JWT | |
| **request** | [**\OpenAPI\Client\Model\SurveyparticipationPostRequest**](../Model/SurveyparticipationPostRequest.md)| Participation answers | |

### Return type

[**\OpenAPI\Client\Model\SurveyparticipationResponseDefault**](../Model/SurveyparticipationResponseDefault.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
