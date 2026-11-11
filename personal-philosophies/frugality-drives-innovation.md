# Frugality Is a Driver of Innovation

## My view

I do not think frugality is only about finding unused resources and reducing a monthly bill. That work matters, but the more valuable version of frugality happens at design time: treating cost as a constraint that pushes you toward a better system.

When cost is part of the design, it can force useful questions. Can this environment create itself instead of requiring manual setup? Can it clean itself up when the work is done? Can the same design be reused safely? Often, the answer improves more than cost—it improves repeatability, speed, and reliability.

## Example: a Kubernetes practice environment

I wanted hands-on Kubernetes practice using EKS because that was the platform I used at work. Running a persistent personal EKS environment would have created ongoing cost, so I designed constructs that could bootstrap the environment when I needed it and tear it down automatically afterward.

The cost constraint led to a more useful design than a permanently running lab. The environment became repeatable, self-service, and disposable, which made it easier to practice without carrying idle infrastructure costs.

I later incorporated the self-bootstrapping idea into a new EKS construct I created at work. What started as a personal cost-control mechanism became a design pattern with practical value in a production engineering context.

## Skim notes

- Frugality is a design input, not only post-hoc cost cleanup.
- Wanted to practice Kubernetes on EKS because it matched the production platform.
- Persistent personal infrastructure would create unnecessary recurring cost.
- Built constructs that bootstrap the environment and automatically tear it down.
- Result: reusable, disposable, self-service practice environment with lower idle cost.
- Reused the self-bootstrapping pattern in a new EKS construct at work.
- Better design can be cheaper, more repeatable, faster, and more reliable.

## Interview answer

> I think frugality is more than finding resources that should be turned off. The best form of frugality is using cost as a design constraint early, because it can lead to a better system. For example, I wanted to practice Kubernetes with EKS because that was the platform I used at work. Rather than leave a personal environment running, I built constructs that could bootstrap it when needed and automatically tear it down afterward. That eliminated idle cost, but it also made the environment repeatable and disposable. I later incorporated the self-bootstrapping pattern into an EKS construct I created at work. The lesson for me was that cost constraints can be a design factory: they push you to simplify, automate, and build something that is often better than the original approach.

## Details to add before the interview

- What did the EKS construct provision and tear down?
- What triggered automatic teardown, and what guardrails prevented accidental cost or data loss?
- What specific part of the self-bootstrap pattern was reused at work?
- What improvement did the work version create: setup time, reliability, standardization, or cost?
