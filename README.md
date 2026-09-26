# Juno PM

Juno helps RocketShip PMs turn fragmented product signals into evidence-backed insights and prioritization decisions, grounded in RocketShip’s live product and strategy context.

Nassim Ayari - AI PM Cohort - September 2026

This repo is my final project for the **AI Product Management Certification**. Each module's artefact lives in its own folder; this README is the dashboard and the pitch.

**How to use this template:** click **Use this template → Create a new repository**, name it `juno-pm`, and commit one module's artefact per session. Assemble this dashboard with the **Final Project Deliverables Builder** (paste its `README.md` output over this file).

---

## Module artefacts

### M1 · Prompting
- **System prompt** — [`01-prompting/system-prompt.md`](01-prompting/system-prompt.md)
- **Lovable prototype** — (https://ai-prd-synthesizer.lovable.app)

### M2 · Strategy
- **Decision matrix** — [`02-strategy/decision-matrix.md`](02-strategy/decision-matrix.md)
- **AI Strategy one-pager** — [`02-strategy/strategy-one-pager.md`](02-strategy/strategy-one-pager.md)

### M3 · RAG / AI PRD
- **AI PRD** — [`03-rag-prd/prd.md`](03-rag-prd/prd.md)

### M4 · AI-Native UX
- **AI user flow** — [`04-ai-ux/user-flow.md`](04-ai-ux/user-flow.md)
- **Trust-gap mitigations** — [`04-ai-ux/trust-gaps.md`](04-ai-ux/trust-gaps.md)

### M5 · Agentic Workflows
- **Agent Workflow Spec (AWSpec)** — [`05-agentic-workflows/awspec.md`](05-agentic-workflows/awspec.md)
- **Agent Control Panel** — [`05-agentic-workflows/agent-control-panel.md`](05-agentic-workflows/agent-control-panel.md)

### M6 · Evals & Guardrails
- **Eval stack** — [`06-evals/eval-stack.md`](06-evals/eval-stack.md)
- **Human evaluation rubric** — [`06-evals/human-rubric.md`](06-evals/human-rubric.md)

---

## PM Execution Plan

### Where Juno is today
Prototype-stage AI PM assistant. Juno can synthesize fragmented product signals, connect them to RocketShip strategy, verify evidence grounding, and prepare draft priorities for PM review. Roadmap commitments remain human-controlled.
_____

### What ships next (next 2 sprints)
Sprint 1: Strengthen evidence retrieval and verification; improve handling of conflicting/incomplete evidence.
Sprint 2: Instrument PM workflow-time tracking, finalize automated evals, and test Juno with a broader set of real prioritization requests.
_____

### What I watch (dashboards)
PM time per prioritization cycle
Juno usage and repeat usage
Insight rejection/regeneration rate
Human eval score
Evidence-grounding / Unverified rate
Roadmap commitments blocked by verification
_____

### Red lines (what blocks shipping — numbers, not feelings)
>10% of outputs contain fabricated or unsupported evidence → stop prioritization use.
Any roadmap commitment based on an unverified insight → stop and investigate.
<4.0/5 average human evaluation score → no expansion.
Any permission/safety failure that allows an unapproved roadmap write → immediate block.
_____

### Governance
_Compliance · Safety · Reliability · Reputation._
Compliance: approved data sources and controlled access.
Safety: unverified insights cannot be committed; roadmap writes require PM confirmation.
Reliability: tool failures/timeouts stop the run and surface a partial result.
Reputation: no fabricated evidence, unsupported claims, or silent AI decisions.

---

## Build Insights

- **Friction point.** The hardest part was translating a broad AI product idea into specific workflows, controls, evaluation criteria, and measurable outcomes without over-automating a decision that still requires PM judgment. Also, I do not have a technical background, which made this exercise difficult without AI assistance. 
- **Key learning.** I'll try this exercise for an actual business problem I want to solve.
- **Aha moment.** The biggest shift was realizing that building an AI product isn't just about getting the model to produce a good answer. The product is the system around the model that makes the output trustworthy, usable, and safe to act on.

---

## Repo structure

```
juno-pm/
├── README.md                          ← this dashboard + pitch
├── 01-prompting/
│   ├── system-prompt.md               ← M1: Juno's system prompt
│   └── lovable-prototype.md           ← M1: prototype link + debrief
├── 02-strategy/
│   ├── decision-matrix.md             ← M2: build / buy / fine-tune / partner call
│   └── strategy-one-pager.md          ← M2: AI strategy one-pager
├── 03-rag-prd/
│   └── prd.md                         ← M3: AI PRD with retrieval requirements
├── 04-ai-ux/
│   ├── user-flow.md                   ← M4: AI-native user flow
│   └── trust-gaps.md                  ← M4: trust-gap mitigations
├── 05-agentic-workflows/
│   ├── awspec.md                      ← M5: Agent Workflow Spec
│   └── agent-control-panel.md         ← M5: Agent Control Panel
└── 06-evals/
    ├── eval-stack.md                  ← M6: layered eval stack
    └── human-rubric.md                ← M6: human evaluation rubric
```

---

_Certification submission — AI Product Management Certification._
