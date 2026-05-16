---
last_updated: 2026-05-08
status: draft
visibility: review-required
---

# Followups — Edge AI automation hardware (2026-05-08)

## Action Items

### Kenny

- [ ] Review the generated transcript against the notes before marking this session reviewed.
- [ ] Confirm which attendee names, company affiliations, startup/customer/funding details, and infrastructure references are public-safe.
- [ ] Decide whether the session should remain public-facing or stay internal until the automation/business details are cleaned.
- [ ] Send a short reference pack if useful: NVIDIA embedded systems, Jetson Orin Nano, Tailscale, OpenRouter, and the Coinbase developer post.
- [ ] Clarify the first practical project: local inference, hosted-model orchestration, device networking, industrial vision, internal tooling, or a specific automation workflow.
- [ ] Decide whether AI setup/scaffolding for non-technical users is becoming a Bench offer or just an observed need.

### Guests

- [ ] Identify the first concrete use case to test on edge AI hardware.
- [ ] Decide whether the prototype needs local inference, remote model calls, or both.
- [ ] Inventory what hardware is already available before buying a Jetson-class device.
- [ ] Sketch the deployment environment: where the device sits, how it connects, who needs access, and what data can leave the site.
- [ ] Pick one recurring work loop to automate and document the before/after time cost.
- [ ] If using local models, define what success means before tuning hardware: latency, privacy, cost, reliability, or offline operation.

## Open Questions

1. **What is the actual first workflow?** The references point toward industrial automation, AI-assisted internal tools, and edge vision, but the first job-to-be-done still needs to be named.
2. **Is edge inference required?** Local hardware only matters if latency, connectivity, privacy, cost, or field constraints make hosted inference insufficient.
3. **What data is sensitive?** Before public notes get sharper, confirm whether company names, equipment context, or site details should be omitted.
4. **Which hardware tier fits v0?** Jetson Orin Nano may be enough for experimentation; DGX-class hardware is likely a different decision category.
5. **How should remote access work?** Tailscale is a strong candidate if the prototype needs private access across machines or sites.
6. **What is public-safe about the business discussion?** The generated Granola summary included startup, customer, funding, and distribution details. Do not publish those without review.
7. **Should regular AI summit meetings become part of Bench?** The Granola notes mention recurring group meetings; decide whether that is a separate format from normal Bench sessions.

## Process Notes

- This session exposed a useful capture pattern: Meet chat gives links, Granola gives a working summary, and the recording remains the source of truth.
- For future sessions, save the Granola share link alongside the Meet recording link immediately after the session.
- Granola output should be treated as source material, not a public artifact. It may include private attendee and company details.
- Keep raw recordings, raw transcripts, and raw chat logs outside the publishable repo unless they have been deliberately cleaned.
