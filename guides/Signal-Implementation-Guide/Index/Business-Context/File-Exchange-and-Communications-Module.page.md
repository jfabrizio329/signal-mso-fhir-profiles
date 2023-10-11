---
topic: file-repository-module
---

# {{page-title}}

---

## Context
This module is used for administrative and workflow files that occur outside a specific encounter, though they may refer to one or more encounters or episodes of care.

This module is also used  and specify resources used by the application back-end for interactions between a user and a system administrator.  The following resources are included for both notification and interactions to be contained within the same system and context of the work being recorded, as these resources can provide references and context to other FHIR elements such as Patient or Encounter -relevant.
- FHIR provides for many resources that can be used within a [Workflow](http://hl7.org/fhir/workflow.html), and we will utilize many of those to better integrate with the rest of the resources.
- FHIR provides for many resources that can be used within [Workflow Communications Patterns](http://hl7.org/fhir/workflow-communications.html), and we will utilize many of those to better integrate with the rest of the resources.

## FHIR Focus Resource Types
| Name | Aliases | Description |
| --- | --- | --- |
| {{pagelink:documentreference-profile}} | File repository, metadata        | Contains searchable metadata about attached files, including references to encounters, episodes of care, patient, and more |
| {{pagelink:task-profile}} | --- | A task resource describes an activity that can be performed and tracks the state of completion of that activity. It is a representation that an activity should be or has been initiated, and eventually, represents the successful or unsuccessful completion of that activity. |
| {{pagelink:communication-profile}} | Reminder, Alert, Note | An occurrence of information being transmitted; e.g. an alert that was sent to a responsible provider, a public health agency that was notified about a reportable condition. <br /> *This should not contain novel findings about a patient, those should be contained on the associated encounter.* |
| {{pagelink:communicationrequest-profile}} | --- | A request to convey information; e.g. the CDS system proposes that an alert be sent to a responsible provider, the CDS system proposes that the public health agency be notified about a reportable condition. |
| {{pagelink:flag-profile}} | Notification, Warning, Alert | Prospective warnings of potential issues when providing care to the patient. |

## Conceptual Model

{{render:guides/Signal-Implementation-Guide/Index/assets/images/signal-file-module-2023-09-29.png}}

## Notes

### Flags and Communication

Per [Flag Bondaries and Relationships](http://hl7.org/fhir/flag.html#bnr):
> Flags are not used to convey information to a specific individual or organization (e.g. an abnormal lab result reported to the ordering clinician, reporting of an adverse reaction to a regulatory authority). These are handled using the CommunicationRequest and the Communication resources.

Per [Communication Bondaries and Relationships](http://hl7.org/fhir/communication.html#bnr):
> Flag resources represent a continuous ongoing "communication" alerting anyone dealing with the patient of certain precautions to take or issues to be aware of. The flags are continuously present as an ongoing reminder. This is distinct from Communication where there is a specific intended sender and receiver and the information is delivered only once.

### Communication and Encounter

Per [Communication Bondaries and Relationships](http://hl7.org/fhir/communication.html#bnr):
>  The Communication is about the transfer of information (which might or might not occur as part of an encounter), while Encounter is about the coming together (in person or virtually) of a Patient with a Practitioner. Communication does not deal with the duration of a call, it represents the fact that information was transferred at a particular point in time. <br /> The phone calls involving the Patient should be handled using Encounter. 

## Examples
