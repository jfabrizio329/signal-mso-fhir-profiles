---
topic: healthcareservice-profile
---

# {{page-title}}

---

Canonical URL: https://signalbhn.org/fhir/StructureDefinition/healthcareservice

Simplifier project page: https://simplifier.net/signal-mso-fhir-profiles/signalhealthcareservice

Derived from: [HealthcareService (R4)](http://hl7.org/fhir/R4/healthcareservice.html)

Module:  {{pagelink:Organization-Services-Module}}

---

## Formal profile content
<tabs>
	<tab title="Tree snapshot">
		{{tree:https://signalbhn.org/fhir/StructureDefinition/healthcareservice, snapshot}}
	</tab>
	<tab title="Tree, diff/hybrid/snapshot">
		{{tree:https://signalbhn.org/fhir/StructureDefinition/healthcareservice, buttons}}
	</tab>
	<tab title="JSON">
		{{json:https://signalbhn.org/fhir/StructureDefinition/healthcareservice,}}
	</tab>
</tabs>

## Profile usage

The HealthcareService resource is used to describe healthcare services offered by an organization (called a provider) within a given context defined by OrganizationAffiliation. This resource contains many business-specific elements including offered programs, service types (modalities), service categories, procedure codes, and more.  HealthcareService is meant to be a reusable resource, relating the aforementioned business elements to providers.

### Profile element notes

**.program**
- SHALL be used to group services offered by one or more organizations under a formal "program" label; e.g. SUD, CYMHTA, CCS.
- Programs are relatively static within the organization and create the main taxonomy for the service categories and procedures available.

**.category**
- SHALL be used to facilitate groupings of procedures to be offered; e.g. Prevention/Eearly Intervention Services, Screening, Crisis
- Definitions from Colorado BHA USCS Manual and a catch-all Other for business-specific definitions
   - will also include an "Other" code for non-Colorado BHA procedures
- Procedure codes will directly fall into one of these categories
- Secondary level to program, used as a hierarchical relationship to programs; e.g. SUD ASAM-0.5, SUD Differential Assessment, Crisis mobile, CYMHTA treatment.
- Previously referred to as *modality*

**.type**
- Will remain FHIR default (example) but will be unused at this time (see slices)

**.type:services**
- Custom code system for Signal that represents the "services" or "service type" codes that are available based on Organization qualifications; e.g. asam-0.5, da, crisis-mobile, etc.

**.type:procedure** -- *Tentative use, this is likely to change*
- SHOULD be populated with with procedure codes (HCPCS, CPT) that are applicable to this service category
- Definitions come from [Colorado BHA USCS Manual](https://hcpf.colorado.gov/sites/hcpf/files/July%202023%20USCS%20Manual%20Draft%20-Final.pdf)

## Examples
