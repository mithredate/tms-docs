# SwaggerClient-php
This is [Podro TMS's](https://podro.com/products/tms) documentation.

This PHP package is automatically generated by the [Swagger Codegen](https://github.com/swagger-api/swagger-codegen) project:

- API version: 1.0.0
- Build package: io.swagger.codegen.v3.generators.php.PhpClientCodegen

## Requirements

PHP 5.5 and later

## Installation & Usage
### Composer

To install the bindings via [Composer](http://getcomposer.org/), add the following to `composer.json`:

```
{
  "repositories": [
    {
      "type": "git",
      "url": "https://github.com/GIT_USER_ID/GIT_REPO_ID.git"
    }
  ],
  "require": {
    "GIT_USER_ID/GIT_REPO_ID": "*@dev"
  }
}
```

Then run `composer install`

### Manual Installation

Download the files and include `autoload.php`:

```php
    require_once('/path/to/SwaggerClient-php/vendor/autoload.php');
```

## Tests

To run the unit tests:

```
composer install
./vendor/bin/phpunit
```

## Getting Started

Please follow the [installation procedure](#installation--usage) and then run the following:

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

## Documentation for API Endpoints

All URIs are relative to *https://virtserver.swaggerhub.com/mithredate/TMS/1.0.0*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*WorkflowApi* | [**defineWorkflow**](docs/Api/WorkflowApi.md#defineworkflow) | **POST** /workflows | Define a new workflow
*WorkflowApi* | [**workflowsWorkflowIdGet**](docs/Api/WorkflowApi.md#workflowsworkflowidget) | **GET** /workflows/{workflowId} | Get a workflow definition

## Documentation For Models

 - [EndNodeRequest](docs/Model/EndNodeRequest.md)
 - [EndNodeRequestData](docs/Model/EndNodeRequestData.md)
 - [ExclusiveChoiceNodeRequest](docs/Model/ExclusiveChoiceNodeRequest.md)
 - [ExclusiveChoiceNodeRequestData](docs/Model/ExclusiveChoiceNodeRequestData.md)
 - [ExclusiveChoiceNodeRequestDataBranches](docs/Model/ExclusiveChoiceNodeRequestDataBranches.md)
 - [InputNodeRequest](docs/Model/InputNodeRequest.md)
 - [InputNodeRequestData](docs/Model/InputNodeRequestData.md)
 - [OneOfWorkflowRequestNodesItems](docs/Model/OneOfWorkflowRequestNodesItems.md)
 - [StartNodeRequest](docs/Model/StartNodeRequest.md)
 - [StartNodeRequestData](docs/Model/StartNodeRequestData.md)
 - [VariableNodeRequest](docs/Model/VariableNodeRequest.md)
 - [WorkflowRequest](docs/Model/WorkflowRequest.md)
 - [WorkflowResponse](docs/Model/WorkflowResponse.md)
 - [WorkflowResponseAttributes](docs/Model/WorkflowResponseAttributes.md)

## Documentation For Authorization

 All endpoints do not require authorization.


## Author


