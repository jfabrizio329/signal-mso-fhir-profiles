---
topic: questionnaire-terminology
---

# Survey Questionnaires Value sets

---

## Background

The following table contains value sets, which is created for Signal's Survey Questionnaires (Admission & Discharge).
- All the requirement for Survey questionnaires are framed as value sets, which follows a simple and standardized JSON Structure.
- For the Survey Questionnaires, FHIR or US Core valueset binding is not required. 
- Survey Questionnaires will be defined in a CodeSystem resource in addition to the ValueSet.

## Survey Questionnaire value sets defined by this implementation guide

| System | Survey Name | Type | Value name | Value Set URL |
|---|---|---|---|---|
| DACODS | Sexual Orientation | Admission | valueset-questionnaire-dacods-sexual-orientation | https://signalbhn.org/fhir/ValueSet/questionnaire-dacods-sexual-orientation |
| DACODS | Marital Status | Admission | valueset-questionnaire-dacods-marital-status | https://signalbhn.org/fhir/ValueSet/questionnaire-dacods-marital-status  |
| DACODS | Living Situation | Admission & Discharge | valueset-questionnaire-dacods-living-situation | https://signalbhn.org/fhir/ValueSet/questionnaire-dacods-living-situation |
| DACODS | Disability Status | Admission | valueset-questionnaire-dacods-disability-status | https://signalbhn.org/fhir/ValueSet/questionnaire-dacods-client-disability |
| DACODS | Employment Status | Admission & Discharge | valueset-questionnaire-dacods-employment-status | https://signalbhn.org/fhir/ValueSet/questionnaire-dacods-employment-status |
| DACODS | Transfer or referral source | Admission | valueset-questionnaire-dacods-transfer-referral-source | https://signalbhn.org/fhir/ValueSet/questionnaire-dacods-transfer-referral-source |
| DACODS | Family issues and problems | Admission & Discharge | valueset-questionnaire-dacods-family-issues-and-problems | https://signalbhn.org/fhir/ValueSet/questionnaire-dacods-family-issues-and-problems |
| DACODS | Socialization Problems | Admission & Discharge | valueset-questionnaire-dacods-socialization-problems | https://signalbhn.org/fhir/ValueSet/questionnaire-dacods-socialization-problems |
| DACODS | Education Employment Problems | Admission & Discharge | valueset-questionnaire-dacods-education-employment-problems | https://signalbhn.org/fhir/ValueSet/questionnaire-dacods-education-employment-problems |
| DACODS | Medical Physical Problems | Admission & Discharge | valueset-questionnaire-dacods-medical-physical-problems | https://signalbhn.org/fhir/ValueSet/questionnaire-dacods-medical-physical-problems |
| DACODS | Primary drug clinician diagnostic impression | Admission | valueset-questionnaire-dacods-clinician-diagnostic-impression | https://signalbhn.org/fhir/ValueSet/questionnaire-dacods-clinician-diagnostic-impression |
| DACODS | Secondary drug clinician diagnostic impression | Admission | valueset-questionnaire-dacods-clinician-diagnostic-impression | https://signalbhn.org/fhir/ValueSet/questionnaire-dacods-clinician-diagnostic-impression |
| DACODS | Tertiary drug clinician diagnostic impression | Admission | valueset-questionnaire-dacods-clinician-diagnostic-impression | https://signalbhn.org/fhir/ValueSet/questionnaire-dacods-clinician-diagnostic-impression |
| DACODS | Admission Primary Route of Administration | Admission | valueset-questionnaire-admission-dacods-route-of-administration | https://signalbhn.org/fhir/ValueSet/questionnaire-dacods-admission-route-of-administration |
| DACODS | Admission Secondary Drug Route of Administration | Admission | valueset-questionnaire-admission-dacods-route-of-administration | https://signalbhn.org/fhir/ValueSet/questionnaire-dacods-admission-route-of-administration |
| DACODS | Tertiary drug route of administration | Admission | valueset-questionnaire-admission-dacods-route-of-administration | https://signalbhn.org/fhir/ValueSet/questionnaire-dacods-admission-route-of-administration |
| DACODS | Source of illicit drugs | Admission | valueset-questionnaire-dacods-source-of-illicit-drugs | https://signalbhn.org/fhir/ValueSet/questionnaire-dacods-source-of-illicit-drugs |
| DACODS | Tobacco use | Admission | valueset-questionnaire-dacods-toabacco-use | https://signalbhn.org/fhir/ValueSet/questionnaire-dacods-tobacco-use |
| DACODS | Statutory Commitment | Admission & Discharge | valueset-questionnaire-dacods-statutory-commitment | https://signalbhn.org/fhir/ValueSet/questionnaire-dacods-statutory-commitment |
| DACODS | Health insurance status | Admission | valueset-questionnaire-dacods-health-insurance-status | https://signalbhn.org/fhir/ValueSet/questionnaire-dacods-health-insurance-status |
| DACODS | Source of income | Admission | valueset-questionnaire-dacods-source-of-income | https://signalbhn.org/fhir/ValueSet/questionnaire-dacods-source-of-income |
| DACODS | Source of payment for treatment | Admission | valueset-questionnaire-dacods-source-of-payment-for-treatment | https://signalbhn.org/fhir/ValueSet/questionnaire-dacods-source-of-payment-for-treatment |
| DACODS | Primary Drug Type Code | Admission & Discharge | valueset-questionnaire-dacods-drug-type-code | https://signalbhn.org/fhir/ValueSet/questionnaire-dacods-drug-type-code |
| DACODS | Secondary Drug Type | Admission & Discharge | valueset-questionnaire-dacods-secondary-tertiary-drug-type-code | https://signalbhn.org/fhir/ValueSet/questionnaire-dacods-secondary-tertiary-drug-type-code |
| DACODS | Tertiary Drug Type | Admission & Discharge | valueset-questionnaire-dacods-secondary-tertiary-drug-type-code | https://signalbhn.org/fhir/ValueSet/questionnaire-dacods-secondary-tertiary-drug-type-code |
| DACODS | Yes or No | Admission & Discharge | valueset-questionnaire-dacods-yes-no | https://signalbhn.org/fhir/ValueSet/questionnaire-dacods-yes-no |
| DACODS | Yes or No or NA | Admission & Discharge | valueset-questionnaire-dacods-yes-no-na | https://signalbhn.org/fhir/ValueSet/questionnaire-dacods-yes-no-na |
| DACODS | Yes or No or Unknown | Admission & Discharge | valueset-questionnaire-dacods-yes-no-unknown | https://signalbhn.org/fhir/ValueSet/questionnaire-dacods-yes-no-unknown |
| DACODS | Yes or No or Unable to assess | Admission & Discharge | valueset-questionnaire-dacods-yes-no-unable-to-assess | https://signalbhn.org/fhir/ValueSet/questionnaire-dacods-yes-no-unable-to-assess |
| DACODS | Primary route of administration | Discharge | valueset-questionnaire-dacods-discharge-route-of-administration | https://signalbhn.org/fhir/ValueSet/questionnaire-dacods-discharge-route-of-administration |
| DACODS | Secondary route of administration | Discharge | valueset-questionnaire-dacods-discharge-route-of-administration | https://signalbhn.org/fhir/ValueSet/questionnaire-dacods-discharge-route-of-administration |
| DACODS | Tertiary route of administration | Discharge | valueset-questionnaire-dacods-discharge-route-of-administration | https://signalbhn.org/fhir/ValueSet/questionnaire-dacods-discharge-route-of-administration |
| DACODS | Discharge Status | Discharge | valueset-questionnaire-dacods-discharge-status | https://signalbhn.org/fhir/ValueSet/questionnaire-dacods-discharge-status |
| DACODS | Reason for Discharge | Discharge | valueset-questionnaire-dacods-reason-for-discharge | https://signalbhn.org/fhir/ValueSet/questionnaire-dacods-reason-for-discharge |
| DACODS | Progress towards measurable treatment goals | Discharge | valueset-questionnaire-dacods-discharge-progress-treatment-goals | https://signalbhn.org/fhir/ValueSet/questionnaire-dacods-discharge-progress-towards-measurable-treatment-goals |
| CCARS |  RAE ASO Identification Codes | Admission & Discharge | valueset-questionnaire-ccars-rae-aso-identification-codes | https://signalbhn.org/fhir/ValueSet/questionnaire-ccars-rae-aso-identification-codes |
| CCARS |  CCARS Yes No | Admission & Discharge | valueset-questionnaire-ccars-yes-no | https://signalbhn.org/fhir/ValueSet/questionnaire-ccars-yes-no |
| CCARS |  Enrollment Payer | Admission & Discharge | valueset-questionnaire-ccars-enrollment-payer | https://signalbhn.org/fhir/ValueSet/questionnaire-ccars-enrollment-payer |
| CCARS |  Action Types | Admission & Discharge | valueset-questionnaire-ccars-action-types | https://signalbhn.org/fhir/ValueSet/questionnaire-ccars-action-types |
| CCARS |  Type Of Update | -- | valueset-questionnaire-ccars-type-of-update | https://signalbhn.org/fhir/ValueSet/questionnaire-ccars-type-of-update |
| CCARS |  Medication/Psychiatric Service | Admission & Discharge | valueset-questionnaire-ccars-medication-psychiatric-service | https://signalbhn.org/fhir/ValueSet/questionnaire-ccars-medication-psychiatric-service |
| CCARS |  Ethnicity | Admission & Discharge | valueset-questionnaire-ccars-ethnicity | https://signalbhn.org/fhir/ValueSet/questionnaire-ccars-ethnicity |
| CCARS |  Race | Admission & Discharge | valueset-questionnaire-ccars-race | https://signalbhn.org/fhir/ValueSet/questionnaire-ccars-race |
| CCARS |  Type Of Discharge | Discharge | valuset-questionnaire-ccars-type-of-discharge | https://signalbhn.org/fhir/ValueSet/questionnaire-ccars-type-of-discharge |
| CCARS |  Highest Education Level | Admission & Discharge | valueset-questionnaire-ccars-highest-education-level | https://signalbhn.org/fhir/ValueSet/questionnaire-ccars-highest-education-level |
| CCARS |  Marital Status | Admission & Discharge | valueset-ccars-marital-status | https://signalbhn.org/fhir/ValueSet/questionnaire-ccars-marital-status |
| CCARS |  Current Primary Role | Admission & Discharge | valueset-questionnaire-ccars-current-primary-role | https://signalbhn.org/fhir/ValueSet/questionnaire-ccars-current-primary-role |
| CCARS |  Place Of Residence | Admission & Discharge | valueset-questionnaire-ccars-place-of-residence | https://signalbhn.org/fhir/ValueSet/questionnaire-ccars-place-of-residence |
| CCARS |  Current Living Arrangement | Admission & Discharge | valueset-questionnaire-ccars-current-living-arrangement | https://signalbhn.org/fhir/ValueSet/questionnaire-ccars-current-living-arrangement |
| CCARS |  Existence Presenting Problem | Admission & Discharge | valueset-questionnaire-ccars-existence-presenting-problem | https://signalbhn.org/fhir/ValueSet/questionnaire-ccars-existence-presenting-problem |
| CCARS |  Disabilities | Admission & Discharge | valueset-questionnaire-ccars-disabilities | https://signalbhn.org/fhir/ValueSet/questionnaire-ccars-disabilities |
| CCARS |  Legal Status | Admission & Discharge | valueset-questionnaire-ccars-legal-status | https://signalbhn.org/fhir/ValueSet/questionnaire-ccars-legal-status |
| CCARS |  Considerations For Providers | Admission & Discharge | valueset-questionnaire-ccars-considerations-for-providers | https://signalbhn.org/fhir/ValueSet/questionnaire-ccars-considerations-for-providers |
| CCARS |  History Of Issues | Admission & Discharge | valueset-questionnaire-ccars-history-of-issues | https://signalbhn.org/fhir/ValueSet/questionnaire-ccars-history-of-issues |
| CCARS |  Current Issues | Admission & Discharge | valueset-questionnaire-ccars-current-issues | https://signalbhn.org/fhir/ValueSet/questionnaire-ccars-current-issues |
| CCARS |  School Problems | Admission & Discharge | valueset-questionnaire-ccars-school-problems | https://signalbhn.org/fhir/ValueSet/questionnaire-ccars-school-problems |
| CCARS |  School Development | Admission & Discharge | valueset-questionnaire-ccars-school-development | https://signalbhn.org/fhir/ValueSet/questionnaire-ccars-school-development |
| CCARS |  History Current Victimization | Admission & Discharge | valueset-questionnaire-ccars-history-current-victimization | https://signalbhn.org/fhir/ValueSet/questionnaire-ccars-history-current-victimization |
| CCARS |  History Of Mental Health Services | Admission & Discharge | valueset-questionnaire-ccars-history-of-mental-health-services | https://signalbhn.org/fhir/ValueSet/questionnaire-ccars-history-of-mental-health-services |
| CCARS |  Previous Concurrent Services | Admission & Discharge | valueset-questionnaire-ccars-previous-concurrent-services | https://signalbhn.org/fhir/ValueSet/questionnaire-ccars-previous-concurrent-services |
| CCARS |  Current Non-Prescription Substance Use | -- | valueset-questionnaire-ccars-current-non-prescription-substance-use | https://signalbhn.org/fhir/ValueSet/questionnaire-ccars-current-non-prescription-substance-use |
| CCARS |  Gender | Admission & Discharge | questionnaire-ccars-gender | https://signalbhn.org/fhir/ValueSet/questionnaire-ccars-gender |
| CCARS |  Physical Health Rating | Admission & Discharge | valueset-questionnaire-ccars-physical-health-rating | https://signalbhn.org/fhir/ValueSet/questionnaire-ccars-physical-health-rating |
| CCARS |  Self Care Basic Needs Rating | Admission & Discharge | valueset-questionnaire-ccars-self-care-basic-needs-rating | https://signalbhn.org/fhir/ValueSet/questionnaire-ccars-self-care-basic-needs-rating |
| CCARS |  Legal Rating | Admission & Discharge | valueset-questionnaire-ccars-legal-rating | https://signalbhn.org/fhir/ValueSet/questionnaire-ccars-legal-rating |
| CCARS |  Security Supervision Rating | Admission & Discharge | valueset-questionnaire-ccars-security-supervision-rating | https://signalbhn.org/fhir/ValueSet/questionnaire-ccars-security-supervision-rating |
| CCARS |  Suicide Danger To Self Rating | Admission & Discharge | valueset-questionnaire-ccars-suicide-danger-to-self-rating | https://signalbhn.org/fhir/ValueSet/questionnaire-ccars-suicide-danger-to-self-rating |
| CCARS |  Aggression Danger To Others Rating | Admission & Discharge | valueset-questionnaire-ccars-aggression-danger-to-others-rating | https://signalbhn.org/fhir/ValueSet/questionnaire-ccars-aggression-danger-to-others-rating |
| CCARS |  Psychosis Rating | Admission & Discharge | valueset-questionnaire-ccars-psychosis-rating | https://signalbhn.org/fhir/ValueSet/questionnaire-ccars-psychosis-rating |
| CCARS |  Cognition Rating | Admission & Discharge | valueset-questionnaire-ccars-cognition-rating | https://signalbhn.org/fhir/ValueSet/questionnaire-ccars-cognition-rating |
| CCARS |  Attention Rating | Admission & Discharge | valueset-questionnaire-ccars-multiple-issues-rating | https://signalbhn.org/fhir/ValueSet/questionnaire-ccars-multiple-issues-rating |
| CCARS |  Manic Issues Rating | Admission & Discharge | valueset-questionnaire-ccars-multiple-issues-rating | https://signalbhn.org/fhir/ValueSet/questionnaire-ccars-multiple-issues-rating |
| CCARS |  Anxiety Issues Rating | Admission & Discharge | valueset-questionnaire-ccars-multiple-issues-rating | https://signalbhn.org/fhir/ValueSet/questionnaire-ccars-multiple-issues-rating |
| CCARS |  Depressive Issues Rating | Admission & Discharge | valueset-questionnaire-ccars-depressive-issues-rating | https://signalbhn.org/fhir/ValueSet/questionnaire-ccars-depressive-issues-rating |
| CCARS |  Alcohol Use Rating | Admission & Discharge | valueset-questionnaire-ccars-alcohol-use-rating | https://signalbhn.org/fhir/ValueSet/questionnaire-ccars-alcohol-use-rating |
| CCARS |  Drug Use Rating | Admission & Discharge | valueset-questionnaire-ccars-drug-use-rating | https://signalbhn.org/fhir/ValueSet/questionnaire-ccars-drug-use-rating |
| CCARS |  Family Rating | Admission & Discharge | valueset-questionnaire-ccars-family-rating | https://signalbhn.org/fhir/ValueSet/questionnaire-ccars-family-rating |
| CCARS |  Interpersonal Rating | Admission & Discharge | valueset-questionnaire-ccars-interpersonal-rating | https://signalbhn.org/fhir/ValueSet/questionnaire-ccars-interpersonal-rating |
| CCARS |  Socialization Rating | Admission & Discharge | valueset-questionnaire-ccars-socialization-rating | https://signalbhn.org/fhir/ValueSet/questionnaire-ccars-socialization-rating |
| CCARS |  Role Performance Rating | Admission & Discharge | valueset-questionnaire-ccars-role-performance-rating | https://signalbhn.org/fhir/ValueSet/questionnaire-ccars-role-performance-rating |
| CCARS |  Social Support Rating | Admission & Discharge | valueset-questionnaire-ccars-social-support-rating | https://signalbhn.org/fhir/ValueSet/questionnaire-ccars-social-support-rating |
| CCARS |  Hope Rating | Admission & Discharge | valueset-questionnaire-ccars-hope-rating | https://signalbhn.org/fhir/ValueSet/questionnaire-ccars-hope-rating |
| CCARS |  Empowerment Rating | Admission & Discharge | valueset-questionnaire-ccars-empowerment-rating | https://signalbhn.org/fhir/ValueSet/questionnaire-ccars-empowerment-rating |
| CCARS |  Overall Activity Involvement Rating | Admission & Discharge | valueset-questionnaire-ccars-activity-involvement-rating | https://signalbhn.org/fhir/ValueSet/questionnaire-ccars-activity-involvement-rating |
| CCARS |  Overall Recovery Rating | Admission & Discharge | valueset-questionnaire-ccars-overall-recovery-rating | https://signalbhn.org/fhir/ValueSet/questionnaire-ccars-overall-recovery-rating |
| CCARS |  Overall Level Of Functioning Rating | Admission & Discharge | valueset-questionnaire-ccars-overall-level-of-functioning-rating | https://signalbhn.org/fhir/ValueSet/questionnaire-ccars-overall-level-of-functioning-rating |
| CCARS |  CCARS Sexual Orientation | Admission & Discharge | valeuset-questionnaire-ccars-sexual-orientation | https://signalbhn.org/fhir/ValueSet/questionnaire-ccars-sexual-orientation |
| CCARS |  Reason For Discharge | Discharge | valueset-questionnaire-ccars-reason-for-discharge | https://signalbhn.org/fhir/ValueSet/questionnaire-ccars-reason-for-discharge |
| CCARS |  Tobacco Use | Admission & Discharge | valueset-questionnaire-ccars-tobacco-use | https://signalbhn.org/fhir/ValueSet/questionnaire-ccars-tobacco-use |
| CCARS |  CCARS Yes No Unable To Assess | Admission & Discharge | valueset-questionnaire-ccars-yes-no-unable-to-assess | https://signalbhn.org/fhir/ValueSet/questionnaire-ccars-yes-no-unable-to-assess |
| CCARS |  Criteria (Mental Health Services Program) | Admission & Discharge | valueset-questionnaire-ccars-mental-health-services-program | https://signalbhn.org/fhir/ValueSet/questionnaire-ccars-mental-health-services-program |
| CCARS |  Overall Symptom Severity Rating | Admission & Discharge | valueset-questionnaire-ccars-overall-symptom-severity-rating | https://signalbhn.org/fhir/ValueSet/questionnaire-ccars-overall-symptom-severity-rating |
|