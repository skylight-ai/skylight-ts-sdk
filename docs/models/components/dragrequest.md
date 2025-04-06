# DragRequest

## Example Usage

```typescript
import { DragRequest } from "skylight-sdk/models/components";

let value: DragRequest = {
  path: [
    {
      "x": 100,
      "y": 200,
    },
    {
      "x": 200,
      "y": 300,
    },
    {
      "x": 300,
      "y": 400,
    },
  ],
  step: 5,
};
```

## Fields

| Field                                                                                | Type                                                                                 | Required                                                                             | Description                                                                          |
| ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ |
| `path`                                                                               | Record<string, *number*>[]                                                           | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `button`                                                                             | [components.DragRequestButton](../../models/components/dragrequestbutton.md)         | :heavy_minus_sign:                                                                   | N/A                                                                                  |
| `step`                                                                               | *number*                                                                             | :heavy_minus_sign:                                                                   | Optional step size for drag movements. If not provided, movement will be continuous. |