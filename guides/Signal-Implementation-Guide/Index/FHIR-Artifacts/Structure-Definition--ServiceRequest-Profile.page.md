---
topic: servicerequest-profile
---

# {{page-title}}

---

Canonical URL: https://signalbhn.org/fhir/StructureDefinition/servicerequest

Simplifier project page: [ServiceRequest](https://simplifier.net/signal-mso-fhir-profiles/signalservicerequest)

Derived from: [US Core ServiceRequest STU6 (R4)](https://hl7.org/fhir/us/core/StructureDefinition-us-core-servicerequest.html)

Module:  {{pagelink:Clinical-Categorization-Module}}

---

## Formal profile content
<tabs>
	<tab title="Tree snapshot">
		{{tree:https://signalbhn.org/fhir/StructureDefinition/servicerequest, snapshot}}
	</tab>
	<tab title="Tree, diff/hybrid/snapshot">
		{{tree:https://signalbhn.org/fhir/StructureDefinition/servicerequest, buttons}}
	</tab>
	<tab title="JSON">
		{{json:https://signalbhn.org/fhir/StructureDefinition/servicerequest,}}
	</tab>
</tabs>

## Profile usage

Record of request (referral) for a procedure or service to be planned, proposed, or performed on a patient. This will come directly from the referral system of record, Jolata, and will include only necessary details for handling the service in FHIR.

Jolata will be used as the system of record (source) that will maintain referral details. Any updates on the system of record will cascade down to the associated FHIR resources. No new information specific to the referral should be stored in FHIR.

### Profile element notes

**.category:serviceCategory**
- Signal custom service category classification (type of service to be performed).

## Examples

