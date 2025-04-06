# Windows
(*windows*)

## Overview

### Available Operations

* [start](#start) - Start Vm
* [pause](#pause) - Pause Vm
* [resume](#resume) - Resume Vm
* [state](#state) - Get Vm Status
* [instances](#instances) - Get Instances
* [terminate](#terminate) - Terminate Vm

## start

Start a new Windows VM instance.

- timeout_minutes: Optional timeout in minutes (default: 60)

Requires API key authentication.

### Example Usage

```typescript
import { Skylight } from "skylight-sdk";

const skylight = new Skylight({
  apikey: process.env["SKYLIGHT_APIKEY"] ?? "",
});

async function run() {
  const result = await skylight.windows.start({});

  // Handle the result
  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { SkylightCore } from "skylight-sdk/core.js";
import { windowsStart } from "skylight-sdk/funcs/windowsStart.js";

// Use `SkylightCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const skylight = new SkylightCore({
  apikey: process.env["SKYLIGHT_APIKEY"] ?? "",
});

async function run() {
  const res = await windowsStart(skylight, {});

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
| `request`                                                                                                                                                                      | [components.InstanceRequest](../../models/components/instancerequest.md)                                                                                                       | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[components.InstanceStartResponse](../../models/components/instancestartresponse.md)\>**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| errors.ForbiddenErrorResponse | 403                           | application/json              |
| errors.HTTPValidationError    | 422                           | application/json              |
| errors.ServerErrorResponse    | 500                           | application/json              |
| errors.APIError               | 4XX, 5XX                      | \*/\*                         |

## pause

Requires API key authentication.

### Example Usage

```typescript
import { Skylight } from "skylight-sdk";

const skylight = new Skylight({
  apikey: process.env["SKYLIGHT_APIKEY"] ?? "",
});

async function run() {
  const result = await skylight.windows.pause({
    instanceId: "<id>",
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
import { windowsPause } from "skylight-sdk/funcs/windowsPause.js";

// Use `SkylightCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const skylight = new SkylightCore({
  apikey: process.env["SKYLIGHT_APIKEY"] ?? "",
});

async function run() {
  const res = await windowsPause(skylight, {
    instanceId: "<id>",
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
| `request`                                                                                                                                                                      | [operations.PauseRequest](../../models/operations/pauserequest.md)                                                                                                             | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[components.InstanceOperationResponse](../../models/components/instanceoperationresponse.md)\>**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| errors.ForbiddenErrorResponse | 403                           | application/json              |
| errors.HTTPValidationError    | 422                           | application/json              |
| errors.ServerErrorResponse    | 500                           | application/json              |
| errors.APIError               | 4XX, 5XX                      | \*/\*                         |

## resume

Requires API key authentication.

### Example Usage

```typescript
import { Skylight } from "skylight-sdk";

const skylight = new Skylight({
  apikey: process.env["SKYLIGHT_APIKEY"] ?? "",
});

async function run() {
  const result = await skylight.windows.resume({
    instanceId: "<id>",
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
import { windowsResume } from "skylight-sdk/funcs/windowsResume.js";

// Use `SkylightCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const skylight = new SkylightCore({
  apikey: process.env["SKYLIGHT_APIKEY"] ?? "",
});

async function run() {
  const res = await windowsResume(skylight, {
    instanceId: "<id>",
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
| `request`                                                                                                                                                                      | [operations.ResumeRequest](../../models/operations/resumerequest.md)                                                                                                           | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[components.InstanceOperationResponse](../../models/components/instanceoperationresponse.md)\>**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| errors.ForbiddenErrorResponse | 403                           | application/json              |
| errors.HTTPValidationError    | 422                           | application/json              |
| errors.ServerErrorResponse    | 500                           | application/json              |
| errors.APIError               | 4XX, 5XX                      | \*/\*                         |

## state

Requires API key authentication.

### Example Usage

```typescript
import { Skylight } from "skylight-sdk";

const skylight = new Skylight({
  apikey: process.env["SKYLIGHT_APIKEY"] ?? "",
});

async function run() {
  const result = await skylight.windows.state({
    instanceId: "<id>",
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
import { windowsState } from "skylight-sdk/funcs/windowsState.js";

// Use `SkylightCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const skylight = new SkylightCore({
  apikey: process.env["SKYLIGHT_APIKEY"] ?? "",
});

async function run() {
  const res = await windowsState(skylight, {
    instanceId: "<id>",
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
| `request`                                                                                                                                                                      | [operations.StateRequest](../../models/operations/staterequest.md)                                                                                                             | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[components.InstanceStatusResponse](../../models/components/instancestatusresponse.md)\>**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| errors.ForbiddenErrorResponse | 403                           | application/json              |
| errors.HTTPValidationError    | 422                           | application/json              |
| errors.ServerErrorResponse    | 500                           | application/json              |
| errors.APIError               | 4XX, 5XX                      | \*/\*                         |

## instances

Requires API key authentication.

### Example Usage

```typescript
import { Skylight } from "skylight-sdk";

const skylight = new Skylight({
  apikey: process.env["SKYLIGHT_APIKEY"] ?? "",
});

async function run() {
  const result = await skylight.windows.instances();

  // Handle the result
  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { SkylightCore } from "skylight-sdk/core.js";
import { windowsInstances } from "skylight-sdk/funcs/windowsInstances.js";

// Use `SkylightCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const skylight = new SkylightCore({
  apikey: process.env["SKYLIGHT_APIKEY"] ?? "",
});

async function run() {
  const res = await windowsInstances(skylight);

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
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[components.InstancesListResponse](../../models/components/instanceslistresponse.md)\>**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| errors.ForbiddenErrorResponse | 403                           | application/json              |
| errors.ServerErrorResponse    | 500                           | application/json              |
| errors.APIError               | 4XX, 5XX                      | \*/\*                         |

## terminate

Requires API key authentication.

### Example Usage

```typescript
import { Skylight } from "skylight-sdk";

const skylight = new Skylight({
  apikey: process.env["SKYLIGHT_APIKEY"] ?? "",
});

async function run() {
  const result = await skylight.windows.terminate({
    instanceId: "<id>",
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
import { windowsTerminate } from "skylight-sdk/funcs/windowsTerminate.js";

// Use `SkylightCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const skylight = new SkylightCore({
  apikey: process.env["SKYLIGHT_APIKEY"] ?? "",
});

async function run() {
  const res = await windowsTerminate(skylight, {
    instanceId: "<id>",
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
| `request`                                                                                                                                                                      | [operations.TerminateRequest](../../models/operations/terminaterequest.md)                                                                                                     | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[components.InstanceOperationResponse](../../models/components/instanceoperationresponse.md)\>**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| errors.ForbiddenErrorResponse | 403                           | application/json              |
| errors.HTTPValidationError    | 422                           | application/json              |
| errors.ServerErrorResponse    | 500                           | application/json              |
| errors.APIError               | 4XX, 5XX                      | \*/\*                         |