# WeatherLens v1 — Original

A real-time weather dashboard built as a single HTML file. No build tools, no frameworks, no dependencies beyond Chart.js — just open in a browser and go.

---

## Overview

The original build. Functional, clean, and well-structured. Focused on getting all weather data on screen with a minimal dark aesthetic using DM Serif Display typography and a deep navy color palette.

---

## Features

- City search with keyboard support (Enter key)
- GPS geolocation button
- °C / °F unit toggle
- Live current conditions — temperature, feels like, humidity, wind speed, visibility, pressure
- Sunrise & sunset times
- 5-day forecast grid
- 8-hour hourly scroll strip
- Air Quality Index (AQI) with pollutant breakdown (CO, NO₂, O₃, PM2.5, PM10)
- Temperature trend line chart (Chart.js)
- Humidity & wind bar chart (Chart.js)
- Demo data fallback — loads Mumbai by default when no API key is set
- Responsive layout for mobile and tablet

---

## Language Stack

| Language | Lines | Percentage |
|----------|-------|------------|
| JavaScript | 357 | 45.9% |
| CSS | 269 | 34.6% |
| HTML | 151 | 19.4% |
| TypeScript | 0 | 0% |
| **Total** | **777** | |

---

## Fonts

| Font | Usage |
|------|-------|
| DM Serif Display | Headings, city name, logo |
| DM Sans | Body text, labels, buttons |
| JetBrains Mono | Temperature, numbers, data values |

All fonts loaded via Google Fonts CDN — no install needed.

---

## External Dependencies

| Library | Version | Purpose | Load method |
|---------|---------|---------|-------------|
| Chart.js | 4.4.1 | Line and bar charts | CDN |
| OpenWeatherMap API | v2.5 | Weather data | REST / fetch |

---

## API Endpoints Used

| Endpoint | Data fetched |
|----------|-------------|
| `/data/2.5/weather` | Current conditions |
| `/data/2.5/forecast` | 5-day / 3-hour forecast |
| `/data/2.5/air_pollution` | AQI and pollutant levels |

---

## Setup

### 1. Get a free API key
Sign up at [openweathermap.org](https://openweathermap.org/api). The free tier covers all three endpoints used here.

### 2. Add your key
Open `weather-dashboard.html` and find this line near the top of the `<script>` block:

```js
const API_KEY = 'YOUR_API_KEY_HERE';
```

Replace it with your actual key.

### 3. Open in browser
No server needed. Double-click the file or drag it into any browser. Works without a key too — falls back to static demo data for Mumbai.

---

## Design Tokens

```css
--bg:        #0a0f1e   /* page background      */
--surface:   #111827   /* card surfaces        */
--surface2:  #1a2235   /* elevated surfaces    */
--accent:    #38bdf8   /* primary blue         */
--accent2:   #818cf8   /* secondary purple     */
--warm:      #fb923c   /* warm amber           */
--success:   #34d399   /* green                */
--danger:    #f87171   /* red                  */
```

---

## Browser Support

Works in all modern browsers — Chrome, Firefox, Safari, Edge (2018+). No polyfills required.

---

## License

Free to use and modify. Weather data provided by OpenWeatherMap under their terms of service.
