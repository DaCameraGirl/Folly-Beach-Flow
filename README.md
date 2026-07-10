# Folly Flow 🌊

🇺🇸 [English](#) · 🇪🇸 [Español](#) · 🇫🇷 [Français](#) · 🇩🇪 [Deutsch](#) · 🇧🇷 [Português](#) · 🇨🇳 [中文](#) · 🇯🇵 [日本語](#) · 🇰🇷 [한국어](#) · 🇮🇹 [Italiano](#) · 🇸🇦 [العربية](#)

**Live Crowd + Traffic Meter for Folly Beach, SC**

Real conditions so you know if it's worth driving down.

### ✨ Live Demo
**[dacameragirl.github.io/Folly-Beach-Flow](https://dacameragirl.github.io/Folly-Beach-Flow/)**

### What's Actually Real vs. Estimated

| Card | Data | Source |
|---|---|---|
| 🌉 Bridge Traffic | **Real** — live speed vs. normal free-flow speed for the Folly Road bridge | [TomTom Traffic Flow API](https://developer.tomtom.com/traffic-api) |
| 🌉 Bridge Map | **Real** — live embedded map of the actual bridge crossing | Google Maps |
| 🌊 Tide Forecast | **Real** — hourly water level + today's actual high/low | [NOAA CO-OPS](https://tidesandcurrents.noaa.gov/) (Charleston Harbor station 8665530) |
| ☀️ Live Weather | **Real** — current temperature, wind, and conditions | [National Weather Service](https://www.weather.gov/documentation/services-web-api) (station KJZI) |
| 👥 Crowd Level | **Estimated** — an algorithmic guess from time of day, weekend/weekday, and live weather. There's no free public sensor for actual beach headcount, so this is honestly labeled as an estimate, not a live reading. |
| 🚗 Animated cars on the bridge | **Stylized** — a visual density cue driven by the real TomTom congestion number, not an exact vehicle count (TomTom's free tier reports speed, not volume) |

### Features
- Real photo hero (Folly Beach Pier) instead of a CSS-drawn ocean/sun
- Live NOAA tide chart with today's actual high/low
- Live NWS weather (temperature, wind, conditions)
- Live TomTom traffic speed for the Folly Road bridge, plus an embedded live map
- Honest, weather/time-driven crowd estimate (no more random numbers)
- Mobile-friendly, works offline for the static shell

### Why It Exists
After the July 4th chaos, I wanted to know instantly if Folly was still packed or finally chill.

---

### Tech Stack
- HTML • CSS • JavaScript
- NOAA CO-OPS, National Weather Service, and TomTom Traffic Flow APIs (all called directly from the browser, no backend)

### Photo Credit
Hero photo: *Folly-Beach-Pier-sc.jpg* by Brian Stansberry, [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/), via [Wikimedia Commons](https://commons.wikimedia.org/wiki/File:Folly-Beach-Pier-sc.jpg).

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
