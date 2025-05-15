# Weathers
(*weathers*)

## Overview

### Available Operations

* [get](#get) - Retrieve current weather, hourly forecast, and daily forecast based on latitude and longitude.

## get

Retrieve current weather, hourly forecast, and daily forecast based on latitude and longitude.

### Example Usage

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

### Standalone function

The standalone function version of this method:

```typescript
import { SpeakeasyWeatherSdk1Core } from "speakeasy-weather-package/core.js";
import { weathersGet } from "speakeasy-weather-package/funcs/weathersGet.js";

// Use `SpeakeasyWeatherSdk1Core` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const speakeasyWeatherSdk1 = new SpeakeasyWeatherSdk1Core();

async function run() {
  const res = await weathersGet(speakeasyWeatherSdk1, {
    lat: 8525.89,
    lon: 3247.8,
    appid: "<id>",
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
| `request`                                                                                                                                                                      | [operations.GetWeatherDataRequest](../../models/operations/getweatherdatarequest.md)                                                                                           | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[components.WeatherResponse](../../models/components/weatherresponse.md)\>**

### Errors

| Error Type      | Status Code     | Content Type    |
| --------------- | --------------- | --------------- |
| errors.APIError | 4XX, 5XX        | \*/\*           |