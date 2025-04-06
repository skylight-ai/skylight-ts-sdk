# InstancesListResponse

## Example Usage

```typescript
import { InstancesListResponse } from "skylight-sdk/models/components";

let value: InstancesListResponse = {
  instances: [
    {
      instanceId: "i-123456",
      state: "running",
      knowledge: "unknown",
      livestreamUrl: "launchskylight.com/embed/i-123456",
      assignedAt: "2023-01-01T12:00:00Z",
    },
    {
      instanceId: "i-789012",
      state: "stopped",
      knowledge: "unknown",
      livestreamUrl: "launchskylight.com/embed/i-789012",
      assignedAt: "2023-01-02T12:00:00Z",
    },
  ],
};
```

## Fields

| Field                                                                                    | Type                                                                                     | Required                                                                                 | Description                                                                              |
| ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- |
| `instances`                                                                              | [components.InstanceStatusResponse](../../models/components/instancestatusresponse.md)[] | :heavy_check_mark:                                                                       | List of instances associated with the API key                                            |