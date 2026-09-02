# Migration Templates — Project Ignite

## Customer Migration Template
| Field | Value (example) | Required? | Notes |
|---|---|---|---|
| Customer ID | CUST-0142 | Yes | Auto-generated sequential ID |
| Customer Name | Halbrook Industrial Supply | Yes | |
| Billing Address | 4820 Commerce Dr, Columbus, OH 43215 | Yes | |
| Payment Terms | Net 45 | Yes | Standardized during cleansing |
| Assigned Sales Rep | T. Whitman | No | Defaults to house account if blank |
| Credit Limit | $150,000 | No | Pulled from legacy QuickBooks customer limit field |

## Vendor Migration Template
| Field | Value (example) | Required? | Notes |
|---|---|---|---|
| Vendor ID | VEND-0087 | Yes | Auto-generated sequential ID |
| Vendor Name | Buckeye Steel Supply Co. | Yes | |
| 1099 Eligible | Yes | Yes | Cross-checked against ADP W-9 |
| Payment Terms | Net 30 | Yes | |
| Default GL Account | 5100 — Direct Materials | No | |

## Item Migration Template
| Field | Value (example) | Required? | Notes |
|---|---|---|---|
| Item ID | ITEM-0056 | Yes | |
| Item Name | 3/8" Cold Rolled Steel Sheet | Yes | |
| Item Class | Raw Material | Yes | Mapped per new taxonomy |
| Unit of Measure | SqFt | Yes | |

## Project Migration Template
| Field | Value (example) | Required? | Notes |
|---|---|---|---|
| Project ID | JOB-2026-0118 | Yes | Legacy job number preserved as reference |
| Project Name | Halbrook — Conveyor Frame Assembly | Yes | |
| Customer | Halbrook Industrial Supply | Yes | |
| Budget (Total) | $284,500 | Yes | Migrated from shop-floor spreadsheet, validated against sales order |
| Status | Active | Yes | Only active/in-progress jobs migrated |

## Opening Balances Template
| Field | Value (example) | Required? | Notes |
|---|---|---|---|
| Account | 1200 — Accounts Receivable Trade | Yes | |
| Entity | Meridian Fabrication Group LLC | Yes | |
| Opening Balance (as of 8/3/2026) | $2,140,382.17 | Yes | Ties to legacy AR aging report control total |
