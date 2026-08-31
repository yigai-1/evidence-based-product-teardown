# HTML Deliverable Contract

## File requirements

- Deliver one standalone `.html` file in a durable, user-accessible output directory.
- Embed CSS and small JavaScript directly. Avoid build steps and remote dependencies unless a diagram library is essential.
- If using Mermaid from a CDN, keep the Mermaid source readable as fallback and mention that diagram rendering needs network access.
- Support widths from mobile to desktop; wide tables may use a contained horizontal scroll wrapper.
- Use accessible headings, semantic tables, visible labels, sufficient contrast, and keyboard-accessible controls.
- Do not embed secrets, private account data, hidden reasoning, or unsupported architecture facts.

## Minimum report structure

Adapt to scope, but normally include:

1. Executive summary and product archetype.
2. Evidence scope, ledger, and gaps.
3. User layer: journey, decisions, emotions, friction, opportunities.
4. Technical layer: domains, workflows, agents/tools/services, states and failures.
5. Model layer: tasks, capabilities, choices, constraints, cost/safety/retry.
6. Data layer: contexts, entities, versions, producer-consumer relationships.
7. Cross-layer end-to-end flow and architecture diagram.
8. Current architecture (As-Is).
9. Recommended architecture (To-Be).
10. Prioritized risks.
11. Component-to-evidence traceability.
12. Unknowns and next evidence to collect.

Every major table or diagram node must make its evidence status visible: `【已确认】`, `【合理推断】`, `【建议设计】`, or `【未知】`.

## Diagram rules

- Show flow direction and label important edges: trigger, call, read, write, event, confirmation, asset reference, state update.
- Distinguish evidence levels visually and include a legend.
- Show key data and states, not only boxes representing components.
- Mark known consistency defects and missing gates.
- A reader should be able to answer where input enters, who/what processes it, what gets called, where results are stored, how the next step reads them, how users correct the result, and what happens on failure or interruption.

## Validation checklist

- Open the final file and confirm headings, tables, diagrams, and navigation render.
- Check that all local file links use absolute paths when delivered in Codex.
- Search for placeholders and remove unused sections.
- Verify that product-specific facts remain in the report, not in this reusable skill.
- Verify each confirmed claim has an evidence reference.
- Verify unknown implementation choices remain unknown.

