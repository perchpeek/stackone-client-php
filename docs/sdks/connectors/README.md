# Connectors
(*connectors*)

## Overview

### Available Operations

* [listConnectorsMeta](#listconnectorsmeta) - List Connectors Meta Information for all providers
* [getConnectorMeta](#getconnectormeta) - Get Connector Meta information for the given provider key

## listConnectorsMeta

List Connectors Meta Information for all providers

### Example Usage

```php
declare(strict_types=1);

require 'vendor/autoload.php';

use StackOne\client;
use StackOne\client\Models\Components;

$security = new Components\Security(
    username: '',
    password: '',
);

$sdk = client\StackOne::builder()->setSecurity($security)->build();



$response = $sdk->connectors->listConnectorsMeta(
    include: 'field_path,unmapped_fields,resources,inactive,webhooks,static_fields'
);

if ($response->connectorsMetas !== null) {
    // handle response
}
```

### Parameters

| Parameter                                                              | Type                                                                   | Required                                                               | Description                                                            | Example                                                                |
| ---------------------------------------------------------------------- | ---------------------------------------------------------------------- | ---------------------------------------------------------------------- | ---------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| `include`                                                              | *?string*                                                              | :heavy_minus_sign:                                                     | The comma separated list of data that will be included in the response | field_path,unmapped_fields,resources,inactive,webhooks,static_fields   |

### Response

**[?Operations\StackoneListConnectorsMetaResponse](../../Models/Operations/StackoneListConnectorsMetaResponse.md)**

### Errors

| Error Type          | Status Code         | Content Type        |
| ------------------- | ------------------- | ------------------- |
| Errors\SDKException | 4XX, 5XX            | \*/\*               |

## getConnectorMeta

Get Connector Meta information for the given provider key

### Example Usage

```php
declare(strict_types=1);

require 'vendor/autoload.php';

use StackOne\client;
use StackOne\client\Models\Components;

$security = new Components\Security(
    username: '',
    password: '',
);

$sdk = client\StackOne::builder()->setSecurity($security)->build();



$response = $sdk->connectors->getConnectorMeta(
    provider: '<value>',
    include: 'field_path,unmapped_fields,resources,inactive,webhooks,static_fields'

);

if ($response->connectorsMeta !== null) {
    // handle response
}
```

### Parameters

| Parameter                                                              | Type                                                                   | Required                                                               | Description                                                            | Example                                                                |
| ---------------------------------------------------------------------- | ---------------------------------------------------------------------- | ---------------------------------------------------------------------- | ---------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| `provider`                                                             | *string*                                                               | :heavy_check_mark:                                                     | N/A                                                                    |                                                                        |
| `include`                                                              | *?string*                                                              | :heavy_minus_sign:                                                     | The comma separated list of data that will be included in the response | field_path,unmapped_fields,resources,inactive,webhooks,static_fields   |

### Response

**[?Operations\StackoneGetConnectorMetaResponse](../../Models/Operations/StackoneGetConnectorMetaResponse.md)**

### Errors

| Error Type          | Status Code         | Content Type        |
| ------------------- | ------------------- | ------------------- |
| Errors\SDKException | 4XX, 5XX            | \*/\*               |