
Fri, 17 Oct 25

### Agent Activation Issue Resolution

- David William Robbender agent remained inactive despite meeting all setup requirements
    
    - Agent submitted application October 16th at 2:15 PM Central
        
    - System performs automated activation checks twice daily: 9 AM and 2 PM Central
        
    - Missing required state field (California) prevented activation
        
    - Investigation revealed Sherry updated state from blank to California after initial submission
        
- Root cause analysis showed two system errors caught during training:
    
    - David William agent: missing state designation despite valid California license #53127
        
    - Virginia-licensed agent: incorrectly activated without required inactive date
        
- Process improvements identified:
    
    - Team reminded to complete full checklist verification
        
    - All daily activations require double-checking of license state fields and inactive dates
        
    - Angela to follow up offline with activation team on missed checklist items
        
- Agent successfully activated following state field correction
    

### Platform Training - Commission Setup and Structure

- Comprehensive walkthrough of commission configuration for Medicare Advantage products
    
    - Test commission structure established: FMO ($2.50) + Sales Agent ($6.26) = $8.76 total
        
    - Product pricing matrix requires setup before commission entry
        
    - Payment cycles configured for payment #1 only initially
        
    - System validates commission amounts against product pricing (prevented $9.76 error)
        
- Commission tree hierarchy demonstration:
    
    - Innovage (top level carrier)
        
    - Test FMO (middle tier)
        
    - Test Mark (sales agent level)
        
- ZIP code restrictions observed - limited Florida locations (Tampa 33605, Orlando area)
    
    - Products automatically created per approved ZIP code coverage areas
        
    - Explains multiple product variations in system dropdown
        
- Advanced features covered:
    
    - Renewal year commission variations possible
        
    - Different payment structures for subsequent years
        
    - Commission-based vs. percentage-based options available
        

### Transaction Processing and Payment Workflows

- End-to-end transaction creation demonstrated using test participant
    
    - Member enrollment through agent-specific website link
        
    - Real-time data capture including demographics and plan selection
        
    - Automatic commission calculation upon transaction approval
        
- Payment processing rules configuration:
    
    - “If approved, increase last payment number” - enabled
        
    - “Approved move forward next billing date” - optional setting
        
    - “If declined, put on hold” - standard practice
        
- Transaction editing capabilities shown:
    
    - Payables section displays all commission recipients and amounts
        
    - System tracks member billing vs. commission earnings separately
        
    - Edit functionality restricted to authorized administrative users
        
- Chargeback and reversal procedures:
    
    - Rapid disenrollment scenarios handled automatically
        
    - System creates negative commission entries for affected agents
        
    - Clawback amounts appear on subsequent commission statements
        
    - No manual intervention required for standard reversals
        

### Commission Statements and Agent Reporting

- Commission statement generation process demonstrated for test agent
    
    - Current PDF format undergoing redesign per stakeholder feedback (Tony, Ron, Sherry)
        
    - New format will include additional columns and enhanced detail
        
- Distribution channels for commission statements:
    
    - Agent portal: “My Documents” section with download capability
        
    - FMO back office: document section with full visibility
        
    - Automated email notifications direct agents to portal access
        
- Bulk payment processing workflow:
    
    - Summary list generation from payables data
        
    - ACH file creation for automated agent payments
        
    - Handles scale from 200 to 2,000+ agents efficiently
        
- Statement timing and frequency:
    
    - Monthly commission cycles standard
        
    - Date ranges clearly specified on statements
        
    - Historical statements maintained in document archive
        

### Email and Communication System Training

- Template-based communication system walkthrough:
    
    - Dropdown selection of pre-configured email templates
        
    - View function for content preview before sending
        
    - Print-to-PDF option for external distribution or record keeping
        
- Custom email creation capabilities:
    
    - Text version: plain format without logos or formatting
        
    - HTML version: full formatting, logos, and professional layout
        
    - Custom subject lines and sender designation
        
    - All communications automatically logged in system history
        
- Automated vs. manual communication triggers:
    
    - Agent setup emails: automated upon registration completion
        
    - License follow-up reminders: manual initiation required
        
    - Participant communications: primarily agent-driven, not system-generated
        
- Email tracking and audit trail:
    
    - All sent communications recorded with timestamps
        
    - History section maintains complete communication record
        
    - PDF downloads create permanent documentation
        

### Agent Search and Platform Navigation

- Search functionality limitations identified during training:
    
    - System caches previous search parameters (15-year legacy behavior)
        
    - Requires manual “Clear” button activation to reset filters
        
    - Affects both top-right and bottom-left clear options
        
- Impact on FMO users:
    
    - Agents don’t access this administrative view
        
    - FMO staff may experience search result confusion
        
    - Training documentation needed to prevent support tickets
        
- Navigation best practices established:
    
    - Always clear search filters between different queries
        
    - Multiple pathways available for reaching same functions (participants, agent lists)
        
    - Direct participant access preferred for efficiency
        
- License verification workflow demonstrated:
    
    - Virginia license search revealed missing inactive dates
        
    - Cross-referencing capability between states and license status
        
    - Quality control process for multi-state agent verification
        

### Data Management and Cleanup Procedures

- Proper deletion sequence critical for data integrity:
    
    - Void member payments and transactions first
        
    - Delete generated payables (Laura handled during session)
        
    - Remove participant enrollment record
        
    - Delete agent profile if temporary/test account
        
- Test data management strategy:
    
    - Maintain Mark test agent for ongoing demonstrations
        
    - Avoid password changes on shared demo accounts
        
    - Separate test environment from production training
        
- Data relationship dependencies:
    
    - Commission statements must be generated before payable deletion
        
    - Transaction history preserved even after member removal
        
    - Five-step deletion process ensures no orphaned records
        
- Best practices for ongoing operations:
    
    - Regular cleanup of test enrollments
        
    - Documented procedures for legitimate participant removals
        
    - Audit trail maintenance for compliance requirements
        

### Support and Communication Protocols

- Preferred support channels established due to high email volume:
    
    - Ticket system via [support@e123atenrollment123.com](mailto:support@e123atenrollment123.com) preferred over direct email
        
    - Jira integration available for technical issues
        
    - Daily ticket follow-up ensures response tracking
        
- Ticket submission requirements:
    
    - Subject line must include Corp ID 1573
        
    - Specify “question for Laura and Angela” in body text
        
    - Detailed description of platform usage questions
        
- Response time and escalation:
    
    - Hundreds of daily emails create potential for lost communications
        
    - Ticket system provides accountability and tracking
        
    - Implementation team (Miguel) coordinates complex technical issues
        
- Communication tool compatibility noted:
    
    - Cross-platform email functionality confirmed (Outlook, Gmail)
        
    - Historical challenges with isolated email systems resolved
        
    - Universal access ensures seamless collaboration
        

### Action Items and Next Steps

#### Immediate Actions (This Week)

- **Angela**: Provide updated commission statement samples once redesign completed
    
- **Laura**: Follow up with activation team on Virginia agent correction and checklist compliance
    
- **Mark**: Confirm participation in weekly Tony meetings via Miguel coordination
    

#### Setup and Configuration (Next 2 Weeks)

- **Platform Team**: Schedule additional commission setup training after proper system configuration
    
- **Miguel**: Coordinate Mark’s integration into weekly operational meetings
    
- **Training Team**: Create FMO documentation for search functionality limitations
    

#### Ongoing Process Improvements

- **Activation Team**: Implement double-check procedures for daily activation runs (9 AM/2 PM Central)
    
- **Mark**: Utilize ticket system for all platform questions using Corp ID 1573
    
- **All**: Maintain test agent accounts for demonstration purposes without production impact
    

#### Quality Assurance Measures

- **Daily**: Verify license state fields and inactive dates during activation checks
    
- **Weekly**: Review activated agents for compliance with state licensing requirements
    
- **Monthly**: Audit test data cleanup and commission statement accuracy
    

---

Chat with meeting transcript: [https://notes.granola.ai/d/86d37f6a-357c-4af7-80f8-af7093bd591a](https://notes.granola.ai/d/86d37f6a-357c-4af7-80f8-af7093bd591a)