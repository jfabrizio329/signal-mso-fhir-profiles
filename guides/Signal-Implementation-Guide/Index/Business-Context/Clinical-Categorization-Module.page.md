---
topic: {{page-title}}
---

# {{page-title}}

---

## Context
This is the administration module for clinical categorization.  It captures concepts the entire admission or case, individual services, surveys, and discharge events.

For this specific implementation, modifications will be made to the [Clinical Categorization Resources in the Administration module](http://hl7.org/fhir/administration-module.html#clinical-reg):

- Admission defines a Parent (Top-level) `EpisodeOfCare` resource that will record Admission and Discharge Dates.
- `EspisodeOfCare` is loosely based on the service category, previously defined as _modality_.
- `Encounter` resources will be child (lower-level) pointing to a related `EpisodeOfCare` will collect individual service codes/procedures during a case.
- `Encounter` will also be created for each event or transaction including but not limited to admission, discharge, survey, notes, and more.

## FHIR Focus Resource Types

| Name                      | Aliases                                   | Description |
| --- | --- | --- |
| [EpisodeOfCare](http://hl7.org/fhir/R4/episodeofcare.html)         | Admission, Case Program, Problem | --- |
| [Encounter](https://hl7.org/fhir/us/core/StructureDefinition-us-core-encounter.html)             | Visit | --- |
| [ServiceRequest](https://hl7.org/fhir/us/core/StructureDefinition-us-core-servicerequest.html)        | Referral | --- |
| [Procedure](https://hl7.org/fhir/us/core/StructureDefinition-us-core-procedure.html)             | Service | --- |
| [Observation Screening Assessment](https://hl7.org/fhir/us/core/StructureDefinition-us-core-observation-screening-assessment.html) | Survey | --- |
| [QuestionnaireResponse](https://hl7.org/fhir/us/core/StructureDefinition-us-core-questionnaireresponse.html) | Survey Response, Answers | --- |
| [Simple Observation](https://hl7.org/fhir/us/core/StructureDefinition-us-core-simple-observation.html) | --- | --- |
| [Condition Problems](https://hl7.org/fhir/us/core/StructureDefinition-us-core-condition-problems-health-concerns.html) | --- | For practitioner notes on encounter related to condition. Capture clinical concept that is documented and categorized as a problem or health concern including information about a Social Determinants of Health-related condition. |
| [Condition Encounter Diagnosis](https://hl7.org/fhir/us/core/StructureDefinition-us-core-condition-encounter-diagnosis.html) | --- | For encoutner diagnosis |
| [Organization](https://hl7.org/fhir/us/core/StructureDefinition-us-core-organization.html) | Provider, Agency, Location | --- |
| [Patient](https://hl7.org/fhir/us/core/StructureDefinition-us-core-patient.html) | Client | --- |
| [Practitioner](https://hl7.org/fhir/us/core/StructureDefinition-us-core-practitioner.html) | Clinician, doctor | --- |
| [ChargeItem](http://hl7.org/fhir/R4/chargeitem.html) | --- | --- |
| --- | --- | --- |

## Conceptual Model

![organization and services conceptual diagram](../assets/images/signal-admission-2023-08-02.png "Logo Title Text 1")


## Examples
