# AgentStatusResponse

## Example Usage

```typescript
import { AgentStatusResponse } from "skylight-sdk/models/components";

let value: AgentStatusResponse = {
  agentStatus: "running",
  isRunning: true,
  totalSteps: 5,
  stepCount: 5,
  finalSummary: "Successfully completed all tasks",
  files: [
    {},
  ],
  steps: [
    "Step 1: Search for information",
    "Step 2: Download file",
  ],
  createdAt: "2023-01-01T12:00:00Z",
  query: "Find and download information about Windows",
  agentId: "agent-123456",
};
```

## Fields

| Field                                                  | Type                                                   | Required                                               | Description                                            | Example                                                |
| ------------------------------------------------------ | ------------------------------------------------------ | ------------------------------------------------------ | ------------------------------------------------------ | ------------------------------------------------------ |
| `agentStatus`                                          | *string*                                               | :heavy_check_mark:                                     | Current status of the agent                            | running                                                |
| `isRunning`                                            | *boolean*                                              | :heavy_check_mark:                                     | Whether the agent is currently running                 | true                                                   |
| `totalSteps`                                           | *number*                                               | :heavy_check_mark:                                     | Total number of steps executed                         | 5                                                      |
| `stepCount`                                            | *number*                                               | :heavy_check_mark:                                     | Number of steps in memory                              | 5                                                      |
| `finalSummary`                                         | *string*                                               | :heavy_minus_sign:                                     | Final summary of agent execution                       |                                                        |
| `files`                                                | [components.Files](../../models/components/files.md)[] | :heavy_check_mark:                                     | List of files downloaded by the agent                  |                                                        |
| `steps`                                                | *string*[]                                             | :heavy_check_mark:                                     | List of steps executed by the agent                    |                                                        |
| `createdAt`                                            | *string*                                               | :heavy_check_mark:                                     | Timestamp when the agent was created                   |                                                        |
| `query`                                                | *string*                                               | :heavy_check_mark:                                     | Original query given to the agent                      |                                                        |
| `agentId`                                              | *string*                                               | :heavy_check_mark:                                     | Unique identifier for the agent                        |                                                        |