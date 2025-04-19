# FileDownloadResponse

Response containing a presigned URL to download a file

## Example Usage

```typescript
import { FileDownloadResponse } from "skylight-sdk/models/components";

let value: FileDownloadResponse = {
  status: "success",
  message: "File download URL generated successfully",
  downloadUrl: "https://s3.amazonaws.com/bucket/file?token=...",
};
```

## Fields

| Field                                          | Type                                           | Required                                       | Description                                    | Example                                        |
| ---------------------------------------------- | ---------------------------------------------- | ---------------------------------------------- | ---------------------------------------------- | ---------------------------------------------- |
| `status`                                       | *string*                                       | :heavy_check_mark:                             | Status of the operation                        | success                                        |
| `message`                                      | *string*                                       | :heavy_check_mark:                             | Human-readable status message                  | File download URL generated successfully       |
| `downloadUrl`                                  | *string*                                       | :heavy_check_mark:                             | Presigned URL to download the file             | https://s3.amazonaws.com/bucket/file?token=... |