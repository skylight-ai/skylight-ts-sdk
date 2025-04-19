# Files
(*files*)

## Overview

### Available Operations

* [upload](#upload) - Upload To Vm
* [download](#download) - Get File

## upload

Upload a file from S3 to the VM

Takes an S3 URL (often from FileUploader component) and transfers it to the VM.
Updates the files.uploads array in the vm_instances table to track the file.

Requires API key authentication.

### Example Usage

```typescript
import { Skylight } from "skylight-sdk";

const skylight = new Skylight({
  apikey: process.env["SKYLIGHT_APIKEY"] ?? "",
});

async function run() {
  const result = await skylight.files.upload("<id>", {
    s3Url: "https://needy-mallard.info/",
    fileName: "example.file",
  });

  // Handle the result
  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { SkylightCore } from "skylight-sdk/core.js";
import { filesUpload } from "skylight-sdk/funcs/filesUpload.js";

// Use `SkylightCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const skylight = new SkylightCore({
  apikey: process.env["SKYLIGHT_APIKEY"] ?? "",
});

async function run() {
  const res = await filesUpload(skylight, "<id>", {
    s3Url: "https://needy-mallard.info/",
    fileName: "example.file",
  });

  if (!res.ok) {
    throw res.error;
  }

  const { value: result } = res;

  // Handle the result
  console.log(result);
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `instanceId`                                                                                                                                                                   | *string*                                                                                                                                                                       | :heavy_check_mark:                                                                                                                                                             | N/A                                                                                                                                                                            |
| `s3VMUploadRequest`                                                                                                                                                            | [components.S3VMUploadRequest](../../models/components/s3vmuploadrequest.md)                                                                                                   | :heavy_check_mark:                                                                                                                                                             | N/A                                                                                                                                                                            |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[components.FileUploadResponse](../../models/components/fileuploadresponse.md)\>**

### Errors

| Error Type                         | Status Code                        | Content Type                       |
| ---------------------------------- | ---------------------------------- | ---------------------------------- |
| errors.InteractModelsErrorResponse | 400                                | application/json                   |
| errors.ForbiddenErrorResponse      | 403                                | application/json                   |
| errors.HTTPValidationError         | 422                                | application/json                   |
| errors.InteractModelsErrorResponse | 500                                | application/json                   |
| errors.APIError                    | 4XX, 5XX                           | \*/\*                              |

## download

Get a secure download link for a file on the instance

Generates a presigned S3 URL for the client to download the file directly

Requires API key authentication.

### Example Usage

```typescript
import { Skylight } from "skylight-sdk";

const skylight = new Skylight({
  apikey: process.env["SKYLIGHT_APIKEY"] ?? "",
});

async function run() {
  const result = await skylight.files.download("<id>", {
    "key": "<value>",
  });

  // Handle the result
  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { SkylightCore } from "skylight-sdk/core.js";
import { filesDownload } from "skylight-sdk/funcs/filesDownload.js";

// Use `SkylightCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const skylight = new SkylightCore({
  apikey: process.env["SKYLIGHT_APIKEY"] ?? "",
});

async function run() {
  const res = await filesDownload(skylight, "<id>", {
    "key": "<value>",
  });

  if (!res.ok) {
    throw res.error;
  }

  const { value: result } = res;

  // Handle the result
  console.log(result);
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `instanceId`                                                                                                                                                                   | *string*                                                                                                                                                                       | :heavy_check_mark:                                                                                                                                                             | N/A                                                                                                                                                                            |
| `requestBody`                                                                                                                                                                  | Record<string, *string*>                                                                                                                                                       | :heavy_check_mark:                                                                                                                                                             | N/A                                                                                                                                                                            |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[components.FileDownloadResponse](../../models/components/filedownloadresponse.md)\>**

### Errors

| Error Type                         | Status Code                        | Content Type                       |
| ---------------------------------- | ---------------------------------- | ---------------------------------- |
| errors.ForbiddenErrorResponse      | 403                                | application/json                   |
| errors.HTTPValidationError         | 422                                | application/json                   |
| errors.InteractModelsErrorResponse | 500                                | application/json                   |
| errors.APIError                    | 4XX, 5XX                           | \*/\*                              |