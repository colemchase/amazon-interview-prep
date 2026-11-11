# Pioneering an HGN-Based Impaired-Driving Detection Prototype

## Leadership Principles demonstrated

- [Think Big](../leadership-principles/think-big.md) — primary
- [Learn and Be Curious](../leadership-principles/learn-and-be-curious.md)
- [Ownership](../leadership-principles/ownership.md)
- [Deliver Results](../leadership-principles/deliver-results.md)

## STAR story

### Situation

I lost my father to a drunk driver just as I was beginning my undergraduate computer science degree. Soon afterward, I saw a university posting for a software-engineering research role. The team had an early sketch for a device that could sit in a car, monitor a driver’s eye-gaze patterns, and prevent the vehicle from shifting out of neutral when the driver appeared impaired.

I was at the beginning of my computer science education, but the problem had personal meaning. I shared that motivation in the interview and treated the project as an opportunity to build the skills needed to make a real contribution.

### Task

Turn an early concept into an evidence-based prototype: devise a method for detecting impairment, build and test the system, gather data ethically, and present a credible result to the university research community.

### Action

I began by designing an approach around horizontal gaze nystagmus (HGN), a test commonly used in field-sobriety examinations. I incorporated an open-source computer-vision model on an edge device to track eye movement. The test device used a small screen and camera to guide the user through the nystagmus test.

I designed the system so the edge device handled the user-facing eye tracking while AWS handled heavier computation and cold storage. I then built a prototype that worked in a car and could prevent it from shifting out of neutral when the defined impairment condition was met.

After the prototype was working, I conducted an IRB-approved study and collected hundreds of ethically obtained samples to evaluate the device. I presented the resulting work at the University of Virginia symposium. After the presentation, I worked with patent lawyers to draft and pursue patent applications.

### Result

The university provided full funding to pursue a patent. I received the patent earlier this year. The work also outlived my direct involvement: students in following cohorts received grants to continue the research and development of the product I pioneered.

## Why this story fits

- **Think Big:** I helped turn an early concept into a safety-focused research and product effort with long-term continuation beyond the original prototype.
- **Learn and Be Curious:** I built new capability across computer vision, edge devices, AWS, research methods, and patent development while still early in my degree.
- **Ownership:** I took the work from an initial research opportunity through prototype, IRB study, presentation, and patent pursuit.
- **Deliver Results:** I built a working prototype, gathered evidence through an approved study, presented it successfully, and helped carry it through to a patent.

## Impact metrics

- **Research evidence:** Collected **hundreds of ethically obtained samples** through an IRB-approved study.
- **Recognition:** Received full university funding for patent pursuit after the University of Virginia symposium presentation.
- **Durability:** Received a patent, and subsequent student cohorts received grants to continue the research and development.

## Details to add before the interview

- The exact patent title, patent number, and grant date that are safe to share.
- The study’s sample size, participant criteria, and the metrics used to evaluate the prototype.
- The computer-vision model, edge-device hardware, AWS services, and which tasks ran where.
- The definition and safeguards for the condition that kept the vehicle in neutral.
- The specific accuracy, false-positive, or other performance results from the study.
- Your collaborators’ roles and your exact individual ownership at each stage.
- The name and year of the University of Virginia symposium.
- The grants or continuation work by the following student cohort.

## Likely follow-ups

- Why was HGN the right starting point for this product?
- How did you ensure the study was ethical and the data was reliable?
- What technical challenge was hardest: computer vision, edge hardware, vehicle integration, or cloud design?
- How did you decide what belonged on the edge device versus AWS?
- What did you learn from the patent process?
- What would you improve if you were continuing the product today?
