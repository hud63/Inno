Tue, 14 Oct 25

### Lead Processing Issues

- E123 applications not consistently flowing through as leads
    
    - Weekend gap identified: 6-8 applications submitted, only partial conversion to leads
        
    - Issue first spotted by Jeanie 2+ weeks ago, potentially up to a month ago
        
    - Current successful flow: 11 leads received since testing period, 100% success rate on received calls
        
    - Email field causing failures on E123 side despite clear specification as optional
        
        - Many seniors lack email addresses - known requirement from project inception
            
        - E123 system failing internally when no email provided
            
        - No required fields set on our API endpoint
            
- Root cause analysis shows API functioning correctly when calls reach our system
    
    - All received leads processed successfully without errors
        
    - Problem appears to be E123 not sending failed applications to our endpoint
        
    - Should generate error messages on their side if truly failing
        
- Priority #1 escalation: Cody to collaborate with Shayir on incoming leads API testing
    
    - Shayir responsible for testing coordination and providing access
        
    - Critical business impact: “creating a bit of a shit storm on the broker side”
        
    - Mark (new hire) will hear about these issues as problems roll in
        
- Newsletter field filter resolution implemented
    
    - Added “newsletter does not equal yes” filter to open leads view
        
    - Addressed duplicate filter issue Glenn created accidentally
        
    - Legacy workflow needed: if old newsletter field checked, populate new lead type field
        
    - View changes affect all users with access permissions
        

### API Integration Delays & Frustrations

- API #2 development blocked for weeks despite September 26th late-night implementation
    
    - Cody worked until 4AM initially, then 3AM and midnight across two consecutive days
        
    - Three weeks later (October 14th), still not functioning properly
        
    - Miguel/team claiming false dependency on hierarchy adjustments
        
- Access credentials never provided despite repeated requests
    
    - “Just said give me some login information. I’ll tinker with it. Never got some login information”
        
    - Cody can test basic connectivity and data flow independent of hierarchy changes
        
    - Worst case: verify data transmission and reception regardless of final structure
        
- Current hierarchy implementation already functional
    
    - FMO → Agency → Agent structure established
        
    - Campaign taxonomy system: FMO as campaign, Agent as account, Contact as agent
        
    - Encapsulates full hierarchy: “FMO dash account dash agent”
        
    - Company name, address, agent details flowing through successfully
        
- Business context: FMOs need better reporting for agency commission splits
    
    - $200 per enrollment shared between FMO and agency
        
    - E123 system only shows one layer of agent hierarchy
        
    - FMOs lack visibility into which agents roll up to specific agencies
        
    - May require E123-side improvements beyond our integration work
        

### Team Onboarding & Access Management

- Mark designated as “ultimate new hire” for comprehensive training
    
    - Complete OS track + ER track module progression
        
    - Fresh eyes approach: “pretend you’re the new sales rep”
        
    - Document gaps and missing elements during training process
        
    - Focus question: “what would I wish I had when I was hired as a newbie?”
        
    - Half the role involves improving sales team onboarding experience
        
- System access coordination across multiple platforms
    
    - ServiceNow: Critical for revenue operations ticket system and sales team support
        
    - Alan can provide: Teams, Snow, Five9, ClearView access
        
    - Invoka access: Route back to Amber for approval/setup
        
    - Signals platform: Alan unfamiliar, needs Amber coordination
        
- Meeting integration scheduled
    
    - Office hours series addition (had good engagement this week with dashboard and digital documents help)
        
    - Inside sales staff meetings participation
        
    - Glenn has scheduling conflicts but wants Mark included
        
- Revenue ops ticket system explanation
    
    - ServiceNow serves as primary channel for sales team requests
        
    - Maintains organized approach to various topics and issues
        
    - Essential for keeping connected with sales team needs and priorities
        

### Process Improvements & Documentation Standards

- Acceptance criteria documentation mandate established
    
    - “If it’s not written in the acceptance criteria, it doesn’t exist”
        
    - Glenn acknowledges being “terrible at it” along with team
        
    - Current problem: stories lack detail, conversations forgotten after time passes
        
    - Required outcome: every discussion must result in bulleted acceptance criteria list
        
    - Testing phase: clear requirements enable proper validation of completed work
        
- Supplemental contact field update issues investigation needed
    
    - Mitch identified problem during pre-departure meeting
        
    - Intermittent failures: Social Security numbers and last names not populating forms
        
    - Not consistent across all cases - requires debugging with Bowie
        
    - Impacts user experience when required information missing from forms
        
- Knowledge base article consolidation project
    
    - Current state: ~10 articles, 7 focused on different CRM instances
        
    - Examples: schedule lead, schedule intake from contact/lead, assignment processes
        
    - Articles represent current FAQ topics based on usage patterns
        
    - Master sales playbook concept: embed existing articles into comprehensive guide
        
    - URL reference system: “Page 7, URL. Page 12, URL” for easy sales team access
        
    - Mark to review existing knowledge articles as part of training process
        

### Handoff Process & Sales Strategy

- Sherry meeting scheduled regarding scripting and handoff procedures
    
    - Glenn emphasizing consistency requirements based on past “handoff bug” issues
        
    - Inside sales team maintains discovery-based approach for enrollment rep handoffs
        
    - Cannot assume brokers completed perfect information gathering
        
    - More assumptive close approach acceptable since prospects already sold
        
    - Brokers are not innovative salespeople - won’t handle complex requirements
        
- Critical tasks remain with inside sales team:
    
    - ADL assessments and documentation
        
    - Financial qualification processes
        
    - Virginia-specific requirements and compliance
        
    - Glenn firm on maintaining these responsibilities internally
        

### Next Steps & Immediate Actions

- Cody: Prioritize E123 leads API investigation and testing coordination with Shayir
    
- Glenn: Complete Orlando JV quarterly board materials delivery by Friday
    
    - Materials due Friday for October 23rd board meeting
        
    - Target completion today/tomorrow for stakeholder review and feedback
        
    - Analytics subsets and standard reporting components included
        
- Alan: Execute comprehensive access setup and training schedule for Mark
    
    - Submit ServiceNow access request with email approval process
        
    - Coordinate with Amber on Invoka access permissions
        
    - Add Mark to office hours and inside sales staff meeting series
        
- Glenn: Process outstanding dual credit requests from Strider (2 pending from last night)
    
    - Block next couple days for sales compensation work completion
        
    - Review any additional open dual credits or compensation-related items
        
- Mark: Begin new hire training module progression with fresh perspective documentation
    
- Team: Implement acceptance criteria documentation standard across all future projects
    
- Employee referral program: Cody to follow up with Bowie on portal development status
    
    - Wrapped into broader R portal project (not E123-related)
        
    - Bowie pulled into higher priority work last week, status unclear post-long weekend
        

---

Chat with meeting transcript: [https://notes.granola.ai/d/65a1e790-2382-4e9c-9d12-f272152431fb](https://notes.granola.ai/d/65a1e790-2382-4e9c-9d12-f272152431fb)