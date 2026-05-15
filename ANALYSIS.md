# reports — Technical Analysis

> Client campaign reports.

Generated 2026-05-15.

## Purpose

Public-facing repo that holds **standalone HTML campaign reports** for Prospect Engine clients. Each report is a single self-contained HTML file — likely served via GitHub Pages or shared directly as a link.

The repo is **public** (the only public repo in the `ProspectEngineAgentic` org), which makes sense for share-by-link delivery to clients.

## Contents

```
reports/
├── README.md                              # one-liner: "Client campaign reports"
└── algoritmica-campaign-report.html       # 31 KB report for Algoritmica
```

That's the whole repo (2 files).

## How it works

- Reports appear to be **hand-authored or generated HTML** — no build step, no static-site generator (no `package.json`, no `_config.yml`, no Jekyll/Hugo signals).
- Each report is independently shareable via raw GitHub URL or GitHub Pages.
- No template, no shared CSS file at the repo root — likely the HTML inlines its own styles.

## Possible improvements

- **Convention:** establish a filename pattern (`{client-slug}-{campaign-id}-report.html`) so new reports drop in cleanly.
- **Generation:** if reports are produced from Dewx metrics, a small script (in `penbrain` or `insidesales`) could template them rather than hand-authoring.
- **GitHub Pages:** enable Pages on the repo so URLs are `https://prospectengineagentic.github.io/reports/<file>.html` instead of raw blobs.
- **Index page:** add an `index.html` listing available reports — gated by client slug if any reports become sensitive.
- **Privacy:** the repo is public; confirm no client report contains data the client wouldn't want indexed.
