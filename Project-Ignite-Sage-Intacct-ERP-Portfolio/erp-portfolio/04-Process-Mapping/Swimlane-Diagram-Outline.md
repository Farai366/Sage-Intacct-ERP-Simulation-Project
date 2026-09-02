# Swimlane Diagram (Text Outline Version) — Sales Order to Job Kickoff

**Lane: Sales (Salesforce)**
**Lane: Finance (Intacct)**
**Lane: Operations (Intacct Projects)**

| Step | Owner | Description |
|---|---|---|
| 1 | Sales | Opportunity marked Closed Won in Salesforce |
| 2 | Integration (System) | Sales order automatically created in Intacct Order Entry via API |
| 3 | Finance | Controller reviews auto-created sales order for pricing/terms accuracy |
| 4 | Finance | Sales order approved, triggers job shell creation in Projects |
| 5 | Operations | PM assigned to job, enters detailed budget by phase and cost type |
| 6 | Operations | Job status set to "Active," visible on shop floor scheduling reference |
| 7 | Finance | Controller confirms job budget aligns with sales order contract value |
