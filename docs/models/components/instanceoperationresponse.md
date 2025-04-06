# InstanceOperationResponse

## Example Usage

```typescript
import { InstanceOperationResponse } from "skylight-sdk/models/components";

let value: InstanceOperationResponse = {
  status: "<string>",
  message: "<string>",
  awsState: "<string>",
};
```

## Fields

| Field                            | Type                             | Required                         | Description                      | Example                          |
| -------------------------------- | -------------------------------- | -------------------------------- | -------------------------------- | -------------------------------- |
| `status`                         | *string*                         | :heavy_check_mark:               | Status of the operation          | success                          |
| `message`                        | *string*                         | :heavy_check_mark:               | Human-readable status message    | Operation completed successfully |
| `awsState`                       | *string*                         | :heavy_check_mark:               | AWS state of the instance        | running                          |