# 10.7 - 1573 Broker Portal

Tue, 07 Oct 25

### Project Status & Priority Setting

- E123 broker portal project with daily standup format; vendor partner running point on build with Miguel as PM
    
- Mark (new hire) shadowing Tony for onboarding; being added to relevant workstreams (e.g., enrollment sampling audit take two)
    
- MVP deployed ~1.5 weeks ago; active bug-bash/cleanup in progress
    
- Added a priority column plus a “critical path” flag to rank work by impact to first commission payout
    
- Target: have API, account funding, and core broker workflows ready by 11/1
    

### Top Priority Items (Critical Path)

- Priority 1: Hierarchy (agency/FMO) change
    
    - Call later today with Tony/Shire to decide model; decision blocks several API items and link structure
        
    - High knock-on effects: direct links, dashboard views, footer info, and association rules
        
    - Goal: define the minimum decision set now; defer noncritical rules to avoid changing links twice
        
- Priority 2: Password reset (agent portal)
    
    - Users hit a blank page on reset; back office path works
        
    - Workaround exists but is not acceptable for go-live; break-fix ticket opened/escalated (severity 3 noted on call)
        
    - Need end-to-end tracing + logging (time, browser) to speed vendor fix
        
- Priority 3: Reduce password friction
    
    - Customers dislike current password flow; desire fixed URLs without password entry for FMOs/agents where feasible
        
    - Related to: FMO welcome email and contracting landing page without requiring password
        

### API & Technical Dependencies

- "API number two" group: multiple items tied to hierarchy decision; treat as Rank 2 set after hierarchy is resolved
    
- Account funding setup must be complete ahead of 11/1; considered part of go-live essentials
    
- Data layer cleanup: remove all test records near end of project (~Priority ~20)
    
- UAT vs Prod parity
    
    - Environments must match; treat as Priority ~1.5 principle
        
    - Fix dead links in UAT and ensure label consistency (Participants vs Members)
        

### User Experience Improvements

- Direct commission link without password (Priority ~5); frequent customer ask
    
- Export to Excel on all list views
    
    - Largely implemented (marked complete/UAT passed in places); needs verification in E123
        
- Expose dashboard view (answers common BSU questions); keep high priority and validate
    
- Email notifications for status changes (product status changes, declined, disenrolled)
    
- Clear “Home” link to return agents to main dashboard; provide two links where needed
    
- Reduce double sign-in from back office; workaround in place, confirm no longer required
    
- Fix copy/typos and field labels (e.g., phone 1/phone 2 descriptions, “anything else” prompt)
    
- Make list views wider; open external links in a separate tab; minor visual polish (nice-to-haves)
    

### Data/Content Hygiene & Admin

- Remove test data before go-live; confirm footer content is controlled in back office and set per agent
    
- Back office exposure of needed data/views completed; verify in UAT
    
- Attachments: add ability to upload and auto-send email on add; confirm existing attachment work is not duplicated
    

### Next Steps & Open Items

- Decide agency/FMO hierarchy model; avoid another round of link changes if possible
    
- Confirm password reset bug path, logs, and severity; track vendor break-fix to closure
    
- Verify exports and dashboard exposure in UAT; flip to Completed once E123 confirms
    
- Resolve UAT dead links and parity gaps; keep UAT=Prod policy front and center
    
- Clean up Google Sheets: convert to true table (remove merged cells) so priority sort works; then re-sort by Priority and Critical Path
    
- Continue working prioritized list top-down; group API#2 items together after hierarchy decision
    
- Prep change communication if links must change again; aim to do it once with final model
    

---

Chat with meeting transcript: [https://notes.granola.ai/d/69ba2b8b-f6ec-45e0-bf0c-23bb12b1c8bc](https://notes.granola.ai/d/69ba2b8b-f6ec-45e0-bf0c-23bb12b1c8bc)