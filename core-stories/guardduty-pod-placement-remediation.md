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

- What GuardDuty finding or alert pattern was recurring?
- What specific pod-placement configuration was wrong?
- How did you prove the misconfiguration was the source of the alerts?
- How did you validate that the remediation worked and the alerts stopped?
- How many alerts, clusters, workloads, or teams were affected?
- Did you document the root cause or create a safeguard to prevent recurrence?

## Likely follow-ups

- Why had the issue gone unresolved for so long?
- How did you decide this was worth investigating?
- What did the logs show that changed the team’s understanding?
- How did you ensure the fix did not create a new scheduling or availability issue?
