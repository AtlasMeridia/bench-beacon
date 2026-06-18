---
last_updated: 2026-06-12
status: draft
visibility: review-required
session_type: Beacon (Friday, seminar / landscape)
source_artifacts:
  - Google Meet recording, 2026-06-12 14:53 GMT-7 (room `xxb-kopw-ppn`, ~86.9 min)
  - Google Meet chat export, 2026-06-12 14:53 GMT-7 (links only)
  - Local Whisper transcript (mlx_whisper large-v3) under `_dev/transcripts/2026-06-12_distributed-compute-and-ai-investing/`
source_limitations:
  - Transcript has no reliable speaker attribution; speaker assignment is inferred from context.
  - Contains real first names (Justin, AJ, plus Jesse and Nick) and identifying details — an on-mic account/full-name, and AJ's employer profile. Generalize or clear before any public version.
  - Whisper mangled product/model names (e.g. "Cloud"/"Quad" → Claude, "Ben B"/"BNB" → BenBe, "Herney's" → Hermes, "fable" → Fable); corrected here on best effort.
  - "Air / barrier liquidity thesis" is a low-confidence transcription; read as the AI-IPO "liquidity thesis." Several macro/finance claims are Kenny's read of the news, not verified fact.
---

# Beacon — Donated compute, the practical agent stack, and AI for investing (2026-06-12)

The second Friday Beacon under the twice-weekly cadence. Like the prior Beacon, the value landed one-on-one rather than in a group: it ran as two back-to-back 1:1s — first with the builder regular (Justin) about his "donate compute" project, then with the health/finance attendee (AJ) about using AI for investing. The landscape through-line: pooling idle compute (Folding@home, distributed-compute blockchains, free web hosting), the practical agent stack (Codex vs. Claude, the shared Hermes agent "BenBe"), and a long investing segment built around one tension — efficient markets vs. the rare quant who beats them.

## What Happened

The first half opened with the usual Bench-style logistics fumble (sharing a screen, two Gmail sessions, getting a meeting link between two machines — flagged in the transcript as a standing thing to fix). Justin then walked through a GUI mockup of a "donate compute" app: a downloadable tool where people pool idle machines toward a common goal, modeled on Folding@home. It's still at the fake-front-end stage — no working backend, no settled business model. Kenny's main move was to reframe it: this is a portfolio/consulting artifact and a way to learn distributed computing, not (yet) a product. They talked through hosting it free on Vercel, the existence of distributed-compute blockchains ("distributed data center"), the hard part (chunking AI work across unreliable nodes), and the recurring warning not to get lost in tooling. Justin left to prep a BBQ (the group is meeting in person the next day).

The second half, with AJ, went deep on AI for investing. AJ has been feeding screenshots of financial info to Perplexity and finding the summaries useful but generic. That opened the session's core argument: off-the-shelf AI trading bots are reportedly no better than the S&P 500, so the leverage is in using AI to *learn* the markets — as a tutor on top of human experts — rather than to autotrade. Threads: the efficient-market view (*A Random Walk Down Wall Street*) vs. the quant exception (Jim Simons); which paid model a near-beginner should start with (Codex/ChatGPT over Claude); a shared "play" trading account; and the macro backdrop (Fed posture, IPOs, the Bay-Area "liquidity" shift). It closed on Kenny's other side projects (SBA acquisitions, an import/export idea) and the shared Hermes agent, BenBe.

## Attendee Context

Two attendees, each in a separate 1:1; the group is still "jagged" in AI experience.

- **Justin** — the returning builder. Vibe-codes with Claude Code in the terminal; built the compute-pool mockup as a Python app. Runs an open-source local rig (the "hive"/local-LLM thread from prior sessions), is finishing school (this could be a final-project / portfolio piece), and hosts the in-person BBQ the next day. Tends to spread across many threads and over-index on infrastructure before nailing a direction — the recurring coaching point.
- **AJ** — the health/finance attendee (returning from the 2026-06-05 Beacon). Works at a medical-device company, mostly **program management** now (Jira/Bitbucket, spreadsheets, email) rather than engineering; the stack is Ruby on Rails and he knows only the basics. Work restricts AI to Microsoft Copilot (IP/data concerns; a Microsoft-shop culture). Uses Perplexity personally. Planning to leave around October to maximize stock vesting, and wants to automate his workload to free up time for projects like these. Primary interest: investing/finance; secondary: health.
- Brief non-participants: **Jesse** (Justin's kid, on a call interruption) and **Nick** (named as a third machine for the compute pool).

(All attendee names and identifying employer/account details must be generalized or cleared before any public version — see followups.)

## Recommendations and Demonstrations

### Half 1 — Justin's "donate compute" project

**1. Treat the build as a portfolio/consulting artifact, not (yet) a product.**
Justin's instinct was to perfect the app; Kenny's reframe was that the highest-leverage output right now is *evidence of capability*. Standing up a compute-pool tool and learning how distributed/network computing actually works is something he can show for jobs, consulting, or "even just your homies." Concretely: have Claude Code generate a README and an SOP/devlog while building, so the process is documentable after the fact ("you don't have to document as you go — you can walk your Claude Code logs later").

**2. Distributed compute already exists — study the landscape and reappropriate, don't rebuild the PhD layer.**
The honest framing: properly building distributed training across many machines is genuinely hard (chunking work, handling dropped nodes, recombining results — "you kind of need a PhD" for the real version). Rather than build that from scratch, learn the existing landscape: **Folding@home** as the canonical "donate idle GPU to a cause" example (Kenny ran it ~20 years ago), and **distributed-compute blockchains** that already pool machines into a "distributed data center" to train models (Kenny shared a Grok writeup of these in chat). Better path: find an existing open-source client, treat it as a Lego piece, and experiment by connecting real machines (Justin's rig + Kenny's M4 + Nick's box) toward a shared goal — the *learning* is the unlock, regardless of whether anyone ever "donates" compute.

**3. Ship it as a free website; don't over-index on packaging.**
A desktop download is the heaviest packaging; a GitHub repo deployed free on **Vercel** (its own URL, ask Claude Code to wire it up) is the lightest. Mobile/native is even more stack to add. The point is to keep pulling the thread, not to perfect the delivery format — "keep exploring the idea."

**4. Pick a direction before the destination disappears.**
Recurring coaching, restated: Justin wants to do *all* the directions (portfolio piece, learning distributed computing, a business) at once. Kenny pushed for prioritizing one, and for defining the actual problem/task the pooled compute would solve before designing the infrastructure — "we're talking about the car, not whether we're going over the mountains or to the grocery store." Also flagged: don't get distracted by every new tool and harness; focus on the project and sort tooling out after.

### Half 2 — AJ on AI for investing

**5. Off-the-shelf AI trading bots ≈ the S&P; build to your own thesis.**
AJ cited a study (paraphrased) that commercially available AI trading bots aren't meaningfully better than just holding the S&P 500. Conclusion both landed on: the edge isn't a generic bot, it's a tool built around *your* niche, strategy, and sentiment.

**6. Efficient markets vs. the quant exception — learn it via AI, not 400 pages.**
Kenny framed the two poles. *A Random Walk Down Wall Street* (the "industry-standard" investing book) is the efficient-market view: even PhD finance and math gurus mostly can't beat the S&P. The counterexample is **Jim Simons** — the "godfather of quantitative trading," a math PhD who started in the '80s and beat the market systematically (framed as the anti–Warren Buffett; "a YouTube rabbit hole"). The practical recommendation for AJ: don't read the whole book — have an AI (Perplexity, or better a reasoning model) summarize and teach the ideas, ideally tied to a concrete goal so it's salient.

**7. Use AI as a finance *tutor*, not an autotrader.**
The clearest convergence of the half. Rather than handing money to an autonomous agent, point AI at *learning*: take human experts you already trust and have the model explain them from simple to complex. Kenny's heuristic: understand the bond market and options and you have a real handle on trading (bonds alone are a 30-year career for some). Concrete project both want: an **agent that ingests finance-podcast/expert transcripts and emits a weekly executive summary** — Kenny listens to several hour-plus shows and wants the time back. Sources named: **Forward Guidance** (Blockworks — younger, sharp, crypto-to-macro, "arcane but fun") and the **All-In podcast** (Gen-X tech billionaires — "abhorrent personalities," but real industry/IPO signal). Macro that came up, as Kenny's read: **Kevin Warsh** as incoming Fed chair, expected dovish but forced hawkish because U.S. debt is too high to cut rates — "no regime change, because America has too much debt to service."

**8. For a near-beginner, start with Codex/ChatGPT over Claude — and don't marry one model.**
Kenny's standing landscape lesson, applied to AJ: Claude is the smartest for high-level abstract thinking and writing, but Anthropic throttles/nerfs under compute strain, so a beginner is "safer" on ChatGPT/OpenAI for token availability. **Codex** (comes with Codex Desktop; phone↔computer sync on the same files) integrates with the terminal and with Office/Excel far more fluidly than Claude — useful for a non-coder doing spreadsheet/email/research work. Three frontier labs now: Anthropic, OpenAI, XAI. **Fable** (Claude's smartest model, sampled ~10 days) is mostly a novelty — it burns tokens (spawns ~50 agents for trivial tasks) and only pays off on hyper-technical or hard human-language tasks; most work doesn't need it. A non-coder can still get real value: Kenny once gave a model his portfolio weights and account balances and it proposed a reallocation — no coding required, just a paid reasoning account.

**9. A shared "play" trading account to learn by doing.**
Proposal: everyone puts in ~$100, run different agents/wallets with different strategies, and watch how they play out — "putting money on stuff makes it more live." Coinbase now offers agents; AJ has Coinbase + Schwab ("atrocious UI," via the Ameritrade/Thinkorswim lineage). Kenny recommends a **Robinhood** account for the fun/experimental sleeve (good UI, crypto, prediction markets — "degenerate money and fun"), keeping long-term investing separate from short-term trading. Options trading came up as a low-effort, low-risk-if-done-right side-income angle worth learning.

**10. BenBe / Hermes as the group's shared, model-agnostic agent.**
Kenny showed **BenBe** (named for Bench & Beacon), built on **Hermes agents** (Nous Research). It lives on Telegram/Slack/Signal/iMessage, can spin up throwaway web pages, run multi-agent research, and even hold a crypto wallet — currently scoped to just processing meetup transcripts, with room to add per-interest profiles later. It's model-agnostic (Claude/GPT/Grok/Chinese open-source, or Justin's home rig) and currently runs off Kenny's Grok/XAI account; Claude is best but ~20× the per-token cost. Nudge to attendees: get on **Telegram** so the group can use BenBe (and consolidate off Slack).

## Tools and References

Shared in chat:
- Vercel — free GitHub-repo → website hosting (for Justin's project) — https://vercel.com
- Grok writeup of distributed-compute blockchains — https://grok.com/share/bGVnYWN5LWNvcHk_80669aa8-2c1b-44fa-949b-bdf300e61492
- Folding@home — https://foldingathome.org/
- *A Random Walk Down Wall Street* (Burton Malkiel) — https://www.amazon.com/Random-Walk-Down-Wall-Street/dp/1324051132 (and the Kindle edition)
- Jim Simons — https://en.wikipedia.org/wiki/Jim_Simons
- YouTube video shared during the investing segment (likely the Jim Simons / quant rabbit hole) — https://youtu.be/9z4YYo9BQ08
- Hermes agent (Nous Research) — https://hermes-agent.nousresearch.com/
- Kenny's note "Ship first, then find the money" — https://www.kennyliu.io/notes/ship-first-then-find-the-money
- A tweet shared near the IPO/Bay-Area discussion — https://x.com/rohitdotmittal/status/2063010570429669736

Discussed:
- Folding@home; distributed-compute blockchains ("distributed data center"); compute-credit / crypto incentives
- Claude / Claude Code; Codex / Codex Desktop (cross-device sync); Perplexity; Microsoft Copilot (work-mandated); Grok
- Fable (Claude's sampled top model) — novelty/token cost; "don't marry one model"
- Hermes agents → BenBe (Telegram/Slack/Signal/iMessage; multi-agent research; crypto wallet); runs on Grok/XAI
- Investing vs. trading; options; bond markets; off-the-shelf bots ≈ S&P 500
- Brokerages: Robinhood (recommended for the fun sleeve), Coinbase (+ agents), Schwab/Ameritrade/Thinkorswim, E-Trade
- Forward Guidance (Blockworks), All-In podcast; Kevin Warsh / Fed posture; AI-IPO "liquidity thesis" (Bay-Area shift)
- Claude/Grok "conversation mode" — walk-and-brain-dump → cleaned, prioritized summary
- Kenny's side projects: SBA acquisitions (federal cap doubled $5M→$10M; AI agents to screen candidates); an import/export idea; "living archive" of agents on his site
- tmux for persistent terminal sessions across phone/computer

## Open Questions

- For Justin: which single direction first — portfolio piece, learning distributed computing, or a business? And what concrete task would the pooled compute actually run?
- Is there a real incentive layer (crypto/compute-credit) that makes "donate compute" more than a learning exercise, or does it stay a portfolio piece?
- For AJ: which paid account is the right first step — Claude or Codex/ChatGPT — given his non-coding, spreadsheet-heavy work?
- Does the group stand up the weekly finance-podcast-to-summary agent (clear, buildable now), and who owns it?
- Shared play trading account: real money with per-agent strategies, or keep it a thought experiment? Who's in, what's the mandate, which broker?
- How real is the AI-IPO "liquidity thesis" for the Bay Area, and is there anything actionable (real estate, positioning) or is it just narrative?
- Standing logistics gap: get reliable two-machine / two-Gmail screen-sharing and link-passing sorted before the next session.

## Format Notes

Same lesson as the last Beacon, reinforced: the depth comes in 1:1s, not the group. This session never had a group phase — it was two sequential one-on-ones, and each produced something concrete (Justin's project direction; AJ's investing learning plan) precisely because it stayed on one person's situation. The two halves also map cleanly onto Bench vs. Beacon energy: Justin's is hands-on/build (Bench-shaped), AJ's is landscape/learning (Beacon-shaped), even though both happened in a Friday slot. Worth keeping: BenBe + Telegram as the connective tissue so these conversations leave a usable trace (transcripts → summaries → followups) instead of evaporating. And the recurring meta-point — attendees are smart but spread thin — argues again for a standing "one focal thing per person" anchor.
