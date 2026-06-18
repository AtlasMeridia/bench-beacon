---
last_updated: 2026-06-10
status: draft
visibility: review-required
session_type: Bench (Wednesday, hands-on / office hours)
source_artifacts:
  - Google Meet recording, 2026-06-10 15:47 GMT-7
  - Google Meet chat export, 2026-06-10 15:47 GMT-7
  - Local Whisper transcript (mlx_whisper large-v3) under `_dev/transcripts/2026-06-10_local-llm-and-consulting-pivot/`
source_limitations:
  - Transcript has no reliable speaker attribution; speaker assignment is inferred.
  - Contains real first names (attendee, plus third parties) and a real business/LLC name. Generalize or clear before any public version.
  - Whisper mangled some product/model names (e.g. "Qwen 3", "Pymono", "OpenClaw", "Hermes", "Odysseus"); corrected here on best effort.
---

# Bench — Local LLM workstation and the consulting pivot (2026-06-10)

The first Wednesday Bench session under the new twice-weekly cadence: a one-on-one with a returning attendee who has finished building a local AI workstation and is now looking for something to point it at. The conversation moved from local-model tinkering (a self-hosted multi-user chat room, model personality, harness choice) toward a sharper question — pick one project, attach a real incentive to shipping it, and treat AI consulting as the lowest-friction way to start making money.

## What Happened

The attendee opened with a working artifact: a self-hosted chat room he built in an evening — an HTML front end wired to a Node.js service and some Python, running a local Qwen 3 MoE model, usable by multiple people on his local network. He had dropped Docker once he found a lighter path and was working out how to let others in (Tailscale, or a host that simulates the local network). His main complaint was instructive: the model's default persona is an over-enthusiastic, emoji-heavy chatbot, and he assumed changing it meant training his own model. That opened a useful correction — persona is a system-prompt concern, not a fine-tuning one.

From there: harness choices (a batteries-included agent framework vs. a bare-bones one), the Claude `/insights` command and self-improving loops, and a long stretch on direction. The attendee has roughly nine projects in flight and no single commitment, and Kenny kept pushing toward one focal project plus an accountability mechanism. The back half converged on AI consulting as the concrete near-term move: use an existing LLC, a scheduling page, and a single paying customer as the first real test.

## Attendee Context

- Consolidated older gaming machines into one local workstation; selling the spare gaming PC and laptop to roughly break even on the build.
- Running a local Qwen 3 MoE model — fast and more than capable for chat/Q&A, but weak at coding. He estimates his ~70B-class local setup at "about 1% of Claude Code" for actual coding work.
- Comfortable building (vibe-coded the chat room in about an hour) but explicitly more collaborative and social about it — he likes talking projects through with people, which is part of why the sessions help.
- Just finished school; planning a week off before the next push.
- Runs an existing automotive small business (an LLC), which becomes the ready-made vehicle for consulting income.
- Already publishing: two posts into a blog tied to an accountability bet, on a twice-weekly cadence.

## Recommendations and Demonstrations

### 1. Persona is a prompt, not a retrain
The attendee believed the emoji-happy personality was baked into the model file and would require training his own model. The correction: for most local runners there is a system prompt you can set once to define tone and persona, persistently, without touching weights. Fine-tuning is a real tool but the wrong one for "make it stop using emojis."

### 2. Tinkering teaches, but name the tradeoff
Much of what the attendee is building already exists off the shelf. Kenny named the tradeoff: using existing tools is faster when the goal is the outcome; building it yourself is slower but teaches how the stack actually works. Both are valid — but be deliberate about which mode a given project is in, rather than defaulting to "build it myself" by reflex.

### 3. Harness choice: batteries-included vs. bare chassis
On agent frameworks, Kenny framed it as a packaged, skills-included harness (Hermes — "an SUV with all the trim," ~100 skills out of the box) versus a stripped framework you have to know what to do with (a "naked chassis"). For someone still discovering what he wants, batteries-included lowers the activation cost; market share is also a reason to learn the more widely used one, for landscape literacy. For real coding work, the frontier hosted agents (Codex, Claude) remain the practical choice — local/experimental harnesses are learning tools, not production.

### 4. Pick one thing and attach an incentive
The recurring tension: nine projects, no commitment, and energy that goes "anti" whenever pushed to commit. Kenny's proposal was a standing homework structure — by each Friday or Wednesday, name one focal project the conversation returns to, even if everything else stays free-flowing. The deeper point was incentives: social shame isn't enough to force shipping; you need a real incentive or disincentive (Kenny's own example: a public bet to give away $5,000 if he doesn't post for three years). Things get built shockingly fast once committed — the chat room took an evening — so the bottleneck is choosing, not building.

### 5. Treat AI consulting as the near-term business
The clearest convergence of the session. Rather than picking the "right" AI business in the abstract, start consulting now: it's almost free to stand up, recession-resilient, and forces real reps. Scaffolding discussed:
- Use the existing LLC rather than forming a new entity; a DBA can rebrand it later if desired, but that's busywork — get one payment first.
- A scheduling page (cal.com) is already set up: strangers book a free discovery call, you invoice afterward. No third-party marketplace needed.
- Don't sell "AI" or "automation" — nobody buys that. Sell hours saved or dollars added: have a conversation, learn how they work, quantify the value.
- Run a free practice engagement with a friendly first contact end-to-end (website → booking → 30-min call → shared spreadsheet → follow-up email → plan) before taking a stranger.
- Spreadsheet automation is an unglamorous but real wedge — even teaching someone to use Copilot in Excel is billable.
- Target a vertical the attendee already knows: automotive. The local shop with dozens of idle cars in the lot is the archetypal customer — frame it as turning stranded inventory into throughput.

### 6. The big models are "good enough" — stop over-tooling for business
Kenny described his own graduation from constant new-tool experimentation to a stable daily driver: Codex for file/operational work, Claude as a thinking partner. The unsexy truth is that for getting business done, the frontier model is good enough and most extra tooling is optional. Cost backdrop worth flagging: Fable launched ~a day earlier and is materially more expensive than Opus; team token limits exist and are easy to blow through (the attendee burned ~500k tokens in a day by accident).

## Tools and References

Shared in chat:
- Viral build example — https://x.com/the2ndfloorguy/status/2064704204166635930 (hooked a Whoop to a work calendar to find which coworker causes the most stress)
- Kenny's second blog post — https://www.kennyliu.io/notes/i-havent-blown-it-yet
- Ship 30 for 30 (writing cadence) — https://www.ship30for30.com/
- Kenny's scheduling page — https://cal.com/kennyliu

Discussed:
- Local self-hosted multi-user LLM chat room (HTML + Node.js + Python; dropped Docker)
- Qwen 3 MoE local model; system-prompt persona vs. fine-tuning
- Hermes vs. a bare-bones harness; Hermes market share vs. OpenClaw
- Claude `/insights` and self-improving loops (promote repeated fixes into markdown/skill files)
- Codex as daily driver, Claude as co-thinking brain
- cal.com scheduling; DBA vs. LLC; payment processor / Stripe
- Local model as a sub-agent under a hosted orchestrator (open question)
- "Hive network" — multiple people and multiple machines into one shared AI session
- Driving a local model inside VS Code for multi-step coding (kept getting stuck)
- Fable vs. Opus pricing; team-based token limits

## Open Questions

- What is the one focal project, and what incentive/disincentive enforces shipping it?
- Consulting vs. building: does the attendee point mental energy at making money (consulting) or at open-model tinkering? They compete for attention.
- Can the local Qwen model be driven reliably inside VS Code for multi-step coding without stalling — and can an agent auto-recover it when it does?
- Can the local model serve as a sub-agent under Codex/Claude rather than trying to do everything itself?
- What's the right monthly spend for the weekly sessions and any always-on agent (a non-zero number to be set)?
- First content direction: LinkedIn (professional brand) or YouTube (the build visuals)? The AI keeps splitting the two.
- Who is the first paying consulting customer, and what's the offer — spreadsheet automation, automotive-shop throughput, or something else?

## Format Notes

This was the first one-on-one Wednesday Bench under the new cadence, and it worked better than the multi-person format: with one person you can get into their specific situation (here, the move from tinkering to a business). A recurring theme — echoed from prior sessions — is that attendees are "plenty smart" but jagged in where they are with AI, so one-on-one or tightly structured time produces more than open group brainstorming. The session also surfaced a format idea worth keeping: a standing "one focal project" the conversation returns to each week, with Friday for landscape/news and Wednesday for hands-on tool usage.
