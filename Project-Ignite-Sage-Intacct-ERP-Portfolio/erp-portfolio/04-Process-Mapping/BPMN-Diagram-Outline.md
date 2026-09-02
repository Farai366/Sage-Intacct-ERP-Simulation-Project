# BPMN Diagram (Text Outline Version) — AP Invoice-to-Pay Process

Start
 → Vendor invoice received (email / AP inbox)
 → System attempts 3-way match (PO, Receipt, Invoice)
   → Decision: Match within tolerance (2% or $25)?
      → YES → Auto-route for approval by dollar threshold
      → NO → Route to AP Clerk exception queue → Clerk resolves discrepancy → Route for approval
 → Decision: Invoice amount tier?
    → Under $5,000 → Auto-approved (no manager review)
    → $5,000–$24,999 → Department Manager approval
    → $25,000+ → CFO approval
 → Decision: Approved?
    → YES → Bill posted to AP, scheduled for payment run
    → NO → Returned to AP Clerk with rejection note → back to exception queue
 → Payment run executed (ACH/check) per weekly schedule
 → Remittance sent to vendor
End

---

# BPMN Diagram (Text Outline Version) — Job/Project Costing Flow

Start
 → Job created in Projects module (linked to won Sales Order)
 → Budget entered by phase and cost type (Labor, Material, Overhead, Subcontract)
 → Decision: Cost transaction type?
    → Labor → Time entry posted by employee → Cost allocated to job/phase
    → Material → PO receipt posted → Cost allocated to job/phase
    → Subcontract → AP bill coded to job/phase → Cost allocated to job/phase
 → Real-time budget-vs-actual dashboard updates
 → Decision: Job reaches billing milestone (25/50/75/100%)?
    → YES → Draft milestone invoice auto-generated → Controller review → Invoice released to customer
    → NO → Continue cost tracking
 → Decision: Job marked complete?
    → YES → Final billing, job closed, variance report generated
    → NO → Continue cost tracking
End
