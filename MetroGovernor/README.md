# Metro Governor

A city-building and regional governance game for Android, built from the GameSoul design. You govern a tropical island: a coastal capital, Central Park, and seven jungle sub-towns inland. You never appear on screen. You zone land, lay roads, place utilities and services, set taxes and budgets, and watch districts grow.

## Get the APK on your phone

1. On GitHub, create a new repository named `MetroGovernor`. Leave README, gitignore and license unchecked.
2. Unzip this project, open the folder, select everything inside it and drag it onto the repo's "uploading an existing file" page. The `.github` folder, `www`, `icons` and this README all go at the top level. Commit.
   - If the `.github` folder doesn't upload by drag and drop, choose **Add file > Create new file**, type `.github/workflows/build-apk.yml` as the name, and paste in that file's contents.
3. Open the **Actions** tab. The build runs by itself in about 4 minutes.
4. When it's green, open the **Releases** page on your phone, tap `MetroGovernor.apk`, and open it to install. Play Protect may ask; choose "Install anyway" or "Scan app".

Every later upload builds a new version that installs over the old one. Your saved term stays on the phone.

## How to play

- **Start**: the capital has a small road grid and residential lots waiting. Build a power plant and a water tower so families can move in.
- **Zone**: drag rectangles of homes, shops and industry. Lots grow when they have a road beside them, power and water, and demand (the three bars at the end of the tool dock).
- **Revenue** comes from shops and industry. Higher taxes slow business and raise the cost of living.
- **Satisfaction** comes from power and water, clinics, schools and safety, parks and pools, jobs, cost of living, and clean air with some jungle kept.
- **First goal**: a stable, profitable capital (satisfaction 55+ and a positive budget for three months). Then expand to a second district.
- **Region**: at 500 residents in the capital, found sub-towns from the region map. Each has its own character. Falling satisfaction sends residents to other towns; debt cuts services to 70%.
- **The win condition** is the Governor's record: months in a row of a happy (60+), profitable region. The game is an open sandbox; there's no end.

Controls: one finger paints with the current tool, or pans with Inspect. Two fingers pan, pinch to zoom, twist to rotate. The left buttons rotate and zoom.

## What came from each repo

- **Bubble**: all 72 Central Park places, buildable as parks (one each across the island), and the Mapbox maps. The Parks atlas shows the real parks on a Mapbox street map. The region map draws the island with Mapbox GL.
- **ParkCommand**: the seven pools (Splash Landing, Aviator, F-15, Jet Stream, Puddle Jumper, Maverick, Runway 35) as aquatic centers, weather holds during storms, the pool board, and the Barlow fonts.
- **AquaticsTech**: pool plant upkeep, condition, and the parts-replaced log.
- **VoluntTold**: field reports from residents, and volunteer days.
- **bomba-live**: the Bomba Live news channel.
- **Orbit, ParkCommand, Bubble**: the Android build setup (WebView app built by GitHub Actions, fixed signing key).

## Change the game

Edit files in `www/`, upload them, and the APK rebuilds. `sim.js` is the simulation and balance, `render.js` the 3D city, `ui.js` the interface and maps, `audio.js` the music, `data.js` the parks list and Mapbox token.

The atlas street map needs internet and a Mapbox token that allows `https://bombarules.github.io` (the same token and address as Bubble). Everything else works offline.
