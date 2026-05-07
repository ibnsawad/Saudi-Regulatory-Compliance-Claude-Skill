# Test 09 — Incident & Breach Notification Routing

## Eval purpose

Confirm the skill correctly **routes notifications** across SAMA, SDAIA, NCA, CST, NDMO, and customers depending on entity type and incident category. This is a frequent real-world question and a high-stakes one for clients.

---

## Scenario

The user provides three short incident vignettes and asks "what do we have to notify, to whom, and by when?".

### Vignette A — Bank ransomware

A SAMA-licensed bank's **branch back-office segment** is hit by ransomware overnight. ATM and online banking unaffected. ~3,000 employee endpoints encrypted. Personal-data exposure suspected for an internal HR file share. Bank discovers the incident at 02:30; the user is asking at 09:00 the same day.

### Vignette B — Government portal data leak

A ministry's public-facing service exposes ~120 citizens' national-ID + mobile due to a misconfigured object-storage bucket. Discovered by a security researcher and reported to the ministry on a Saturday at 16:00; user is asking on Sunday morning.

### Vignette C — CSP customer-impacting outage

A CST-licensed CSP suffers a regional outage affecting 40 KSA business customers for 6 hours; no data loss confirmed but customer-data integrity not yet verified.

---

## Expected skill behaviour

### A. Vignette A — bank ransomware

- **SAMA Cyber Incident Reporting Procedure** — major incident: verbal notification immediately to SAMA CTI; written report within stipulated window (skill should state it is short and that the user must verify the exact current window in the SAMA procedure rather than guess).
- **PDPL Implementing Regs** — if HR personal-data exposure is **confirmed or likely to cause harm**, notify SDAIA within **72 hours** of awareness. Notify affected employees if high risk.
- **NCA** — significant cyber incident reporting per sectoral procedure and any flow-down through SAMA-NCA coordination.
- **Customer notification** — only if customer data implicated; HR file share suggests employee data, but verify scope before excluding customer impact.
- **Internal**: invoke incident-response plan; preserve forensic evidence; consider law-enforcement notification if extortion involved.

### B. Vignette B — government portal data leak

- **PDPL Implementing Regs** — 72 hours to SDAIA. Notify affected data subjects without undue delay if high risk.
- **NDMO** — government data incident reporting per central procedure.
- **NCA** — significant incident reporting per government sectoral procedure.
- **Sectoral overlay** — depending on the ministry, additional reporting may apply (e.g. Ministry of Health's central reporting if health data; CCC overlay if cloud-hosted).
- **Public communication** — assess whether public statement is required; coordinate with regulator messaging.

### C. Vignette C — CSP outage

- **CST CCRF** — service-disruption notification to CST per licence conditions.
- **Customers** — customer-notification per CCRF customer-protection obligations and contractual SLAs.
- **NCA** — if the incident meets the cyber-incident threshold (integrity not yet verified is a flag).
- **PDPL / SDAIA** — only if personal-data integrity is later confirmed compromised. The skill should note that lack of confirmation is itself a risk; investigate before stand-down.

### D. Output expectations

- One section per vignette with: regulators in order, contact route, statutory window, content of notification, evidence to preserve, follow-up reporting.
- Honest treatment of timeline gaps: if the skill is unsure of the exact SAMA written-report window or NCA sectoral-procedure timeline, it should say so and ask the user to verify against the live procedure.
- A short summary table at the top:

| Vignette | SAMA | SDAIA | NCA | CST | NDMO | Customer |
|----------|------|-------|-----|-----|------|----------|
| A — Bank ransomware | Verbal now; written per procedure | 72h if PII confirmed | Sectoral | — | — | If customers impacted |
| B — Government leak | — | 72h | Sectoral | — | Per central procedure | Affected citizens |
| C — CSP outage | — | If PII confirmed | If cyber-incident threshold met | Per licence | — | Per CCRF + SLA |

---

## Pass criteria

Skill **passes** if it:

1. Routes each vignette to the correct combination of regulators.
2. Flags the **PDPL 72-hour** clock from the moment of awareness, not from confirmation.
3. Reminds the user that SAMA verbal-then-written sequence applies for major incidents and that the skill cannot guarantee the current exact written-report timeline (verify against the live procedure).
4. For Vignette C, treats **integrity-not-yet-verified** as itself a risk — pushes for investigation before assuming no PDPL / NCA scope.
5. Surfaces internal preservation / forensic obligations in addition to external notifications.
6. Does not assume customer notification is required everywhere — distinguishes customer-personal-data exposure from internal employee data.

Skill **fails** if it:

- Gives a single one-size-fits-all timeline (e.g. "always 72 hours").
- Confidently quotes a specific SAMA written-report window without flagging that it must be confirmed.
- Tells the bank it does not need to notify SDAIA because employee data isn't customer data (PDPL covers employee personal data too).
- Tells the CSP it does not need to notify CST because no data loss is confirmed (CCRF covers service disruption irrespective of data loss).
