# DREDGE Collection Planner

An independent, unofficial React + Vite companion for tracking books, unique equipment, and selected DLC rewards in DREDGE.

## Features
- **Interactive schematic chart** showing the starting point, objective POIs, numbered route stops, and the recommended sequence.
- **Configurable starting point:** choose from listed docks, characters, altars, and DLC destinations, or select **Custom point — click the map** to place your start at any chart location. Name the custom point if desired.
- **Route optimization:** unfinished objective stops are sequenced from the selected start using a nearest-stop heuristic followed by 2-opt crossing reduction. Checking off objectives immediately recalculates the route.
- **Mini route checklist:** expand a stop, check off its tasks, and watch the route update.
- **Collection filters:** all objectives, books only, all equipment, rods, crab pots, trawl nets, gadgets, talismans, or engines; also filter by content pack and search names/effects/fish/locations.
- **DLC modules:** independently enable or disable The Pale Reach, The Iron Rig, and Blackstone Key. Progress remains saved when a module is disabled.
- **Local progress persistence** with JSON export/import.
- **Responsive layout** and basic PWA/offline shell.
- Original schematic map, interface, code and explanatory text; no game artwork, screenshots, official logos, copied map image, music, or extracted game files.

## Run locally
```bash
yarn install
yarn dev
```

## Build
```bash
yarn build
yarn preview
```

## Deploy to Render
Create a **Static Site** connected to this repository:
- Build command: `yarn install && yarn build`
- Publish directory: `dist`
- Environment variables: none
- Start command: none (Static Sites do not need one)

No server, database, API keys, or environment variables are required.

## Route-planning limitations
The route order is a **map-distance heuristic**, not a true nautical shortest-path solver. It uses straight-line distance between the schematic POI coordinates and does not model coastlines, navigable channels, hazards, currents, boat speed, fuel, or day/night. Use the sequence as a planning aid and follow the in-game chart while sailing. Some checklist steps (especially catching fish) occur away from the final turn-in POI; the map plots the item's primary objective/turn-in location and the checklist retains the prerequisite steps.

The POI selector includes the named docks, selected characters, altars, and supported DLC destinations represented in the planner. To start from any other in-game point, choose **Custom point — click the map** and click the corresponding chart position. The schematic is an original approximation, not an official game map.

## Data scope
The base-game book list and selected unique equipment are included, along with a broader set of Pale Reach, Iron Rig, and Blackstone Key equipment rewards. DLC coverage is structured as separate enable/disable content packs so additional records can be added without changing the route engine. Some acquisition steps are concise planning summaries; verify detailed requirements in-game or against the linked reference sources.

## Progress storage
Progress and settings are saved in this browser's local storage. They persist across reloads in the same browser profile, but are not shared between devices or browsers. Use **Export progress** to back up or move progress. The app attempts to migrate existing v1 planner progress automatically. Clearing browser data can erase local progress.

## Copyright and trademarks
This is an unofficial fan-made project and is not affiliated with or endorsed by the developers or publisher of DREDGE. DREDGE and all related intellectual property remain with their respective owners. The app uses factual game references and independently written descriptions. It contains no game screenshots, extracted game files, official logos, copied maps, music, or other proprietary game assets. The schematic map is original. The original project code is licensed under MIT; see `LICENSE` and `COPYRIGHT_AND_TRADEMARKS.md`.

External community reference pages are linked, not reproduced. Third-party sites retain their own rights and terms.

## Important
This is a copyright-conscious implementation, not a guarantee of legal immunity. Review rights-holder policies and seek legal advice before commercial distribution.
\n\n## Map reference\nThe interactive route layer is drawn over the map image supplied by the project owner. Base-game POIs are plotted on the supplied chart. Pale Reach and Iron Rig are DLC modules; their destinations are indicated at the chart edge because the supplied image does not depict their separate areas. The route is a planning heuristic, not turn-by-turn navigational routing.\n