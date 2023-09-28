---
topic: practitionerrole-profile
---

# {{page-title}}

Canonical URL: http://hl7.org/fhir/us/core/StructureDefinition/us-core-practitionerrole

Simplifier project page: Not Applicable

Derived from: [US Core PractitionerRole STU6 (R4)](https://hl7.org/fhir/us/core/StructureDefinition-us-core-practitionerrole.html)

Module:  {{pagelink:organization-services-module}}

---

## Formal profile content
<tabs>
	<tab title="Tree snapshot">
		{{tree:http://hl7.org/fhir/us/core/StructureDefinition/us-core-practitionerrole, snapshot}}
	</tab>
	<tab title="Tree, diff/hybrid/snapshot">
		{{tree:http://hl7.org/fhir/us/core/StructureDefinition/us-core-practitionerrole, buttons}}
	</tab>
	<tab title="JSON">
		{{json:http://hl7.org/fhir/us/core/StructureDefinition/us-core-practitionerrole,}}
	</tab>
</tabs>

## Profile usage

The PractionerRole resource profile is used to establish relationship(s) between a Practioner and Organization (and potentially location and healthcare services).  PractitionerRole will define both clinicians and system users differentiated by codes.

### Profile element notes

**.practitioner**
- Practitioner that is able to provide the defined services for the organization

**.organization**
- Organization where the roles are available

**.code**
- Roles which this practitioner may perform
- These will not reflect user system permissions, but rather defines the responsibility of the individual

**.specialty**
- *SHOULD* match the NPI specialty designation 

**.location**
- Currently not used
- May be used in the future to define in what region(s) the individual may perform work

## Examples

