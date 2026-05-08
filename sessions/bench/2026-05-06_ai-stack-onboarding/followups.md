---
last_updated: 2026-05-07
status: reviewed
visibility: public
---

# Followups — Bench AI stack onboarding (2026-05-06)

## Action items

### Guest

- [ ] Download Obsidian and set up a personal vault. Use Claude Code to walk through the setup rather than the GUI cold.
- [ ] Create an OpenAI account if not already; install Codex and try connecting it to a model backend (Ollama / local first if curious about local LLMs).
- [ ] Connect GitHub to Claude Code (Cmd+, → Connectors → authorize). Repeat the same authorization separately for any other AI agent used (Codex, etc.) — connections do not propagate.
- [ ] Map out the receipt → pantry → recipes agent before next session. Specifically: what's the minimum-viable process (mobile-only, no app), and what triggers the upgrade to a real app?
- [ ] Sketch the job tracker / customized job board project. Decide whether v0 is a static HTML/Vercel page, a scraper-driven board, or just a Notion/Obsidian list.
- [ ] Add Kenny on GitHub.

### Kenny

- [ ] Send the guest the link to this session folder once notes are reviewed.
- [ ] Decide on collaborative substrate (see open question #5) and propose to the guest.

## Open questions

1. **Cursor's near-future trajectory.** Claim made in the session that "money is being dumped into Cursor" was sourced verbally and may have been confused with a different acquisition. Worth a fact-check before treating it as a load-bearing input for the guest's tool selection. As of session date the canonical Cursor story is its standalone trajectory + frontier-model push; specifics should be verified rather than recalled.
2. **Token-cost intuition.** The guest has spent ~$21 / ~300k tokens on a small work project and doesn't yet have intuition for what those numbers mean in scope-of-work terms. Candidate topic for a future Bench session — possibly a quick "cost-per-task" calibration exercise.
3. **Process vs. app for the recipe agent.** Open framing: can the entire value of the recipe project be captured in a process (mobile photos + pinned Claude conversations + monthly synthesis pass) without ever building an app? Resolve before next session.
4. **Mobile Obsidian — Sync vs. iCloud.** Both work. The guest hasn't picked yet. Default recommendation if no strong preference: iCloud (free, already configured for most macOS users).
5. **Collaboration substrate between Kenny and the guest.** Three options on the table:
   - Shared Obsidian space (Kenny's default).
   - HackMD (the guest's instinct).
   - Per-project GitHub repos (decoupled, less central).
   No decision.
6. **Seminar format identity.** The guest asked whether to model sessions after a startup standup, a venture-firm partner meeting, or a podcast. Tabled. Worth revisiting once Bench has 3–4 sessions of data on what's actually valuable.

## Process notes for the Bench loop itself

- **Recording quality.** First 36 minutes of main recording captured no speech. Cause unclear — could be Meet starting recording before audio capture was hot, or the conversation genuinely starting that late. Mitigation for next session: confirm both attendees are audible in the first minute, and consider trimming the recording on stop rather than relying on Whisper to skip silence.
- **Whisper transcription.** Default `condition_on_previous_text=True` caused a `Thank you.` hallucination loop on the silent portion that contaminated the whole transcript on first pass. Re-running with `--condition-on-previous-text False` fixed it. **Add this flag by default in any future Bench transcription pipeline.**
- **Format recommendation.** This session was an onboarding, not a topical seminar. Future onboarding sessions might warrant a separate folder convention or a tag — the prep/live-doc/notes/followups structure assumes a topical session and doesn't quite fit a guided tour.
