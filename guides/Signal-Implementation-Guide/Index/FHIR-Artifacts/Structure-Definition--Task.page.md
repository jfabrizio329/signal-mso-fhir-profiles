---
topic: task-profile
---

# {{page-title}}

---

Status: WIP, will receive additional profile notes in the near future

Canonical URL: http://hl7.org/fhir/StructureDefinition/task

Simplifier project page: Not Applicable

Derived from: [Task (R4)](http://hl7.org/fhir/R4/task.html)

Module:  {{pagelink:file-repository-module}}

---

## Formal profile content
<tabs>
	<tab title="Tree snapshot">
		{{tree:http://hl7.org/fhir/StructureDefinition/task, snapshot}}
	</tab>
	<tab title="Tree, diff/hybrid/snapshot">
		{{tree:http://hl7.org/fhir/StructureDefinition/task, buttons}}
	</tab>
	<tab title="JSON">
		{{json:http://hl7.org/fhir/StructureDefinition/task,}}
	</tab>
</tabs>

## Profile usage

The Task resource will primarily be used when an activity needs to be performed on files exchanged between a service organization and a provider; e.g. if a document requires review by a provider or approval by a service organization.

### Profile element notes

**.status**
- Required field that will represent the status of a Task
- As an example: If the task is newly created and requires a provider to review a document sent by the service org, the status will be `requested`.

## Examples

