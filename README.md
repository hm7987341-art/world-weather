# WORLD WEATHER

A full-stack, mobile-first weather application with live global weather data, geocoding, current conditions, 24-hour hourly forecast, 10-day forecast, precipitation, wind, humidity/UV/dew point, sunrise/sunset, saved locations, location detection, responsive UI, adaptive atmospheric backgrounds, loading/error states and an OpenStreetMap map view.

## Data architecture

- Weather: Open-Meteo Forecast API
- Geocoding/reverse geocoding: Open-Meteo Geocoding API
- Coordinates are used as the canonical weather lookup key after location selection.
- Server-side proxy adds response caching and keeps the browser architecture independent of provider URLs.
- No fake or hardcoded production weather values are used. The initial location is only a default coordinate for first launch.

## Run locally

Requirements: Node.js 20+

```bash
npm install
npm run dev
```

Frontend: http://localhost:5173
API: http://localhost:8787

Production build:

```bash
npm run build
npm start
```

Set `CLIENT_ORIGIN` and `PORT` on the server if deploying behind a reverse proxy. Set `VITE_API_BASE` on the client when the API is hosted on a separate origin.

## Notes

The implementation uses Open-Meteo as the live provider so it can run without a Google Cloud credential. A provider adapter can be added later for Google Weather API if you have the required project/API access. Official provider alerts are not fabricated; the UI is ready for an alert adapter when an alert-capable provider is configured.
