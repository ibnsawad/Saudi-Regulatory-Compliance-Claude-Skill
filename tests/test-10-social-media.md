# Test 10 — Social Media Account Assessment (OSMACC-1:2021)

## Scenario

A Saudi government ministry operates 6 official social media accounts across
X (Twitter), LinkedIn, and Instagram. The accounts are managed by a 3-person
communications team. No formal cybersecurity controls have been applied to
these accounts. A recent phishing attempt targeted the ministry's X account
administrator.

## Test Prompt

```
We are a Saudi government ministry. We operate 6 official social media accounts
(X, LinkedIn, Instagram) managed by our communications team. We have no formal
controls in place. Following a recent phishing attempt on one of our account
administrators, we need to assess our obligations under OSMACC-1:2021 and
identify the highest-priority gaps.
```

## Expected Behaviour

The skill should:
1. Confirm entity classification: government entity → ECC-2:2024 baseline + OSMACC-1:2021 overlay (ECC compliance is a prerequisite for OSMACC)
2. Reference OSMACC-1:2021 (3 domains, 12 subdomains, 15 controls, 38 subcontrols)
3. Identify high-priority gaps including:
   - Account inventory and ownership register (Domain 1)
   - MFA on all account administrators (Domain 2 — directly relevant to phishing incident)
   - Access revocation process for departing staff (Domain 2)
   - Incident response procedure for account compromise (Domain 3)
   - Monitoring for account impersonation (Domain 3)
4. Map findings to ECC-2:2024 controls where overlap exists (§2-2 access controls, §2-13 incident management)
5. Provide a P1/P2/P3 prioritised remediation list
6. Note that OSMACC is mandatory for NCA-scoped entities with official accounts

## Scoring Criteria

| Criterion | Weight |
|-----------|--------|
| Correctly identifies OSMACC-1:2021 as the primary framework | 20% |
| States ECC-2:2024 compliance as a prerequisite | 10% |
| Covers all 3 OSMACC domains in the assessment | 20% |
| Flags MFA gap as P1 given the phishing incident | 20% |
| Provides control references (domain/subdomain level) | 15% |
| Offers a phased remediation roadmap | 15% |

**Minimum pass score: 70%**
