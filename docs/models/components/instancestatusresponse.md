# InstanceStatusResponse

## Example Usage

```typescript
import { InstanceStatusResponse } from "skylight-sdk/models/components";

let value: InstanceStatusResponse = {
  instanceId: "i-123456",
  state: "running",
  knowledge: "The user previously asked to perform ....",
  livestreamUrl: "https://launchskylight.com/embed/i-123456",
  assignedAt: "2023-01-01T12:00:00Z",
};
```

## Fields

| Field                             | Type                              | Required                          | Description                       | Example                           |
| --------------------------------- | --------------------------------- | --------------------------------- | --------------------------------- | --------------------------------- |
| `instanceId`                      | *string*                          | :heavy_check_mark:                | N/A                               |                                   |
| `state`                           | *string*                          | :heavy_check_mark:                | Current state of the instance     | running                           |
| `knowledge`                       | *string*                          | :heavy_check_mark:                | Current knowledge of the instance | unknown                           |
| `livestreamUrl`                   | *string*                          | :heavy_check_mark:                | URL to livestream the instance    | launchskylight.com/embed/i-123456 |
| `assignedAt`                      | *string*                          | :heavy_minus_sign:                | When the instance was assigned    | 2023-01-01T12:00:00Z              |