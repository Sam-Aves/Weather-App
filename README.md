# Atmos: Weather, at a glance

A responsive weather app that shows current conditions, a 24-hour forecast, and a 5-day outlook for any city. The interface adapts its colors, icons, and background particles to the weather it's showing.

**[Live demo](https://sam-aves.github.io/Weather-App/)**

## Features

- **City search** with geocoding, plus quick-city chips and a "recently searched" list saved in `localStorage`
- **Current conditions**: temperature, weather description, wind speed, daily high and low
- **24-hour hourly forecast** and **5-day forecast**; click any hour or day to see it in the main card
- **Weather-aware design**: accent colors shift with temperature, and animated rain, snow, or floating-dust particles are drawn on a canvas
- **Clothing tip** based on temperature and conditions (umbrella, light jacket, sunscreen, and so on)
- **Light and dark mode** that follows your system setting, with a manual toggle
- **Graceful failure**: if the API is unreachable or a city isn't found, the app shows clearly labeled sample data instead of breaking
- **Accessible by design**: semantic HTML, ARIA live regions, keyboard focus styles, screen-reader labels, and `prefers-reduced-motion` support
- **Fully responsive**, from small phones to wide desktops

## Tech stack

- HTML, CSS, and vanilla JavaScript (no frameworks, no build step)
- [Open-Meteo](https://open-meteo.com/) Geocoding and Forecast APIs (free, no API key)
- Canvas API for the weather particles

## Run locally

```bash
git clone https://github.com/sam-aves/Weather-App.git
cd Weather-App
```

Then open `index.html` in your browser. No install or API key is needed.

## How it works

1. The city name is sent to the Open-Meteo geocoding API to get coordinates.
2. Coordinates are sent to the forecast API, which returns current, hourly, and daily data.
3. WMO weather codes are mapped to descriptions, icons, and particle effects.
4. All UI state (selected hour or day, theme, recent cities) is handled in plain JavaScript.

## Project structure

```
.
├── index.html
└── README.md
```

## About this project

I built Atmos to learn AI-assisted web development with GitHub Copilot. I used AI to speed up scaffolding and iteration, and I reviewed and tested the code myself to understand how each part works.

## Roadmap

- [ ] Split into `index.html`, `styles.css`, and `app.js`
- [ ] Add a Node/Express backend to cache API responses
- [ ] User accounts with saved favorite cities
- [ ] °C / °F toggle
- [ ] Use browser geolocation for "my location"
- [ ] Unit tests for the data-mapping functions

## Credits

Weather data by [Open-Meteo](https://open-meteo.com/).

## License

MIT

## Author

**Asliraf Samaylan**: [GitHub](https://github.com/sam-aves)