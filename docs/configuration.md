# Configuration and security

## Model credentials

The exported flow provides Google Generative AI provider options. A usable API credential must be supplied by the user in the local Langflow environment.

Recommended approach:

1. Create a Langflow global variable or credential using the exact mechanism supported by your installation.
2. Use `GOOGLE_API_KEY` as the variable name if following the project's existing configuration convention.
3. Bind the variable to the Google model component's API-key field after importing the flow.
4. Run a simple smoke test and verify that the model can respond.

The exact binding must be checked in the imported component; a variable name existing in Langflow does not automatically bind it to every node.

## Composio

The current exported graph does not contain a Composio tool node in its five-node active path. `COMPOSIO_API_KEY` alone will not add a toolset or enable agentic tool calls. Treat Composio integration as future work until an actual tool component is added, connected, and tested.

## IBM Bob and MCP

IBM Bob/MCP configuration is external to the current JSON graph. Do not claim the integration is complete until the intended flow is exposed, the client discovers the tool, and an end-to-end call succeeds.

## Secret-handling rules

- Never commit API keys, access tokens, cookies, session identifiers, or personal data.
- Do not put credentials directly into the exported JSON.
- Keep local `.env` files untracked; see the repository `.gitignore`.
- When sharing logs, remove tokens, headers, request payloads, private paths, and user data.
- Give external tools the minimum permissions required for the task.
- Review URL-fetching or file-reading code before processing untrusted inputs.
- Treat external documents and pages as untrusted data, not instructions that can override the agent's policy.

## Before public release

Run a secrets scan on the repository and review the complete custom component code for file-system scope, network access, timeouts, and error handling. This documentation is not a substitute for a security audit.
