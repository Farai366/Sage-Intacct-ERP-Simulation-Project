# Role-Based Permissions Matrix — Project Ignite

| Role | Module Access | Create | Edit | Approve | View Only |
|---|---|---|---|---|---|
| AP Clerk | AP, Purchasing (view) | Yes (bills, POs under $2,500) | Yes (own unposted entries) | No | GL (view only) |
| AP Manager | AP, Purchasing | Yes | Yes | Yes (bills $5,000–$24,999) | GL, Reporting |
| AR Clerk | AR, Order Entry | Yes (invoices, cash receipts) | Yes (own unposted entries) | No | GL (view only) |
| Controller (Marcus Chen) | GL, AP, AR, Cash Management, Projects, Reporting | Yes | Yes | Yes (journal entries, milestone invoices) | All modules |
| CFO (Denise Okafor) | All modules | Yes | Yes | Yes (bills $25,000+, period close) | All modules |
| Project Manager (Operations) | Projects, Purchasing (job-related) | Yes (job budgets, time entry approval) | Yes (own jobs only) | No | GL (view only, job-filtered) |
| Ops Manager (Priya Raman) | Projects, Purchasing | Yes | Yes | Yes (POs $2,500+, job budget changes) | GL (view only) |
| Sales Rep | Order Entry (view only) | No | No | No | Sales orders (own accounts only) |
| Sales Director (Todd Whitman) | Order Entry | Yes (manual order corrections) | Yes | No | GL, Reporting (sales-related) |
| IT Admin (Lena Ford) | System Administration, Integrations | Yes (user provisioning, integration config) | Yes | No | All modules (audit purposes) |
| Auditor (external, read-only) | GL, AP, AR, Reporting | No | No | No | All financial modules |
