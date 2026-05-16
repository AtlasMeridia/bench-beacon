---
last_updated: 2026-05-13
status: draft
visibility: review-required
source_artifacts:
  - Google Meet recording, 2026-05-13 14:52 GMT-7
  - Google Meet chat export, 2026-05-13 14:52 GMT-7
  - Local Whisper transcript generated 2026-05-14 under `_dev/transcripts/2026-05-13_hermes-x402-zec-assets/`
source_limitations:
  - Transcript has no reliable speaker attribution.
  - Public review should check attendee identity, work examples, and company references before publication.
---

# Local LLM agent workstation

## What happened

This session picked up after the attendee had started experimenting heavily with local LLMs, Ollama, MSTY Studio, Claude in the terminal, and local hardware. They had also begun building practical projects: a family tree site inspired by Kenny's family vault pattern, local model benchmarks, and a work form built through Claude Terminal and deployed through Google Apps Script / embedded web tooling.

The core theme was moving from "many AI apps" toward a clearer working environment. Kenny framed agents as partly a way of thinking rather than only a product interface, and suggested reducing context switching by working through a proper IDE with an integrated terminal.

The attendee had tested local models by asking each model to produce comparable output and watching speed metrics such as tokens per second and first-token latency. They were also building a low-power AI workstation using NVIDIA A2000 GPUs, with the idea that slower local jobs can run overnight if the power cost stays low.

## Recommendations and demonstrations

- Keep testing local models, but expect the best local model choice to change every few weeks.
- Look beyond the default Ollama catalog; use AI search to identify strong local coding models.
- Try Zed or VS Code as the central IDE, especially if the goal is one place for Claude Code, local Ollama models, files, and terminal work.
- Treat Cursor as part of the VS Code family of interfaces; choose based on workflow fit, not hype.
- Explore Hermes / OpenHands-style agent projects to catch up on current agent patterns.
- Watch x402 and wallet/payment protocols as a possible future substrate for online agent actions.

## Tools and references

- Ollama
- MSTY Studio
- Claude Terminal / Claude Code
- VS Code
- Zed
- Nous Hermes agent: https://github.com/nousresearch/hermes-agent
- Hermes agent demo/site: https://hermes-agent.nousresearch.com/
- x402 open payment protocol
- ZEC / privacy cryptocurrency
- Work application page shared in chat — link omitted pending review

## Open questions

- Which IDE should become the attendee's default workspace for local models plus Claude Code?
- Which local model is best for code generation on the current hardware?
- Whether the A2000 workstation path is "good enough" for overnight agent work before investing in larger hardware.
- What communication surface should Bench & Beacon use for repeat attendees: Slack, Discord, Telegram, or something simpler.

## Format notes

This session shows the value of repeat sessions. The attendee arrived with real experiments, hardware decisions, working code, and sharper questions. The next session should assume momentum rather than restart onboarding.
