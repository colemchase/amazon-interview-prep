# Automating SRE Maintenance to Clear a Longstanding Ticket Backlog

## Leadership Principles demonstrated

- [Invent and Simplify](../leadership-principles/invent-and-simplify.md) — primary
- [Ownership](../leadership-principles/ownership.md)

## STAR story

### Situation

I joined an SRE team after most of the architecture had already been built. In my first few months, maintenance fixes consumed a significant amount of my time. That made it difficult to respond to developer requests and complete other service desk tickets, while the ticket board continued to carry a longstanding backlog.

### Task

Reduce the time and attention required for recurring maintenance work so that I could keep the platform healthy while making consistent progress on developer asks and the service desk backlog.

### Action

I examined the maintenance tasks that were consuming the most time and simplified their execution. For work that did not need ongoing human judgment, I implemented automation. For tasks that needed light supervision, I wrote reusable skills and workflows so they could run as background work rather than requiring my full attention from start to finish.

I treated the maintenance burden as a system problem to improve, rather than accepting it as the permanent cost of operating the existing architecture. This created a clearer separation between work that required active SRE judgment and work that could be automated or supervised asynchronously.

### Result

Recurring maintenance tasks became either fully automated or background tasks. This created capacity to handle developer asks and other tickets, and it allowed me to clear the service desk ticket board for the first time in over a year.

## Why this story fits

- **Invent and Simplify:** I reduced a complex, manual operating model by automating repeatable work and creating reusable workflows for low-supervision tasks.
- **Ownership:** I improved the system causing the maintenance burden instead of only working through the next individual fix.

## Impact metrics

- **Backlog outcome:** Cleared the service desk ticket board for the first time in **over one year**.
- **Capacity outcome:** Converted recurring maintenance work from active, manual effort into automated or background work, freeing time for developer requests and other tickets.

## Details to add before the interview

- Biggest manual tasks.
- Automated/supervised split.
- Tools/workflows built.
- Time saved.
- Backlog size/duration.
- Safety guardrails.
- Developer turnaround.

## Likely follow-ups

- Automation criteria.
- Why manual?
- Hardest simplification.
- Reliability proof.
- Prevent backlog return.
