---
topic: custom-terminology
---

# Custom Value sets

---

## Background

The following table contains code systems an/or value sets have been modified or created for Signal. 
- An attempt was made to use a standards-based, [external code systems](https://www.hl7.org/fhir/terminologies-systems.html#external) whenever possible; e.g. ICD-10, LOINC, SNOMED, CPT, etc. to retain interoperability.
- When possible, the original FHIR or US Core valueset binding was included in a custom ValueSet in order to maintain integrity and both codes may be used. 
- Any custom values will be defined in a CodeSystem resource in addition to the ValueSet.

## Signal custom value sets defined by this implementation guide

| Item Name | Value set Name |Value set URL | Binding Strength |
|---|---|---|---|
| Region    | valueset-signal-region.json | https://signalbhn.org/fhir/ValueSet/signal-region | Location.address.extension:signalRegion |
| State  | valueset-us-core-usps-state | http://hl7.org/fhir/us/core/ValueSet/us-core-usps-state | - |
| Taxonomy | valueset-provider-taxonomy | http://hl7.org/fhir/ValueSet/provider-taxonomy | PractitionerRole.specialty<br> Organization.type:npiTaxonomy |
| Program | valueset-signal-program | https://signalbhn.org/fhir/ValueSet/signal-program | HealthcareService.program <br>  EpisodeOfCare.type:program |
| classification  | valueset-signal-filerepo-classification | https://signalbhn.org/fhir/us/core/ValueSet/signal-filerepo-classification | DocumentReference.category |
| Gender | valueset-administrative-gender | http://hl7.org/fhir/ValueSet/administrative-gender | - |
| Gender identity | valeuset-2.16.840.1.113762.1.4.1021.32 | http://cts.nlm.nih.gov/fhir/ValueSet/2.16.840.1.113762.1.4.1021.32 | - |
| BirthSex | valueset-birthsex | http://hl7.org/fhir/us/core/ValueSet/birthsex | - |
| Ethnicity | valueset-omb-ethnicity-category | http://hl7.org/fhir/us/core/ValueSet/omb-ethnicity-category | - |
| Race | valueset-omb-race-category | http://hl7.org/fhir/us/core/ValueSet/omb-race-category | - |
| County | valueset-fips-county-co | https://signalbhn.org/fhir/ValueSet/fips-county-co | Patient.address.district <br> Location.address.district |
| Service | valueset-signal-healthcare-service-type | https://signalbhn.org/fhir/ValueSet/signal-healthcare-service-type | ServiceRequest.category:serviceType <br> HealthcareService.type:services <br> EpisodeOfCare.type <br> EpisodeOfCare.type:services <br> Encounter.serviceType |
| Place of service | valueset-place-of-service | https://signalbhn.org/fhir/ValueSet/place-of-service | Location.type |
| Procedure code | valueset-healthcare-service-procedure-code-cpt | https://signalbhn.org/fhir/ValueSet/healthcare-service-procedure-code-cpt | HealthcareService.type:procedure |
| Modifer | valueset-modifier | https://signalbhn.org/fhir/ValueSet/modifier | - |
| Reason for discharge | valueset-reason-for-discharge | https://signalbhn.org/fhir/ValueSet/reason-for-discharge | - |
| Organization License | valueset-signal-organization-license | https://signalbhn.org/fhir/ValueSet/signal-organization-license | Organization.extension:qualification.extension:code.value[x] |
|
