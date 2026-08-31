# Product Archetype Router

Use this reference after evidence intake and before selecting the teardown emphasis.

## Classification method

Classify from observed value delivery, not brand language. Ask:

1. What terminal outcome does the user seek?
2. What does the product do autonomously?
3. What is the highest-risk irreversible action?
4. What state must remain consistent across sessions?
5. What artifact, relationship, transaction, or decision is the product optimizing?

Choose a primary archetype and, when useful, a secondary archetype.

## Archetype emphasis matrix

| Archetype | Primary evidence | User-layer emphasis | Technical-layer emphasis | Model-layer emphasis | Data-layer emphasis |
|---|---|---|---|---|---|
| AIGC creation | prompts, settings, generated media, revisions, model options | creative intent, preview, approval, correction, cost anxiety | generation pipeline, async tasks, asset dependencies, quality gates | modality, reference control, resolution/duration, safety, cost/latency | project config, prompt versions, media assets, lineage, feedback |
| General execution agent | plans, tool calls, approvals, task results, external effects | delegation, trust, approval, interruption, audit | orchestration, permissions, retries, idempotency, side-effect control | planning/tool selection, structured output, fallbacks | task state, tool ledger, external references, errors, approvals |
| Conversational companion | conversation history, persona, memory, safety interventions | emotional need, continuity, boundaries, retention | memory retrieval, session continuity, safety escalation | persona control, empathy, moderation, hallucination | profile, consented memory, sensitive data, retention/deletion |
| Workflow/SaaS | records, roles, forms, status transitions, integrations | job-to-be-done, collaboration, handoffs, reporting | transactions, workflow, RBAC, integrations, notifications | assistive automation, extraction, summarization, recommendations | business entities, permissions, audit log, source of truth |
| Marketplace/content | listings/content, discovery, ranking, transactions, moderation | supply/demand loop, discovery, trust, conversion | search/ranking, moderation, payments, rights, fulfillment | recommendation, moderation, creation assistance | catalog, graph, events, transactions, reputation, rights |
| Developer tool | repository, terminal, diffs, tests, CI, artifacts | intent, review, control, reproducibility | sandbox, filesystem/git, tests, deployment, permissions | code reasoning, tool use, context selection | repository state, patches, traces, test results, environment |

## Hybrid examples

- An AIGC product with autonomous publishing is primarily AIGC and secondarily an execution agent. Add approval and side-effect controls to the creative pipeline analysis.
- A companion that creates images is primarily conversational companion if relationship continuity is the core value. Treat media generation as a supporting model flow.
- A SaaS product with an embedded agent remains workflow/SaaS when authoritative business records and role permissions determine completion.

## Avoid common classification errors

- Do not classify every chat interface as a conversational product.
- Do not classify every product using models as an AIGC product.
- Do not infer autonomous execution from an agent persona label.
- Do not let a single visible model selector determine the entire product architecture.

