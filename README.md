# Utility AI Semantic Layer

A utility grid-intelligence reference architecture showing how MuleSoft APIs can translate operational signals into governed context for grid operators, field teams, customer-service channels, and AI agents.

> **Project status:** Reference architecture and demonstration implementation. The repository includes API specifications, Mule application assets, configuration standards, tests, and documentation. Operational outcomes shown in scenarios are design targets, not independently validated production results.

## Why this project exists

Utility response depends on information distributed across SCADA, outage management, weather, smart-meter, distributed-energy-resource, asset, customer, and workforce systems. This project demonstrates an API-led semantic layer that converts those signals into reusable operational context.

The design emphasizes:

- a consistent vocabulary across operational and enterprise systems;
- separation of system connectivity, process orchestration, and user experiences;
- priority and safety context for AI-assisted decisions;
- traceable interactions across agents, APIs, and human operators;
- reusable contracts for storm response, dispatch, outage communications, and grid coordination.

## Reference architecture

| Layer | Responsibility | Representative capabilities |
|---|---|---|
| Experience APIs | Channel-specific views | Field alerts, operator dashboard, executive overview |
| Process APIs | Cross-system orchestration | Incident coordination, crew dispatch, critical-facility prioritization, agent coordination |
| System APIs | Governed source access | SCADA, weather, smart meters, DER, Salesforce assets |
| Semantic layer | Operational meaning | Asset relationships, customer impact, priority, safety and policy context |

The platform currently catalogs API contracts across these layers. See the repository folders for the authoritative specifications and implementation assets.

## Demonstration scenario

A storm event produces equipment and outage signals. The reference flow:

1. normalizes telemetry and weather information;
2. associates affected assets with customers and critical facilities;
3. produces an impact and priority context;
4. proposes dispatch and communication actions;
5. routes consequential actions through policy and human-oversight boundaries;
6. records correlation identifiers and decision evidence.

This scenario is intended for architecture evaluation and demonstration. It does not claim autonomous control of a production electric grid.

## Repository contents

```text
api-specs/       API contracts organized by architectural layer
mule-apps/       Mule implementation assets
config/          Naming, versioning and error-handling conventions
tests/           Test assets
docs/            Architecture, semantic-layer and portfolio documentation
SECURITY.md      Security guidance
```

## Documentation

- [Semantic layer explained](docs/SEMANTIC_LAYER_EXPLAINED.md)
- [Utility portfolio guide](docs/portfolio-guide.md)
- [Utility capability map](docs/capability-map.md)
- [Implementation status and evidence](docs/implementation-status.md)
- [Security guidance](SECURITY.md)

## Portfolio role

This is the flagship grid-intelligence project in a broader utilities portfolio:

| Capability | Repository |
|---|---|
| Grid and operational intelligence | **This repository** |
| Grid, demand and renewable-energy APIs | [energy-api-evolution](https://github.com/msaleme/energy-api-evolution) |
| Utility compliance architecture | [Utilities-Compliance-Management](https://github.com/msaleme/Utilities-Compliance-Management) |
| Field technician assistance | [field-operations-support-agent](https://github.com/msaleme/field-operations-support-agent) |
| Vegetation analysis | [vegetation-management-process-api](https://github.com/msaleme/vegetation-management-process-api) |
| Customer-service orchestration | [utility-customer-service-process-api](https://github.com/msaleme/utility-customer-service-process-api) |
| Energy-efficiency enrollment | [Energy-Efficiency-Program-Enrollment-API](https://github.com/msaleme/Energy-Efficiency-Program-Enrollment-API) |
| Utility test-data generation | [Utilities-Generator-API](https://github.com/msaleme/Utilities-Generator-API) |
| Smart-meter agent API | [SmartMeterAIAPI](https://github.com/msaleme/SmartMeterAIAPI) |
| Smart-meter events | [SmartMeterAsyncAPI](https://github.com/msaleme/SmartMeterAsyncAPI) |

## Evaluation and use

Use this repository to:

- review API contracts and canonical domain boundaries;
- evaluate semantic context for agent-assisted utility operations;
- demonstrate MuleSoft integration patterns;
- test simulated storm, outage, meter and dispatch scenarios;
- extend governance controls before connecting consequential systems.

Before production use, validate requirements with utility operations, cybersecurity, safety, regulatory, data-governance, and platform teams. Apply organization-specific NERC CIP and other obligations; this repository does not constitute certification or compliance assurance.

## Technology

- MuleSoft and API-led connectivity
- OpenAPI-based contracts
- DataWeave and Mule application assets
- OAuth 2.0, mTLS and policy-oriented security patterns
- SCADA, weather, smart-meter, DER and Salesforce integration concepts

## License

See [LICENSE](LICENSE).
