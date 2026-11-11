# Tell Me About a Time You Raised the Bar on Quality or Security

**Leadership Principle:** Insist on the Highest Standards  
**Use:** [Resolving a Multi-Year GuardDuty Alert Issue](../core-stories/guardduty-pod-placement-remediation.md)

## Draft answer

> Our team had received GuardDuty alerts for years, and the accepted assumption was that they were an EKS problem outside our control. The pods were eventually being placed, so the issue had become normalized. I did not believe eventual security coverage was an acceptable standard: if the intended security posture is delayed, there is still a period without it. I used available time to investigate the logs and traced the alerts to a pod-placement misconfiguration. I corrected the configuration so that placement happened immediately rather than eventually. That resolved a multi-year issue and eliminated the gap before the expected security posture was in place. The key decision was refusing to accept a degraded security outcome just because the system eventually recovered.

## Skim notes

- Multi-year GuardDuty alerts had been normalized as an EKS-owned issue.
- Standard: delayed security coverage is not acceptable security coverage.
- Investigated logs; found a pod-placement misconfiguration.
- Corrected configuration so placement was immediate, not eventual.
- Eliminated the security-posture gap and resolved the longstanding alert issue.

## What to emphasize

- State the standard you applied: immediate, not eventual, security coverage.
- Explain why the existing assumption was insufficient without criticizing prior owners.
- Be ready to describe how you validated the absence of new scheduling or availability risks.

## Details to confirm

- The GuardDuty finding, pod-placement misconfiguration, and exact validation.
- Scope: alerts, clusters, workloads, or teams affected.
- Documentation, monitoring, or preventive guardrails added after remediation.

## Likely follow-ups

- Why had the issue persisted for so long?
- How did you balance urgency with validating the change?
- What did you do to ensure the alert would not recur?
