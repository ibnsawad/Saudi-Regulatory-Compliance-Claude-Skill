# Test 11 — ICT Service Provider / CST CRF RT08 Assessment

## Scenario

A company holds a CST licence as a Managed Security Service Provider (MSSP)
serving both government and private-sector clients in KSA. It has 120
employees, operates a NOC/SOC in Riyadh, and provides remote monitoring
services. It has never undergone a formal CST CRF RT08 assessment and is
unsure which compliance level (CL1 / CL2 / CL3) applies to it.

## Test Prompt

```
We are a CST-licensed Managed Security Service Provider (MSSP) in Saudi Arabia.
We have 120 employees and operate a SOC in Riyadh providing remote monitoring
to government and private clients. We have never done a CST CRF RT08 assessment.
What compliance level applies to us, what are the 6 domains we need to address,
and what are the most critical gaps to close before our first assessment?
```

## Expected Behaviour

The skill should:
1. Classify the entity: CST-licensed ICT Service Provider → CST CRF RT08 primary + ECC-2:2024 + PDPL
2. Determine compliance level: CL2 or CL3 depending on whether any government/CNI clients are served (skill should ask or note the condition)
3. Reference CST CRF RT08 Second Version, October 2023; 6 domains, 25 subdomains
4. Name all 6 CRF domains
5. Flag high-priority gaps for an MSSP: third-party access controls, SOC physical residency requirements, incident reporting to CST, data segregation between clients
6. Note overlap/layering with ECC-2:2024 (all CRF controls are additive to ECC baseline)
7. Note PDPL obligations for personal data processed on behalf of clients (processor role)
8. Distinguish CST CRF RT08 from CST CCRF (RS10 — cloud licensing) — common confusion point

## Scoring Criteria

| Criterion | Weight |
|-----------|--------|
| Identifies CST CRF RT08 as the primary framework (not CCRF) | 25% |
| Explains CL1/CL2/CL3 structure and which level likely applies | 20% |
| Names all 6 domains | 20% |
| Identifies MSSP-specific gaps (client segregation, access controls, incident reporting) | 20% |
| Distinguishes CRF RT08 from CCRF RS10 | 15% |

**Minimum pass score: 70%**
