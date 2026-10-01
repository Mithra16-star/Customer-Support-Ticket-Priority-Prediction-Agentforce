# Customer Support Ticket Priority Prediction & Automated Assignment System

An enterprise-grade autonomous support triage and ticket routing system built natively on Salesforce using **Agentforce** and **Autolaunched Flows (System Mode without Sharing)**.


## 📌 Project Deliverables & Demonstration

* 📄 **Complete Project Documentation (PDF):** [View Documentation Report]([(https://drive.google.com/file/d/19eCQx7pT-8fMAIgGfXWTTbf3xANtdWpO/view?usp=sharing)])
* 🎥 **Technical Video Demonstration:** [Watch Video Demonstration]([(https://drive.google.com/file/d/1CAQkMLhpNCaTFwAg9xPMBaPBPNgJ19fy/view?usp=sharing)])


## 👥 Project Team
* **Mithra** – Team Leader 
* **Lethya Sibi** 
* **Vishakha** 
* **Swetha**


## 🚀 Key Features & Architectural Enhancements
Beyond baseline triage requirements, our system implements five enterprise additions:
1. **Multidimensional Sentiment Analysis:** Dedicated decision branching evaluating customer sentiment into `Negative`, `Neutral`, and `Positive` states to immediately identify high-friction escalations.
2. **Automated SLA Breach Risk Flagging:** Active database DML updates that dynamically flag `SLA_Breach_Risk__c = True` for aged unresolved incidents.
3. **Dynamic Tiered Specialist Routing:** Automated workload balancing routing critical tickets to a `Tier 2 Technical Specialist` and standard tickets to the `General Support Queue`.
4. **System Mode Execution Security:** Configured in `System Mode without Sharing` (Flow Version 8) to ensure smooth autonomous execution without user permission roadblocks.
5. **Enterprise Multi-Agent Canvas Orchestration:** Subagent (`Support_Ticket_Priority_Analysis`) integrated into Salesforce's scalable `Agent Router` architecture.


## 🛠️ Tech Stack & Salesforce Artifacts
* **Platform:** Salesforce Developer Edition (Spring/Summer Release)
* **AI Engine:** Salesforce Agentforce (`Support Intelligence Agent`)
* **Automation:** Autolaunched Flow (`Support_Ticket_Intelligence` - Version 8)
* **Custom Object:** `Support_Ticket_Intelligence__c`
* **Execution Context:** System Mode without Sharing


## 🔄 Workflow Summary
1. User prompts Agentforce in natural language: `"Run ticket analysis for Acme Corp"`.
2. Agent Router delegates intent to the specialized subagent `Ticket Intelligence Analyzer`.
3. Subagent triggers the Autolaunched Flow action with the Account name.
4. The flow queries the latest ticket, evaluates description keywords and customer sentiment, flags SLA breach risks, sets priority to High, and assigns a Tier 2 specialist.
5. An `Urgent Ticket Handling` task is automatically inserted on the Account Activity Timeline.
6. Agentforce returns a verified **GROUNDED** conversational summary to the user.
