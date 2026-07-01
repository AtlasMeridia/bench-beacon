---
last_updated: 2026-07-01
---
# Bench & Beacon

Bench & Beacon is a weekly seminar pairing under the Atlas Meridia umbrella.
It lives under `VENTURE/business-dev/` as a subordinate practice and audience
surface for practical business-development work.

- **Bench** — Wednesday 3pm–5pm. Office Hours format: practitioner, hands-on, workflow-level.
- **Beacon** — Friday 1pm–3pm. Seminar format: frontier developments, new tools, and SOTA filtered through practical value.

## Status

Pre-launch, but maturing from a session/workspace experiment into a named web surface. Kenny purchased `benbe.org` and `benbe.dev` through Cloudflare on 2026-06-19. Primary public namespace: `benbe.org`; secondary technical/developer namespace: `benbe.dev`. The project still uses a reduced operating spine until the weekly loop proves what else it needs.

## What this repository contains

This repository is the cleaned, publishable knowledge base for Bench & Beacon.

Live collaboration can happen in Google Docs, HackMD, or Google Meet during sessions. Durable artifacts return here after review.

## Structure

- `sessions/` — per-session artifacts for Bench and Beacon.
- `ops/` — reusable operational language and standards.
- `ops/assets-and-deployment.md` — custody map for GitHub, Drive, VPS, and web deployment.
- `offer/` — offer-shaping docs: the offerings note and the BenBe public-agent spec.
- `brand-design/` — public-safe pointers to the active local brand workspace.

Deployable website/app code lives outside this vault bundle:

- public site: `~/Projects/bench-beacon/site` (`AtlasMeridia/bench-beacon-site`)
- private evaluator app: `~/Projects/bench-beacon/eval`
- brand source: `~/Projects/bench-beacon/brand`

## Session loop

prep → live working doc → AI notes → followups → next session

Raw recordings, raw transcripts, private planning, and internal development notes are intentionally excluded from the publishable repository.

## Web namespace

- `benbe.org` — recommended primary public home for Bench & Beacon under the Atlas Meridia umbrella.
- `benbe.dev` — reserve for developer/technical surfaces: API docs, agent demos, build notes, experiments, or redirects.
- BenBe agent portal — recommended as gated `chat.benbe.org` for human-facing access; current implementation notes are private in `_dev/decisions/2026-06-19_benbe-org-and-agent-portal.md`.

## Brand system

Use the active local brand workspace before creating Bench & Beacon visual
surfaces:

`~/Projects/bench-beacon/brand`

The current source of truth is `brand/system/css/colors_and_type.css` plus
reviewed exports under `brand/assets/**/exports/`. Public landing/reading
surfaces use the light cream-paper default; product/agent tools use `workbench`.

## Deferred on purpose

No attendee roster, polished public portal, GitBook, or open anonymous agent yet. Those get added only when the operating loop proves they are needed. A private/gated BenBe Hermes/Open WebUI surface is allowed as a demo/operator surface before a full public portal.
