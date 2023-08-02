## Administration, Clinical Categorization Module

** WIP as of 2023-06-20 **

For this specific implementation, a slight modification will be made to the [Clinical Categorization Resources in the Administration module](http://hl7.org/fhir/administration-module.html#clinical-reg):

- Admission defines a Parent (Top-level) Encounter resource that will record Admission and Discharge Dates.  Child (lower-level) Encounter resources will collect individual service codes/procedures during a stay.
- An EpisodeOfCare resource may also be defined and contain the top-level Encounter resource. (TBD)
- 

### Example resource utilization for distint Signal 'admission' scenario

A client (patient) is admitted into a care center for 3 days. During the stay, they receive an initial assessment, 2 therapy sessions, and are subsequently discharged from care.

```
EpisodeOfCare (TBD)
.
|-- Encounter A        - Admission/Discharge dates, entire stay
    |-- Encounter A1   - Assessment 
    |   └-- Procedure A1.1
    |-- Encounter A2   -  Therapy
    |   └-- Procedure A2.1
    |-- Encounter A3   - Therapy
    |   └-- Procedure A3.1
    └-- Encounter A4   - Discharge Procedure
        └-- Encounter A4.1   - QuestionnaireResponse Procedure
            └-- QuestionnaireResponse A4.1.1   - (exit survey)

```