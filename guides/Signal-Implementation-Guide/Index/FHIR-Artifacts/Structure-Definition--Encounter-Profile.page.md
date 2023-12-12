---
topic: encounter-profile
---

# {{page-title}}

Canonical URL: https://signalbhn.org/fhir/StructureDefinition/encounter

Simplifier project page: [Signal Encounter](https://simplifier.net/signal-mso-fhir-profiles/signalencounter)

Derived from: [US Core Encounter STU6 (R4)](https://hl7.org/fhir/us/core/StructureDefinition-us-core-encounter.html)

Module:  {{pagelink:Clinical-Categorization-Module}}

---

## Formal profile content
<tabs>
	<tab title="Tree snapshot">
		{{tree:https://signalbhn.org/fhir/StructureDefinition/encounter, snapshot}}
	</tab>
	<tab title="Tree, diff/hybrid/snapshot">
		{{tree:https://signalbhn.org/fhir/StructureDefinition/encounter, buttons}}
	</tab>
	<tab title="JSON">
		{{json:https://signalbhn.org/fhir/StructureDefinition/encounter,}}
	</tab>
</tabs>

## Profile usage

This resource is used to capture an interaction between a patient and healthcare provider(s) for the purpose of providing healthcare service(s) or assessing the health status of a patient. Encounter is primarily used to record information about the actual activities that occurred.

### Procedure and Encounter
In general, a Procedure resource may not be necessary for capturing the type of encounter for billing purposes, `Encounter.type` SHOULD be used for capturing billable codes and the primary description of the encounter.

The Procedure and encounter have references to each other (`Procedure.encounter` and `Encounter.reasonReference`, respectively). In the case both are used these SHOULD be to different procedure resources. I.E. the former for the procedure that was performed during the encounter (stored in Procedure.encounter). The latter used for cases where an encounter is a result of another procedure (stored in Encounter.reasonReference) such as a follow-up encounter to resolve complications from an earlier procedure.

See additional information on {{pagelink:procedure-profile}}.

### Encounter vs. Admission (EpisodeOfCare)

Per the [Encounter scope and usage](http://hl7.org/fhir/R5/encounter.html#scope):
> The admission component is intended to store the extended information relating to an admission event. It is always expected to be the same period as the encounter itself. Where the period is different, another encounter instance should be used to capture this information as a partOf this encounter instance.

The definition of admission in a Signal context does not fit for this use. We are using the {{pagelink:episodeofcare-profile}} to store Signal's admission information.  See {{pagelink:clinical-categorization-module}} for additional information on Encounter vs. EpisodeOfCare.

### Special Note for available Encounter Procedure Codes

Encounter procedure codes (billable codes for services performed for a patient during an encounter) SHOULD be captured in `Encounter.type` (see below for more info).  These codes will be populated through a complex set of logic to allow a provider to see only the most relevant codes based on a number of factors, including:
1. Qualifications and licenses held by the provider location(s) selected as the serviceProvider via the `Organization.extension.qualification` on file
2. Programs and services provided by their organization via the `HealthcareService` resource and the associated Service Category and Service Type SQL lookup/crosswalk table
3. Potentially as services available via contracted rates

### Profile element notes

**.status**
- Will typically contain `finished` in this system, since these typically only entered after they have occurred.  An exception would be when an encounter is `entered-in-error` and should be completely removed from the patient's medical record after it came into the system.

**.class**
- Determined by provider.
- Will typically contain `AMB`, as this represents healthcare in a practitioner's office or nonresident care.
- For long term care, `IMP` will likely be used to represent a patient admitted to a facility.
- See value set definitions for more information.

**.type**
- SHALL contain the procedure code representing the encounter.
- This code is not required to have an explicit contracted rate based on the provider and procedure. 
- In the case this code is not billable encounter for a provider, the code SHOULD represent the same concept as the healthcare service performed. E.g. an Encounter record for a survey may not have an associated bill but SHOULD represent that procedure in CPT or SNOMED terminology.
- See for {{pagelink:finance-module}} for billing information.

**.serviceType**
- SHALL represent the Signal Service Type (defined by BHA or other) for high-level categorization
- SHOULD match service type(s) available on the EpisodeOfCare

**.subject**
- SHALL reference the Patient/client defined on the EpisodeOfCare

**.episodeOfCare**
- EpisodeOfCare resource that contains the patient, program(s) and service type(s)
- SHOULD match [one of] the service type(s) on the EpisodeOfCare
- MAY point to more than one EpisodeOfCare if service is applicable to a plurality of concurrent ongoing services (EpisodeOfCare resources) for the same patient

**.basedOn**
- MAY represent the Referral that caused the initial admission.
- The referral information will also be contained on EpisodeOfCare and SHALL be preferentially used to Encounter

**.participant.individual**
- SHOULD reference the {{pagelink:practitioner-profile}} for the primary performer (see .participant.type)
- `.participant.type` SHOULD be set to `PPRF` to indicate this as the primary performer
- When the `EpisodeOfCare.team` element is populated, this individual SHOULD be listed there if it is used here

**.reasonReference or .reasonCode**
- MAY represent a procedure or condition that caused this encounter
- SHALL NOT represent the services performed during this Encounter. `Encounter.type` will be the primary method to identify the type of encounter. Furthermore, {{pagelink:procedure-profile}} may reference this encounter with additional type and/or information.)

**.period**
- The start and end time of the encounter

**.length**
- MAY be used to represent time the encounter lasted. In this case it SHALL match applicable time units on {{pagelink:chargeitem-profile}}
- This SHOULD NOT be used for billing purposes but instead for reporting puroses on Encounter lengths

**.account**
- MAY be used to specify payer and/or funding that is different from one specified on EpisodeOfCare

**.location.location**
- SHOULD be used to specify the [Place of Service](https://www.cms.gov/medicare/coding-billing/place-of-service-codes/code-sets) (POS) Codes maintained by CMS.  
- See {{pagelink:location-profile}} for more information on POS.

**.serviceProvider**
- SHALL reference the Organization resource for the Provider (provider-location).  See {{pagelink:organization-services-module}}

**.partOf**
- MAY be used to point to encounter that created this encounter

## Examples

