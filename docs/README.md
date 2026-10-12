# DBRI Documentation

Use this documentation map to navigate the technical documentation for DataBrain Research Intelligence (DBRI).

| Page                                                    | What it covers                                                              |
| ------------------------------------------------------- | --------------------------------------------------------------------------- |
| [Architecture](./architecture.md)                       | Existing flow components, connection paths, and planned integrations.       |
| [Getting Started](./getting-started.md)                 | Import the JSON into a local Langflow 1.12.4 instance and run a smoke test. |
| [Configuration and Security](./configuration.md)        | Model credentials, API-key hygiene, and external-service boundaries.        |
| [Output Contract](./output-contract.md)                 | The sections and structure expected in a useful research brief.             |
| [Limitations and Roadmap](./limitations-and-roadmap.md) | What is known, what remains unverified, and the next validation steps.      |

## Langflow Flow Artifact

The canonical Langflow project export is available here:

* **[Open the DBRI Langflow JSON](../flows/DataBrain%20Update%20Version%202.2%20-%20Task%2011%20IntegrationDeployment.json)** — Open the exported workflow file.
* **[View the flows directory](../flows/)** — Browse the available flow files and import documentation.
* **[Read flow import instructions](../flows/README.md)** — Review the workflow metadata and import steps.

## Import and Validation

1. Open the JSON export linked above.
2. Download it to your computer.
3. Import it into Langflow 1.12.4.
4. Configure the required model credentials locally.
5. Run a smoke test and review any component warnings before further use.

**Prototype status:** Import compatibility, runtime behavior, and external integrations must be validated in the target environment.
