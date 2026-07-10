# ModelShippingAccountMetrics

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**created** | **int** | is sum of &#x60;createdWithCredentials&#x60; and &#x60;createdWithoutCredentials&#x60; | [optional]
**created_with_credentials** | **int** | is subset of &#x60;created&#x60; | [optional]
**created_without_credentials** | **int** | is subset of &#x60;created&#x60; | [optional]
**overwritten_passwords** | **int** | is subset of &#x60;updated&#x60; | [optional]
**sent_mails** | **int** | is subset of sum of &#x60;created&#x60; and &#x60;updated&#x60; | [optional]
**unshipped** | **int** | could be either not started yet or failed on shipping. more information can be found in &#x60;process&#x60; | [optional]
**update_skipped** | **int** | update was skipped because nothing changed | [optional]
**updated** | **int** |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
