---
topic: episodeofcare-profile
---

# {{page-title}}

---

**Status**:  WIP, Signal custom profile is being modified for new elements

---

Canonical URL: https://signalbhn.org/fhir/StructureDefinition/StructureDefinition-profile-SignalEpisodeOfCare

Simplifier project page: [EpisodeOfCare](https://signalbhn.org/fhir/StructureDefinition/StructureDefinition-profile-SignalEpisodeOfCare)

Derived from: [FHIR Core R4 EpisodeOfCare](http://hl7.org/fhir/R4/episodeofcare.html)

Module:  {{pagelink:Clinical-Categorization-Module}}

---

## Formal profile content
<tabs>
	<tab title="Tree snapshot">
		{{tree:https://signalbhn.org/fhir/StructureDefinition/StructureDefinition-profile-SignalEpisodeOfCare, snapshot}}
	</tab>
	<tab title="Tree, diff/hybrid/snapshot">
		{{tree:https://signalbhn.org/fhir/StructureDefinition/StructureDefinition-profile-SignalEpisodeOfCare, buttons}}
	</tab>
	<tab title="JSON">
		{{json:https://signalbhn.org/fhir/StructureDefinition/StructureDefinition-profile-SignalEpisodeOfCare,}}
	</tab>
</tabs>

## Profile usage

The EpisodeOfCare resource represents the container for all services or contact points between a patient (client) and a healthcare services (provider).  This resource is also called the 'admission' and captures the entire case history for a patient for a program and selected services (service types).

EpisodeOfCare will rarely change once it is created.  Some instances of changes will be: an updated period.start date in the case of a referral or a period.end date for a discharge.  In the latter case, the status should also be updated to 'complete'.  Additional encounters will point to an EpisodeOfCare resource and not the other way around.

### Referrals in EpisodeOfCare
Any referrals from the Jolata system (called referrals) will reference a {{pagelink:servicerequest-profile}} on the `EpisodeOfCare.referralRequest` element. This will often begin a patient's admission record and SHOULD contain an Encounter record for the first contact or any interaction attempt with related codes.  Although this first attempt may start an admission and encounter records, the EpisodeOfCare.period.start date MAY correspond to when an admission took place, usually beginning with a survey assessment. 

### Profile element notes

**.type**
- Will remain FHIR default (example) but will be unused at this time (see slices)

**.type:program**
- Represents the same concept as the `HealthcareService.program` element
- SHALL be used to group services offered by one or more organizations under a formal "program" label; e.g. SUD, CYMHTA, CCS.
- Programs are relatively static within the organization and create the main taxonomy for the service categories and procedures available.

**.type:services**
- Represents the same concept as the `HealthcareService.type:services` element
- Custom code system for Signal that represents the "services" or "service type" codes that are available based on Organization qualifications; e.g. asam-0.5, da, crisis-mobile, etc.

**.managingOrganization**
- Represents the UI field 'Primary Service Location'
- Although this represents a single provider location, encounters pointing to this EpisodeOfCare may have different locations and/or with entirely different provider agencies
- This will primarily be used to provide default HealthcareService offerings on the UI
- The higher-level Provider Agency (accessed via the highest level of Organization.partOf) should be considered for all HealthcareService offerings available to the UI

**.careManager**
- Not presently used

**.team**
- Not presently used

## Examples

