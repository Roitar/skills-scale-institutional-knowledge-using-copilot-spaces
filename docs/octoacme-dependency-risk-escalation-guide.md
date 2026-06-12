# OctoAcme Dependency & Risk Escalation Guide

This guide clarifies how to identify, escalate, and track dependencies and risks across all project phases, with clear ownership and decision authority.

---

## Dependency Management

### Types of Dependencies

| Dependency Type | Example | Owner | Escalation Path |
|-----------------|---------|-------|-----------------|
| **External System** | Integration with third-party API | Engineering Ambassador | Delivery Lead → Project Manager |
| **Team/Resource** | Waiting for design review | Delivery Lead | Project Manager → Sponsor |
| **Data/Content** | Marketing copy for release notes | Stakeholder Rep | Project Manager |
| **Environment** | Staging environment not ready | Release Coordinator | Project Manager → Infrastructure |
| **Approval** | Legal review of terms | Change Owner | Project Manager → Legal |

### Dependency Tracking

**Delivery Lead** maintains a dependency log updated weekly:

```
| Dependency | Owner | Status | Risk Level | Mitigation |
|------------|-------|--------|------------|------------|
| Payment API integration | Engineering | Waiting for API keys | High | Escalate to PM by Friday |
| Design review | Engineering | In Progress | Low | On track |
| Stakeholder approval | Change Owner | Pending | Medium | Follow up Monday |
```

**Escalation Trigger:** If any dependency moves to "Blocked" or "At Risk", **Delivery Lead** immediately escalates to **Project Manager**.

---

## Risk Management

### Risk Categories & Owners

| Risk Category | Primary Owner | Secondary Owner | Escalation |
|---------------|---------------|-----------------|------------|
| **Technical** | Engineering Ambassador | Developers | Project Manager |
| **Quality** | QA/Verification Owner | Engineering Ambassador | Delivery Lead |
| **Schedule** | Delivery Lead | Project Manager | Sponsor |
| **Resource** | Project Manager | Delivery Lead | Sponsor |
| **Privacy/Compliance** | Data Privacy Lead | Engineering Ambassador | Legal / Compliance |
| **Stakeholder** | Stakeholder Rep | Project Manager | Sponsor |

### Risk Assessment Framework

**Probability:** High (>50%), Medium (20-50%), Low (<20%)  
**Impact:** High (blocks release), Medium (slips schedule), Low (workaround available)  
**Risk Level:** Probability × Impact

| Level | Color | Action |
|-------|-------|--------|
| **Critical** | 🔴 Red | Escalate immediately, daily tracking |
| **High** | 🟠 Orange | Weekly tracking, mitigation plan required |
| **Medium** | 🟡 Yellow | Bi-weekly tracking, monitor for escalation |
| **Low** | 🟢 Green | Monthly review, watch list |

---

## Weekly Risk Review Process

**When:** Every Monday, 10 AM  
**Who:** Project Manager, Delivery Lead, and role-specific owners  
**Duration:** 30 minutes  
**Cadence:** Weekly through project completion

### Agenda

1. **New Risks** (10 min)
   - Identify new risks by category
   - Assign owner and risk level
   - Define mitigation strategy

2. **Risk Status Updates** (15 min)
   - Review all open risks (Critical and High priority)
   - Update probability/impact assessments
   - Track mitigation progress

3. **Escalations & Decisions** (5 min)
   - Identify risks requiring sponsor escalation
   - Document decisions made

### Risk Log Template

```markdown
## Risk #RK-001: Payment API Delay

**Category:** Technical | **Owner:** Engineering Ambassador  
**Probability:** High | **Impact:** High | **Level:** 🔴 Critical

**Description:**
Third-party payment API integration may be delayed due to vendor processing times.

**Mitigation Strategy:**
- Contact vendor daily for status
- Prepare mock API as fallback for testing
- Plan to defer payment features to next release if necessary

**Escalation Threshold:**
If API not available 2 weeks before release date, escalate to Project Manager.

**Status:**
- [x] Mitigation plan in place
- [ ] Escalated
- [ ] Resolved

**Last Updated:** 2026-06-12
**Owner:** Alice (Engineering Ambassador)
```

---

## Role-Specific Escalation Paths

### Delivery Lead → Project Manager

**Escalate if:**
- Any Critical (🔴) risk emerges
- Dependency blocked for >1 day
- Multiple Medium risks converge
- Schedule slip imminent

**Required Info:**
- Risk/dependency description
- Impact to timeline
- Proposed mitigation or decision needed
- Escalation deadline

---

### Engineering Ambassador → Delivery Lead

**Escalate if:**
- Technical risk blocks critical path
- Architecture decision required outside team authority
- Non-functional requirement conflict

**Required Info:**
- Technical issue description
- Options considered
- Recommended approach
- Decision deadline

---

### QA/Verification Owner → Delivery Lead

**Escalate if:**
- Test environment not ready
- Quality blocker prevents acceptance
- Testing effort exceeds estimate significantly

**Required Info:**
- Quality issue or blocker
- Impact to release readiness
- Time needed to resolve
- Workaround options

---

### Data Privacy Lead → Project Manager

**Escalate if:**
- Privacy/compliance risk blocks release
- Regulatory requirement not met
- Data handling approach non-compliant

**Required Info:**
- Compliance gap identified
- Regulatory/policy violated
- Remediation required
- Timeline to fix

---

### Project Manager → Sponsor

**Escalate if:**
- Release may slip >1 week
- Budget/resource constraints prevent delivery
- Stakeholder alignment required
- Strategic decision needed

**Required Info:**
- Executive summary of issue
- Impact to business outcomes
- Options and recommendations
- Decision deadline

---

## Blocker Resolution SLA

| Blocker Type | Owner | Target Resolution Time |
|--------------|-------|------------------------|
| Critical (🔴) | Project Manager | 24 hours |
| High (🟠) | Delivery Lead | 2-3 business days |
| Medium (🟡) | Role-specific owner | 1 week |
| Low (🟢) | Role-specific owner | As scheduled |

---

## Example Escalation Scenario

**Scenario:** Testing infrastructure fails one week before release.

1. **QA/Verification Owner** identifies blocker → Updates risk log as Critical (🔴)
2. **QA Owner escalates** to **Delivery Lead** with: blocker description, impact (can't complete testing), proposed mitigation (use staging env, but slower)
3. **Delivery Lead** reviews options and escalates to **Project Manager**
4. **Project Manager** makes decision: allocate IT resources to fix infrastructure (24-hour SLA)
5. **Project Manager** communicates decision to team and stakeholders
6. **QA Owner** monitors infrastructure fix and updates risk log when resolved

---

## Risk Register Template

Maintain a project-wide Risk Register with all identified risks, owners, status, and mitigations:

```markdown
# Risk Register — [Project Name]

| ID | Category | Description | Owner | Probability | Impact | Level | Mitigation | Status | Last Updated |
|----|----------|-------------|-------|-------------|--------|-------|------------|--------|--------------|
| RK-001 | Technical | API delay | Eng Ambassador | High | High | 🔴 | Mock API fallback | In Progress | 2026-06-12 |
| RK-002 | Quality | Test env ready | QA Owner | Medium | High | 🟠 | Use staging | Monitoring | 2026-06-11 |
| RK-003 | Compliance | Data audit | Privacy Lead | Low | High | 🟡 | Audit scheduled | Planning | 2026-06-10 |
```

Update the Risk Register every Monday and share with the team and stakeholders.
