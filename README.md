# Mohammad Dawood Saddiqi: portfolio website

A one-page static website presenting Mohammad Dawood Saddiqi (software developer, lecturer at
Ghalib University, in charge of Ghalib Software Service Company, owner of Cyber System Software
House) and his systems: Hesab-o-Ketab, ZargarMan System, Naft System and other websites.

* Languages: English, Dari and Pashto (switcher at the top right; Dari and Pashto are right to left).
* No build step, no server code, no database, no cookies, no tracking. Plain HTML, CSS and a small script.
* Light and dark appearance follow the visitor's setting, with a toggle in the header that is remembered on that device.
* Also the public home for Hesab-o-Ketab's privacy policy, which Google Play needs (`hesab-o-ketab/privacy-policy/`).

## Folder layout

| Path | What |
|---|---|
| `index.html` | The whole site: content, styles and the language switcher script. English text is in the page; Dari and Pashto texts are in the `T` dictionary inside the script. |
| `assets/photo.jpg`, `assets/photo-360.jpg` | Portrait, square crops (720 px and 360 px), metadata removed. |
| `assets/icon-192.jpg` | Browser tab icon. |
| `hesab-o-ketab/privacy-policy/` | Hesab-o-Ketab privacy policy (a copy of `ModerMan/privacy-policy/index.html` from the app work; copy it again whenever the app's policy changes). |
| `docs/` | Startup, troubleshooting and editing guides. |

## Guides

* [docs/STARTUP_GUIDE.md](docs/STARTUP_GUIDE.md): preview on your computer and put the site online.
* [docs/TROUBLESHOOTING.md](docs/TROUBLESHOOTING.md): common problems and fixes.
* [docs/USER_GUIDE.md](docs/USER_GUIDE.md): how visitors use the site and how to edit its text.

## Status

* ZargarMan System and Naft System show their names only ("Description coming soon") until a
  description is supplied. Nothing about them was invented.
* The page uses Google Fonts (Sora, Source Sans 3, IBM Plex Mono, Vazirmatn). Without internet
  access to Google Fonts it falls back to system fonts and still works.
* Dari and Pashto wording should be read once by a native speaker.
