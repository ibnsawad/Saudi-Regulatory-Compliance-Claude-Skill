# Compliance Scoring Model

The skill uses a **multi-axis** scoring approach. Each finding carries a status, two risk dimensions, a priority, and (optionally) a maturity rating. This matches what NCA, SAMA, and SDAIA assessors look for and avoids the "everything is High Risk" trap.

---

## 1. Status

Status is the binary-ish answer to "is the obligation met?"

| Status | Meaning | Auditor read |
|--------|---------|--------------|
| **Compliant** | Implemented, documented, evidenced. | No action. |
| **Partial** | Implemented but incomplete (coverage gap, missing documentation, unproven effectiveness, expired evidence). | Remediation plan expected. |
| **Non-compliant** | Control absent or materially deficient. | Treated as a gap; usually a finding in the report. |
| **Not applicable** | Control does not apply to the entity / system. **Justification required.** | Auditors challenge unjustified N/A claims. |
| **Insufficient evidence** | Cannot determine — evidence not produced or not reviewable. | Treated as Non-compliant if not closed. |

Avoid using "Compliant" for controls that exist on paper only. If awareness, training, or effectiveness cannot be demonstrated, the correct status is Partial.

---

## 2. Regulatory risk

How exposed is the entity to regulator action if this gap is not closed?

| Level | Definition | Indicators |
|-------|------------|------------|
| **Critical** | Likely to result in licence action, mandated remediation, or significant fine. | Cited in NCA / SAMA / SDAIA enforcement guidance; statutory notification missed; data residency violated; PDPL sensitive-data exposure; SAMA major incident un-reported. |
| **High** | Likely to be raised as a major finding in inspection, with corrective deadline. | Missing core control mandated by ECC / SAMA CSF / CCC; expired or absent regulator-required artefact. |
| **Medium** | Likely to be raised as a minor finding or recommendation. | Documentation weak, coverage incomplete, control operates but not measured. |
| **Low** | Unlikely to attract regulator attention but still a gap. | Optimisations, naming-convention issues, low-impact gaps. |

Regulatory risk depends on the *regulator's* posture, not just security severity. Missing logging on a non-critical workstation = Low. Missing logging on a SAMA-supervised core banking server = Critical.

---

## 3. Operational risk

What is the cyber / operational impact if the gap is exploited or persists?

| Level | Likelihood × Impact |
|-------|---------------------|
| **High** | High likelihood and / or high impact (loss of life, major outage, mass data loss, material financial loss). |
| **Medium** | Moderate likelihood and / or moderate impact. |
| **Low** | Low likelihood or low impact. |

Operational risk is a security judgement, independent of the regulator. A finding can be **High operational** but **Low regulatory** (e.g. internal pen-test gap with no specific regulator obligation), or **Critical regulatory** but **Low operational** (e.g. missing privacy notice on a low-traffic page that has minimal data exposure but is mandated by PDPL).

---

## 4. Priority

Drives the remediation roadmap. Tied to time, not severity alone.

| Priority | Target | Use for |
|----------|--------|---------|
| **P1** | Before next audit cycle, regulator inspection, or designated event (often 30 days). | Critical regulatory or High operational findings. |
| **P2** | Within 90 days. | High regulatory or Medium operational findings; partial controls needing completion. |
| **P3** | Within next planning cycle (6–12 months). | Medium-rated findings; structural improvements. |
| **P4** | Track only — accept residual risk; revisit at next assessment. | Low-rated findings; optimisations. |

Priority is set after looking at both risk axes together. Resist the urge to mark everything P1 — auditors and remediation teams stop trusting the report.

---

## 5. NCA compliance levels (when reporting against ECC / CCC / DCC / CSCC / OTCC / TCC)

NCA's assessment methodology uses a 1–5 scale per control:

| Level | Label |
|-------|-------|
| 1 | Not implemented |
| 2 | Partially implemented |
| 3 | Implemented |
| 4 | Implemented and documented |
| 5 | Implemented, documented, and effective (assessed) |

Used when a NCA-style scorecard or "Haseen"-style submission is in scope. Map to status as follows: Levels 1–2 → Non-compliant or Partial; Level 3 → Partial (documentation gap); Level 4 → Compliant; Level 5 → Compliant + effective.

---

## 6. SAMA maturity (when reporting against SAMA CSF / IT Governance / BCM)

SAMA expects a 0–5 maturity per subdomain / control:

| Level | Label |
|-------|-------|
| 0 | Non-existent |
| 1 | Ad-hoc |
| 2 | Repeatable but informal |
| 3 | Structured and formalised |
| 4 | Managed and measurable |
| 5 | Adaptive |

SAMA Member Organisations typically target Level 3 minimum, with Level 4 expected on core control areas (IAM, monitoring, incident management, third-party). Track current vs. target separately.

---

## 7. Putting it together — scoring matrix

Use this matrix to set Priority from the two risk axes:

| Operational ↓ / Regulatory → | Critical | High | Medium | Low |
|------------------------------|----------|------|--------|-----|
| **High** | P1 | P1 | P2 | P3 |
| **Medium** | P1 | P2 | P3 | P3 |
| **Low** | P1 | P2 | P3 | P4 |

Override rules:

- If statutory notification has been missed (PDPL 72-hour, SAMA major incident), it is **always P1** regardless of axes.
- If a finding affects designated **critical systems** (CSCC scope), upgrade Priority by one level.
- If a control is required but **uncertain** (insufficient evidence), default to P2 pending verification.

---

## 8. Reporting summary block

Every full assessment should end with:

```
Findings total: 50
Status: Compliant 27 / Partial 14 / Non-compliant 9
Regulatory risk: Critical 2 / High 7 / Medium 20 / Low 21
Operational risk: High 5 / Medium 22 / Low 23
Priority: P1 9 / P2 13 / P3 18 / P4 10
NCA compliance level (avg): 2.8 / 5
SAMA maturity (avg): 2.6 / 5  (target 3.5)
```

Numbers without context are misleading — always pair with the executive summary's posture statement.
