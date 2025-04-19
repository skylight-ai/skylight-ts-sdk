# FileUploadResponse

Response when a file is successfully uploaded to a VM

## Example Usage

```typescript
import { FileUploadResponse } from "skylight-sdk/models/components";

let value: FileUploadResponse = {
  status: "success",
  message: "File uploaded successfully",
  filePath: "C:\Users\Public\Downloads\file.pdf",
};
```

## Fields

| Field                                   | Type                                    | Required                                | Description                             | Example                                 |
| --------------------------------------- | --------------------------------------- | --------------------------------------- | --------------------------------------- | --------------------------------------- |
| `status`                                | *string*                                | :heavy_check_mark:                      | Status of the operation                 | success                                 |
| `message`                               | *string*                                | :heavy_check_mark:                      | Human-readable status message           | File uploaded successfully              |
| `filePath`                              | *string*                                | :heavy_check_mark:                      | Path where the file was saved on the VM | C:\Users\Public\Downloads\file.pdf      |