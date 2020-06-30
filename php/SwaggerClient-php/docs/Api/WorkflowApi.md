# Swagger\Client\WorkflowApi

All URIs are relative to *https://virtserver.swaggerhub.com/mithredate/TMS/1.0.0*

Method | HTTP request | Description
------------- | ------------- | -------------
[**defineWorkflow**](WorkflowApi.md#defineworkflow) | **POST** /workflows | Define a new workflow
[**workflowsWorkflowIdGet**](WorkflowApi.md#workflowsworkflowidget) | **GET** /workflows/{workflowId} | Get a workflow definition

# **defineWorkflow**
> \Swagger\Client\Model\WorkflowResponse defineWorkflow($body)

Define a new workflow

This is the main API for defining workflows, which can then be used in order processing. Accessing this API requires you to be authenticated. Read more about authentication on our documents.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\WorkflowApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$body = new \Swagger\Client\Model\WorkflowRequest(); // \Swagger\Client\Model\WorkflowRequest | Workflow definition object that needs to be stored

try {
    $result = $apiInstance->defineWorkflow($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WorkflowApi->defineWorkflow: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Swagger\Client\Model\WorkflowRequest**](../Model/WorkflowRequest.md)| Workflow definition object that needs to be stored |

### Return type

[**\Swagger\Client\Model\WorkflowResponse**](../Model/WorkflowResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **workflowsWorkflowIdGet**
> \Swagger\Client\Model\WorkflowResponse workflowsWorkflowIdGet($workflow_id)

Get a workflow definition

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\WorkflowApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$workflow_id = 56; // int | Id of the workflow

try {
    $result = $apiInstance->workflowsWorkflowIdGet($workflow_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WorkflowApi->workflowsWorkflowIdGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workflow_id** | **int**| Id of the workflow |

### Return type

[**\Swagger\Client\Model\WorkflowResponse**](../Model/WorkflowResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

