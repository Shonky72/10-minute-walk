# Ten Minute Loop

One page. Open it on your phone, allow location, get a ~10 minute walking loop that starts and ends where you stand. Tap **New loop** for a different one.

- Map: Leaflet + OpenStreetMap tiles
- Routing: OSRM car profile at routing.openstreetmap.de (no API key). Car profile means real streets only. Loops that touch a lane, alley or unnamed way are thrown out and re-rolled.
- Distance is never under the 10 minute target. Slightly over is accepted.
- Pace assumed: 80 m/min. Change `MINUTES` or `PACE_M_PER_MIN` in `index.html`.

Needs HTTPS for location. Host anywhere static (GitHub Pages, Vercel, Netlify).
