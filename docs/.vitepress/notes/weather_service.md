---
name: weather-service
description: >
  Retrieve meteorological forecasts and historical weather datasets.
---

# Weather Forecast API

## Overview
Query real-time weather forecasts, historical data, and atmospheric telemetry using endpoints from services like OpenWeatherMap.

## REST API Integration
OpenWeatherMap exposes specific endpoints.
- **Current Weather**: `GET https://api.openweathermap.org/data/2.5/weather?q={city_name}&appid={API_KEY}&units=metric`
- **One Call API**: `GET https://api.openweathermap.org/data/2.5/onecall?lat={lat}&lon={lon}&exclude=minutely&appid={API_KEY}`
