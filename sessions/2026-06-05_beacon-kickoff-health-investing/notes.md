---
last_updated: 2026-06-10
status: draft
visibility: review-required
session_type: Beacon (Friday, seminar / landscape)
source_artifacts:
  - Google Meet recording, 2026-06-05 13:55 GMT-7
  - Google Meet chat export, 2026-06-05 13:55 GMT-7
  - iPhone screen-recording of the pre-meeting Meet room `mgt-chyr-nns` (~51 min, ~1:05–1:56 PM; silent, Meet live-captions only)
  - iPhone screen-recording of the main meeting `rnx-opxs-bvg` (~20 min; silent, redundant with the desktop recording)
  - Local Whisper transcripts (mlx_whisper large-v3) under `_dev/transcripts/2026-06-05_beacon-kickoff-health-investing/`
source_limitations:
  - Transcript has no reliable speaker attribution; speaker assignment is inferred from context.
  - Contains real first names of multiple attendees and third parties, plus a venue/event detail. Generalize or clear before any public version.
  - Whisper mangled some product/model names (e.g. "Hermes", "OpenClaw", "Misty Studios", "retatrutide", "Mythos"); corrected here on best effort.
  - The two "ScreenRecording" files are silent iPhone captures of the Meet (no usable audio); only Google Meet's burned-in live captions are readable. The pre-meeting room (`mgt-chyr-nns`) is summarized below from sampled captions (partial, ASR-error-prone, NOT verbatim); the during-meeting capture is redundant with the desktop recording. Provenance: `_dev/transcripts/.../screen-captures-note.md`.
  - On-screen labels exposed attendee full names and an email address (see followups → Review Before Publication).
---

# Beacon — Group kickoff, the agent landscape, and a health/investing 1:1 (2026-06-05)

The first formal Friday Beacon under the new twice-weekly cadence. It opened as a small group setting up how the meetings will run, moved through show-and-tell and the experimental-agent landscape, then narrowed — after most attendees left — into a substantive one-on-one on using AI for health and for investing. The through-line: explore broadly in the group, but the real value lands when one person's specific situation gets worked through in depth.

## What Happened

The group spent the first stretch defining format rather than content — half-jokingly drafting a session template (a few minutes of small talk, a news segment, a ~20-minute show-and-tell, then open brainstorming). The stated operating principle: "we don't do surveys, we only do people talking." A goals round-robin surfaced a wide spread of intent — from a blunt "make $10M, early exit" to "use AI to execute a cool business idea that makes money" — which Kenny compressed into "cool people doing cool things with AI."

Show-and-tell produced the session's best concrete artifact (see Recommendations #1). The group then riffed on several project ideas, talked through the experimental-agent landscape (Hermes / OpenClaw vs. the frontier hosted agents), and sketched a safer way to stand up a shared collaborative agent. As people peeled off for other commitments, the session became a one-on-one with a health-industry attendee, and the back half went deep on two threads he actually cares about: AI for personal health optimization, and AI for investing.

## Attendee Context

The group is mixed and "jagged" in AI experience — some are building, some barely use it. Notable in this session:

- A builder attendee (returning regular) who is standing up a self-hosted, multi-user LLM chat room on a new local workstation and wants a "hive network" pooling everyone's hardware; he showed a Warp setup the prior week.
- A health-industry attendee ("AJ" in the raw transcript) who became the 1:1 partner — background in biomechanics / human performance engineering, more systems engineer than software engineer. He can edit, debug, and triage code with AI but doesn't build from scratch yet. Uses Perplexity Pro (a free year) personally and GitHub Copilot at work (mandated), recently wiring Copilot to the work codebase for log parsing and bug triage. He noted human-written codebases are harder for AI to reason about than AI-native ones.
- Others attended briefly and left early (one for a birthday gathering the next day).

(All attendee names, the venue/event, and other identifying details must be generalized or cleared before any public version.)

## Recommendations and Demonstrations

### 1. AI as a physics/math solver, not just a chatbot (show-and-tell)
An attendee had a magnetics design question — how to maximize a magnetic coil's field as a function of coil size versus proximity to surrounding metal — that a human engineer kept answering in circles. He handed it to AI, which pulled the relevant magnetics equations and produced a 2D interpolation heat map showing the optimal trade-off point. The takeaway Kenny drew out: AI did real physics and math here, not retrieval, and the obvious extension is turning niche, obscure engineering computations into simple web tools ("how to size your coil"). This is a cleaner example than most of AI doing genuine technical work.

### 2. Experimental agents are learning tools; build the business on frontier agents
On the agent landscape, Kenny separated two layers. Experimental harnesses (Hermes, OpenClaw) are the "hot thing" — Hermes a bit more stable than OpenClaw, both doing impressive out-of-the-box things (email, image/video, acting like their own operator) but still "toys": they break, need resets, and aren't production-ready. They are excellent for *seeing what an agent can do* beyond being smart. For anything meaningful — a business, a consultancy, a real workflow — go through Codex or Claude as the agent. The frame: "the practical stuff is OpenAI/Anthropic; the exploratory stuff is whatever you want it to be."

### 3. Stand up a shared test box before exposing a personal machine
The builder wanted to host the collaborative agent on his own workstation (to use his local LLM) and add everyone via Tailscale. Kenny's safer sequencing: spin up a separate test box / VPS first, prove the collaborative pattern there, then bridge to the local machine — rather than opening a personal network to the group on day one. Keeps the local-LLM experiment alive without exposing the home network as the first move.

### 4. For the health attendee: start cheap, connect what you already have
The attendee wants to load Withings sleep/weight data and find trends, but needs richer vitals (blood tests, biomarkers, possibly DNA) to get past generic "eat healthy, reduce carbs" advice. He's also wary of DNA sequencing tied to his identity and is hunting for anonymized DNA labs. Kenny's practical path: before paying for Function Health or a genome test, get Claude ($20) and use the iPhone Apple Health connector to analyze the metrics already on his phone — see how far that goes first. Test whether Perplexity Pro is already "enough" before stacking another subscription.

### 5. Kenny's health-max project as a template
Kenny shared his own parallel project: biomarkers drawn via Function Health, with a plan to feed biomarkers plus food intake to Claude/Codex, follow the regimen it suggests (a personal, Brian-Johnson-style health-max), and record the whole loop. He framed it as a content-producing, self-improving, deliberately AI-dependent project — a repeatable shape, not a one-off. Adjacent topics: photographing yourself for lifestyle/health suggestions from image models; GLP-1 / peptide developments (a three-pathway compound, "retatrutide," expected later this year) and sites selling pre-release peptides. (Peptide-sourcing references should stay out of any public artifact.)

### 6. Investing is the other real use case — and the IPOs are the story
The longest 1:1 thread. Kenny's argument: the most consequential market event of the coming year is the wave of IPOs — SpaceX, Anthropic, OpenAI — and it connects to the national debt and to how the AI labs are funded. He used the SpaceX index-fund inclusion controversy (flipping from auto-included to excluded) as a live example of why following lab/company financing matters for an investor, not just a builder. Practical notes that came up:
- Don't pre-pay an annual subscription for any frontier model — rotate (see #7).
- Options: the attendee is just starting; a friend runs covered calls daily for low-risk side income. Robinhood has gamified options; Interactive Brokers exposes an API for robo-trading. The durable edge is in longer-term bets, not minute-to-minute trading.
- Tools like Unusual Whales (mirroring politicians' and big investors' trades) exist but mostly serve lagging info.
- Idea: a small investment club — put real money up, assign an agent to track it across the year, learn by watching it move. "Putting money on stuff makes it more live."

### 7. Don't stay married to one frontier model
Kenny's landscape lesson, told as recent history: Anthropic throttled Claude (even $20 users) around February when it ran out of compute/infrastructure funding, while OpenAI — earlier mocked for raising ~$100B — had the infrastructure to hand out free tokens; the effect of those funding decisions shows up on a lag of months. Anthropic later partnered with XAI/Elon's infrastructure to catch back up. He also read Anthropic's unreleased "Mythos" as a compute-distribution/funding problem rather than a safety hold. The practical conclusion: rotate frontier models, and don't lock into one. (Treat the specific funding/throttling claims as Kenny's read of the news, not verified fact, before publishing.)

## Tools and References

Shared in chat:
- Kenny's accountability-bet post — https://www.kennyliu.io/notes/three-year-publishing-bet
- CleanShot image (Beacon signpost)

Discussed:
- Warp (terminal/IDE); Claude in the terminal; Codex; Grok; Gemini
- Hermes, OpenClaw (experimental agents); Codex / Claude as the practical agents
- Misty Studios (shared project/workspace collaboration); Tailscale (network access)
- Perplexity (Pro); GitHub Copilot (work-mandated)
- Function Health (biomarkers); Withings (sleep/weight); Apple Health → Claude connector (iPhone)
- Unusual Whales; Interactive Brokers (API trading); Robinhood (options)
- Basecamp (Beacon's attendee-facing followup surface)
- Recurring riffs: "hive network" (multi-person, multi-machine shared session); AI dog trainer (detect pre-reaction, dispense a treat — "put a Ring on the dog and track the data"); niche-physics → web-app tools; AI cuisine / a recipe model that fuses traditions

## Open Questions

- What is each attendee actually here for? Intent ranges from a $10M exit to "cool things with AI" to specific health/investing use — the group needs a way to surface and respect that spread.
- For the health attendee: connect existing Apple Health / Withings data first, or invest in biomarkers/DNA up front? And how to get DNA analysis without identity exposure?
- Is there a sellable artifact in any of these threads (a coil-sizing tool, an AI cookbook), or is everyone just generating what they need on demand?
- Investment club: real money with an agent tracking it, or keep it as discussion? Who's in, and what's the mandate?
- How should the group host a shared collaborative agent safely — test box/VPS first, then bridge to a local LLM?
- Which frontier subscription is the right first paid step for a near-beginner — Claude $20, or is Perplexity Pro already enough?

## Format Notes

This session confirmed something about the format: the open group is good for show-and-tell and idea generation, but it's hard to "conduct" with several people of very different levels and intents — people drift in and out, and energy dips when nothing specific is happening. The depth came after the group thinned and it became one-on-one, where the attendee's actual situation (health, investing) could be worked through. That argues for the intended split — Friday Beacon for landscape/news and group show-and-tell, with deliberate one-on-one or tightly structured time for where the real value lands. Basecamp is the place the cleaned notes, news items, and agendas should land for attendees.

## Pre-meeting (phone-captured): a Bench-style 1:1 before the group call

_Source: the `mgt-chyr-nns` Meet room, ~1:05–1:56 PM, captured only on Kenny's phone (silent; reconstructed from burned-in captions — partial and low-confidence). Kenny and Justin talked one-on-one, with the health attendee joining late, before the group call moved to desktop (`rnx-opxs-bvg`) at ~1:55 PM. The two screen recordings folded into this session are this phone capture._

The pre-call conversation previewed several threads that recur in the following Wednesday's Bench session:

- **Model rotation.** Kenny described switching between frontier models and open/local models depending on the task — the same "don't marry one model" point he later made to the group.
- **Edge / local-AI product idea.** The builder floated that a ~2 GB model is small enough to run locally on a laptop and could power a "smart kitchen device" — an appliance running an offline model. (Connects to his local-LLM workstation work.)
- **Claude versions.** Some back-and-forth on which model versions to use.
- **An automotive roadside angle.** He mentioned a partner ("Honk"), a tow-truck/roadside service — early context for the automotive-consulting direction that becomes central later.
- **The accountability bet.** Kenny referenced being "out $5,000 — it's that in stone," tying his public publishing bet to actually showing up for these meetings (the `three-year-publishing-bet` link he dropped in chat).

_The second screen recording (~20 min) is a phone view of the main `rnx-opxs-bvg` meeting and is redundant with the desktop recording (biotech news, sharing Basecamp links, collecting emails). Both screen recordings are silent — only Google Meet captions are readable. Full provenance + caption fragments: `_dev/transcripts/2026-06-05_beacon-kickoff-health-investing/screen-captures-note.md`._
