---
topic: {{page-title}}
---

# {{page-title}}

---

Canonical URL: https://signalbhn.org/fhir/StructureDefinition/OrganizationAffiliation

Simplifier project page: [Signal OrganizationAffiliation](https://simplifier.net/signal-mso-fhir-profiles/organizationaffiliation)

Derived from: [OrganizationAffiliation (R4)](http://hl7.org/fhir/R4/organizationaffiliation.html)

Module:  {{pagelink:Organization-Services-Module}}

---

# Formal profile content
<tabs>
	<tab title="Tree snapshot">
		{{tree:https://signalbhn.org/fhir/StructureDefinition/OrganizationAffiliation, snapshot}}
	</tab>
	<tab title="Tree, diff/hybrid/snapshot">
		{{tree:https://signalbhn.org/fhir/StructureDefinition/OrganizationAffiliation, buttons}}
	</tab>
	<tab title="JSON">
		{{json:https://signalbhn.org/fhir/StructureDefinition/OrganizationAffiliation,}}
	</tab>
</tabs>

# Profile usage

The OrganizationAffiliation resource is used to establish a relationship between a Organization resources such as Service Organization and Providers (provider locations) in addition to defining services that are offered via the HealthcareService resource.  Hierarchies between a provider agency and provider location are captured via `Organization.partOf`.

## Profile element notes

**.organization**
- SHOULD reference the service organization that owns the contract with the participatingOrganization

**.participatingOrganization**
- SHOULD reference a provider agency,  provider location, or payer entity that will be offering services or covering the cost of services rendered, defined by the `.code`

**.code**
- In a 'provider' role, the agency or provider-location Organization type (Organization referenced in  `.participatingOrganization`) will be assigned to a service organization Organization type (Organization referenced in  `.organization`)
- In a 'payper' role, the payer account (Organization referenced in `.participatingOrganization`) will be assigned to a agency or provider-location Organization type (Organization referenced in  `.organization`)

**.healthcareService**
- SHOULD reference all currently offered services between the participatingOrganization and Organiztion

**.period**
- When an affiliation is created, the `.period.start` date SHOULD be set to today the earliest date the relationship will be referenced
- When an affiliation no longer exists, the `.period.end` date SHOULD be set to the last day it was active

**.location**
- MAY specify physical location where the affiliation is valid or applicable
- Will typically represent the business region for offered services (relative to the service organization)


# Examples
