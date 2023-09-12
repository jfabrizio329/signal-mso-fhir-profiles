---
topic: {{page-title}}
---

# {{page-title}}

---

Most profiles are derived from [US Core](https://hl7.org/fhir/us/core/index.html) or [FHIR Core R4](http://hl7.org/fhir/R4/resourcelist.html), which contains detailed background: 
> A simple narrative summary gives each profile’s requirements and guidance. A formal hierarchical table presents a [logical view](http://hl7.org/fhir/R4/formats.html#table) of the content in both a differential and snapshot view and references to appropriate terminologies and examples are provided.

In this implementation guide, there is additional business logic and specifications around how to use key fields.

## Profile page format

**Status**:  `Will describe any Work-in-Progress (WIP) information.`

---

Canonical URL: < Used to identify the resource.  *This is the preferred way to reference a conformance or knowledge resource.* >

Simplifier project page: < Link to Simplifier project page where issues can be opened. >

Derived from: < Link to base definition canonical URL that forms the basis of the specification. This will typically be the US Core STU6 or FHIR Core R4 page.  Contains detailed information on how resource should be used. outside institute-specific context available in this IG. >

Module:  < Link to IG module specification which includes conceptual model and high-level business context. >

---

**Formal profile content**

Tree structure of profile that is available as: 
- Snapshot - includes all elements and descriptions
- Tree, diff/hybrid/snapshot - selectable, combined view of all options include diff (differences from base canonical URL from which the profile was derived), hybrid (differences highlighted), snapshot
- JSON - shows JSON differences from base definition canonical URL

Tip:  To highlight institution-specific changes from base definition canonical URL, choose the `diff` tree type.

**Profile useage**
Will describe implementation-specific usage and key elements with notes.

## List of Profiles 

{{index:current}}