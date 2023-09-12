---
topic: patient-profile
---

# {{page-title}}

---

Canonical URL: https://signalbhn.org/fhir/StructureDefinition/patient

Simplifier project page: [Patient](https://simplifier.net/signal-mso-fhir-profiles/patientprofile)

Derived from: [US Core Patient STU6 (R4)](https://hl7.org/fhir/us/core/StructureDefinition-us-core-patient.html)

Module:  {{pagelink:Patient-Administration-Module}}

---

## Formal profile content
<tabs>
	<tab title="Tree snapshot">
		{{tree:http://signalbhn.org/fhir/StructureDefinition/patient, snapshot}}
	</tab>
	<tab title="Tree, diff/hybrid/snapshot">
		{{tree:http://signalbhn.org/fhir/StructureDefinition/patient, buttons}}
	</tab>
	<tab title="JSON">
		{{json:http://signalbhn.org/fhir/StructureDefinition/patient,}}
	</tab>
</tabs>

## Profile usage

The Organization resource is used to collect basic demographic and administrative information on individual patients that are receiving services.  It is designed to be specific to each provider organization (utilizing the `manageingOrganization` element.

### Profile element notes

**.managingOrganization**
- SHALL reference the provider agency from whom the patient record was entered
- The patient record SHOULD be available to all locations in the Organization.partOf hierarchy

**.identifier:SSN**
- Contains the Social Security Number for the patient, if available
- Fixed values are created for the associated codeable concepts

**.identifier:MedicaidID**
- Contains the Medicaid ID for the patient, if available
- Fixed values are created for the associated codeable concepts
- No assumption is made as to the state associated for the Medicaid ID; to accomodate this, `.system` is set as a fixed value to `https://signalbhn.org/fhir/sid/us-medicaidid`

**.identifier:MedicareID**
- Contains the Medicaid ID for the patient, if available
- Fixed values are created for the associated codeable concepts
- Note, this includes only the Medicare ID, information on benefits is contained on the Coverage resource

~~**.identifier:ProviderClientID**~~
- Contains any of the Provider's ID(s) for the patient
- Note, the `system` element needs to be entered as the URL to that Provider's domain; e.g. https://example.org to be linked to the proper provider identity

**.identifier:ClientID**
- Contains the carryover identifiers for the patient from Signal's Beacon system

**.adoptionInfo** (extension) - `Patient.extension:adoptionInfo`
- Utilized for specific programs
- If present, a fixed value representing the SNOWMED code for "Adopted" is supplied in the `Extension.value[x]:valueCodeableConcept`
- `Extension.value[x]:valueDate` represents the adoption date and is required when adoption is used.

**.address.noFixedAddress** (extension) - `Patient.address.extension:noFixedAddress`
- The No Fixed Address indictor, when present, will be assigned a fixed boolean value of `true` on `Extension.value[x]:valueBoolean`
- The No Fixed Address indicator SHALL take priority for administrative purposes, even if some other address fields contain information

**.address.district** - `Patient.address.district`
- Contains a ValueSet binding for Colorado counties using FIPs code plus Other

## Examples

