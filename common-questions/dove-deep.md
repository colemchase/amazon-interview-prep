# Tell Me About a Time You Dove Deep into a Problem

**Leadership Principle:** Dive Deep  
**Use:** [Restoring Consistent SSM Access](../core-stories/ssm-node-access-standardization.md)

## Draft answer

> SSM access to EKS nodes worked in some environments but failed in others, which was a serious operational and audit risk. Looking at one environment at a time was not revealing the cause, so I created a truth table that compared every condition required for access across environments. That made the pattern visible: private hosted zone entries for the `dkr.ecr` endpoints and their VPC associations were inconsistent because the setup had been done manually. I wrote a script to restore the correct configuration immediately and a QA script to regression-test it. Then I put the hosted-zone configuration into infrastructure as code, so future environments would not depend on a manual step. The result was consistent SSM node access across all environments and the required control for a successful FedRAMP audit.

## Skim notes

- SSM node access worked inconsistently across environments; audit risk.
- Created a cross-environment truth table instead of debugging one environment at a time.
- Found inconsistent `dkr.ecr` private hosted-zone entries and VPC associations.
- Immediate fix: update script plus QA regression test.
- Durable fix: managed configuration in IaC.
- Result: consistent access everywhere; FedRAMP audit control satisfied.

## What to emphasize

- The comparison method was the turning point; it turned a confusing inconsistency into testable differences.
- Separate the immediate recovery from the durable prevention.
- Explain the business risk in plain language before the technical detail.

## Details to confirm

- The environments and conditions represented in the truth table.
- Why the endpoint DNS and VPC associations affected the SSM workflow.
- How you validated access after the script and again after the IaC rollout.

## Likely follow-ups

- Why did you start with a script rather than IaC?
- How did you prove that the configuration difference was causal?
- What would you investigate first if the issue recurred?
