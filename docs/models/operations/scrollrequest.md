# ScrollRequest

## Example Usage

```typescript
import { ScrollRequest } from "skylight-sdk/models/operations";

let value: ScrollRequest = {
  instanceId: "<id>",
  scrollRequest: {
    x: 100,
    y: 200,
    step: 20,
  },
};
```

## Fields

| Field                                                                | Type                                                                 | Required                                                             | Description                                                          | Example                                                              |
| -------------------------------------------------------------------- | -------------------------------------------------------------------- | -------------------------------------------------------------------- | -------------------------------------------------------------------- | -------------------------------------------------------------------- |
| `instanceId`                                                         | *string*                                                             | :heavy_check_mark:                                                   | N/A                                                                  |                                                                      |
| `scrollRequest`                                                      | [components.ScrollRequest](../../models/components/scrollrequest.md) | :heavy_check_mark:                                                   | N/A                                                                  | {<br/>"scroll_x": 0,<br/>"scroll_y": 100,<br/>"step": 20,<br/>"x": 100,<br/>"y": 200<br/>} |