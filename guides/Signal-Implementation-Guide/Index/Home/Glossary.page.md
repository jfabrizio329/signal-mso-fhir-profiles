---
topic: glossary
---

# {{page-title}}

---
# FHIR focus elements to business terms
The following describes Signal-specific aliases and definitions and how they align to FHIR resources.  US Core profiles shall be used where they exist:

|Signal term|FHIR resource|Notes|
|--- | --- | ---|
|Client|Patient|Individual receiving services|
|Provider|Organization, OrganizationAffiliation, Location|Provider refers to the county-provider.|
|Admission|EpisodeOfCare, Encounter|Includes admission/discharge dates, modalities, payers. <br /> EpisodeOfCare defined for type of service (prev. modality) <br />May have nested encounters for services during stay|
|Contract / Funding Agreement|Contract| Includes agreed-upon pricing/rates for procedure codes between a service organization and provider agency and/or location |
|Payer/Payor / Payer Account|Organization|Will reference as part of another Organization|
|Clinician|Practitioner, PractitionerRole|Individual providing services to a patient. May or may not be directly related to the provider|
|Referral|Organization|Match to different provider/organization|
|Service Codes|Procedure, HealthServices|Capture services rendered in Procedures. <br /> Services available in HealthServices|
|Modality|Organization.qualification, HealthServices, Service Type |ASAM levels will be defined under Organization.qualification|
|Survey|Observation (Screening Assessment) Questionnaire, QuestionnaireResponse|Includes DACODS and CCAR surveys results (Questionnaire/Survey is simply linked to relevant manual) <br /> linked to Encounter|

# Terms, Acronyms, and Abbreviations

|Term/Acronym/Abbreviation|Description|
|--- | --- |
| FHIR | [HL7 Fast Healthcare Interoperability Resources Standard](http://hl7.org/fhir/) |
| HL7 | [Health Level Seven](http://www.hl7.org/) |
| asdf | asdf |
| asdf | asdf |
| asdf | asdf |
| asdf | asdf |
| asdf | asdf |
| asdf | asdf |
| asdf | asdf |
| asdf | asdf |
