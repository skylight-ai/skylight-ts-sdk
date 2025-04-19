# S3VMUploadRequest

## Example Usage

```typescript
import { S3VMUploadRequest } from "skylight-sdk/models/components";

let value: S3VMUploadRequest = {
  s3Url: "https://vast-hamburger.info",
  fileName: "example.file",
};
```

## Fields

| Field                                                                       | Type                                                                        | Required                                                                    | Description                                                                 |
| --------------------------------------------------------------------------- | --------------------------------------------------------------------------- | --------------------------------------------------------------------------- | --------------------------------------------------------------------------- |
| `s3Url`                                                                     | *string*                                                                    | :heavy_check_mark:                                                          | The S3 URL of the file to upload                                            |
| `fileName`                                                                  | *string*                                                                    | :heavy_check_mark:                                                          | Original name of the file                                                   |
| `fileType`                                                                  | *string*                                                                    | :heavy_minus_sign:                                                          | MIME type of the file                                                       |
| `targetPath`                                                                | *string*                                                                    | :heavy_minus_sign:                                                          | Target path on the VM (defaults to Users/Administrator/Desktop/{file_name}) |