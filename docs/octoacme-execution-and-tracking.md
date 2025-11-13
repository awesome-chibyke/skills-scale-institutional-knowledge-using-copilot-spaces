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
  - **QA Lead Involvement:** QA Lead reviews PRs for testability and validates that automated tests adequately cover acceptance criteria

## Acceptance Criteria Verification

All backlog items must have clear, testable acceptance criteria before moving to "Ready" state. 

### Process
1. **During Planning:** Product Owner defines acceptance criteria with input from QA Lead on testability
2. **Before Development:** Developer reviews criteria with QA Lead to clarify test expectations
3. **During Development:** Developer implements code and unit tests that satisfy criteria
4. **Code Review:** Reviewer verifies that implementation addresses all acceptance criteria
5. **QA Phase:** QA Lead or tester validates all acceptance criteria met in test environment
6. **Definition of Done:** Item moves to "Done" only after all criteria verified and approved

### QA Lead Responsibilities in Execution
- Review backlog items for clear, testable acceptance criteria
- Coordinate with developers on test coverage expectations
- Validate that automated and manual tests adequately cover acceptance criteria
- Provide QA status updates in weekly delivery sync
- Flag quality risks early (e.g., insufficient test coverage, unclear criteria)
- Sign off on release readiness using the [Release Checklist](./checklists/release-checklist.md)

**Example Interaction:** Product Owner prioritizes backlog item for next sprint → QA Lead reviews acceptance criteria for testability → Developer implements feature with tests → QA Lead verifies acceptance criteria in QA environment → QA Lead approves item as "Done"

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

## Blocker Escalation & Risk Management
- Level 1: Team-level triage in daily standup
- Level 2: PM escalates to Product Lead and dependent teams
- Level 3: Sponsor-level escalation for business-impacting issues

For detailed escalation procedures, risk classification, communication paths, and ownership, see the [Risk Escalation Checklist](./checklists/risk-escalation-checklist.md).

**Key Escalation Principles:**
- Escalate early when risk severity is high (P0-P1)
- Document all risks in the risk register with owner and mitigation plan
- Use defined communication paths to ensure timely resolution
- Follow up escalations with retrospectives to improve risk identification

## Execution Checklist
- [ ] Branching and PR conventions documented in repo
- [ ] CI configured for tests and lint
- [ ] Regular demos scheduled
- [ ] Risk register updated weekly
- [ ] QA Lead assigned and engaged in acceptance criteria review
- [ ] [Release Checklist](./checklists/release-checklist.md) reviewed and ready for upcoming releases
- [ ] [Risk Escalation Checklist](./checklists/risk-escalation-checklist.md) communicated to team
