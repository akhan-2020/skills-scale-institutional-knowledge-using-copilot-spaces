# OctoAcme — Release & Deployment Guide

## Purpose
Standardize how OctoAcme releases features to production to reduce risk and improve observability.

## Release Types
- Patch: hotfixes addressing critical production issues
- Minor: incremental features and improvements
- Major: significant functionality or breaking changes

## Pre-release requirements
Use the comprehensive [Release Readiness Checklist](./checklist-release-readiness.md) to ensure:
- All acceptance criteria met and PRs merged
- Passing CI and security scans
- Release notes drafted
- Rollback / mitigation plan documented
- Smoke tests prepared
- [Definition of Done](./template-definition-of-done.md) criteria verified

## Deployment Checklist
See the detailed [Release Readiness Checklist](./checklist-release-readiness.md) for comprehensive pre-release, deployment, and post-release steps.

### Quick Reference
- [ ] Deployment window scheduled (if needed)
- [ ] Backup or snapshot (if applicable)
- [ ] Deploy to staging and run smoke tests
- [ ] Deploy to production (automated pipeline preferred)
- [ ] Run post-deploy verifications
- [ ] Monitor metrics and error rates
- [ ] Announce release to stakeholders and support

## Post-Release Verification
Follow the [Release Readiness Checklist](./checklist-release-readiness.md) post-release section:
- Monitor application health and metrics (first 1-4 hours)
- Validate user flows and gather feedback (first 24 hours)
- Track success metrics (first week)
- Address any issues discovered
- Update Project README with release status

## Rollback & Incident Playbook
- If a deployment fails or causes a critical issue:
  - Trigger incident response and notify on-call
  - Rollback to last known-good release if necessary
  - Triage root cause and capture action items
  - Document incident in Decision Log
  - Update Risk Register with learnings

## Release Notes Template
- Release name / number:
- Date:
- Summary:
- Notable changes:
- Migration steps (if any):
- Known issues:

## Inputs & Outputs

### Inputs to Release
- Completed and tested features (from Execution)
- Updated [Definition of Done](./template-definition-of-done.md) verification
- Release notes and documentation
- Deployment plan and rollback strategy
- Stakeholder approvals

### Outputs from Release
- Deployed production release
- Release announcement and documentation
- Post-deployment metrics and monitoring data
- Incident reports (if any)
- Updated Project README with release status
- Learnings for next release

## Related Documents
- [Execution & Tracking](./octoacme-execution-and-tracking.md) - previous phase
- [Retrospective & Continuous Improvement](./octoacme-retrospective-and-continuous-improvement.md) - next phase
- [Release Readiness Checklist](./checklist-release-readiness.md)
- [Definition of Done Template](./template-definition-of-done.md)
- [Risk Register Template](./template-risk-register.md)
