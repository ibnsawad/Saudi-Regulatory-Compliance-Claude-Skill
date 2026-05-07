# CST — Cloud Computing Regulatory Framework and Related Regulations

## Issuer

Communications, Space and Technology Commission (CST), Kingdom of Saudi Arabia. CST was renamed in 2023 from CITC (Communications and Information Technology Commission). Older user references to "CITC" should be translated to "CST".

## Headline regulation

**Cloud Computing Regulatory Framework (CCRF)** — currently CCRF v2 (issued 2023). Establishes:

- Licensing classes for cloud service providers
- Customer data classification levels with corresponding requirements
- Customer protection obligations
- Information sharing and law-enforcement cooperation rules
- Service-quality and incident-reporting expectations

Note that NCA's CCC-2:2024 governs *cybersecurity controls* on cloud, while CST CCRF governs *licensing, customer protection, and operational obligations*. A CSP operating in KSA must comply with both. Holding a CST cloud licence does not exempt a provider from NCA cybersecurity controls.

## Licensing classes

CST CCRF defines licence categories for cloud providers operating in KSA. The user should expect:

- **Class B** — generally for providers of cloud services to KSA customers without full local hosting; conditions on data flows and service obligations.
- **Class C** — for providers with infrastructure within KSA serving customer workloads at higher data-sensitivity levels.
- **Registration** — required for providers offering cloud to KSA customers (including from outside KSA) before commercial offering.
- **Local presence / data residency** is required at higher tiers and for certain customer categories (e.g. government).

Confirm the exact class against the published CCRF before stating obligations — class scope has been refined across CCRF versions.

## Customer data categorisation

CCRF uses a customer-data tier model (typically four levels) that maps to permitted handling:

- Level 1 — public / non-sensitive
- Level 2 — private / commercial
- Level 3 — sensitive (regulated; often residency-restricted)
- Level 4 — top sensitive (e.g. national-security adjacent; tightly residency- and access-restricted)

Higher levels constrain:

- CSP class permitted to process / store
- Permitted geographic location (in-KSA only at Level 4)
- Sub-processor permissibility
- Permitted access from outside KSA (admin or support access)
- Cryptographic key custody (often customer-held HSM at higher levels)

Verify exact level numbering and criteria against the current CCRF version when working with the user.

## Customer protection and operational obligations

CCRF requires:

- Transparent terms of service in plain language
- Defined SLAs and remedies
- Pricing transparency
- Notice periods for material change
- Data-portability and exit support
- Security and privacy disclosures
- Documented incident-handling and customer notification
- Information-sharing with CST on request, within legal limits

## Reporting and engagement

- Service disruption reporting to CST per the licence conditions
- Periodic regulatory reporting (KPIs, customer numbers, incidents)
- Engagement with CST on regulatory inquiries and investigations
- Cooperation with law-enforcement requests within KSA legal process

## Other CST-relevant regulations

CST also issues / oversees:

- Telecom licensing and quality regulations (relevant to telcos and ISPs)
- Bylaws and regulations on Internet of Things, AI services, and digital content (where applicable)
- Postal regulations (out of scope for cybersecurity but useful context for CST-licensed entities)
- The IoT Regulatory Framework — applies to providers of connected devices and platforms

## Audit hot spots

- CSP active in KSA without registration / licence under CCRF
- Marketing materials claiming "data resident in KSA" without actual in-Kingdom processing
- Sub-processor list outdated or undisclosed
- Incident notification process not aligned to CCRF customer-notification timelines
- Exit and portability provisions absent or unfair
- Cross-border admin access not declared to customers in regulated tiers

## Required artefacts

- CST registration / licence with current version
- Customer-facing terms aligned to CCRF
- Service catalogue with data-tier mapping
- SLAs, change-management notices, exit-support procedure
- Sub-processor register with locations and data tiers
- Incident notification procedure (customer + CST)
- Data residency attestation, where claimed
- Reports filed with CST in the last 12 months

## Cross-references

- NCA CCC-2:2024 — cybersecurity controls (parallel obligation)
- PDPL + Transfer Regulation — for cross-border personal-data flows
- NDMO Standards — where the customer is a government entity
- ISO/IEC 27017 / 27018 — international cloud and PII alignment

## Verification note

CCRF has evolved across versions and CST issues clarifications periodically. Tier numbering, licence-class names, and reporting timelines should be confirmed against the current published CCRF before being relied on in formal output.
