# InstanceStartResponse

## Example Usage

```typescript
import { InstanceStartResponse } from "skylight-sdk/models/components";

let value: InstanceStartResponse = {
  instanceId: "<string>",
  message: "<string>",
  livestreamUrl: "<string>",
  state: "<string>",
};
```

## Fields

| Field                                                            | Type                                                             | Required                                                         | Description                                                      | Example                                                          |
| ---------------------------------------------------------------- | ---------------------------------------------------------------- | ---------------------------------------------------------------- | ---------------------------------------------------------------- | ---------------------------------------------------------------- |
| `instanceId`                                                     | *string*                                                         | :heavy_check_mark:                                               | Unique identifier of the created instance                        |                                                                  |
| `message`                                                        | *string*                                                         | :heavy_check_mark:                                               | Human-readable status message                                    | Instance ready to use                                            |
| `livestreamUrl`                                                  | *string*                                                         | :heavy_check_mark:                                               | URL to livestream the instance                                   | launchskylight.com/embed/i-123456                                |
| `state`                                                          | *string*                                                         | :heavy_check_mark:                                               | State of the instance (running, pending, hibernated, terminated) | running                                                          |