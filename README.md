# Climate Cache: New York City - Weather

![weather workflow](https://github.com/climate-cache/nyc-weather/actions/workflows/nyc_24h_openmeteo.yml/badge.svg)

A daily archive of weather in New York City, powered by the free Open-Meteo API.

#### Data starts at: 2023-10-08

#### Looking for historical 14-day forecast data? Check out [Climate Cache: NYC Forecasts](https://github.com/climate-cache/nyc-forecasts)

### Data Source

Every day at 05:00 US Eastern GitHub actions calls the Open-Meteo API to get the previous day's weather, and saves it to
a JSON file in this repository.

### Variables Recorded

| Variable                    | Description                              | Units                      |
|-----------------------------|------------------------------------------|----------------------------|
| `time`                      | Date of the weather record               | ISO8601 (2023-10-08T00:00) |
| `temperature_2m`            | Temperature at 2m/6ft above ground       | °F                         |
| `relative_humidity_2m`      | Relative humidity at 2m/6ft above ground | %                          |
| `dewpoint_2m`               | Dewpoint at 2m/6ft above ground          | °F                         |
| `apparent_temperature`      | Apparent temperature                     | °F                         |
| `precipitation_probability` | Probability of precipitation             | %                          |
| `rain`                      | Rainfall                                 | inches                     |
| `showers`                   | Showers                                  | inches                     |
| `snowfall`                  | Snowfall                                 | inches                     |
| `surface_pressure`          | Surface pressure                         | hPa                        |
| `cloudcover`                | Cloud cover                              | %                          |
| `windspeed_10m`             | Wind speed at 10m above ground           | mp/h                       |
| `winddirection_10m`         | Wind direction at 10m above ground       | °                          |
| `windgusts_10m`             | Wind gusts at 10m above ground           | mp/h                       |

### Sample JSON File:
#### Values cut for brevity, this shows hours 1 and 24, the real file has all 24
    
```json
{
    "latitude": 40.710335,
    "longitude": -73.99307,
    "generationtime_ms": 0.10597705841064453,
    "utc_offset_seconds": -14400,
    "timezone": "America/New_York",
    "timezone_abbreviation": "EDT",
    "elevation": 7.0,
    "hourly_units": {
        "time": "iso8601",
        "temperature_2m": "°F",
        "relativehumidity_2m": "%",
        "dewpoint_2m": "°F",
        "apparent_temperature": "°F",
        "precipitation_probability": "%",
        "rain": "inch",
        "showers": "inch",
        "snowfall": "inch",
        "surface_pressure": "hPa",
        "cloudcover": "%",
        "windspeed_10m": "mp/h",
        "winddirection_10m": "°",
        "windgusts_10m": "mp/h"
    },
    "hourly": {
        "time": [
            "2023-10-08T00:00",
            ...
            "2023-10-08T23:00"
        ],
        "temperature_2m": [
            52.1,
            ...
            53.2
        ],
        "relativehumidity_2m": [
            78,
            ...
            50
        ],
        "dewpoint_2m": [
            45.4,
            ...
            35.1
        ],
        "apparent_temperature": [
            46.8,
            ...
            45.4
        ],
        "precipitation_probability": [
            0,
            ...
            0
        ],
        "rain": [
            0.0,
            ...
            0.0
        ],
        "showers": [
            0.0,
            ...
            0.0
        ],
        "snowfall": [
            0.0,
            ...
            0.0
        ],
        "surface_pressure": [
            1002.8,
            ...
            1006.0
        ],
        "cloudcover": [
            0,
            ...
            99
        ],
        "windspeed_10m": [
            9.6,
            ...
            10.8
        ],
        "winddirection_10m": [
            259,
            ...
            249
        ],
        "windgusts_10m": [
            26.8,
            ...
            20.8
        ]
    }
}
```