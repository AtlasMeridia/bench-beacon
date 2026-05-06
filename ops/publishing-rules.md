---
last_updated: 2026-05-05
---

# Publishing Rules

Bench & Beacon keeps private thinking adjacent to public knowledge, but not mixed with it.

## Rule

Only cleaned, attendee-safe artifacts get committed and published.

## Never commit

- Raw recordings.
- Raw transcripts.
- Local Obsidian configuration.
- Private planning notes.
- Manifesto drafting questions.
- Internal decisions or deferred infrastructure notes.
- Credentials, tokens, API keys, or deployment secrets.

## Publishable by default after review

- `README.md`
- `sessions/*/*/notes.md`
- `sessions/*/*/followups.md`
- `ops/*.md`

## Conditional

- `sessions/*/*/prep.md` — publish only if it contains no private attendee context.
- `sessions/*/*/live-doc.md` — publish only if cleaned. The live doc is usually messy by design.
- Links to Google Docs, Slack, Drive, or Meet — publish only if the linked surface is intentionally public or permission-safe.

## Session publish checklist

Before a session folder is published:

1. `notes.md` has been reviewed for accuracy and usefulness.
2. Private attendee details are removed unless explicitly consented.
3. Action items do not expose private asks, emails, phone numbers, or company-sensitive context.
4. Raw transcript/live-doc material is removed or clearly cleaned.
5. Frontmatter includes:

```yaml
last_updated: YYYY-MM-DD
status: reviewed
visibility: public
```

## Privacy boundary

The `_dev/` folder is local-only and ignored by Git. It is not a publishing source.

Git ignore is a guardrail, not the whole privacy model. Anything committed should be assumed publishable.
