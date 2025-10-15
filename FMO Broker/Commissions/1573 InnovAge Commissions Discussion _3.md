
Wed, 15 Oct 25

### Bank Form Status Update

- Unified TPA currently waiting on one form from bank to complete 50K account funding setup
    
    - Parent company E123 recently moved their banking to new institution
        
    - New bank refusing to rubber-stamp previously approved documentation
        
    - Requiring complete re-verification of all corporate information including officer lists
        
- E123 owner estimates one-day completion once all required documents submitted
    
    - Working directly with E123 to gather comprehensive officer documentation
        
    - Banking relationship complications causing delays in standard processing
        
- Critical timeline: form submission required by Friday 17th to meet Tuesday 21st drop-dead date
    
    - Payment processing needs full Tuesday to issue funds by Thursday 24th target
        
    - Vendor master setup taking longer than usual, requiring early submission
        

### Commission Statement Format Confirmation

- FMO commission statement design approved with specific layout requirements
    
    - InnovAge logo placement in header confirmed
        
    - Agent information includes: agent ID, FMO name, FMO NPN
        
    - Broker details: name, ID, and NPN for transparency
        
    - Product display: “Pace by InnovAge” (full name when space permits)
        
    - Transaction details: payment number (always 1 for first year, 2 for second year), credit/debit status
        
- Broker statement mirrors FMO format but excludes upline/FMO information
    
    - Only shows direct sales relationship participants
        
    - Same transaction and member detail structure
        
- Angela requested addition of activation/renewal date field
    
    - Purpose: customer service triangulation for duplicate member names
        
    - Helps agents understand payment timing (e.g., “enrolled November, paid in December”)
        
    - Reduces support calls by clarifying enrollment-to-payment cycles
        
    - Angela to verify technical feasibility with existing data table structure
        

### GL Code Integration Requirements

- Outstanding deliverable: updated crosswalk for locations and GL codes
    
    - Previous version outdated due to entity structure changes
        
    - GL codes vary by California entity and location combinations
        
- Jane committed to providing streamlined version today
    
    - Three-column format required: entity, GL code, location (specific sequence)
        
    - Data structure: alphabetic entity, numeric GL, numeric location
        
    - GL codes consistent (expense side), but location numbers change by entity
        
- Angela’s development team requires immediate access for CRM integration
    
    - Backend coding depends on accurate GL mapping
        
    - E123 compatibility requires proper location/GL tagging
        
    - Cross-referencing capability needed for commission processing
        

### Commission Payment Rules Clarification

- Payment rate structure definitively confirmed based on commission year
    
    - Example 1: Enrolled 11/01/25, commission paid 11/19/25 → 2025 rates apply
        
    - Example 2: Renewed 11/01/26, paid December → 2026 renewal rates apply
        
    - Example 3: Enrolled 01/01/26, renewed 01/01/27 → 2027 rates apply
        
- Three-month clawback policy finalized with specific scenarios
    
    - Rule: If member remains active for three full months, no clawback occurs
        
    - Scenario 1: Enrolled 11/01, disenrolls 01/31 → clawback (only 2 months active)
        
    - Scenario 2: Enrolled 11/01, disenrolls 02/28 → no clawback (3 months completed)
        
    - InnovAge receives three monthly payments from CMS, meeting broker obligation threshold
        
- Death exception handling initially maintained as clawback
    
    - Disenrollment reason codes will be captured in second API development
        
    - Policy may be revised after implementation based on operational experience
        
    - Industry practice varies; erring on side of consistent clawback for now
        
- Clawback timing: immediate processing upon disenrollment notification
    
    - No waiting period once three-month threshold determination made
        
    - Applies to both FMO and broker commission levels
        
- Renewal commission exclusion confirmed: no clawbacks on renewal payments per Sherry’s email directive
    

### Next Steps

- Angela: Update commission statement samples with activation date fields, circulate for written approval today
    
- Jane: Deliver finalized GL code crosswalk with entity/GL/location mapping today
    
- InnovAge team: Submit complete vendor setup package, W-9, and invoice by Friday 17th
    
    - All documentation required simultaneously for Tuesday 21st processing deadline
        
    - Payment target remains Thursday 24th pending timely submission
        
- Development coordination: Shayir to incorporate participant ID, entity, GL code, and location code requirements
    
- Cody integration: Ensure disenrollment reason codes included in second API specification
    
- Next meeting: Tuesday October 21st, 7AM Pacific (drop-dead date status verification)
    

---

Chat with meeting transcript: [https://notes.granola.ai/d/566eb704-8e6c-49dd-8483-8661b8360881](https://notes.granola.ai/d/566eb704-8e6c-49dd-8483-8661b8360881)