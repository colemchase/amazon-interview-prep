# Tell Me About a Time You Simplified a Complex Process

**Leadership Principle:** Invent and Simplify  
**Use:** [Automating SRE Maintenance](../core-stories/sre-maintenance-automation.md)

## Draft answer

> On an SRE team, recurring maintenance work had become a collection of manual fixes that demanded continuous attention. It was complex in practice because every task interrupted higher-value work, even when many of the steps were repeatable. I mapped the maintenance work by the level of judgment it required. I automated the repeatable tasks and turned the low-supervision tasks into reusable workflows that could run in the background. I deliberately retained manual handling for work where active operational judgment was important. That simplified the operating model from constant manual intervention to a clear split between automated, supervised, and hands-on work. It freed enough capacity to address developer requests and clear a service desk backlog that had existed for over a year.

## Skim notes

- Manual maintenance interrupted higher-value work.
- Classified tasks by the operational judgment they required.
- Automated repeatable tasks; background workflows for low-supervision work.
- Kept high-judgment work manual.
- Simplified to three paths: automated, supervised, hands-on.
- Result: more developer capacity and a year-old backlog cleared.

## What to emphasize

- Simplification is not automation for its own sake; it removes unnecessary human effort safely.
- Describe the decision rule that separated fully automated work from supervised and manual work.
- Connect the simpler process to business impact: faster response to developers and a cleared backlog.

## Details to confirm

- One before-and-after example of a maintenance task.
- The reliability checks and ownership model for each automated workflow.
- Time saved per week or month.

## Likely follow-ups

- What was the most difficult workflow to simplify?
- How did you make the automation safe?
- How could another engineer understand and operate the new process?
