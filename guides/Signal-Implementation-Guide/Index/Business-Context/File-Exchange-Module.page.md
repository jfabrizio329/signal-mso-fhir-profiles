---
topic: file-repository-module
---

# {{page-title}}

---

## Context
This is the file repository module which is used for administrative and workflow files that occur outside a specific encounter, though they may refer to one or more encounters or episodes of care.

FHIR provides for many resources that can be used within a [Workflow](http://hl7.org/fhir/workflow.html), and we will utilize many of those to better integrate with the rest of the resources.

## FHIR Focus Resource Types

| Name                      | Aliases                                   | Description |
| --- | --- | --- |
| {{pagelink:documentreference-profile}} | File repository, metadata        | Contains searchable metadata about attached files, including references to encounters, episodes of care, patient, and more |
| {{pagelink:task-profile}} | --- | A task resource describes an activity that can be performed and tracks the state of completion of that activity. It is a representation that an activity should be or has been initiated, and eventually, represents the successful or unsuccessful completion of that activity. |


## Conceptual Model

{{render:guides/Signal-Implementation-Guide/Index/assets/images/signal-file-module-2023-09-25.png}}

## Examples


