# A/B Experiment Brief, Riverty business-unit case

## Parameters
| Parameter | Decision |
|---|---|
| Feature under test | "Why we ask" on every income question (addresses research theme that consumers don't understand why information is requested) |
| Persona | Role: The consumer Mara, a shift worker with two open claims and variable but stable income; Goal: Agree an instalment plan she can actually afford and keep, without making her situation worse; Friction: She opens the portal after a reminder and hits the income and affordability questions. She doesn't know why they're asked, what an affordable plan looks like, whether a wrong answer or a missed payment will make things worse, or whether both claims can be handled together. Unable to find the right documents or get answers, she gives up and calls an agent. This also fits your "panic" angle: the fear of consequences is the trigger. |
| Expected outcome | 31% Journey starters contacting an agent within 7 days; 28% Uploaded income documents needing clarification or review |
| Primary success metric | The share of journey starters who contact an agent within 7 days, baseline 31%, measured in the pilot segment against a comparison group |
| Baseline rate | 31% Journey starters contacting an agent within 7 days |
| Guardrail metric | 60-day plan survival: no more than 19% of new agreements missing a payment within 60 days (baseline), so a higher completion rate can't come from plans people can't keep |
| Guardrail boundary | Must not fall below 81%. Today, 19% miss a payment. No room below that baseline. |
| Second guardrail | · |
| Minimum Detectable Effect | -5% |
| Sample size per arm | 2796 |
| Traffic split | 50/50 |
| Test duration | 4 weeks |
| Significance threshold | 0.05 |

## Control vs. Variant
- **Control (A):** 31% of starters contact an agent within 7 days, roughly 2,600. The research themes say consumers don't know what's affordable, don't understand why income is requested, and fear the consequences of a wrong answer or missed payment. 28% of uploaded income documents need clarification or review.
- **Variant (B):** Screens to build (exactly 3)
Screen 1: Entry point (“Set up your instalment plan”)
•	Header and one-line intro: “Next we’ll ask about your income. Each question comes with a reason.”
•	Primary button: “Start”.
•	Secondary link: “Talk to an agent” (static stub).
•	Prototype banner: “Prototype copy, not approved by legal or data protection”.
Screen 2: Feature core (income and affordability questions)
•	Progress indicator (for example, “Question 2 of 4”).
•	Four question cards. The questions are prototype placeholders, not Riverty’s real set: net monthly income, other regular income, monthly fixed costs, and an income-document upload (simulated file picker).
•	Under each field, an always-visible note component with the labelled Why / How used / Who sees lines.
•	Inline validation message sits above the note, so the note never moves or hides.
•	“Continue” and “Back” buttons, and a persistent “Talk to an agent” link.
Screen 3: Success / confirmation (“Thanks, here’s what happens with your answers”)
•	Recap of the four answers, each with an “Edit” link back to screen 2.
•	Short “what happens next” text: “You’ll see plan options next” (stub, since plan options aren’t built).
•	Reminder of who can see the recap, reusing the approved “Who sees” copy.
•	Disabled placeholder button “Continue to plan options”.
•	“Talk to an agent” link.
Functional requirements (from MUST HAVE)
1.	100% of income and affordability fields on screen 2 (4 of 4, including the upload step) render a note. A missing note blocks the field from rendering.
2.	Every note has three non-empty parts: Why, How used, Who sees (3 of 3). A schema check fails the build otherwise.
3.	Notes are visible on load, directly below their field, with 0 taps needed.
4.	Each note is 40 words or fewer (proposed) and contains none of the terms on the legal-wording list.
5.	All copy comes from one content object keyed by question ID and locale (de-DE only). 0 hard-coded strings in components.
6.	Screen 2 works at 360px width. Body text is at least 16px, contrast is at least 4.5:1, and each note is linked to its field with aria-describedby.
7.	Answers persist across all three screens. Editing from screen 3 returns to screen 2 with 0 values lost.
8.	No note may promise an outcome (for example, “this won’t affect your plan”). A phrase check against an agreed list runs on every note.
- **Held constant (isolation check):** The consumers still not trust the why we ask statements and give up and call an agent

## Hypothesis
> I believe that "Why we ask" on every income question (addresses research theme that consumers don't understand why information is requested) for Role: The consumer Mara, a shift worker with two open claims and variable but stable income; Goal: Agree an instalment plan she can actually afford and keep, without making her situation worse; Friction: She opens the portal after a reminder and hits the income and affordability questions. She doesn't know why they're asked, what an affordable plan looks like, whether a wrong answer or a missed payment will make things worse, or whether both claims can be handled together. Unable to find the right documents or get answers, she gives up and calls an agent. This also fits your "panic" angle: the fear of consequences is the trigger. will result in 31% Journey starters contacting an agent within 7 days; 28% Uploaded income documents needing clarification or review, as measured by a -5% change in The share of journey starters who contact an agent within 7 days, baseline 31%, measured in the pilot segment against a comparison group within 4 weeks. We will protect 60-day plan survival: no more than 19% of new agreements missing a payment within 60 days (baseline), so a higher completion rate can't come from plans people can't keep throughout the test.

## Shipping criteria
> We will **ship** if The share of journey starters who contact an agent within 7 days, baseline 31%, measured in the pilot segment against a comparison group improves by ≥ -5% at 0.05 and 60-day plan survival: no more than 19% of new agreements missing a payment within 60 days (baseline), so a higher completion rate can't come from plans people can't keep does not reach Must not fall below 81%. Today, 19% miss a payment. No room below that baseline. after 4 weeks.
> We will **iterate** if direction is positive but lift is below the MDE.
> We will **kill** if the primary metric shows no improvement or moves negatively.
> The read date is fixed at the end of 4 weeks, no results reviewed before this date.
