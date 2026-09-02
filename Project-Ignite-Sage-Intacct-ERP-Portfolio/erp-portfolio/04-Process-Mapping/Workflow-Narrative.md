# Workflow Narrative — Project Ignite

## Process: Month-End Close
**Trigger:** Last business day of the month (calendar-driven, automated reminder to Controller)
**Steps:**
1. AP/AR sub-ledgers closed by respective clerks; period locked for new sub-ledger entries
2. Automated ADP payroll GL feed imported and reviewed for both entities
3. Bank reconciliations completed for all 4 operating accounts via Cash Management feeds
4. Intercompany transactions reviewed; automated elimination entries verified
5. Controller runs consolidated trial balance report across both entities
6. Standard report package (P&L by location/department, Balance Sheet, job cost summary) generated from Intacct dashboards
7. CFO reviews and approves close; period locked in system
**Outputs:** Consolidated financial statements, job cost variance report, board reporting package
**Controls:** System-enforced period lock; segregation of duties between preparer (Controller) and approver (CFO); full audit trail of all adjusting entries

## Process: Milestone Billing
**Trigger:** Job reaches a pre-defined percent-complete milestone (25/50/75/100%) as updated by PM in Projects module
**Steps:**
1. PM updates job percent-complete in Intacct Projects based on shop floor progress
2. System auto-generates a draft milestone invoice per the job's billing schedule
3. Controller reviews draft invoice against job budget and contract terms
4. Controller releases invoice; system sends to customer via Intacct AR
5. Cash application occurs automatically upon customer payment via bank feed matching
**Outputs:** Customer invoice, updated AR aging, job cost-to-billing reconciliation
**Controls:** Draft-to-approved workflow requires Controller sign-off before customer-facing invoice is released; job budget variance flagged if billing exceeds budget threshold
