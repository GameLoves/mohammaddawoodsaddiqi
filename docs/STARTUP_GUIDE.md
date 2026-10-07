# Startup guide

The site is static files. Nothing needs to be installed on a server and no service has to run
before it opens: no database, cache, background worker or container.

## Requirements

| Item | Version | Needed for |
|---|---|---|
| Any modern browser (Chrome, Edge, Firefox, Safari; Android or iOS) | 2023 or newer | Viewing |
| Python 3 | 3.8 or newer | Optional local preview server |
| A GitHub account (`dawoodsaddiqi1998`) | n/a | Free hosting on GitHub Pages |

Supported systems for preview: Windows 10/11, macOS, Linux. Ports: 8000 for the optional local preview only.

## 1. Preview on your computer

Quick look: double-click `index.html`. Everything works except that the browser may block the
language choice from being remembered.

Proper preview (same as the live site). Working directory: the `Portfolio` folder.

```bash
# Windows (PowerShell): py -m http.server 8000
python3 -m http.server 8000
```

Expected output: `Serving HTTP on :: port 8000 ...`. Open **http://localhost:8000/** in a browser.
Add `?lang=fa` or `?lang=ps` to open directly in Dari or Pashto. Stop with **Ctrl+C**.

Ready check: the page shows the photo and name, and the English / دری / پښتو buttons switch language.

## 2. Put the site online with GitHub Pages (free)

Publishing makes the photo and phone number public. Do this only when you are happy with the text.

1. Sign in at https://github.com and use the public repository **`GameLoves/mohammaddawoodsaddiqi`**.
   Its name gives the address `https://gameloves.github.io/mohammaddawoodsaddiqi/`
   (a repository named `GameLoves.github.io` would give the shorter root address instead).
2. In the repository, choose **Add file → Upload files**, and drag in the *contents* of the
   `Portfolio` folder (`index.html`, `assets`, `hesab-o-ketab`, and optionally `README.md` and `docs`).
   Click **Commit changes**.
3. Open **Settings → Pages**. Under **Build and deployment**, choose **Deploy from a branch**,
   branch **main**, folder **/ (root)**, then **Save**.
4. Wait one or two minutes and open `https://gameloves.github.io/mohammaddawoodsaddiqi/`.
5. In `index.html`, remove the `<!--` and `-->` around the `og:image` line (and change the address if
   you host elsewhere) so link previews in WhatsApp, Telegram and Facebook show the photo.
   Upload the changed file again.

Hesab-o-Ketab's privacy policy will then be at
`https://gameloves.github.io/mohammaddawoodsaddiqi/hesab-o-ketab/privacy-policy/`. Paste that address into
Google Play Console → **App content → Privacy policy**.

Other hosts (Netlify, Cloudflare Pages, any web hosting with a `public_html` folder) work the
same way: upload the folder contents to the web root.

## 3. Updating the live site

Edit the file (see `USER_GUIDE.md`), preview it locally, then upload the changed files to the same
repository. GitHub Pages republishes automatically within a few minutes.

## 4. Taking it offline

Repository **Settings → Pages → Unpublish site**, or delete the repository. Search engines and
link previews may keep a cached copy for a while.
