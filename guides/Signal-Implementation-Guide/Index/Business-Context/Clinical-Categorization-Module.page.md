---
topic: clinical-categorization-module
---

# {{page-title}}

---

## Context
This is the administration module for clinical categorization.  It captures concepts the entire admission or case, individual services, surveys, and discharge events.

For this implementation, modifications will be made to the [Clinical Categorization Resources in the Administration module](http://hl7.org/fhir/administration-module.html#clinical-reg):

- Admission defines a Parent (top-level) `EpisodeOfCare` resource that will record Admission and Discharge Dates.
- `EspisodeOfCare` is loosely based on the service category, previously defined as _modality_.
- `Encounter` resources will be child (lower-level) pointing to a related `EpisodeOfCare` will collect individual service codes/procedures during a case.
- `Encounter` will also be created for each event or transaction including but not limited to admission, discharge, survey, notes, and more.

## FHIR Focus Resource Types

| Name                      | Aliases                                   | Description |
| --- | --- | --- |
| {{pagelink:episodeofcare-profile}}         | Admission, Case Program, Problem | --- |
| {{pagelink:encounter-profile}} | Visit | --- |
| {{pagelink:servicerequest-profile}}        | Referral | --- |
| {{pagelink:procedure-profile}}             | Service | --- |
| {{pagelink:simple-observation-profile}} | --- | --- |
| {{pagelink:condition-problems-profile}} | --- | For practitioner notes on encounter related to condition. Capture clinical concept that is documented and categorized as a problem or health concern including information about a Social Determinants of Health-related condition. |
| {{pagelink:condition-encounter-profile}} | --- | For encoutner diagnosis |
| {{pagelink:organization-profile}} | Provider, Agency, Location | --- |
| {{pagelink:patient-profile}} | Client | --- |
| {{pagelink:practitioner-profile}} | Clinician, doctor | Not currently used |
| {{pagelink:practitionerrole-profile}} | --- | Not currently used |
| {{pagelink:chargeitem-profile}} | --- | --- |
| {{pagelink:observation-screening-assessment-profile}} | Survey | --- |
| {{pagelink:questionnaire-profile}} | Survey (DACODS, CCAR) | --- |
| {{pagelink:questionnaireresponse-profile}} | Survey Response, Answers | --- |


## Conceptual Model

{{render:guides/Signal-Implementation-Guide/Index/assets/images/signal-clinical-module-2023-08-31.png}}

### Structured Screening and Assessments - Survey, Questionnaire, and Questionnaire Response

Following [HL7.FHIR.US.CORE\Screening and Assessments - FHIR v4.0.01](http://hl7.org/fhir/us/core/screening-and-assessments.html) guidance.
- US Core Observation Screening Assessment Profile
- SDC Base Questionnaire
- US Core QuestionnaireResponse Profile

## Examples


