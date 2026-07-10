# Folly Flow 🌊

🇺🇸 [English](#) · 🇪🇸 [Español](#) · 🇫🇷 [Français](#) · 🇩🇪 [Deutsch](#) · 🇧🇷 [Português](#) · 🇨🇳 [中文](#) · 🇯🇵 [日本語](#) · 🇰🇷 [한국어](#) · 🇮🇹 [Italiano](#) · 🇸🇦 [العربية](#)

**Live Crowd + Traffic Meter for Any US Beach**

Real conditions so you know if it's worth driving down — pick your own beach, not just Folly.

### ✨ Live Demo
**[dacameragirl.github.io/Folly-Beach-Flow](https://dacameragirl.github.io/Folly-Beach-Flow/)**

### Choose Your Beach
- Pick from a curated list of popular US beaches (Folly Beach, Myrtle Beach, Virginia Beach, Miami Beach, Santa Monica, and more)
- Search any US location by name (powered by OpenStreetMap Nominatim)
- Or tap "Use My Location" to jump straight to wherever you are
- Your last choice is remembered on your next visit

Kept to the US so every card stays backed by real, free data — tide predictions in particular are a US-only free API (NOAA), so expanding worldwide would mean the tide card silently goes fake outside the US, which defeats the point.

### What's Actually Real vs. Estimated

| Card | Data | Source |
|---|---|---|
| 🚗 Road Traffic | **Real** — live speed vs. normal free-flow speed for the road nearest your selected beach | [TomTom Traffic Flow API](https://developer.tomtom.com/traffic-api) |
| 🚗 Road Map | **Real** — live embedded map of the actual location | Google Maps |
| 🌊 Tide Forecast | **Real** — hourly water level + today's actual high/low from whichever NOAA station near your beach actually publishes usable predictions | [NOAA CO-OPS](https://tidesandcurrents.noaa.gov/) (nearest of ~3,500 US stations, resolved dynamically) |
| ☀️ Live Weather | **Real** — current temperature, wind, and conditions from the nearest reporting station | [National Weather Service](https://www.weather.gov/documentation/services-web-api) (station resolved dynamically per beach) |
| ⚠️ Weather Alerts | **Real** — any active NWS warning (severe thunderstorm, flood, extreme heat, etc.) for your beach, issued the moment a forecaster calls it | [NWS Active Alerts](https://www.weather.gov/documentation/services-web-api) |
| 👥 Crowd Level | **Estimated** — an algorithmic guess from time of day, weekend/weekday, live weather, and active alerts. There's no free public sensor for actual beach headcount, so this is honestly labeled as an estimate, not a live reading. |
| 🚗 Animated cars on the road | **Stylized** — a visual density cue driven by the real TomTom congestion number, not an exact vehicle count (TomTom's free tier reports speed, not volume) |

### Features
- Real photo hero instead of a CSS-drawn ocean/sun
- Pick any US beach: curated list, free-text search, or "Use My Location"
- Live NOAA tide chart with today's actual high/low, wherever you are
- Live NWS weather (temperature, wind, conditions) and active severe-weather alerts
- Live TomTom traffic speed near your beach, plus an embedded live map
- Honest, weather/time-driven crowd estimate (no more random numbers)
- Mobile-friendly, works offline for the static shell

### Why It Exists
After the July 4th chaos, I wanted to know instantly if Folly was still packed or finally chill.

---

### Tech Stack
- HTML • CSS • JavaScript
- NOAA CO-OPS, National Weather Service, and TomTom Traffic Flow APIs (all called directly from the browser, no backend)

### Photo Credit
Hero photo: *Folly-Beach-Pier-sc.jpg* by Brian Stansberry, [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/), via [Wikimedia Commons](https://commons.wikimedia.org/wiki/File:Folly-Beach-Pier-sc.jpg). It's a fixed brand backdrop for the app, not a live photo of whichever beach you select.

### Search Attribution
Beach search and "Use My Location" reverse-geocoding use OpenStreetMap Nominatim. Data © OpenStreetMap contributors, ODbL.

---

### How to Use
1. Open `index.html` in any browser, or visit the live demo link above
2. Bookmark it or "Add to Home Screen" on your phone
3. Hit Refresh for the latest conditions

### A Note on the TomTom Key
`index.html` includes a client-side TomTom API key (this is TomTom's normal usage model for their free tier, similar to a Google Maps browser key). It's recommended to add an HTTP-referrer restriction for this domain in the TomTom developer dashboard so the key can't be hotlinked from other sites.

### Future Plans
- User crowd reports
- 7-day tide/weather history graph
- Push notifications

---

Made with 🏖️ for Folly Lovers
