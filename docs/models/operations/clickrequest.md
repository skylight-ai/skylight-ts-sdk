# ClickRequest

## Example Usage

```typescript
import { ClickRequest } from "skylight-sdk/models/operations";

let value: ClickRequest = {
  instanceId: "<id>",
  clickRequest: {
    x: 100,
    y: 200,
  },
};
```

## Fields

| Field                                                              | Type                                                               | Required                                                           | Description                                                        | Example                                                            |
| ------------------------------------------------------------------ | ------------------------------------------------------------------ | ------------------------------------------------------------------ | ------------------------------------------------------------------ | ------------------------------------------------------------------ |
| `instanceId`                                                       | *string*                                                           | :heavy_check_mark:                                                 | N/A                                                                |                                                                    |
| `clickRequest`                                                     | [components.ClickRequest](../../models/components/clickrequest.md) | :heavy_check_mark:                                                 | N/A                                                                | {<br/>"button": "left",<br/>"clicks": 1,<br/>"x": 100,<br/>"y": 200<br/>} |