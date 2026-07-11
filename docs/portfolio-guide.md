# Utilities portfolio guide

This portfolio organizes utility-sector reference implementations around operational capabilities rather than individual technologies.

## Positioning

The body of work demonstrates how governed enterprise integration can connect grid operations, field service, customer programs, smart-meter telemetry, compliance, and AI-assisted decision-making.

## Capability domains

### Grid intelligence and resilience

- [utility-ai-mulesoft-api](https://github.com/msaleme/utility-ai-mulesoft-api)
- [energy-api-evolution](https://github.com/msaleme/energy-api-evolution)

### Field operations and asset context

- [field-operations-support-agent](https://github.com/msaleme/field-operations-support-agent)
- [vegetation-management-process-api](https://github.com/msaleme/vegetation-management-process-api)

### Customer and energy programs

- [utility-customer-service-process-api](https://github.com/msaleme/utility-customer-service-process-api)
- [Energy-Efficiency-Program-Enrollment-API](https://github.com/msaleme/Energy-Efficiency-Program-Enrollment-API)

### Smart meters and operational telemetry

- [SmartMeterAIAPI](https://github.com/msaleme/SmartMeterAIAPI)
- [SmartMeterAsyncAPI](https://github.com/msaleme/SmartMeterAsyncAPI)
- [Utilities-Generator-API](https://github.com/msaleme/Utilities-Generator-API)

### Compliance and critical infrastructure

- [Utilities-Compliance-Management](https://github.com/msaleme/Utilities-Compliance-Management)

## Suggested review paths

**Executive:** begin with this repository's README, the capability map, and the storm-response scenario.

**Enterprise architect:** review the layered API boundaries, canonical models, security guidance, and cross-repository integration responsibilities.

**Developer:** begin with the API specifications and available reference documentation. Where sibling repositories contain implementation or test assets, inspect those separately and apply their stated evidence status.

## Curation principles

- distinguish reference designs from deployed production systems;
- label modeled benefits as scenarios or design targets;
- avoid unsupported certifications or compliance assertions;
- connect each component to a business capability;
- preserve human authority for safety-critical and consequential actions;
- keep customer, employer and confidential information outside public artifacts.
