# OctoAcme Personas

This document defines typical roles and responsibilities used in OctoAcme project docs and exercises.

---

## Core Personas

### Developers

#### Role Summary
Developers design, build, test, and deliver software components. They collaborate with product and project leads to implement features that meet acceptance criteria and quality standards.

#### Responsibilities
- Implement features and fixes to meet acceptance criteria
- Write and maintain tests and documentation
- Participate in design and code reviews
- Assist in estimating and planning work
- Help identify technical risks and propose mitigations

#### Goals
- Deliver reliable, maintainable code
- Reduce cycle time from idea to production
- Maintain high test coverage and observability

#### Typical Communication
- Daily standups and sprint planning
- PR descriptions and code review comments
- Technical design docs when needed

---

### Product Managers

#### Role Summary
Product Managers define what should be built to deliver customer and business value. They own the product vision, prioritize the backlog, and measure outcomes.

#### Responsibilities
- Define problem statements and success metrics
- Prioritize the roadmap and backlog
- Collaborate with stakeholders and engineering on trade-offs
- Validate solutions through user research and metrics

#### Goals
- Maximize customer value and impact
- Make clear, data-driven prioritization decisions
- Ensure product-market fit and usability

#### Typical Communication
- Weekly alignment with PM and engineering leads
- Roadmap updates and stakeholder briefings
- Acceptance criteria and feature specs

---

### Project Managers

#### Role Summary
Project Managers coordinate delivery activities, manage schedules, risks, and communications. They enable the team to deliver on commitments efficiently.

#### Responsibilities
- Create and maintain project plans and timelines
- Manage risks, dependencies, and resource constraints
- Facilitate meetings (kickoff, planning, retrospectives)
- Ensure consistent project documentation and status reporting
- Coordinate cross-team and stakeholder communication

#### Goals
- Deliver projects on time and within scope
- Minimize unplanned work and escalations
- Maintain transparency and alignment across stakeholders

#### Typical Communication
- Weekly status updates and stakeholder reports
- Risk registers and decision logs
- Coordination via project boards and meeting facilitation

---

## Additional Personas (Operational & Governance)

### Delivery Lead

#### Role Summary
Owns end-to-end delivery for a release or initiative. Coordinates cross-functional teams, tracks milestones, and escalates risks to the Program Manager to ensure on-time, on-scope delivery.

#### Responsibilities
- Coordinate delivery across engineering, QA, and product teams
- Track milestone progress and manage dependencies
- Identify and escalate blockers and risks daily
- Ensure handoffs between phases (dev → QA → release)
- Own release readiness sign-off

#### Key Interactions
- **Receives input from:** Product Manager (scope/priorities), Engineering Ambassador (feasibility), QA Owner (acceptance readiness)
- **Hands off to:** Release Coordinator (deployment readiness)
- **Reports to:** Project Manager (status and escalations)

#### Decision Authority
- Approve scope adjustments within agreed parameters
- Escalate schedule risks and resource conflicts
- Sign off on release go/no-go decisions

#### Typical Artifacts
- Milestone status dashboards
- Dependency and blocker logs
- Release readiness checklists

---

### Engineering Ambassador

#### Role Summary
Liaises between engineering teams and program management. Clarifies technical constraints, reviews acceptance criteria for feasibility, and ensures implementation decisions align with architecture and non-functional requirements.

#### Responsibilities
- Review acceptance criteria and feature specs for technical feasibility
- Communicate technical constraints and trade-offs to product and project leads
- Validate that requirements align with system architecture
- Identify technical risks early and propose mitigations
- Ensure quality standards are defined before development begins

#### Key Interactions
- **Receives input from:** Product Manager (requirements), Developers (technical feedback)
- **Hands off to:** Delivery Lead (feasibility confirmation)
- **Partners with:** QA Owner (defining test strategy), Developers (architecture alignment)

#### Decision Authority
- Approve or flag requirement feasibility
- Recommend technical approach or alternatives
- Escalate architecture misalignment

#### Typical Artifacts
- Technical feasibility assessments
- Architecture alignment documents
- Non-functional requirements sign-off

---

### Change Owner

#### Role Summary
Owns scope and change approvals for a given initiative or release. Manages change requests, maintains the project artifact registry, and ensures all scope changes are documented and approved before implementation.

#### Responsibilities
- Evaluate change requests against approved scope
- Document rationale for approved and rejected changes
- Update project artifacts and acceptance criteria
- Communicate scope decisions to all stakeholders
- Maintain change log and audit trail

#### Key Interactions
- **Receives input from:** Project Manager (scope baseline), Stakeholders (change requests)
- **Hands off to:** Product Manager (priority impact), Delivery Lead (schedule impact)
- **Partners with:** Engineering Ambassador (feasibility assessment)

#### Decision Authority
- Approve/reject scope changes within authority limits
- Escalate high-impact changes to Project Manager and Sponsor

#### Typical Artifacts
- Change request log
- Scope baseline document
- Change impact assessment

---

### QA/Verification Owner

#### Role Summary
Responsible for test planning, acceptance validation, and sign-off criteria. Coordinates test cycles with engineering and product, and ensures quality standards are met before release.

#### Responsibilities
- Define acceptance test strategy and test plans
- Collaborate on acceptance criteria definition
- Execute functional, integration, and regression tests
- Coordinate manual and automated testing efforts
- Provide sign-off on acceptance criteria met

#### Key Interactions
- **Receives input from:** Product Manager (acceptance criteria), Developers (test readiness), Engineering Ambassador (test strategy)
- **Hands off to:** Delivery Lead (acceptance readiness), Release Coordinator (pre-release testing)

#### Decision Authority
- Approve or reject readiness to test
- Sign off on acceptance criteria met/not met
- Escalate quality blockers

#### Typical Artifacts
- Test plans and strategies
- Test case logs
- Acceptance sign-off documents
- Known issues and workarounds

---

### Stakeholder Representative

#### Role Summary
Single point of contact for a specific stakeholder group (e.g., customers, partners, support, legal). Consolidates feedback and communicates decisions back to stakeholders to maintain alignment and address concerns early.

#### Responsibilities
- Gather and consolidate stakeholder feedback
- Communicate project status and decisions to stakeholder group
- Identify and escalate stakeholder concerns and blockers
- Validate that stakeholder requirements are represented in scope
- Facilitate stakeholder sign-off on key decisions

#### Key Interactions
- **Receives input from:** Project Manager (project updates), Product Manager (requirements and priorities)
- **Hands off to:** Stakeholder group (communications and feedback)
- **Partners with:** Change Owner (scope decisions affecting stakeholders)

#### Decision Authority
- Represent stakeholder interests in scope discussions
- Escalate stakeholder-level concerns to Project Manager
- Approve stakeholder-facing communications

#### Typical Artifacts
- Stakeholder feedback logs
- Status reports and announcements
- Stakeholder sign-off documents

---

### Release Coordinator

#### Role Summary
Coordinates release tasks including deployment windows, runbooks, rollback procedures, and post-deployment verification. Liaises between Delivery Lead, engineering teams, and operations to ensure smooth, safe releases.

#### Responsibilities
- Plan deployment windows and communicate schedules
- Prepare and test rollback/mitigation procedures
- Coordinate deployment across environments (staging → production)
- Execute post-deployment verifications and smoke tests
- Manage incident response if deployment issues occur
- Prepare release announcements

#### Key Interactions
- **Receives input from:** Delivery Lead (release readiness), QA Owner (test completion), Developers (deployment artifacts)
- **Hands off to:** Operations/Support teams (production handoff)
- **Partners with:** Data Privacy Lead (compliance verification)

#### Decision Authority
- Approve or defer deployment based on readiness checks
- Execute emergency rollback if critical issues occur
- Escalate deployment blockers to Delivery Lead

#### Typical Artifacts
- Deployment checklists and runbooks
- Rollback procedures and playbooks
- Post-deployment verification reports
- Release announcement templates

---

### Data Privacy Lead

#### Role Summary
Ensures compliance with data privacy, security, and regulatory requirements. Reviews data-handling decisions, validates that privacy by design principles are followed, and provides approval for release.

#### Responsibilities
- Review data collection, storage, and processing decisions
- Validate privacy-by-design implementation
- Ensure compliance with relevant regulations (GDPR, SOC2, etc.)
- Review data retention and deletion policies
- Provide security and privacy sign-off for release

#### Key Interactions
- **Receives input from:** Product Manager (feature requirements involving data), Developers (implementation approach)
- **Hands off to:** Release Coordinator (compliance verification), Deployment teams (go/no-go decision)
- **Partners with:** Engineering Ambassador (architecture alignment)

#### Decision Authority
- Approve or escalate privacy/security concerns
- Require changes to data handling practices
- Block release if compliance gaps exist

#### Typical Artifacts
- Privacy impact assessments
- Data handling documentation
- Compliance checklists
- Security sign-off documents

---

## Persona Interaction Map

| Phase | Primary Owner | Key Collaborators | Decisions Made |
|-------|---------------|-------------------|-----------------|
| **Planning** | Product Manager | Project Manager, Engineering Ambassador, Stakeholder Reps | Scope, priorities, feasibility |
| **Design & Estimation** | Engineering Ambassador | Developers, QA Owner | Technical approach, test strategy, NFRs |
| **Execution** | Delivery Lead | Developers, QA Owner, Change Owner | Scope changes, milestone adjustments |
| **Acceptance** | QA/Verification Owner | Product Manager, Developers | Acceptance sign-off, known issues |
| **Privacy & Compliance** | Data Privacy Lead | Engineering Ambassador, Release Coordinator | Release approval from privacy/security view |
| **Release** | Release Coordinator | Delivery Lead, QA Owner, Deployment teams | Go/no-go, deployment timing, rollback |

---

## How these personas are used in the exercise
- Use these persona definitions to frame scenarios and sample interactions in the Skills Exercise.
- Each persona can be used as a persona prompt for Copilot Spaces to shape role-specific guidance.
- Reference the Interaction Map to understand dependencies and handoff points across project phases.
