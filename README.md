# Track Log PWA v1

A mobile-first, monochrome track-day logbook that can be hosted on GitHub Pages.

## Files

- `index.html` — full app UI, forms, storage logic, comparisons and styling.
- `manifest.webmanifest` — installable PWA metadata.
- `sw.js` — app-shell caching for offline loading after the first successful visit.
- `icon-192.png` and `icon-512.png` — app icons used by the manifest, page favicon and header. Both PNG files must be in the same folder as `index.html`.

## Publish on GitHub Pages

1. Add `index.html`, `manifest.webmanifest`, `sw.js`, `icon-192.png` and `icon-512.png` to the root of the repository (or keep them together in the configured Pages folder).
2. Commit and push.
3. In GitHub, open **Settings → Pages** and enable deployment from the intended branch/folder.
4. Open the published HTTPS URL once while online. Then use the browser menu to install/add it to the home screen.

## Included in v1

- Add multiple cars, vehicle photos, nicknames, registration/year and a basic mods/setup list.
- Add tracks, track photos, multiple named layouts, direction and layout notes/photos.
- Log track days by car, date, track and exact layout.
- Manually enter a best lap and optional individual lap times, conditions, tyres, pressures, setup and notes.
- Personal bests are calculated by **car + track + layout**; different layouts are not compared.
- Export/import a JSON backup that includes photos and records.
- IndexedDB persistence, with localStorage fallback where IndexedDB is unavailable.
- Offline app-shell support after the first successful online load.

## Data and limitations

- Data stays in the browser on the device where it was entered. There is no cloud sync or shared account in v1.
- Export backups regularly and before clearing browser data, changing devices or reinstalling the browser.
- Browser storage can still be cleared by the user, browser settings or device cleanup. Export is the backup, not a decorative button.
- Lap times are entered manually from your timing app. The app does not connect to Lap Trophy.
- Setup notes are records, not proof that a modification caused a time improvement.
- The SVG icon is a scalable starter icon. If a store or platform specifically requires raster icons, create 192×192 and 512×512 PNG versions and add those to the manifest.

## Next iteration ideas

- Session and lap progression charts.
- More detailed setup history with dated changes and tyre set tracking.
- Optional CSV export and printable track-day report.
- Dedicated track/layout detail screens and richer weather data.
