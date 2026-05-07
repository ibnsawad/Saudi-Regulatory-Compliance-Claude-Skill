# Saudi PDPL — Personal Data Protection Law

## At a glance

| Field | Value |
|-------|-------|
| Instrument | Personal Data Protection Law (PDPL) |
| Original issuance | Royal Decree M/19, dated 09/02/1443H (16 Sept 2021) |
| Material amendment | Royal Decree M/148, dated 05/09/1444H (27 March 2023) |
| Effective date | 14 September 2023 |
| Full enforcement (post grace period) | 14 September 2024 |
| Implementing Regulations | Issued by SDAIA, 7 September 2023 |
| Personal Data Transfer Regulation | Issued by SDAIA, 5 September 2024 |
| Competent authority | Saudi Data and AI Authority (SDAIA), with NDMO supervising public-sector entities |

## Scope

Applies to:

- Any processing of personal data of individuals **residing in KSA**, by any means, regardless of where the controller / processor is located.
- Public-sector and private-sector entities.
- Includes processing of deceased individuals' personal data where it would identify them or a family member.

Extraterritorial reach: a foreign entity processing the personal data of KSA residents falls within PDPL.

## Key definitions

- **Personal Data** — any data, of whatever source or form, that would identify an individual or make them identifiable, directly or indirectly. Examples include name, ID number, address, contact details, bank and credit card numbers, photographs, recordings.
- **Sensitive Personal Data** — data revealing racial or ethnic origin, religious / intellectual / political belief, security-related data, criminal and security records, biometric data, genetic data, credit data, health data, location data, and data revealing the parents.
- **Controller** — entity that determines purpose and means of processing.
- **Processor** — entity that processes on behalf of a controller.

## Lawful bases (PDPL Art. 6)

Processing is permitted where one of the following applies:

- Consent of the data subject
- Achievement of an actual benefit to the data subject where contacting them is impossible or impractical
- Compliance with a legal obligation
- Compliance with a previous or future agreement to which the data subject is a party
- A legitimate interest of the controller, provided it does not prejudice the data subject's rights and is not personal nor sensitive data

Sensitive data has narrower bases — generally requires explicit consent or a specific legal basis.

## Data-subject rights

PDPL grants data subjects the right to:

- Be informed of the legal basis and purpose
- Access their data
- Request correction or completion
- Request destruction when no longer needed
- Withdraw consent

Implementing Regulations specify response timelines (generally 30 days, extendable in defined circumstances).

## Controller obligations (selected)

- **Registration** with SDAIA's national register where required (initially expected; the Implementing Regulations / SDAIA notices provide details and the current state has been adjusted in updates).
- **Records of processing activities**.
- **Privacy notice** at point of collection.
- **Data minimisation** and purpose limitation.
- **Accuracy and up-to-dateness**.
- **Security measures** appropriate to risk.
- **Retention** limited to what is necessary; defined retention periods.
- **DPIA** for high-risk processing (likely to involve sensitive data, large-scale processing, profiling, etc.).
- **Data Protection Officer (DPO)** designation — required where processing meets thresholds defined in the Implementing Regulations (large-scale sensitive processing, public-sector entities, regular and systematic monitoring).
- **Sub-processor governance** with written agreements.

## Breach notification

PDPL Implementing Regulations require:

- **To SDAIA**: notify within **72 hours** of becoming aware where the breach is likely to cause harm.
- **To the data subject**: notify without undue delay where the breach is likely to cause serious harm.

The notification must describe the breach, categories and approximate numbers of data subjects, likely consequences, measures taken, and contact for further information.

## Cross-border transfer

The **Personal Data Transfer Regulation** (Sept 2024) governs transfers outside KSA. Permitted mechanisms include (subject to conditions and SDAIA guidance):

- Adequacy decisions / list of jurisdictions deemed to provide an appropriate level of protection
- Appropriate safeguards (binding common rules, certification, codes of conduct, standard contractual clauses approved by SDAIA)
- Specific exemptions (consent, contract performance, vital interests, public interest)

A **Transfer Impact Assessment (TIA)** is expected for transfers to third countries without an adequacy decision, evaluating laws and practices that might affect the data and any supplementary measures needed.

Sensitive data and large-scale transfers attract stricter conditions, sometimes including SDAIA notification or pre-approval.

## Penalties

PDPL provides for administrative penalties, financial fines, and in certain cases criminal liability. Notable bands include:

- **Disclosure or publication of sensitive personal data** in violation of the Law — imprisonment up to 2 years and / or a fine up to **SAR 3,000,000**.
- **Transfer of personal data outside KSA** in violation — administrative penalties and fines.
- **General violations** — administrative penalties and fines up to **SAR 5,000,000**, doubling for repeat offences.
- Reputational sanctions (publication of decisions) and orders to cease processing also apply.

Confirm latest penalty levels against SDAIA-issued schedules before quoting.

## Public-sector overlay (NDMO)

For government and public-sector entities, the **NDMO Personal Data Protection Standards** (and broader Data Management Standards) layer specific obligations and processes. NDMO may take supervisory action alongside SDAIA. See `NDMO-Standards.md`.

## Mapping to ISO 27701 and GDPR

- ISO/IEC 27701:2019 PIMS controls map cleanly to PDPL controller and processor obligations and provide an evidence framework.
- GDPR-alignment is broadly consistent on principles (lawful basis, data-subject rights, breach notification) with some divergences (specific lawful bases, the registration obligation, the role of SDAIA, and Saudi-specific transfer mechanics).

## Audit hot spots

- Privacy notices missing on web forms or buried in T&Cs
- Consent collection without granular opt-ins
- Records of processing not maintained or out of date
- DPO not designated where thresholds are met, or DPO without independence
- No documented retention schedule
- Vendors processing personal data without a data-processing agreement
- Cross-border transfers with no TIA or transfer mechanism
- Marketing databases retained without lawful basis review

## Required artefacts

- Privacy notices for each collection point
- Consent records with granular log
- Records of processing (RoPA)
- DPO designation letter and contact details
- Retention schedule
- DPIAs for high-risk processing
- TIAs for outbound transfers
- Data-processing agreements with all processors
- Breach response procedure with 72-hour notification path
- Data-subject rights workflow with logged requests and SLA evidence
- SDAIA registration evidence (where required for the entity)

## Verification note

Article numbering above follows the published English translation of PDPL. Implementing Regulations and the Transfer Regulation use their own numbering — cite from the documents directly when quoting. Penalty levels and registration obligations have been refined since the 2021 Royal Decree; always re-check against the latest SDAIA notices before using in client output.
