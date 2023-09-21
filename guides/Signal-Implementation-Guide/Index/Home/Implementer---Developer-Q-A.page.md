---
topic: implementer-developer-qa
---

# {{page-title}}

---

## How are programs stores in healthcare service and retrieved for an Organization?

Programs are the highest level of heath services and offerings available at Signal.  Programs determine the service types (formerly modalities), service categories, and procedures that may be performed.

Programs are contained in the [Signal Program ValueSet](http://signalbhn.org/fhir/ValueSet/signal-program) .  Programs are found on the following elements:
- HealthcareService.program
- EpisodeOfCare.reason(Reference HealthcareService) (TBD)

A Provider-location (Organization.participatingOrganization) has a relationship to a Service Organization (Organization.organization) using an OrganizationAffiliation resource.  
OrganizationAffiliation.healthcareService 0..* (HealthcareService) references all the offered programs, services, service categories, and procedure codes.  There will be 1 or many HealthcareService references, depending on the number of programs and services offered by the provider.
HealthcareService.program (Signal MSO FHIR Profiles | SignalProgram - SIMPLIFIER.NET) contains the applicable programs. 

See the {{pagelink:Index/Business-Context/Organization-Services-Module.page.md}} for more information.

## What is the difference between EpisodeOfCare and Encounter?

See {{pagelink:clinical-categorization-module}} notes and examples sections.