---
topic: finance-module
---

# {{page-title}}

---

## Context
This is the Finance Module for capturing information related to contracts, accounts, coverage, and more.  This module is used for creating billing documents, financial reporting, capturing payer accounts, and inputing contracts including healthcare service rates.

## FHIR Focus Resource Types

See [FHIR Financial module glossary](https://www.hl7.org/fhir/R5/financial-module.html#fingloss) for a list of financial information terms related to or including health information.

| Name                      | Aliases                                   | Description |
| --- | --- | --- |
| {{pagelink:account-profile}} | Fund, funding account | A financial tool for tracking value accrued for a particular purpose. In the healthcare field, used to track charges for a patient, cost centers, etc.  <br /> Administrative category. |
| {{pagelink:contract-profile}} | Rates, service rates | Legally enforceable, formally recorded unilateral or bilateral directive i.e., a policy or agreement.  <br /> Administrative category. |
| {{pagelink:coverage-profile}} | --- | Financial instrument which may be used to reimburse or pay for health care products and services. Includes both insurance and self-payment.  <br /> Administrative category. |
| {{pagelink:invoice-profile}} | Payment reconciliation, bill | Invoice containing collected ChargeItems from an Account with calculated individual and total price for Billing purpose. |
| {{pagelink:chargeitem-profile}} | Line item | The resource ChargeItem describes the provision of healthcare provider products for a certain patient, therefore referring not only to the product, but containing in addition details of the provision, like date, time, amounts and participating organizations and persons. Main Usage of the ChargeItem is to enable the billing process and internal cost allocation. |
| [ChargeItemDefinition](http://hl7.org/fhir/R4/chargeitemdefinition.html) | Line item pricing rules | The ChargeItemDefinition resource provides the properties that apply to the (billing) codes necessary to calculate costs and prices. The properties may differ largely depending on type and realm, therefore this resource gives only a rough structure and requires profiling for each type of billing code system. |
| {{pagelink:organization-profile}} | Payer, payor, guarantor, cost center, insurer, policy owner, policy holder | Organization involved in and/or responsible financial interactions between service providers and patients. <br /> See {{pagelink:organization-services-module}} for other uses. |
| {{pagelink:patient-profile}} | Client, subject, beneficiary | See {{pagelink:patient-administration-module}}. |
| TBD | TBD        | TBD |
| Claim | Adjudication Request, Preauthorization Request | A provider issued list of professional services and products which have been provided, or are to be provided, to a patient which is sent to an insurer for reimbursement. <br /> Billing category. |
| ClaimResponse | Remittance Advice | A payor's adjudication and/or authorization response to the suite of services provided in a Claim. Typically the ClaimResponse references the Claim but does not duplicate the clinical or financial information provided in the claim. <br /> Billing category. |
| PaymentNotice | TBD        | This resource provides the status of the payment for goods and services rendered, and the request and response resource references. <br /> Payment category. |
| PaymentReconciliation | TBD        | Provides the bulk payment details associated with a payment by the payor for goods and services rendered by a provider to patients covered by insurance plans offered by that payor.  This resource provides the details including amount of a payment and allocates the payment items being paid. <br /> Payment category. |
| ExplanationOfBenefit | EOB | This resource combines the information from the Claim and the ClaimResponse, stripping out any provider or payor proprietary information, into a unified information model suitable for use for: patient reporting; transferring information to a Patient Health Record system; and, supporting complete claim and adjudication information exchange with regulatory and analytics organizations and other parts of the provider's organization. |



## Conceptual Model

{{render:guides/Signal-Implementation-Guide/Index/assets/images/signal-finance-module-2023-11-13.png}}


## Notes

### Relative Order of Use

The [FHIR financial module](https://www.hl7.org/fhir/R5/financial-module.html) revolves around a traditional patient, provider, payer situation, which is not the focus of this Finance Module in Signal's context.  See [FHIR financial module Relative Order of Use](https://www.hl7.org/fhir/R5/financial-module.html#order) for an illustrative order of events and use of financial resources.

## Examples

