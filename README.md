# Utility AI Semantic Layer

A utility grid-intelligence reference architecture showing how MuleSoft APIs can translate operational signals into governed context for grid operators, field teams, customer-service channels, and AI agents.

> **Project status:** Reference architecture and API specification (specs-and-documentation only). The repository includes OpenAPI contracts, configuration standards, and documentation. It does **not** yet include runnable Mule applications or an automated test suite. Operational outcomes shown in scenarios are design targets, not independently validated production results.

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

The platform currently catalogs API contracts across these layers. See the `api-specs/` folder for the authoritative specifications.

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
api-specs/       17 OpenAPI 3.0 contracts, organized by architectural layer:
                   experience/ (3) · process/ (8) · system/ (6)
config/          Naming, versioning and error-handling conventions (3 files)
docs/            Semantic-layer, capability-map, implementation-status and
                 portfolio documentation (+ architecture diagram)
SECURITY.md      Security guidance
CONTRIBUTING.md  Contribution guidance
LICENSE          Project license
```

## What's actually included

This repository is **specs-and-documentation only** at this stage. The concrete artifacts present are:

- **17 OpenAPI 3.0 API contracts** under `api-specs/`, grouped by API-led layer:
  - `experience/` (3): `agent-alerts-api`, `agent-dashboard-api`, `dashboard-overview-api`
  - `process/` (8): `incident-create-api`, `dispatch-crew-api`, `grid-coordination-api`, `critical-infra-alerts-api`, `a2a-coordination-api`, `a2a-priority-alerts-api`, `mcp-grid-exchange-api`, `mcp-safety-orchestration-api`
  - `system/` (6): `scada-status-api`, `scada-devices-api`, `smart-meter-usage-api`, `der-devices-api`, `weather-forecast-api`, `salesforce-assets-api`
- **3 governance/config standards** under `config/`: `naming-conventions.yaml`, `versioning-rules.yaml`, `error-handling-standards.yaml`
- **Documentation** under `docs/`: `SEMANTIC_LAYER_EXPLAINED.md`, `capability-map.md`, `implementation-status.md`, `portfolio-guide.md`, and the `utilities-ai-semantic-layer.png` architecture diagram
- **Project docs** at the root: `SECURITY.md`, `CONTRIBUTING.md`, `LICENSE`

**Not included (planned / reference only):** this repository has no `mule-apps/` directory (runnable Mule applications) and no `tests/` directory. The Mule flows, DataWeave transformations, and automated tests referenced in the scenarios are design intent, not shipped assets.

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
- review the simulated storm, outage, meter and dispatch scenarios described in the specifications;
- extend governance controls before connecting consequential systems.

Before production use, validate requirements with utility operations, cybersecurity, safety, regulatory, data-governance, and platform teams. Apply organization-specific NERC CIP and other obligations; this repository does not constitute certification or compliance assurance.

## Technology

- MuleSoft and API-led connectivity
- OpenAPI-based contracts
- DataWeave and Mule application patterns (design concepts)
- OAuth 2.0, mTLS and policy-oriented security patterns
- SCADA, weather, smart-meter, DER and Salesforce integration concepts

## License

See [LICENSE](LICENSE).
