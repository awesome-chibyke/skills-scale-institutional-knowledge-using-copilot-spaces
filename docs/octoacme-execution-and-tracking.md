# OctoAcme — Execution & Tracking

## Purpose
Guidance for managing day-to-day execution and tracking progress toward project milestones.

## Team Rhythm
- Daily standups (15 min) — focus on progress, blockers, dependencies
- Weekly delivery sync — show progress, updates, and flagged risks
- Demo/Review at the end of each sprint or milestone

## Workflows
- Use the project board (e.g., GitHub Projects) with columns: Backlog, Ready, In Progress, In Review, QA, Done
- Pull Request workflow:
  - Small PRs (<= 400 lines when possible)
  - Include issue link and acceptance criteria in PR description
  - Run automated tests and linting in CI before requesting review
  - Require at least one approval before merging (or team-defined policy)

## Quality & Testing
- Unit tests for new logic
- Integration tests where applicable
- End-to-end smoke tests for critical flows before release
- Security scanning in CI
- Manual QA for feature acceptance when needed

## Reporting & Metrics
- Track velocity and burndown
- Monitor success metrics identified in the Project One-pager
- Use dashboards for key signals (errors, latency, usage)

## Blocker Escalation
- Level 1: Team-level triage in daily standup
- Level 2: PM escalates to Product Lead and dependent teams
- Level 3: Sponsor-level escalation for business-impacting issues

## Execution Checklist
- [ ] Branching and PR conventions documented in repo
- [ ] CI configured for tests and lint
- [ ] Regular demos scheduled
- [ ] Risk register updated weekly


# OctoAcme — Roles & Personas

Purpose
This document defines additional personas and roles used in OctoAcme project management processes, their core responsibilities, and how they interact with existing roles (Project Manager, Scrum Master, Engineering Lead). Use this as a reference when assigning responsibilities, planning hand-offs, or creating RACI matrices.

Roles covered
- Product Owner
- Project Sponsor
- Change Manager
- QA Lead
- Communication Coordinator

---

## Product Owner
Purpose: Represents customer/stakeholder priorities and defines product value.

Core responsibilities
- Define vision and goals for the product or project scope.
- Prioritize backlog items and acceptance criteria.
- Clarify requirements for the delivery team.
- Accept or reject deliverables against acceptance criteria.

Interactions
- PM: Aligns priorities and timeline constraints; participates in planning.
- Scrum Master: Works with the Scrum Master to refine backlog and remove ambiguity.
- Engineering Lead: Collaborates to understand technical feasibility and trade-offs.

Quick RACI examples
- Planning: R = Product Owner, A = PM, C = Engineering Lead, I = Sponsor
- Release acceptance: R = Product Owner, A = Product Owner, C = QA Lead, I = Communication Coordinator

---

## Project Sponsor
Purpose: Ensures strategic alignment, secures resources, and removes organizational impediments.

Core responsibilities
- Champion the project at leadership level.
- Approve major scope changes and funding.
- Serve as escalation point for critical risks.

Interactions
- PM: Provides strategic direction and supports prioritization or resourcing escalations.
- Product Owner: Validates alignment of vision with organization goals.
- Engineering Lead: May be consulted for resourcing discussions.

Quick RACI examples
- Major scope change: R = PM, A = Sponsor, C = Product Owner, I = Engineering Lead
- Funding & resource allocation: R = Sponsor, A = Sponsor, C = PM, I = Stakeholders

---

## Change Manager
Purpose: Coordinate adoption of process or product changes and ensure smooth transition.

Core responsibilities
- Assess change impact and readiness.
- Coordinate communication and training for affected teams.
- Track adoption metrics and acceptance.

Interactions
- PM: Works with PM to plan timing and communication of the change.
- QA Lead: Ensures test/validation plans include change scenarios.
- Communication Coordinator: Ensures consistent messaging.

Quick RACI examples
- Change adoption rollout: R = Change Manager, A = PM, C = QA Lead, I = Sponsor

---

## QA Lead
Purpose: Own quality standards, test strategy, and acceptance verification.

Core responsibilities
- Define test plans and acceptance criteria verification approach.
- Coordinate testing activities and sign off on release readiness.
- Track quality metrics and defect trends.

Interactions
- Engineering Lead: Collaborate on test automation, environment readiness, and debugging.
- Product Owner: Confirm acceptance criteria are testable and met.
- PM: Communicate QA status and risks to PM and stakeholders.

Quick RACI examples
- Release QA sign-off: R = QA Lead, A = QA Lead, C = Engineering Lead, I = Product Owner, PM

---

## Communication Coordinator
Purpose: Manage stakeholder communications and ensure transparency.

Core responsibilities
- Prepare regular project updates and stakeholder-specific messages.
- Coordinate meeting logistics and follow-up action summaries.
- Maintain public status dashboards or mailing lists.

Interactions
- PM: Receives direction on messaging frequency and content.
- Product Owner: Ensures messaging reflects product decisions.
- Sponsor: Shares strategic status updates when requested.

Quick RACI examples
- Stakeholder update: R = Communication Coordinator, A = PM, C = Product Owner, I = Sponsor

---

## RACI Examples (short)
Activity: Sprint / Planning
- Responsible: Product Owner / PM
- Accountable: PM
- Consulted: Engineering Lead, QA Lead
- Informed: Sponsor, Communication Coordinator

Activity: Release
- Responsible: Engineering Lead / QA Lead
- Accountable: PM
- Consulted: Product Owner, Change Manager
- Informed: Sponsor, Communication Coordinator

Activity: Change adoption
- Responsible: Change Manager
- Accountable: PM
- Consulted: Product Owner, QA Lead
- Informed: Sponsor, Communication Coordinator

---

Notes and usage guidance
- Use this file as a canonical reference for role expectations.
- Copy the RACI examples into project-level plans or JIRA/Board cards.
- If additional roles are needed for a specific program, document them in the project README and reference this file.

# OctoAcme — Execution & Tracking

(Existing content kept; below are clarifications and references to checklists and QA role involvement.)

## Acceptance criteria verification & QA involvement
- Ensure every deliverable has clear acceptance criteria owned by the Product Owner.
- QA Lead must be included in sprint demos or delivery reviews for acceptance validation.
- QA verification steps must be listed on the ticket and linked to the release checklist before release.

## References to checklists
- Pre-release and release steps: docs/checklists/release-checklist.md
- Risk identification and escalation: docs/checklists/risk-escalation-checklist.md

Guidance on hand-offs
- When a feature is ready for release:
  - Engineering Lead marks the item ready for QA.
  - QA Lead performs verification and records results on the ticket.
  - PM reviews QA sign-off and triggers the release checklist.
  - Communication Coordinator prepares stakeholder notifications.

Example interaction
- Product Owner prioritizes backlog; Engineering Lead implements; QA Lead verifies acceptance criteria; PM coordinates release window; Communication Coordinator notifies stakeholders after PM approval.
