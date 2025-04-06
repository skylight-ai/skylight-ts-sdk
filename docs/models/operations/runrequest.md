# RunRequest

## Example Usage

```typescript
import { RunRequest } from "skylight-sdk/models/operations";

let value: RunRequest = {
  instanceId: "<id>",
  claudeRequest: {
    query: "Search for something on the VM",
  },
};
```

## Fields

| Field                                                                | Type                                                                 | Required                                                             | Description                                                          | Example                                                              |
| -------------------------------------------------------------------- | -------------------------------------------------------------------- | -------------------------------------------------------------------- | -------------------------------------------------------------------- | -------------------------------------------------------------------- |
| `instanceId`                                                         | *string*                                                             | :heavy_check_mark:                                                   | N/A                                                                  |                                                                      |
| `claudeRequest`                                                      | [components.ClaudeRequest](../../models/components/clauderequest.md) | :heavy_check_mark:                                                   | N/A                                                                  | {<br/>"query": "Search for something on the VM"<br/>}                |