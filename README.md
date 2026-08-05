# Daily

A personal daily dashboard — one mobile-friendly page that replaces a handful of apps I used to check every morning. Single HTML file, no build step, no backend. Hosted on GitHub Pages.

## Tabs

- **Habits** — tap-to-mark daily habits with streaks and a 4-week grid
- **Calendar** — upcoming events from a personal iCal link
- **Weather** — current conditions, hourly + 5-day forecast, and remaining daylight
- **BBC News / BBC Sport / Al Jazeera** — latest headlines with links to full articles

Plus a daily quote in the header, and a dark / light theme toggle.

## Setup

1. Drop `index.html` in the repo and enable GitHub Pages (Settings → Pages).
2. Open the hosted `https://<you>.github.io/...` URL — not the local file, or the news feeds won't load.
3. **Weather** works out of the box (Edinburgh). Change `LAT` / `LON` near the top of the script for elsewhere.
4. **Calendar** — open the Calendar tab and paste your Google Calendar *secret iCal address* (Settings → your calendar → *Secret address in iCal format*). It's stored in your browser only, never in the repo.

Add to your home screen to use it like an app.

## How it works

- **Weather** — [Open-Meteo](https://open-meteo.com), no key required.
- **News & calendar** — fetched via public CORS proxies, since these sources don't allow direct browser requests.
- **Quote** — [ZenQuotes](https://zenquotes.io), with an offline fallback so the header is never empty.
- **Habits, calendar link, and theme** — saved in the browser's `localStorage`, on-device only.

## Notes

- All personal data stays in your browser. Nothing is committed to the repo and there are no accounts.
- The public proxies are free and occasionally flaky; if a feed fails, hit refresh or try again later.

Built for personal use. Fork it and make it yours.
