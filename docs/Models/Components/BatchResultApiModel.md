# BatchResultApiModel


## Fields

| Field                                                         | Type                                                          | Required                                                      | Description                                                   | Example                                                       |
| ------------------------------------------------------------- | ------------------------------------------------------------- | ------------------------------------------------------------- | ------------------------------------------------------------- | ------------------------------------------------------------- |
| `statusCode`                                                  | *?float*                                                      | :heavy_minus_sign:                                            | N/A                                                           | 202                                                           |
| `message`                                                     | *?string*                                                     | :heavy_minus_sign:                                            | N/A                                                           | Batch operation accepted                                      |
| `timestamp`                                                   | [\DateTime](https://www.php.net/manual/en/class.datetime.php) | :heavy_minus_sign:                                            | N/A                                                           | 2021-01-01T01:01:01.000Z                                      |
| `errors`                                                      | array<array<*string*>>                                        | :heavy_minus_sign:                                            | N/A                                                           | [<br/>[<br/>"Missing field: name"<br/>],<br/>[],<br/>[]<br/>] |