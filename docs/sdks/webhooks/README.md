# Webhooks
(*webhooks*)

## Overview

### Available Operations

* [create](#create)

## create

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



$response = $sdk->webhooks->create(
    xAccountId: '<id>',
    id: 4865.89,
    requestBody: [
        new Components\CreateEvent(
            event: 'hris_employees.created',
            recordId: '<id>',
        ),
    ]

);

if ($response->createEventResponses !== null) {
    // handle response
}
```

### Parameters

| Parameter                                                               | Type                                                                    | Required                                                                | Description                                                             |
| ----------------------------------------------------------------------- | ----------------------------------------------------------------------- | ----------------------------------------------------------------------- | ----------------------------------------------------------------------- |
| `xAccountId`                                                            | *string*                                                                | :heavy_check_mark:                                                      | The account identifier                                                  |
| `id`                                                                    | *float*                                                                 | :heavy_check_mark:                                                      | N/A                                                                     |
| `requestBody`                                                           | array<[Components\CreateEvent](../../Models/Components/CreateEvent.md)> | :heavy_check_mark:                                                      | N/A                                                                     |

### Response

**[?Operations\CreateResponse](../../Models/Operations/CreateResponse.md)**

### Errors

| Error Type          | Status Code         | Content Type        |
| ------------------- | ------------------- | ------------------- |
| Errors\SDKException | 4XX, 5XX            | \*/\*               |