# Tell Me About a Time You Worked Through Ambiguity

**Leadership Principles:** Dive Deep; Insist on the Highest Standards

**Use:** [Restoring Consistent SSM Access](../core-stories/ssm-node-access-standardization.md)

## Draft answer

> I was initially asked to investigate why we did not have SSM access to nodes in development. I found that access worked in test but not in production, so the problem was not as simple as a broken dev configuration. A senior engineer’s initial hypothesis was an instance-log or node-permissions issue. The node permissions looked correct, and we could not inspect the node logs because the missing SSM access was exactly what prevented us from reaching them.
>
> I reframed the problem as a cross-environment comparison. Since the networking had been configured manually rather than through CDK, there was no single source of truth to compare. I used the working test environment to access a node and trace the actual network path. Seeing that its traffic was exiting through the public internet gave me the clue to compare endpoint DNS behavior and private hosted zones across environments. I then created a truth table of the networking conditions required for access and used it to compare development, test, and production. That narrowed the problem to inconsistent private-hosted-zone entries and VPC associations for the `dkr.ecr` endpoints.
>
> I wrote an idempotent script to fix the immediate issue and created a QA regression test. I then scheduled and implemented the long-term CDK change so the configuration became repeatable and the environments would stay aligned. The fix is still in place today. The ambiguity was not resolved by guessing; it was resolved by creating a structured comparison when there was no documentation or consistent infrastructure definition to rely on.

## What the interviewer is listening for

- You make progress when requirements, ownership, or the answer is unclear.
- You separate facts, assumptions, and decisions that need validation.
- You create clarity for other people, not only yourself.

## Skim notes

- Development SSM failure.
- Permissions/logs hypothesis.
- Permission check passed.
- Compare environment networking.
- Test public egress.
- Inspect DNS behavior.
- Missing CDK baseline.
- Truth-table comparison.
- Script, test, CDK.
- Durable configuration remains.

## Details to add before the interview

- What conditions and columns did the truth table include?
- What observation proved the test node was using public egress, and what was the expected path in each environment?
- Which environment differences ruled out the original permissions hypothesis?
- Why did the `dkr.ecr` private hosted zone and VPC associations affect node SSM access?
- What did the idempotent script change, and how did the QA regression test validate it?
- How did you schedule, review, and roll out the CDK fix?

## Likely follow-ups

- What made you suspect networking rather than permissions?
- How did you use the working test environment as a baseline?
- How did the public-egress observation point specifically to the private hosted zone?
- Why did you choose a script first and CDK second?
- How did you make sure the environments would not drift again?
