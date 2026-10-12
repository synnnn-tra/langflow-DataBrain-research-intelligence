# Getting started

This guide targets a local Windows setup using Langflow 1.12.4 and the flow export in this repository. Exact menu labels can vary with the way Langflow is installed.

## 1. Get the flow

Download the [DBRI Langflow JSON](./flows/DataBrain%20Update%20Version%202.2%20-%20Task%2011%20IntegrationDeployment.json). to a working folder.

## 2. Import into Langflow

1. Open the local Langflow interface.
2. Use its flow import/upload action and select `dbri-langflow-1.12.4.json`.
3. Inspect the canvas after import. Confirm the five nodes and four main-path connections are present.
4. Open the model component and configure a valid Google Generative AI credential through the installed component's supported interface.

Do not assume that a syntactically valid JSON import means custom code or dependencies will execute successfully.

## 3. Run a smoke test

Start with a simple request without confidential material:

> Create an outline for a research brief about evaluating AI customer-support assistants for Indonesian small businesses. Separate facts, assumptions, questions to investigate, risks, and recommendations. Do not invent statistics or citations.

Check that:
- The flow completes without a component error.
- The response is returned from Chat Output.
- Missing evidence is clearly called out.
- The model does not claim that it searched sources or used tools unless that actually happened.

Record the Langflow version, the prompt, the result, and any sanitized error message.

## 4. Test file input separately

After text-only execution works, attach a small non-sensitive text or PDF file supported by the Chat Input configuration. Ask the model to extract the document's main claims and indicate which claims require external verification.

Do not use confidential documents during initial tests. File parsing and retrieval should be validated against known expected content before treating outputs as reliable.

## 5. Keep a reproducible test log

For each run, record:
- Date and Langflow version
- Model/provider selected
- Input prompt and whether a file was attached
- Expected behavior
- Actual behavior
- Error or limitation
- Pass/fail decision

## 6. IBM Bob / MCP integration

Do this only after the flow passes direct testing. Follow the MCP exposure and client configuration supported by your installed Langflow version, then verify in order: endpoint availability, tool discovery, one explicit tool call, and returned output. See [Architecture](architecture.md).
