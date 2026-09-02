# Defect Log — Project Ignite UAT (July 6–17, 2026)

| ID | Module | Severity | Description | Assigned To | Status |
|---|---|---|---|---|---|
| DEF-001 | Order Entry (Integration) | Sev 2 | Salesforce-to-Intacct sales order creation took ~40 min vs. 15 min target due to default API batch interval | Jordan Ruiz | Resolved — batch interval reduced to 10 min |
| DEF-002 | AP | Sev 3 | Exception queue notification email did not include invoice number in subject line | Elevate Config Team | Resolved — email template updated |
| DEF-003 | Projects | Sev 3 | Job dashboard budget-vs-actual chart mislabeled "Overhead" as "Other" | Elevate Config Team | Resolved — dimension label corrected |
| DEF-004 | Cash Management | Sev 3 | Reno NV bank feed required manual re-authentication after 24 hours | Lena Ford | Resolved — bank connection set to persistent token |
| DEF-005 | GL | Sev 3 | Consolidated TB report did not default to both entities on first run (defaulted to top-level only) | Elevate Config Team | Resolved — default report filter updated |

**Summary:** 5 defects logged, all resolved prior to UAT exit. No Severity 1 defects identified. Formal UAT sign-off obtained July 18, 2026.
