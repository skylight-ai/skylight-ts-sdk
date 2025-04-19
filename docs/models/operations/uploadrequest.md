# UploadRequest

## Example Usage

```typescript
import { UploadRequest } from "skylight-sdk/models/operations";

let value: UploadRequest = {
  instanceId: "<id>",
  s3VMUploadRequest: {
    s3Url: "https://gripping-complication.info",
    fileName: "example.file",
  },
};
```

## Fields

| Field                                                                        | Type                                                                         | Required                                                                     | Description                                                                  |
| ---------------------------------------------------------------------------- | ---------------------------------------------------------------------------- | ---------------------------------------------------------------------------- | ---------------------------------------------------------------------------- |
| `instanceId`                                                                 | *string*                                                                     | :heavy_check_mark:                                                           | N/A                                                                          |
| `s3VMUploadRequest`                                                          | [components.S3VMUploadRequest](../../models/components/s3vmuploadrequest.md) | :heavy_check_mark:                                                           | N/A                                                                          |