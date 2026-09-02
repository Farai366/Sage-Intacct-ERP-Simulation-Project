# Business Requirements Document (BRD) — Project Ignite

## Section 1: Introduction
**Purpose:** This BRD captures the business requirements for MFG's migration from QuickBooks Enterprise and ancillary spreadsheet tools to Sage Intacct, covering General Ledger, AP, AR, Cash Management, Order Entry, Purchasing, and Projects/Job Costing.

**Scope:** Financial operations across both legal entities (Meridian Fabrication Group LLC, Meridian Precision Components LLC) and all three sites (Dayton OH, Waco TX, Reno NV).

**Assumptions:**
- MFG will provide dedicated SME time from AP, AR, Operations, and Sales for workshops and UAT
- Salesforce administrator access will be granted to Elevate's integration developer for the duration of the build
- Historical data prior to FY2023 will remain accessible in a read-only QuickBooks archive and is not in scope for migration

## Section 2: Business Processes
- **General Ledger:** Multi-entity chart of accounts, monthly close, intercompany eliminations, budget vs. actual reporting
- **Accounts Payable:** Vendor bill entry, 3-way PO match for inventory/materials purchases, ACH and check payment runs, 1099 tracking
- **Accounts Receivable:** Progress billing on fabrication jobs, milestone invoicing, cash application, aging and collections reporting
- **Billing:** Contract/T&M billing for custom fabrication projects tied to job costing
- **Projects/Job Costing:** Real-time job cost tracking (labor, materials, overhead) against budget, by job and by phase
- **Cash Management:** Multi-bank reconciliation across 4 operating accounts, cash forecasting

## Section 3: Requirements
| Req ID | Description | Priority | Module | Notes |
|---|---|---|---|---|
| REQ-001 | System shall support consolidated and standalone reporting for 2 legal entities with automated intercompany elimination | Must Have | GL | Core driver for PE readiness |
| REQ-002 | System shall support 3-way match (PO, receipt, invoice) for materials purchases over $500 | Must Have | AP | Current process is fully manual |
| REQ-003 | System shall allow job-level budget vs. actual cost tracking updated at least daily | Must Have | Projects | Replaces shop-floor spreadsheet |
| REQ-004 | System shall support progress/milestone billing tied to job completion percentage | Must Have | AR/Billing | ~60% of revenue is milestone-billed |
| REQ-005 | System shall integrate with Salesforce to auto-create a sales order upon opportunity close-won | Should Have | Order Entry | POC required before commit |
| REQ-006 | System shall receive a summarized payroll journal entry feed from ADP Workforce Now by department and location | Must Have | GL | Bi-weekly feed |
| REQ-007 | System shall support role-based approval workflows for AP bills over $5,000 (manager) and over $25,000 (CFO) | Must Have | AP | Controls requirement |
| REQ-008 | System shall provide a dimensional reporting structure by Location, Department, Project, Customer, and Item Class | Must Have | GL/Reporting | Needed for management reporting |
| REQ-009 | System shall support bank reconciliation across 4 operating bank accounts with daily transaction feeds | Must Have | Cash Management | |
| REQ-010 | System shall retain a minimum 3-year rolling GL history natively in the new system | Must Have | GL | |

## Section 4: Pain Points
- Month-end close currently takes 12–15 business days due to manual consolidation in Excel
- Job costing is tracked in a shop-floor spreadsheet that is frequently out of sync with GL by 5–10 days
- No automated 3-way match; AP clerks manually compare paper POs to invoices
- Intercompany transactions between the two entities are tracked and eliminated manually, introducing error risk
- Sales orders are re-keyed manually from Salesforce into QuickBooks, taking 1–2 days per large order
