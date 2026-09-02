# UAT Test Cases — Project Ignite

| Test Case ID | Scenario | Steps | Expected Result | Actual Result | Status |
|---|---|---|---|---|---|
| UAT-GL-001 | Tag a GL entry with all 5 dimensions | Enter manual journal entry with Location, Department, Project, Customer, Item Class populated | Entry saves and all 5 dimensions appear in the GL detail report | Matched expected | Passed |
| UAT-GL-004 | Consolidated trial balance with intercompany elimination | Post intercompany transaction between the 2 entities; run consolidated TB | Elimination entry auto-posts; consolidated TB nets to zero for intercompany account | Matched expected | Passed |
| UAT-AP-002 | 3-way match within tolerance | Enter PO for $10,000, receive full quantity, enter invoice at $10,150 (1.5% variance) | Invoice auto-matches and routes for approval without exception | Matched expected | Passed |
| UAT-AP-005 | Tiered approval routing | Submit bills at $4,999 / $12,000 / $30,000 | $4,999 auto-approves; $12,000 routes to Dept Manager; $30,000 routes to CFO | Matched expected | Passed |
| UAT-AR-003 | Milestone invoice generation | Update test job to 50% complete | Draft invoice auto-generates for 50% of contract value, routes to Controller for review | Matched expected | Passed |
| UAT-PJ-001 | Real-time job cost visibility | Post a labor time entry and a material PO receipt to test job | Job dashboard reflects updated actual cost within 5 minutes | Matched expected | Passed |
| UAT-CM-001 | Bank feed reconciliation | Import test bank feed file for Reno NV account | Transactions import and auto-match to existing GL entries where applicable | Matched expected | Passed |
| UAT-INT-001 | Salesforce opportunity to sales order | Mark test opportunity Closed Won in Salesforce sandbox | Sales order auto-creates in Intacct within 15 minutes with correct customer/pricing | Order created after 40 minutes due to API batch timing; workaround: reduced batch interval to 10 minutes | Passed w/ Workaround |
| UAT-INT-002 | ADP payroll GL feed import | Import test bi-weekly ADP file | Journal entry posts to GL by department/location and balances to ADP register | Matched expected | Passed |
| UAT-MIG-001 | Historical trial balance tie-out | Pull migrated FY2024 trial balance from Intacct, compare to legacy QuickBooks | Balances tie within $1 per account | Matched expected | Passed |
