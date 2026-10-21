# Tiny Weather

A minimal frontend that **requires a sandbox environment variable** to fetch San Francisco weather. There is no API-key input or fallback key.

## Run

1. Set `VITE_OPENWEATHER_API_KEY` in your sandbox environment to an OpenWeather API key. Locally, you can copy `.env.example` to `.env.local` and fill in the value instead.
2. Run `npm install`.
3. Run `npm run dev`. Restart the server after changing the variable.

Without the variable, the page shows a setup error and disables the weather button. `npm run build` embeds the configured value into the frontend; set it before building. The page can render without a key, but weather requests cannot run.

Get a key at https://home.openweathermap.org/api_keys. This deliberately simple frontend sends the key directly to OpenWeather. Vite exposes `VITE_` values to the browser, so this is not a secret-storage example. Never commit a real key.
