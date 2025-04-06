# InstallRequest

## Example Usage

```typescript
import { InstallRequest } from "skylight-sdk/models/operations";

let value: InstallRequest = {
  instanceId: "<id>",
  packageInstallRequest: {
    packages: [
      "<value>",
    ],
  },
};
```

## Fields

| Field                                                                                | Type                                                                                 | Required                                                                             | Description                                                                          |
| ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ |
| `instanceId`                                                                         | *string*                                                                             | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `packageInstallRequest`                                                              | [components.PackageInstallRequest](../../models/components/packageinstallrequest.md) | :heavy_check_mark:                                                                   | N/A                                                                                  |