# Sage Intacct Setup Package — Meridian Fabrication Group ("Project Ignite")
### For: Implementation Partner / Configuration Consultant

This package gives your ERP implementor everything needed to build Sage Intacct from a blank company through data-ready-for-UAT, in the correct dependency order.

## Start here
Open **`00-Setup-Instructions/Setup-Sequence-and-Instructions.xlsx`** first. It lists all 17 build steps in order, each pointing to the exact file to use, with target week and owner. Every other file in this package is referenced from that sequence — don't jump ahead, since later steps depend on earlier ones (e.g., dimensions must exist before the Chart of Accounts references them).

## Folder Contents
| Folder | Contains |
|---|---|
| `00-Setup-Instructions` | Master build sequence (start here) |
| `01-Company-Entity-Setup` | Company/entity creation, fiscal calendar, locations |
| `02-Dimensions` | Location, Department, Item Class, Customer Type import lists |
| `03-Chart-of-Accounts` | Redesigned COA with required dimensions per account |
| `04-Users-Roles-Permissions` | 35 named users + role definitions + permissions matrix |
| `05-Customers-Vendors-Items` | Customer, Vendor, and Item master import files |
| `06-Projects-Jobs` | Active job import, budget-by-cost-type template, milestone billing schedule template |
| `07-Opening-Balances` | Opening trial balance, open AP bills, open AR invoices (load LAST, after UAT sign-off) |
| `08-Approval-Workflows` | AP tiered approval, PO approval, 3-way match tolerance configuration |
| `09-Integrations-Setup` | Salesforce and ADP field-mapping and test checklists |

## Notes on data completeness
Several import files (Customers, Vendors, Items, Projects, Open AP/AR) show a **representative sample** of rows rather than the full record count, since the complete cleansed dataset lives in separate CSV exports from the legacy-system cleansing sprint (per the Data Migration Strategy). Each file states the full record count and points to the corresponding full export. Use the sample rows to confirm field mapping and formatting before importing the full files.

## Related documents
This package is the *build* companion to the **Project Ignite ERP Implementation Portfolio** (the 11-phase document set covering charter, requirements, UAT, cutover, training, and hypercare). Cross-references to that portfolio (e.g., validation sign-offs, UAT test case IDs) appear throughout these files where relevant.
