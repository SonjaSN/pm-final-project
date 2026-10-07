# AI Synthesis, Product Health & Insights Summary (Module 2)

## Responses
- **Moment of misery / red flag #1 (e.g., “user gave up after 3 tries”):** Every second journeys isn't ending in an agreement
- **Moment of misery / red flag #2:** Every fifth user miss a payment after 60 days
- **Moment of misery / red flag #3:** More than every second agent is busy with payment, legal and enforcement processes
- **Product Health & Insights Summary (Claude's output):** Product Health & Insights Summary: Digital Instalment Journey
Executive Summary

The platform's components exist and function (portal, payment processing, case management, agent workflows), but they are not joined into a coherent journey. Technically the product is available, yet the user experience loses 54% of started journeys before agreement, and 31% of starters still contact an agent within 7 days. Even completed journeys are fragile: 19% of new agreements miss a payment within 60 days, and the north-star SSR counts a plan as resolved at creation, so it can overstate real health.

Thematic Synthesis

1. Journey Friction and Drop-off (Discovery/UX)
Consumers enter the portal at a reasonable rate (38%), but progress narrows sharply at the instalment step. The journey is spread across the portal, letters, digital reminders, decision logic and agent processes, so users like Mara, on a phone with little time, have no single coherent path. Many fall back on calling.

Over half of started journeys (54%) end without an agreement. Critical
31% of journey starters contact an agent within 7 days, which undermines the self-service intent. High
Multi-claim consumers are unsure whether claims can be handled together. Medium

2. Comprehension, Trust and Perceived Risk
Research points to a confidence gap more than a feature gap. Consumers don't know what an affordable plan looks like, don't understand why information is requested, and fear that a wrong answer or missed payment will make things worse. This is likely to drive both abandonment and escalation, though the brief itself cautions that some themes may matter less than they appear.

No guidance on what an affordable agreement looks like. High
Unexplained purpose for income and affordability questions. High
Fear of consequences from incorrect answers or missed payments. High
Vulnerable consumers lack a clearly visible support path. High

3. Affordability Data Quality
The affordability step produces unreliable inputs. Consumers supply incomplete information or documents they struggle to find, which pushes work back to agents and weakens the basis for plan decisions.

28% of uploaded income documents need clarification or review. High
Incomplete affordability data feeds plans that consumers cannot sustain. High
Data quality varies across acquired portfolios, which complicates consistent decisioning. Medium

4. Plan Sustainability and Portfolio Economics
Agreements are being created that do not hold. This matters most on purchased portfolios, where Riverty bears the loss directly and short-term commitments can reduce long-term value.

19% of new agreements miss a payment within 60 days. Critical
Optimising for agreement volume or higher monthly payments risks masking worse outcomes for consumers and portfolios. High

5. Agent Handoff and Operational Load
When digital journeys escalate, agents receive too little context. They re-verify identity, affordability and case details, and lack visibility of what the consumer entered, why a recommendation was made, and how current the data is.

Escalations arrive without a summary of consumer inputs or decision rationale. High
Repeated manual verification and follow-up, in a workload where payment, legal and enforcement processes already take over 50% of agent capacity. High
No easy, auditable way for agents to correct a poor automated result. Medium

6. Measurement and Instrumentation
The product cannot yet reliably show whether it is helping. SSR credits a plan at creation rather than at completion, and analytics tooling needs better instrumentation.

SSR can rise while plan failure and consumer harm rise. Critical
Limited visibility into where in the journey users abandon and why. High
Minor Technical Debt

Inconsistent chatbot/voicebot availability across contexts, and uneven analytics tagging across channels.
- **Did the AI catch the specific moment of misery / pain point you found in Step 1?:** 1 out of 3, yes
- **Did it smooth over a critical frustration into a generic bullet point?:** Partly, yes
- **Did the AI try to suggest features or a roadmap despite the constraints?:** Not explicitly, but it smuggled in solution-shaped framing
- **Logic leak / hallucination #1 (e.g., “AI suggested a new search bar feature, roadmap leak”):** "The platform's components exist and function." is a hallucinated fact
- **Logic leak / hallucination #2:** "Consumers enter the portal at a reasonable rate (38%)" has no benchmark to judge whether 38% is reasonable or not / good or bad
