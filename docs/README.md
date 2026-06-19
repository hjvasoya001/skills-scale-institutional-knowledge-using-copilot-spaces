# OctoAcme Project Management — Quick Reference Guide

## Overview

OctoAcme operates a structured yet iterative project management approach designed around customer value, clear ownership, and data-informed decisions. The organization applies a five-phase lifecycle to all cross-functional projects: **Initiation**, **Planning**, **Execution**, **Release**, and **Retrospective**. Central to this model are three key roles—Project Manager (PM), Product Manager (PdM), and the delivery team (Developers and QA)—each with distinct responsibilities. The PM coordinates delivery, schedules, and communications; the PdM defines outcomes and prioritizes the backlog; and developers and QA collaborate to implement and validate work. This role clarity, combined with a commitment to psychological safety and iterative delivery, ensures that projects remain aligned with business objectives while maintaining team morale and quality.

## Workflows & Communication Cadence

Day-to-day execution is anchored in a disciplined team rhythm: **daily standups** (15 minutes) focus on progress and blockers, **weekly delivery syncs** track risk and updates, and **demos or reviews** occur at sprint or milestone endpoints. Work flows through a GitHub Projects board with standardized columns (Backlog, Ready, In Progress, In Review, QA, Done), and pull requests follow a lightweight convention (≤400 lines when possible) requiring at least one approval before merge. Risk and dependency management is continuous—captured in a Risk Register and escalated through a three-tier path: team-level triage, PM escalation to Product Lead and dependent teams, and sponsor-level escalation for business-impacting issues. Weekly syncs between PM and PdM, along with monthly stakeholder updates and ad-hoc communications, ensure transparency across all levels.

## Quality Assurance & Release Management

Quality is built into every phase through **unit tests**, **integration tests**, **end-to-end smoke tests**, and **security scanning** in CI. Before release, all acceptance criteria must be met, CI and security scans must pass, and a rollback plan must be documented. Releases are categorized by type (Patch, Minor, Major) and follow a standardized deployment checklist that includes staging verification, production deployment (ideally automated), post-deploy verification, and stakeholder announcement. Should an incident occur, the team triggers incident response, rolls back if necessary, and conducts a blameless retrospective to capture root causes and action items.

## Continuous Improvement & Documentation

Every sprint, release, or milestone concludes with a **retrospective** (45–75 minutes) where the team reviews what went well, identifies improvements, and assigns 2–3 prioritized action items with clear owners and timelines. Learnings feed back into the project backlog and are tracked in weekly PM syncs to ensure accountability. All project artifacts—Charter, Roadmap, Backlog, Risk Register, and Retrospective notes—are maintained in the project repository (under `docs/` or `.copilot/`), creating a single source of truth that supports onboarding, transparency, and institutional knowledge retention across the organization.

---

## Process Documentation — Table of Contents

### Core References

| Document | Purpose |
|----------|---------|
| [Project Management Overview](./octoacme-project-management-overview.md) | High-level principles, roles, lifecycle, and how to use these docs. Start here for new team members. |
| [Roles & Personas](./octoacme-roles-and-personas.md) | Detailed role summaries and responsibilities for Developers, Product Managers, and Project Managers. |

### Project Lifecycle

| Phase | Document | Key Activities |
|-------|----------|-----------------|
| **Initiation** | [Project Initiation Guide](./octoacme-project-initiation.md) | Validate business need, confirm stakeholders, create one-pager, decision gate. |
| **Planning** | [Project Planning](./octoacme-project-planning.md) | Break work into increments, estimate scope, identify dependencies, define Definition of Done. |
| **Execution** | [Execution & Tracking](./octoacme-execution-and-tracking.md) | Daily standups, sprint workflows, quality & testing, blocker escalation. |
| **Release** | [Release & Deployment Guide](./octoacme-release-and-deployment.md) | Release types, pre-release requirements, deployment checklist, rollback playbook. |
| **Retrospective** | [Retrospective & Continuous Improvement](./octoacme-retrospective-and-continuous-improvement.md) | Capture learnings, identify action items, track improvements. |

### Cross-Cutting Concerns

| Document | Purpose |
|----------|---------|
| [Risk Management & Communication](./octoacme-risks-and-communication.md) | Risk register, escalation paths, stakeholder communication templates, incident response. |

---

## Quick Reference Checklists

### Project Initiation
- [ ] One-pager completed and reviewed by Product Lead
- [ ] Sponsor / Stakeholder alignment confirmed
- [ ] Decision: Approve to move into planning?
- [ ] Create repo or project board skeleton
- [ ] Add initial artifacts to repo

### Planning
- [ ] Project kickoff held
- [ ] Backlog prioritized and estimated
- [ ] Release timeline and milestones agreed
- [ ] Definition of Done documented
- [ ] Initial test plan / QA approach drafted

### Execution
- [ ] Branching and PR conventions documented in repo
- [ ] CI configured for tests and lint
- [ ] Regular demos scheduled
- [ ] Risk register updated weekly

### Release
- [ ] Deployment window scheduled (if needed)
- [ ] Backup or snapshot prepared (if applicable)
- [ ] Deploy to staging and run smoke tests
- [ ] Deploy to production (automated pipeline preferred)
- [ ] Run post-deploy verifications
- [ ] Announce release to stakeholders and support

---

## Communication Cadence

- **Daily**: Team standups (15 minutes) — progress, blockers, dependencies
- **Weekly**: PM + PdM alignment sync; Delivery team sync with progress and risk updates
- **Sprint/Milestone**: Demo or review session
- **Monthly**: Stakeholder updates
- **Ad-hoc**: Escalations and incident communication

---

## Key Artifacts to Maintain

- **Project Charter / One-pager**: Problem, goal, success metrics, stakeholders, timeline
- **Roadmap & Release Plan**: High-level feature roadmap and release schedule
- **Sprint/Iteration Backlog**: Prioritized backlog with acceptance criteria
- **Risk Register**: ID, description, impact, likelihood, owner, mitigation, status
- **Retrospective Notes**: What went well, improvements, action items with owners and due dates
- **Definition of Done**: Shared understanding of when work is complete

---

## How to Use These Docs

1. **New to OctoAcme?** Start with [Project Management Overview](./octoacme-project-management-overview.md) and [Roles & Personas](./octoacme-roles-and-personas.md).
2. **Starting a new project?** Follow the [Project Initiation Guide](./octoacme-project-initiation.md) and [Project Planning](./octoacme-project-planning.md).
3. **In execution?** Reference [Execution & Tracking](./octoacme-execution-and-tracking.md) and [Risk Management & Communication](./octoacme-risks-and-communication.md).
4. **Preparing a release?** Consult [Release & Deployment Guide](./octoacme-release-and-deployment.md).
5. **Closing out a project?** Review [Retrospective & Continuous Improvement](./octoacme-retrospective-and-continuous-improvement.md).

Keep project artifacts (Charter, Backlog, Risk Register) in your project repo under `docs/` or `.copilot/` for easy Copilot Spaces integration and team access.
