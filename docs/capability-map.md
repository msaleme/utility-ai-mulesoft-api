# Utility capability map

| Business capability | Operational concern | Portfolio evidence |
|---|---|---|
| Grid situational awareness | Normalize SCADA, weather, meter and asset context | utility-ai-mulesoft-api |
| Storm and outage coordination | Associate incidents, impact, priority and dispatch | utility-ai-mulesoft-api |
| Demand and renewable integration | Model load, devices and optimization boundaries | energy-api-evolution |
| Field execution | Retrieve SOP, asset, inventory and work-order context | field-operations-support-agent |
| Vegetation risk | Analyze imagery and surface inspection context | vegetation-management-process-api |
| Customer operations | Orchestrate billing, usage, outage and service requests | utility-customer-service-process-api |
| Energy-efficiency programs | Eligibility, enrollment and status | Energy-Efficiency-Program-Enrollment-API |
| Smart-meter operations | Readings, alerts and asynchronous telemetry | SmartMeterAIAPI; SmartMeterAsyncAPI |
| Compliance management | Facilities, inspections, violations and evidence | Utilities-Compliance-Management |
| Test and demonstration data | Simulated readings, outages and faults | Utilities-Generator-API |

## Cross-cutting architecture

Every capability should be evaluated across five concerns:

1. identity and authorization;
2. runtime policy and decision rights;
3. data provenance and semantic consistency;
4. observability and audit evidence;
5. human oversight and safe failure modes.
