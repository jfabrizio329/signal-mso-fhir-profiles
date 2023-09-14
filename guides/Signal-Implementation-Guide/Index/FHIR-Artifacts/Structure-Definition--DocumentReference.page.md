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

### File Storage
Files are intended to be stored in an external storage (e.g. Azure storage) and be linked with a resolvable URI for parties with proper permissions.

In all instances, the correct mimetype SHALL be specified for the attached file.

### Profile element notes

**.type**
- *FUTURE* - asdf

## Examples

