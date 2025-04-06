<!-- Start SDK Example Usage [usage] -->
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
<!-- End SDK Example Usage [usage] -->