---
topic: communication-profile
---

# {{page-title}}

---

Canonical URL: http://hl7.org/fhir/StructureDefinition/communication

Simplifier project page: Not Applicable

Derived from: [Communication (R4)](http://hl7.org/fhir/R4/communication.html)

Module:  {{pagelink:file-repository-module}}

---

## Formal profile content
<tabs>
	<tab title="Tree snapshot">
		{{tree:http://hl7.org/fhir/StructureDefinition/communication, snapshot}}
	</tab>
	<tab title="Tree, diff/hybrid/snapshot">
		{{tree:http://hl7.org/fhir/StructureDefinition/communication, buttons}}
	</tab>
	<tab title="JSON">
		{{json:http://hl7.org/fhir/StructureDefinition/communication,}}
	</tab>
</tabs>

## Profile usage

This Communication resource profile is intended to be used for messages passed between a provider and service organization specifically related to a DocumentReference in the File Exchange portal. 

A Communication is not intended to provide additional or novel findings for a Patient (e.g. observations) that occurred during an Encounter, this information should be located on or referenced from the Encounter.  If the communication relates to an encounter, it may be directly referenced.

### Profile element notes
**.status**
- Required field that will represent the status of a communication.

**.sender**
- Required field that will represent the status of a communication
- *SHOULD* reference the Practitioner resource for the currently logged-in user

**.recipient**
- Required field that will represent the status of a communication
- *MAY* reference an Organization resource (e.g. Service Organization) if message is intended for all Practitioners associated with the Organization, otherwise *SHOULD* reference a Practitioner

**.sent**
- The time when this communication was sent.
- For messages not yet sent needing a date time, consider using the `Communication.meta.lastUpdated` element.

**.received**
- The time when this communication arrived at the destination.

**.payload**
- Text, attachment(s), or resource(s) that was communicated to the recipient.
- Multiple types allowed:
   - Text-only values may use `Communication.payload.content[x].contentString`
   - `Communication.payload.content[x].contentAttachment` *SHOULD NOT*  include files that need to be tracked by the {{pagelink:documentreference-profile}} part of the file exchange.

**.reasonReference**
- *SHALL* reference the DocumentReference about which the communication was made
- Note: a custom search parameter was created to facilitate lookup references on this field

**.basedOn**
- When used, this SHOULD reference a Task resource assigned to the DocumentReference; i.e. this communication is regarding and/or has additional information for fullfilling the Task.

**.encounter**
- The Encounter to which the creation of this record is tightly associated.
- Note that novel findings for a Patient should be recorded on or reference from the Encounter and *SHALL NOT* exist solely on the communication.

**.inResponseTo**
- *MAY* be used to indicate a reply to a previous communication, to create a conversation thread.

## Examples

