# OctoAcme Project Management Docs

This README provides an index and brief summary of the OctoAcme project management processes and links to all documents in the docs/ folder.

## OctoAcme Project Management Overview

OctoAcme follows a lightweight, iterative project management approach designed to deliver customer value efficiently while maintaining clear ownership, transparency, and continuous improvement.

### Core Workflow and Lifecycle

OctoAcme employs a structured yet iterative project lifecycle spanning five key phases: **Initiation, Planning, Execution, Release, and Retrospective**. During initiation, teams validate business needs and establish success metrics through a lightweight One-pager, gaining stakeholder alignment before proceeding to planning. The planning phase breaks work into shippable increments with clear acceptance criteria, dependency mapping, and a prioritized backlog using T-shirt sizing or story points. Execution then follows an agile cadence with daily standups and twice-weekly delivery syncs, leveraging GitHub Projects for task management through columns (Backlog, Ready, In Progress, In Review, QA, Done). Pull requests are kept small (≤400 lines), require CI checks and at least one approval, and maintain traceability to issues. Finally, releases follow a structured deployment checklist with smoke tests, rollback plans, and incident playbooks, followed by retrospectives that capture learnings and drive continuous improvement.

### Roles and Clear Ownership

OctoAcme operates with three primary delivery personas—**Product Managers** (who define "what" and prioritize based on customer value), **Project Managers** (who coordinate delivery, manage risks, and ensure stakeholder alignment), and **Developers** (who implement features with quality and design rigor). Each project is anchored by a named PM and Product Lead with clear, delegated responsibilities. This clarity of ownership is reinforced through structured communication: weekly syncs between PM and Product Manager, twice-weekly team standups, and monthly stakeholder updates. The organization maintains a three-level escalation path (Team → PM → Product Lead → Sponsor) for blockers and risks, enabling rapid issue resolution while preserving decision-making authority at appropriate levels.

### Communication and Risk Management

OctoAcme prioritizes transparency and psychological safety through a consistent communication rhythm and lightweight documentation practices. Teams maintain a **Risk Register** (capturing ID, Description, Impact, Likelihood, Owner, and Mitigation) that is reviewed weekly and updated throughout execution. Stakeholder communication is anchored to a single source of truth—typically the project README or release documentation—with standard weekly status templates covering progress, next steps, risks, and decisions needed. For incidents, the organization follows a blameless retrospective model with triage summaries and post-incident reviews, ensuring learning over blame.

### Quality Assurance and Continuous Improvement Culture

Quality is embedded throughout execution with unit tests for new logic, integration tests where applicable, end-to-end smoke tests for critical flows before release, and security scanning in CI. OctoAcme measures success through velocity tracking, burndown charts, and dashboards that monitor the success metrics defined in the project charter (e.g., error rates, latency, usage). After each sprint, release, or milestone, retrospectives are held (45–75 minutes) to discuss what went well, what could improve, and to identify 2–3 prioritized action items. This disciplined approach to learning—tracking and measuring the impact of improvements—creates a culture of continuous iteration aligned with OctoAcme's core principle of iterative delivery and data-informed decisions.

---

## Process Documentation Index

Below are the core OctoAcme project management process documents. Each covers a specific phase or aspect of our approach:

### Foundational Guides

- **[octoacme-project-management-overview.md](./octoacme-project-management-overview.md)** — High-level introduction to OctoAcme's project management approach, core roles, key artifacts, and communication cadence.

- **[octoacme-roles-and-personas.md](./octoacme-roles-and-personas.md)** — Detailed descriptions of core roles (Project Manager, Product Manager, Developer) with responsibilities, goals, and typical communication patterns.

### Lifecycle Phases

- **[octoacme-project-initiation.md](./octoacme-project-initiation.md)** — How to validate and authorize new work, align stakeholders, create a Project One-pager, and make the go/no-go decision to enter planning.

- **[octoacme-project-planning.md](./octoacme-project-planning.md)** — How to turn an approved initiative into an actionable plan: breaking work into increments, defining acceptance criteria, estimating scope, and creating release plans.

- **[octoacme-execution-and-tracking.md](./octoacme-execution-and-tracking.md)** — Day-to-day execution guidance: team rhythm (standups, syncs, demos), workflows (GitHub Projects and pull requests), quality practices (testing, CI, metrics), and blocker escalation.

- **[octoacme-release-and-deployment.md](./octoacme-release-and-deployment.md)** — Release types, pre-release requirements, deployment checklists, rollback playbooks, and release notes templates.

- **[octoacme-retrospective-and-continuous-improvement.md](./octoacme-retrospective-and-continuous-improvement.md)** — How to run effective retrospectives, capture action items, track improvements, and foster a continuous improvement culture.

### Cross-Cutting Concerns

- **[octoacme-risks-and-communication.md](./octoacme-risks-and-communication.md)** — Risk register management, risk lifecycle, stakeholder communication templates, escalation paths, and incident communication protocols.

---

## How to Use These Docs

- **For new projects:** Start with the [Project Management Overview](./octoacme-project-management-overview.md) and [Roles & Personas](./octoacme-roles-and-personas.md), then follow the lifecycle guides in order.
- **For phase-specific guidance:** Jump to the document that matches your current phase (Initiation, Planning, Execution, Release, or Retrospective).
- **For process improvements:** Submit a [Process Doc Update](../.github/ISSUE_TEMPLATE/add-update-content-to-process-docs.yml) issue to propose changes or additions to these docs.
- **For Copilot Spaces context:** Add links to these docs in your Copilot Space configuration for role-specific AI guidance.

---

## Contributing to These Docs

OctoAcme's project management docs are living documents. If you identify gaps, improvements, or new best practices to capture, please:

1. **Create an issue** using the [Process Doc Update](../.github/ISSUE_TEMPLATE/add-update-content-to-process-docs.yml) template.
2. **Include rationale** — explain why the update is needed and what gap it addresses.
3. **Propose content** — include draft text, checklists, or examples when possible.
4. **Request stakeholder review** — involve Product Managers, Project Managers, and team leads as needed.
5. **Merge and communicate** — once approved, merge and highlight the update in team communications.

This ensures our processes remain current, aligned, and continuously improved based on team feedback and real-world experience.
