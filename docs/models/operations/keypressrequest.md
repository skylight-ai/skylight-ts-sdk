# KeypressRequest

## Example Usage

```typescript
import { KeypressRequest } from "skylight-sdk/models/operations";

let value: KeypressRequest = {
  instanceId: "<id>",
  keyRequest: {
    keys: [
      "super",
      "shift",
      "s",
    ],
  },
};
```

## Fields

| Field                                                          | Type                                                           | Required                                                       | Description                                                    | Example                                                        |
| -------------------------------------------------------------- | -------------------------------------------------------------- | -------------------------------------------------------------- | -------------------------------------------------------------- | -------------------------------------------------------------- |
| `instanceId`                                                   | *string*                                                       | :heavy_check_mark:                                             | N/A                                                            |                                                                |
| `keyRequest`                                                   | [components.KeyRequest](../../models/components/keyrequest.md) | :heavy_check_mark:                                             | N/A                                                            | {<br/>"keys": [<br/>"super",<br/>"shift",<br/>"s"<br/>]<br/>}  |