---
last_updated: 2026-05-07
status: reviewed
visibility: public
---

# Bench — AI stack onboarding (2026-05-06)

A 1:1 office-hours session with a guest new to AI tooling. Kenny gave a guided tour of his working setup — coding agents, Obsidian as a durable knowledge base, and GitHub-as-second-cloud — paired against two concrete project ideas the guest brought.

## Format note

Two MP4 files were recorded for this session: a 21-second mic-check clip ("Test, test, test"), and a ~68-minute main recording. The first ~36 minutes of the main recording contains no detectable speech. Real conversation begins around the 36:00 mark, which lines up with the first chat-sidebar URL drop. Effective session length: ~32 minutes.

Worth checking next time whether Meet's recording was capturing audio before the conversation actually started, or whether the audio stream lagged the recording start.

## Topics

### 1. AI coding stack — what to use, when

The guest had been trying to set up Cursor at work but is blocked on GitHub access (the company gates GitHub to engineering team members only). What they actually want is a local AI interface on their desktop — Claude Code-like, but able to switch between models — without enterprise wiring.

Discussed:

- **Codex (OpenAI)** as the more open option that can connect to any model backend, including local ones via Ollama. Native fit for someone with an OpenAI subscription who wants flexibility.
- **Cursor** still considered a contender despite Codex/Claude Code overlap — Kenny noted there is real money about to flow into it that should keep it on the radar. (See followup #1 for a fact-check item on this claim — the sourcing was verbal and uncertain.)
- **Claude Code + Claude subscriptions** for vault-driven and file-aware work.

Subscription value: the guest wants both a Claude and an OpenAI subscription so models can be picked per task. The $100 tiers were considered "decent value" for moderate use; $200 tiers seen as overkill at current usage levels.

Token-cost question raised but not resolved: the guest has a small project at work that has accumulated ~$21 / ~300k tokens. They don't yet have intuition for what token counts mean in dollar terms or in scope-of-work terms. Worth a future Bench session.

### 2. Obsidian as durable knowledge base

The core argument Kenny pitched: tools and models churn weekly; your vault is what compounds. Markdown is native to every LLM, so any model can read your notes — no lock-in.

Demoed:

- A personal vault (used for daily notes; AI is allowed to copy from it but not edit it — a deliberate "freeze the substrate, let the model derive" pattern).
- The Atlas Cortex vault, where multiple agents work alongside Kenny across departments (TREASURY, MEATSPACE, PRESENCE).
- The Bench-Beacon vault structure under PRESENCE — Wednesdays = practitioner office hours, Fridays = frontier/SOTA.
- Obsidian's graph view as a way to see relationships between notes.

Recommendation Kenny gave the guest: start with Cloud Code as a guide *into* Obsidian rather than figuring out Obsidian's UI cold. Obsidian is feature-rich and tedious to bootstrap manually; an agent can walk you through it.

Mobile question: Obsidian Sync (paid) vs iCloud sync (free, supported). No decision yet.

### 3. Project: receipt → pantry → recipes agent

The guest's first concrete project idea, surfaced during the session:

- Scan grocery receipts to populate a pantry inventory.
- Cross-reference pantry against a stored recipe library.
- Answer "what can I make in 30 minutes with what I have?"
- Over time, learn the user's preferences — favored cuisines, sources (which recipe sites they tend to like), seasoning style — and start synthesizing personalized recipes.

Kenny's framing: this is a strong jumping-off project to learn agents (vs. just chat) because it has a real loop — input → state update → query → output → preference learning — and the data accumulates into something durable.

A simpler v0 was discussed: just open Claude on phone, take pictures of fridge/pantry, pin the conversation, accumulate the corpus by hand for a month, then have the AI propose a structured program based on the accumulated history. Process before app.

Open question raised by Kenny: do you actually need a custom app, or is the *process* the asset? You can ship the process via mobile Claude/Codex without ever building an app. Building the app becomes optional, not foundational.

### 4. GitHub + Vercel as a second cloud

For the guest's second project idea — a personal job tracker / customized job board — Kenny showed:

- GitHub as the artifact/code home and the friend-sharing surface.
- Vercel for free hosting of the deployed app, with custom domain support.
- This stack collapses "where do my projects live?" and "where do friends look at them?" into one substrate.

Walked through connecting GitHub to Claude Code via the Connectors UI (Cmd+,) and authorizing the integration. Note: the connector authorization is per-AI — connecting GitHub in Claude Code doesn't propagate to Codex or other agents; each one needs its own authorization pass.

### 5. File organization with coding agents

A side observation from Kenny that's worth banking: he no longer manages file paths manually. He renames projects to memorable names, then asks Claude to "open file X" or "find file X" — and the agent handles the path resolution. The cognitive load of "where did I save that?" disappears once the agent is the file-system interface.

Caveat surfaced: AI tends to organize a computer "like a computer, not a human" — flat, mechanical hierarchies. Worth keeping a human-friendly folder structure on top of whatever the agent does, and pointing the agent at *specific* folders rather than letting it reorganize the whole machine.

### 6. Collaboration substrate question (open)

The guest asked how teams typically share information. Kenny's read: most companies use a fragmented mix — Slack for messaging, a wiki for documentation, a portal for everything else — and that's not going away.

For the two of them specifically, the question is whether to:

- Set up a shared Obsidian space (Kenny's default), or
- Use HackMD (the guest's instinct), or
- Just share via GitHub for project-specific work.

No decision made. See followup #5.

## Tools & references that came up

- Skirano tweet — https://x.com/skirano/status/2052112224538509349 (chat sidebar, ~36:13)
- Obsidian — https://obsidian.md/ (chat sidebar, ~40:28)
- HackMD — https://hackmd.io/ (chat sidebar, ~47:09)
- Karpathy tweet — https://x.com/karpathy/status/2039805659525644595 (chat sidebar, ~49:49). Mentioned in audio as the canonical "use Obsidian with your AI workflow" reference; the speaker's name was garbled in transcription as "Andre Carpoffi."
- AtlasMeridia/transcript-pipeline — https://github.com/AtlasMeridia/transcript-pipeline (chat sidebar, ~1:03:32). Kenny described it in audio as "something I built that I don't really use anymore."
- Codex (OpenAI) and Cursor — discussed by name; no specific URLs shared.
- Cloud Code Connectors UI — Cmd+, in Claude Code to add per-tool integrations like GitHub.

## Format / process observations for the seminar itself

- This was effectively a guided onboarding, not a topic-driven seminar. Worth tagging it as such — the format suits "first session with someone" but doesn't extrapolate to weekly Bench cadence.
- The guest raised an interesting framing question: should sessions be modeled as a startup standup, a venture firm partner meeting, or a podcast? No answer reached. Tabled.
- Kenny's working assumption stated aloud: meetings get recorded, AI-generated notes go into PRESENCE/Bench-Beacon/sessions/, attendees can review back later. This file is part of validating that loop.
