# OctoAcme — Execution & Tracking

## Purpose
Guidance for managing day-to-day execution and tracking progress toward project milestones.

## Team Rhythm
- Daily standups (15 min) — focus on progress, blockers, dependencies
- Weekly delivery sync — show progress, updates, and flagged risks
- Demo/Review at the end of each sprint or milestone

## Workflows
- Use the project board (e.g., GitHub Projects) with columns: Backlog, Ready, In Progress, In Review, QA, Done
- Update Project README weekly with status and progress
- Pull Request workflow:
  - Small PRs (<= 400 lines when possible)
  - Include issue link and acceptance criteria in PR description
  - Verify [Definition of Done](./template-definition-of-done.md) criteria are met
  - Run automated tests and linting in CI before requesting review
  - Require at least one approval before merging (or team-defined policy)
- Track important decisions in [Decision Log](./template-decision-log.md)

## Quality & Testing
- Follow team's [Definition of Done](./template-definition-of-done.md)
- Unit tests for new logic
- Integration tests where applicable
- End-to-end smoke tests for critical flows before release
- Security scanning in CI
- Manual QA for feature acceptance when needed

## Reporting & Metrics
- Track velocity and burndown
- Monitor success metrics identified in the Project One-pager
- Use dashboards for key signals (errors, latency, usage)

## Blocker Escalation
- Level 1: Team-level triage in daily standup
- Level 2: PM escalates to Product Lead and dependent teams
- Level 3: Sponsor-level escalation for business-impacting issues

## Execution Checklist
- [ ] Branching and PR conventions documented in repo
- [ ] CI configured for tests and lint
- [ ] Definition of Done displayed and enforced
- [ ] Regular demos scheduled
- [ ] Risk register updated weekly
- [ ] Decision log maintained for key choices
- [ ] Project README updated with weekly status

## Inputs & Outputs

### Inputs to Execution
- Prioritized backlog (from Planning)
- Definition of Done
- Risk Register with initial risks
- Release plan and milestones
- Project README with team structure and cadence

### Outputs from Execution
- Working software increments
- Updated Risk Register with new/mitigated risks
- Decision Log with architecture and design choices
- Updated Project README with current status
- Test results and quality metrics
- Demo artifacts and stakeholder feedback
- Burndown/velocity metrics

## Related Documents
- [Project Planning](./octoacme-project-planning.md) - previous phase
- [Release & Deployment](./octoacme-release-and-deployment.md) - next phase
- [Definition of Done Template](./template-definition-of-done.md)
- [Decision Log Template](./template-decision-log.md)
- [Risk Register Template](./template-risk-register.md)
- [Project README Template](./template-project-readme.md)
