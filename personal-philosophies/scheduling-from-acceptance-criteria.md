# Scheduling from Acceptance Criteria

## My view

I schedule work by defining success before I define activity. For any goal, I start with acceptance criteria: what must be true for the outcome to be complete and successful? That prevents a calendar from becoming a list of busywork.

Once the acceptance criteria are clear, I work backward from the goal. I identify the prerequisites, milestones, reviews, validation, and recovery time required to reach the outcome. I then block time for that work in the order the dependencies require, rather than filling my schedule with the most visible or urgent-looking tasks.

## Competing priorities

When priorities compete, I use the project’s core values as the decision rule. On my current project, those values are security and stability. All else equal, I choose the feature or task that produces the more secure and stable outcome.

The exception is a dependency-chain conflict: the safest or most stable next step may be blocked by a prerequisite. In that case, I make the conflict explicit and schedule the work that unblocks the dependency. The values still guide the destination; dependency chaining determines the viable sequence.

## Gauging my use of time

I periodically review where my time is actually going rather than assuming that a full calendar means progress. I separate operational work from engineering work:

- **Operational work:** on-call, incidents, tickets, requests, and manual maintenance needed to keep the service running.
- **Engineering work:** projects that create lasting value, such as automation, infrastructure as code, reliability improvements, and changes that reduce future operational load.

Google SRE uses a guardrail of at least 50% project or engineering work, with operational work capped at 50%. Its practical guidance describes roughly one-third operational work and two-thirds project work as a healthy balance. I use that as a directional health check rather than a rigid rule for every week: incidents and launches are spiky, so the pattern matters over a quarter or longer.

If repetitive maintenance starts consuming too much of my time, I treat that as a signal to create an engineering project. Manual work that only restores the current state is toil; automation or a durable redesign that prevents the work from returning is engineering. The goal is not to avoid operations—it is to use what operations teaches us to make the system more reliable and require less manual intervention.

## Skim notes

- Define acceptance criteria.
- Work backward.
- Map dependencies.
- Sequence by dependency.
- Prioritize core values.
- Security and stability.
- Default to stability.
- Unblock prerequisites first.
- Audit time allocation.
- Separate operations engineering.
- Protect engineering time.
- Automate recurring maintenance.
- Learn from operations.

## Interview answer

> I start scheduling by defining the acceptance criteria for the goal—what must be true for the work to be successful. Then I work backward to identify the dependencies, milestones, validation, and time blocks needed to get there. When priorities compete, I use the project’s core values as the decision rule. On my current project, security and stability come first, so I default to the more secure and stable option. The exception is when a dependency-chain conflict blocks that option. In that case, I make the conflict explicit and schedule the prerequisite work needed to unblock it, rather than pretending that the preferred outcome is immediately achievable.
>
> I also review how I am actually using my time. I separate operational work from engineering work that creates lasting value. As a health check, I want at least half of my time over the long term to be engineering or project work; if recurring maintenance starts taking too much capacity, that is a signal to automate or redesign it. That keeps the calendar connected to the real path to a successful outcome.

## Details to add before the interview

- One real goal where working backward changed your schedule or prevented a miss.
- The acceptance criteria, dependencies, and milestones for that example.
- A competing-priorities decision where security or stability changed the order of work.
- A dependency-chain conflict and how you resolved or communicated it.
- How you will measure operational versus engineering time: calendar categories, tickets, an iteration review, or another mechanism.
- One recurring maintenance task that should become a project to automate or redesign.
