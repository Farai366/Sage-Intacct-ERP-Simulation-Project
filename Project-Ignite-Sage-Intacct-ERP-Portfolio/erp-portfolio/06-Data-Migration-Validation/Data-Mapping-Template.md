# Data Mapping Template — Project Ignite

| Legacy Field | New ERP Field | Transformation Rule | Notes |
|---|---|---|---|
| QuickBooks "Class" (e.g., "Dayton-Fab") | Dimension: Location + Department | Split composite class string into two discrete dimension values | Required regex parsing during extraction; 14 legacy classes mapped to combinations of 3 Locations x 9 Departments |
| QuickBooks "Customer:Job" | Dimension: Customer + Project | Parent "Customer" becomes Customer dimension; "Job" sub-record becomes Project dimension | 240 active jobs migrated; 60 dormant jobs archived, not migrated |
| Shop-floor spreadsheet "Cost Category" (free text, 40+ variants) | Projects: Cost Type | Mapped to standardized 5-value taxonomy (Labor, Material, Overhead, Subcontract, Freight) via lookup table | Required manual review of ~15% of entries with ambiguous categorization |
| QuickBooks Vendor "Vendor Name" + "1099 flag" | Vendor Master: Vendor Name + 1099 Eligible | Direct field mapping; 1099 flag cross-checked against ADP W-9 records | 340 vendor records; 22 duplicates merged during cleansing |
| QuickBooks Customer "Customer Name" + "Terms" | Customer Master: Customer Name + Payment Terms | Direct field mapping; terms standardized to Net 30/45/60 | 180 customer records |
| QuickBooks "Item" (inventory/service items) | Item Master + Item Class dimension | Items re-categorized into 6 Item Class values (Raw Material, Fabricated Component, Assembly Labor, Subcontract Service, Freight, Misc) | 95 active items migrated |
