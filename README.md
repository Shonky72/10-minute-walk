# Ten Minute Loop

One page. Open it on your phone, allow location, get a walking loop that starts and ends on the nearest named street. Tap **New loop** for a different one, **Locate** for a fresh GPS fix.

- Map: Leaflet + OpenStreetMap tiles
- Routing: OSRM car profile at routing.openstreetmap.de (no API key). Car profile means real streets only. Loops that touch a lane, alley or unnamed way are thrown out and re-rolled.
- Start and every waypoint snap to the nearest *named* street via OSRM `nearest` (lanes, alleys, unnamed ways skipped).
- Loop is a ring of waypoints on a circle through the start, tangent to the street, with departure and arrival bearings locked so you leave one way and return the other. Any route that walks a segment twice is rejected and re-rolled.
- Direction arrows on the line, a collapsible turn list, screen stays awake, slider setting remembered.
- Distance is never under the target. Up to 30% over is accepted.
- Slider sets the target: minutes (10 to 120, step 10) or km (1 to 15, step 1). Pace assumed 80 m/min; change `PACE_M_PER_MIN` in `index.html`.

Needs HTTPS for location. Host anywhere static (GitHub Pages, Vercel, Netlify).
