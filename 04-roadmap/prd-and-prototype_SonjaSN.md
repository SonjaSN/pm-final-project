# PRD & Prototype Sprint (Module 4)

## Pick & scope with MoSCoW
- **The “Now” feature I’m scoping (name + one-line core description):** "Why we ask" on every income question (addresses research theme that consumers don't understand why information is requested)
- **My finalized Must-Haves (after overriding the AI):** 1. Each note answers three things: why it's needed, how the answer is used, and who can see it. Dropping any one leaves part of her doubt open. "How used" must state plainly whether the answer feeds a recommendation, in line with the explainability guardrail.
2. The note sits inline, under the question, with no tap needed. She is on a phone with little time, and a hidden note is one she won't open.
3. Readable on a small screen and reachable by screen readers. A note she can't read or hear fails her.
- **What I demoted from Must → Should/Won’t, and why:** 1. Plain German, short, no legal wording. The pilot is in Germany. Set a hard length cap, for example one or two short sentences per note. => Should, because even in Germany we're international
2. Every claim in the note is true and signed off by legal and data-protection. A wrong statement about who sees her data makes her trust worse. I can't supply the access and retention facts, so they must come from the data-protection team. Start the review in week 1, since it is the real lead time. => Should, because it would need lots of efforts getting all signs together which would make it not a quick-win anymore

## Generate your Simplified PRD
- **One thing my PRD makes explicit that a vague brief would have missed:** It makes explicit that the note’s content is a compliance-gated deliverable, not just interface copy

## Prompt-to-prototype sprint
- **Where did the prototype reveal a gap in my PRD logic? (what I had to update):** The PRD says a field without an approved note must not render, but never says what happens to the journey then (skip, block, or route to an agent), so the prototype made the question a dead end with Continue disabled and only the agent link left, which could strand Mara on any question whose copy fails review.
- **My prototype, as a link or a screenshot (publish or share from your tool; in Lovable that is Share → Share Preview, in Bolt Publish → Web. No share URL? Screenshot the working flow):** See Link
