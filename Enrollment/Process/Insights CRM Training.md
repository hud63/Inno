
Thu, 16 Oct 25

### CRM Overview & Record Types

- Three main record types in the CRM system with distinct purposes:
    
    - Account records: Businesses/organizations that refer potential participants to the program
        
        - Examples: Churches, independent living facilities, government agencies, adult protection services
            
        - Community-based organizations: food banks, veteran support organizations, assisted living facilities
            
        - Key fields tracked: Name, phone number, account type (various channels), call routing priority
            
        - Call routing indicates profitability level for outreach specialists and field sales prioritization
            
        - Contact management: tracks known contacts (directors, social workers) within each account
            
        - Physical address information for brick-and-mortar locations stored
            
    - Lead records: Capture basic qualification information for potential participants
        
        - Demographics, address, basic insurance information, activities of daily living assessment
            
        - ADL needs: bathing, grooming, eating, toileting assistance requirements
            
        - Income verification, social security, religion, marital status details
            
        - Decision-making capacity assessment, Power of Attorney information
            
        - Financial assets evaluation, spouse demographics if applicable
            
        - More marketing/qualifying focused than enrollment-focused
            
    - Contact records: Generated after qualified leads successfully move to enrollment process
        
        - Lead records become read-only and close out as “qualified”
            
        - Same person has two record types to separate marketing/qualifying from enrollment processes
            
        - All enrollment tabs generated within contact records for sales team use
            

### Lead Generation & Qualification Process

- Two distinct pathways for generating leads with similar processes but different entry points:
    
    - Field specialists (outreach specialists) generating leads through events and direct outreach
        
        - Build direct rapport with local enrollment reps in their geographic areas
            
        - Example: Linda (outreach specialist) and Montoya (enrollment rep) both work in Thornton, have established working relationship
            
        - Skip inside sales team entirely, schedule intakes directly with enrollment reps
            
        - Local teams develop own systems for intake scheduling
            
    - Inside sales team (call center) handling inbound 1-800 number calls
        
        - Ask identical qualification questions as field specialists
            
        - Trained to find local enrollment rep and schedule quickest available appointment time
            
        - Handle leads that call in rather than attend field events
            
- Both pathways result in digital handoff from outreach specialist/inside sales to enrollment rep
    
- Lead scheduling creates intake appointment as beginning of enrollment process
    
- If participant re-engages after initial non-enrollment, use existing contact record for clean slate restart
    

### Timeline Documentation & Call Recordings

- Timeline section exists in all record types (accounts, leads, contacts) under summary tab
    
- Captures all activities performed with each record: phone calls, appointments, center tours
    
- Phone call activities show direction (outbound vs inbound), phone numbers, disposition (voicemail, completed)
    
- Call recordings accessible through two systems:
    
    - Five9 admin: More primitive interface, can download and listen to recordings
        
        - Access through user records under recordings tab
            
    - Invoka: Preferred system with advanced features
        
        - Provides agent script adherence scoring, missed elements tracking
            
        - Combines actual recordings with performance scorecards
            
        - Better user interface than Five9 system
            
- Timeline activities automatically sync to Outlook calendars when scheduled
    

### Contact Records & Enrollment Entities

- Contact records contain multiple specialized entities for comprehensive enrollment approval:
    
    - Enrollment entity: Primary finalization and reporting hub
        
        - Key fields: Anticipated signature date, intake meeting scheduling and completion
            
        - Qualification date tracking, finance finalization section completion
            
        - Heavy reporting usage, critical for enrollment metrics
            
        - Managed by enrollment representatives throughout process
            
    - Financial entity: Handled exclusively by eligibility and finance department
        
        - Medicaid application submission for financial approval
            
        - Verification of existing correct approval status
            
        - Required for program participation given Medicaid funding model
            
        - Most markets have dedicated eligibility/finance teams managing this portion
            
    - Functional entity: Clinical evaluation and agency approval process
        
        - Clinical nurse conducts comprehensive evaluation assessment
            
        - Submission to external agency for care appropriateness determination
            
        - Must meet specific health criteria: not too healthy (better with separate health plan) or too unhealthy
            
        - State deems too-healthy participants unqualified since they’re giving up existing insurance
            
        - Medicaid funding requirements drive health status parameters
            
    - HSD entity: Internal team approval with documented political challenges
        
        - Known internal politics and pushback from clinical team
            
        - Suspected understaffing issues causing excessive denials/holds
            
        - Data collected to prove problematic patterns
            
        - Cases can be escalated to regional team for local decision overrides
            
        - Improved recently but remains touchy part of process for sales team
            

### Health & Safety (HSD) Approval Process

- Comprehensive team voting system with four participating departments:
    
    - Enrollment representatives (sales team perspective)
        
    - Nurses (clinical assessment)
        
    - Doctors (medical evaluation)
        
    - Operations department (operational feasibility)
        
- Three voting options available for each department:
    
    - Approve: Case moves forward for enrollment
        
    - Hold: Additional information needed before re-discussion
        
    - Deny: Flat rejection from program participation
        
- Common denial reasons documented:
    
    - Behavioral issues and history of physical abuse
        
    - Substance abuse problems (alcoholism, drug use)
        
    - Participants deemed inappropriate for program environment
        
- Approval process based entirely on documentation review:
    
    - Primary source: Intake tab completed by enrollment rep during initial assessment
        
    - In-depth information gathered during Montoya-style enrollment rep visits
        
    - No additional physical viewing or assessment of participants during voting
        
- Individual voter tracking implemented for trend analysis:
    
    - Monitor approval/denial patterns by specific team members
        
    - Example: 80% denial rate from specific clinical staff vs higher approval rates from others
        
    - Data used to identify problematic voting behaviors and biases
        
- Final approval entity generated once all four departments vote to approve case
    

### Next Steps

- Continue comprehensive CRM training tomorrow during scheduled one-hour block
    
- Mark to explore Invoka system access for call recording review and script analysis
    
    - Tony requesting script adjustments based on call analysis
        
    - Invoka preferred over Five9 for advanced features and scoring capabilities
        
- Potential additional 30-minute follow-up session later same day if schedules permit
    
- Focus upcoming sessions on more detailed CRM functionality and advanced features
    

---

Chat with meeting transcript: [https://notes.granola.ai/d/3d84ee89-be9d-4381-93b4-47aec95efff4](https://notes.granola.ai/d/3d84ee89-be9d-4381-93b4-47aec95efff4)


# CRM Training P. 2

Fri, 17 Oct 25

### System Issues & Current Problems

- Portal experiencing major problems with broker agents
    
- Agents unable to log in, applications not processing
    
- Verification emails not being sent
    
- Developer Cody out sick today, delaying fixes
    
- Sherry mentioned campaign call routing issues
    

### CRM Training Knowledge Base Project

- Building comprehensive standard practices guide for sales users
    
- Creating ~40 different process articles with step-by-step instructions
    
- Video tutorials planned for each click-through process
    
- Targeting new hires and infrequent CRM users
    
- Early development stage, interface currently bland but will improve
    

### Lead Management Process

- Lead record creation requires:
    
    - First and last name
        
    - Contact information
        
    - ZIP code for assignment
        
- Assignment based on ZIP code catchment areas
    
    - Each outreach specialist owns specific ZIP codes
        
    - Auto-assignment can create ownership conflicts
        
    - Users trained to manually reassign leads to themselves
        

### Lead Conversion Workflow

- Discovery call qualification process
    
    - Age 55+ verification
        
    - Catchment area confirmation
        
    - Health status assessment
        
    - Housing stability check
        
- Required fields must be completed before proceeding
    
- Lead converts to contact record type after qualification
    
- Generates enrollment forms automatically (functional, financial, HSD approvals)
    

### Common Support Tickets

- Duplicate detection errors for Social Security numbers and state IDs
    
- Lead reassignment requests for ZIP code conflicts
    
- Old lead reactivation and ownership transfer
    
- Knowledge base articles being created to reduce these tickets
    

### Contact Record Structure

- Summary tab: basic info, referral source, appointments
    
- Discovery/Intake tabs: detailed qualification information
    
- Documents/Punch list: required enrollment forms
    
- Electronic forms integration with email and mobile signing
    
- Connections tab (RevOps use): shows linked forms and status
    

### Next Steps

- Monday training session scheduled (1-2 PM Pacific)
    
- Additional Five9 adapter training planned with Sherry
    
- Tony prefers keeping processes within adapter system
    
- Continue ServiceNow training sessions
    

---

Chat with meeting transcript: [https://notes.granola.ai/d/69896755-40d1-464a-a43d-c75e9c7128b9](https://notes.granola.ai/d/69896755-40d1-464a-a43d-c75e9c7128b9)