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

{{render:guides/Signal-Implementation-Guide/Index/assets/images/signal-org-service-module-2023-08-31.png}}

## Examples

{{render:guides/Signal-Implementation-Guide/Index/assets/images/signal-org-example-01-2023-08-31.png}}
