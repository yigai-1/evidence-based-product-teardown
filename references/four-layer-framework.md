# Four-Layer Teardown Framework

Analyze each layer independently, then connect them through events, reads/writes, model invocations, assets, and state transitions.

## 1. User layer

Determine:

- target user and job-to-be-done;
- entrypoint, onboarding, input, configuration, and permissions;
- normal journey, correction loop, failure, interruption, and return paths;
- decisions and confirmation gates;
- visible feedback, waiting, cost, trust, emotion, and friction;
- collaboration, sharing, export, and terminal success;
- archetype-specific risks.

Required outputs:

- evidence-backed journey table;
- journey/decision flow;
- user thoughts, emotions, pain points, and opportunities;
- observable terminal condition versus the user's real goal.

## 2. Technical layer

Determine visible or necessary functional domains:

- client/workbench surfaces;
- applications and business capabilities;
- agent/workflow orchestration;
- tools and services;
- task state, asynchronous work, retries, cancellation, idempotency;
- permissions, safety, billing, export, storage, and integrations;
- observability and quality gates.

Do not claim backend languages, databases, queues, clouds, or vendors without evidence. For hidden infrastructure, separate:

- required capability;
- plausible choices;
- recommended design;
- reason it cannot be confirmed.

Required outputs:

- functional-domain map;
- end-to-end control/tool flow;
- layered As-Is architecture;
- To-Be improvements and priority risks.

## 3. Model layer

For every visible or inferred model task, check:

- modality and role: text, image, video, audio, speech, embedding, moderation;
- user-selectable model, mode, resolution, duration, language, reference inputs;
- prompt/template compilation and structured output;
- capability registry and model routing evidence;
- safety, copyright, cost, latency, failure rate, fallback, retry, and quality checks;
- whether the model result becomes a versioned asset or only chat text;
- whether user feedback is tied to the exact model invocation and asset version.

Do not infer a complete router from one model selector. Do not infer a model vendor from output style.

Required outputs:

- model-task matrix;
- invocation and result flow;
- capability/constraint gaps;
- separation between current choices and recommended model gateway.

## 4. Data layer

Separate data domains instead of drawing one “global context” box:

- UserContext: identity, locale, plan, allowance, permissions, private assets;
- ProjectConfig: task type, format, language, style, model settings;
- DomainContext: product-specific records such as script, character, case, order, or plan;
- AssetContext: media/files, ownership, lineage, versions, storage references;
- WorkflowState: current step, task, agent/run, approval, error, cancellation;
- BillingContext: estimate, reservation, consumption, refund;
- EvaluationContext: user feedback, automated checks, failure reasons;
- KnowledgeContext: public knowledge, private memory, style/templates, capability rules.

These are analysis templates, not claims about real field or table names.

For each field/object, document:

- value or visible state;
- producer and consumers;
- read/write timing;
- version and ownership;
- evidence level and citation;
- invalidation and recomputation rule;
- permission and retention boundary.

Required outputs:

- context/data dictionary;
- producer-consumer table;
- entity/relationship diagram when evidence supports it;
- consistency, lineage, versioning, privacy, and billing risks.

## Cross-layer flows

At minimum draw or tabulate:

1. User event → interface → workflow/agent.
2. Agent → tool/service → model.
3. Model result → asset/version → context/state.
4. Context/state → next agent or UI.
5. User confirmation/modification → dependency invalidation → recomputation.
6. Failure/interruption → retry/cancel/compensation → billing outcome.

The analysis is incomplete if the four layers appear only as independent inventories.

