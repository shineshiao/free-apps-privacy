# free-apps-privacy

Privacy policy pages for the [free-apps](https://github.com/shineshiao/free-apps)
monorepo, published via GitHub Pages at
https://shineshiao.github.io/free-apps-privacy/

One folder per app, each with its own `index.html`:

- `decision-wheel/` — Decision Wheel (`com.shineshiao.decisionwheel`)
- `countdown-timer/` — Countdown Timer (`com.shineshiao.countdowntimer`)
- `bmi-body-metrics/` — BMI & Body Metrics (`com.shineshiao.bmibodymetrics`)
- `snapend/` — Snapend (`com.shineshiao.snapend`)

`index.html` at the root lists all of them.

## Adding a new app

1. Copy an existing app folder (e.g. `decision-wheel/`) to `<new-app>/`.
2. Update the title, package name, app description, and the
   "Information stored on your device" / analytics-event copy to match
   what the new app actually does and collects — check its `pubspec.yaml`
   for which Firebase/AdMob services it actually uses before copying the
   data table verbatim.
3. Add a link to it in the root `index.html`.
4. Point that app's Play Console "Privacy policy" field at
   `https://shineshiao.github.io/free-apps-privacy/<new-app>/`.

## Updating shared boilerplate

The Google Privacy Policy links, retention periods, and contact email are
duplicated across every app page (kept as static HTML on purpose — no
build step). If one of those changes, update it in each `index.html`.
