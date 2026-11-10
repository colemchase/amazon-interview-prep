# Restoring Consistent SSM Access to EKS Nodes Across Environments

## Leadership Principles demonstrated

- [Dive Deep](../leadership-principles/dive-deep.md) — primary
- [Insist on the Highest Standards](../leadership-principles/insist-on-the-highest-standards.md)
- [Deliver Results](../leadership-principles/deliver-results.md)

## STAR story

### Situation

SSM access to EKS nodes worked in some environments but not in others. This inconsistency made node access unreliable and created risk for the operational controls needed for a FedRAMP audit.

### Task

Identify why SSM access differed by environment, restore reliable access to all nodes, and ensure the problem could not be silently repeated in future environment implementations.

### Action

I investigated the issue across environments and created a truth table to compare the conditions required for SSM access. The comparison showed that the private hosted zone entries for the `dkr.ecr` endpoints and their VPC associations were inconsistently configured. Some entries and associations existed while others did not because the setup had been performed manually.

I first stopped the immediate problem by writing a script that correctly updated the private hosted zone configuration. I also created a QA script to regression-test the fix.

Once access was restored, I implemented the hosted-zone configuration in infrastructure as code. This turned an easy-to-miss manual setup step into a repeatable, version-controlled part of every future implementation.

### Result

SSM access was made consistent for nodes across all environments. The short-term remediation restored access and added regression testing; the long-term IaC fix prevented the configuration from being forgotten in future deployments. This ensured the node-access control required for the FedRAMP audit was in place, and the audit was passed successfully.

## Why this story fits

- **Dive Deep:** I used a cross-environment truth table to isolate a configuration difference that was not apparent when looking at any single environment.
- **Insist on the Highest Standards:** I did not stop after restoring access; I eliminated the manual configuration gap and added regression testing to prevent recurrence.
- **Deliver Results:** I restored node access across environments and enabled the organization to satisfy an important FedRAMP audit requirement.

## Impact metrics

- **Coverage:** Restored and standardized SSM access for EKS nodes across **all environments**.
- **Quality:** Replaced an inconsistent manual private-hosted-zone setup with infrastructure as code and regression testing.
- **Compliance:** Ensured the required node-access control was in place for a successful **FedRAMP audit**.

## Details to add before the interview

- How many environments, VPCs, clusters, or nodes were affected?
- Which specific SSM workflow failed, and what was the operational impact?
- What columns or conditions were included in the truth table?
- Why did the `dkr.ecr` private hosted zone and VPC association affect SSM access?
- What did the short-term update script and QA regression script validate?
- How did you prove access was reliable across every environment after the change?
- Which FedRAMP control or audit requirement depended on this access?

## Likely follow-ups

- How did you choose the first data points for the truth table?
- Why were the environments configured differently in the first place?
- Why did you use a script first instead of moving immediately to IaC?
- What would have happened if the issue had remained unresolved?
- How did you validate that the IaC fix would not introduce regressions?
