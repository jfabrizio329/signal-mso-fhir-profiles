---
topic: clinical-categorization-module
---

# {{page-title}}

---

## Context
This is the administration module for clinical categorization.  It captures concepts the entire admission or case, individual services, surveys, and discharge events.

## FHIR Focus Resource Types

| Name                      | Aliases                                   | Description |
| --- | --- | --- |
| {{pagelink:episodeofcare-profile}}         | Admission, case, program, problem, episode | An association between a patient and an organization / healthcare provider(s) during which time encounters may occur. The managing organization assumes a level of responsibility for the patient during this time. |
| {{pagelink:encounter-profile}} | Visit | An interaction between a patient and healthcare provider(s) for the purpose of providing healthcare service(s) or assessing the health status of a patient. |
| {{pagelink:servicerequest-profile}}        | Referral | A record of a request for service such as diagnostic investigations, treatments, or operations to be performed. |
| {{pagelink:procedure-profile}}             | Service, codes | An action that is or was performed on or for a patient, practitioner, device, organization, or location. |
| {{pagelink:simple-observation-profile}} | Clinical notes, notes | Measurements and simple assertions made about a patient, device or other subject. |
| {{pagelink:condition-problems-profile}} | Condition, problem, diagnosis | A clinical condition, problem, diagnosis, or other event, situation, issue, or clinical concept that has risen to a level of concern.  Used to query for a Patient’s current or historical problems and health concerns. |
| {{pagelink:condition-encounter-profile}} | Condition, problem, piagnosis | A clinical condition, problem, diagnosis, or other event, situation, issue, or clinical concept that has risen to a level of concern. Used for {{pagelink:encounter-profile}} diagnosis. |
| {{pagelink:organization-profile}} | Provider, Provider Agency, Provider Location | Organization providing services. <br /> See {{pagelink:organization-services-module}} |
| {{pagelink:patient-profile}} | Client | See {{pagelink:patient-administration-module}} |
| {{pagelink:practitioner-profile}} | Clinician, provider (individual) physician, doctor, nurse, user | See {{pagelink:organization-services-module}} |
| {{pagelink:practitionerrole-profile}} | --- | See {{pagelink:organization-services-module}} |
| {{pagelink:chargeitem-profile}} | --- | See {{pagelink:finance-module}} |
| {{pagelink:observation-screening-assessment-profile}} | Survey | Contains details on type of screening or assessment and results |
| {{pagelink:questionnaire-profile}} | Survey (e.g. DACODS, CCAR, etc.) | Contains questions asked on screening or assessment |
| {{pagelink:questionnaireresponse-profile}} | Survey response, answers | Contains answers for questions asked on screening or assessment |


## Conceptual Model

{{render:guides/Signal-Implementation-Guide/Index/assets/images/signal-clinical-categorization-module-2023-10-05.png}}

### Structured Screening and Assessments - Survey, Questionnaire, and Questionnaire Response

Following [HL7.FHIR.US.CORE\Screening and Assessments - FHIR v4.0.01](http://hl7.org/fhir/us/core/screening-and-assessments.html) guidance.  Using the following resources:
- {{pagelink:questionnaire-profile}}
- {{pagelink:questionnaireresponse-profile}}
- {{pagelink:observation-screening-assessment-profile}}

 In addition, we are utilizing the US Core Screening and Assessments guidance.

## Notes

### EpisodeOfCare and Encounters

Per [EpisodeOfCare Boundaries and Relationships](https://www.hl7.org/fhir/episodeofcare.html#bnr):
> The primary difference between the EpisodeOfCare and the Encounter is that the Encounter records the details of an activity directly relating to the patient, while the EpisodeOfCare is the container that can link a series of Encounters together for problems/issues.

For this implementation, modifications will be made to the [Clinical Categorization Resources in the Administration module](http://hl7.org/fhir/administration-module.html#clinical-reg):

- Admission defines a Parent (top-level) `EpisodeOfCare` resource that will record Admission and Discharge Dates.
- `EspisodeOfCare` is loosely based on the service category, previously defined as _modality_.
- `Encounter` resources will be child (lower-level) pointing to a related `EpisodeOfCare` will collect individual service codes/procedures during a case.
- `Encounter` will also be created for each event or transaction including but not limited to admission, discharge, survey, notes, and more.


## Examples

### Example 1 - Patient receives 2 weeks of therapy an is discharged
A patient is referred into or presents relevant healthcare issue(s), e.g., signs, symptoms, and defined conditions applicable to the Substance Use Disorder (SUD) program.  A {{pagelink:patient-profile, text:Patient}} and {{pagelink:episodeofcare-profile, text:EpisodeOfCare}} resource will be instantiated. When that patient is associated with a managing provider ({{pagelink:organization-profile, text:organization}}), the `EpisodeOfCare.managingOrganization` and `Patient.managingOrganization` SHALL be assigned to that organization.  

Day 1: The patient arrives at the provider location for assessment which requires a screening and urinary analysis.
- An Encounter is created for the overall assessment and a reasonReference is assocaited with the {{pagelink:procedure-profile, text:Procedure}}
- A reasonReference is assigned to the {{pagelink:observation-screening-assessment-profile, text:observation screening assessment}}
- `Encounter.length` is assigned a value based on the associated Procedure
- EITHER 
   - (Preferred) A new encounter is created for the urinary Procedure, assgined via reasonReference, with a reference in partOf pointing to the parent encounter
- OR
   - Another reasonReference is assigned to the urinary Procedure
- This establishes the first contact with the patient and `EpisodeOfCare.period.start` is assigned the same value as this `Encounter.period`
   - If the patient was a referral and already spoke to an agent, there may have been an Encounter for that conversation and that MAY be used as the first point of contact
- `Encounter.episodeOfCare` is assigned a reference to the top-level EpisodeOfCare for each encounter
- (WIP) `Encounter.account` references the Account with the main payer information.

Day 8: The patient returns to the provider location receive an in-peron therapy session.
- A new Encounter is created and has a reasonReference to a {{pagelink:procedure-profile, text:Procedure}} with the applicable code for the therapy session
- `Encounter.episodeOfCare` is assigned a reference to the top-level EpisodeOfCare
- A reasonReference is created linking to a {{pagelink:simple-observation-profile, text:simple observation}} with notes from the practitioner

Day 15: The patient returns to a different provider location with the same provider to receiving a therapy session and subsequently receives a discharge, which requires a discharge survey.
- A new Encounter is created and has a reasonReference to a {{pagelink:procedure-profile, text:Procedure}} with the applicable code for the therapy session
- `Encounter.episodeOfCare` is assigned a reference to the top-level EpisodeOfCare
- `Encounter.length` is assigned a value based on the associated Procedure
- EITHER
   - (Preferred) A new encounter is created for the discharge survey with a reasonReference assigned for discharge survey Procedure code AND a reasonReference assigned for the disarge observation screening assessment
- OR
   - Another reasonReference is assigned for the discharge survey Procedure AND a reasonReference assigned for the disarge observation screening assessment
- `EpisodeOfCare.period.end` is assigned the same values as this Encounter.period date and `EpisodeOfCare.status` is changed to `complete`

