

Tue, 28 Oct 25

### System Settings Overview

- Backend configuration affects entire company - requires team consultation before changes
    
- TPA restrictions prevent certain modifications due to money transfer implications
    
- Basic company contacts: Tony as primary, broker support email available
    
- Password settings, inactive user controls, commission/vendor payable configurations available
    
- Test agent IDs excluded from report data automatically
    

### Text Messaging Setup Discussion

- Currently no SMS capability - would require separate Twilio account setup
    
- Mark interested in basic notification texts (training reminders, website links)
    
- Email templates handle SMS content in bottom section alongside HTML/text versions
    
- Process: Get Twilio account → team configures → use existing email template system for SMS
    

### Custom Fields and Questions

- Standard questions: Add tracking fields to participant/agent profiles for reports and flags
    
    - Available attributes include driver’s license, bank accounts, training dates
        
    - Can rename fields (e.g., “NPN” to “National Producer Number”)
        
    - Validation and help text options available
        
- Custom questions: Application-side questions for participants
    
    - Insurance coverage type, duration, Medicaid status already configured
        
    - Can filter by state, downline, or specific requirements
        
    - New custom questions require dev team to add to saved lists/reports
        

### Bulk Updates and Flag Management

- Drop-down options control available flags and status labels
    
- Bulk agent updates possible through selection + update button
    
- Use case: Adding notes to specific downlines (“call this person”)
    
- Agent types (recontracted FMO, LOA, agent) customizable
    
- Caution: Deleting flags removes historical data - migrate users to new flags first
    

### Email Template Configuration

- Text vs HTML versions are separate - HTML version sends by default
    
- Tracking requires “track if opened” set to “yes” in template settings
    
- Mark’s bulk email didn’t track because tracking was disabled
    
- Agent signup links best sent by FMOs directly to maintain proper attribution and avoid conflicts
    

### Automation Capabilities

- Workflows trigger on positive actions (member activated, email opened)
    
- Cannot trigger on negative actions (email not opened)
    
- Potential use cases:
    
    - Top performer recognition based on application count
        
    - Status update notifications when member moves through approval process
        
- 60-day PACE approval process - automated status emails could reduce agent anxiety
    
- Member-focused automations only (not agent actions)
    

### Next Steps

- Mark to enable email tracking on existing templates
    
- Explore Twilio account setup for SMS notifications
    
- Plan automated email workflow once member status integration is complete (Cody/Shadi coordination)
    
- Consider multi-step approval notifications to keep agents informed during 60-day process
    

---

Chat with meeting transcript: [https://notes.granola.ai/d/8e9152ba-e537-4184-83ca-322de5c0097812](https://notes.granola.ai/d/8e9152ba-e537-4184-83ca-322de5c00978)