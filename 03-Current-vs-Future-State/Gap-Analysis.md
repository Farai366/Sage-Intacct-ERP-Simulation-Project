# Gap Analysis — Project Ignite

| Current State | Future State | Gap | Recommendation | Owner |
|---|---|---|---|---|
| Manual Excel consolidation across 2 entities | Native multi-entity consolidation in Intacct | No native intercompany elimination rules configured yet | Configure elimination entity and auto-elimination rules during GL build sprint | Jordan Ruiz |
| No 3-way match in QuickBooks | Automated 3-way match in Intacct Purchasing | Vendor master and PO data not currently standardized for matching | Cleanse vendor master data and standardize PO templates before go-live | Aisha Bello / Marcus Chen |
| Job costing lives outside the financial system | Native Projects/job costing module | Legacy job data structure (240+ open jobs) doesn't map cleanly to Intacct project/task/cost-type model | Run job data cleansing workshop with Ops before migration; define standard cost type taxonomy | Priya Raman / Aisha Bello |
| Sales orders manually re-keyed from Salesforce | Automated Salesforce-to-Intacct integration | No existing API integration; Salesforce field mapping undefined | Build and test integration in Sprint 2 POC; document field mapping | Lena Ford / Jordan Ruiz |
| No formal dollar-based approval workflow | System-enforced tiered approval workflow | Approval thresholds not formally documented in current policy | Formalize AP approval policy as part of configuration workshop, obtain CFO sign-off | Marcus Chen / Denise Okafor |
