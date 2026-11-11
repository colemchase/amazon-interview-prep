# Tell Me About a Failure or Mistake

**Leadership Principles:** Earn Trust; Insist on the Highest Standards

**Use:** [Pioneering an HGN-Based Impaired-Driving Detection Prototype](../core-stories/hgn-impaired-driving-detection.md)

## Draft answer

> In my undergraduate capstone project, I built a machine-learning model that graded a user’s movement. Based on my K-fold validation results, I told the team the model was 99 percent accurate. A few weeks before I was scheduled to present the project at a research technology event, I discovered that the result was flawed: the evaluation was being affected by the order in which I had fed the training samples to the model. I had put all passing samples first and all failing samples last. When I corrected that configuration and reran the evaluation, accuracy dropped to 75 percent.
>
> I was disappointed, but presenting the 99 percent result would have been misleading. I told the team immediately, explained the error and its impact, and took ownership of correcting it. Over the following week, I improved the model using a valid evaluation approach and raised its accuracy into the low 90s. I presented the accurate result at the event, and the project received full university funding to pursue a patent. The mistake taught me that validation results are only as trustworthy as the evaluation setup, and that bad news needs to be shared quickly when others are relying on your work.

## What the interviewer is listening for

- You own the mistake without blaming people or circumstances.
- You acted to limit the impact and communicated honestly.
- You changed a process, habit, or system so the same failure is less likely to recur.

## Skim notes

- Movement-grading capstone.
- Report 99% accuracy.
- Ordered-data validation flaw.
- Accuracy falls 75%.
- Share bad news.
- Ethically rebuild model.
- Patent funding awarded.
- Validate validation setup.

## Details to add before the interview

- What K-fold configuration or data-processing behavior allowed ordering to affect the evaluation?
- How did you confirm the corrected evaluation was valid?
- What model, feature, or training changes raised accuracy from 75% into the low 90s?
- Who did you tell, how did they respond, and what did they need from you next?
- What did you change in your validation process afterward?

## Likely follow-ups

- How did you discover the ordering issue?
- Why did you trust the original validation result?
- How did you improve the model without compromising the evaluation again?
- How has this changed how you validate technical results today?
