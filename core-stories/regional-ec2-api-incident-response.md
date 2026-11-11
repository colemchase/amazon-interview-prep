# Protecting Service During an EC2 API Incident

## Leadership Principles demonstrated

- [Bias for Action](../leadership-principles/bias-for-action.md) — primary
- [Dive Deep](../leadership-principles/dive-deep.md)
- [Insist on the Highest Standards](../leadership-principles/insist-on-the-highest-standards.md)

## STAR story

### Situation

During an incident, the EC2 API in one region was unavailable. Karpenter could not launch replacement instances there, creating a risk to service capacity and traffic handling.

### Task

Keep the service available while avoiding additional node churn in the affected region, then return traffic safely only after AWS indicated that the underlying EC2 issue was resolved.

### Action

I failed traffic over to the other region to protect availability. I then froze Karpenter in the affected region so it would not continue trying to destroy or replace nodes while the EC2 API was unhealthy.

I monitored the AWS Health status and waited until it reported the service was safe before beginning recovery. I did not immediately send all traffic back. I waited additional time and then failed traffic back gradually, rather than creating a sudden surge that could have contributed to a thundering-herd problem while AWS was recovering.

### Result

Traffic remained served through the other region during the EC2 API incident. By freezing Karpenter, waiting for the AWS Health confirmation, and using a gradual failback, I protected the service through the incident and returned it to normal operation without adding avoidable recovery pressure.

## Why this story fits

- **Bias for Action:** I made the timely decision to fail traffic over and stabilize the affected region rather than waiting for the outage to resolve itself.
- **Dive Deep:** I connected the EC2 API failure to Karpenter’s inability to launch instances and adjusted the system’s behavior accordingly.
- **Insist on the Highest Standards:** I did not treat the first healthy signal as sufficient for full recovery; I used a cautious, staged return to reduce risk.

## Details to add before the interview

- Which AWS Region was affected, which region received the traffic, and what service or customers were affected?
- What signals showed the EC2 API issue and Karpenter launch failures?
- How did you fail traffic over, freeze Karpenter, and verify that each action took effect?
- What AWS Health signal did you wait for, and how long did you wait after it became healthy?
- What did the gradual failback look like: traffic percentages, timing, health checks, or rollback criteria?
- What capacity was available in the receiving region, and how did you confirm it could absorb the traffic?
- Were any runbooks, alarms, capacity changes, or post-incident actions created afterward?

## Likely follow-ups

- Why was freezing Karpenter necessary after traffic had already failed over?
- How did you decide it was safe to fail traffic back?
- Why did you choose a gradual failback instead of returning all traffic at once?
- What would you have done if the receiving region had not had enough capacity?
