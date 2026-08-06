# Micro Filer — Dormant & Micro Company Accounts / Tax Return

Static landing pages for Micro Filer, deployed on Vercel. No build step, no
dependencies — plain HTML with inline CSS.

## Layout

```
public/                                     # ← Vercel output directory (the only deployed folder)
  index.html                                # staging index, links to both pages
  dormant-company-accounts-tax-return.html  # → /dormant-company-accounts-tax-return
  micro-company-accounts-tax-return.html    # → /micro-company-accounts-tax-return
  robots.txt
clients/microfiler/docs/                    # internal working docs — NOT deployed
  source-verification.md
  diagnostic.md
vercel.json
```

Anything outside `public/` is never served. That is deliberate: the
verification and diagnostic notes stay in the repo but off the public web.

## Routes

`cleanUrls: true` strips the `.html`, so the deployed paths match the
`rel=canonical` and the in-page internal links exactly:

| Path | File |
| --- | --- |
| `/` | `public/index.html` |
| `/dormant-company-accounts-tax-return` | `public/dormant-company-accounts-tax-return.html` |
| `/micro-company-accounts-tax-return` | `public/micro-company-accounts-tax-return.html` |

`trailingSlash: false` keeps a single canonical form of each URL — requests
with a trailing slash 308 to the version without.

**If you rename a file in `public/`, the public URL changes with it.** The
filenames are the routes.

## Deploying

Zero-config. Import the repo at [vercel.com/new](https://vercel.com/new) and
deploy — framework preset "Other", no build command, output directory `public`
(already declared in `vercel.json`).

Or from the CLI:

```bash
npx vercel        # preview deployment
npx vercel --prod # production
```

## Before pointing a production domain here

This deployment is currently **noindex**, because the pages declare
`rel=canonical` to `https://www.microfiler.co.uk/...` and a crawlable staging
copy on `*.vercel.app` would be a duplicate. Two things to undo when this
project becomes the real host of those URLs:

1. Delete `public/robots.txt` (or replace the `Disallow: /`).
2. Remove the `X-Robots-Tag: noindex, nofollow` header from `vercel.json`.

Miss either one and the live site will not be indexed.

## Local preview

```bash
npx serve public          # http://localhost:3000
# or
python3 -m http.server -d public 8000
```

Note that neither strips `.html` the way Vercel does, so the clean internal
links (`/dormant-company-accounts-tax-return`) 404 locally. `npx vercel dev`
reproduces the real routing.

## External dependencies

The pages load two things from third-party origins at runtime:

- Google Fonts (Montserrat, Roboto)
- The Micro Filer logo, hosted on `lirp.cdn-website.com`

Both are remote, so they are subject to that host's availability. Worth
self-hosting into `public/` if these pages become the production site.
