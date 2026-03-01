# OctoAcme — Risk Management & Communication

## Purpose
Explain how to identify, manage, and communicate risks and dependencies.

## Risk Register
Use the [Risk Register Template](./template-risk-register.md) to maintain a structured table with:
- ID
- Description
- Category (Technical/Resource/Schedule/External/etc.)
- Impact (High/Med/Low)
- Likelihood (High/Med/Low)
- Priority (calculated)
- Owner
- Mitigation plan
- Status
- Last updated

## Risk Lifecycle
- Identify: during planning and ongoing execution
- Assess: estimate impact and likelihood
- Mitigate: reduced via actions, contingency plans
- Monitor: review at weekly syncs and update status

## Stakeholder Communication
- Identify stakeholder groups and communication needs (e.g., engineering, sales, support)
- Provide regular updates (weekly or milestone-based)
- Use Project README as the single source of truth (see [template-project-readme.md](./template-project-readme.md))
- Keep status information in one place to avoid confusion
- Share key decisions from [Decision Log](./template-decision-log.md) with stakeholders

## Communication Templates
Weekly Status Template:
- Progress this week:
- Next steps:
- Risks & blockers:
- Ask / decisions needed:

Incident Communication
- Triage summary
- Actions being taken
- Expected timeline
- Post-incident blameless retrospective scheduled

## Escalation Paths
- Team-level -> PM -> Product Lead -> Sponsor
- For security incidents, follow the security incident runbook and notify Security on-call
- Document escalation decisions in [Decision Log](./template-decision-log.md)

## Inputs & Outputs

### Inputs to Risk & Communication Management
- Initial risks from Project Initiation
- Ongoing risk identification during Execution
- Stakeholder requirements and expectations
- Project status and progress updates
- Incident reports and issues

### Outputs from Risk & Communication Management
- Updated Risk Register with current risks and mitigations
- Stakeholder status updates and reports
- Escalation notifications when needed
- Decision Log entries for risk-related choices
- Communication plans and cadence schedules

## Related Documents
- [Project Management Overview](./octoacme-project-management-overview.md)
- [Project Planning](./octoacme-project-planning.md) - initial risk assessment
- [Execution & Tracking](./octoacme-execution-and-tracking.md) - ongoing risk monitoring
- [Risk Register Template](./template-risk-register.md)
- [Decision Log Template](./template-decision-log.md)
- [Project README Template](./template-project-readme.md)
