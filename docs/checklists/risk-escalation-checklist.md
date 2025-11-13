# Risk Escalation Checklist

Purpose
Defines when to escalate risks, who should be involved, and how to communicate escalations to ensure timely resolution.

When to escalate
- Risk has high probability and high impact (technical, timeline, budget).
- A blocker prevents a major milestone completion for > 24 hours.
- Unresolved dependencies with external teams or vendors.
- Security, compliance, or production incidents affecting customers.

Escalation steps
1. Document the risk: owner, description, impact, and mitigation attempts.
2. Notify the PM and Engineering Lead immediately.
3. If unresolved within agreed SLA (e.g., 24 hours for high-priority), escalate to Sponsor and Product Owner.
4. Convene an emergency triage meeting to decide mitigation vs. scope adjustment.
5. Communication Coordinator prepares stakeholder message after triage.

Owners and typical contacts
- First-line owner: Engineering Lead or feature owner (responsible to document and track).
- PM: Accountable to manage escalations and options.
- Sponsor: Decision authority on major scope or budget changes.
- Change Manager: Coordinate adoption or procedural impacts.

Communication templates (short)
- Initial alert (to PM/Engineering Lead): "Risk alert — [short title], impact: [short], immediate blocker: [yes/no], action requested: [what we need]."
- Escalation message (to Sponsor): Include risk summary, mitigation options, and recommended decision.

Example scenario
- Risk: 3rd-party API rate-limit causing failed jobs.
  - Triage: Engineering Lead attempts mitigation; PM evaluates schedule impact; Sponsor engaged if customer SLAs at risk.
  - Outcome: Temporary workaround + change request for long-term fix tracked in backlog.