---
topic: practitioner-profile
---

# {{page-title}}

---

Canonical URL: http://hl7.org/fhir/us/core/StructureDefinition/us-core-practitioner

Simplifier project page: Not Applicable

Derived from: [US Core Practitioner STU6 (R4)](https://hl7.org/fhir/us/core/StructureDefinition-us-core-practitioner.html)

Module:  {{pagelink:organization-services-module}}

---

## Formal profile content
<tabs>
	<tab title="Tree snapshot">
		{{tree:http://hl7.org/fhir/us/core/StructureDefinition/us-core-practitioner, snapshot}}
	</tab>
	<tab title="Tree, diff/hybrid/snapshot">
		{{tree:http://hl7.org/fhir/us/core/StructureDefinition/us-core-practitioner, buttons}}
	</tab>
	<tab title="JSON">
		{{json:http://hl7.org/fhir/us/core/StructureDefinition/us-core-practitioner,}}
	</tab>
</tabs>

## Profile usage

The Practitioner resource will be used to store both healthcare provider (clinician) information as well as system user information.  Every resource will be attached to an organiation via a {{pagelink:practitionerrole-profile}}.

### Profile element notes

**.identifier:NPI**
- 10-digit identifier for the person as this agent

**.name**
- The name(s) associated with the practitioner 

## Examples

