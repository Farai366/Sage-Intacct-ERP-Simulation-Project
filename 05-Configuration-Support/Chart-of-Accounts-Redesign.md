# Chart of Accounts Redesign — Project Ignite

| Account No | Name | Type | Dimension | Notes |
|---|---|---|---|---|
| 1000 | Operating Cash — Dayton | Asset | Location: Dayton OH | Replaces legacy QB account 1010 |
| 1010 | Operating Cash — Waco | Asset | Location: Waco TX | Replaces legacy QB account 1015 |
| 1020 | Operating Cash — Reno | Asset | Location: Reno NV | New account; Reno previously shared Dayton cash account |
| 1200 | Accounts Receivable — Trade | Asset | Entity-level | Consolidated from 3 legacy sub-accounts |
| 1310 | WIP — Fabrication Jobs | Asset | Project (required) | New account; job costing WIP was previously untracked in GL |
| 1500 | Raw Materials Inventory | Asset | Location | Consolidated from site-level inventory accounts |
| 2000 | Accounts Payable — Trade | Liability | Entity-level | Standard |
| 2100 | Intercompany Payable | Liability | Entity-level, eliminates on consolidation | New account to support automated eliminations |
| 4000 | Fabrication Revenue | Revenue | Project, Customer, Department | Replaces 6 legacy revenue accounts, now split via dimensions instead |
| 4100 | Assembly Services Revenue | Revenue | Project, Customer, Department | |
| 5000 | Direct Labor — Fabrication | COGS | Project, Department | Feeds job costing dashboard |
| 5100 | Direct Materials — Fabrication | COGS | Project, Department | |
| 5200 | Subcontract Costs | COGS | Project, Department | New account; previously buried in generic "Outside Services" |
| 6000 | Overhead Allocation | COGS | Project, Department, Location | New allocation account for indirect shop costs |
| 7000 | SG&A — Corporate | Expense | Department: Executive/Finance | |
