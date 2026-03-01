# Release Readiness Checklist

## Purpose
Ensure comprehensive preparation, execution, and verification for production releases to minimize risk and maximize reliability.

## When to use
- Before any production deployment
- During release planning and preparation
- As a gate for release approval
- For post-release verification

## How to use
1. Begin checklist review 1-2 weeks before planned release
2. Assign ownership for each section
3. Track completion in release planning meetings
4. Do not proceed with release until all critical items are complete
5. Use this checklist for retrospective review

---

## Pre-Release Preparation

### Code & Quality
- [ ] All planned features merged to release branch
- [ ] All acceptance criteria met for included features
- [ ] Code freeze communicated to team (no new features)
- [ ] Code review completed for all changes
- [ ] [Definition of Done](./template-definition-of-done.md) criteria met for all items
- [ ] No critical or high severity bugs in release scope
- [ ] Performance benchmarks met (load time, API latency, etc.)
- [ ] Security scan passed (no critical/high vulnerabilities)
- [ ] Dependency audit completed (no critical vulnerabilities)
- [ ] License compliance verified

### Testing
- [ ] Unit tests passing (coverage meets minimum: ___%)
- [ ] Integration tests passing
- [ ] End-to-end tests passing in staging
- [ ] Regression tests completed (existing features work)
- [ ] Browser/platform compatibility testing done
- [ ] Mobile responsiveness verified (if applicable)
- [ ] Accessibility testing completed (WCAG compliance)
- [ ] Performance/load testing completed (if applicable)
- [ ] Security testing completed (penetration test, if needed)
- [ ] Usability testing with target users (if applicable)
- [ ] Edge cases and error scenarios tested

### Infrastructure & Environment
- [ ] Staging environment matches production configuration
- [ ] Database migrations tested in staging
- [ ] Configuration changes documented and reviewed
- [ ] Environment variables/secrets configured in production
- [ ] Infrastructure capacity verified (scale for expected load)
- [ ] Monitoring and alerting configured for new features
- [ ] Log aggregation and error tracking configured
- [ ] Backup and disaster recovery verified
- [ ] SSL/TLS certificates valid and up to date
- [ ] CDN and caching configured (if applicable)

### Documentation
- [ ] Release notes drafted and reviewed
- [ ] User-facing documentation updated
- [ ] API documentation updated (if API changes)
- [ ] README or CHANGELOG updated
- [ ] Internal runbooks updated
- [ ] Known issues documented
- [ ] Migration guides created (if breaking changes)
- [ ] Training materials updated (if needed)

### Communication & Planning
- [ ] Release date and time scheduled
- [ ] Deployment window communicated to stakeholders
- [ ] Maintenance notification sent to users (if downtime expected)
- [ ] Support team briefed on changes and potential issues
- [ ] Customer success team notified of new features
- [ ] Sales/marketing team updated (if customer-facing changes)
- [ ] On-call rotation confirmed for release window
- [ ] Incident response plan reviewed

### Rollback & Risk Management
- [ ] Rollback plan documented and tested
- [ ] Previous stable version tagged and accessible
- [ ] Database rollback strategy defined (if schema changes)
- [ ] Feature flags configured for gradual rollout (if applicable)
- [ ] Canary deployment strategy defined (if applicable)
- [ ] Risks documented in [Risk Register](./template-risk-register.md)
- [ ] Emergency contacts list updated
- [ ] Rollback decision criteria defined (e.g., error rate threshold)

### Approvals & Sign-offs
- [ ] Product Manager approval
- [ ] Engineering Lead approval
- [ ] QA sign-off
- [ ] Security review (if required)
- [ ] Compliance review (if required)
- [ ] Stakeholder approval (if required)

---

## Release Execution

### Pre-Deployment (Day Of)
- [ ] Team availability confirmed (deployment team + on-call)
- [ ] Communication channels ready (Slack, war room, etc.)
- [ ] Monitoring dashboards open and reviewed
- [ ] Final smoke tests run in staging
- [ ] Database backup completed (if applicable)
- [ ] Deployment checklist printed/accessible
- [ ] Go/no-go decision made

### Deployment Steps
- [ ] Announce deployment start to team and stakeholders
- [ ] Enable maintenance mode (if applicable)
- [ ] Run database migrations (if applicable)
- [ ] Deploy application code to production
- [ ] Update configuration/environment variables
- [ ] Restart services or refresh application (as needed)
- [ ] Disable maintenance mode
- [ ] Verify deployment completed successfully

### Immediate Post-Deployment
- [ ] Application health check passes
- [ ] Core functionality smoke tests pass
- [ ] Critical user flows tested in production
- [ ] Error rates reviewed (should be at baseline)
- [ ] Performance metrics reviewed (latency, throughput)
- [ ] Database connections healthy
- [ ] Background jobs running correctly
- [ ] Integrations with external services working
- [ ] No critical errors in logs

---

## Post-Release Verification

### Monitoring & Observability (First 1-4 Hours)
- [ ] Application metrics monitored (CPU, memory, disk, network)
- [ ] Error rates within acceptable thresholds
- [ ] Response times/latency within SLA
- [ ] Database performance normal (query time, connections)
- [ ] API endpoints responding correctly
- [ ] Background job queues processing normally
- [ ] Third-party integrations functioning
- [ ] User traffic patterns normal
- [ ] No unexpected alerts triggered

### User Validation (First 24 Hours)
- [ ] User feedback channels monitored (support, social media)
- [ ] No spike in support tickets
- [ ] User authentication/login working
- [ ] Key user workflows verified by customers
- [ ] A/B test or feature flag metrics reviewed (if applicable)
- [ ] Analytics tracking working correctly
- [ ] No reports of data loss or corruption

### Extended Monitoring (First Week)
- [ ] Success metrics trending positively
- [ ] User adoption of new features tracking as expected
- [ ] System stability maintained over time
- [ ] No increase in technical debt or incidents
- [ ] Performance benchmarks remain within acceptable range

---

## Post-Release Communication

### Internal Communication
- [ ] Deployment completion announced to team
- [ ] Status update sent to stakeholders
- [ ] Engineering team notified of any issues to watch
- [ ] On-call schedule confirmed for post-release period

### External Communication
- [ ] Release announcement published (blog, social media, etc.)
- [ ] Release notes shared with users
- [ ] Customer support team updated with FAQ
- [ ] Training or demo sessions scheduled (if applicable)
- [ ] Maintenance completion notification sent (if applicable)

---

## Rollback Procedures

### Rollback Decision Criteria
Initiate rollback if:
- [ ] Critical functionality is broken
- [ ] Error rate exceeds ___% above baseline
- [ ] Performance degradation > ___% (e.g., 50% slower response time)
- [ ] Data integrity issues detected
- [ ] Security vulnerability introduced
- [ ] Unable to diagnose/fix within ___ minutes/hours

### Rollback Execution
- [ ] Notify stakeholders of rollback decision
- [ ] Enable maintenance mode (if applicable)
- [ ] Revert application code to previous version
- [ ] Rollback database migrations (if safe to do so)
- [ ] Revert configuration changes
- [ ] Restart services
- [ ] Verify previous version is functioning
- [ ] Disable maintenance mode
- [ ] Announce rollback completion
- [ ] Schedule post-mortem

---

## Post-Release Retrospective

### Review (Within 1-2 Days)
- [ ] Retrospective scheduled with team
- [ ] Release metrics reviewed (time, issues, etc.)
- [ ] What went well documented
- [ ] What could be improved documented
- [ ] Action items created for improvements
- [ ] Update release process documentation based on learnings
- [ ] Celebrate successes!

### Follow-up Actions
- [ ] Address any technical debt introduced
- [ ] Resolve known issues documented in release notes
- [ ] Implement process improvements identified
- [ ] Update this checklist based on learnings

---

## Checklist Customization

Adjust this checklist based on:
- **Release size:** Hotfixes may skip some items; major releases need more rigor
- **Risk level:** Higher risk changes need more testing and validation
- **Project type:** Internal tools vs. customer-facing vs. enterprise SaaS
- **Compliance:** Regulated industries may need additional approvals

---

## Related Documents
- See [octoacme-release-and-deployment.md](./octoacme-release-and-deployment.md) for release process overview
- See [template-definition-of-done.md](./template-definition-of-done.md) for quality standards
- See [template-risk-register.md](./template-risk-register.md) for risk management
- See [octoacme-project-management-overview.md](./octoacme-project-management-overview.md) for overall project lifecycle
