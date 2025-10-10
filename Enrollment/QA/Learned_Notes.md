Here’s everything Mark Learned said in the **Ppt Onboarding Data/Indicators** meeting:

## Mark Learned’s Statements - Ppt Onboarding Data/Indicators Meeting

**On Current Dashboard Limitations:**

- No vanilla ice cream solution yet for center directors
    
- Can’t see disenrollments on a time series chart
    
- Need an always-available KPI dashboard at center and participant levels
    
- Without this core element, downstream correlation/causation work won’t stick operationally
    

**On Disenrollment Analysis:**

- Key derivatives needed on the dashboard: controllable vs non-controllable, death, hospice-related
    
- Disenrollment by living situation is a critical gap to fill
    
- Prior analysis by Nick Armstrong about 1 year ago showed step changes in disenrollment and unit economics across living situations
    
- Nursing home (SNF) residents: lose money
    
- Assisted Living (ALF): roughly break-even
    
- Independent living: profit center
    
- Center directors need to see trends over time and drill into names to resolve disputes
    
- Need links to CRM records
    

**On Living Situation Impact:**

- Strong correlation between living situation and retention/economics
    
- Independent living: primary profit source; focus on maximizing duration in this state
    
- Assisted Living: near break-even
    
- SNF: negative margin; less concern when SNF residents cancel
    
- Participants progress through acuity over time (shift from independent to ALF around months 6-7, and ALF to SNF)
    
- Six-month care plan cadence likely drives observed tenure-based transitions
    
- Priority: instrument “participant + month” to understand tenure, lifetime value, and economic pull-through by living situation
    

**On Data Infrastructure:**

- Existing Power BI environment with a hardened CRM data model (including disenrollment reasons/flavors)
    
- Owner/contact: Alan Rodriguez (RevOps analyst) for access
    
- Likely in a “Revenue Operations” workspace
    
- Many legacy dashboards exist; reuse dataset vs. rebuilding
    
- Include deep links to CRM records to eliminate name disputes
    
- Required granularity: participant + month (to handle time-varying attributes like living situation and care team)
    

**On Early Warning Indicators:**

- Focus on months 1-4/5 post-enrollment (gradual decline, then leveling)
    
- Target voluntary disenrollments in early months vs. capricious “rapid” disenrollments
    

**On Care Team Analysis:**

- Need effective-dated care team assignments in Epic
    
- Otherwise back into history via appointment/provider data
    
- Explore directional signals (sample sizes may be small)
    
- Discipline impact: PCP vs social work vs dietitian vs rehab on no-shows/disenrollment
    
- Individual provider effects (bedside manner differences) acknowledging low N and outlier risk
    
- Compare outcomes when specific disciplines are engaged (dental as a potential retention lever)
    

**On Metrics & Build Considerations:**

- Build participant-level features and then aggregate (center, market, tenure bands: 30/60/120 days)
    
- Prefer simple correlations initially (small N); multivariate/ML later if signal warrants
    

**On Next Steps:**

- Stand up the disenrollment dashboard (core KPIs, time series, controllable vs non-controllable, drill-to-names with CRM links)
    
- Implement required CRM fields for key gaps (caregiver co-residency, prior home care hours, referral channel details)
    
- Run participant-level correlations on prioritized features
    
- Create a simple risk index and center-level chase lists
    
- Validate signals with clinicians/operations
    
- Iterate feature set
    
- Tie impacts to center P&L