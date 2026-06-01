# Antarctic Mapping Database

A web-based mapping application for Antarctic place names, research facilities and geospatial data.

## Live App
Open in your browser: `https://yourusername.github.io/antarctic-mapping-database`

## Files
- `index.html` — the app
- `scar_data.js` — 40,127 SCAR Antarctic place names
- `contours_low.js` — ADD contour lines (low resolution, loads at startup)
- `contours_high.js` — ADD contour lines (medium resolution, downloads on demand ~37MB)
- `facilities.js` — 114 COMNAP research facilities
- `claims.js` — Antarctic territorial claims boundaries
- `sw.js` — service worker for offline support
- `manifest.json` — PWA manifest for installing on iPhone/iPad

## Installing on iPhone
1. Open the GitHub Pages URL in **Safari**
2. Tap Share → **Add to Home Screen**
3. Opens like a native app, works offline after first load

## Running locally (for development)
Cannot be opened by double-clicking index.html — needs a local server:
```
cd /path/to/files
python3 -m http.server 8080
```
Then open `http://localhost:8080`

## Importing your own data
Use the ⧉ Layers button → + Add file. Supports:
- GeoJSON (.geojson, .json)
- KML / KMZ (.kml, .kmz)
- GPX tracks and waypoints (.gpx)
- GeoTIFF rasters (.tif) — Mercator view only. LERC-compressed files
  need re-exporting from QGIS: Raster → Convert → Cloud Optimised GeoTIFF
  with Deflate or LZW compression.
