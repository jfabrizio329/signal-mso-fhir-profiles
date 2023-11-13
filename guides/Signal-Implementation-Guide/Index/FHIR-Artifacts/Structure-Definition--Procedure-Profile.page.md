---
topic: procedure-profile
---

# {{page-title}}

Canonical URL: http://hl7.org/fhir/us/core/StructureDefinition/us-core-procedure

Simplifier project page: Not Applicable

Derived from: [US Core Procedure STU6 (R4)](https://hl7.org/fhir/us/core/StructureDefinition-us-core-procedure.html)

Module:  {{pagelink:Clinical-Categorization-Module}}

---

## Formal profile content
<tabs>
	<tab title="Tree snapshot">
		{{tree:http://hl7.org/fhir/us/core/StructureDefinition/us-core-procedure, snapshot}}
	</tab>
	<tab title="Tree, diff/hybrid/snapshot">
		{{tree:http://hl7.org/fhir/us/core/StructureDefinition/us-core-procedure, buttons}}
	</tab>
	<tab title="JSON">
		{{json:http://hl7.org/fhir/us/core/StructureDefinition/us-core-procedure,}}
	</tab>
</tabs>

## Profile usage

- `Encounter.type` SHOULD be preferentially used to capture billable codes on the encounter (see {{pagelink:encounter-profile}} for more information).
- Procedure MAY be used to capture specific service codes and additional information for each encounter (resource and business definition) that have explicit billable codes.  

Per [FHIR Encounter Scope and Usage](http://hl7.org/fhir/R5/procedure.html#scope): 
> This resource is used to record the details of current and historical procedures performed on, with, or for a patient, practitioner, device, organization, or location. Examples include surgical procedures, diagnostic procedures, endoscopic procedures, biopsies, counseling, physiotherapy, personal support services, adult day care services, non-emergency transportation, home modification, exercise, verification of enrollment qualifications for a social program etc. Procedures may be performed by a healthcare professional, a service provider, a friend or relative or in some cases by the patient themselves.

### Profile element notes

**.encounter**
- SHOULD be populated with the encounter when this procedure was performed

**.performed[x].performedDateTime**
- SHOULD be used to represent when procedure took place
- SHALL NOT be used for billing purposes.  See {{pagelink:finance-module}} for more information.

## Examples

