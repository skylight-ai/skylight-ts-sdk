# InactiveOperationResponse

## Example Usage

```typescript
import { InactiveOperationResponse } from "skylight-sdk/models/components";

let value: InactiveOperationResponse = {
  status: "<string>",
  message: "<string>",
  state: "<string>",
};
```

## Fields

| Field                                                            | Type                                                             | Required                                                         | Description                                                      | Example                                                          |
| ---------------------------------------------------------------- | ---------------------------------------------------------------- | ---------------------------------------------------------------- | ---------------------------------------------------------------- | ---------------------------------------------------------------- |
| `status`                                                         | *string*                                                         | :heavy_check_mark:                                               | Status of the operation                                          | success                                                          |
| `message`                                                        | *string*                                                         | :heavy_check_mark:                                               | Human-readable status message                                    | Operation completed successfully                                 |
| `state`                                                          | *string*                                                         | :heavy_check_mark:                                               | State of the instance (running, pending, hibernated, terminated) | running                                                          |