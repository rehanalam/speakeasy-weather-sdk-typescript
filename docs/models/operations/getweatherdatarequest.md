# GetWeatherDataRequest

## Example Usage

```typescript
import { GetWeatherDataRequest } from "speakeasy-weather/models/operations";

let value: GetWeatherDataRequest = {
  lat: 4301.29,
  lon: 7938,
  appid: "<id>",
};
```

## Fields

| Field                       | Type                        | Required                    | Description                 |
| --------------------------- | --------------------------- | --------------------------- | --------------------------- |
| `lat`                       | *number*                    | :heavy_check_mark:          | Latitude of the location.   |
| `lon`                       | *number*                    | :heavy_check_mark:          | Longitude of the location.  |
| `appid`                     | *string*                    | :heavy_check_mark:          | API key for authentication. |