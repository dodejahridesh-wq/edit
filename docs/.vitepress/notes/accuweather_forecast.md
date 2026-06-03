---
name: accuweather-forecast
description: >
  AccuWeather location key resolution, current conditions, and meteorological forecast API.
---

# AccuWeather Meteorological Interface

## Overview
Query current weather status, hourly telemetry, and multi-day forecasts using the AccuWeather REST API.

## REST API Integration
AccuWeather requires a location key, which must be resolved first.
- **Resolve Location Key**: `GET http://dataservice.accuweather.com/locations/v1/cities/search?apikey={API_KEY}&q={city_name}`
- **Get Current Conditions**: `GET http://dataservice.accuweather.com/currentconditions/v1/{location_key}?apikey={API_KEY}`
- **Get 5-Day Forecast**: `GET http://dataservice.accuweather.com/forecasts/v1/daily/5day/{location_key}?apikey={API_KEY}`
