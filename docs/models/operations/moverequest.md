# MoveRequest

## Example Usage

```typescript
import { MoveRequest } from "skylight-sdk/models/operations";

let value: MoveRequest = {
  instanceId: "<id>",
  mouseMoveRequest: {
    x: 100,
    y: 200,
  },
};
```

## Fields

| Field                                                                      | Type                                                                       | Required                                                                   | Description                                                                | Example                                                                    |
| -------------------------------------------------------------------------- | -------------------------------------------------------------------------- | -------------------------------------------------------------------------- | -------------------------------------------------------------------------- | -------------------------------------------------------------------------- |
| `instanceId`                                                               | *string*                                                                   | :heavy_check_mark:                                                         | N/A                                                                        |                                                                            |
| `mouseMoveRequest`                                                         | [components.MouseMoveRequest](../../models/components/mousemoverequest.md) | :heavy_check_mark:                                                         | N/A                                                                        | {<br/>"x": 100,<br/>"y": 200<br/>}                                         |