# Role

The role of manager


## Fields

| Field                                                       | Type                                                        | Required                                                    | Description                                                 | Example                                                     |
| ----------------------------------------------------------- | ----------------------------------------------------------- | ----------------------------------------------------------- | ----------------------------------------------------------- | ----------------------------------------------------------- |
| `id`                                                        | *?string*                                                   | :heavy_minus_sign:                                          | Unique identifier                                           | 8187e5da-dc77-475e-9949-af0f1fa4e4e3                        |
| `remoteId`                                                  | *?string*                                                   | :heavy_minus_sign:                                          | Provider's unique identifier                                | 8187e5da-dc77-475e-9949-af0f1fa4e4e3                        |
| `label`                                                     | *?string*                                                   | :heavy_minus_sign:                                          | The label of the role type                                  | Admin                                                       |
| `roleType`                                                  | [?Components\RoleType](../../Models/Components/RoleType.md) | :heavy_minus_sign:                                          | The manager role type (e.g., admin, viewer)                 | admin                                                       |