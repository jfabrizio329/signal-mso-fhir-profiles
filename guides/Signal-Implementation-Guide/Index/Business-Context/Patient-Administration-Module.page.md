---
topic: patient-administration-module
---

# {{page-title}}

---

## Context
This is the Patient Administration Module for describing Patient interaction touchpoints.

Note that there is no program, admission, encounter, or other provider interaction information contained on the Patient resource.  Nor is there any insurance, coverage, or payment information directly on Patient.  The Patient resource only covers the "who" information about the patient. Other resources will point to the patient, as noted in the conceptual model diagram.

## FHIR Focus Resource Types

| Name                      | Aliases                                   | Description |
| --- | --- | --- |
| {{pagelink:patient-profile}} | Client        | Represents the ID of a distinct patient in the context of the provider organization. (See notes below) |
| {{pagelink:organization-profile}} | Provider, Agency        | Represents a provider agency that is in charge of a patient's episode of care. |


## Conceptual Model

{{render:guides/Signal-Implementation-Guide/Index/assets/images/signal-patient-admin-module-2023-09-11.png}}

## Examples

