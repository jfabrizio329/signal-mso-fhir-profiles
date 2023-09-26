---
topic: organization-services-module
---

# {{page-title}}

---

## Context
This is the administration module for Organiation Services, which defines the relationship between service organizations, provider agencies, and locations and the types of programs, services, and procedures they are able to provide.

## FHIR Focus Resource Types

| Name                      | Aliases                                   | Description |
| --- | --- | --- |
| {{pagelink:organization-profile}} | Provider, Agency, State Agency, County, Location        | Represents a distinct place where services are offered, in hierarchical fashion; e.g. a provider agency is an organization with 1 or more provider locations which are also organizations (their relationship is recorded using the .partOf reference |
| {{pagelink:organizationaffiliation-profile}}  | --- | Create associations between participanting providers (locations) and the service provider where specified services are provided in 1 or more HealthcareService resource(s) |
| {{pagelink:healthcareservice-profile}}   | Program, Services, Service Categories, Procedure codes | --- |
| {{pagelink:location-profile}}                 | --- | Utilized as a fact table for further descriptive elements of an Organization |


## Conceptual Model

{{render:guides/Signal-Implementation-Guide/Index/assets/images/signal-org-service-module-2023-09-22.png}}

## Examples
(An example is intended to be illustrative of the relationship between resources but may not represent a completely accurate business process at the time the example was published.)

### Provider Agency, Provider Locations, Services example

Fabricated provider *Denver Medical* has a location called *Denver East* that has affiliations for both Signal and RMHC.  (see diagram below)
- Denver East has 2 qualifications with Colorado BHA (via LADDERS) which allows services ASAM-0.5 and CYMHTA Treatment which are also coded as qualifications via the administrator.
- Denver East's affiliation with Signal offers 2 services, ASAM-0.5 (via SUD) and Treatment (via CYMHTA), and this occurs in Signal's South region.
- Denver East's affiliation with RMHC offers 1 service, Treatment (via CYMHTA), and this occurs in RMHC's Mid-West region.


{{render:guides/Signal-Implementation-Guide/Index/assets/images/signal-org-example-2023-09-22.png}}
