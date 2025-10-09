## 1. Broker Channel Workflow (FMO / e123 Flow)

### Process Overview

1. **New FMO created in e123**
    
2. **Broker logs into e123**
    
3. **Broker contracts and certifies with FMO via e123**
    
4. **Broker submits application/B2C lead**
    
    - Upserts:
        
        - Account
            
        - Contact
            
        - B2C Lead
            
        - Parent–child account relationship
            
        - Taxonomy
            

### Account Channel → Opportunity Type Mapping

1. Non-Contracted Referral Source Account
    
2. Contracted Referral Source Account
    
3. FMO Referral Source Account _(new)_
    

---

## 2. Campaigns System Design

### Key Definitions

|Field|Definition|
|---|---|
|**Trigger**|Event that causes campaign taxonomy or association record to be upserted|
|**Contact Method**|Event or source that created the related record|
|**Campaign ID**|Unique combination of inputs used to create a unique identifier|
|**Campaign Name**|Defaults to Campaign ID until renamed; doesn’t need to be unique|
|**Category**|Overall marketing strategy|
|**Channel**|Setting through which the call-to-action was communicated|
|**Medium**|Platform used to communicate the message|
|**Source**|Marketing tactic that sourced the customer|
|**Content**|Visual and copy used in marketing materials|
|**Term**|Keywords or phrases in paid search|
|**Agent**|Contact that referred the participant lead|
|**Language**|Language used in the marketing copy|

---

### Campaign Taxonomy Examples

#### Digital – Search (Web)

- **Medium:** Web
    
- **Source:** Google
    
- **Content:** InnovAge Landing Page
    
- **Term:** Search Keyword
    
- **Language:** English
    
- **Trigger:** Web Qualifier Tool (UTM embedded)
    

#### Digital – Social (Facebook)

- **Medium:** Web
    
- **Source:** Facebook
    
- **Content:** InnovAge Scroll Ad
    
- **Term:** N/A
    
- **Language:** English
    

#### Traditional – Print

- **Medium:** Phone
    
- **Source:** Newspaper / Brochure
    
- **Content:** “Spring 2024 Tri-Fold”
    
- **Term:** N/A
    

#### Sales – Referral

- **Medium:** Portal / e123
    
- **Source:** Independent Living or Broker Account
    
- **Content:** Account Name
    
- **Language:** English
    

---

## 3. Sales Lead Sub-Process

### Overview

- **Web Qualifier Tool (WQT)** → Lead created in CRM with UTM tracking
    
- **Invoca → Five9 integration** handles call tracking and auto-search for existing lead records.
    

**Decision Flow:**

1. Invoca passes UTM info to Five9
    
2. Five9 searches CRM → if **record exists**, user links it; else, a new lead is created.
    
3. **Campaign Taxonomy Workflow (CampTax)** auto-parses UTM to populate campaign fields.
    

Includes logic for web, phone, chat, and SMS leads.

---

## 4. Participant Pipeline (Field Sales / B2C)

### Primary Stages

1. **New** → Not yet contacted
    
2. **Attempted** → Contact attempt made
    
3. **Contacted** → Lead spoken with, discovery incomplete
    
4. **Intake Scheduled** → Pre-qualified; meeting booked
    
5. **Intake Completed** → Meeting held
    
6. **One Approved** → One related case (Functional / Financial / HSD) approved
    
7. **Two Approved** → Two cases approved
    
8. **Three Approved** → All three approved
    
9. **Enrolled** → Official gross enrollment
    

### Supporting Systems

- **Forms**, **Portal**, **Email**
    
- **Campaigns:** Digital marketing, organic traffic, and awareness partners.
    

---

## 5. Outreach Pipeline (B2B Referral Source Flow)

### Funnel Stages

|Stage|Definition|
|---|---|
|**New**|Lead created; not yet actioned|
|**Attempted**|Sales team attempted contact|
|**Contacted**|Sales team confirmed info (address, phone, email)|
|**Qualified**|Lead appears to be viable referral source|
|**Engage**|Discussion of partnership and expected lead volume|
|**Onboard**|Contract executed; account trained and portal established|
|**Nurture**|Working toward first referral submission|
|**Closed Won**|Referral source produced a participant lead in past 3 months|

**Account Health Categories:**

- _Productive_, _At Risk_, _Critical_, _Former_, _Prospect_
    

**Metrics:**  
Track activity, leads created, enrollments, and cycle times.

---

## 6. Participant Intake Pipeline (Functional, Financial, HSD)

### Shared Case Structure

- **Financial (EFD)**
    
- **Functional (LOC)**
    
- **HSD (Health & Safety Determination)**
    
- **Enrollment**
    

All cases linked to the **Potential Participant (PPT)** record.

---

### Financial Case Stages

1. **New** → Default
    
2. **Ready** → Required attachments complete
    
3. **Submitted** → Sent to third-party agency
    
4. **Action Needed** → Awaiting more info
    
5. **Re-Submitted** → Sent multiple times
    
6. **Approved** → Financially cleared
    

---

### Functional Case Stages (Level of Care)

1. **New**
    
2. **Scheduled** → Appointment booked
    
3. **Assessed** → Assessment performed
    
4. **Ready** → Awaiting submission
    
5. **Submitted** → Sent to certification agency
    
6. **Deferred** → Returned for revision
    
7. **Approved** → Nursing home level of care confirmed
    

---

### HSD (Health & Safety Determination) Stages

1. **New**
    
2. **Ready**
    
3. **Held**
    
4. **Pended**
    
5. **Denied**
    
6. **Approved**
    

**Definition:**  
Evaluates if the participant can safely live under PACE/LIFE model.

---

## 7. Key Field Automation and Flow Logic

- **Last Stage Change Date** → Auto-stamped when status changes
    
- **Days in Stage** → Calculated (Today – Last Stage Change Date)
    
- **Third-Party Submission / Response Dates** → Track Medicaid and LOC submissions
    
- **Counters:**
    
    - HSD Pend/Hold/Denial/Approval
        
    - LOC Assessment Scheduled/Completed/Deferred
        
- **Prior Stage Field:** Tracks historical progression
    

---

## 8. Intake Readiness Checklist

### Demographics

- DOB, Gender, Race, Ethnicity, Marital Status, Contact Info, Assigned Staff
    

### Safe & Stable Home

- Center, Residence Type, Address, Emergency Contact Details
    

### Medical / ADL

- Diagnosis Comments, Behavioral Health Info, VA / Insurance coverage
    

### Medicaid Eligibility

- Verification of all coverage and account details (checking, savings, brokerage)
    

---

## 9. Functional Assessment Workflow (Outlook-Integrated)

### Appointment Scheduling

- Enrollment Rep checks nurse availability via Outlook calendar
    
- Appointment synced to CRM timeline and Outlook
    
- **Counters:** Scheduled, Completed, Cancelled, Rescheduled
    

### Assessment Completion

- Nurse performs assessment → Updates Functional record
    
- System stamps:
    
    - **Assessment Date/Time**
        
    - **Decision Date**
        
    - **Agency Determination**
        

### Determination Outcomes

- Approved
    
- Deferred
    
- Denied
    

**Metrics:**

- Days to Complete Clinical Assessment
    
- Write-ups completed vs pending
    
- Appointment Reschedule Frequency
    

---

## 10. Parking Lot (Future Enhancements)

- Standardize **Denial Letter Workflow**
    
- Add **Deferred Case Flag**
    
- Enhance **Analytics on Stage Duration**
    
- Create **SLUMS Score Field**
    
- Introduce **Role-Based Dashboards (ER / Nurse / HSD)**
    

---

Would you like me to output this as a **single `.md` file** (with clean YAML frontmatter and table of contents for navigation) — or break it into smaller Markdown docs (e.g., `broker-channel.md`, `campaigns-design.md`, `participant-pipeline.md`, etc.) for GitHub documentation structure?