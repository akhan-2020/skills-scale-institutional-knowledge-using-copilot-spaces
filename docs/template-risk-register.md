# Risk Register Template

## Purpose
Systematically identify, assess, track, and mitigate project risks to minimize negative impacts and improve delivery predictability.

## When to use
- During project initiation (capture initial risks)
- During planning (detailed risk assessment)
- Throughout execution (ongoing risk identification and monitoring)
- During milestone reviews and retrospectives

## How to use
1. Create a Risk Register document in your project repository (e.g., `RISKS.md`)
2. Identify risks proactively during planning and execution
3. Review and update weekly during team syncs
4. Escalate high-priority risks to stakeholders
5. Mark risks as closed when mitigated or no longer applicable

## Template Structure

### Risk Register

| ID | Risk Description | Category | Impact (H/M/L) | Likelihood (H/M/L) | Priority | Owner | Mitigation Strategy | Status | Last Updated |
|----|------------------|----------|----------------|--------------------|---------|----|---------------------|--------|--------------|
| R-001 | Brief description of the risk | Technical/Resource/Schedule/External | High/Med/Low | High/Med/Low | Calculated | Name | Actions to reduce/eliminate | Open/Monitoring/Mitigated/Closed | YYYY-MM-DD |

## Risk Categories
- **Technical:** Architecture, dependencies, complexity, technical debt
- **Resource:** Team capacity, skills gaps, competing priorities
- **Schedule:** Timeline pressure, dependency delays, scope creep
- **External:** Vendor issues, regulatory changes, market shifts
- **Integration:** Cross-team dependencies, API changes, data migrations
- **Security:** Vulnerabilities, compliance, data protection
- **Quality:** Testing coverage, performance, user experience

## Priority Calculation
Use a simple formula: **Priority = Impact × Likelihood**

| Impact/Likelihood | High (3) | Medium (2) | Low (1) |
|-------------------|----------|------------|---------|
| **High (3)**      | 9 - Critical | 6 - High | 3 - Medium |
| **Medium (2)**    | 6 - High | 4 - Medium | 2 - Low |
| **Low (1)**       | 3 - Medium | 2 - Low | 1 - Low |

## Risk Status Values
- **Open:** Risk identified, mitigation planned or in progress
- **Monitoring:** Mitigation in place, watching for changes
- **Mitigated:** Successfully reduced to acceptable level
- **Closed:** No longer relevant or fully resolved
- **Accepted:** Acknowledged but no mitigation planned (document why)

## Example Entries

| ID | Risk Description | Category | Impact | Likelihood | Priority | Owner | Mitigation Strategy | Status | Last Updated |
|----|------------------|----------|--------|------------|----------|-------|---------------------|--------|--------------|
| R-001 | Third-party API may be deprecated in Q3 | External | High | Medium | 6 - High | Sarah Chen | Evaluate alternative APIs; plan migration | Monitoring | 2026-02-28 |
| R-002 | Team member on leave during final sprint | Resource | Medium | High | 6 - High | Alex Kumar | Cross-train team; adjust sprint scope if needed | Open | 2026-02-20 |
| R-003 | Database migration may cause downtime | Technical | High | Low | 3 - Medium | Dev Team | Test migration in staging; plan maintenance window | Mitigated | 2026-02-15 |

## Detailed Risk Record (Optional)

For critical risks, maintain detailed tracking:

```markdown
# Risk: [Brief Title]

**ID:** R-XXX  
**Owner:** [Name]  
**Status:** [Open/Monitoring/Mitigated/Closed]  
**Last Updated:** YYYY-MM-DD

## Description
Full description of the risk and its potential impact.

## Assessment
- **Impact:** High/Medium/Low - [Why?]
- **Likelihood:** High/Medium/Low - [Why?]
- **Priority:** [Calculated priority]

## Mitigation Strategy
1. [Specific action to reduce impact or likelihood]
2. [Specific action to reduce impact or likelihood]
3. [Contingency plan if risk occurs]

## Progress Log
- **YYYY-MM-DD:** Initial identification
- **YYYY-MM-DD:** Mitigation action X completed
- **YYYY-MM-DD:** Status updated to Monitoring
```

## Best Practices
- **Be specific:** "API may be deprecated" not just "dependency risk"
- **Assign owners:** Each risk needs someone accountable for monitoring
- **Review regularly:** Weekly reviews during execution phase
- **Update promptly:** Change status and priority as circumstances evolve
- **Don't over-index:** Focus on actionable risks, not every possible issue
- **Link to decisions:** Reference Decision Log entries for risk-related choices
- **Celebrate mitigations:** Recognize when risks are successfully handled
- **Learn from materialized risks:** Add to retrospective if risk becomes an issue

## Escalation Triggers
Escalate to stakeholders when:
- Priority 9 (Critical) risks are identified
- Priority 6+ (High) risks cannot be mitigated by the team
- Multiple risks compound to threaten project success
- Risk materializes and becomes an active issue

## Related Documents
- See [octoacme-project-initiation.md](./octoacme-project-initiation.md) for initial risk identification
- See [octoacme-project-planning.md](./octoacme-project-planning.md) for planning-phase risk assessment
- See [octoacme-execution-and-tracking.md](./octoacme-execution-and-tracking.md) for ongoing risk monitoring
- See [octoacme-risks-and-communication.md](./octoacme-risks-and-communication.md) for risk communication guidance
