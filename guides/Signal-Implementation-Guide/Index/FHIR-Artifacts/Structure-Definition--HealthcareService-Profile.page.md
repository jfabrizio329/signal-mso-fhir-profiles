---
topic: {{page-title}}
---

# {{page-title}}

---

Canonical URL: https://signalbhn.org/fhir/StructureDefinition/SignalHealthcareService

Simplifier project page: https://simplifier.net/signal-mso-fhir-profiles/signalhealthcareservice

Derived from: [HealthcareService (R4)](http://hl7.org/fhir/R4/healthcareservice.html)

Module:  {{pagelink:Organization-Services-Module}}

---

# Formal profile content
<tabs>
	<tab title="Tree snapshot">
		{{tree:https://signalbhn.org/fhir/StructureDefinition/SignalHealthcareService, snapshot}}
	</tab>
	<tab title="Tree, diff/hybrid/snapshot">
		{{tree:https://signalbhn.org/fhir/StructureDefinition/SignalHealthcareService, buttons}}
	</tab>
	<tab title="JSON">
		{{json:https://signalbhn.org/fhir/StructureDefinition/SignalHealthcareService,}}
	</tab>
</tabs>

# Profile usage

The HealthcareService resource is used to describe healthcare services offered by an organization (called a provider) within a given context defined by OrganizationAffiliation. This resource contains many business-specific elements including offered programs, service types (modalities), service categories, procedure codes, and more.  HealthcareService is meant to be a reusable resource, relating the aforementioned business elements to providers.

## Profile element notes

**.program**
- SHALL be used to group services offered by one or more organizations under a formal "program" label; e.g. SUD, CYMHTA, CCS.
- Programs are relatively static within the organization and create the main taxonomy for the service categories and procedures available.

**.type** -- *Future change* call this the `.type.services` element
- SHALL be used as a secondary grouping of services offered, creating a hierarchical relationship to programs; e.g. SUD ASAM-0.5, SUD Differential Assessment, Crisis mobile, CYMHTA treatment.

**.type.serviceCategory**  -- *Future change* change this to .category element
- SHALL be used to facilitate groupings of procedures to be offered; e.g. Prevention/Eearly Intervention Services, Screening, Crisis
- Definitions from Colorado BHA USCS Manual and a catch-all Other for business-specific definitions

**.type.procedure**
- SHOULD be populated with with procedure codes (HCPCS, CPT) available under each related .serviceCategory
- Definitions from Colorado BHA USCS Manual

**.category**
- *Future change*: this will be the .type.serviceCategory

**.type**
- asdf

**.type**
- asdf

**.type**
- asdf

**.type**
- asdf

**.type**
- asdf

**.type**
- asdf

**.type**
- asdf





### Examples
