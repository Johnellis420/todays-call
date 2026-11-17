# Today's Call

A free, private training app for your phone. Each morning you log sleep, soreness and energy, and Today's Call tells you whether to **rest**, go **hypertrophy**, or go **heavy**. It also:

- builds the day's workout from your split, with suggested weights based on your recent lifts
- learns your own exercises and set counts after you've logged a split day twice
- tracks every lift with PRs, estimated 1-rep max, and progress charts
- times your meals around training (pre-workout, post-workout, before bed)

No account, no ads, no tracking. All data stays on the phone in the browser's storage. Users can save a backup file and restore it on a new phone.

## Install on a phone

Open the site, then:
- **iPhone (Safari):** Share → Add to Home Screen
- **Android (Chrome):** ⋮ menu → Add to Home screen / Install app

It opens full screen and works offline.

## How it's built

A single static page with no build step and no server:

- `index.html`: the whole app (HTML, CSS, JavaScript)
- `sw.js`: service worker for offline use and update prompts
- `manifest.webmanifest`, `icons/`: home-screen install
- `fonts/`: Inter and Barlow Condensed (SIL Open Font License), bundled so nothing loads from third parties

Hosted on GitHub Pages.

## Releasing a change

1. Edit the files.
2. Bump `APP_VERSION` in `index.html` and `VERSION` in `sw.js`.
3. Push to `main`. Phones that have the app open get an "Update" banner.

## Disclaimer

Today's Call gives general fitness guidance, not medical advice. Readiness calls and weight suggestions are rules of thumb. Protein guidance follows the International Society of Sports Nutrition position stands.
