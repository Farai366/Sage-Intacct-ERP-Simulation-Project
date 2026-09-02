# Sage Intacct ERP Portfolio Simulation Project

A complete, internally-consistent simulation of a Sage Intacct ERP implementation for a fictional
mid-size manufacturer, **Meridian Fabrication Group**. Built as a reference example / training
resource covering the full lifecycle of a real-world ERP engagement — from project delivery
documentation through to the technical configuration and data-import work an implementor would
actually carry out.

> **Note:** All company names, people, figures, and dates in this project are fictional and
> illustrative. They are built to be internally consistent with each other (same dates, same
> issues, same people) so the material reads as one coherent case study rather than a set of
> disconnected templates.

## Scenario

Meridian Fabrication Group (MFG) is an $85M custom metal fabrication and light-assembly
manufacturer operating two legal entities across three sites (Dayton OH, Waco TX, Reno NV),
migrating from QuickBooks Enterprise and disconnected spreadsheets to Sage Intacct ahead of an
anticipated 2027 private equity investment. The project — "Project Ignite" — runs from kickoff
(January 12, 2026) through go-live (August 3, 2026) to post-go-live stabilization (September 2026),
delivered by a fictional implementation partner, Elevate Consulting Partners.

## Contents

This repository contains two companion packages.

### 1. `Project-Ignite-Sage-Intacct-ERP-Portfolio.zip`

The **project delivery documentation** — 33 documents across the 11 standard phases of an ERP
engagement.

| Folder | Contains |
|---|---|
| `01-Project-Overview` | Project charter, RACI matrix, communication plan |
| `02-Requirements-Gathering` | BRD, FRS, requirements traceability matrix |
| `03-Current-vs-Future-State` | As-Is/To-Be process descriptions, gap analysis, fit-gap analysis |
| `04-Process-Mapping` | BPMN and swimlane outlines, workflow narratives |
| `05-Configuration-Support` | Configuration workbook, chart of accounts redesign, permissions matrix |
| `06-Data-Migration-Validation` | Migration strategy, data mapping, migration templates, validation report |
| `07-UAT` | UAT plan, test cases, defect log |
| `08-Go-Live-Preparation` | Readiness checklist, cutover plan, user access provisioning |
| `09-Cutover` | Cutover execution log, opening balances load report |
| `10-Training-Adoption` | Training plan, quick reference guides, adoption metrics |
| `11-Post-Go-Live-Support` | Hypercare log, stabilisation report, continuous improvement roadmap |

**Use case:** Reference material for ERP project managers, business analysts, or consultants who
want a realistic, end-to-end example of what a fully documented implementation looks like.

### 2. `Sage-Intacct-Setup-Package-Meridian-Fabrication.zip`

The **technical build companion** — a step-by-step Sage Intacct configuration and data-import
package, written as if handed directly to an implementation consultant.

| Folder | Contains |
|---|---|
| `00-Setup-Instructions` | Master build sequence — 17 ordered steps, target week, owner, reference file |
| `01-Company-Entity-Setup` | Legal entity creation, elimination entity, fiscal calendar, locations |
| `02-Dimensions` | Location, Department, Item Class, Customer Type import lists |
| `03-Chart-of-Accounts` | Redesigned COA import file with required dimension tagging |
| `04-Users-Roles-Permissions` | 35 named users, role definitions, permissions matrix |
| `05-Customers-Vendors-Items` | Customer, Vendor, and Item master import files (sample rows) |
| `06-Projects-Jobs` | Active job import, budget-by-cost-type and milestone billing templates |
| `07-Opening-Balances` | Opening trial balance, open AP bills, open AR invoices (load last, post-UAT) |
| `08-Approval-Workflows` | Tiered AP approval, PO approval thresholds, 3-way match tolerances |
| `09-Integrations-Setup` | Salesforce and ADP field-mapping tables, integration test checklist |

**Use case:** A ready-to-adapt configuration and data-import reference for anyone standing up
Sage Intacct — useful as an implementor's build checklist or a starting template to swap in real
company data.

Both packages should be worked through in the order listed in
`00-Setup-Instructions/Setup-Sequence-and-Instructions.xlsx` — later steps depend on earlier ones
(e.g., dimensions must exist before the Chart of Accounts references them).

## How the two packages relate

```
Project-Ignite-Sage-Intacct-ERP-Portfolio.zip   →  what happened, when, and why (delivery narrative)
Sage-Intacct-Setup-Package-Meridian-Fabrication.zip  →  exactly what to configure and import (technical build)
```

The delivery portfolio's Configuration Support, Data Migration, and Cutover documents describe the
same activities the Setup Package operationalizes into concrete import files and instructions —
read the portfolio for context, use the setup package to actually build the system.

## File formats

- Delivery documents: Markdown (`.md`), rendered natively in GitHub
- Import/data files: Excel (`.xlsx`), formatted with header styling and example rows

## Disclaimer

This is a simulated case study for reference, training, and template purposes. It does not
represent any real company, individual, or engagement, and none of the figures should be treated
as real financial or personnel data.
