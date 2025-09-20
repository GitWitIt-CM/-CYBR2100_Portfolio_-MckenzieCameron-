# ROE Outline (Final)

## Purpose & Approvals
- **Purpose:** Assess designated systems to reduce security risk without disrupting normal service, in line with ethical and legal standards.  
- **Authorization:**  
  - Authorized by: [Approver role, e.g., Dean or CIO]  
  - Testing performed by: [Testing Team]  
  - Effective dates: [Start UTC] – [End UTC]  
  - Authorization may be paused or revoked at any time by [Approver role].  
- **Explicit Authorization Statement:**  
  “[Approver role] authorizes [Testing Team] to test the listed systems as defined in this ROE. All activity outside this scope is prohibited.”

## Scope (In-Scope / Out-of-Scope)
- **In-Scope:**  
  - Named hosts/URLs and IP ranges  
  - Synthetic/test accounts  
  - Read-only or controlled actions, including:  
    - Port scanning  
    - Authenticated web/app testing  
    - Input validation checks  
    - Password policy checks  
    - Role-based access attempts  
    - Controlled exploit use  

- **Out-of-Scope:**  
  - Social engineering unless explicitly approved  
  - Physical intrusion or after-hours entry without law enforcement coordination  
  - DoS/DDoS or service-degrading load tests during business hours  
  - Real PII exfiltration; use only test/synthetic accounts  
  - Third-party/vendor systems without written vendor consent  

## Timing & Deconfliction
- **Testing window:** [Dates/times UTC]  
- **Restrictions:** No testing during business-critical hours (e.g., 8am–6pm weekdays).  
- **Change freeze:** No system changes during testing.  
- **Helpdesk routing:** All tickets related to target systems routed to Security during testing.  
- **Traffic thresholds:** Test traffic must remain below agreed thresholds to avoid degradation.  
- **Schedule:** Documented start/end times with detailed test schedule.  

## Communications & Escalation
- **Real-Time Contacts:**  
  - Test Lead (cell)  
  - SecOps On-Call (bridge)  
  - Application/System Owner (with backup)  

- **Notification Windows:**  
  - Critical = 15 minutes  
  - High = 1 hour  
  - Medium/Low = by end of day  

- **Stop-Test Conditions:**  
  - Service impact or outage  
  - Unauthorized access to third-party or out-of-scope systems  
  - Law enforcement interaction  
  - Safety risk or any deviation from scope  

- **Escalation Authority:** Only the Approver or System Owner may authorize resumption after a stop-test.  

## Data Handling
- Collect minimum-necessary evidence only  
- Store in encrypted repository with role-limited access  
- Retain evidence for 90 days, unless extension approved  
- Document deletion after retention period  
- Redact personal identifiers; never include passwords (even hashed)  
- Hash exported evidence for chain-of-custody  

## Reporting & Handoff
- **Draft Report:** Delivered within 5 business days  
- **Final Report:** Delivered within 15 business days, including executive summary and technical details  
- **Report Includes:**  
  - Scope tested (note deviations)  
  - Attack vectors used  
  - Timeline of activity  
  - Findings with sanitized evidence  
  - Remediation plan  
- **Handoff:** Fix-plan meeting with stakeholders, followed by retest window  

---

# Consent/Authorization Snippet
“[Approver role] authorizes [Testing Team] to test the listed systems from [start date] to [end date] as defined in this ROE. Authorization may be paused or revoked at any time by [Approver role]. Testing must follow all communication, escalation, and data-handling terms.”

---

# Escalation Contacts
- **Test Lead (cell):** Immediate real-time coordination  
- **SecOps On-Call (bridge):** 24/7 technical escalation  
- **Application/System Owner (backup contact):** Business continuity and system authority  

**Notification Windows:** Critical = 15 minutes; High = 1 hour; Medium/Low = by end of day.  
**Stop-Test Triggers:** Service outage, unauthorized third-party access, law enforcement interaction, or any deviation from scope.  

---

# Evidence Links
[ROE Document (PDF)](../docs/week5-ROE_outline.pdf)
[Week 5 Reflection (PDF)](../docs/week5-reflection.pdf)


---

# Reflection
One trade-off I would look at again is how wide the in-scope testing list should be. Adding things like controlled exploit use makes the test more realistic and covers more ground, but it also raises the chance of causing problems. Keeping the scope tighter would be safer, but then you might miss important issues. Finding the right balance between safety and coverage is something I would want to revisit with the client.

---

# AI Use Note
I used ChatGPT to help understand how policies, standards, procedures, and guidelines connect to accountability, and how each one plays a role in enforcement. It also helped me clarify the purpose of key ROE clauses such as scope, stop-test authority, and data handling. 

