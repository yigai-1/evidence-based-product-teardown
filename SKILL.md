---
name: evidence-based-product-teardown
description: Evidence-led teardown and architecture analysis of software products from screenshots, live sites, recordings, documents, or source code. Use when the user asks to reverse-engineer a product's journey, features, agents, models, data, workflow, tools, or architecture. Do not use for evidence-free product ideation or ordinary reviews.
---

# Evidence-Based Product Teardown

Produce a verifiable product teardown without embedding any particular product's names, flows, or conclusions into the method.

## Non-negotiable gates

1. **Classify before decomposing.** Determine what kind of product is being analyzed and adjust the emphasis. Read [references/product-archetypes.md](references/product-archetypes.md).
2. **Require primary product evidence.** Do not begin substantive teardown from a product name, marketing summary, or the user's recollection alone. Read [references/evidence-protocol.md](references/evidence-protocol.md).
3. **Separate observation from architecture design.** Mark every conclusion as:
   - `【已确认】`: directly supported by primary evidence or official documentation.
   - `【合理推断】`: behavior supports the conclusion, but implementation is not directly visible.
   - `【建议设计】`: a proposed architecture or product improvement.
   - `【未知】`: evidence is insufficient.
4. **Use four layers.** Guide the teardown through User, Technical, Model, and Data layers. Read [references/four-layer-framework.md](references/four-layer-framework.md).
5. **Deliver one HTML file.** Use and adapt [assets/report-template.html](assets/report-template.html), following [references/html-deliverable.md](references/html-deliverable.md).

## Evidence intake

Accept one or more primary sources:

- complete, ordered product screenshots;
- an accessible product/site URL with permission to inspect it;
- source code or repository contents;
- screen recording with readable states;
- exported conversations, logs, API/tool results, product specifications, or official documentation.

Before analysis, state:

- the product object and suspected archetype;
- sources received and what each can prove;
- missing evidence that would materially change the result;
- the authorized interaction boundary.

If no primary evidence is available, stop and ask for screenshots, a URL, source code, or another inspectable artifact. Do not manufacture a generic teardown.

If evidence exists but is incomplete, either collect more evidence within the user's authorization or narrow the report scope. Never silently upgrade a partial view to a complete product architecture.

## Product classification

Choose the closest archetype, or a hybrid, from the reference. Explain the choice with evidence. The classification controls the emphasis:

- AIGC creation products: creation pipeline, prompt/configuration, consistency, assets, model constraints, cost, asynchronous generation, quality gates.
- General execution agents: planning, tool permissions, task state, approvals, retries, idempotency, external side effects, auditability.
- Conversational companion products: persona continuity, memory, safety, emotional feedback, privacy, retention, intervention and escalation.
- Workflow/SaaS products: roles, records, business state, collaboration, permissions, integrations, reporting and transaction consistency.
- Marketplaces/content platforms: supply, discovery, ranking, transactions, moderation, rights and creator/user loops.
- Developer tools: repository context, execution environment, diffs, tests, permissions, reproducibility and delivery.

Do not force a product into one category when evidence supports a hybrid. Name the primary and secondary archetypes and split the emphasis accordingly.

## Execution workflow

### 1. Build the evidence ledger

Inventory sources, assign stable evidence IDs, order them chronologically, and record exact page text, visible controls, assets, statuses, errors, model choices, and code locations. Keep source metadata separate from what the pixels or code actually prove.

When sources conflict, record the conflict. Do not select the more convenient source as truth.

### 2. Reconstruct the user flow

Follow one real task from entry to the furthest observed terminal state. Capture:

- user goal and action;
- interface feedback and decisions;
- system/agent result;
- asset and state changes;
- success, correction, failure, interruption, and return paths;
- emotion, friction, and product opportunity.

### 3. Decompose the four layers

For each layer, distinguish current evidence, inferred implementation, and recommended design. Connect the layers with explicit flows:

- user events and approvals;
- orchestration and tool calls;
- model inputs, outputs, limitations, safety, cost, and retries;
- context reads/writes, assets, versions, tasks, errors, permissions, and billing.

### 4. Test cross-layer consistency

Check at minimum:

- Does interface “complete” match task, asset, and final-output states?
- Do upstream edits invalidate downstream assets?
- Are model capabilities and cost enforced by services or merely described in text?
- Can every generated asset be traced to an input version and invocation?
- Are private user assets separated from public knowledge and shared assets?
- Is failure recovery idempotent and billing-safe?
- Is the terminal state based on verified results rather than an agent's claim?

### 5. Produce the HTML report

The report must be usable without reading the chat. Include source scope, evidence gaps, product archetype, executive summary, four-layer analysis, end-to-end flows, architecture diagrams, As-Is/To-Be, risks, traceability, and unknowns. Adapt the template rather than preserving irrelevant empty sections.

## Browsing and code inspection boundaries

- Treat live products as read-only unless the user explicitly authorizes a mutation.
- Do not send messages, generate content, publish, buy, recharge, delete, or overwrite assets during evidence collection unless explicitly requested.
- Never inspect or output passwords, cookies, tokens, authentication headers, browser storage, or unrelated personal data.
- Use an existing signed-in session only within the user's stated scope. If login, CAPTCHA, or takeover is required, hand control to the user and wait.
- For code, distinguish implementation facts from dead code, mocks, fixtures, configuration, and inferred runtime behavior.
- Use official product documentation only as a separate evidence class. Marketing claims do not override observed behavior.

## Quality bar

Before delivery, verify:

- every architecture component has evidence or a clear design rationale;
- every important claim has an evidence ID or code/document citation;
- product-type-specific concerns are covered;
- the four layers are connected rather than presented as unrelated lists;
- failures, corrections, interruptions, permissions, billing, safety, and versioning are not omitted merely because no example occurred;
- missing examples remain `【未知】`, not assumed;
- the HTML is a single, valid, responsive file with readable tables and diagrams;
- no product-specific methodology, System Prompt, credentials, or hidden reasoning is embedded in the skill.

