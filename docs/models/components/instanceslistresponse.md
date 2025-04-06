# InstancesListResponse

## Example Usage

```typescript
import { InstancesListResponse } from "skylight-sdk/models/components";

let value: InstancesListResponse = {
  instances: [
    {},
    {},
  ],
};
```

## Fields

| Field                                                          | Type                                                           | Required                                                       | Description                                                    |
| -------------------------------------------------------------- | -------------------------------------------------------------- | -------------------------------------------------------------- | -------------------------------------------------------------- |
| `instances`                                                    | [components.Instances](../../models/components/instances.md)[] | :heavy_check_mark:                                             | List of instance IDs and states associated with the API key    |