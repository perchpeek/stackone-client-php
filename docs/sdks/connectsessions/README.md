# ConnectSessions
(*connectSessions*)

## Overview

### Available Operations

* [authenticateConnectSession](#authenticateconnectsession) - Authenticate Connect Session
* [createConnectSession](#createconnectsession) - Create Connect Session

## authenticateConnectSession

Authenticate Connect Session

### Example Usage

```php
declare(strict_types=1);

require 'vendor/autoload.php';

use StackOne\client;
use StackOne\client\Models\Components;

$sdk = client\StackOne::builder()
    ->setSecurity(
        new Components\Security(
            username: '',
            password: '',
        )
    )
    ->build();

$request = new Components\ConnectSessionAuthenticate(
    token: '<value>',
);

$response = $sdk->connectSessions->authenticateConnectSession(
    request: $request
);

if ($response->connectSession !== null) {
    // handle response
}
```

### Parameters

| Parameter                                                                                      | Type                                                                                           | Required                                                                                       | Description                                                                                    |
| ---------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- |
| `$request`                                                                                     | [Components\ConnectSessionAuthenticate](../../Models/Components/ConnectSessionAuthenticate.md) | :heavy_check_mark:                                                                             | The request object to use for the request.                                                     |

### Response

**[?Operations\StackoneAuthenticateConnectSessionResponse](../../Models/Operations/StackoneAuthenticateConnectSessionResponse.md)**

### Errors

| Error Type          | Status Code         | Content Type        |
| ------------------- | ------------------- | ------------------- |
| Errors\SDKException | 4XX, 5XX            | \*/\*               |

## createConnectSession

Create Connect Session

### Example Usage

```php
declare(strict_types=1);

require 'vendor/autoload.php';

use StackOne\client;
use StackOne\client\Models\Components;

$sdk = client\StackOne::builder()
    ->setSecurity(
        new Components\Security(
            username: '',
            password: '',
        )
    )
    ->build();

$request = new Components\ConnectSessionCreate(
    originOwnerId: '<id>',
    originOwnerName: '<value>',
    categories: [
        Components\Categories::Ats,
        Components\Categories::Hris,
        Components\Categories::Iam,
        Components\Categories::Crm,
        Components\Categories::Iam,
        Components\Categories::Marketing,
        Components\Categories::Lms,
        Components\Categories::Ats,
        Components\Categories::Documents,
        Components\Categories::Ticketing,
        Components\Categories::Screening,
    ],
);

$response = $sdk->connectSessions->createConnectSession(
    request: $request
);

if ($response->connectSessionTokenAuthLink !== null) {
    // handle response
}
```

### Parameters

| Parameter                                                                          | Type                                                                               | Required                                                                           | Description                                                                        |
| ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- |
| `$request`                                                                         | [Components\ConnectSessionCreate](../../Models/Components/ConnectSessionCreate.md) | :heavy_check_mark:                                                                 | The request object to use for the request.                                         |

### Response

**[?Operations\StackoneCreateConnectSessionResponse](../../Models/Operations/StackoneCreateConnectSessionResponse.md)**

### Errors

| Error Type          | Status Code         | Content Type        |
| ------------------- | ------------------- | ------------------- |
| Errors\SDKException | 4XX, 5XX            | \*/\*               |