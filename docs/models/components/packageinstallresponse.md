# PackageInstallResponse

## Example Usage

```typescript
import { PackageInstallResponse } from "skylight-sdk/models/components";

let value: PackageInstallResponse = {
  status: "<string>",
  message: "Operation completed successfully",
  awsState: "running",
};
```

## Fields

| Field                                         | Type                                          | Required                                      | Description                                   | Example                                       |
| --------------------------------------------- | --------------------------------------------- | --------------------------------------------- | --------------------------------------------- | --------------------------------------------- |
| `status`                                      | *string*                                      | :heavy_check_mark:                            | Status of the operation                       | success                                       |
| `message`                                     | *string*                                      | :heavy_check_mark:                            | Human-readable status message                 | Operation completed successfully              |
| `awsState`                                    | *string*                                      | :heavy_check_mark:                            | AWS state of the instance                     | running                                       |
| `commandId`                                   | *string*                                      | :heavy_minus_sign:                            | Command ID for tracking installation progress |                                               |