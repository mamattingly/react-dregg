# DREDGE Collection Planner

An independent, unofficial React + Vite fan-made companion for tracking DREDGE books and selected unique equipment rewards.

## Features
- Automatically saved progress using browser `localStorage`.
- Region-ordered remaining objective list; completed steps disappear from the route.
- Book and unique equipment checklists.
- Search and region filters.
- JSON export/import for moving progress between browsers/devices.
- Installable PWA shell with basic offline caching.
- Original interface and explanatory text; system fonts; no game artwork or extracted game assets.

## Run locally
```bash
npm install
npm run dev
```

## Build
```bash
npm run build
npm run preview
```

## Deploy to Render
Create a **Static Site** connected to this GitHub repository:
- Build command: `npm install && npm run build`
- Publish directory: `dist`

No server, database, environment variables, or API keys are required.

## Progress storage
Progress is stored in this browser's local storage. It persists across reloads and browser restarts in the same browser profile. Use **Export progress** to back up or move it. Clearing browser data can erase local progress.

## Route planner note
The route groups tasks in a practical regional sequence. Completing a step removes it from the remaining route. This is a region-ordered checklist planner, not a live GPS/navigation solver; fish and delivery objectives can be completed in advance and checked off whenever done.

## Data scope
Includes 13 book entries (base game plus The Pale Reach) and seven selected equipment rewards. Some rewards are DLC-gated. The Iron Rig toggle is currently a planning note; the expansion's full equipment tree is not catalogued in this version.

## Copyright and trademarks
This is an unofficial fan-made project and is not affiliated with or endorsed by the developers or publisher of DREDGE. DREDGE and all related intellectual property remain with their respective owners. The app uses factual game references and independently written descriptions. It contains no game screenshots, extracted game files, official logos, copied maps, music, or other proprietary game assets. The original project code is licensed under MIT; see `LICENSE`. Read `COPYRIGHT_AND_TRADEMARKS.md` for the project's content-provenance policy and limitations.

External community reference pages are linked, not reproduced. Third-party sites retain their own rights and terms.

## Important
This is a copyright-conscious implementation, not a guarantee of legal immunity. Review rights-holder policies and seek legal advice before commercial distribution.
