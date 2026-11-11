# Mentoring Interns and New Grads Through a Cloud-Native Learning Path

## Leadership Principles demonstrated

- [Hire and Develop the Best](../leadership-principles/hire-and-develop-the-best.md) — primary
- [Strive to be Earth’s Best Employer](../leadership-principles/strive-to-be-earths-best-employer.md)
- [Learn and Be Curious](../leadership-principles/learn-and-be-curious.md)

## STAR story

### Situation

Interns and new graduates need a way to build practical cloud and platform-engineering skills without being dropped directly into a production-grade Kubernetes platform. The technologies are interconnected, and learning one tool in isolation does not prepare someone to understand how an application moves from a simple website to a production delivery workflow.

### Task

Create a structured, hands-on learning path that shares the platform concepts I use at work, builds skills in a safe sequence, and gives interns and new grads a clear route from basic cloud services to modern CI/CD.

### Action

I created a progressive set of labs where each stage builds on the prior one:

1. Build a static website in an S3 bucket.
2. Build a dynamic website on an EC2 instance.
3. Recreate the dynamic website with infrastructure as code using CDK.
4. Containerize the dynamic website and run it as an ECS service.
5. Build an EKS cluster with foundational platform capabilities, including Argo CD and Karpenter.
6. Build a delivery pipeline across build, development, test, and production environments using Kargo.

I use the path to share the platform concepts and learning sequence that helped me build my own cloud-native capability. Each lab has a visible outcome, introduces one new layer of complexity, and makes the next stage feel like a natural extension of the last rather than an unrelated technology exercise.

### Result

The learning path gives interns and new grads a concrete way to develop platform skills through real builds instead of passive documentation or isolated tutorials. It creates a shared vocabulary for discussing the current platform and a repeatable foundation for growing from basic AWS services into container orchestration and progressive delivery.

## Why this story fits

- **Hire and Develop the Best:** I created a repeatable mechanism to help early-career engineers build practical capability and confidence.
- **Strive to be Earth’s Best Employer:** I invested in a learning environment that makes growth more accessible, structured, and hands-on.
- **Learn and Be Curious:** The path encourages people to build, test, and connect technologies rather than memorize them in isolation.

## Details to add before the interview

- How many interns or new grads have used the learning path?
- Which labs have you personally taught, reviewed, or improved based on learner feedback?
- What was one learner’s starting point and concrete outcome after completing part of the path?
- How long does each stage take, and what does a successful completion look like?
- What guardrails keep AWS costs, permissions, and security safe in the labs?
- How does the final Kargo pipeline compare with the delivery platform you use at work?
- What feedback or evidence shows that the path builds learner independence?

## Likely follow-ups

- Why did you choose this sequence instead of teaching Kubernetes first?
- How do you adapt the path for someone with different prior experience?
- How do you know when a learner is ready to move to the next stage?
- How do you balance giving help with letting someone learn through debugging?
- What would you add next to the curriculum?
