Expanded meeting notes for “1573 InnovAge Commissions Discussion #2” (Oct 8, 2025, 14:04)

Participants/context

- Meeting owner: Mark Newagemedia (InnovAge side)
- Purpose: Finalize commissions structure details, reporting fields, GL coding, invoicing and funding flow, and align on API/status integration timelines; set recurring touchpoints.

Key topics and decisions

1. Commission structure and renewal amounts

- Open item: Confirm full commission structure, including:
    - FMO and agent initial commission amounts
    - Renewal payments at month 13 and month 26
    - State-by-state differences
    - Overrides vs. non-overrides for first-time sales vs. renewals
- Action: Tony to provide the complete fee breakdown. If 2026 rates are available, include them.
- Notes:
    - Payments are effective-dated and follow CMS guidelines; when calendar flips to 2026, rates change.
    - Mark sent a “fill-in-the-blank” table to simplify data collection by state and by payment type (initial/renewal/override).

2. Member center assignment and GL coding for commissions

- Center assignment:
    - At lead intake, center may be unknown; at enrollment, center is known.
    - Safer approach: Use enrollment to confirm center before sending for commissions logic.
    - Consider ZIP-to-center mapping in CRM to pre-assign for visibility; final mapping confirmed at enrollment.
- GL code crosswalk:
    - InnovAge needs a report “by center” listing members paid commissions and including GL codes for the member’s location.
    - Two implementation options for GL code mapping:
        1. Provide an external crosswalk (e.g., “Center A -> these GL codes”) and E123 populates a field with that code.
        2. Bake mapping into CRM and send GL via API back to E123.
    - Faster near-term: InnovAge provides GL crosswalk; E123 stores it in a dedicated field and returns it in monthly reconciliation.
- Field placement:
    - Ensure the GL code is in a field available on the payables/export file used for remittances and reimbursement requests.
    - Include location name + code for easier visual QA when dealing with large volumes (e.g., “Tampa” vs. “Orlando”; multiple sites in VA).
- Action:
    - InnovAge (Mary/Jessica) to send exact ledger codes by center (latest crosswalk).
    - E123 to accept and store GL code in a field that flows into the monthly reconciliation export.

3. Commission statements (agent and FMO) and data fields

- Audience:
    - Agent statement: visible in agent back office; shows only the agent being paid (no upline visibility).
    - FMO statement: shows payments to the FMO.
- Format options:
    - PDF and Excel available. Excel will include more columns; can be trimmed to InnovAge’s needs.
- Columns/labels:
    - Replace internal “E123” terminology with InnovAge-friendly labels.
    - Preferred sequence/labels: FMO, Agent, Participant (Member).
    - Add NPNs:
        - Agent statement: include agent NPN.
        - FMO statement: include FMO NPN (and agent NPN if applicable).
    - Product name: “InnovAge PACE.” Note: In Pennsylvania, product is “LIFE” (cannot change product label dynamically; pulls from configured product).
    - Include payment number context (e.g., Payment 1, Payment 2 after 13 months).
    - Include member details (name, member ID), payee details (name, address), date, amount, credits/debits (for chargebacks inside 90 days).
    - Include location name and GL code in the export for accounting allocation.
- Chargebacks:
    - Debits will reflect clawbacks (e.g., member disengaged within 90 days).
- Actions:
    - E123 to send sample PDF and Excel statements with proposed headers for review.
    - InnovAge (Jane/accounting) to mark up which columns are required; aim to keep agent statement simple: FMO (if applicable), Agent, NPN(s), Participant, Product, Date, Amount, Location, GL code, Total.

4. Invoicing and funding flow

- Funding model:
    - Initial funding (e.g., ~$50k) to a dedicated account; hits InnovAge’s prepaid asset (balance sheet).
    - Subsequent monthly invoices “top off” the account based on expected payouts.
    - Monthly detailed commission statement is used to expense to the correct entity/location via GL coding.
    - Separate the cover invoice (amount only) from the detailed commission statement to avoid auto-upload of detailed rows into AP.
- Vendor setup:
    - The payable entity is “Unified TPA,” separate from Enrollment123; invoice name must match W-9.
    - E123 believes they sent vendor setup package after last meeting; InnovAge to confirm receipt.
    - Actions:
        - E123 to resend the new vendor paperwork and separate W-9 for Unified TPA to Miguel; Miguel to route to Jessica/AP.
        - InnovAge to complete vendor setup, including bank account details (once bank establishes the account).
- Timing targets:
    - First applications received; potential 11/1 commissions.
    - Goal: Have vendor setup + initial invoice processed by next Friday’s payment run if documentation arrives promptly; otherwise by 10/31 at the latest, to ensure funds are ready.
    - Sandy aligns on timeline, with dependency on receiving W-9/vendor details and Tony’s approval.

5. Operational cadence and upcoming meetings

- Weekly commissions/API touchpoint:
    - Purpose: Track commission readiness and adjacent API topics until launch stabilizes.
    - Recurring time: Wednesdays, 9:00 AM Central (7:00 AM Pacific).
    - Accounting attendance: Optional unless there are open questions on amounts/structure or statement fields; accounting can provide feedback via email on statement columns.
- API/status integration (“Integration 2”)
    - Critical path: E123 must return enrollment statuses to enable commission processing.
    - Status field approach:
        - Aim to translate multiple CRM fields into a single status field back to E123; allow a second field if absolutely necessary.
        - Required statuses include “Enrolled” (trigger for commissions) and a clear indicator for “clawback” events (e.g., disenrolled within 90 days).
        - Map “Inactive/Disenrollment Date” to support rule-based clawback identification and full status history.
    - Dependencies: Clarifications after internal hierarchy/status discussions (yesterday and Thursday).
    - Meeting: Friday, 10:00 AM Central (8:00 AM Pacific) with Cody for API status integration. Include Mark.

6. Platform/process notes

- E123 back office creates “transactions” on participants to generate payables matching InnovAge’s commission logic.
- Monthly process:
    - After first-week clearing and prior to the third Wednesday, E123 queries payables for the period, compiles detail and summary, and issues statements and payments.
- First line of support:
    - E123 call center will help agents find/read statements and answer basic “why didn’t I get paid?” questions; escalations go to support as needed.

Open actions summary

- Tony
    
    - Provide full commission structure: FMO/agent amounts, renewals at months 13/26, overrides, and 2026 rates; state-by-state table.
- E123 (Angela/Jess/Jessica/Shayir/Cody)
    
    - Send sample agent and FMO commission statements (PDF + Excel) with proposed headers; include columns for NPNs, product, participant, amounts, location, GL code, credits/debits.
    - Confirm which field will hold GL code and that it appears on payables/export files used for reconciliation and reimbursement.
    - Resend Unified TPA vendor setup package and W-9 to Miguel; ensure invoice name matches W-9.
    - Schedule and attend:
        - Weekly commissions call: Wednesdays, 9:00 AM Central.
        - API/status integration with Cody: Friday, 10:00 AM Central; include Mark.
    - Align status taxonomy and mapping into single field (with history), including “Enrolled” and clawback indicator; map disenrollment date.
- InnovAge (Mark/Miguel/Jane/Jessica/Sandy)
    
    - Send latest center-to-GL crosswalk with exact ledger codes; include location names.
    - Review commission statement samples; confirm minimal required columns and naming; reply via email if possible.
    - Complete vendor setup for Unified TPA upon receipt (W-9, bank info), prioritize for next Friday payment run; Sandy/Jess to process AP.
    - Approve initial invoice amount (Tony) to fund prepaid asset; target payment by next Friday, fallback by 10/31.

Milestones/timelines

- First applications received; potential 11/1 commission cycle.
- Vendor setup + initial funding:
    - Target: Next Friday payment run (if docs are complete), latest by 10/31.
- Recurring commissions/API sync: Wednesdays, 9:00 AM Central.
- API integration working session with Cody: Friday, 10:00 AM Central.

Risks/considerations

- Delay in vendor setup (W-9, bank details) could push initial funding past desired date.
- Status integration must be live before commission processing; ensure history tracking and clear clawback status.
- Ensure product labeling nuances (PACE vs. LIFE in PA) are understood in reports; cannot dynamically rename product label outside configured product.

Requests/clarifications needed

- Confirm whether InnovAge wants both location name and GL code on exports (recommended) and any additional identifiers (entity code).
- Confirm if NPN should be displayed on both agent and FMO statements consistently, and if any privacy concerns exist about showing FMO NPN to agents (current plan: agent statement only shows agent NPN).
- Confirm if chargeback window is strictly 90 days and if any exceptions apply.