## {{page-title}}

Canonical URL: [https://signalbhn.org/fhir/StructureDefinition/Organization](https://signalbhn.org/fhir/StructureDefinition/Organization)

Simplifier project page: [Signal Organization](https://simplifier.net/signal-mso-fhir-profiles/organizationprofile)

Derived from: [US Core Organization STU6 (R4)](http://hl7.org/fhir/us/core/STU6/StructureDefinition-us-core-organization.html)

Module:  {{pagelink:Organization-Services-Module}}

### Formal views of profile content
{{tree:https://signalbhn.org/fhir/StructureDefinition/Organization, snapshot}}


### Usage
The Organization resource is used to collect information on healthcare service providers, provider locations, or service organizations that may be used as support for other resources that need to reference organizations.  Hierarchies (levels via Organization.partOf), affiliations (via the OrganizationAffliation resource), and services (via the HealthcareServices resource) are established to provide context into relationships and capabilities of each organization.

#### Notes

**.type**
- Signal custom code system that identifies the kind of organization (e.g. service organization, agency, location)
- Does not explicitly denote hierarchy `.partOf` and the *OrganizationAffiliation* resource should be used for this purpose

**.partOf**
- The organization of which this organization forms a part
- Most common example is the specific location for a Provider Agency;  e.g. Denver West would contain `.partOf='Denver Medical'`
- This relationship will be used for determining user access to services associated with Patients at the provider agency

**.qualification (extension)**
- This should represent the same as the `Organization.qualification` element now included in [Organization (R5)](https://hl7.org/fhir/R5/organization.html)
- Signal custom code system and valueset that identifies services (licenses) a provider is qualified to offer

**.photo (extension)**
- Used to store Organization logo for use in the user interface (UI)


### Examples
