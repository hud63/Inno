got it — I dug through both workbooks end-to-end. here’s what they are, what they’re saying, and the most useful trends I found (with numbers).
https://chatgpt.com/c/68e66a08-de7c-8326-9cb4-bb85963e3d3a
# what these files are (big picture)

## 1) **PPT Onboarding QA_v01_2025-10-07.xlsx**

- A structured **intake / onboarding QA dataset** (54 records, 93 fields) capturing clinical, functional, and social needs for new participants.
    
- Most people share a common **Actual Enrollment Date of Oct 1, 2025**; records were originally created between 2021–2025, with the **bulk in 2025**.
    
- The workbook includes a raw data sheet, a (mostly formatting-heavy) pivot, and two control/hidden sheets with **data-validation lists** (e.g., “Yes/No/Needs more information”, Review Status values).
    
- Two fields that look intended for workflow are present but **unused** in the data: **Review Status** and **Completeness Score** (both entirely blank).
    

## 2) **CO- Operations Projections 9-30-2025 8-30-40 PM.xlsx**

- A **roster / pipeline snapshot** of **74 participants** across six centers, with each row holding center, participant, outreach/enrollment owners, address, and **Residence Type**.
    
- A small pivot (“Sheet1”) summarizes **count by center**. Another hidden sheet holds validation lists (statuses and residence types).
    
- Records were **last modified Sep 6–Oct 1, 2025** → the snapshot is fresh.
    

---

# key signals & trends

## 1) Onboarding QA (who’s coming in + what they’ll need)

**Referral mix** (n=54)

- Community-based orgs **33.3%**, Government **27.8%**, Assisted Living **7.4%**, Healthcare Professional **5.6%**, Care Management **5.6%**, others smaller.  
    → You’re sourcing primarily from **community & government channels** (over 60% together).
    

**Clinical / functional risk profile**

- **Mental health diagnosis:** **44.4%** (24/54) report a dx, but only **14.8%** (8/54) are **currently treated** ⇒ **treatment gap = 16/24 = 66.7%** of those with dx not in care.
    
- **Medication adherence:** **14.8%** report **missed meds**.
    
- **Incontinence (non-“none” entries):** **68.5%** (37/54).
    
- **Fall history (non-“none”):** **70.4%** (38/54).
    
- **Durable Medical Equipment requested (actual requests, not “none”):** **44.4%** (24/54).
    
- **Oxygen use (non-“none”):** **11.1%** (6/54).
    
- **Dialysis (non-“none”):** **7.4%** (4/54).
    

**Composite risk** (flags: fall history, incontinence, missed meds, oxygen, dialysis):

- **2+ risk flags:** **66.7%** (36/54)
    
- **3+ risk flags:** **20.4%** (11/54)  
    → Expect a **high-touch cohort** with meaningful safety & ADL support needs.
    

**Home support picture**

- **Home Support Type**: “None Reported” shows most frequently (32 entries), with **In-Home Support Services (6)** and **Unpaid Caregiver (4)** next.  
    → Many arrive **without formal in-home support** in place.
    

**Workload distribution (Outreach Specialists)** _(top 5 by case count)_  
_(cases = #records; avg_risk_flags = mean count of the 5 risk flags above)_

- Dana Lewis — **14 cases**, avg risk **1.50**, **8** with 2+ risk flags
    
- Denise Sanchez — **7**, avg **2.14**, **6** with 2+
    
- Gabriel Townsend — **7**, avg **2.00**, **6** with 2+
    
- Shalise Francoeur — **6**, avg **1.50**, **3** with 2+
    
- Tahara Bailey — **4**, avg **2.00**, **4** with 2+  
    → A few owners hold **higher-risk caseloads**; consider balancing as you assign next steps.
    

**Data quality / structure observations**

- **Review Status** and **Completeness Score** exist but are **entirely blank** → ideal for gating downstream workflows (triage, assignment, QA).
    
- Free-text “none/No/N/A” appears in many comments → **standardize** (single code) to tighten analytics.
    
- Pivot sheet is mostly presentation; the **raw sheet is the truth**.
    

### what this conveys / so what

- You’re about to onboard a **medically and functionally complex cohort**, heavily skewed toward **falls, incontinence, and prior surgeries**, plus a **substantial mental-health treatment gap**.
    
- Expect **DME**, **home-safety**, **continence**, and **fall-prevention** interventions to drive early workload, with **medication adherence** a recurring theme.
    
- Many lack formal home supports → **care navigation**, **IHSS** / home health referrals, and **caregiver linkage** will matter immediately.
    

**Recommended actions (fast wins)**

1. **Make “Review Status” required** (Not Started / Action Needed / Completed) and auto-compute a **Completeness Score** (e.g., % of required fields present).
    
2. **Create a one-click risk score**: +1 each for fall history, incontinence, missed meds, oxygen, dialysis; segment: 0–1 (low), 2 (mod), 3+ (high).
    
3. **Close the MH gap**: auto-flag **dx=yes & treated=no** for **warm hand-offs** to behavioral health within 7 days.
    
4. **Standardize text**: collapse “none / No / N/A” to a single code; add picklists for recurring DME items; make “Home Support Type” a multi-select with definitions.
    
5. **Ops view**: build a **caseload/risk dashboard** by owner and referral source to rebalance high-risk assignments.
    

---

## 2) Operations Projections (where people are + center mix)

**By center** (n=74)

- Lakewood **23.0% (17)** | Thornton **18.9% (14)** | Denver **17.6% (13)** | Loveland **16.2% (12)** | Aurora **12.2% (9)** | Pueblo **12.2% (9)**  
    → **Lakewood + Thornton** together are **~42%** of this cohort.
    

**Residence types** (n=74)

- **Assisted Living 36.5% (27)**
    
- **Apartment – Living Alone 33.8% (25)**
    
- House – w/Family Caregiver 12.2% (9)
    
- House – Living Alone 6.8% (5)
    
- Apt – w/Family Caregiver 5.4% (4)
    
- Other single-digits: Senior Housing, Room/Board, roommate situations.  
    → Nearly **70%** are **Assisted Living or living alone**, each with different logistics:
    
    - AL: facility coordination, med passes, on-site DME installs, cross-org scheduling
        
    - Living alone: **transportation**, home safety, med setup, frequent check-ins
        

**Top residence types by center (quick read)**

- **Aurora:** Assisted Living (6), Apt–Living Alone (1)
    
- **Denver:** Apt–Living Alone (9), Apt–w/Family (2)
    
- **Lakewood:** Assisted Living (8), Apt–Living Alone (7)
    
- **Loveland:** Assisted Living (5), Apt–Living Alone (3)
    
- **Pueblo:** House–Living Alone (3), Apt–Living Alone (2)
    
- **Thornton:** Assisted Living (6), Apt–Living Alone (3)
    

**Recency**

- “Modified On” ranges **Sep 6 → Oct 1, 2025** → the roster is **current**.
    

### what this conveys / so what

- This is the **operational footprint** you’ll staff and schedule against.
    
- **Lakewood, Thornton, Denver** are the main load-bearing centers.
    
- The **mix of AL vs living alone** implies **two different playbooks** you should run in parallel (facility coordination vs home-based logistics).
    

**Recommended actions (fast wins)**

1. **Capacity planning per center**: set staffing thresholds proportional to counts (e.g., RN/SW/OT, transportation slots, DME installs).
    
2. **Separate playbooks** for **Assisted Living** vs **Living Alone** (SLA templates, contact cadence, who-calls-who, escalation trees).
    
3. **Expose “Status”** (Active, Postponed, Cancel, etc. — present on the hidden list) on the main sheet and add **Expected Enrollment Date** to track slippage.
    
4. **Join to QA where possible** (if/when a common ID is available) to **overlay risk** on **center + residence** for smarter routing (e.g., high-risk living-alone → prioritize fall prevention & med setup visits within 72 hours).
    

---

# cross-file takeaways (how to operationalize this)

- **Risk-informed routing:** Use the QA risk score to **sequence first 2–3 weeks** of touchpoints (falls + incontinence + DME + med adherence + MH warm hand-offs).
    
- **Owner load-balancing:** Reassign a few high-risk cases from owners with many 2+-flag members.
    
- **Standardize inputs now:** lock picklists, normalize “none,” surface Review Status, and compute Completeness to improve pivots and dashboards.
    
- **Center-specific SLAs:** Lakewood/Thornton/Denver get **more transportation and DME bandwidth**; Denver’s high “living alone” skew suggests **more wellness checks**.
    
- **Quality & compliance:** Given the PHI-like content, ensure the workbook flows live inside your **HIPAA-aligned** system (audit trail, role-based access).
    

If you want, I can spin up a compact dashboard (risk by owner, center mix, MH-treatment gap, and DME demand) or produce a cleaned CSV with standardized codes—just say the word and I’ll generate it here.