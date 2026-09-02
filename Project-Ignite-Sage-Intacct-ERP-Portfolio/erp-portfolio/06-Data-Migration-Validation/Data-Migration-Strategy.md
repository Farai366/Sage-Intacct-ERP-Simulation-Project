# Data Migration Strategy — Project Ignite

**Scope:** GL history (FY2023–FY2025), open AP/AR balances, active job records (240+), customer master, vendor master, item master, opening trial balance as of cutover date (August 3, 2026).

**Sources:** QuickBooks Enterprise (both entity files), shop-floor job costing spreadsheet (Ops), Salesforce (customer master reference), ADP Workforce Now (vendor 1099 data cross-reference).

**Mapping:** Legacy QuickBooks class/customer/job fields mapped to Intacct dimensions (Location, Department, Project, Customer, Item Class) per the Data Mapping Template. Shop-floor job spreadsheet fields mapped to Intacct Projects cost types per the standardized taxonomy defined in the Configuration Workbook.

**Cleansing:** 3-week dedicated cleansing sprint (weeks of May 4–May 22, 2026) covering: duplicate vendor/customer record merge, standardization of job naming conventions, correction of orphaned job cost entries with no valid GL class, and archiving of 60+ closed/dormant jobs not requiring migration.

**Validation:** Each dataset validated against source system control totals (trial balance, AP/AR aging totals, job budget totals) with sign-off required before load into production. Reconciliation performed by Aisha Bello with independent review by Marcus Chen.

**Sign-off:** Formal written sign-off required from Marcus Chen (Controller) and Priya Raman (VP Operations, for job data) before cutover proceeds. Denise Okafor holds final override authority in case of unresolved discrepancies under $5,000 aggregate.
