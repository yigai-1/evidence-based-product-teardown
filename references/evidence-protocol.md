# Evidence Protocol

## Evidence gate

Substantive teardown requires at least one primary product artifact that can be inspected. A product name, summary, memory, or marketing claim alone is insufficient.

### Strong primary evidence

- ordered screenshots covering entry, core flow, decision points, output, and errors;
- an accessible live product with a clear read-only scope;
- source code with the relevant entrypoints, state, services, and configuration;
- screen recordings with readable text and visible transitions;
- exported conversations, tool results, task histories, or official specifications.

### Secondary evidence

- official product documentation;
- official pricing/model capability pages;
- official release notes.

Keep secondary evidence separate. It may explain intended behavior but does not prove that a particular session executed that behavior.

## Completeness check

Before analysis, test coverage across these checkpoints:

1. entry and user intent;
2. configuration/input;
3. first product response;
4. core processing or execution;
5. user confirmation/correction;
6. produced asset or external effect;
7. task/current state;
8. terminal output/export;
9. error, interruption, permission, or billing state;
10. history/version/asset persistence.

Missing checkpoints do not always block a limited report. They block claims of a complete architecture. State the resulting scope explicitly.

## Evidence ledger schema

Use a stable record such as:

| ID | Source | Time/order | Exact observation | Element type | Supports | Contradicts | Access limit |
|---|---|---:|---|---|---|---|---|

Element types include user action, text, button, form, asset, state, error, model option, tool result, code location, and official documentation.

For screenshots, cite the screenshot number and exact visible wording. For code, cite the absolute file path and line. For live pages or official documentation, cite the URL and access date.

## Claim rules

- An agent saying “done” proves only that the message appeared.
- An asset card proves an asset is visible, not necessarily persisted, versioned, or valid.
- A button proves an entrypoint exists, not that its downstream operation succeeds.
- A public planning/thinking summary proves the product exposed that summary, not hidden reasoning or a completed tool call.
- A visible model name proves that option exists in the interface, not a multi-provider routing architecture.
- A UI graph edge proves a displayed relationship, not a stable backend foreign key.
- Source code proves an implementation path exists; runtime use still requires invocation, configuration, tests, logs, or observable behavior.

## Contradictions

When chat, task state, canvas, asset library, logs, or final output disagree:

1. preserve every observation;
2. state the capture time/order if known;
3. avoid choosing one as authoritative without evidence;
4. identify the missing source of truth;
5. classify the consistency problem and its user impact.

## Safe collection

- Prefer read-only inspection.
- Do not trigger paid or irreversible actions to obtain evidence.
- Do not inspect secrets or unrelated private data.
- Ask for user takeover when authentication or CAPTCHA is required.
- If a requested architecture depth cannot be supported safely, stop at the supported depth and list the evidence needed next.

