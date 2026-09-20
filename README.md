# JJLEInnovations.github.io

The public website for JJLE Innovations, served by GitHub Pages at
<https://jjleinnovations.github.io>.

Apple requires a reachable **Privacy Policy URL** and **Support URL** for every
app on the App Store. Those pages live here.

## Layout

```
/                       Company landing page, lists the apps
/style.css              Shared stylesheet — every page links /style.css
/mail-assistant/        One folder per app
    index.html          Product page      → Marketing URL
    privacy.html        Privacy policy    → Privacy Policy URL  (required)
    support.html        Support page      → Support URL         (required)
```

## Adding another app

1. `mkdir <app-name>` and copy the three pages from `mail-assistant/` as a
   starting point.
2. Rewrite them for that app. **Do not copy the privacy policy without
   re-reading it** — it claims the app cannot reach the network, which is true
   of Mail Assistant because it ships with no network entitlement. If a future
   app does talk to a server, that wording is false and would contradict its
   App Store privacy label.
3. Add a card for it on the root `index.html`.
4. Commit and push. Pages redeploys in about a minute.

## Editing

Plain HTML and one stylesheet. No build step, no dependencies. Edit, commit,
push — the live site follows `main`.

URLs are absolute (`/style.css`, `/mail-assistant/privacy.html`) so a page
keeps working if it moves to a different depth.
