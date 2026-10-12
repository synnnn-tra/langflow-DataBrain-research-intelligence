# Limitations and roadmap

## Verified from the current repository artifact

- The JSON file parses as valid JSON.
- The export metadata identifies Langflow 1.12.4.
- The graph contains five nodes and four edges.
- The model component offers Google Generative AI provider options.
- The active graph's main path runs from Chat Input through the custom orchestrator and model/formatter components to Chat Output.

These are artifact-level checks, not end-to-end runtime test results.

## Not yet verified

- Import and execution on a clean Langflow 1.12.4 installation.
- Runtime availability of all custom component dependencies.
- File parsing/retrieval quality across representative documents.
- Accuracy and evidence traceability of generated reports.
- Live web search or external-source coverage.
- A real Composio Toolset connection.
- MCP endpoint exposure, IBM Bob tool discovery, and end-to-end calls.
- Performance, reliability, and production readiness.

## Roadmap

### Phase 1 — Baseline validation
- [ ] Import the flow into a clean local Langflow 1.12.4 environment.
- [ ] Confirm every custom node loads and inspect warnings.
- [ ] Run text-only and file-input smoke tests.
- [ ] Check output claims against known input evidence.

### Phase 2 — Evidence-aware research
- [ ] Define a repeatable test set of research questions.
- [ ] Add explicit source provenance and evidence-quality assessment.
- [ ] Test date handling, conflicting sources, and missing-evidence behavior.
- [ ] Ensure the agent does not claim to have used unavailable tools.

### Phase 3 — Integrations
- [ ] Add a real Composio Toolset only where the use case needs it.
- [ ] Test each tool in isolation and then through the agent.
- [ ] Expose the target flow through MCP.
- [ ] Connect IBM Bob and verify discovery, invocation, and returned results.

### Phase 4 — Release readiness
- [ ] Add actual, consented screenshots or sanitized sample run artifacts.
- [ ] Add repeatable validation steps and record known failures.
- [ ] Review custom code and secret handling.
- [ ] Select and add an explicit project license if reuse is intended.

## Status language

Use **implemented** only for behavior visible in code or verified in execution. Use **tested** only when a test was run and its result recorded. Use **planned** for capabilities still awaiting integration or validation.
