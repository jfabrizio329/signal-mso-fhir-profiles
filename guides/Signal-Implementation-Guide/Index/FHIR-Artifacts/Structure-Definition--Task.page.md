---
topic: task-profile
---

# {{page-title}}

---

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

The current use case for this resource is in the context of a provider or service organization requesting a review of the DocumentReference file.  The notes in thie page will assume a "review" task for descriptions.

### Profile element notes

**.status**
- Required field that will represent the status of a Task
- As an example: If the task is newly created and requires a provider to review a document sent by the service org, the status will be `requested`.

**.code**
- For review task, will represent an 'approve' task code.
- This code may change as the task moves through the review process; e.g. if a request to update or change the focus DocumentReference, the *SHOULD* change to replace or change, as needed by the requester. In this case, the `input` and `output` elements may be used.

**.focus**
- *SHOULD* reference the DocumentReference resource that contains the document for review.

**.requester**
- *SHOULD* reference the individual (Practitioner) assigning the task.
- *MAY* reference the provider (Organization) that assigned the task, if no particular individual needs to be aware of task progress.

**.owner**
- *SHOULD* reference the individual (via Practitioner) who is responsible for completing the task (responsible individual).  
- *MAY* reference a provider (via Organization) if there is no one particular person responsible for it. This is a less direct ask but will be available to every user within that organization.

**.for**
- *MAY* reference the provider or individual that needs to be informed of the task progress. Consider this the equivalent of a CC field so they are made aware of a task.

**.input**
- *MAY* be used in the case of a requested change or request for an updated file. Input may be used to define the new file that may need review before it is uploaded as a new DocumentReference.

**.output**
- *MAY* be used in the case of a requested change or request for an updated file. Output may contain the new or finalzied DocumentReference based on the action. If the action is immediately completed upon review, the output may be ommitted and task closed.


## Examples

