# Decision Log Template

## Purpose
Track important project decisions, their rationale, alternatives considered, and outcomes to maintain institutional knowledge and ensure transparency.

## When to use
- During planning when making architectural or design decisions
- During execution when choosing between implementation approaches
- When making scope, schedule, or resource trade-offs
- When stakeholder alignment on a direction is needed

## How to use
1. Create a Decision Log document in your project repository (e.g., `DECISIONS.md`)
2. Add entries as decisions are made throughout the project lifecycle
3. Reference decision IDs in related issues, PRs, and documentation
4. Review during retrospectives to understand decision impacts

## Template Structure

### Decision Log

| ID | Date | Decision | Context | Alternatives Considered | Decision Maker(s) | Status | Outcome/Impact |
|----|------|----------|---------|------------------------|-------------------|--------|----------------|
| D-001 | YYYY-MM-DD | Brief decision statement | Why this decision was needed | Other options evaluated | Name(s) | Active/Superseded/Reversed | Impact or result |

## Example Entry

| ID | Date | Decision | Context | Alternatives Considered | Decision Maker(s) | Status | Outcome/Impact |
|----|------|----------|---------|------------------------|-------------------|--------|----------------|
| D-001 | 2026-01-15 | Use REST API instead of GraphQL | Need simple integration with existing services; team has more REST experience | GraphQL, gRPC | Sarah Chen (PdM), Dev Team Lead | Active | Faster implementation; some over-fetching in mobile app |

## Detailed Decision Record (Optional)

For complex or high-impact decisions, you may want to create a separate markdown file with more detail:

```markdown
# Decision: [Brief Title]

**ID:** D-XXX  
**Date:** YYYY-MM-DD  
**Status:** [Proposed / Accepted / Superseded / Deprecated]  
**Decision Makers:** [Names and roles]

## Context
What is the issue we're trying to solve? What are the constraints?

## Decision
What are we choosing to do?

## Alternatives Considered
1. **Option A:** [Description, pros, cons]
2. **Option B:** [Description, pros, cons]
3. **Option C:** [Description, pros, cons]

## Rationale
Why did we choose this option?

## Consequences
- Positive consequences
- Negative consequences
- Risks and mitigation

## Follow-up Actions
- [ ] Action item 1
- [ ] Action item 2
```

## Best Practices
- **Log early:** Capture decisions when made, not in retrospect
- **Be concise but clear:** Enough context for future readers to understand
- **Include alternatives:** Shows due diligence and helps with future similar decisions
- **Update status:** Mark decisions as superseded when circumstances change
- **Link to artifacts:** Reference related PRs, designs, or discussions
- **Review regularly:** During retrospectives and project reviews

## Related Documents
- See [octoacme-project-planning.md](./octoacme-project-planning.md) for when to create decision logs
- See [octoacme-execution-and-tracking.md](./octoacme-execution-and-tracking.md) for decision tracking during execution
- See [octoacme-project-management-overview.md](./octoacme-project-management-overview.md) for overall artifact guidance
