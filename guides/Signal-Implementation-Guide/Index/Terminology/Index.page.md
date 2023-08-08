## {{page-title}}

### Background
The following coded values are used to describe administrative and clinical concepts within the FHIR elements to meet structural requirements of both the data model profiles and user interfaces.

Whenever possible, value sets and code systems were taken from the [US Core Terminology](https://hl7.org/fhir/us/core/terminology.html) and/or [FHIR Core Terminology](http://hl7.org/fhir/terminologies-valuesets.html) that were associated with the resources for interoperability.

#### Notes
- ValueSet resources in Signal's IG have been ["expanded"](https://www.hl7.org/fhir/valueset.html#expansion) utilizing the `ValueSet.expansion` element backbone. This is because Azure FHIR Service lacks a terminology server, so any value set that is not [extensional](https://www.hl7.org/fhir/valueset.html#int-ext), and UI developers require an enumerated lists of all values for display.
   - Expanded value sets retain their original Canonical URL if they are otherwise unmodified
   - Any changes to the original value set including adding or removing a code system, defining additional values, or removing values from the `.compose` element is considered a custom value set and will be noted below
- **\* (Asterisk) Denotes that these code systems an/or value sets have been modified or created for Signal.** 
   - An attempt was made to use a standards-based system whenever possible; e.g. ICD-10, LOINC< SNOMED, CPT, etc. to retain interoperability
   - Any custom values will be defined in a CodeSystem resource in addition to the ValueSet


### Value sets defined by this implementation guide

|Value Set|Description|Profile(s)|
|---|---|---|
| [AddressType](https://www.hl7.org/fhir/valueset-address-type.html) | The type of an address (physical / postal). | [**Organization** - Organization.address.type](Structure-Definition--Organization-Profile) <br /> [**Organization** - Organization.contact.address.type](Structure-Definition--Organization-Profile) |
| asdf | asdf | [**OrganizationAffiliation** - ](Structure-Definition--OrganizationAffiliation-Profile) <br /> |
| asdf | asdf | [**HealthcareService** - ](Structure-Definition--HealthcareService-Profile) <br /> |
| asdf | asdf | asdf |
| asdf | asdf | asdf |
| asdf | asdf | asdf |
| asdf | asdf | asdf |
| asdf | asdf | asdf |
| asdf | asdf | asdf |


### Other value set notes
[Procedure ValueSet](https://hl7.org/fhir/us/core/ValueSet-us-core-procedure-code.html) will include code systems from ICD, HCPCS, CPT, LOINC, Snomed.