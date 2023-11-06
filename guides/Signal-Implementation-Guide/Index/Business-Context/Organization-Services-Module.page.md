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
| {{pagelink:organization-profile}} | Provider (organization), Agency, State Agency, County, Location        | Represents a distinct place where services are offered, in hierarchical fashion; e.g. a provider agency is an organization with 1 or more provider locations which are also organizations (their relationship is recorded using the .partOf reference |
| {{pagelink:organizationaffiliation-profile}}  | --- | Create associations between participanting providers (locations) and the service provider where specified services are provided in 1 or more HealthcareService resource(s) |
| {{pagelink:healthcareservice-profile}}   | Program, Services, Service Categories, Procedure codes | Describes a single healthcare service or category of services that are provided by an organization at a location. The location of the services could be virtual, as with telemedicine services. |
| {{pagelink:location-profile}}                 | Region | Details and position information for a place where services are provided and resources and participants may be stored, found, contained, or accommodated. |
| {{pagelink:practitioner-profile}}                 | Clinician, provider (individual), physician, doctor, case manager, user | Practitioner covers all individuals who are engaged in the healthcare process and healthcare-related services as part of their formal responsibilities and this Resource is used for attribution of activities and responsibilities to these individuals. This will include both healthcare service staff and users of this system. |
| {{pagelink:practitionerrole-profile}}                 | --- | A specific set of Roles/Locations/specialties/services that a practitioner may perform at an organization for a period of time. |


## Conceptual Model

{{render:guides/Signal-Implementation-Guide/Index/assets/images/signal-org-services-module-2023-10-30.png}}

## Examples
(An example is intended to be illustrative of the relationship between resources but may not represent a completely accurate business process at the time the example was published.)

### Provider Agency, Provider Locations, Services example

Fabricated provider *Denver Medical* has a location called *Denver East* that has affiliations for both Signal and RMHC.  (see diagram below)
- Denver East has 2 qualifications with Colorado BHA (via LADDERS) which allows services ASAM-0.5 and CYMHTA Treatment which are also coded as qualifications via the administrator.
- Denver East's affiliation with Signal offers 2 services, ASAM-0.5 (via SUD) and Treatment (via CYMHTA), and this occurs in Signal's South region.
- Denver East's affiliation with RMHC offers 1 service, Treatment (via CYMHTA), and this occurs in RMHC's Mid-West region.


{{render:guides/Signal-Implementation-Guide/Index/assets/images/signal-org-services-module-example-2023-10-30.png}}
