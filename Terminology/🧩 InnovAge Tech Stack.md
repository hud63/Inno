### Overview

InnovAge uses a connected tech ecosystem centered around **Microsoft Dynamics 365** as the CRM and single source of truth for managing leads, marketing campaigns, and participant interactions.

### 📞 Contact & Communication Channels

- **Portal**, **E123**, **MS Forms**, **Calls**, **SMS/Text**, **Email**, **Web Qualifier Tool**  
    These are the main channels for inbound leads. Calls, texts, and emails are often unstructured communications between referral sources and outreach specialists.
    

### 🧠 Core Systems

- **Microsoft Dynamics 365** — _Customer Relationship Manager_  
    Central hub connecting campaigns, forms, marketing automation, analytics, and reputation tools.
    
- **Invoca** — _Marketing Campaigns & AQA_
    
    - Source of truth for assigning marketing campaigns to marketing-driven leads (digital and inbound calls).
        
    - Integrates call tracking, recording, and AI-based quality scoring.
        
- **Five9** — _Contact Center Manager_
    
    - Manages all inside-sales calls and SMS across the enterprise.
        
    - Natively integrated with Dynamics CRM via plug-in.
        
    - Includes Clearview dashboards and reputation-management extensions.
        
    - 1-way API for SMS.
        
- **Dynamics 365 for Marketing** — _Marketing Automation Platform (MAP)_
    
    - Automates journeys that send email and SMS based on logic triggers.
        
    - Supports welcome texts, pre-intake emails, and post-enrollment surveys.
        
- **Microsoft Co-Pilot (AI Assistant)**
    
    - Recently enabled to streamline workflows and enhance productivity.
        
    - Exploration phase for AI-driven automation opportunities.
        

### 🧾 Data & Form Management

- **Adobe Forms Manager** — Captures digital forms integrated with CRM.
    
- **Adobe Sign (eSign Solution)** — Handles email-based e-signatures.
    
    - Power Automate parses signed documents into CRM.
        
    - In-person signing and barcoded paper workflows are in development.
        

### 🌐 Data Infrastructure & Visualization

- **Matillion ETL Tool** — Extracts and loads CRM data into warehouse.
    
- **Snowflake** — _Enterprise Data Warehouse_
    
    - Stores and connects data from CRM and other systems.
        
    - Current dataset still pending validation.
        
- **Power BI** — _Data Visualization Tool_ for analytics and dashboards.
    

### 💬 Reputation & Feedback

- **BirdEye** — _Reputation Management_
    
    - Monitors online reviews and encourages positive survey feedback.
        
    - Integrates with CRM to track sentiment and outreach success.


### InnovAge Tech Stack

This section outlines the various technologies and software platforms that InnovAge uses for its operations, from marketing to data management.

**Central Hub**

- **Microsoft Dynamics 365 (Customer Relationship Manager):** This is the core platform for managing all customer and participant interactions.
    
    - **Dynamics 365 for Marketing:** An integrated marketing automation tool used to create customer journeys, send automated communications like emails and SMS, and manage various outreach campaigns.
        
    - **MS Co-Pilot (AI Assistant):** A recently implemented AI assistant designed to improve workflow efficiency.
        

**Lead and Communication Management**

- **Lead Intake Channels:** Leads are captured from a variety of sources:
    
    - Portal
        
    - E123
        
    - MS Forms
        
    - Calls
        
    - Text and Email
        
    - Web Qualifier Tool
        
- **Invoca (Marketing Campaigns & AI Quality Assurance):** This tool serves as the definitive source for tracking marketing campaign performance and uses AI to review and score call recordings for quality.
    
- **Five9 (Contact Center Manager):** Manages all inbound and outbound sales calls and SMS communications. It integrates directly into Dynamics 365, allowing staff to use the contact center from within the main CRM system.
    

**Reputation and Data Management**

- **BIRDEYE (Reputation Management):** A tool used to monitor the company's online reputation and encourage positive customer feedback and surveys.
    
- **Snowflake (Enterprise Data Warehouse):** The central repository for enterprise data. A legacy dashboard has been set up to connect data between the CRM and the warehouse, although this dataset has not yet been fully validated.
    
- **Matillion (ETL Tool):** An "Extract, Transform, Load" tool used to move and process data between different systems.
    
- **Power BI (Data Visualization Tool):** Used to create dashboards and reports to visualize data.
    

**Document and Signature Management**

- **Adobe Suite:**
    
    - **Forms Manager:** Manages the creation and deployment of digital forms.
        
    - **Adobe Sign (eSign Solution):** Powers digital forms with legally binding e-signatures. It is integrated with Power Automate to automatically process signed documents and save them to the CRM.