<!-- Start SDK Example Usage [usage] -->
```typescript
import { SpeakeasyWeatherSdk1 } from "speakeasy-weather-package";

const speakeasyWeatherSdk1 = new SpeakeasyWeatherSdk1();

async function run() {
  const result = await speakeasyWeatherSdk1.weathers.get({
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