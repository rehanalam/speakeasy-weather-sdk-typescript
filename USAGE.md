<!-- Start SDK Example Usage [usage] -->
```typescript
import { SpeakeasyWeatherSDK } from "speakeasy-weather";

const speakeasyWeatherSDK = new SpeakeasyWeatherSDK();

async function run() {
  const result = await speakeasyWeatherSDK.weathers.get({
    lat: 8525.89,
    lon: 3247.8,
    appid: "<id>",
  });

  // Handle the result
  console.log(result);
}

run();

```
<!-- End SDK Example Usage [usage] -->