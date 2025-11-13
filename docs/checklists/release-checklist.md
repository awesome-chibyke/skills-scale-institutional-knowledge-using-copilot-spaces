# Release Checklist

Purpose
A reproducible checklist for pre-release, release, and immediate post-release activities to reduce risk and ensure clear communication.

Pre-release (T-3 to T-0)
- [ ] Confirm code freeze time and communicate to teams.
- [ ] Ensure all planned PRs merged and smoke tests passing on main.
- [ ] QA Lead has the final test execution report.
  - [ ] Regression tests run and pass (or known issues listed).
  - [ ] Acceptance criteria verified for release items.
- [ ] Release notes draft prepared (who, what, impact).
- [ ] Rollback plan prepared and validated (including a restore point).
- [ ] Deployment script and runbook updated and reviewed.
- [ ] Stakeholders informed by Communication Coordinator (date/time, possible impacts).

Release (day-of)
- [ ] PM or Release Lead authorizes the release window.
- [ ] Engineering Lead coordinates deployment; follow runbook step-by-step.
- [ ] QA Lead performs post-deploy smoke tests and signs off.
- [ ] Communication Coordinator notifies stakeholders of release start and expected completion.
- [ ] Monitor key telemetry and alerts during the release window.

Post-release (T+0 to T+48)
- [ ] Verify production health metrics for agreed observation window.
- [ ] Confirm feature toggles / flags state and rollback triggers.
- [ ] Publish final release notes and update relevant dashboards.
- [ ] Retrospective: collect feedback and update checklist if gaps were found.

Roles & responsibilities (short)
- PM: Accountable for scheduling and stakeholder decisions.
- Engineering Lead: Responsible for deployment execution.
- QA Lead: Responsible for verification and sign-off.
- Communication Coordinator: Responsible for stakeholder messaging.
- Product Owner: Consulted for acceptance of feature behavior.
- Change Manager: Consulted for adoption plan if this release changes processes.

Quick escalations
- If critical failure during deployment:
  - Immediate: Engineering Lead (take ownership of rollback/mitigation).
  - Notify PM and Sponsor within 30 minutes.
  - Change Manager and Communication Coordinator prepare stakeholder message.

Example runbook excerpt (short)
1. Announce start of deployment.
2. Put service in maintenance mode (if required).
3. Apply database migrations (step 1).
4. Deploy services in order: backend -> API -> frontend.
5. Run post-deploy smoke tests.
6. Confirm success and announce completion.