# CreateEventResponse


## Fields

| Field                                            | Type                                             | Required                                         | Description                                      | Example                                          |
| ------------------------------------------------ | ------------------------------------------------ | ------------------------------------------------ | ------------------------------------------------ | ------------------------------------------------ |
| `event`                                          | *string*                                         | :heavy_check_mark:                               | The event name                                   | hris_employees.created                           |
| `recordId`                                       | *string*                                         | :heavy_check_mark:                               | The record id associated with the event          |                                                  |
| `status`                                         | *float*                                          | :heavy_check_mark:                               | The response http status code                    | 200                                              |
| `message`                                        | *?string*                                        | :heavy_minus_sign:                               | The message associated with the operation result | The event was created                            |