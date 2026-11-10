# summitweather-support

Help page, privacy policy and EULA for the iPhone app **Mountain Weather: Summit**. GitHub Pages builds it with Jekyll.

| File | Served at | Used for |
|---|---|---|
| `index.md` | `https://developer-barseghyan.github.io/summitweather-support/` | Support URL in App Store Connect, Help link in the app |
| `privacy.md` | `https://developer-barseghyan.github.io/summitweather-support/privacy` | Privacy Policy URL, "Privacy Policy" link in the app |
| `terms.md` | `https://developer-barseghyan.github.io/summitweather-support/terms` | "Terms of Use (EULA)" link in the app, paywall and description |

The app hard-codes these three addresses in `SummitWeather/App/Config/AppFacts.swift`, so keep the repository name and the `permalink` lines as they are.

## Layout

`_layouts/default.html` holds all markup and CSS: a frosted top strip with the icon, app name and page menu, the page body on a dark gradient, and a short base note. Class names start with `sw-` and CSS variables with `--sw-`. The palette is the app's: ground `#0C0D0F`, ink `#F4F1EA`, amber `#F2B544`, cold blue `#7FC7FF`. Each page sets `sw_section` (`help`, `privacy`, `terms`) in its front matter to mark the current menu item. Only `assets/icon.png` and `assets/favicon.png` are used. There are no outside fonts or scripts.

## Publishing

1. Push this folder to the public `developer-barseghyan/summitweather-support` repository.
2. In Settings, Pages, deploy from the `main` branch, root folder.
3. Open all three addresses on a phone and on a desktop.
4. Add the site to the apps list on `developer-barseghyan.github.io`.

## Keep in sync

- The effective date on `privacy.md` and `terms.md` is 10 November 2026. Change it whenever the text changes.
- If the app starts collecting any data beyond the weather requests, update `privacy.md` and the App Store privacy label together. Version 1.0 declares Location (not linked, not for tracking) because route coordinates go to MET Norway.
- Prices and the free/Pro split on the help page and in the EULA must match App Store Connect and `Paywall.swift`.
- If a second weather provider (Open-Meteo) is switched on, add it to the data flows table, the help page's data sources and the EULA's Part E.
