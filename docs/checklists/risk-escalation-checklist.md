# OctoAcme — Risk Escalation Checklist

## Purpose
This checklist defines when and how to escalate project risks, who owns escalation at each level, and the communication paths to ensure timely resolution of issues that could impact project success.

---

## Risk Severity Classification

### Critical (P0)
- **Impact:** Project cannot proceed; delivery at risk; customer-impacting production issue
- **Examples:** Major blocker with no workaround, security breach, data loss, complete service outage
- **Response Time:** Immediate (within 1 hour)
- **Escalation Level:** Level 3 (Sponsor-level)

### High (P1)
- **Impact:** Significant delay to milestone or release; major feature broken; degraded service for customers
- **Examples:** Key dependency blocked, critical resource unavailable, major technical debt blocking progress
- **Response Time:** Same business day (within 4 hours)
- **Escalation Level:** Level 2 (Product Lead)

### Medium (P2)
- **Impact:** Minor delays possible; workaround available; impacts single feature or team
- **Examples:** Minor technical blockers, resource constraints, dependency delays with alternatives
- **Response Time:** Within 2 business days
- **Escalation Level:** Level 1 (Team/PM)

### Low (P3)
- **Impact:** Minimal impact; future concern; easily mitigated
- **Examples:** Process improvements, minor technical debt, documentation gaps
- **Response Time:** Within 1 week
- **Escalation Level:** Team-level tracking (no escalation needed)

---

## Escalation Levels & Owners

### Level 1: Team-Level Triage
**When to use:**
- Risk severity is P2 or P3
- Team can resolve within sprint/iteration
- No cross-team dependencies involved

**Owners:**
- **Primary:** Scrum Master / Team Lead
- **Support:** Developers, QA Lead (as applicable)

**Actions:**
- Discuss in daily standup or dedicated risk triage
- Assign owner and timeline for resolution
- Update risk register with mitigation plan
- Monitor progress and escalate if unresolved within agreed timeline

**Communication:**
- Document in risk register
- Update project board with blocker tag
- Notify PM if resolution will take >3 days

---

### Level 2: PM & Product Lead Escalation
**When to use:**
- Risk severity is P1
- Team-level efforts have not resolved issue within agreed timeline
- Cross-team dependencies or resource constraints involved
- Requires product prioritization decisions or roadmap changes

**Owners:**
- **Primary:** Project Manager
- **Support:** Product Owner, Engineering Lead, dependent team leads

**Actions:**
1. PM documents risk details and attempted resolutions
2. PM schedules urgent sync with Product Lead and affected stakeholders
3. Product Lead evaluates options (re-prioritize, add resources, adjust scope, defer features)
4. Decision documented in decision log with rationale
5. PM communicates resolution plan to team and stakeholders
6. PM monitors execution and escalates to Level 3 if needed

**Communication:**
- Email or Slack to Product Lead with risk summary and urgency
- Follow-up meeting within 4 hours for P1 risks
- Status update to team and stakeholders after decision
- Risk register updated with resolution plan and owner

**Example Communication Template:**
```
Subject: [P1 ESCALATION] Risk requiring Product Lead decision

Risk ID: RISK-123
Severity: P1 (High)
Summary: [Brief description]
Impact: [What is blocked or at risk]
Attempts to Resolve: [What the team has tried]
Options: [Possible solutions]
Decision Needed By: [Date/time]
```

---

### Level 3: Sponsor-Level Escalation
**When to use:**
- Risk severity is P0
- Level 2 escalation has not resolved issue
- Requires executive decision, budget approval, or organizational change
- Business-impacting or customer-facing critical issue

**Owners:**
- **Primary:** Project Sponsor
- **Support:** PM, Product Owner, Product Lead, executive stakeholders

**Actions:**
1. PM prepares executive summary with business impact analysis
2. PM and Product Lead brief Project Sponsor immediately
3. Sponsor convenes decision-making session with necessary executives
4. Sponsor makes final decision or provides necessary authority/resources
5. Sponsor communicates decision and accountability
6. PM implements resolution plan with Sponsor oversight
7. PM provides daily updates to Sponsor until resolved

**Communication:**
- Immediate phone call or meeting (within 1 hour for P0)
- Written executive summary sent within 2 hours
- Daily status updates until resolved
- Post-resolution report and lessons learned

**Example Escalation Summary:**
```
EXECUTIVE ESCALATION - P0 RISK

Project: [Project Name]
Risk ID: RISK-456
Date: [Date/Time]

SITUATION:
[What has happened]

IMPACT:
- Business impact: [Revenue, customers, compliance]
- Timeline impact: [Delay estimates]
- Scope impact: [What is at risk]

ACTIONS TAKEN:
[What has been attempted at Level 1 and 2]

DECISION REQUIRED:
[What needs Sponsor decision/action]

PROPOSED OPTIONS:
1. [Option A with pros/cons]
2. [Option B with pros/cons]

RECOMMENDATION:
[PM and Product Lead recommendation]

REQUESTED DECISION BY: [Date/Time]
```

---

## Risk Escalation Process Flow

```
Step 1: Identify Risk
    ↓
Step 2: Classify Severity (P0-P3)
    ↓
Step 3: Determine Escalation Level
    ↓
Step 4: Notify Owner & Stakeholders
    ↓
Step 5: Document in Risk Register
    ↓
Step 6: Owner Takes Action
    ↓
Step 7: Monitor Progress
    ↓
Step 8: Escalate if Unresolved or Worsens
    ↓
Step 9: Close & Retrospect
```

---

## When to Escalate

### Timing Triggers
- **P0:** Escalate immediately to Level 3
- **P1:** Escalate to Level 2 within 4 hours if team cannot resolve
- **P2:** Escalate to Level 2 after 2 days if unresolved
- **P3:** Escalate to Level 2 after 1 week if unresolved or trends indicate worsening

### Condition Triggers (regardless of initial severity)
- Risk severity increases (e.g., P2 becomes P1)
- Multiple related risks emerge indicating systemic issue
- Stakeholder confidence eroding
- Team morale significantly impacted
- Customer escalation received
- Contractual obligations at risk

---

## Communication Paths

### Internal Team
- **Channel:** Daily standup, Slack #project-team channel, project board comments
- **Frequency:** Daily for active risks
- **Format:** Brief status updates

### PM to Product Lead
- **Channel:** Direct message, email, scheduled syncs
- **Frequency:** As needed for P1/P2, weekly review for P3
- **Format:** Risk ID, severity, status, action needed

### PM to Stakeholders
- **Channel:** Weekly status report, email updates for urgent items
- **Frequency:** Weekly (routine), as needed (urgent)
- **Format:** Summarized risk register with status and mitigation plans

### PM to Sponsor
- **Channel:** Email, phone, executive briefing meetings
- **Frequency:** Monthly (routine), immediate (P0), as needed (P1)
- **Format:** Executive summary with business impact

---

## Risk Register Template

All risks should be documented in the project risk register with the following information:

| Field | Description | Example |
|-------|-------------|---------|
| Risk ID | Unique identifier | RISK-123 |
| Date Identified | When risk was discovered | 2025-11-13 |
| Severity | P0-P3 classification | P1 (High) |
| Description | Clear summary of risk | External API dependency not meeting SLA |
| Impact | What will be affected | Release delayed by 2 weeks, customer-facing feature broken |
| Probability | Likelihood of occurrence | High / Medium / Low |
| Owner | Person responsible for mitigation | Jane Doe (PM) |
| Status | Current state | Open / In Progress / Resolved / Escalated |
| Escalation Level | Current level | Level 2 (Product Lead) |
| Mitigation Plan | Actions to resolve or reduce | 1. Negotiate SLA improvement, 2. Build fallback solution |
| Timeline | Expected resolution date | 2025-11-20 |
| Last Updated | Most recent update | 2025-11-15 |

---

## Roles & Responsibilities for Risk Management

### Project Manager (PM)
- **Responsible for:** Maintaining risk register, coordinating escalations, monitoring resolution progress
- **Accountable for:** Ensuring risks are tracked and communicated appropriately
- **Escalates to:** Product Lead (Level 2), Project Sponsor (Level 3)

### Product Owner
- **Consulted for:** Product prioritization decisions when risks impact scope or features
- **Informed of:** All P1+ risks that may impact roadmap or customer commitments

### QA Lead
- **Responsible for:** Identifying quality-related risks during testing
- **Consulted for:** Risk assessment of defects and release readiness
- **Informs:** PM of quality risks that may delay release

### Engineering Lead
- **Responsible for:** Identifying technical risks and dependencies
- **Consulted for:** Technical mitigation strategies and feasibility assessments
- **Escalates to:** PM for resource or timeline impacts

### Scrum Master / Team Lead
- **Responsible for:** Facilitating team-level risk triage (Level 1)
- **Escalates to:** PM when team cannot resolve or risk worsens

### Change Manager
- **Consulted for:** Risks related to organizational adoption or process changes
- **Informs:** PM of change resistance or adoption risks

### Communication Coordinator
- **Responsible for:** Distributing risk communications to stakeholders per PM guidance
- **Informs:** PM of stakeholder feedback or concerns

### Project Sponsor
- **Accountable for:** Final decisions on P0 risks and resource allocation
- **Informed of:** All P0-P1 risks and resolution status

---

## Examples of Risk Escalation Scenarios

### Example 1: Technical Dependency Blocker (P1)
**Situation:** External API team is 2 weeks behind, blocking integration for upcoming release.

**Level 1 Response:**
- Team Lead discusses with developers to find workaround
- After 1 day, no viable workaround found
- Escalate to Level 2

**Level 2 Response:**
- PM schedules sync with Product Lead and external team PM
- Options evaluated: 1) Delay release, 2) Descope integration, 3) Build mock/temporary solution
- Product Lead decides to build temporary mock for release, integrate in next iteration
- PM communicates plan to team and stakeholders
- Risk resolved

### Example 2: Critical Production Bug (P0)
**Situation:** Data corruption bug discovered in production affecting customer data.

**Immediate Level 3 Escalation:**
- PM immediately notifies Project Sponsor via phone
- Engineering Lead begins emergency fix
- PM prepares executive summary with customer impact
- Sponsor authorizes overtime resources and communications to customers
- Change Manager coordinates customer notifications
- PM provides hourly updates to Sponsor until resolved
- Post-incident retrospective scheduled

### Example 3: Resource Constraint (P2)
**Situation:** Key developer unavailable due to illness during critical sprint.

**Level 1 Response:**
- Scrum Master discusses workload redistribution in standup
- Team can absorb some work but not all
- After 2 days, sprint goals still at risk
- Escalate to Level 2

**Level 2 Response:**
- PM discusses with Product Lead: options to defer lower-priority work or bring in contractor
- Product Lead approves deferring P3 features to next sprint
- PM updates sprint plan and communicates to stakeholders
- Risk resolved

---

## Retrospective & Continuous Improvement

After any Level 2 or Level 3 escalation, conduct a brief retrospective to capture lessons learned:

- **What triggered the escalation?**
- **Was escalation timely?**
- **Were communication paths effective?**
- **Could the risk have been identified earlier?**
- **What process improvements would prevent recurrence?**

Document insights and action items in the risk register and project retrospective.

---

## Related Documents
- [Project Planning](../octoacme-project-planning.md)
- [Execution & Tracking](../octoacme-execution-and-tracking.md)
- [Risks & Communication](../octoacme-risks-and-communication.md)
- [Release Checklist](./release-checklist.md)
- [Roles & Personas](../octoacme-roles-and-personas.md)
