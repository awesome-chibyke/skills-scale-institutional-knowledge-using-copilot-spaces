# OctoAcme Project Management Docs

## About these Docs

This directory contains OctoAcme's project management process documentation—the single source of truth for how we plan, execute, and deliver cross-functional projects. These documents serve multiple purposes:

- **Onboarding**: Help new team members quickly understand our project management approach, roles, and workflows
- **Reference**: Provide consistent guidance for PMs, Product Managers, Developers, QA, and stakeholders throughout the project lifecycle
- **Collaboration**: Enable teams to align on processes, artifacts, and communication practices
- **Continuous improvement**: Capture evolving best practices and lessons learned from retrospectives

Use these docs to guide your project work, propose updates through our issue templates, and add context files to `.copilot/` for GitHub Copilot Spaces to reference during your work.

## OctoAcme Project Management Summary

OctoAcme follows a structured yet iterative approach to project management that emphasizes customer value, clear ownership, and data-informed decisions. Projects flow through five key lifecycle stages: **Initiation**, where we validate business need and define success metrics through a lightweight Project One-pager; **Planning**, where we break work into shippable increments, estimate scope, create a prioritized backlog with acceptance criteria, and define our Definition of Done; **Execution**, where teams build, test, and iterate using daily standups, weekly syncs, and end-of-sprint demos; **Release**, where we deploy to production following pre-release gates including passing CI, security scans, smoke tests, and documented rollback plans; and **Retrospective**, where we capture learnings and convert them into actionable improvements tracked as backlog items.

Our key workflows center on the project board (using columns: Backlog, Ready, In Progress, In Review, QA, Done) and a disciplined Pull Request process. PRs should be small (≤400 lines when possible), include issue links and acceptance criteria, run automated tests and linting in CI, and require at least one approval before merging. Quality assurance is embedded throughout, with unit tests for new logic, integration tests where applicable, end-to-end smoke tests for critical flows before release, security scanning in CI, and manual QA for feature acceptance when needed.

Explicit roles and responsibilities drive accountability: **Project Managers** coordinate delivery, schedules, risks, and communications; **Product Managers** define outcomes, prioritize the backlog, and measure success metrics; **Developers** implement features, write tests, and participate in design reviews; **QA/Testing** validates quality and acceptance criteria; and **Stakeholders** provide inputs and approvals. Communication cadences include daily 15-minute standups focused on progress and blockers, weekly syncs between PM and Product Manager, twice-weekly delivery team standups, and monthly stakeholder updates. Risks are tracked in a Risk Register with impact, likelihood, owner, and mitigation plans, reviewed weekly and escalated through defined paths: team-level triage → PM → Product Lead → Sponsor.

Release and deployment follow standardized gates to reduce risk: all acceptance criteria must be met with passing CI and security scans, release notes drafted, rollback plans documented, and smoke tests prepared. Post-deployment, we run verifications and announce to stakeholders. Retrospectives occur after each sprint, release, or milestone, using a simple structure: what went well, what could be improved, action items with owners and due dates, and follow-up on previous actions. We prioritize 2–3 top action items to avoid overload, add them to the project backlog with clear owners, and review outstanding actions in weekly PM syncs—fostering a culture of continuous improvement where we measure impact, celebrate wins, and make small iterative changes.

## Process Docs

Explore the detailed process documentation for each stage of the OctoAcme project lifecycle:

- [octoacme-project-management-overview.md](octoacme-project-management-overview.md) — High-level introduction to principles, roles, artifacts, and communication cadence
- [octoacme-project-initiation.md](octoacme-project-initiation.md) — How to validate and authorize new projects with stakeholder alignment and Project One-pagers
- [octoacme-project-planning.md](octoacme-project-planning.md) — Breaking work into actionable plans, backlog creation, sprint planning, and dependency management
- [octoacme-execution-and-tracking.md](octoacme-execution-and-tracking.md) — Day-to-day execution guidance, project board workflows, PR conventions, QA practices, and blocker escalation
- [octoacme-risks-and-communication.md](octoacme-risks-and-communication.md) — Risk identification, assessment, mitigation, stakeholder communication templates, and escalation paths
- [octoacme-release-and-deployment.md](octoacme-release-and-deployment.md) — Release types, pre-release requirements, deployment checklists, rollback procedures, and release notes
- [octoacme-retrospective-and-continuous-improvement.md](octoacme-retrospective-and-continuous-improvement.md) — Running effective retrospectives, tracking action items, and fostering continuous improvement culture
- [octoacme-roles-and-personas.md](octoacme-roles-and-personas.md) — Detailed role definitions and responsibilities for Developers, Product Managers, and Project Managers

## How to Contribute

We welcome improvements to these process docs! If you have suggestions for updates, clarifications, or new content:

1. **Use the issue template**: Open a new issue using [`.github/ISSUE_TEMPLATE/add-update-content-to-process-docs.yml`](../.github/ISSUE_TEMPLATE/add-update-content-to-process-docs.yml) to propose your change. This template helps you specify which document to update, summarize the content, and explain the rationale.

2. **Add content strategically**:
   - Place new process documentation in the `docs/` folder to keep it version-controlled and discoverable
   - For context-specific guidance you want GitHub Copilot Spaces to reference, consider adding files to `.copilot/` as well

3. **Follow the process**: Once your issue is reviewed and approved, make your changes in a feature branch, open a PR with clear descriptions and links to the issue, and request reviews from relevant stakeholders.

Continuous improvement of our processes is a team effort—thank you for contributing!
