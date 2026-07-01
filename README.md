# andrewnelson.dev

Static landing page for `andrewnelson.dev` — a hub linking out to a small suite of
personal health/fitness tools. Single self-contained `index.html`, no build step.

## Links

| # | Tool | URL | Notes |
|---|------|-----|-------|
| 01 | Body Composition | https://bodycomp.andrewnelson.dev/ | private |
| 02 | Meal Plan | https://visceral-meal-plan.andrewnelson.dev/ | carb cycling |
| 03 | Workout Schedule | https://weekly-workout.andrewnelson.dev/ | full body, Mon/Wed/Fri |
| 04 | Momentum Log | https://momentum-log.andrewnelson.dev/ | daily tracking |

## Stack

- Plain HTML + CSS, no framework, no JS dependencies (one inline script sets the footer year).
- Fonts: IBM Plex Sans / IBM Plex Mono via Google Fonts.
- Hosted on Cloudflare Pages; subdomains protected via Cloudflare Access (email OTP) where marked private.

## Design system

Shared across all `*.andrewnelson.dev` tools:

- White background, IBM Plex Sans (body) + IBM Plex Mono (labels/data).
- Accent palette: red-orange `#e8552d`, gray `#6b7280`, blue `#2563eb`, teal `#0f766e`.
- Each tool keyed to its own accent on the left border.

## Deploy

```sh
wrangler pages deploy . --project-name=andrewnelson-dev
```

Or push to the connected branch and let Cloudflare Pages build on commit. No build
command needed — output directory is the repo root.

## Files

```
.
├── index.html   # the landing page
└── README.md
```
