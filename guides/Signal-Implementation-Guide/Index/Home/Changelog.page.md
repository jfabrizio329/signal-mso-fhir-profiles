---
topic: changelog
---

# {{page-title}}

---

## Description

This page contains manually listed chagnes, which generally correspond to major changes additions or breaking changes.

**Note:  This IG is still under development.  Changes should be expected often, including potentially breaking changes that will not be explicitly called-out.**  An effort will be made to list such changes here.

Detailed changes can be found on the [GitHub 'main' commits](https://github.com/enjoysparkling/signal-mso-fhir-profiles/commits/main) page.

## Chronological changes

| Date | Description | New Package Version |
| --- | --- | --- |
| 2023-11-13 | - Updated {{pagelink:encounter-profile}} with substantial updates to `.type` and procedure code usage <br /> - Updated {{pagelink:procedure-profile}} usage to indicate a preference for `Encounter.type` <br /> - {{pagelink:communication-profile}} updated `.reasonReference` with a note about the custom search parameter created for it. <br /> - Reorganized {{pagelink:terminology}} to break out signal custom and survey pages from the index. <br /> - Added ChargeItemDefinition to {{pagelink:finance-module}}, updated diagram, created {{pagelink:chargeitemdefinition-profile}}. | 0.2.0 |
| 2023-11-10 | - Added finance Structure Definition pages <br /> - Updated {{pagelink:finance-module}} with new potential resources, definitions, and updated conceptual diagram | --- |
| 2023-11-02 | - Removed Observation Screening Assessment, no planned use | --- |
| 2023-10-31 | - Fixed resource trees throughout <br /> - Added description to {{pagelink:servicerequest-profile}}. <br /> - Updated conceptual diagram for {{pagelink:clinical-categorization-module}} | 0.1.10 |
| 2023-10-30 | - IG updates, Org, practitioner, documentreference, and more | --- |
| 2023-10-04 | - Updated {{pagelink:clinical-categorization-module}} diagram for Procedure-->Reference(Encounter) <br /> - Created {{pagelink:encounter-profile}} usage notes. | 0.1.9 |
| 2023-09-29 | - Updated {{pagelink:task-profile}} notes | 0.1.8 |
| 2023-09-28 | - Added profile notes to {{pagelink:communication-profile}} <br /> - Added Practitioner resources to {{pagelink:organization-services-module}} <br /> - Updated {{pagelink:clinical-categorization-module}} concpetual model for Practitioner <br /> -Added notes to {{pagelink:practitioner-profile}} and {{pagelink:practitionerrole-profile}} | 0.1.7 |
| 2023-09-26 | - Combined Communications Module with File Exchange, creating the {{pagelink:file-repository-module}} <br /> - Created {{pagelink:communication-profile}}, {{pagelink:communicationrequest-profile}}, {{pagelink:flag-profile}} pages | 0.1.6 |
| 2023-09-25 | - Created {{pagelink:task-profile}} <br /> - Added Task to {{pagelink:file-repository-module}} <br /> - Renamed File Repository Module to File Exchange Module to align with business definitions (links should automatically update) <br /> - Updated communications-module with additional information | 0.1.5 |
| 2023-09-22 | - Updated images on {{pagelink:organization-services-module}} <br /> - Added note for future region add on {{pagelink:location-profile}} | 0.1.4 |
| 2023-09-21 | - Updated {{pagelink:clinical-categorization-module}} with an example and additional clarification for EpisodeOfCare vs. Encounter rationale <br /> - Created communications-module | 0.1.3 |
| 2023-09-19 | - Updated {{pagelink:documentreference-profile}} with new information <br /> - Updated {{pagelink:episodeofcare-profile}} from last discussion <br /> - Updated {{pagelink:healthcareservice-profile}} with latest elements | 0.1.2 |
| 2023-09-14 | - Created {{pagelink:file-repository-module}}  <br /> - Created {{pagelink:documentreference-profile}} <br /> - Created {{pagelink:changelog}}| 0.1.1 |

