# Signal Managed Service Organization FHIR profiles

This repository is used for suggesting, reviewing, and correcting resources and files that ultimately end up in the [Signal MSO FHIR Profiles - SIMPLIFIER.NET](https://simplifier.net/Signal-MSO-FHIR-Profiles/).

These profiles are based on the US Core version 6.0.0 ([hl7.fhir.us.core 6.0.0](http://hl7.org/fhir/us/core/STU6/)) which, in turn, is based on FHIR core Version R4 ([hl7.fhir.r4.core 4.0.1](https://hl7.org/fhir/R4)).

See the [Signal Implementation Guide](https://simplifier.net/guide/signal-implementation-guide) for more details.

Recommended tools:
- [Forge](https://fire.ly/products/forge/) for building and modifying FHIR Profiles
- [Visual Studio Code](https://code.visualstudio.com/) for editing ValueSets and manually checking JSON structures

# Folder organization

```
.
|-- .simplifier/           Rules for Forge application and Simplifier.net
|-- guides/                Implementation guide (IG) for use on Simplifier.net
|-- input/
|   \-- resources/         Profiles in the form of StructureDefinition resource types
|   \-- vocabulary/        ValueSets used in Profiles, with static values populated
```

# Contribution guidelines
Follow [Microsoft Azure DevOps branching guidance](https://github.com/MicrosoftDocs/azure-devops-docs/blob/main/docs/repos/git/git-branching-guidance.md) for committing code.

For Example:
1. Create a new branch for your work, name it according to what you are looking to accomplish; e.g. bugfix/<valueset_name> or feature/practitioner/<extention_name>
1. Commit changes to your branch as you go, every 2 hours at least
1. Publish your branch 
1. Create a Pull Request (PR) when you are finished with changes and want a review from me
1. Watch your PR for comments and actions from me
1. Admin will review, and if your changes look good merge with main

