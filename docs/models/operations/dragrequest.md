# DragRequest

## Example Usage

```typescript
import { DragRequest } from "skylight-sdk/models/operations";

let value: DragRequest = {
  instanceId: "<id>",
  dragRequest: {
    path: [
      {
        "x": 100,
        "y": 200,
      },
    ],
    step: 5,
  },
};
```

## Fields

| Field                                                               | Type                                                                | Required                                                            | Description                                                         | Example                                                             |
| ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- |
| `instanceId`                                                        | *string*                                                            | :heavy_check_mark:                                                  | N/A                                                                 |                                                                     |
| `dragRequest`                                                       | [components.DragRequest](../../models/components/dragrequest.md)    | :heavy_check_mark:                                                  | N/A                                                                 | {<br/>"button": "left",<br/>"path": [<br/>{<br/>"x": 100,<br/>"y": 200<br/>}<br/>],<br/>"step": 5<br/>} |