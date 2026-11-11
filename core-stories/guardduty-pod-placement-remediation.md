# Resolving a Multi-Year GuardDuty Alert Issue

## Leadership Principles demonstrated

- [Bias for Action](../leadership-principles/bias-for-action.md) — primary
- [Insist on the Highest Standards](../leadership-principles/insist-on-the-highest-standards.md)

## STAR story

### Situation

GuardDuty alerts had been treated as a waste of time because the issue was believed to be owned by EKS. As a result, the alerts had persisted across both the current role and the previous role, becoming a multi-year unresolved problem.

### Task

Determine whether the alerts were genuinely outside the team’s control and, if possible, identify and remediate their underlying cause.

### Action

When I had an afternoon available, I chose to investigate rather than continue accepting the assumption that the issue was solely an EKS concern. I dove into the relevant logs and traced the alert behavior back to a pod-placement misconfiguration.

The pods were eventually placed under the prior configuration, but that delay meant the intended security posture was not available immediately. I identified the configuration issue and remediated it so placement occurred immediately. My standard was: “If we don’t have security immediately, then we don’t have it at all.”

### Result

I resolved a multi-year issue that had spanned the current and previous roles. The remediation changed pod placement from eventually occurring to occurring immediately, eliminating the period in which the expected security posture was delayed.

## Why this story fits

- **Bias for Action:** I used available time to investigate and fix a long-standing security issue rather than accepting the existing delay.
- **Insist on the Highest Standards:** I did not treat eventual security coverage as acceptable; I set immediate protection as the required standard.

## Details to add before the interview

- Recurring finding.
- Placement misconfiguration.
- Root-cause proof.
- Fix validation.
- Impact scope.
- Recurrence guardrail.

## Likely follow-ups

- Why unresolved?
- Why investigate?
- Key log evidence.
- Scheduling safety.
