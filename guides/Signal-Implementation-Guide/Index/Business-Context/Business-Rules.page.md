---
topic: {{page-title}}
---

# {{page-title}}

---

## HealthcareService programs and services

References the following elements:
`.program`, `.category`, `.type.service`, `.type.procedure`

We need to computationally enforce relationships between disparate code systems and/or FHIR elements.  For example (pulling from [Colorado State BHA Billing Manual](https://hcpf.colorado.gov/sites/hcpf/files/July%202023%20USCS%20Manual%20Draft%20-Final.pdf) pg. 31):
CPT code 90785 is allowed to have only the following HCPCS/CPT modifiers HE, HK, U4, TM. In addition, the code is only allowed at a subset of [Place of Service](https://www.hl7.org/fhir/valueset-service-place.html) (03 School, 04 Shelter, 11 Office, etc.), for a certain subset of [Service Provider](http://hl7.org/fhir/R4/v2/0360/2.7/index.html)(??) and Provider Bill Types (01, 02, etc.).

{{render:guides/Signal-Implementation-Guide/Index/assets/images/services-procedures-02-2023-08-29.png}}

{{render:guides/Signal-Implementation-Guide/Index/assets/images/services-procedures-01-2023-08-29.png}}


