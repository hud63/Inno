# Ppt Onboarding Data/Indicators

Tue, 07 Oct 25

Data Dashboard - 

https://app.powerbi.com/groups/me/apps/0f6ace48-b0b6-46e2-8059-3d5022a2b131/reports/37ad588a-c184-4182-9a8a-6e1bbe511f75/99299c3377174c69c3c1?experience=power-bi

**From:** Anthony Horner **Sent:** Friday, September 26, 2025 3:18 PM **To:** Edgar Cooney <ECooney@innovage.com>; Shadie Qaqish <SQaqish@innovage.com>; Priya Gupta <PGupta@innovage.com>; Megan Elliott <MElliott@innovage.com>; Kristen Kennedy <KKennedy@innovage.com>; Nick Armstrong <NArmstrong@innovage.com> **Cc:** Matthew Kidwell <MKidwell@innovage.com>; Matt Huray <MHuray@innovage.com> **Subject:** Proposal: Attrition Rate by Living Situation

Hi Edgar, Team,

Thank you for today's discussion on the participant onboarding project. I introduced a metric that I believe could deliver meaningful insights across the organization. It was suggested I bring this idea to Edgar to further the idea along. I've attached a mock-up in Excel for reference (see attached).

My goal is to evolve this concept into a **systematically updated KPI: Attrition Rate by Living Situation**. We know that transitions have different implications. An independent senior moving to assisted living carries a different economic and care impact than a skilled nursing resident disenrolling altogether. By tracking attrition through this lens, we can make better decisions about both care planning and financial outcomes.

I'd like to **tap into our Business Intelligence resources** to automate this metric and **publish the data in a way that's easily consumable by all levels of the organization, spanning front-line teammates thru senior leadership**.

Looking at this data by **participant tenure** in the past revealed even deeper insights (if my memory serves):

- Six-month care plan reviews correlated with spikes in IND → ALF and IND → SNF moves.
- Early disenrollments looked very different when comparing new IND participants versus new ALF participants.
- Add filters to uncover deeper insights (e.g., last service request, total grievances, anything else worth considering, etc.).

Building this KPI into our standard reporting could give us the visibility we need to refine onboarding and care processes at scale.

# Ppt Onboarding Data/Indicators

Tue, 07 Oct 25

### Current Disenrollment Data & Challenges

- No vanilla ice cream solution yet for center directors
    
    - Can’t see disenrollments on a time series chart; need an always-available KPI dashboard at center and participant levels
        
    - Without this core element, downstream correlation/causation work won’t stick operationally
        
- Key derivatives needed on the dashboard: controllable vs non-controllable, death, hospice-related
    
- Disenrollment by living situation is a critical gap to fill
    
    - Prior analysis (Nick Armstrong, ~1 year ago) showed step changes in disenrollment and unit economics across living situations
        
    - Nursing home (SNF) residents → lose money; Assisted Living (ALF) → roughly break-even; Independent living → profit center
        
    - Center directors need to see trends over time and drill into names to resolve disputes (link to CRM records)
        

### Proposed Disenrollment Prediction Framework

- Five main buckets for analysis and early warning:
    
    - Grievances
        
        - Lagging indicator; often after the fact and many participants leave silently without filing
            
    - Transportation (biggest bucket now)
        
        - Factors: travel distance/time from center, participants per trip, early/late pickups, number of canceled/missed rides
            
        - Repeat cancellations predict future cancellations; distinguish patient-driven vs center-driven; prior-day vs same-day
            
    - Change in condition (acuity/risk)
        
        - Signals: inpatient velocity, ER visit velocity, SNF days, faster cadence of claims, higher care intensity
            
        - Indicates moving toward uncontrollable disenrollment (e.g., end-of-life) or that the plan of care isn’t working
            
    - Appointments (center, external, home)
        
        - Track missed/late/no-shows, reschedule frequency and reasons, who was unavailable (transport, provider, patient)
            
        - “Schedules per appointment” as a friction metric; higher count = more abrasion/less leeway from patients
            
    - Patient touch points and service responsiveness
        
        - Care plan completion and timeliness, SDRs submitted, response speed/quality, overall contact cadence
            

### Living Situation Impact Analysis

- Strong correlation between living situation and retention/economics
    
    - Independent living: primary profit source; focus on maximizing duration in this state
        
    - Assisted Living: near break-even
        
    - SNF: negative margin; less concern when SNF residents cancel
        
- Participants progress through acuity over time (e.g., shift from independent to ALF around months 6–7, and ALF to SNF)
    
    - Six-month care plan cadence likely drives observed tenure-based transitions
        
    - Priority: instrument “participant + month” to understand tenure, lifetime value, and economic pull-through by living situation
        

### Data Infrastructure & Accessibility

- Existing Power BI environment with a hardened CRM data model (incl. disenrollment reasons/flavors)
    
    - Owner/contact: Alan Rodriguez (RevOps analyst) for access; likely in a “Revenue Operations” workspace
        
    - Many legacy dashboards exist; reuse dataset vs. rebuilding; include deep links to CRM records to eliminate name disputes
        
- Required granularity: participant + month (to handle time-varying attributes like living situation and care team)
    

### Early Warning Indicators Discussion

- Focus on months 1–4/5 post-enrollment (gradual decline, then leveling)
    
    - Target voluntary disenrollments in early months vs. capricious “rapid” disenrollments
        
- Candidate early measures
    
    - Time to first appointment scheduled and first-appointment show rate
        
    - Time to care plan completion (regulatory within first month, but downstream access lags matter)
        
    - Touchpoint cadence during the enrollment handoff gap (often ~3 weeks before services start on the 1st)
        
    - Time to key specialty services (e.g., dental, podiatry, optometry)—time to 3rd/4th appointment may be more stabilizing than time to 1st
        

### Transportation & Geographic Factors

- Hypotheses to test
    
    - Disenrollment/attendance vs. drive time and distance from center; van ride time is a common complaint
        
    - Map participants by distance bands; consider time-of-day traffic (8AM vs 2PM) for true catchment
        
    - Assess show rate and cancellation rate vs. travel metrics; evaluate “participants per trip” saturation effects
        
- Operational implications
    
    - Deprioritize outreach far from centers if retention drops beyond a threshold (e.g., >45 minutes)
        
    - Set expectations upfront for long-ride participants; reconsider aggregator partners that source distant prospects
        

### Care Team & Provider Analysis

- Need effective-dated care team assignments in Epic; otherwise back into history via appointment/provider data
    
- Explore directional signals (sample sizes may be small)
    
    - Discipline impact: PCP vs social work vs dietitian vs rehab on no-shows/disenrollment
        
    - Individual provider effects (e.g., bedside manner differences) acknowledging low N and outlier risk
        
    - Compare outcomes when specific disciplines are engaged (e.g., dental as a potential retention lever)
        

### Hospice & End-of-Life Nuances (esp. California)

- Frequent voluntary disenrollments to hospice due to discharge teams/facilities recommending hospice
    
    - Participants may not realize enrolling in hospice revokes PACE benefits
        
    - Outside CA: Comfort Care Team (CCT) via VANS approximates hospice; CA lacks home services license → gap in 24/7 support
        
    - Facilities may push hospice to secure extra nursing; creates friction with PACE recommendations
        
- Consider tracking “end-of-life support gap” and education touchpoints to reduce inadvertent disenrollments
    

### Food Quality & Day Center Utilization

- Recurrent complaints about food quality; hypothesis: modest spend increase/more options could reduce churn
    
    - Explore offering multiple hot options and greater choice/control
        
- Day center attendance: belief it improves retention and lowers costs is unproven; prior piecemeal looks didn’t confirm
    
    - Test relationship between day center utilization and retention/costs; control for acuity and home care hours
        

### Home Care Hours & Caregiver Dynamics

- Pre-PACE home care hours and expectations influence satisfaction
    
    - Participants often trimmed from prior plan’s hours (e.g., 40 → 20); consider a threshold (e.g., 30) that retains without overproviding
        
    - Reduce the “no hours” window between enrollment and care plan; prioritize early home care for high-need entrants
        
- Capture support-at-home context
    
    - Caregiver present? Lives with participant? POA on file?
        
    - POA-driven referrals convert ~3x vs self-referrals; test whether POA presence correlates with retention
        

### Referral Source & Channel Effects

- Track outcomes by channel (paid ads, outreach, senior centers, APS, hospitals, aggregators) and by named source
    
    - APS often leads to independent-living entrants who are then moved to ALF
        
    - Evaluate enrollment and retention by channel to guide marketing spend and outreach routing
        

### Metrics & Build Considerations

- Build participant-level features and then aggregate (center, market, tenure bands: 30/60/120 days)
    
- Prefer simple correlations initially (small N); multivariate/ML later if signal warrants
    
- Add feature ideas:
    
    - Counts by touchpoint type per month: center days, PCP visits, specialist visits, phone encounters
        
    - Appointment “reach & frequency” metrics and reschedule chains (schedules per appointment)
        
    - Transportation KPI bundle: distance, ride time bands, cancellations (by driver: patient/center), early/late pickups
        
    - Care team discipline/provider engagement flags; effective-dated assignments
        
    - Home care hours bands; presence/type of caregiver; POA flag; living situation effective-dated
        

### Next Steps

- Stand up the disenrollment dashboard (core KPIs, time series, controllable vs non-controllable, drill-to-names with CRM links)
    
- Implement required CRM fields for key gaps (caregiver co-residency, prior home care hours, referral channel details)
    
- Run participant-level correlations on prioritized features; create a simple risk index and center-level chase lists
    
- Validate signals with clinicians/operations; iterate feature set; tie impacts to center P&L
    
- Explore targeted pilots
    
    - Transportation interventions (routing, distance thresholds)
        
    - Food quality/choice expansion
        
    - Early home care hours for high-need new enrollees
        
    - Education to prevent inadvertent hospice disenrollments (esp. CA)
        

---

Chat with meeting transcript: [https://notes.granola.ai/d/c235de66-cb42-4e24-a294-ed6adedf9146](https://notes.granola.ai/d/c235de66-cb42-4e24-a294-ed6adedf9146)