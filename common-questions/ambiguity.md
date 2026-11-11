# Tell Me About a Time You Acted Quickly Without Complete Information

**Leadership Principle:** Bias for Action  
**Use:** [Protecting Service During an EC2 API Incident](../core-stories/regional-ec2-api-incident-response.md)

## Draft answer

> During an incident, an EC2 API failure in one region prevented Karpenter from launching replacement instances. I needed to protect service capacity without making the affected region less stable while AWS recovered. I failed traffic over to the other region and froze Karpenter in the affected region so it would not continue creating node churn during the API failure. Once AWS Health reported the issue as resolved, I still did not immediately return all traffic. I waited additional time, then failed traffic back gradually to avoid a thundering-herd problem during recovery. The service stayed available through the other region, and we returned to normal operation in a controlled way. The fast action was not just failing over; it was stabilizing the affected system and recovering carefully.

## Skim notes

- Regional EC2 outage.
- Fail over region.
- Pause Karpenter actions.
- Await AWS Health.
- Gradual traffic return.
- Stabilize, then recover.

## What to emphasize

- Failing over was only one part of the response; explain why freezing Karpenter mattered.
- A fast response still used safeguards: AWS Health confirmation, extra wait time, and gradual failback.
- Be clear about how you verified capacity and health in both regions.

## Details to confirm

- How traffic was failed over and how the receiving region’s capacity was verified.
- What you used to freeze Karpenter and how you confirmed it was not changing nodes.
- AWS Health signal, additional wait time, and failback increments.
- Customer impact, incident duration, and any post-incident prevention work.

## Likely follow-ups

- How did you know the other region could handle the traffic?
- Why not immediately fail all traffic back when AWS Health turned green?
- What would you have done if the EC2 API remained unavailable longer?
