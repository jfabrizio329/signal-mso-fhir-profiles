---
topic: encounter-profile
---

# {{page-title}}

Canonical URL: http://signalbhn.org/fhir/StructureDefinition/encounter

Simplifier project page: [ServiceRequest](https://simplifier.net/signal-mso-fhir-profiles/signal-encounter-profile) 

Derived from: [US Core Encounter STU6 (R4)](https://hl7.org/fhir/us/core/StructureDefinition-us-core-encounter.html)

Module:  {{pagelink:Clinical-Categorization-Module}}

---

## Formal profile content
<tabs>
	<tab title="Tree snapshot">
		{{tree:http://signalbhn.org/fhir/StructureDefinition/encounter, snapshot}}
	</tab>
	<tab title="Tree, diff/hybrid/snapshot">
		{{tree:http://signalbhn.org/fhir/StructureDefinition/encounter, buttons}}
	</tab>
	<tab title="JSON">
		{{json:http://signalbhn.org/fhir/StructureDefinition/encounter,}}
	</tab>
</tabs>

## Profile usage

This resource is used to capture an interaction between a patient and healthcare provider(s) for the purpose of providing healthcare service(s) or assessing the health status of a patient. Encounter is primarily used to record information about the actual activities that occurred.

### Procedure and Encounter
The Procedure and encounter have references to each other, and these should be to different procedures; **one for the procedure that was performed during the encounter (stored in Procedure.encounter)**, and another for cases where an encounter is a result of another procedure (stored in Encounter.reason) such as a follow-up encounter to resolve complications from an earlier procedure.

See additional information on {{pagelink:procedure-profile}}.

### Encounter vs. Admission (EpisodeOfCare)

Per the [Encounter scope and usage](http://hl7.org/fhir/R5/encounter.html#scope):
> The admission component is intended to store the extended information relating to an admission event. It is always expected to be the same period as the encounter itself. Where the period is different, another encounter instance should be used to capture this information as a partOf this encounter instance.

The definition of admission in a Signal context does not fit for this use. We are using the {{pagelink:episodeofcare-profile}} to store Signal's admission information.  See {{pagelink:clinical-categorization-module}} for additional information on Encounter vs. EpisodeOfCare.

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
- This code will MAY NOT explicitly be used for billing purposes; although, it should represent the same concept. (e.g. an Encounter record for a survey MAY NOT have an associated bill but will represent that procedure).
- See for {{pagelink:finance-module}} for billing information.

**.serviceType**
- SHALL represent the Signal Service Type (defined by BHA or other) for high-level categorization
- SHOULD match service type(s) available on the EpisodeOfCare

**.subject**
- Patient/client

**.episodeOfCare**
- EpisodeOfCare resource that contains the program and service type
- SHOULD match the service type on the EpisodeOfCare
- MAY point to more than 1 EpisodeOfCare if service is applicable to a plurality of concurrent ongoing services (EpisodeOfCare resources)

**.basedOn**
- MAY represent the Referral that caused the initial admission.
- The referral information will also be contained on EpisodeOfCare and SHALL be preferentially used to Encounter

**.reasonReference or .reasonCode**
- MAY represent a procedure or condition that caused this encounter
- SHALL NOT represent the services performed during this Encounter (the Procedure will reference this encounter will represent those services)

**.period**
- The start and end time of the encounter

**.length**
- MAY be used to represent time the encounter lasted. In this case it SHALL match applicable time units on {{pagelink:chargeitem-profile}}
- This SHOULD NOT be used for billing purposes but instead for reporting puroses on Encounter lengths

**.account**
- MAY be used to specify payer and/or funding that is different from one specified on EpisodeOfCare

**.serviceProvider**
- SHALL reference the Organization resource for the Provider (provider-location).  See {{pagelink:organization-services-module}}

**.partOf**
- MAY be used to point to encounter that created this encounter

## Examples
