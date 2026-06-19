# OctoAcme — Cross-Functional Roles Interaction Guide

## Purpose
This guide clarifies how cross-functional and leadership roles interact with core delivery roles, defining decision ownership, communication patterns, and escalation paths.

## Overview
Modern project delivery requires coordination across multiple specialized roles. This guide maps interactions and dependencies to avoid bottlenecks, clarify ownership, and ensure smooth cross-team collaboration.

---

## Core Interaction Patterns

### 1. Feature Definition & Validation Loop

**Participants:** Product Managers → UX Researcher/Designer → Developers → QA

**Workflow:**
1. **Product Manager** defines problem statement and success metrics
2. **UX Researcher/Designer** validates with users and creates design specs
3. **Developers** implement with reference to acceptance criteria and design
4. **QA** validates implementation against criteria and design

**Decision Ownership:**
- What to build: **Product Manager**
- How to design it for users: **UX Researcher/Designer**
- How to build it technically: **Engineering Lead** (with input from Developers)
- Is it done correctly: **QA**

**Escalation Path:** Design conflict? → UX + PM → Delivery Lead if schedule impact

---

### 2. Technical Readiness & Risk Management

**Participants:** Engineering Lead → Developers → Security Owner → Project Manager

**Workflow:**
1. **Engineering Lead** reviews designs for technical feasibility
2. **Developers** estimate effort and identify technical risks
3. **Security Owner** conducts threat modeling and security review
4. **Project Manager** incorporates risks into project plan

**Decision Ownership:**
- Technical feasibility: **Engineering Lead**
- Implementation complexity: **Developers** (with Engineering Lead review)
- Security risk assessment: **Security Owner**
- Schedule/resource impact: **Project Manager**

**Escalation Path:** Blocker? → Engineering Lead → Delivery Lead → Project Manager → Sponsor (if high impact)

---

### 3. Release Readiness & Deployment Coordination

**Participants:** Delivery Lead → Engineering Lead → QA → Support Liaison → Security Owner

**Workflow:**
1. **Delivery Lead** creates release checklist (features, tests, docs, security approvals)
2. **Engineering Lead** confirms technical readiness and merged PRs
3. **QA** confirms smoke tests pass in staging
4. **Support Liaison** confirms runbooks and support readiness
5. **Security Owner** confirms security review completed
6. **Delivery Lead** coordinates deployment window

**Decision Ownership:**
- Release timeline: **Delivery Lead** (with PM input on priority)
- Technical readiness: **Engineering Lead**
- Quality approval: **QA**
- Support readiness: **Support Liaison**
- Security approval: **Security Owner**
- Go/No-Go decision: **Delivery Lead** (escalates to Sponsor if needed)

**Escalation Path:** Risk detected? → Delivery Lead → Project Manager → Sponsor (if schedule impact)

---

### 4. Metrics & Measurement Setup

**Participants:** Product Manager → Data Analyst/Measurement Owner → Developers → Delivery Lead

**Workflow:**
1. **Product Manager** defines success metrics for the feature
2. **Data Analyst** translates to instrumentation requirements
3. **Developers** implement tracking and telemetry
4. **Delivery Lead** ensures monitoring is live before deployment
5. **Data Analyst** validates data collection and produces dashboards

**Decision Ownership:**
- What to measure: **Product Manager**
- How to measure it: **Data Analyst/Measurement Owner**
- Implementation details: **Developers**
- Deployment readiness: **Delivery Lead**

**Escalation Path:** Data quality issues? → Data Analyst → Product Manager (may trigger post-release patches)

---

### 5. Production Incident Response

**Participants:** Support Liaison → Engineering Lead → Developers → Delivery Lead → Security Owner (if security-related)

**Workflow:**
1. **Support Liaison** detects customer-impacting issue, triages severity
2. **Support Liaison** escalates to **Engineering Lead** with context
3. **Engineering Lead** assigns root cause investigation to **Developers**
4. **Developers** propose fix (patch or rollback)
5. **QA** validates fix in staging
6. **Delivery Lead** coordinates hotfix deployment window
7. **Support Liaison** validates customer impact is resolved

**Decision Ownership:**
- Incident severity/priority: **Support Liaison** + **Engineering Lead**
- Root cause: **Developers**
- Fix or rollback decision: **Engineering Lead** + **Delivery Lead**
- Deployment timing: **Delivery Lead**
- Post-incident learning: **Project Manager** (organizes blameless retro)

**Escalation Path:** Critical incident? → Support Liaison → Delivery Lead → Project Manager → Sponsor (comms to customers/executives)

---

### 6. Project Planning & Risk Management

**Participants:** Project Manager → Product Manager → Engineering Lead → Delivery Lead → Security Owner

**Workflow:**
1. **Project Manager** kicks off planning with stakeholders
2. **Product Manager** prioritizes backlog and defines scope
3. **Engineering Lead** assesses technical complexity and dependencies
4. **Developers** estimate effort
5. **Security Owner** identifies security requirements and risk
6. **Delivery Lead** creates milestone and dependency map
7. **Project Manager** integrates into risk register

**Decision Ownership:**
- What's in scope: **Product Manager**
- Technical feasibility and complexity: **Engineering Lead**
- Effort estimates: **Developers** (facilitated by Engineering Lead)
- Security requirements: **Security Owner**
- Timeline and dependencies: **Delivery Lead**
- Risk ownership and mitigation: **Project Manager**

**Escalation Path:** Scope conflict? → PM + PdM → Sponsor | Technical blocker? → Engineering Lead → Delivery Lead

---

## Communication Cadence by Role Pair

| Primary Role | Secondary Role | Cadence | Purpose |
|---|---|---|---|
| Project Manager | Delivery Lead | Weekly | Align on timeline, risks, blockers |
| Product Manager | UX Researcher | Weekly | Validate design decisions against user needs |
| Engineering Lead | Developers | Daily | Stand up, remove blockers, design reviews |
| Delivery Lead | Engineering Lead | Bi-weekly | Assess technical readiness, manage dependencies |
| Support Liaison | Delivery Lead | Per-release | Deployment window coordination, support handoff |
| Security Owner | Engineering Lead | Per-feature | Threat modeling, security review completion |
| Data Analyst | Product Manager | Weekly | Success metric progress, insights |
| QA | Developers | Daily | Test results, bug triage, acceptance validation |

---

## Decision Matrix: Who Decides What?

### Feature Scope & Prioritization
- **What features to build?** → **Product Manager** (with stakeholder input)
- **How to prioritize the backlog?** → **Product Manager** (with PM and Engineering Lead input)
- **Can we descope a feature?** → **Product Manager** + **Project Manager** (may escalate to Sponsor)

### Technical Decisions
- **Architecture & design?** → **Engineering Lead** (with team input)
- **Which tech stack?** → **Engineering Lead** (with security review from Security Owner)
- **Code quality standards?** → **Engineering Lead**
- **Is the code ready to merge?** → **Engineering Lead** (via code review)

### Delivery & Timeline
- **Release date & milestones?** → **Delivery Lead** + **Project Manager** (with PM input)
- **Deployment window?** → **Delivery Lead** (coordinated with Support Liaison)
- **Go/No-Go for release?** → **Delivery Lead** (escalates to PM/Sponsor if high risk)

### Quality & Acceptance
- **Are acceptance criteria met?** → **QA** (validated by Developers & Product Manager)
- **Is the design pixel-perfect?** → **UX Researcher/Designer** (reviewed with Developers)
- **Is it secure & compliant?** → **Security Owner** (reviewed with Engineering Lead & Developers)

### Incident & Escalation
- **Is this incident critical?** → **Support Liaison** + **Engineering Lead**
- **Do we rollback or patch?** → **Engineering Lead** + **Delivery Lead** (Support Liaison provides customer context)
- **Is this a security incident?** → **Security Owner** (coordinates incident response)

---

## Avoiding Common Bottlenecks

### Bottleneck: Unclear Accountability for Technical Decisions
**Solution:** Engineering Lead owns architecture; escalates trade-offs with PM to Project Manager if schedule impact.

### Bottleneck: Design Changes Late in Development
**Solution:** UX Researcher finalizes design before feature enters development; changes after must go through change control.

### Bottleneck: Security Review Delays Release
**Solution:** Security Owner reviews design early; include security requirements in acceptance criteria; run security tests in CI.

### Bottleneck: Support Not Ready for Deployment
**Solution:** Delivery Lead coordinates support readiness checklist 2 weeks before release; Support Liaison owns runbooks and training.

### Bottleneck: Metrics Not Available Post-Release
**Solution:** Data Analyst defines instrumentation requirements during planning; Developers implement before release; validated before deployment.

### Bottleneck: Production Incidents Lack Context
**Solution:** Support Liaison provides customer impact and context; escalates with severity and timeline; owns communication to customers.

---

## When to Escalate

### Level 1: Team-Level Triage (Daily Standup)
- Blocker prevents daily work (e.g., broken build, unclear requirement)
- Owned role: Engineering Lead or Project Manager
- Resolution: Remove blocker within 24 hours or escalate

### Level 2: Cross-Team Coordination (Weekly Sync)
- Dependency between teams or roles (e.g., design not ready, API spec unclear)
- Owned role: Project Manager or Delivery Lead
- Resolution: Coordinate owners; resolve within 1 week or escalate

### Level 3: Risk or Schedule Impact (Sponsor Review)
- Significant schedule delay, resource constraint, or business risk
- Owned role: Project Manager or Delivery Lead
- Resolution: Adjust scope, timeline, or resources; escalate to Sponsor if needed

### Critical: Production Incident (Incident Commander)
- Customer-impacting production issue
- Owned role: Support Liaison or Engineering Lead (triggers incident response)
- Resolution: Triage severity; activate incident commander; coordinate rapid resolution

---

## Using This Guide

1. **During Planning:** Use the "Decision Matrix" to clarify who owns what
2. **During Execution:** Reference "Communication Cadence" to schedule syncs
3. **During Risk:** Check "Escalation Paths" to know when and how to escalate
4. **During Incidents:** Use "Interaction Patterns" to coordinate response
5. **Resolving Conflicts:** Reference "Decision Matrix" to clarify authority and ownership
