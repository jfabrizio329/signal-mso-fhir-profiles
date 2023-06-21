## {{page-title}}
The following describes Signal-specific aliases and definitions and how they align to FHIR resources.  US Core profiles shall be used where they exist:

|Signal term|FHIR resource|Notes|
|--- | --- | ---|
|Client|Patient|Individual receiving services|
|Provider|Organization, Location|Provider refers to the county-provider.|
|Admission|Encounter, EpisodeOfCare|Includes admission/discharge dates, modalities, payers. <br /> May have nested encounters for services during stay|
|Contract / Funding Agreement|Contract||
|Payer/Payor / Payer Account|Organization|Will reference as part of another Organization|
|Clinician|Practitioner, PractitionerRole|data13|
|Referral|Organization|Match to different provider/organization|
|Service Codes|Procedure, HealthServices|Capture services rendered in Procedures. <br /> Services available in HealthServices|
|Modality|Organization.qualification, HealthServices|ASAM levels will be defined under Organization.qualification|
|Survey|QuestionnaireResponse|Includes DACODS and CCAR surveys results (Questionnaire/Survey is simply linked to relevant manual)|
