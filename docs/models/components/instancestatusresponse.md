# InstanceStatusResponse

## Example Usage

```typescript
import { InstanceStatusResponse } from "skylight-sdk/models/components";

let value: InstanceStatusResponse = {
  state: "<string>",
  knowledge: "<string>",
};
```

## Fields

| Field                             | Type                              | Required                          | Description                       | Example                           |
| --------------------------------- | --------------------------------- | --------------------------------- | --------------------------------- | --------------------------------- |
| `state`                           | *string*                          | :heavy_check_mark:                | Current state of the instance     | running                           |
| `knowledge`                       | *string*                          | :heavy_check_mark:                | Current knowledge of the instance | unknown                           |