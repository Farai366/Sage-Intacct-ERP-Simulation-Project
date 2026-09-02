# Configuration Workbook — Project Ignite (Sage Intacct)

| Module | Field | Setting | Value | Rationale | Owner |
|---|---|---|---|---|---|
| GL | Multi-Entity Structure | Top-Level + Subsidiary | Meridian Fabrication Group LLC (Top) / Meridian Precision Components LLC (Sub) | Matches legal entity structure | Jordan Ruiz |
| GL | Fiscal Calendar | Standard 12-period | Jan–Dec, calendar year | Matches existing tax year | Marcus Chen |
| GL | Base Currency | Currency | USD | Single-currency operations | Jordan Ruiz |
| GL | Elimination Entity | Auto-elimination | "MFG-Consolidated-Elim" entity created | Automates intercompany elimination at consolidation | Jordan Ruiz |
| AP | 3-Way Match Tolerance | Threshold | 2% or $25, whichever greater | Balances control rigor with clerk efficiency | Jordan Ruiz / Marcus Chen |
| AP | Approval Workflow Tier 1 | Amount Range | $0–$4,999 | No manager approval required (system auto-approve) | Marcus Chen |
| AP | Approval Workflow Tier 2 | Amount Range | $5,000–$24,999 | Requires Department Manager approval | Marcus Chen |
| AP | Approval Workflow Tier 3 | Amount Range | $25,000+ | Requires CFO approval | Denise Okafor |
| AR | Billing Method | Milestone-based | % complete triggers at 25/50/75/100 | Matches fabrication project billing model | Priya Raman |
| Cash Management | Bank Feed Accounts | Daily auto-feed | 4 accounts (2 per entity: Operating + Payroll clearing) | Supports daily reconciliation objective | Lena Ford |
| Purchasing | PO Approval Threshold | Amount | $2,500+ requires Ops Manager approval | Aligns with existing informal practice, now systematized | Priya Raman |
| Projects | Cost Type Taxonomy | Standard list | Labor, Material, Overhead, Subcontract, Freight | Standardizes previously inconsistent spreadsheet categories | Priya Raman / Aisha Bello |
| Reporting | Dimension Set | 5 dimensions | Location, Department, Project, Customer, Item Class | Enables management reporting cuts required by BRD REQ-008 | Jordan Ruiz |
| Dimensions | Location Values | 3 values | Dayton OH, Waco TX, Reno NV | Matches physical site structure | Lena Ford |
| Dimensions | Department Values | 9 values | Finance, Sales, Ops-Fab, Ops-Assembly, Ops-Shipping, Engineering, Quality, IT, Executive | Matches org chart | Marcus Chen |
