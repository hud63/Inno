
Thu, 16 Oct 25

### Password Reset Issue Resolution

- Fixed password reset bug that was causing blank screens when users clicked “forgot password”
    
- Issue originated from [broker.innovage.com](http://broker.innovage.com/) (without “manage” in URL) reset functionality
    
- Mark successfully tested reset password functionality using his personal account
    
    - Avoided using demo accounts to prevent “knockdown effect”
        
    - Demo accounts used by multiple people for agent training calls
        
    - Password changes would disrupt live demonstrations and confuse trainees
        
- Workaround procedures no longer required
    
- Angela walked Mark through complete testing process including email receipt and login verification
    

### New Email Communication System for License Management

- Tony/system team created automated saved lists for license tracking:
    
    - “Expired licenses”: agents with licenses expired yesterday to 60 days prior
        
    - “Going to expire”: agents with licenses expiring today through next 30 days
        
- Separate email templates created for each license status:
    
    - Expired license notification (tells agents license has expired)
        
    - Expiration warning notification (tells agents license will expire)
        
- New E&O certificate management process:
    
    - Added email template for agents with expired E&O certificates
        
    - System flags agents needing updated E&O documentation
        
    - Automated follow-up capability through saved lists
        
- Enables targeted communications replacing previous manual processes
    

### Administrative Access and Permission Updates

- Tony completed individual permission changes for Mark’s team
    
- Specific changes made:
    
    - Updated PSU access permissions
        
    - Modified broker support access levels
        
    - Mark restored to admin level with customized broker support permissions
        
- Approach: individual account modifications rather than creating new user accounts
    
- Changes implemented during daily call between Laura and Tony
    
- System now properly configured for Mark and David’s administrative needs
    

### To-Do System Training and Implementation

- Comprehensive demonstration of task management functionality:
    
    - Tasks created with action dates, assigned users, color coding options
        
    - Example: created follow-up task for agent E&O certificate verification (October 20th)
        
    - Successfully assigned test task to David to demonstrate multi-user capability
        
- Task visibility and management:
    
    - Tasks appear on home page dashboard on designated action date
        
    - Tasks disappear from main view if not completed on action date
        
    - Full task history available in dedicated “To Do” tab with calendar view
        
    - Tasks remain marked “incomplete” until manually marked “complete”
        
- Integration with agent profiles:
    
    - Tasks can be created directly from agent records
        
    - Useful for tracking follow-ups, document requests, compliance checks
        
- Limitations noted: system doesn’t provide automatic reminders like Outlook
    

### Agent Profile Management and Documentation

- Reviewed complete agent profile management workflow
    
- Status change procedures:
    
    - Demonstrated activation/deactivation process using agent with expired E&O
        
    - Emphasized importance of adding explanatory notes for all status changes
        
    - Example: agent inactivated due to expired E&O certificate (03/01/2025 expiration)
        
- Documentation and access controls:
    
    - Notes section configured as private from FMO access
        
    - Administrative comments should use notes for internal communication
        
    - Media section access restricted - consultation required before modifications
        
    - Information section accessible to FMOs and agents
        
- E&O certificate validation process:
    
    - System tracks certificate expiration dates
        
    - Multiple certificate versions can be stored (don’t delete previous versions)
        
    - Manual verification required against uploaded documents
        
    - Example case: Ron mistakenly activated agent with expired certificate
        

### Commission Structure and Payment Framework

- Two-tier commission payment system established:
    
    - FMO commission: flat $250 per sale across all states
        
    - Broker commission: state-based variable rates (different amounts per state)
        
- Payment timeline structure:
    
    - Initial payment: upon member enrollment and activation
        
    - Renewal payment: 13 months after initial enrollment effective date
        
- Year-based renewal rate calculations:
    
    - 2025 enrollments (11/01/2025) → 2026 renewal rates (12/01/2026)
        
    - 2026 enrollments (12/01/2025) → 2027 renewal rates (01/01/2027)
        
- Clawback policy framework:
    
    - No clawback if member dies (not agent’s fault)
        
    - Clawback applies if member becomes inactive within first payment period
        
    - No clawback after 3+ consecutive monthly payments collected
        
    - Specific example: member active 11/01, 12/01, 01/01 then inactive 02/01 = no clawback
        
- Commission visibility: will appear in agent profiles under “Commissions” tab once implemented
    

### Platform Testing Process and Agent Enrollment

- Complete walkthrough of agent enrollment portal functionality:
    
    - Portal access through FMO hierarchy links
        
    - Multi-step application including personal information, coverage details, banking
        
    - Required documents upload (E&O certificate, license information)
        
    - Mandatory certification quiz (100% pass required)
        
    - Knowledge test covering PACE program basics, eligibility (age 55+), service areas
        
- Backend processing workflow:
    
    - New agent applications appear in admin system as “pending” status
        
    - Manual review and activation required by administrative team
        
    - System generates automatic email notifications upon activation
        
    - Agent receives portal access credentials and welcome information
        
- Testing protocols established:
    
    - Use “test” prefix for all test accounts (agents and participants)
        
    - Test in UAT environment to avoid production data contamination
        
    - Demonstrated search functionality for newly created accounts
        

### Email Template Configuration Issues

- Multiple email template problems identified requiring immediate attention:
    
    - Member confirmation emails incorrectly configured
        
    - Templates addressed to members but containing agent-focused content
        
    - Portal links pointing to placeholder/non-functional URLs
        
    - Uncertainty about member vs agent communication protocols
        
- Specific templates requiring fixes:
    
    - “Participant application confirmation” - appears to be agent notification misconfigured as member email
        
    - “Application closed/duplicate” - similar agent notification misconfigured as member email
        
- Current state: emails not scheduled for automatic sending (manual trigger only)
    
- Laura committed to working with Miguel and Tony to resolve template configurations
    

### Commission Tracking and Statement Generation

- Commission statement design in progress for two audiences:
    
    - FMO statements showing hierarchical commission summaries
        
    - Individual broker statements showing personal earnings
        
- Transaction processing workflow:
    
    - Member approval triggers transaction creation in system
        
    - Transactions calculate appropriate commissions based on state rates and payment tier
        
    - Commission records attached to agent profiles for tracking and payment
        
- Payment verification process for customer service:
    
    - Agents can call with commission questions
        
    - Support team can verify active status, effective dates, transaction records
        
    - Limited to information visible in system - refer complex issues to Innovage
        
    - Example scenarios: “Why wasn’t I paid for Mary Sue?” - check activation date and transaction history
        

### Participant Application Management

- Member profile structure mirrors agent profiles with key differences:
    
    - Demographic information, product enrollment details, status tracking
        
    - Payment method always “list bill” for PACE participants
        
    - Transaction history showing commission calculations upon approval
        
- Status progression workflow:
    
    - Applications start in “pending” status
        
    - Upon approval, system assigns effective date and creates commission transactions
        
    - Various status codes for tracking (approved, disenrolled, etc.)
        
- Integration with agent commission tracking:
    
    - Each approved participant generates commission transaction
        
    - Transactions link to responsible agent for payment processing
        
    - Disenrollment triggers clawback calculations where applicable
        

### Open Questions and Follow-ups

- Email template fixes needed (Laura with Miguel/Tony):
    
    - Correct member vs agent email addressing
        
    - Fix portal links to functional URLs
        
    - Clarify communication protocols for member notifications
        
- Commission system finalization pending:
    
    - Final approval of commission rates and clawback rules document
        
    - Testing of disenrollment and clawback processing
        
    - Implementation of automated commission calculations
        
- Training schedule coordination:
    
    - Next session timing for participant application demonstration
        
    - Mark and David inclusion in upcoming commission setup calls
        
    - Completion of agent portal testing with participant creation
        
- System access verification:
    
    - Confirm FMO access restrictions for notes and administrative functions
        
    - Validate email template permissions and modification capabilities
        
- Bounced payment notification email template creation needed
    

---

Chat with meeting transcript: [https://notes.granola.ai/d/0d10d40f-de58-48b9-a0c4-0f44266d1103](https://notes.granola.ai/d/0d10d40f-de58-48b9-a0c4-0f44266d1103)