# Functional Requirements Specification (FRS) — Project Ignite

| Req ID | Functional Requirement | Acceptance Criteria | Module | Dependency |
|---|---|---|---|---|
| FR-001 | Configure multi-entity structure with Meridian Fabrication Group LLC as top-level and Meridian Precision Components LLC as subsidiary | Consolidated trial balance produces correct eliminations for a test intercompany transaction | GL | REQ-001 |
| FR-002 | Configure 3-way match rules in Purchasing/AP with $500 threshold and tolerance of 2% or $25 (whichever greater) | Test PO/receipt/invoice trio with $10 variance auto-approves; $50 variance routes to exception queue | AP | REQ-002 |
| FR-003 | Configure Projects module with budget entry by job, phase, and cost type (labor, material, overhead, subcontract) | Test job shows real-time budget-to-actual variance within 5 minutes of a cost transaction posting | Projects | REQ-003 |
| FR-004 | Configure milestone billing schedules linked to project percent-complete | Test job generates correct milestone invoice at 25/50/75/100% triggers | AR/Billing | REQ-004 |
| FR-005 | Build Salesforce-to-Intacct integration using Intacct's REST API to create sales orders on Opportunity Stage = Closed Won | Test opportunity in Salesforce sandbox creates matching sales order in Intacct sandbox within 15 minutes | Order Entry | REQ-005 |
| FR-006 | Build scheduled SFTP import of ADP GL summary file into Intacct GL journal entries | Bi-weekly test file imports without manual intervention and balances to ADP payroll register | GL | REQ-006 |
| FR-007 | Configure AP approval workflow: $5,000–$24,999 requires Department Manager; $25,000+ requires CFO | Test bills at $4,999 / $5,000 / $25,000 route correctly per threshold | AP | REQ-007 |
| FR-008 | Configure dimension structure: Location (3 values), Department (9 values), Project, Customer, Item Class | Sample GL entry can be tagged with all 5 dimensions and reported on individually | GL/Reporting | REQ-008 |
| FR-009 | Configure daily bank feed connections for 4 operating accounts (2 per entity) | Bank feed successfully imports test transactions for all 4 accounts | Cash Management | REQ-009 |
| FR-010 | Migrate FY2023–FY2025 GL detail into Intacct as historical journal entries | Trial balance for each historical period ties to legacy QuickBooks trial balance within $1 | GL | REQ-010 |
