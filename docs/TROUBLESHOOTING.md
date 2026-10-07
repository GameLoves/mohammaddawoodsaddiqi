# Troubleshooting

All entries below are anticipated problems; none has been reported yet.

| Symptom | Likely cause | Check | Fix | Confirm |
|---|---|---|---|---|
| GitHub address shows "404 There isn't a GitHub Pages site here" | Pages not switched on, or wrong repository name | Settings → Pages shows a "Your site is live" line | Choose branch `main`, folder `/ (root)`, Save; repository must be named `dawoodsaddiqi1998.github.io` | Address opens after 1-2 minutes |
| Page opens without the photo | `assets` folder not uploaded, or uploaded inside another folder | Open `…/assets/photo.jpg` directly | Upload `assets` at the top level, next to `index.html` | Photo appears after a refresh |
| Privacy policy link missing or 404 | `hesab-o-ketab/privacy-policy/index.html` not uploaded, or link still hidden | Open `…/hesab-o-ketab/privacy-policy/` | Upload the folder; in `index.html` remove `hidden` from `<div class="links" id="mm-links" hidden>` | Link shows under Hesab-o-Ketab and opens the policy |
| Fonts look plain | Google Fonts blocked or offline | Browser developer tools → Network shows fonts.googleapis.com failing | Nothing needed; system fonts are the designed fallback | Text still readable in all three languages |
| Language does not stay chosen after reload | Browser blocks local storage (private mode, or file opened by double-click) | Try via `http://localhost:8000` | Use the local server, or link with `?lang=fa` / `?lang=ps` | Reload keeps the language |
| "Call" or "Message" does nothing | Computer has no phone app | Try on a phone | Use **Copy number** | Number pasted elsewhere |
| `python3: command not found` (Windows) | Python launcher is `py` | `py --version` | Run `py -m http.server 8000` | "Serving HTTP" message |
| `OSError: [Errno 98] Address already in use` | Port 8000 busy | Run with another port | `python3 -m http.server 8080`, open `http://localhost:8080/` | Page opens |
| Link preview in WhatsApp has no photo | `og:image` line still commented out | Search `index.html` for `og:image` | Uncomment it, set the real site address, re-upload | New shares show the photo (old shares may stay cached) |

Diagnostics: the site has no server logs of its own. In a browser, press F12 → **Console** to see
script errors. GitHub shows deployment status under the repository's **Actions** tab.
