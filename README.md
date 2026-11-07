# E DAILY

A single-file, client-side news reader. Pulls top headlines from the [GNews](https://gnews.io) API and renders them as a newspaper-style feed, with a world map heatmap view, a stock/market snapshot panel (mock data), text-to-speech article playback, and PDF digest export.

Everything lives in `E-paper.html` — no build step, no server required.

## Setup

1. Get a free API key from [gnews.io](https://gnews.io).
2. Copy `config.example.js` to `config.js`:
   ```
   cp config.example.js config.js
   ```
3. Edit `config.js` and replace `YOUR_GNEWS_API_KEY_HERE` with your key.
4. Open `E-paper.html` in a browser (or serve the folder with any static file server).

`config.js` is gitignored — your key never gets committed.

## Features

- Top headlines by country, with search/filter
- World map heatmap view (Leaflet)
- Mock stock market / exchange / commodities snapshot (Chart.js)
- Text-to-speech playback per article, with on-the-fly Urdu translation
- Save article as image (html2canvas) or export a PDF digest (jsPDF)
- Light/dark theme toggle
- Browser push notifications for breaking news

## Notes

- This is a static frontend-only app: the GNews key is loaded in the browser and is visible to anyone who opens dev tools. Don't use a key you need to keep fully secret — for production use, proxy GNews requests through a small backend instead.
- Stock/market data is mocked; there's no real financial data source wired up.
