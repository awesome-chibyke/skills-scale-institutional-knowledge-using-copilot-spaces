# OctoAcme Personas

This document defines typical roles and responsibilities used in OctoAcme project docs and exercises.

---

## Developers

### Role Summary
Developers design, build, test, and deliver software components. They collaborate with product and project leads to implement features that meet acceptance criteria and quality standards.

### Responsibilities
- Implement features and fixes to meet acceptance criteria
- Write and maintain tests and documentation
- Participate in design and code reviews
- Assist in estimating and planning work
- Help identify technical risks and propose mitigations

### Goals
- Deliver reliable, maintainable code
- Reduce cycle time from idea to production
- Maintain high test coverage and observability

### Typical Communication
- Daily standups and sprint planning
- PR descriptions and code review comments
- Technical design docs when needed

---

## Product Managers

### Role Summary
Product Managers define what should be built to deliver customer and business value. They own the product vision, prioritize the backlog, and measure outcomes.

### Responsibilities
- Define problem statements and success metrics
- Prioritize the roadmap and backlog
- Collaborate with stakeholders and engineering on trade-offs
- Validate solutions through user research and metrics

### Goals
- Maximize customer value and impact
- Make clear, data-driven prioritization decisions
- Ensure product-market fit and usability

### Typical Communication
- Weekly alignment with PM and engineering leads
- Roadmap updates and stakeholder briefings
- Acceptance criteria and feature specs

---

## Project Managers

### Role Summary
Project Managers coordinate delivery activities, manage schedules, risks, and communications. They enable the team to deliver on commitments efficiently.

### Responsibilities
- Create and maintain project plans and timelines
- Manage risks, dependencies, and resource constraints
- Facilitate meetings (kickoff, planning, retrospectives)
- Ensure consistent project documentation and status reporting
- Coordinate cross-team and stakeholder communication

### Goals
- Deliver projects on time and within scope
- Minimize unplanned work and escalations
- Maintain transparency and alignment across stakeholders

### Typical Communication
- Weekly status updates and stakeholder reports
- Risk registers and decision logs
- Coordination via project boards and meeting facilitation

---

---

## Product Owner

### Role Summary
Product Owners define the product vision and prioritize deliverables to maximize value for customers and the business. They bridge stakeholder needs and development teams.

### Responsibilities
- Define and communicate product vision and goals
- Prioritize backlog items and features based on business value
- Ensure deliverables meet customer needs and acceptance criteria
- Make trade-off decisions on scope and timelines
- Interface with stakeholders to gather requirements and feedback

### Goals
- Deliver maximum value to customers
- Ensure product-market fit and alignment with business objectives
- Maintain clear, prioritized backlog

### Typical Communication
- Weekly prioritization sessions with PM and Scrum Master
- Backlog refinement meetings with development team
- Regular stakeholder updates on roadmap and priorities

### Interactions with Other Roles
- **With PM:** Collaborates on timelines, resources, and delivery milestones; PM tracks execution while Product Owner sets priorities
- **With Scrum Master:** Aligns on sprint planning and team capacity; Scrum Master facilitates while Product Owner decides what to build
- **With Engineering Lead:** Discusses technical feasibility and trade-offs; Engineering Lead advises on implementation complexity
- **With QA Lead:** Reviews acceptance criteria and ensures testability; QA Lead validates that deliverables meet standards

### RACI Examples
| Activity | Product Owner | PM | QA Lead | Engineering Lead |
|----------|--------------|----|---------|--------------------|
| Backlog prioritization | **A/R** | C | C | C |
| Release planning | **A** | **R** | C | C |
| Acceptance criteria definition | **A/R** | C | C | C |
| Feature sign-off | **A** | I | **R** | C |

---

## Project Sponsor

### Role Summary
Project Sponsors provide strategic direction, secure resources, and champion the project within the organization. They ensure alignment with company objectives and act as escalation points for major issues.

### Responsibilities
- Champion the project and secure necessary resources
- Provide strategic direction and ensure organizational alignment
- Review progress and remove roadblocks at executive level
- Act as final escalation point for major risks and decisions
- Empower PM and Product Owner to drive outcomes

### Goals
- Ensure project success aligns with organizational strategy
- Remove executive-level obstacles
- Maintain stakeholder confidence and support

### Typical Communication
- Monthly or milestone-based progress reviews
- Executive briefings and business case updates
- Escalation handling for critical issues

### Interactions with Other Roles
- **With PM:** Receives regular status updates; PM escalates critical risks and requests resource decisions
- **With Product Owner:** Provides strategic guidance on priorities; Product Owner aligns roadmap with business objectives
- **With Change Manager:** Reviews change impact assessments for organizational alignment
- **With Communication Coordinator:** Approves key stakeholder messages and organizational announcements

### RACI Examples
| Activity | Project Sponsor | PM | Product Owner | Change Manager |
|----------|----------------|----|--------------|--------------------|
| Project charter approval | **A** | **R** | C | I |
| Resource allocation | **A** | **R** | C | I |
| Major risk escalation | **A** | I | I | C |
| Go/no-go decision | **A** | **R** | C | C |

---

## Change Manager

### Role Summary
Change Managers facilitate and track changes, communicate impacts, and ensure smooth adoption of new processes, features, and systems across the organization.

### Responsibilities
- Develop and execute change management plans
- Track and communicate change impacts to affected teams
- Coordinate feedback and adoption metrics
- Facilitate training and documentation for new features
- Partner with PM to adapt plans based on change readiness

### Goals
- Maximize adoption and minimize disruption
- Ensure stakeholders are prepared for changes
- Maintain clear change documentation and communication

### Typical Communication
- Change impact assessments and adoption plans
- Training materials and user guides
- Regular updates to stakeholders on adoption progress

### Interactions with Other Roles
- **With PM:** Coordinates timing of changes with delivery schedule; PM provides change details, Change Manager plans adoption
- **With Communication Coordinator:** Collaborates on messaging and stakeholder updates; Communication Coordinator distributes Change Manager's content
- **With Product Owner:** Aligns changes with business priorities; Product Owner ensures changes deliver value
- **With QA Lead:** Coordinates user acceptance testing; QA Lead validates changes meet quality standards

### RACI Examples
| Activity | Change Manager | PM | Communication Coordinator | Product Owner |
|----------|----------------|----|--------------------------|------------------|
| Change impact assessment | **A/R** | C | I | C |
| Adoption plan creation | **A/R** | C | C | C |
| User training | **A/R** | I | **R** | I |
| Change communication | **A** | C | **R** | I |

---

## QA Lead

### Role Summary
QA Leads oversee testing strategy, ensure deliverable quality, and coordinate validation activities. They work closely with development and product teams to maintain quality standards.

### Responsibilities
- Develop quality standards and comprehensive test plans
- Lead testing team and coordinate test execution
- Verify all deliverables meet acceptance criteria
- Coordinate release quality sign-off with PM and Engineering Lead
- Identify quality risks and recommend mitigations

### Goals
- Ensure all releases meet quality standards
- Minimize production defects and customer-impacting issues
- Maintain efficient, automated testing processes

### Typical Communication
- Test status reports and quality metrics
- Bug triage and severity assessment
- QA sign-off documentation for releases

### Interactions with Other Roles
- **With PM:** Reports on testing progress and quality risks; PM coordinates QA resources and schedules
- **With Engineering Lead:** Collaborates on test strategy and automation; Engineering Lead ensures testability of code
- **With Product Owner:** Validates acceptance criteria and feature completeness; Product Owner provides context for testing priorities
- **With Developers:** Reviews test coverage and coordinates bug fixes; Developers write unit tests, QA Lead validates integration

### RACI Examples
| Activity | QA Lead | PM | Engineering Lead | Product Owner |
|----------|---------|----|--------------------|------------------|
| Test plan creation | **A/R** | C | C | C |
| Acceptance criteria verification | **A/R** | I | C | **R** |
| Release sign-off | **A** | **R** | C | I |
| Bug prioritization | **R** | **A** | C | C |

---

## Communication Coordinator

### Role Summary
Communication Coordinators manage project updates, stakeholder messaging, and ensure transparent, timely communication across all project participants.

### Responsibilities
- Develop and execute communication plans
- Manage stakeholder updates and project announcements
- Maintain clear escalation paths and contact lists
- Ensure consistent messaging across channels
- Coordinate with PM on status reporting

### Goals
- Maintain transparency and stakeholder alignment
- Ensure timely, accurate information flow
- Minimize communication gaps and confusion

### Typical Communication
- Weekly stakeholder updates and newsletters
- Release announcements and change notifications
- Escalation communications and incident updates

### Interactions with Other Roles
- **With PM:** Receives status updates and key messages; PM provides content, Communication Coordinator distributes and manages stakeholder engagement
- **With Product Owner:** Coordinates product announcements and roadmap communications; Product Owner approves messaging
- **With Change Manager:** Amplifies change management communications; Change Manager provides content strategy
- **With Project Sponsor:** Distributes executive updates after approval; Project Sponsor reviews high-level communications

### RACI Examples
| Activity | Communication Coordinator | PM | Product Owner | Project Sponsor |
|----------|--------------------------|----|--------------|--------------------|
| Stakeholder communication plan | **A/R** | C | C | C |
| Weekly status distribution | **A/R** | **R** | C | I |
| Release announcements | **A/R** | C | **R** | I |
| Escalation communication | **R** | **A** | I | C |

---

## How these personas are used in the exercise
- Use these persona definitions to frame scenarios and sample interactions in the Skills Exercise.
- Each persona can be used as a persona prompt for Copilot Spaces to shape role-specific guidance.

