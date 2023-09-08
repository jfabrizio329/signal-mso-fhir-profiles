---
topic: {{page-title}}
---

# {{page-title}}

---

Canonical URL: https://signalbhn.org/fhir/StructureDefinition/Location

Simplifier project page: [Location](https://simplifier.net/signal-mso-fhir-profiles/locationprofile)

Derived from: [US Core Organization STU6 (R4)](http://hl7.org/fhir/us/core/STU6/StructureDefinition-us-core-location.html)

Module:  {{pagelink:Organization-Services-Module}}

---

## Formal profile content
<tabs>
	<tab title="Tree snapshot">
		{{tree:https://signalbhn.org/fhir/StructureDefinition/Location, snapshot}}
	</tab>
	<tab title="Tree, diff/hybrid/snapshot">
		{{tree:https://signalbhn.org/fhir/StructureDefinition/Location, buttons}}
	</tab>
	<tab title="JSON">
		{{json:https://signalbhn.org/fhir/StructureDefinition/Location,}}
	</tab>
</tabs>

## Profile usage

The Location resource is used to provide supporting fact information to other resources, including re-usable concepts such as service regions.  This resource may also be used as linkage between organization and location using HealthcareService that says "this service at this organization at this site (possibly scoped by time)".

### Profile element notes

**.type**
- *FUTURE* - will want to include [CMS Place of Service](https://www.cms.gov/Medicare/Coding/place-of-service-codes/Place_of_Service_Code_Set.html), which is in https://www.hl7.org/fhir/valueset-service-place.html.  May need to add it to the existing set.

## Examples

