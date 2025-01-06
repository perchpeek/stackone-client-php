# Iam
(*iam*)

## Overview

### Available Operations

* [getGroup](#getgroup) - Get Group
* [getPolicy](#getpolicy) - Get Policy
* [getRole](#getrole) - Get Role
* [getUser](#getuser) - Get User
* [listGroups](#listgroups) - List Groups
* [listPolicies](#listpolicies) - List Policies
* [listRoles](#listroles) - List Roles
* [listUsers](#listusers) - List Users

## getGroup

Get Group

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

$request = new Operations\IamGetGroupRequest(
    xAccountId: '<id>',
    id: '<id>',
    fields: 'id,remote_id,parent_id,remote_parent_id,name,description,roles,type,created_at,updated_at',
    expand: 'roles',
);

$response = $sdk->iam->getGroup(
    request: $request
);

if ($response->iamGroupResult !== null) {
    // handle response
}
```

### Parameters

| Parameter                                                                      | Type                                                                           | Required                                                                       | Description                                                                    |
| ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ |
| `$request`                                                                     | [Operations\IamGetGroupRequest](../../Models/Operations/IamGetGroupRequest.md) | :heavy_check_mark:                                                             | The request object to use for the request.                                     |

### Response

**[?Operations\IamGetGroupResponse](../../Models/Operations/IamGetGroupResponse.md)**

### Errors

| Error Type          | Status Code         | Content Type        |
| ------------------- | ------------------- | ------------------- |
| Errors\SDKException | 4XX, 5XX            | \*/\*               |

## getPolicy

Get Policy

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

$request = new Operations\IamGetPolicyRequest(
    xAccountId: '<id>',
    id: '<id>',
    fields: 'id,remote_id,name,permissions,description,created_at,updated_at',
    expand: 'permissions',
);

$response = $sdk->iam->getPolicy(
    request: $request
);

if ($response->iamPolicyResult !== null) {
    // handle response
}
```

### Parameters

| Parameter                                                                        | Type                                                                             | Required                                                                         | Description                                                                      |
| -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- |
| `$request`                                                                       | [Operations\IamGetPolicyRequest](../../Models/Operations/IamGetPolicyRequest.md) | :heavy_check_mark:                                                               | The request object to use for the request.                                       |

### Response

**[?Operations\IamGetPolicyResponse](../../Models/Operations/IamGetPolicyResponse.md)**

### Errors

| Error Type          | Status Code         | Content Type        |
| ------------------- | ------------------- | ------------------- |
| Errors\SDKException | 4XX, 5XX            | \*/\*               |

## getRole

Get Role

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

$request = new Operations\IamGetRoleRequest(
    xAccountId: '<id>',
    id: '<id>',
    fields: 'id,remote_id,name,type,policies,description,created_at,updated_at',
    expand: 'policies',
);

$response = $sdk->iam->getRole(
    request: $request
);

if ($response->iamRoleResult !== null) {
    // handle response
}
```

### Parameters

| Parameter                                                                    | Type                                                                         | Required                                                                     | Description                                                                  |
| ---------------------------------------------------------------------------- | ---------------------------------------------------------------------------- | ---------------------------------------------------------------------------- | ---------------------------------------------------------------------------- |
| `$request`                                                                   | [Operations\IamGetRoleRequest](../../Models/Operations/IamGetRoleRequest.md) | :heavy_check_mark:                                                           | The request object to use for the request.                                   |

### Response

**[?Operations\IamGetRoleResponse](../../Models/Operations/IamGetRoleResponse.md)**

### Errors

| Error Type          | Status Code         | Content Type        |
| ------------------- | ------------------- | ------------------- |
| Errors\SDKException | 4XX, 5XX            | \*/\*               |

## getUser

Get User

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

$request = new Operations\IamGetUserRequest(
    xAccountId: '<id>',
    id: '<id>',
    fields: 'id,remote_id,first_name,last_name,name,primary_email_address,username,roles,groups,status,avatar,is_bot_user,last_active_at,last_login_at,created_at,updated_at,multi_factor_enabled',
    expand: 'roles,groups',
);

$response = $sdk->iam->getUser(
    request: $request
);

if ($response->iamUserResult !== null) {
    // handle response
}
```

### Parameters

| Parameter                                                                    | Type                                                                         | Required                                                                     | Description                                                                  |
| ---------------------------------------------------------------------------- | ---------------------------------------------------------------------------- | ---------------------------------------------------------------------------- | ---------------------------------------------------------------------------- |
| `$request`                                                                   | [Operations\IamGetUserRequest](../../Models/Operations/IamGetUserRequest.md) | :heavy_check_mark:                                                           | The request object to use for the request.                                   |

### Response

**[?Operations\IamGetUserResponse](../../Models/Operations/IamGetUserResponse.md)**

### Errors

| Error Type          | Status Code         | Content Type        |
| ------------------- | ------------------- | ------------------- |
| Errors\SDKException | 4XX, 5XX            | \*/\*               |

## listGroups

List Groups

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

$request = new Operations\IamListGroupsRequest(
    xAccountId: '<id>',
    fields: 'id,remote_id,parent_id,remote_parent_id,name,description,roles,type,created_at,updated_at',
    filter: new Operations\IamListGroupsQueryParamFilter(
        updatedAfter: '2020-01-01T00:00:00.000Z',
    ),
    expand: 'roles',
);

$response = $sdk->iam->listGroups(
    request: $request
);

if ($response->iamGroupsPaginated !== null) {
    // handle response
}
```

### Parameters

| Parameter                                                                          | Type                                                                               | Required                                                                           | Description                                                                        |
| ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- |
| `$request`                                                                         | [Operations\IamListGroupsRequest](../../Models/Operations/IamListGroupsRequest.md) | :heavy_check_mark:                                                                 | The request object to use for the request.                                         |

### Response

**[?Operations\IamListGroupsResponse](../../Models/Operations/IamListGroupsResponse.md)**

### Errors

| Error Type          | Status Code         | Content Type        |
| ------------------- | ------------------- | ------------------- |
| Errors\SDKException | 4XX, 5XX            | \*/\*               |

## listPolicies

List Policies

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

$request = new Operations\IamListPoliciesRequest(
    xAccountId: '<id>',
    fields: 'id,remote_id,name,permissions,description,created_at,updated_at',
    filter: new Operations\IamListPoliciesQueryParamFilter(
        updatedAfter: '2020-01-01T00:00:00.000Z',
    ),
    expand: 'permissions',
);

$response = $sdk->iam->listPolicies(
    request: $request
);

if ($response->iamPoliciesPaginated !== null) {
    // handle response
}
```

### Parameters

| Parameter                                                                              | Type                                                                                   | Required                                                                               | Description                                                                            |
| -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- |
| `$request`                                                                             | [Operations\IamListPoliciesRequest](../../Models/Operations/IamListPoliciesRequest.md) | :heavy_check_mark:                                                                     | The request object to use for the request.                                             |

### Response

**[?Operations\IamListPoliciesResponse](../../Models/Operations/IamListPoliciesResponse.md)**

### Errors

| Error Type          | Status Code         | Content Type        |
| ------------------- | ------------------- | ------------------- |
| Errors\SDKException | 4XX, 5XX            | \*/\*               |

## listRoles

List Roles

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

$request = new Operations\IamListRolesRequest(
    xAccountId: '<id>',
    fields: 'id,remote_id,name,type,policies,description,created_at,updated_at',
    filter: new Operations\IamListRolesQueryParamFilter(
        updatedAfter: '2020-01-01T00:00:00.000Z',
    ),
    expand: 'policies',
);

$response = $sdk->iam->listRoles(
    request: $request
);

if ($response->iamRolesPaginated !== null) {
    // handle response
}
```

### Parameters

| Parameter                                                                        | Type                                                                             | Required                                                                         | Description                                                                      |
| -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- |
| `$request`                                                                       | [Operations\IamListRolesRequest](../../Models/Operations/IamListRolesRequest.md) | :heavy_check_mark:                                                               | The request object to use for the request.                                       |

### Response

**[?Operations\IamListRolesResponse](../../Models/Operations/IamListRolesResponse.md)**

### Errors

| Error Type          | Status Code         | Content Type        |
| ------------------- | ------------------- | ------------------- |
| Errors\SDKException | 4XX, 5XX            | \*/\*               |

## listUsers

List Users

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

$request = new Operations\IamListUsersRequest(
    xAccountId: '<id>',
    fields: 'id,remote_id,first_name,last_name,name,primary_email_address,username,roles,groups,status,avatar,is_bot_user,last_active_at,last_login_at,created_at,updated_at,multi_factor_enabled',
    filter: new Operations\IamListUsersQueryParamFilter(
        updatedAfter: '2020-01-01T00:00:00.000Z',
    ),
    expand: 'roles,groups',
);

$response = $sdk->iam->listUsers(
    request: $request
);

if ($response->iamUsersPaginated !== null) {
    // handle response
}
```

### Parameters

| Parameter                                                                        | Type                                                                             | Required                                                                         | Description                                                                      |
| -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- |
| `$request`                                                                       | [Operations\IamListUsersRequest](../../Models/Operations/IamListUsersRequest.md) | :heavy_check_mark:                                                               | The request object to use for the request.                                       |

### Response

**[?Operations\IamListUsersResponse](../../Models/Operations/IamListUsersResponse.md)**

### Errors

| Error Type          | Status Code         | Content Type        |
| ------------------- | ------------------- | ------------------- |
| Errors\SDKException | 4XX, 5XX            | \*/\*               |