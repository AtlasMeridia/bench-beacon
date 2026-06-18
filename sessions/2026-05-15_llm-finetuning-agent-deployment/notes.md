---
last_updated: 2026-05-15
status: draft
visibility: review-required
source_artifacts:
  - Google Meet recording, 2026-05-15 12:54 GMT-7
  - Google Meet chat export, 2026-05-15 12:54 GMT-7
  - Local Whisper transcript generated 2026-05-15 under `_dev/transcripts/2026-05-15_llm-finetuning-agent-deployment/`
source_limitations:
  - Whisper hallucinated repeated "Thank you" during the pre-conversation/silent portion of the recording.
  - Transcript has no reliable speaker attribution.
  - Public review should check attendee identity, work examples, and private/personal references before publication.
---

# Bench — Local LLM fine-tuning and agent deployment (2026-05-15)

A repeat Bench session focused on moving from local AI experimentation toward a usable agent workflow, learning loop, and possible business/content surface. The attendee brought concrete local-hardware results, work experiments, and questions about model training. Kenny pushed toward documentation, public process, and choosing a business direction through live artifacts rather than waiting for the stack to feel finished.

## What Happened

The session opened around local model performance on a multi-GPU workstation. The attendee had discovered that model size and VRAM placement matter more than generic benchmark numbers: a model that fits cleanly across the GPUs runs well, a larger model spilling into system memory runs badly, and a smaller model can underuse the hardware.

That led into a discussion of training, fine-tuning, LoRAs, and when to use local hardware versus rented GPUs. Kenny explained LoRA-style adaptation as a lighter way to steer a large base model toward a specific behavior or identity without retraining the whole model. RunPod and Unsloth came up as concrete tools for doing heavier optimization or training outside the local machine.

The second thread was workflow maturity. The attendee had met with an internal LLM team and came away with advice to get better at plan mode, skills, context, prompting, and markdown files. Kenny reframed this as two different layers of learning:

- hardware/model infrastructure: GPUs, VRAM, local model choice, training, inference speed;
- agent/user workflow: markdown context, skills, project files, planning, and repeatable prompts.

Kenny showed AtlasCortex and the Bench & Beacon repository as examples of how files can become the operating surface for agents. The important move was not adding more apps; it was making the file system, terminal, markdown, and agent instructions legible enough that an AI can pick up context and keep working.

## Attendee Context

The attendee arrived with more momentum than in the prior local-LLM session:

- local models had been benchmarked and felt manually, not just measured;
- the workstation’s memory/VRAM constraints were clearer;
- work projects had started becoming visible as a project board;
- markdown, skills, and planning mode had shifted from abstract advice into practical next steps;
- the attendee was beginning to ask how this becomes career leverage, content, consulting, or a business.

The public version should keep company/work details generalized unless explicitly cleared.

## Recommendations and Demonstrations

### 1. Do not wait to be fully dialed in

Kenny pushed back on the idea that the attendee should first get all tools, prompting, context, markdown, and hardware into equilibrium. The AI landscape will not hold still long enough for that. The better move is to document the current setup continuously so the system can tell the attendee what is already known, what changed, and what to try next.

The practical rule: document the current state, then iterate. Do not wait for a finished state before building with it.

### 2. Treat fine-tuning as one tool, not the whole project

Fine-tuning and LoRAs are useful, but they are not the first bottleneck for every use case. Before training models, define the workflow:

- what task should improve;
- what examples or data are available;
- what output would be visibly better;
- whether local inference, rented GPUs, or a hosted model is the right first step.

For the attendee’s current phase, learning what fine-tuning is may be useful homework. Building a repeatable agent/documentation workflow may be more immediately valuable.

### 3. Use GitHub and project boards as the visible work surface

The attendee had started a simple project board showing project name, platform/tools, and status. Kenny connected this to GitHub: if experiments become repos, the repo list itself becomes a portfolio, a learning log, and a substrate for AI agents.

This matters because the attendee’s work is currently fragmented across local models, work tools, scripts, and ideas. A project-board view could turn that into momentum.

### 4. Start posting before the business idea is perfect

The business discussion moved from "what business should we start?" toward "ship the process and let the business emerge." Kenny pointed to the pattern: data company first, media company second, product/service company third.

For this group, that suggests a near-term path:

- record or summarize the weekly AI-building process;
- post useful fragments on LinkedIn, YouTube, or another surface;
- build an audience around the learning process;
- use audience and repeated themes to discover product or consulting demand.

A professional LinkedIn presence came up as the lowest-friction first channel, especially for career leverage and recruiter visibility.

### 5. Keep consent and publishing boundaries explicit

A consent boundary came up in the content discussion. Bench & Beacon can become public media, but only with clear participant expectations and deliberate review before anything is published.

The useful version: invite people to talk about AI experiments, tell them what is being recorded, and publish only cleaned/public-safe material.

### 6. Turn business ideas into one-page evaluated artifacts

Late in the session, the discussion shifted from choosing a single business idea to building a repeatable way to evaluate many of them. The working concept was a lightweight business-discovery tool: collect rough ideas, notes, screenshots, and criteria; ask AI to organize them; then produce a one-page brief covering the idea, opportunity, risks, market whitespace, and next test.

Kenny connected this to a recent workflow that turned phone photos of handwritten notes into structured markdown and then into an HTML page. The useful pattern is not the specific page format. It is the agent loop: capture messy source material, convert it into a readable artifact, publish or share it, and use the artifact to decide what to test next.

## Tools and References

Shared in chat:

- Unsloth — https://unsloth.ai/
- RunPod — https://www.runpod.io/
- Bench & Beacon repository — https://github.com/AtlasMeridia/bench-beacon
- Alex Finn post on AI companies / data-media-product framing — https://x.com/AlexFinn/status/2054300833987342443?s=20

Discussed:

- local multi-GPU inference and VRAM fit;
- LoRA / low-rank adaptation;
- model distillation and fine-tuning;
- Hugging Face model discovery;
- markdown files as agent context;
- plan mode and skills;
- Obsidian / AtlasCortex as an AI-readable working vault;
- Claude Code / terminal-based agent work;
- Codex-assisted weekly review;
- here.now as an agent-first publishing surface;
- OCR / image-to-markdown / HTML one-page briefs for rough ideas;
- GitHub repos as portfolio and agent context;
- LinkedIn / YouTube as possible output channels.

## Open Questions

- Which model sizes fit cleanly on the attendee’s current GPU setup, and which spill into system memory?
- Is the first useful training experiment a LoRA, a small fine-tune, or simply better prompts/context over an existing model?
- What should the attendee’s project board track: projects, tools, business ideas, learning milestones, or all of them?
- What is the first public/professional post that is useful without overexposing work context?
- Should Bench & Beacon become a public recording/content surface, or stay primarily a private working seminar for now?
- Which business ideas deserve actual research: family-tree tooling, fridge/pantry-photo workflows, business discovery tools, content/consulting, or something else?
- What should a one-page business-discovery brief always include: market scan, SWOT, buyer, distribution path, first test, or technical build plan?

## Format Notes

This session shows Bench & Beacon becoming a repeat working loop rather than one-off AI advice. The value is accumulating across sessions: local hardware experiments, agent workflow literacy, business ideation, and publishing strategy are starting to reinforce each other.

The public notes should be cleaned carefully. The transcript contains personal jokes, company/work context, and names that should not automatically become publishable. The durable public value is the pattern: document current state, turn experiments into artifacts, and let repeated artifacts create both learning and business surface.
