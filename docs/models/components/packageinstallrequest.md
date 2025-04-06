# PackageInstallRequest

## Example Usage

```typescript
import { PackageInstallRequest } from "skylight-sdk/models/components";

let value: PackageInstallRequest = {
  packages: [
    "<value>",
  ],
};
```

## Fields

| Field                                       | Type                                        | Required                                    | Description                                 |
| ------------------------------------------- | ------------------------------------------- | ------------------------------------------- | ------------------------------------------- |
| `packages`                                  | *string*[]                                  | :heavy_check_mark:                          | List of Chocolatey package names to install |