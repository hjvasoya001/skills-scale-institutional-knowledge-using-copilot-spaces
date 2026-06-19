# OctoAcme Personas

This document defines typical roles and responsibilities used in OctoAcme project docs and exercises.

---

## Core Delivery Roles

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

### Key Interactions
- **Engineering Lead**: Seeks guidance on architecture and design decisions; escalates technical blockers
- **QA/Testing**: Collaborates on test coverage and acceptance criteria definition
- **Product Managers**: Clarifies requirements and acceptance criteria

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

### Key Interactions
- **Project Managers**: Align on timelines, scope, and priorities
- **UX Researcher/Designer**: Validate design and user research insights
- **Data Analyst/Measurement Owner**: Define and track success metrics
- **Developers**: Clarify requirements and validate feasibility

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

### Key Interactions
- **Product Managers**: Align on priorities and timelines
- **Delivery Lead**: Coordinate on cross-team dependencies and milestone readiness
- **Engineering Lead**: Assess technical feasibility and risks
- **Support Liaison**: Coordinate production issue escalations

---

## Cross-Functional & Leadership Roles

## Engineering Lead

### Role Summary
Technical leadership for the project; ensures architectural integrity and technical direction. The Engineering Lead removes technical blockers, makes critical design decisions, and mentors the development team.

### Responsibilities
- Own major technical architecture and design decisions
- Review technical designs and approve implementations
- Remove technical blockers and unblock the team
- Mentor developers and guide technical problem-solving
- Coordinate with other engineering teams on integrations and dependencies
- Assess technical feasibility and risks for new features
- Define code quality standards and testing requirements

### Goals
- Ensure scalable, maintainable architecture
- Minimize technical debt and rework
- Foster a culture of technical excellence
- Reduce time spent on technical blockers

### Typical Communication
- Design reviews and architecture discussions
- Technical spike assessments and feasibility studies
- Code review feedback and guidance
- Cross-team technical coordination

### Key Interactions
- **Developers**: Provides technical guidance and removes blockers
- **Project Managers**: Assesses feasibility, estimates impact, escalates technical risks
- **QA/Testing**: Defines test strategy and coverage requirements
- **Delivery Lead**: Escalates cross-team technical dependencies
- **Security Owner**: Collaborates on security architecture and threat modeling

---

## Delivery Lead

### Role Summary
Focused on delivery orchestration and cross-team coordination to meet milestones. The Delivery Lead ensures all dependencies are managed, deployment readiness is maintained, and teams stay synchronized.

### Responsibilities
- Track release milestones and delivery timelines
- Coordinate cross-team dependencies and integration points
- Maintain release readiness checklist and deployment schedules
- Run delivery-focused syncs and escalation meetings
- Manage deployment windows and coordinate with support teams
- Identify and resolve blockers that span multiple teams
- Track post-release verification and rollback procedures

### Goals
- Deliver features on schedule and on scope
- Minimize delays caused by cross-team dependencies
- Ensure smooth, low-risk deployments
- Maintain clear visibility into delivery status

### Typical Communication
- Delivery sync meetings and cross-team coordination calls
- Release readiness checklists and deployment timelines
- Dependency and blocker escalation reports
- Post-deployment verification and incident communication

### Key Interactions
- **Project Managers**: Coordinates on timelines and priorities
- **Engineering Lead**: Ensures technical readiness and manages technical dependencies
- **Support Liaison**: Coordinates production deployments and support handoffs
- **Security Owner**: Ensures security reviews and approvals are completed before release
- **Data Analyst/Measurement Owner**: Coordinates instrumentation and monitoring setup

---

## UX Researcher / Designer

### Role Summary
Ensures product decisions are informed by user research and design principles. The UX Researcher/Designer validates design decisions, defines usability requirements, and advocates for user needs.

### Responsibilities
- Conduct user research, interviews, and usability testing
- Validate product designs and feature concepts with users
- Define accessibility and usability acceptance criteria
- Create design assets, specs, and interaction documentation
- Collaborate on feature prioritization based on user feedback
- Review implementations for design fidelity and usability

### Goals
- Ensure features are intuitive and user-friendly
- Reduce support burden through better UX
- Validate product-market fit through user feedback
- Maintain consistent design language and accessibility standards

### Typical Communication
- Research findings and usability test results
- Design specs and interaction documentation
- Feedback on feature implementations and prototypes
- Accessibility and design review comments

### Key Interactions
- **Product Managers**: Provides user research insights to inform prioritization
- **Developers**: Clarifies design intent and reviews implementations
- **QA/Testing**: Defines acceptance criteria for user-facing quality
- **Project Managers**: Communicates design-related timeline impacts

---

## Security Owner

### Role Summary
Responsible for security posture and compliance for the project scope. The Security Owner ensures security requirements are defined, threats are modeled, and vulnerabilities are remediated.

### Responsibilities
- Define security requirements and compliance needs for the project
- Conduct threat modeling and security reviews of designs
- Ensure CI/CD security scanning and checks are configured
- Review code and architecture for security vulnerabilities
- Coordinate with Security on-call team for incident response
- Track security-related action items and remediation efforts
- Provide security guidance and best practices to the team

### Goals
- Prevent security vulnerabilities from reaching production
- Maintain compliance with organizational and regulatory standards
- Foster a security-aware development culture
- Minimize security incident impact and response time

### Typical Communication
- Threat modeling sessions and security reviews
- Vulnerability reports and remediation tracking
- Security scanning and CI configuration reviews
- Incident response coordination and post-incident analysis

### Key Interactions
- **Engineering Lead**: Collaborates on secure architecture and design
- **Developers**: Provides security guidance and reviews code
- **Delivery Lead**: Ensures security reviews and approvals before release
- **Project Managers**: Communicates security-related timeline impacts and risks

---

## Support Liaison (Customer/Production Support)

### Role Summary
The bridge between product/support teams and the delivery team for production issues and customer impact. The Support Liaison ensures production quality, triages incidents, and advocates for customer needs.

### Responsibilities
- Triage and prioritize customer-impacting production incidents
- Provide context and business impact assessment for bugs and issues
- Own post-release support handoff documentation and runbooks
- Coordinate hotfixes and critical patches with the delivery team
- Escalate production issues to engineering and product teams
- Gather customer feedback and report trends to product
- Coordinate with QA on smoke tests and production validation

### Goals
- Minimize customer impact from production issues
- Enable fast incident response and resolution
- Ensure smooth deployments with minimal support disruption
- Advocate for reliability and customer needs in prioritization

### Typical Communication
- Incident reports and escalation notifications
- Support readiness documentation and runbooks
- Customer feedback summaries and trend reports
- Hotfix coordination and deployment windows

### Key Interactions
- **Project Managers**: Escalates production issues and communicates customer impact
- **Engineering Lead**: Provides context on incident severity and customer impact
- **Delivery Lead**: Coordinates hotfixes and deployment windows
- **QA/Testing**: Collaborates on smoke tests and production validation
- **Developers**: Provides customer context and priority for bug fixes

---

## Data Analyst / Measurement Owner

### Role Summary
Owns instrumentation and success-metric measurement for the feature. The Data Analyst ensures data quality, validates analytics, and provides insights to guide decisions.

### Responsibilities
- Define instrumentation and telemetry requirements
- Implement tracking for success metrics and user behavior
- Validate data quality and accuracy of analytics
- Produce dashboards and analyses for key metrics
- Provide insights on feature usage and customer impact
- Track and communicate progress toward success metrics
- Identify anomalies and potential issues through data trends

### Goals
- Ensure decisions are informed by accurate data
- Track progress toward project success metrics
- Enable rapid feedback loops through instrumentation
- Reduce guesswork through data-driven insights

### Typical Communication
- Instrumentation requirements and data schema reviews
- Analytics dashboards and metric reports
- Data quality alerts and anomaly notifications
- Success metric progress updates and insights

### Key Interactions
- **Product Managers**: Provides analytics insights to guide decisions and prioritization
- **Developers**: Collaborates on instrumentation implementation
- **Delivery Lead**: Ensures monitoring and observability are ready before deployment
- **Engineering Lead**: Advises on data collection and performance implications

---

## QA / Testing

### Role Summary
Validates quality and acceptance criteria. QA ensures features meet requirements, work reliably, and are ready for production.

### Responsibilities
- Define and execute test plans aligned with acceptance criteria
- Conduct manual and automated testing
- Report bugs and track defect resolution
- Validate feature acceptance and quality standards
- Define smoke tests for production deployments
- Collaborate on test coverage and strategy
- Perform exploratory testing to identify edge cases

### Goals
- Catch defects early before production
- Ensure features meet acceptance criteria
- Build confidence in release quality
- Enable faster deployment cycles with high quality

### Typical Communication
- Test plans and test case documentation
- Bug reports and defect tracking
- Test execution results and quality metrics
- Smoke test results and deployment validation

### Key Interactions
- **Developers**: Reports bugs and validates fixes
- **Engineering Lead**: Collaborates on test strategy and coverage
- **Product Managers**: Clarifies acceptance criteria
- **Support Liaison**: Coordinates smoke tests and production validation

---

## How these personas are used in the exercise
- Use these persona definitions to frame scenarios and sample interactions in the Skills Exercise.
- Each persona can be used as a persona prompt for Copilot Spaces to shape role-specific guidance.
- Reference the "Key Interactions" sections to understand dependency patterns and communication flows.
- When defining ownership for decisions, refer to the specific responsibilities of each role to avoid ambiguity.
