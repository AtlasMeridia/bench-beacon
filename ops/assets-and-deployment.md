---
last_updated: 2026-06-30
status: draft
visibility: public
---

# Assets And Deployment Custody

Bench & Beacon should use a simple split:

- GitHub holds public, reviewable source.
- Google Drive holds master assets and collaboration material.
- The VPS runs live services.
- Private ops decisions stay in `bench-beacon-ops`.

## Canonical Surfaces

| Surface | Role | What belongs there |
|---|---|---|
| `AtlasMeridia/bench-beacon` | Public session/archive source | Public session notes, reviewed public copy, and public-safe Markdown artifacts. |
| `AtlasMeridia/bench-beacon-site` | Public website source | Landing page source, optimized web images, SVG logo and favicon exports, and deploy config. |
| Bench & Beacon Google Drive | Asset masters | Recordings, raw audio/video, transcripts, working docs, deck masters, thumbnail masters, high-resolution brand exports. |
| `AtlasMeridia/bench-beacon-ops` | Private ops record | VPS notes, deployment decisions, service topology, non-secret pointers, runbooks. |
| `beacon-mind-01` VPS | Live services | `chat.benbe.org`, gated demos, Open WebUI/Hermes services, tunnels, service backups. |
| `~/Projects/bench-beacon/brand` | Active brand workspace | Design system, tokens, logos, marks, illustrations, mockups, and archived design imports. |

## Public GitHub Rule

Anything committed to either public Bench & Beacon repo should be publishable.

Allowed:

- reviewed Markdown;
- public landing-page source in `bench-beacon-site`;
- optimized web images;
- SVG logo and favicon exports;
- non-secret deployment config;
- public session artifacts after review.

Not allowed:

- raw transcripts;
- recordings;
- private attendee details;
- unreviewed live docs;
- credentials, tokens, keys, or `.env` files;
- internal VPS/debug notes.

## Google Drive Tree

The whole connected Drive is devoted to Bench & Beacon. For the current
landing-page work, use the top-level folder
[`Website - benbe.org`](https://drive.google.com/drive/folders/1yYQErxSi-GII4ybJ68ZVcMK7AjMW3499):

```text
Website - benbe.org/
  01 Copy drafts/
  02 Brand exports/
  03 Web-ready assets/
  04 Deployment handoff/
  99_Archive/
```

Drive is the source for heavy and collaborative material. GitHub receives only
small, web-ready exports copied from Drive or local source folders.

## Website Deployment

Use `benbe.org` as the primary public landing page.

Deploy from `AtlasMeridia/bench-beacon-site`, using the repo root as the Vercel
project root. Local checkout: `~/Projects/bench-beacon/site`. The vault bundle
does not carry a nested `site/` directory.

Recommended routing:

- `benbe.org` — public landing page and session archive.
- `www.benbe.org` — redirect to `benbe.org`.
- `chat.benbe.org` — gated BenBe portal on the VPS.
- `demo.benbe.org` — gated or temporary demo surface.
- `benbe.dev` — technical/developer namespace only.

## VPS Rule

The VPS is not the canonical asset library. It may keep service files, cache,
exports required by a running service, and backups needed for recovery. Canonical
media masters and collaborative files stay in Drive; public web exports stay in
GitHub.

## Brand Rule

Use `~/Projects/bench-beacon/brand` as the source of truth for Bench & Beacon
visual surfaces. Deploy repos may vendor
`brand/system/css/colors_and_type.css` as-is; this file is explicitly approved
to exceed the usual 300-line review threshold. Copy only reviewed exports from
`brand/assets/**/exports/` into public repos.

## Current Handoffs

- Keep Vercel project `bench-beacon` connected to `AtlasMeridia/bench-beacon-site`
  with root directory `.`.
- Keep brand source in `~/Projects/bench-beacon/brand`; commit only reviewed
  web-ready exports and vendored CSS to deploy repos.
