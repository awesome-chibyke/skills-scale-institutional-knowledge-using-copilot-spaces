# OctoAcme Project Management Docs — README

## About these docs
This README serves as the central hub for OctoAcme’s project management process documentation. It exists to help new and existing team members quickly find the processes, templates, and guidelines used to run projects at OctoAcme. These documents are the single source of truth for project artifacts, cadence, and responsibilities; please update process docs in this folder or propose changes via the process update issue template so the documentation stays current.

## Project management processes summary
OctoAcme runs projects through a clear, stage-gated lifecycle: Initiation, Planning, Execution, Release, and Retrospective/Continuous Improvement. Initiation focuses on validating the problem, defining success metrics, and producing a one‑pager to align stakeholders and decide go/no‑go. Planning converts approved initiatives into an actionable backlog and release plan: kickoff meetings, backlog prioritization with acceptance criteria, estimation, and a documented Definition of Done. Releases are treated deliberately with pre‑release checks (CI, security scans, release notes, rollback plans) and structured deployment checklists for patch, minor, and major releases.

Workflows are centered on lightweight, repeatable artifacts and the project board (Backlog → Ready → In Progress → In Review → QA → Done). Pull requests are kept small, must reference the related issue and acceptance criteria, run automated tests in CI, and require review approvals before merging. Teams use sprint/iteration planning to pull work that meets the DoD, and execution tracking relies on velocity/burndown, dashboards for key signals, and a weekly delivery sync to surface progress and flagged risks. Blockers are escalated through defined levels (team → PM → Product Lead → Sponsor) to ensure timely resolution.

Roles and responsibilities are explicit: Project Managers coordinate delivery, schedules, risks, and communication; Product Managers own outcomes, prioritize the backlog, and measure success; Developers implement and test features; QA validates acceptance and quality; stakeholders provide input and approvals. The docs recommend named PM and Product Lead for each project, with communication cadences that include daily standups, weekly PM+PdM syncs, twice‑weekly or agreed delivery standups, and monthly stakeholder updates. Communication artifacts (one‑pagers, weekly status templates, and a single source-of-truth project README) are emphasized to reduce ambiguity and centralize status.

Quality assurance is integrated into the workflow through automated and manual practices: unit and integration tests, end‑to‑end smoke tests for critical flows, CI linting and security scanning, and manual QA when needed for feature acceptance. PR conventions, test coverage expectations, and deployment smoke tests form pre‑release gates, while post‑deploy verifications and an incident playbook (including rollback procedures) protect production stability. Continuous improvement is supported by regular retrospectives that produce a small set of prioritized action items tracked back into the backlog with owners and success criteria.

## Process Docs
- docs/octoacme-project-management-overview.md
- docs/octoacme-project-initiation.md
- docs/octoacme-project-planning.md
- docs/octoacme-execution-and-tracking.md
- docs/octoacme-risks-and-communication.md
- docs/octoacme-release-and-deployment.md
- docs/octoacme-retrospective-and-continuous-improvement.md
- docs/octoacme-roles-and-personas.md

## How to contribute
To propose edits or add new process content, use the repository issue template: .github/ISSUE_TEMPLATE/add-update-content-to-process-docs.yml. Select the process document to update (or choose '<new document>' for a new file), provide a summary of the change, the rationale, and any suggested content. Prefer adding new content under docs/ (or .copilot/ if you want it to be used as context for Copilot Spaces). When in doubt, open an issue and discuss the change with the PM and PdM for the project.