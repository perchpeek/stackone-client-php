# Accounts
(*accounts*)

## Overview

### Available Operations

* [listLinkedAccounts](#listlinkedaccounts) - List Accounts
* [getAccount](#getaccount) - Get Account
* [deleteAccount](#deleteaccount) - Delete Account
* [updateAccount](#updateaccount) - Update Account
* [getAccountMetaInfo](#getaccountmetainfo) - Get meta information of the account

## listLinkedAccounts

List Accounts

### Example Usage

```php
declare(strict_types=1);

require 'vendor/autoload.php';

use StackOne\client;
use StackOne\client\Models\Components;
use StackOne\client\Models\Operations;

$security = new Components\Security(
    username: '',
    password: '',
);

$sdk = client\StackOne::builder()->setSecurity($security)->build();

$request = new Operations\StackoneListLinkedAccountsRequest();

$response = $sdk->accounts->listLinkedAccounts(
    request: $request
);

if ($response->linkedAccounts !== null) {
    // handle response
}
```

### Parameters

| Parameter                                                                                                    | Type                                                                                                         | Required                                                                                                     | Description                                                                                                  |
| ------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------ |
| `$request`                                                                                                   | [Operations\StackoneListLinkedAccountsRequest](../../Models/Operations/StackoneListLinkedAccountsRequest.md) | :heavy_check_mark:                                                                                           | The request object to use for the request.                                                                   |

### Response

**[?Operations\StackoneListLinkedAccountsResponse](../../Models/Operations/StackoneListLinkedAccountsResponse.md)**

### Errors

| Error Type          | Status Code         | Content Type        |
| ------------------- | ------------------- | ------------------- |
| Errors\SDKException | 4XX, 5XX            | \*/\*               |

## getAccount

Get Account

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



$response = $sdk->accounts->getAccount(
    id: '<id>'
);

if ($response->linkedAccount !== null) {
    // handle response
}
```

### Parameters

| Parameter          | Type               | Required           | Description        |
| ------------------ | ------------------ | ------------------ | ------------------ |
| `id`               | *string*           | :heavy_check_mark: | N/A                |

### Response

**[?Operations\StackoneGetAccountResponse](../../Models/Operations/StackoneGetAccountResponse.md)**

### Errors

| Error Type          | Status Code         | Content Type        |
| ------------------- | ------------------- | ------------------- |
| Errors\SDKException | 4XX, 5XX            | \*/\*               |

## deleteAccount

Delete Account

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



$response = $sdk->accounts->deleteAccount(
    id: '<id>'
);

if ($response->linkedAccount !== null) {
    // handle response
}
```

### Parameters

| Parameter          | Type               | Required           | Description        |
| ------------------ | ------------------ | ------------------ | ------------------ |
| `id`               | *string*           | :heavy_check_mark: | N/A                |

### Response

**[?Operations\StackoneDeleteAccountResponse](../../Models/Operations/StackoneDeleteAccountResponse.md)**

### Errors

| Error Type          | Status Code         | Content Type        |
| ------------------- | ------------------- | ------------------- |
| Errors\SDKException | 4XX, 5XX            | \*/\*               |

## updateAccount

Update Account

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

$patchAccountExternalDto = new Components\PatchAccountExternalDto();

$response = $sdk->accounts->updateAccount(
    id: '<id>',
    patchAccountExternalDto: $patchAccountExternalDto

);

if ($response->linkedAccount !== null) {
    // handle response
}
```

### Parameters

| Parameter                                                                                | Type                                                                                     | Required                                                                                 | Description                                                                              |
| ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- |
| `id`                                                                                     | *string*                                                                                 | :heavy_check_mark:                                                                       | N/A                                                                                      |
| `patchAccountExternalDto`                                                                | [Components\PatchAccountExternalDto](../../Models/Components/PatchAccountExternalDto.md) | :heavy_check_mark:                                                                       | N/A                                                                                      |

### Response

**[?Operations\StackoneUpdateAccountResponse](../../Models/Operations/StackoneUpdateAccountResponse.md)**

### Errors

| Error Type          | Status Code         | Content Type        |
| ------------------- | ------------------- | ------------------- |
| Errors\SDKException | 4XX, 5XX            | \*/\*               |

## getAccountMetaInfo

Get meta information of the account

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



$response = $sdk->accounts->getAccountMetaInfo(
    id: '<id>'
);

if ($response->linkedAccountMeta !== null) {
    // handle response
}
```

### Parameters

| Parameter          | Type               | Required           | Description        |
| ------------------ | ------------------ | ------------------ | ------------------ |
| `id`               | *string*           | :heavy_check_mark: | N/A                |

### Response

**[?Operations\StackoneGetAccountMetaInfoResponse](../../Models/Operations/StackoneGetAccountMetaInfoResponse.md)**

### Errors

| Error Type          | Status Code         | Content Type        |
| ------------------- | ------------------- | ------------------- |
| Errors\SDKException | 4XX, 5XX            | \*/\*               |