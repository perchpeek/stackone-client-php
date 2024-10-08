# CrmCreateContactRequestDto


## Fields

| Field                                 | Type                                  | Required                              | Description                           | Example                               |
| ------------------------------------- | ------------------------------------- | ------------------------------------- | ------------------------------------- | ------------------------------------- |
| `firstName`                           | *?string*                             | :heavy_minus_sign:                    | The contact first name                | Steve                                 |
| `lastName`                            | *?string*                             | :heavy_minus_sign:                    | The contact last name                 | Wozniak                               |
| `companyName`                         | *?string*                             | :heavy_minus_sign:                    | The contact company name              | Apple Inc.                            |
| `emails`                              | array<*string*>                       | :heavy_minus_sign:                    | List of contact email addresses       | [<br/>"steve@apple.com"<br/>]         |
| `phoneNumbers`                        | array<*string*>                       | :heavy_minus_sign:                    | List of contact phone numbers         | [<br/>"123-456-7890"<br/>]            |
| `dealIds`                             | array<*string*>                       | :heavy_minus_sign:                    | List of associated deal IDs           | [<br/>"deal-001",<br/>"deal-002"<br/>] |
| `accountIds`                          | array<*string*>                       | :heavy_minus_sign:                    | List of associated account IDs        | [<br/>"account-123",<br/>"account-456"<br/>] |
| `passthrough`                         | array<string, *mixed*>                | :heavy_minus_sign:                    | Value to pass through to the provider | {<br/>"other_known_names": "John Doe"<br/>} |