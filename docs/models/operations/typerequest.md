# TypeRequest

## Example Usage

```typescript
import { TypeRequest } from "skylight-sdk/models/operations";

let value: TypeRequest = {
  instanceId: "<id>",
  typeRequest: {
    text: "Hello, world!",
    interval: 0.05,
  },
};
```

## Fields

| Field                                                            | Type                                                             | Required                                                         | Description                                                      | Example                                                          |
| ---------------------------------------------------------------- | ---------------------------------------------------------------- | ---------------------------------------------------------------- | ---------------------------------------------------------------- | ---------------------------------------------------------------- |
| `instanceId`                                                     | *string*                                                         | :heavy_check_mark:                                               | N/A                                                              |                                                                  |
| `typeRequest`                                                    | [components.TypeRequest](../../models/components/typerequest.md) | :heavy_check_mark:                                               | N/A                                                              | {<br/>"interval": 0.05,<br/>"text": "Hello, world!"<br/>}        |