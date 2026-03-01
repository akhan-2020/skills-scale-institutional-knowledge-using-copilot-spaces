# Definition of Done (DoD) Template

## Purpose
Establish clear, consistent quality standards that all work items must meet before being considered complete, reducing rework and ensuring predictable quality.

## When to use
- During project planning to define team-wide standards
- When creating backlog items with acceptance criteria
- During code reviews and QA to verify completeness
- In sprint planning to confirm items are ready for "Done" column

## How to use
1. Customize this template during project planning based on your project's needs
2. Document your team's DoD in the project README or CONTRIBUTING guide
3. Reference the DoD in backlog items, PRs, and during reviews
4. Review and refine the DoD during retrospectives

## Standard Definition of Done Checklist

### Code Quality
- [ ] Code follows team coding standards and style guide
- [ ] Code is peer-reviewed and approved (minimum reviewers: ___)
- [ ] No linting errors or warnings (unless explicitly documented/suppressed)
- [ ] Code is well-structured, readable, and maintainable
- [ ] No commented-out code or debug statements left in
- [ ] Technical debt is documented if intentionally introduced

### Testing
- [ ] Unit tests written and passing (minimum coverage: ___%)
- [ ] Integration tests written and passing (if applicable)
- [ ] Manual testing completed for UI/UX changes
- [ ] Edge cases and error handling tested
- [ ] Regression tests pass (existing functionality unaffected)
- [ ] Performance testing completed (if applicable)
- [ ] Accessibility requirements met (WCAG compliance if applicable)

### Documentation
- [ ] Code comments added for complex logic
- [ ] README updated (if new features or setup changes)
- [ ] API documentation updated (if API changes)
- [ ] User-facing documentation updated (if needed)
- [ ] CHANGELOG or release notes updated
- [ ] Architecture diagrams updated (if design changed)

### Security & Compliance
- [ ] Security scan passed (no critical/high vulnerabilities)
- [ ] No secrets or credentials in code
- [ ] Input validation and sanitization implemented
- [ ] Authorization/authentication verified (if applicable)
- [ ] Data privacy requirements met
- [ ] Compliance requirements addressed (e.g., GDPR, SOC2)

### Integration & Deployment
- [ ] CI/CD pipeline passes (all stages green)
- [ ] Build completes successfully
- [ ] Deployment tested in staging/preview environment
- [ ] Database migrations tested and documented (if applicable)
- [ ] Configuration changes documented
- [ ] Rollback plan documented (for risky changes)
- [ ] Feature flags configured (if using gradual rollout)

### Acceptance Criteria
- [ ] All acceptance criteria from the issue/story met
- [ ] Product Owner or stakeholder review completed (if required)
- [ ] Design specifications matched (for UI changes)
- [ ] Success metrics instrumented (logging, analytics, monitoring)

### Housekeeping
- [ ] Issue/story moved to "Done" in project board
- [ ] Related issues linked and closed (if applicable)
- [ ] Branch merged and deleted (if using feature branches)
- [ ] PR description includes context, changes, and testing notes

## Customizing Your DoD

Different project types may need different standards. Consider:

### For MVP/Prototype Projects
- Reduce testing requirements (focus on critical paths)
- Simplify documentation (inline comments may suffice)
- Allow for documented technical debt

### For Production/Critical Systems
- Increase testing requirements (add load/stress testing)
- Require security review for all changes
- Mandate chaos engineering or failure testing
- Require runbook updates

### For Open Source Projects
- Add contributor license agreement check
- Require maintainer approval
- Ensure contribution guidelines followed

## Acceptance Criteria Template

Each backlog item should have specific acceptance criteria in addition to the general DoD:

```markdown
## Acceptance Criteria

Given [context/precondition]
When [action/event]
Then [expected outcome]

### Example:
Given a user is logged in
When they click "Export Data"
Then a CSV file downloads containing their account data
And the download is logged for audit purposes
And the user receives a confirmation message
```

### Alternative Format (Checklist)

For simpler items, use a checklist:

```markdown
## Acceptance Criteria
- [ ] User can click "Export Data" button
- [ ] CSV file downloads with correct data format
- [ ] Download is logged for audit purposes
- [ ] User sees confirmation message
- [ ] Works in Chrome, Firefox, Safari, Edge
```

## Definition of Ready (DoR)

Consider also defining when items are ready to be worked on:

### Definition of Ready Checklist
- [ ] User story/requirement is clear and understandable
- [ ] Acceptance criteria defined
- [ ] Dependencies identified and resolved
- [ ] Estimated by the team
- [ ] Design mockups available (for UI work)
- [ ] API contracts defined (for integration work)
- [ ] Test data or test environment available
- [ ] No blocking issues

## Best Practices
- **Keep it realistic:** DoD should be achievable, not aspirational
- **Team ownership:** Entire team should agree on and commit to the DoD
- **Living document:** Update the DoD as team practices evolve
- **Visible:** Keep DoD in project README or pinned to project board
- **Enforced consistently:** Don't waive requirements without team discussion
- **Balanced:** Balance quality with delivery speed for your context
- **Automated:** Automate checks where possible (linting, tests, security scans)

## Handling Exceptions
When an item can't meet all DoD criteria:
1. **Document why** in the PR or issue
2. **Create follow-up issue** to address gaps
3. **Get team consensus** before merging
4. **Update risk register** if it introduces technical debt
5. **Track exceptions** and discuss in retrospectives

## Related Documents
- See [octoacme-project-planning.md](./octoacme-project-planning.md) for defining DoD during planning
- See [octoacme-execution-and-tracking.md](./octoacme-execution-and-tracking.md) for applying DoD during execution
- See [octoacme-project-management-overview.md](./octoacme-project-management-overview.md) for overall quality standards
