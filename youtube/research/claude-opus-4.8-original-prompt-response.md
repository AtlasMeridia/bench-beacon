---
model: Claude Opus 4.8 (1M context)
model_id: claude-opus-4-8[1m]
generated: 2026-06-17
prompt: >
  Task list for setting up a weekly YouTube channel for Bench & Beacon:
  inventory of potential assets, list of video ideas, and a task list to
  start. Maximally produced video without buying gear not already owned.
  Thoughts seeded in COUNSEL/walk-talk; assets across AtlasCortex,
  ~/AudioVisual, ~/Projects/atlas-style-guide, and other ~/Projects.
---

# Bench & Beacon — weekly YouTube channel: assets, templates, ideas, task list

A few judgment calls made on review before writing this up:

- **Corrected the gear picture** to the actual inventory (the Fujifilm SD card
  an agent found was only a fragment of it; the canonical Tech Setup Summary is
  far deeper).
- **Flagged the `~/AudioVisual/characters/` library as off-limits** for this
  channel. An agent enthusiastically nominated "Sable/Elle/Nadine" as channel
  mascots. Those belong to a separate, not-brand-safe AI-character project
  (robotica). Using them here would be a brand mistake. The *agents* Ben B /
  Nadine / Sophia are a different thing.
- **Wrote this whole brief without em dashes**, since the voice profile makes
  that non-negotiable. The channel inherits the same rule.

---

## The assessment, up front

**You are not gear-constrained. You are template-and-workflow-constrained.** That
is the entire finding.

The research consensus on perceived production value is **audio > lighting >
camera**, and per the Tech Setup Summary you already own the top of all three
tiers: a broadcast dynamic mic (**Shure MV7+**, USB-C/XLR, auto-level), a 63W
bicolor COB light (**SmallRig RC 60B**, CRI 97+), a gimbal vlog cam with
face-tracking and a built-in mic (**DJI Osmo Pocket 3**), a film-sim stills
camera (**Fujifilm X100VI**), a B-roll drone (**DJI Mini 4 Pro**), and a **16"
M4 Max / 128GB** that edits 4K without flinching. On the software side you have
Final Cut Pro, DaVinci Resolve, the full Adobe suite, Blender, TouchDesigner,
local Whisper, ffmpeg, a Higgsfield generation MCP, and a mature brand token
system with a live export endpoint.

"Maximally produced without buying gear" is not a stretch for this kit. It is
the easy part. The hard part is the **one-time setup tax** you already named in
`landmarks.md` (deck template, thumbnail template, recording workflow, design
assets, rehearsal) plus **one open decision** that is quietly blocking
everything: *live-chat capture vs. clean lecture.* This brief closes the tax and
recommends a default for the decision.

---

## Part 1 — Asset inventory (what you already have)

### A. Hardware (per `2025-09-09 Tech Setup Summary.md`)

| Role | Gear you own | Use in the channel |
|---|---|---|
| **Primary voice** | Shure MV7+ dynamic (USB-C + XLR, auto-level, pop filter) | The single biggest quality lever for a slides/screen format. 15–30 cm from mouth, level to −14 LUFS. |
| **Key light** | SmallRig RC 60B COB, 63W bicolor, CRI 97+ | Soft key for talking-head segments. Bounce off ceiling/wall or shoot through a diffuser. |
| **A-cam (talking-head / walk)** | DJI Osmo Pocket 3 Creator Combo (1", 4K/120, gimbal, ActiveTrack, flip screen, built-in mic) | Run-and-talk and to-camera bookends. Face-tracking means no operator. |
| **B-cam (static, "look")** | Fujifilm X100VI (film sims) | Static talking-head with signature color, or as a webcam via Fujifilm X Webcam. |
| **B-roll / aerial** | DJI Mini 4 Pro (4K) | Establishing shots, "touch grass while building computer stuff" texture. |
| **Edit station** | MacBook Pro M4 Max, 128GB, 4TB | Local Whisper captions, FCP/Resolve, even local LoRA training, all on-device. |
| **Monitor / NAS** | LG 34" UltraWide, Synology DS923+ 16TB | Editing real estate; media backbone and backup. |
| **Upgrade path (optional, not needed)** | Sony a6700 + Sigma 70mm (the "LOCKED" Living Archive build) | Only if you want a flip-screen APS-C A-cam later. Skip for launch. |

**Conclusion:** this is an indie-studio kit. No purchase is justified to ship
video #1.

### B. Software and tooling (installed unless noted)

- **Edit / color:** Final Cut Pro, DaVinci Resolve (free, Hollywood-grade
  color), iMovie, Adobe Premiere (sub).
- **Motion / graphics:** After Effects, Blender (+ your `blender-bridge` HTTP
  control), TouchDesigner (+ `touchdesigner-bridge`) for generative intros/B-roll.
- **Design:** Photoshop, Illustrator, Figma, Keynote. Topaz Gigapixel/Photo AI
  for upscaling.
- **Audio:** GarageBand (royalty-free sting + loops), local Whisper (captions, $0).
- **CLI:** ffmpeg (encode/burn captions/batch), yt-dlp.
- **Generative:** Higgsfield MCP in this session (`generate_image` Soul,
  `generate_video` DoP, `generate_talking_head` Speak v2, `create_character`) ≈
  $3/video if used. `ai-toolkit` for a custom FLUX style LoRA.
- **Automation / publishing:** Hermes "BenBe" agent on the beacon box (Telegram
  + Drive OAuth), `headless-atlas` (Ghost publishing), Buffer wired to 1 X + 1 IG
  + **1 YouTube channel** (already created, verified 2026-06-10).
- **To verify/install (free or owned):** **iA Presenter** (your chosen deck
  tool; `landmarks.md` flags "verify feature set" — Keynote is the installed
  fallback and can record narrated slides + export video). **OBS Studio** (free)
  if you want to composite slides + screen + webcam in one live scene.

### C. Brand system (mature, exact values ready to drop into templates)

Source of truth: `~/Projects/atlas-style-guide/data/tokens.json` → live at
`style.kennypliu.com/api/export/css`.

- **Color:** navy `#0e1318` (deep bg) / `#08090c` (near-black), cream `#f3f0ea`
  (fg), **accent gold `#c9924a`** (and `#ddb878` light / `#8a6530` deep).
  Semantic green `#6a9a70`, red `#b05454`.
- **Type:** Cormorant Garamond (display), Lora (body), DM Sans (UI), IBM Plex
  Mono (code), Noto Serif TC (zh).
- **Invariants (apply to thumbnails and lower-thirds too):** no emoji, no
  gradients, no stock photography, **sentence case**, Phosphor light icons,
  **zero em dashes**.
- **Logo:** telescope + wrench, production-ready with full export set:
  - `~/AudioVisual/Branding/Bench-And-Beacon/openai-logo-simple-telescope-wrench-1-clean.svg` (master)
  - `…-clean-transparent.png` (transparent) + `…-exports/` (16→1024px + favicon).
- **Signposts:** `bench-beacon/Pasted image 20260428150627.jpg` (Bench),
  `bench-beacon/CleanShot 2026-05-07 at 10.24.30@2x.png` (Beacon).

### D. Visual / footage assets (and one explicit caution)

- **Usable now:** the logo set above; the brand token system; your own future
  screen-grabs and diagrams (the best B-roll for this niche, per research).
  Higgsfield can generate on-brand backgrounds/B-roll on demand.
- **Do not use:** `~/AudioVisual/characters/` (Sable, Elle, Nadine folders,
  "robotica") and the `grok animation` library. These are a separate,
  not-brand-safe AI-character project. An inventory agent nominated them as
  mascots; that would be a real brand mistake for a credibility-driven AI/PKM
  channel. Keep them out.
- **Headshots:** `~/AudioVisual/Branding/headshots/2026-03-29-midjourney-portraits/`
  exist, but they are AI portraits. For a "fellow traveler, building in public,
  voice-is-the-moat" channel, **your real face on the Osmo is more authentic.**
  Reserve the AI portraits for a stylized avatar/about image if you want one.

### E. Distribution rails already in place

YouTube channel created + phone-verified (2026-06-10), Buffer connected, Ghost
via `headless-atlas`, the Tue/Thu post cadence and `kennyliu.io` newsletter
already shipping. **Flag:** your design skill says `kennypliu.com` but live posts
publish to `kennyliu.io`. Pick the canonical domain before you bake it into
lower-thirds/end cards.

---

## Part 2 — Templates and setup to establish (the "setup tax," done once)

### Channel-level, one-time

- **@handle + identity:** set handle (Studio → Customization), confirm "not made
  for kids" so end screens/cards work.
- **Banner** 2560×1440, all content inside the centered **1235×338** safe area:
  wordmark + "Practical AI, weekly" + schedule line. Navy bg, gold rule, cream
  type.
- **Avatar** 800×800: the telescope-wrench mark on navy (legible at 36px in
  comments).
- **About + upload defaults:** keyword-rich description, default description
  footer (links to `kennyliu.io`, Substack/X), default category, language,
  end-screen/card defaults.
- **Playlists from day one (your moat):** one playlist per *live project*
  (Flywheel, Weekly Briefing, Health Nudge, Ben B Demos) so viewers can watch a
  project iterate chronologically. `landmarks.md` calls this the archive no
  competitor has.

### Reusable production templates (build once, reuse weekly)

| Template | Spec | Build with (owned) |
|---|---|---|
| **Deck / slide master** | 16:9, navy bg, Cormorant headlines, DM Sans labels, gold accent, drop-cap title slide, "output-first" layout | iA Presenter (verify) or Keynote |
| **Thumbnail master** | 1280×720 (master at 4K), text **≤4 words sentence case**, mark bottom-left, keep bottom-right 20% clear, navy + cream + gold, flat (no gradient/stock) | Figma or Photoshop, fed by `tokens.css`; Higgsfield Soul for optional on-brand backdrop |
| **Title formula bank** | clarity-forward keyword + curiosity, hook in first ~48 chars, ≤70–80 chars, no em dash | text snippet file in `bench-beacon-ops` |
| **Lower-third** | name / role line, DM Sans, gold underline, 150–300ms ease-in | FCP/Resolve title or After Effects template |
| **Intro/outro sting** | 3–5s: mark draw-on + wordmark + one-line promise; outro = "next video" plate w/ ~20s of pad | After Effects (or Blender via `blender-bridge`); GarageBand for the audio bed |
| **End screen + cards** | end screen last ~20s: next-video + Subscribe; 1–2 cards mid-roll | YouTube Studio (set as default) |
| **Description + chapters** | hook in first 2–3 lines, chapters from `00:00`, ≥3 stamps, each ≥10s, links footer | template in repo |
| **Caption workflow** | local Whisper → `.srt` → upload + quick fix (feeds SEO/NLP + accessibility) | `whisper`, ffmpeg to burn if desired |
| **Episode project + folders** | FCP/Resolve project template; `episodes/NNN_slug/{raw, deck, exports, thumb, captions, shownotes}` on the NAS | FCP/Resolve + Finder/NAS |

### Thumbnail / title direction (a decisive recommendation)

The AI/PKM niche is drowning in identical Impact/Montserrat shouty thumbnails.
**Lean into your brand serif instead:** a large Cormorant Garamond headline (≤4
words) in cream on navy, a single gold accent, the mark small in the corner, and
a clean diagram or screen-grab as the only image. Credibility over shock. Make
**type style (serif vs bold sans)** and **face vs. no-face** your first two A/B
tests via YouTube's Test & Compare, with ~10k impressions before judging.
**Package before you film:** if you cannot write a compelling title + thumbnail
for an idea, the idea is not ready. Kill it early.

---

## Part 3 — The weekly pipeline and the open-decision recommendation

**One idea → keystone video → two derivative posts → optional Short.** This
matches your `landmarks.md` model (video is the main labor; Tue = the *how*, Thu
= the *why*).

1. **Capture** the idea on a walk-talk (your real method, and on-brand to show).
2. **Outline** 3–5 bullets; fully script only the first ~10 seconds (the hook).
3. **Record** in one session; batch 2–3 episodes when you can (saves 30–60 min
   of cold-start each).
4. **Edit lean:** silence/filler trim, captions, chapters, lower-thirds, light
   color match. Polish the first 60 seconds, then stop.
5. **Package:** title + thumbnail (built first), description with chapters.
6. **Publish scheduled** for the same day/time; pin a CTA comment.
7. **Fan out:** Tue/Thu posts from the transcript, a Short via the free Opus
   Clip tier, cross-post via Buffer. Automate this with BenBe only *after* the
   offer locks (your stated guardrail: "otherwise it's content into the void").

Realistic time budget once templates exist: **~1–3 hours per video** (lean
regime). The first one costs more because it builds the templates.

**Recommended resolution of the open "recording mode" question:**

- **Video #1 (the flywheel talk):** clean iA Presenter/Keynote lecture.
  Controlled, low-risk, lead-with-output, and it is what forges your templates.
- **Recurring format (Ben B demos):** **capture the live session, then trim.**
  Record the real Ben B + Hear-That-Now run (screen + audio), then lightly edit.
  Do *not* re-record a separate clean lecture. This protects your moat
  (authentic, unscripted, voice-led) and is the only sustainable choice weekly.
  So: lecture once to set the bar, then live-capture as the durable default.

---

## Part 4 — Video ideas (content bank, drawn from your own roadmap and voice)

**Beacon (Thursday "why" / longview thesis):**

1. **The flywheel principle** — "the model isn't the bottleneck; the input +
   curation flywheel is." *(Friday #1, already chosen.)*
2. **You are the harness** — the three-layer personalized stack (read-only vault
   → human-AI working layer → outsourced production).
3. **The therapy progression** — Freud → talk therapy → sycophantic ChatGPT →
   your own tuned stack. Why generic AI can't do self-discovery.
4. **Datasets that appreciate with model capability** — why your curated source
   files get *more* valuable as models improve.
5. **A default is a discipline** — the brakes thesis; "use Codex by default";
   avoiding tool-paralysis.
6. **AI as a market tutor, not an autotrader** — efficient markets vs. the
   Simons exception; your transparent NBLS portfolio.

**Bench (Tuesday "how" / hands-on tactics):**

7. **Ben B live demo** — agent runs a research/brainstorm loop, returns a Hear
   That Now page, reviewed together. *(Friday #2, already chosen.)*
8. **Build a weekly briefing automation** — "consume smarter, not more" (MVP
   result already exists in `CRAFT/GROK/loops/`).
9. **Voice is the input layer** — your walk-talk → structured-note pipeline,
   shown end to end. Maximally on-brand.
10. **Build a read-only personal vault** — layer 1 of the stack, from scratch.
11. **The health nudge loop** — data in → one verbal nudge out. "Dashboards are
    production porn."
12. **Lateral references mode** — a reusable Claude instruction that surfaces
    three adjacent concepts to widen ideation.

**First 8 weeks (suggested slate, packaged titles as examples, sentence case, no
em dash):**

| Wk | Video | Example title |
|---|---|---|
| 1 | Flywheel talk | "The model was never the bottleneck" |
| 2 | Ben B demo | "I let my AI agent run the research, live" |
| 3 | Voice is the input layer | "How I think out loud and let AI do the typing" |
| 4 | Weekly briefing build | "Consume smarter, not more: a weekly AI briefing" |
| 5 | Read-only vault | "Why your AI needs a source of truth it can't edit" |
| 6 | The therapy progression | "Your AI is too agreeable to know you" |
| 7 | A default is a discipline | "Stop tool-hopping: pick a default, get to work" |
| 8 | Health nudge loop | "I deleted the dashboard and kept one nudge" |

---

## Part 5 — The task list

### Phase 0 — Lock three decisions (15 minutes, unblocks everything)

- [ ] **Recording mode:** confirm "clean lecture for #1, live-capture
  thereafter" (recommended above).
- [ ] **Canonical domain:** `kennyliu.io` vs `kennypliu.com` for on-screen
  credits.
- [ ] **On-camera presence:** real face (Osmo) for hooks/bookends — recommended
  — vs. voice-only over slides.

### Phase 1 — Setup tax (this week, ~1 day total, one-time)

- [ ] Verify/install iA Presenter; if it falls short, use Keynote.
- [ ] Channel polish: @handle, banner (2560×1440, safe 1235×338), avatar
  (800×800), About, upload defaults, "not made for kids."
- [ ] Create the per-project **playlists** (Flywheel, Weekly Briefing, Ben B
  Demos, Health Nudge).
- [ ] Build the **deck master** (brand tokens, output-first layout).
- [ ] Build the **thumbnail master** in Figma/Photoshop from `tokens.css`;
  export 2 variants for A/B.
- [ ] Save the **title bank**, **description+chapters template**, and **episode
  folder template** in `bench-beacon-ops`.
- [ ] Build **intro/outro sting** (After Effects) + audio bed (GarageBand);
  **lower-third** title template.
- [ ] Set up the **caption workflow**: Whisper command → `.srt` → upload/fix.
- [ ] Confirm a **mic + light + Osmo** setup spot (face the window, COB as key,
  MV7+ 15–30 cm) and dial in one repeatable lighting/audio preset.

### Phase 2 — Ship video #1 (flywheel) by next Friday

- [ ] Package first: write title + design thumbnail (kill it if the package is
  weak).
- [ ] Outline the talk (lead with output); script only the 10-second hook.
- [ ] Record the lecture; record a 20–30s to-camera intro on the Osmo.
- [ ] Edit lean (trim, captions, chapters, lower-third, sting), color-match,
  export H.264 MP4 1080p at 8–12 Mbps.
- [ ] Upload, set end screen + 1–2 cards, chapters from `00:00`, schedule for
  your fixed slot, pin a CTA comment.
- [ ] Derive Tue (how) + Thu (why) posts; cross-post via Buffer.

### Phase 3 — Build the buffer and the recurring format

- [ ] Rehearse the **Ben B live demo** a couple hours/day; record a test run end
  to end.
- [ ] Bank a **3–4 video buffer** before leaning fully public, so cadence never
  slips.
- [ ] Run the **type and face A/B tests** on the first thumbnails; let data, not
  taste, decide.
- [ ] Tie each video's CTA to the **July 13 first-dollar** ask (the videos are
  the acquisition engine, not just content).

### Phase 4 — Systematize (only after the offer locks)

- [ ] Wire **BenBe** to auto-draft posts + Shorts from each transcript and queue
  them.
- [ ] Optional polish: a Higgsfield **on-brand visual identity for Ben B**,
  generated cleanly (not the robotica library); Higgsfield Soul/DoP for
  occasional B-roll (~$3/video).
- [ ] Log decisions + workflow in `bench-beacon-ops/devlog.md`.

---

## Open flags for you to settle

1. **iA Presenter** may not be installed yet (your own TODO). Keynote is the safe
   fallback and is installed.
2. **Domain** inconsistency (`kennyliu.io` vs `kennypliu.com`) before printing it
   on screen.
3. **Type style and face/no-face** are genuinely niche-split in the research.
   Treat them as your first A/B tests, not as settled choices.
4. The `~/AudioVisual/characters/` and `grok animation` libraries are **not**
   brand-safe for this channel. Keep the studio identity built from the
   telescope-wrench mark and your real footage.

---

This brief reconciled the gear conflict to your real inventory, kept everything
anchored to decisions you already made in the walk-talks (`landmarks.md`, the
July 13 deadline, video-as-keystone, voice-as-moat, lead-with-output), resolved
your one open format question with a concrete default, and respected the brand
rules down to the em-dash.
