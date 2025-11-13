# OctoAcme — Release Checklist

## Purpose
This checklist provides a reproducible, step-by-step guide for preparing and executing software releases. Use it to ensure all quality gates, stakeholder communications, and deployment activities are completed before and during release.

---

## Pre-Release Checklist

### Code Freeze & Quality Gates
- [ ] **Code freeze announced** — Communicate freeze date to all developers (typically 3-5 days before release)
- [ ] **All planned features merged** — Verify that all feature branches for this release are merged to main/release branch
- [ ] **CI/CD pipeline passing** — Ensure all automated tests, linting, and security scans pass successfully
- [ ] **Security scanning completed** — Review and address any critical/high vulnerabilities discovered
- [ ] **Test coverage verified** — Confirm test coverage meets team standards (e.g., >80% for critical paths)
- [ ] **Performance testing completed** — Validate that performance benchmarks meet requirements (load time, throughput, etc.)

### QA Sign-Off
- [ ] **QA Lead assigned** — Confirm QA Lead ownership for this release
- [ ] **Test plan executed** — Complete all test cases in the release test plan
- [ ] **Acceptance criteria verified** — QA Lead confirms all features meet documented acceptance criteria
- [ ] **Regression testing completed** — Verify existing functionality still works as expected
- [ ] **User acceptance testing (UAT)** — If applicable, complete UAT with product owner or pilot users
- [ ] **Critical bugs resolved** — No open P0/P1 bugs remaining; P2+ bugs triaged and accepted for release or deferred
- [ ] **QA sign-off obtained** — QA Lead provides written approval to proceed with release

### Stakeholder Communication
- [ ] **Release notes drafted** — Document new features, bug fixes, breaking changes, and known issues
- [ ] **Release announcement prepared** — Communication Coordinator drafts stakeholder announcement
- [ ] **Stakeholders notified** — Send release schedule and expected impact to all stakeholders (PM, Product Owner, Project Sponsor)
- [ ] **Customer-facing communication ready** — If applicable, prepare customer release notes or upgrade guides
- [ ] **Support team briefed** — Ensure support/operations team is aware of changes and how to handle potential issues

### Deployment Preparation
- [ ] **Rollback plan documented** — Define clear steps to rollback if deployment fails (DB migrations, feature flags, previous version restore)
- [ ] **Deployment runbook reviewed** — Verify deployment steps are documented and tested
- [ ] **Environment readiness** — Confirm staging/production environments are healthy and ready (disk space, dependencies, configurations)
- [ ] **Feature flags configured** — If using feature flags, verify they are set correctly for gradual rollout
- [ ] **Database migrations tested** — If applicable, test DB migrations in staging environment identical to production
- [ ] **Monitoring and alerts configured** — Ensure monitoring dashboards and alerting rules are ready to catch issues
- [ ] **On-call engineer assigned** — Confirm engineering support during and after deployment window

### Final Approvals
- [ ] **Product Owner approval** — Product Owner reviews release scope and approves go-live
- [ ] **PM approval** — PM confirms release readiness and approves deployment schedule
- [ ] **Project Sponsor notified** — Inform sponsor of release timeline (if major release)

---

## Release Execution Checklist

### Deployment
- [ ] **Pre-deployment announcement** — Notify stakeholders that deployment is starting (expected duration and impact)
- [ ] **Backup production data** — Complete backup of production database and critical data before deployment
- [ ] **Deploy to staging** — Verify release works in staging environment before production
- [ ] **Staging smoke tests passed** — Run critical smoke tests in staging to validate deployment
- [ ] **Deploy to production** — Execute production deployment following runbook
- [ ] **Database migrations applied** — If applicable, run and verify database migrations
- [ ] **Production smoke tests passed** — Run critical end-to-end smoke tests in production
- [ ] **Verify key metrics** — Check dashboards for errors, latency, and core business metrics
- [ ] **Verify feature flags** — Confirm feature flags are enabled/disabled as intended

### Post-Deployment Validation
- [ ] **Monitor for 30-60 minutes** — Actively monitor logs, dashboards, and alerts for issues
- [ ] **Check error rates** — Verify error rates are within normal range
- [ ] **Validate critical user flows** — Manually test or verify monitoring for key user journeys
- [ ] **Confirm no rollback needed** — After monitoring period, confirm deployment is stable

### Communication
- [ ] **Release completion announced** — Communication Coordinator sends "release complete" message to stakeholders
- [ ] **Release notes published** — Publish release notes to documentation site or internal wiki
- [ ] **Customer announcement sent** — If applicable, notify customers of new release
- [ ] **Post-release retrospective scheduled** — PM schedules release retrospective within 1-2 days

---

## Post-Release Checklist

### Monitoring & Support
- [ ] **Continue monitoring for 24-48 hours** — Watch for delayed issues or edge cases
- [ ] **Triage any new issues** — Prioritize and assign any bugs discovered post-release
- [ ] **Update known issues list** — Document any known issues or workarounds

### Documentation & Retrospective
- [ ] **Update release log** — Document release date, version, and any issues encountered
- [ ] **Conduct release retrospective** — Review what went well and what could be improved
- [ ] **Action items captured** — Document and track action items from retrospective

---

## Rollback Procedures

### When to Rollback
Consider rollback if:
- Critical functionality is broken (P0 severity)
- Data integrity issues detected
- Error rates exceed 5x normal baseline
- Performance degradation impacts >50% of users
- Security vulnerability introduced

### Rollback Steps
1. **Announce rollback decision** — PM or on-call lead notifies team and stakeholders
2. **Stop current deployment** — If deployment in progress, halt immediately
3. **Revert code deployment** — Deploy previous stable version
4. **Rollback database migrations** — Execute rollback scripts if DB changes were made
5. **Verify rollback success** — Run smoke tests to confirm previous version restored
6. **Monitor for stability** — Watch metrics to ensure system returns to normal
7. **Post-mortem scheduled** — Schedule incident review to understand root cause and prevent recurrence

---

## Release Type Guidelines

### Patch Release (x.x.X)
- **Focus:** Bug fixes and minor improvements, no new features
- **Timeline:** 1-2 days notice, shorter testing cycle
- **QA:** Focused regression testing on affected areas

### Minor Release (x.X.0)
- **Focus:** New features, enhancements, non-breaking changes
- **Timeline:** 1-2 weeks notice, full QA cycle
- **QA:** Full regression testing plus new feature validation

### Major Release (X.0.0)
- **Focus:** Breaking changes, major features, architectural changes
- **Timeline:** 1-4 weeks notice, extensive testing and stakeholder alignment
- **QA:** Comprehensive testing, UAT, beta testing if applicable

---

## Owner & Contact Information
- **Primary Owner:** Project Manager
- **QA Sign-off:** QA Lead
- **Deployment Execution:** Engineering Lead / DevOps
- **Stakeholder Communication:** Communication Coordinator
- **Approval Authority:** Product Owner & PM

---

## Related Documents
- [Project Planning](../octoacme-project-planning.md)
- [Execution & Tracking](../octoacme-execution-and-tracking.md)
- [Release & Deployment](../octoacme-release-and-deployment.md)
- [Risk Escalation Checklist](./risk-escalation-checklist.md)
