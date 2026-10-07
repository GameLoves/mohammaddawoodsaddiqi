# User guide

## For visitors

* **Header**: the name (returns to the top), section links (About, Work, Systems, Contact) and the
  language switcher **English / دری / پښتو**. Dari and Pashto turn the whole page right to left.
* **Header extras**: the moon/sun button switches light and dark; the choice is remembered on that device.
* **Top of the page**: a terminal-style line cycling through the roles, the name, two buttons, and a strip of
  four numbers (11 years teaching English, 4+ institutes, 3+ systems, 3 app languages).
* **About**: the bio, a `profile.json` card with the same facts, and six areas of work.
* **Experience**: a timeline, newest first. Green dots are current roles; English teaching 2012–2023 lists
  AIL, AIELS, Barez and Tolo.
* **Systems**: Hesab-o-Ketab with features, a spec list, the tools it is built with and a link to its
  privacy policy; ZargarMan System, Naft System and other websites.
* **Contact**: the phone number with **Call**, **Message** and **Copy number**. After copying, the
  page says "Number copied"; if the browser refuses, it selects the number so it can be copied by hand.

Direct links by language: `/?lang=en`, `/?lang=fa`, `/?lang=ps` (or `#fa`, `#ps` at the end of the address).

## For the owner: editing the text

Open `index.html` in any text editor (Notepad++, VS Code).

* **English text** is written directly in the page, between tags such as
  `<p data-i18n="bio_intro">…</p>`.
* **Dari and Pashto** are in the script near the bottom, in `T.fa` and `T.ps`, under the same key
  (for example `bio_intro: "…"`). Change both languages when you change English.
* Keep product and company names in Latin letters and wrapped in `<bdi>…</bdi>` inside Dari and
  Pashto text; this keeps them in the right order in right-to-left lines.

### Adding descriptions for ZargarMan System and Naft System

Replace `<span data-i18n="soon">Description coming soon</span>` in that system's card with, for example,
`<span data-i18n="zargarman_sub">Your one-line English description</span>`, then add
`zargarman_sub: "…"` to both `T.fa` and `T.ps`.

### Adding a role to the timeline

Copy one `<li class="current">…</li>` block inside `<ol class="timeline">`, change the texts and give
each new `data-i18n` key a Dari and Pashto string in `T.fa` and `T.ps`. Remove `class="current"`
and put the years in `<span class="when">` for past roles.

### Changing the photo

Replace `assets/photo.jpg` (720 × 720) and `assets/photo-360.jpg` (360 × 360) with square JPEG
images of the same names. Remove location data from photos before uploading.

### Changing the phone number

Change it in three places in `index.html`: the visible number (`id="phone"`), the `tel:` and `sms:`
links, and `var number = "…"` in the copy-button script.

