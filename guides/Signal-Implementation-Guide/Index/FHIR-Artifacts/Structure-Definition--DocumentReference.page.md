---
topic: documentreference-profile
---

# {{page-title}}

---

**Status**:  WIP, expanded valueset in [issue #38](https://github.com/enjoysparkling/signal-mso-fhir-profiles/issues/38)

---

Canonical URL: http://hl7.org/fhir/StructureDefinition/DocumentReference

Simplifier project page: Not Applicable

Derived from: [DocumentReference (R4)](http://hl7.org/fhir/R4/documentreference.html)

Module:  {{pagelink:File-Repository-Module}}

---

## Formal profile content
<tabs>
	<tab title="Tree snapshot">
		{{tree:http://hl7.org/fhir/StructureDefinition/DocumentReference, snapshot}}
	</tab>
	<tab title="Tree, diff/hybrid/snapshot">
		{{tree:http://hl7.org/fhir/StructureDefinition/DocumentReference, buttons}}
	</tab>
	<tab title="JSON">
		{{json:http://hl7.org/fhir/StructureDefinition/DocumentReference,}}
	</tab>
</tabs>

## Profile usage

The DocumentReference resource will be used to store metadata about files uploaded and interchanged between a service organization and a provider agency or location so they can be discovered and managed.  The files may be of any kind and used for any purpose.  In the case they relate to a specific encounter or episode of care (admission), those references SHOULD be provided.

**Note**:  Although there exists a [US Core DocumentReference](https://hl7.org/fhir/us/core/StructureDefinition-us-core-documentreference.html), it is geared towards Clinical Notes and requires a Patient reference.  Signal's DocumentReference will be used in a much more general capacity and will not always have an explicit Patient.

### File Storage
Files are intended to be stored in an external storage (e.g. Azure storage) and be linked with a resolvable URI for parties with proper permissions.

In all instances, the correct mimetype SHALL be specified for the attached file.

### Additional notes
Additional notes and corespondance between a service organization and provider about the document MAY be stored as additional attachments

ALTERNATIVELY, additional notes on a DocumentReference file may be added as a new DocumentReference that uses the `relatesTo.code = appends` and references it in `relatesto.target`.

### Profile element notes

**.status**
- will contain `current` unless it has been marked as `entered-in-error` or `superseded`
- Alternatively the file may be deleted from the system

**.description**
- MAY be used for document name or short description that is searchable

**.type**
- Kind of document, specified by LOINC, which defines the FHIR document code
- Especially important to lend context to clinical notes

**.category** - *FUTURE* - will need to add Signal's "classifications" to this, should be LOINC
- Categorization of document, "classification" in Signal's glossary
- Will be used for business purposes to group documents

**.content.attachment.url**
- SHALL use the `.attachment.url` field to reference files; do not directly attach data to avoid very large file returns from FHIR 

**.content.attachment.contentType**
- SHALL be populated with the appropriate MimeType, either identified programmatically or during entry
- MAY be used to render document for display

**.content.attachment.title**
- MAY be listed for display purposes
- Currently NOT used in search parameters; use the `.description` field for searchable information 

**.content.format** - *FUTURE* - potential future add
- SHOULD be fixed value at `urn:ihe:iti:xds:2017:mimeTypeSufficient`
- Requires proper `DocumentReference.content.attachment.contentType` code associated with `DocumentReference.content.attachment.url`

**.subject**
- Reference the Patient in cases where document specifically discusses an individual that is subject of services
- Note:  In [DocumentReference (R5)](http://hl7.org/fhir/R5/documentreference.html) this field references ANY file, but will likely still be Patient in Signal's context

**.author**
- MAY represent the Organization that creates the document, since Users are not stored in FHIR

**.custodian**
- SHOULD represent the provider Organization that has created and maintaining the document

**.context.encounter**
- SHOULD reference the encounter and/or episode of care for which the services were performed related to the document

**.context.sourcePatientInfo**
- Reference the Patient in cases where document specifically discusses an individual that is subject of services

**.context.related**
- References any other resources or identifiers that may be referenced or related to the file


## Examples

