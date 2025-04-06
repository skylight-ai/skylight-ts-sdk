# Agent
(*agent*)

## Overview

### Available Operations

* [run](#run) - Run Agent
* [stop](#stop) - Stop Agent Endpoint
* [status](#status) - Get Agent Status Endpoint

## run

Run a loop with Anthropic's computer use agent to perform tasks on the VM.

Requires API key authentication.

### Example Usage

```typescript
import { Skylight } from "skylight-sdk";

const skylight = new Skylight({
  apikey: process.env["SKYLIGHT_APIKEY"] ?? "",
});

async function run() {
  const result = await skylight.agent.run({
    instanceId: "<id>",
    claudeRequest: {
      query: "Search for something on the VM",
    },
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
import { agentRun } from "skylight-sdk/funcs/agentRun.js";

// Use `SkylightCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const skylight = new SkylightCore({
  apikey: process.env["SKYLIGHT_APIKEY"] ?? "",
});

async function run() {
  const res = await agentRun(skylight, {
    instanceId: "<id>",
    claudeRequest: {
      query: "Search for something on the VM",
    },
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
| `request`                                                                                                                                                                      | [operations.RunRequest](../../models/operations/runrequest.md)                                                                                                                 | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[components.StandardResponse](../../models/components/standardresponse.md)\>**

### Errors

| Error Type                 | Status Code                | Content Type               |
| -------------------------- | -------------------------- | -------------------------- |
| errors.HTTPValidationError | 422                        | application/json           |
| errors.ErrorResponse       | 500                        | application/json           |
| errors.APIError            | 4XX, 5XX                   | \*/\*                      |

## stop

Stop a running agent for a specific instance.

Requires API key authentication.

### Example Usage

```typescript
import { Skylight } from "skylight-sdk";

const skylight = new Skylight({
  apikey: process.env["SKYLIGHT_APIKEY"] ?? "",
});

async function run() {
  const result = await skylight.agent.stop({
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
import { agentStop } from "skylight-sdk/funcs/agentStop.js";

// Use `SkylightCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const skylight = new SkylightCore({
  apikey: process.env["SKYLIGHT_APIKEY"] ?? "",
});

async function run() {
  const res = await agentStop(skylight, {
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
| `request`                                                                                                                                                                      | [operations.StopRequest](../../models/operations/stoprequest.md)                                                                                                               | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[components.StandardResponse](../../models/components/standardresponse.md)\>**

### Errors

| Error Type                 | Status Code                | Content Type               |
| -------------------------- | -------------------------- | -------------------------- |
| errors.ErrorResponse       | 404                        | application/json           |
| errors.HTTPValidationError | 422                        | application/json           |
| errors.ErrorResponse       | 500                        | application/json           |
| errors.APIError            | 4XX, 5XX                   | \*/\*                      |

## status

Get the current status of an agent for a specific instance.

Requires API key authentication.

### Example Usage

```typescript
import { Skylight } from "skylight-sdk";

const skylight = new Skylight({
  apikey: process.env["SKYLIGHT_APIKEY"] ?? "",
});

async function run() {
  const result = await skylight.agent.status({
    agentId: "<id>",
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
import { agentStatus } from "skylight-sdk/funcs/agentStatus.js";

// Use `SkylightCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const skylight = new SkylightCore({
  apikey: process.env["SKYLIGHT_APIKEY"] ?? "",
});

async function run() {
  const res = await agentStatus(skylight, {
    agentId: "<id>",
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
| `request`                                                                                                                                                                      | [operations.StatusRequest](../../models/operations/statusrequest.md)                                                                                                           | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[components.StandardResponse](../../models/components/standardresponse.md)\>**

### Errors

| Error Type                 | Status Code                | Content Type               |
| -------------------------- | -------------------------- | -------------------------- |
| errors.ErrorResponse       | 404                        | application/json           |
| errors.HTTPValidationError | 422                        | application/json           |
| errors.ErrorResponse       | 500                        | application/json           |
| errors.APIError            | 4XX, 5XX                   | \*/\*                      |