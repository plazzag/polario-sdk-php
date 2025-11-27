# OpenAPI\Client\UtilApi



All URIs are relative to https://custom.polario.de/api, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**configCspPost()**](UtilApi.md#configCspPost) | **POST** /config/csp | Check csp of url |


## `configCspPost()`

```php
configCspPost($session, $request): \OpenAPI\Client\Model\ConfigurationCSPResponse
```

Check csp of url

This endpoint is for checking Content-Security-Policy of an url to get information about showing inside an iframe is possible or should be better opened in new tab. See: https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Security-Policy for more information.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\UtilApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session = 'session_example'; // string | JWT
$request = new \OpenAPI\Client\Model\ConfigurationCSPRequest(); // \OpenAPI\Client\Model\ConfigurationCSPRequest | url to be checked

try {
    $result = $apiInstance->configCspPost($session, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UtilApi->configCspPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **session** | **string**| JWT | [optional] |
| **request** | [**\OpenAPI\Client\Model\ConfigurationCSPRequest**](../Model/ConfigurationCSPRequest.md)| url to be checked | [optional] |

### Return type

[**\OpenAPI\Client\Model\ConfigurationCSPResponse**](../Model/ConfigurationCSPResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
