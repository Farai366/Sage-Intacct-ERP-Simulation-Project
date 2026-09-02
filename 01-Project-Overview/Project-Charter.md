# Project Charter — Sage Intacct ERP Implementation

**Project Name:** Meridian Fabrication Group — Sage Intacct ERP Implementation ("Project Ignite")
**Client:** Meridian Fabrication Group (MFG)
**Prepared By:** Sarah Whitfield, Engagement Manager, Elevate Consulting Partners
**Date:** January 8, 2026

## 1. Background & Business Need
Meridian Fabrication Group is a custom metal fabrication and light-assembly manufacturer operating out of three sites (Dayton, OH — HQ & Plant 1; Waco, TX — Plant 2; Reno, NV — Distribution Center), generating approximately $85M in annual revenue with 240 employees. MFG currently runs QuickBooks Enterprise for financials, a standalone shop-floor job costing spreadsheet system maintained by the Operations team, and a separate Excel-based consolidation process for multi-entity reporting across its two legal entities (Meridian Fabrication Group LLC and Meridian Precision Components LLC).

This patchwork of systems has led to a 12–15 business day month-end close, no real-time job costing visibility, manual inter-company eliminations, and an inability to produce departmental or project-level P&Ls without significant manual rework. The Board has mandated a move to a scalable cloud ERP ahead of an anticipated private equity minority investment in early 2027, which will require audited, timely, multi-entity financials.

## 2. Objectives
- Improve reporting accuracy and reduce reliance on manual Excel consolidation
- Streamline AP/AR processing, including 3-way PO matching and automated AR cash application
- Reduce month-end close from 12–15 business days to 5 business days within two full close cycles of go-live
- Strengthen internal controls (segregation of duties, approval workflows, audit trail)
- Provide real-time job/project costing visibility to Operations and Sales Engineering
- Establish a multi-entity, multi-dimensional reporting structure to support the 2027 investment readiness review

## 3. Scope
- Sage Intacct Core Financials: General Ledger, Accounts Payable, Accounts Receivable, Cash Management, Order Entry, Purchasing
- Sage Intacct Projects/Job Costing module (replacing the legacy shop-floor spreadsheet tool)
- Multi-entity consolidation across Meridian Fabrication Group LLC and Meridian Precision Components LLC, including inter-entity eliminations
- Dimensional reporting structure: Location (3), Department (9), Project/Job, Customer, Item Class
- Integration with ADP Workforce Now (payroll GL feed) and Salesforce (won-opportunity to sales order)
- Migration of 3 years of historical GL, open AP/AR, active jobs, and customer/vendor master data
- User training and hypercare support for Finance, Operations, and Sales Engineering (approx. 35 named users)

## 4. Out-of-Scope
- Payroll processing (remains on ADP Workforce Now; GL feed only)
- CRM functionality (remains on Salesforce; one-way sales order integration only)
- Shop-floor scheduling/MES functionality (remains on existing FabShop Scheduler; no integration in Phase 1)
- Fixed Assets module (deferred to Phase 2, targeted Q1 2027)
- Historical data prior to FY2023 (available in read-only QuickBooks archive)

## 5. Stakeholders
| Name | Role | Responsibility |
|---|---|---|
| Denise Okafor | CFO, MFG (Executive Sponsor) | Budget authority, final go-live decision |
| Marcus Chen | Controller, MFG (Project Manager) | Day-to-day project ownership, resource coordination |
| Priya Raman | VP Operations, MFG | Job costing/Projects module requirements owner |
| Todd Whitman | Sales Director, MFG | Order Entry & Salesforce integration owner |
| Lena Ford | IT Manager, MFG | Integrations, security, data migration technical lead |
| Sarah Whitfield | Engagement Manager, Elevate Consulting Partners | Implementation delivery lead |
| Jordan Ruiz | Solution Architect, Elevate Consulting Partners | Configuration & integration design |
| Aisha Bello | Data Migration Lead, Elevate Consulting Partners | Data extraction, mapping, load |

## 6. Governance
A Steering Committee (Denise Okafor, Marcus Chen, Sarah Whitfield) meets bi-weekly to review status, budget, and risk. Marcus Chen holds day-to-day project management authority; scope changes above 20 consulting hours or $15,000 require Steering Committee sign-off. Sarah Whitfield escalates delivery risks; Denise Okafor is the final go/no-go decision-maker for go-live.

## 7. Risks & Mitigation
| Risk | Impact | Mitigation |
|---|---|---|
| Legacy job costing data is inconsistently structured across 240+ open jobs | High — delayed migration, inaccurate opening WIP balances | Dedicated 3-week data cleansing sprint with Operations before extraction; Aisha Bello to run validation scripts against job status reports |
| Key Operations SMEs also carry full production responsibilities during Q2 (peak season) | Medium — workshop attendance and UAT participation risk | Schedule workshops in early morning blocks; secure backfill approval from Priya Raman for UAT week |
| Salesforce-to-Intacct integration is a net-new build | Medium — technical risk, timeline risk | Proof-of-concept integration build in Sprint 2 before full workshop cycle; fallback to manual CSV import if POC fails |
| Multi-entity elimination logic is complex (intercompany fabrication transfers) | High — financial reporting accuracy at go-live | Dedicated elimination workshop with Elevate finance configuration lead; parallel-run one full close cycle pre-go-live |
| Change fatigue among AP/AR clerks used to QuickBooks | Medium — adoption risk post go-live | Named "super users" per department; hypercare office hours for first 6 weeks |
