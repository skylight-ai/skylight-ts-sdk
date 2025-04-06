# ScrollRequest

## Example Usage

```typescript
import { ScrollRequest } from "skylight-sdk/models/components";

let value: ScrollRequest = {
  x: 100,
  y: 200,
  step: 20,
};
```

## Fields

| Field                                                                                  | Type                                                                                   | Required                                                                               | Description                                                                            |
| -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- |
| `x`                                                                                    | *number*                                                                               | :heavy_check_mark:                                                                     | N/A                                                                                    |
| `y`                                                                                    | *number*                                                                               | :heavy_check_mark:                                                                     | N/A                                                                                    |
| `scrollX`                                                                              | *number*                                                                               | :heavy_minus_sign:                                                                     | Horizontal scroll amount                                                               |
| `scrollY`                                                                              | *number*                                                                               | :heavy_minus_sign:                                                                     | Vertical scroll amount                                                                 |
| `step`                                                                                 | *number*                                                                               | :heavy_minus_sign:                                                                     | Optional step size for scroll movements. If not provided, movement will be continuous. |