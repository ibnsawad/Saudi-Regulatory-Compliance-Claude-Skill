# Test 13 — E-commerce Service Provider (CGESP-1:2019 + ECC + PDPL)

## Scenario

A Saudi SME operates an online retail platform selling consumer electronics.
They process payments via a third-party payment gateway, store customer order
history and shipping addresses, and use a cloud-hosted storefront. They have
8 employees and no dedicated IT or security staff.

## Test Prompt

```
We are a small Saudi e-commerce company selling electronics online. We use a
third-party payment gateway, store customer names, addresses, and order history
on a cloud platform, and have 8 employees with no dedicated security staff.
What cybersecurity and data protection obligations apply to us, and what are
the top 10 things we must do first?
```

## Expected Behaviour

The skill should:
1. Classify correctly: SME e-commerce → CGESP-1:2019 (primary awareness framework for SME/SoHo e-commerce SPs) + PDPL (mandatory, processes personal data of KSA residents) + ECC-2:2024 (if NCA-scoped, note scope threshold) + CGEC-1:2019 (implied operator obligations from consumer guideline)
2. Reference CGESP-1:2019 (7 categories, 34 guidelines; note SME vs SoHo scope tags)
3. Cover key obligations: account security, customer data protection, payment security, incident response, third-party vendor management
4. Address PDPL obligations: lawful basis for data collection, retention limits, data subject rights, privacy notice
5. Flag payment gateway due diligence (third-party risk)
6. Note that CGESP is awareness/non-mandatory but strongly encouraged; ECC-2:2024 applies if entity meets NCA scope thresholds
7. Provide a top-10 actionable list appropriate for a small team with no security staff — practical, not overwhelming

## Scoring Criteria

| Criterion | Weight |
|-----------|--------|
| Identifies CGESP-1:2019 and PDPL as primary frameworks | 25% |
| Correctly describes CGESP scope (SME/SoHo tags) | 15% |
| Covers all 7 CGESP categories in assessment | 20% |
| Addresses PDPL obligations specifically | 20% |
| Top-10 list is practical and right-sized for an SME | 20% |

**Minimum pass score: 70%**
