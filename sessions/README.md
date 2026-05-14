---
last_updated: 2026-05-07
---

# Session Structure

The session loop is the product before the product:

prep → live working doc → AI notes → followups → next session

## Per-session folders

Each session gets its own dated folder directly under `sessions/`:

`YYYY-MM-DD_short-topic-slug/`

Inside:

- `prep.md` — pre-session notes, agenda, links, intended outcomes.
- `live-doc.md` — the working surface from the session, exported or pasted from Google Docs / HackMD.
- `notes.md` — AI-generated session notes, post-processed for usefulness.
- `followups.md` — open threads, action items, decisions, and links to durable project artifacts.

## Naming

- Use `YYYY-MM-DD_topic` for all sessions.
- Example: `2026-05-13_claude-code-vault-prep`
- If the Bench/Beacon distinction matters for a session, keep it in the session title, frontmatter, or notes — not in the folder hierarchy.

## Defaults

- Keep raw live mess in the live doc during the session.
- Convert to durable notes after the session.
- Do not preserve raw recordings unless there is a specific reason.
- Do not commit raw recordings or transcripts.
- Treat every committed file as potentially public.

## Publishable session frontmatter

Use this once a session artifact has been reviewed:

```yaml
---
last_updated: YYYY-MM-DD
status: reviewed
visibility: public
---
```

A session is publishable only after `notes.md` and `followups.md` are cleaned for attendee safety. `prep.md` and `live-doc.md` are optional public artifacts, not defaults.
