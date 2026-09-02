# Fit-Gap Analysis — Project Ignite

| Requirement | Fit | Gap | Workaround | Customisation | Notes |
|---|---|---|---|---|---|
| Multi-entity consolidation with eliminations (REQ-001) | Full Fit | None | — | Standard Intacct multi-entity + elimination entity config | No customization needed |
| 3-way PO match with tolerance thresholds (REQ-002) | Full Fit | None | — | Standard Purchasing configuration | Tolerance set at 2%/$25 |
| Real-time job costing by phase and cost type (REQ-003) | Full Fit | None | — | Standard Projects module configuration | Requires disciplined cost type taxonomy |
| Milestone billing tied to % complete (REQ-004) | Full Fit | None | — | Standard billing schedule templates | |
| Salesforce integration for sales order creation (REQ-005) | Partial Fit | No pre-built native connector for MFG's custom Opportunity fields | Manual CSV import fallback for first 30 days if API build slips | Custom REST API integration via Intacct Platform Services | POC required; flagged as Should Have in BRD |
| ADP payroll GL feed (REQ-006) | Full Fit | None | — | Scheduled SFTP file import mapped to GL journal template | Bi-weekly cadence |
| Tiered dollar-based AP approval workflow (REQ-007) | Full Fit | None | — | Standard approval workflow rules | |
| 5-dimension reporting structure (REQ-008) | Full Fit | None | — | Standard Intacct dimensions | |
| 4-account daily bank reconciliation (REQ-009) | Full Fit | None | — | Standard Cash Management bank feeds | Confirm bank supports direct feed for Reno NV account |
| 3-year historical GL migration (REQ-010) | Full Fit | Data volume (~45,000 journal lines) requires staged load | — | Standard historical journal import via Intacct import templates | Load performed in 3 batches by fiscal year |
