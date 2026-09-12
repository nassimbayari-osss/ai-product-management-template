# AI Strategy One-Pager · Juno

> Module 2 · Strategy. Built with the **M2 · AI Strategy One-Pager Builder** (informed by the Three-Layer Model Mapper). Paste the tool's markdown over this file.

## The bet

Juno will help RocketShip PMs turn fragmented product signals into evidence-backed prioritization decisions faster, using AI grounded in RocketShip’s live product and strategy context while keeping final roadmap decisions with the PM.

_____

## Three-layer model

- **Model layer:** Use a capable general-purpose LLM through an API rather than building a foundation model. The model provides synthesis, classification, reasoning, and drafting; RocketShip's differentiated value comes from the system around it.
- **Data / retrieval layer:** Ground Juno in RocketShip's proprietary product-signal corpus — support tickets, customer interviews, usage signals, and strategy documents — using RAG to retrieve current, relevant evidence before making a recommendation. This creates an advantage because the model can apply RocketShip-specific priorities and evidence rather than relying on generic knowledge.
- **Product layer:** A PM co-pilot that identifies recurring problems, evaluates them against company strategy and customer evidence, and produces an evidence-backed priority recommendation with sources, rationale, and confidence. The PM reviews and approves the final decision.

## Why now

RocketShip's rapid growth has created Signal Collapse: PMs have more customer and product signals than they can reliably synthesize, while headcount is frozen. AI can now combine retrieval, synthesis, and workflow automation well enough to reduce this bottleneck without requiring RocketShip to build its own foundation model. The defensible advantage is not the model itself; it is RocketShip's proprietary signal corpus, prioritization logic, workflow integration, and trust controls.

_____

## Success metric

50% reduction in PM time spent synthesizing and ranking incoming product signals before a prioritization decision.

Measure baseline time to produce a prioritized opportunity list against time with Juno, while maintaining human approval and evidence grounding.

_____

# Raw Work: AI Strategy One-Pager - Juno Automated Prioritization

## 1. Problem & Workflow

The Problem: PMs prioritize the loudest or most visible request rather than the highest-value customer problem, because signals are fragmented and manually synthesized. Priorities reverse weekly; stakeholder trust is eroding.

Prevention: Juno is not deciding the roadmap. It is preventing bad input to the roadmap decision: an unreliable priority ranking.

## 2. Target Metrics

Cycle time: reduce average weekly roadmap prioritization from 2 hours to 30 minutes (75% reduction).

Leadership proof: under-10% rate of decisions reversed within 1 week, AND 90%+ of prioritised items have at least 2 cited sources from the corpus. Both metrics measurable in the first 30 days post-launch.

## 3. Autonomy Level

Choice: Copilot. Juno drafts a ranked backlog with written reasoning + source citations; the PM reviews and clicks 'approve' before publish.

Explicitly avoiding: Agent. Letting Juno move sprint priorities or shift live dates without a human approval step is a one-way trust-erosion door - a single wrong call lets stakeholders dismiss the system permanently.

## 4. Data & Model Approach

Approach: Ground (RAG). We will ground the model in the RocketShip corpus - Slack #escalations, support tickets, interview notes, Notion product pages, Jira tickets - so every priority cites a source ID.

Explicitly avoiding: We are not refining/fine-tuning the model to encode RocketShip's prioritization logic at V1. Fine-tuning could improve consistency later, but it would not solve the core problem: Juno needs access to current, changing evidence from customers, usage, support, and product systems.

## 5. Risks & Mitigations

Risk: training data lag. Juno systematically overweights frequent or loud customer signals, causing PMs to deprioritize important problems affecting smaller or less vocal customer segments.One quarter of skewed priorities and the roadmap drifts.

Mitigation: a hard 'evidence balance' eval gate - reject any priority list where less than 20% of cited sources come from any one source type. Run weekly; PM reviews.

## 6. V1 Scope

In: ranking the existing backlog with cited evidence; surfacing under-cited items; flagging conflicts between Slack escalations and Jira priorities.

Out: (1) Autonomously committing or changing the product roadmap.
(2) Automatically sending customer/external communications or creating irreversible product actions.
