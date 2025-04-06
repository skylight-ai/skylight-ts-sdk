# InstanceStartResponse

## Example Usage

```typescript
import { InstanceStartResponse } from "skylight-sdk/models/components";

let value: InstanceStartResponse = {
  status: "<string>",
  instanceId: "<string>",
  message: "<string>",
  livestreamUrl: "<string>",
  awsState: "<string>",
};
```

## Fields

| Field                                     | Type                                      | Required                                  | Description                               | Example                                   |
| ----------------------------------------- | ----------------------------------------- | ----------------------------------------- | ----------------------------------------- | ----------------------------------------- |
| `status`                                  | *string*                                  | :heavy_check_mark:                        | Status of the instance start operation    | success                                   |
| `instanceId`                              | *string*                                  | :heavy_check_mark:                        | Unique identifier of the created instance |                                           |
| `message`                                 | *string*                                  | :heavy_check_mark:                        | Human-readable status message             | Instance ready to use                     |
| `livestreamUrl`                           | *string*                                  | :heavy_check_mark:                        | URL to livestream the instance            | launchskylight.com/embed/i-123456         |
| `awsState`                                | *string*                                  | :heavy_check_mark:                        | AWS state of the instance                 | running                                   |