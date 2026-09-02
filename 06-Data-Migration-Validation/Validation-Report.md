# Data Validation Report — Project Ignite (Pre-Cutover, July 28, 2026)

| Dataset | Records Loaded | Errors | Reconciled? | Sign-off |
|---|---|---|---|---|
| GL Historical (FY2023–FY2025) | 46,210 journal lines | 3 (rounding differences <$1, corrected) | Yes | Marcus Chen, 7/28/2026 |
| Customer Master | 180 | 0 | Yes | Marcus Chen, 7/28/2026 |
| Vendor Master | 340 (originally 362, 22 duplicates merged) | 0 | Yes | Marcus Chen, 7/28/2026 |
| Item Master | 95 | 2 (missing UOM, corrected) | Yes | Lena Ford, 7/28/2026 |
| Active Jobs / Projects | 241 (originally 302, 61 dormant jobs archived) | 4 (budget total mismatches >$500, corrected after Ops review) | Yes | Priya Raman, 7/29/2026 |
| Open AP Balances | $1,847,220.44 total, 212 open bills | 0 | Yes (ties to legacy AP aging) | Marcus Chen, 7/28/2026 |
| Open AR Balances | $2,140,382.17 total, 168 open invoices | 1 (duplicate invoice identified and removed, -$8,400) | Yes (ties to legacy AR aging after correction) | Marcus Chen, 7/29/2026 |
| Opening Trial Balance (both entities) | 2 entities, 214 accounts | 0 | Yes | Denise Okafor, 7/30/2026 |

**Overall Status:** All datasets reconciled and signed off by July 30, 2026, ahead of the August 3, 2026 cutover date. No open discrepancies carried into go-live.
