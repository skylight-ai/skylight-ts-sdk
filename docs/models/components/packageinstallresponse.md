# PackageInstallResponse

## Example Usage

```typescript
import { PackageInstallResponse } from "skylight-sdk/models/components";

let value: PackageInstallResponse = {
  status: "<string>",
  message: "Operation completed successfully",
  state: "running",
  livestreamUrl: "launchskylight.com/embed/i-123456",
};
```

## Fields

| Field                                                            | Type                                                             | Required                                                         | Description                                                      | Example                                                          |
| ---------------------------------------------------------------- | ---------------------------------------------------------------- | ---------------------------------------------------------------- | ---------------------------------------------------------------- | ---------------------------------------------------------------- |
| `status`                                                         | *string*                                                         | :heavy_check_mark:                                               | Status of the operation                                          | success                                                          |
| `message`                                                        | *string*                                                         | :heavy_check_mark:                                               | Human-readable status message                                    | Operation completed successfully                                 |
| `state`                                                          | *string*                                                         | :heavy_check_mark:                                               | State of the instance (running, pending, hibernated, terminated) | running                                                          |
| `livestreamUrl`                                                  | *string*                                                         | :heavy_check_mark:                                               | URL to livestream the instance                                   | launchskylight.com/embed/i-123456                                |
| `commandId`                                                      | *string*                                                         | :heavy_minus_sign:                                               | Command ID for tracking installation progress                    |                                                                  |