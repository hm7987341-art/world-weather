# WORLD WEATHER: mobile app-style deployment

This build is PWA-ready. It serves the React app and `/api/*` from the same Node/Express service.

## Build
`npm install && npm run build`

## Start
`NODE_ENV=production SERVE_CLIENT=true npm start`

After deployment to an HTTPS URL, open it in Chrome on Android and choose **Install app** or **Add to Home screen**. It will launch as WORLD WEATHER in standalone app mode.

The app uses live Open-Meteo data and coordinate-based geocoding/weather requests.
