# Finding Template

Use this format for every finding row in an assessment.

## Row template (markdown table)

```
| ID | Framework / Control Ref | Domain | Finding | Status | Regulatory Risk | Operational Risk | Priority | Owner | Remediation | Evidence Required |
```

## Field guidance

- **ID** — sequential, e.g. `F-001`, `F-002`. Include a sub-prefix if grouping by framework (e.g. `ECC-001`, `PDPL-001`).
- **Framework / Control Ref** — cite the framework version and the specific control or article (e.g. `ECC-2:2024 §2-x-x` or `PDPL Art. 20`). Where a control number cannot be confirmed, write the obligation in plain language and tag `[verify ref]`.
- **Domain** — the framework domain or subdomain the finding sits within.
- **Finding** — one or two sentences stating what was observed and why it falls short of the obligation. Avoid jargon; auditors and management both read this.
- **Status** — `Compliant` | `Partial` | `Non-compliant` | `Not applicable` (with justification) | `Insufficient evidence`.
- **Regulatory Risk** — `Critical` | `High` | `Medium` | `Low`. Critical = potential licence action, large fine, or regulator-mandated remediation.
- **Operational Risk** — `High` | `Medium` | `Low`. Tied to threat impact / likelihood independent of the regulator.
- **Priority** — `P1` (before next audit cycle / before designated event), `P2` (within 90 days), `P3` (within next planning cycle), `P4` (track only).
- **Owner** — role, not person, by default (CISO, DPO, Head of IT Ops, CIO, Vendor Manager).
- **Remediation** — concrete action. "Implement MFA on all privileged accounts using FIDO2" — not "improve authentication".
- **Evidence Required** — the artefact that, when produced, will close the finding. "Conditional access policy export + sample audit log" — not "evidence of MFA".

## Worked example row

```
| ECC-007 | ECC-2:2024 §2-9 (Logging & Monitoring) [verify ref] | Cybersecurity Defence | SIEM ingests logs from endpoint and AD only; cloud, network, and database logs are not centralised. Detection coverage gaps confirmed via use-case review. | Partial | High | High | P1 | CISO | Onboard cloud, network, and database log sources to the SIEM; build and tune the missing detection use cases per the entity's threat model; document use-case catalogue. | Use-case catalogue with mapped log sources; sample alerts triaged in the last 30 days; tuning records. |
```

## Findings summary block

After the table, include a summary block:

```
Total findings: 50
Compliant: 27
Partial: 14
Non-compliant: 9
By regulatory risk: Critical 2 / High 7 / Medium 20 / Low 21
P1 items: 9
```
