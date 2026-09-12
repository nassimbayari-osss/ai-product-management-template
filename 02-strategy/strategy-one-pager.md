# AI Strategy One-Pager · Juno

> Module 2 · Strategy. Built with the **M2 · AI Strategy One-Pager Builder** (informed by the Three-Layer Model Mapper). Paste the tool's markdown over this file.

## The bet

_The one-sentence strategic bet._

_____

## Three-layer model

- **Model layer:** _which model(s), and why._
- **Data / retrieval layer:** _what proprietary data or context creates advantage._
- **Product layer:** _the experience users actually pay for._

## Why now

_Market timing + why this is defensible._

_____

## Success metric

_The single number that says the bet paid off._

_____
# AI Strategy One-Pager - Juno Automated Prioritization

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
