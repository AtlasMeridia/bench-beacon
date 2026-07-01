---
last_updated: 2026-06-30
---
# Brand Assets

Bench & Beacon brand assets now live in the local brand workspace:

`/Users/atlas/Projects/bench-beacon/brand`

Treat `brand/system/` and `brand/assets/` as active source. Treat
`brand/archive/` as provenance only unless a file is deliberately promoted.

## Active Exports

- Wordmark: `~/Projects/bench-beacon/brand/assets/logos/exports/logo-wordmark.svg`
- Monogram: `~/Projects/bench-beacon/brand/assets/logos/exports/logo-monogram.svg`
- Seal / telescope-wrench mark:
  `~/Projects/bench-beacon/brand/assets/marks/exports/seal-telescope-wrench.png`
- Standalone telescope-wrench mark:
  `~/Projects/bench-beacon/brand/assets/marks/exports/telescope-wrench-logo.png`

## Active Design System

- CSS tokens/type/modes:
  `~/Projects/bench-beacon/brand/system/css/colors_and_type.css`
- Web UI kit: `~/Projects/bench-beacon/brand/system/ui-kits/web/`
- App UI kit: `~/Projects/bench-beacon/brand/system/ui-kits/app/`
- Templates: `~/Projects/bench-beacon/brand/system/templates/`

## Use Rule

Deploy repos may vendor the active CSS file as-is and copy reviewed exports.
Do not build production surfaces from archived bundle files or the older
`/Users/atlas/AudioVisual/Branding/Bench-And-Beacon/` cache.
