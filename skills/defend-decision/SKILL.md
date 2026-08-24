---
name: defend-decision
description: Harden a product design decision until it survives being questioned — name the alternative at its strongest, name what the choice costs, name what would prove it wrong, and predict the outcome that will cut against it. Use when recording a decision, writing an ADR or design rationale, preparing to defend a call in review, or when a stated reason sounds more like a preference than a decision. For writing up finished work use write-case-study; for the underlying philosophy see randy-design-eng.
---

# Defending a Decision

A construction skill. It does ONE thing: take a design decision and turn it into one that survives interrogation. It does not write case studies (that's `write-case-study`) or teach the underlying philosophy (that's `randy-design-eng`).

The test a decision has to pass: **someone who disagrees with you reads it and concedes you understood their position and paid a real price for yours.**

## The Failure This Fixes

Most stated decisions are preferences wearing a decision's clothes:

> "We used progressive disclosure because it keeps the interface clean."

Nothing here is falsifiable. No alternative, no cost, no way to be wrong. It cannot be reviewed, only agreed or disagreed with.

## The Four Moves

Work them in order. Do not skip to 3.

### 1. State the action, not the goal

One sentence, active voice, naming what was done.

- ✗ "We prioritized trust." → a goal
- ✗ "We took an accessibility-first approach." → a posture
- ✓ "Plant recognition shows the top candidates and requires the user to confirm one." → an action

If the sentence has no verb someone could have refused to do, it is not a decision yet.

### 2. Build the alternative at its strongest

Write the option you rejected the way its best advocate would. Then check it against this list — if any apply, you have built a strawman and must rewrite:

- The alternative sounds obviously worse
- The alternative's advantage is not named at all
- The alternative is described only by its downside
- No competent person would choose it

**Ask directly: what is this alternative genuinely better at?** Every real alternative is better at something. Find it and write it down.

| Strawman | Real alternative |
| --- | --- |
| "A form would be rigid and annoying" | "A form produces clean structured input, is far easier to validate, and reads as more professional" |
| "Building from scratch would take too long" | "A clean sheet gives total control of the foundation with no inherited mistakes" |
| "A mandate wouldn't have worked" | "A policy on a delivery gate is measurable, fundable, and has a completion date" |
| "The magic version would be creepy" | "Surfacing the result without explanation is a dramatically better demo moment" |

### 3. Name the price, not the risk

A risk is something that might happen. A cost is something you paid. Decisions have costs.

Costs come in recognizable shapes — find yours:

| Shape | Example |
| --- | --- |
| A worse experience for a named group | Experienced users have to earn their way to depth they already know they want |
| Inherited constraints | You take on the foundation's awkward decisions along with its good ones |
| A metric you can no longer report | Aiming past conformance loses the clean audit score |
| Time | Multi-tenant from day one added three weeks |
| Money or compute | ~15% higher token cost per generation |
| Surface area | A two-layer API is twice the documentation |
| Data quality | A one-tap rating buys volume and loses depth |

**If you cannot find a cost, the decision was not real.** Either the alternative was never viable — say so and stop calling it a decision — or you have not looked hard enough.

### 4. Predict the outcome that will cut against you

Before the result is in, write the sentence you expect to regret. Then, when the result arrives, check it and report honestly.

Three honest endings:

- **The cost landed as predicted.** "Users in sparse regions got a populated feed, and the content they got was the least climate-relevant. Exactly as designed."
- **The cost landed harder than predicted, and it's yours.** "Developers did not find the primitives on their own. That is a documentation failure, not an architecture one, and it is mine to fix."
- **The cost did not land, and here's why you think that is.** Say why, and say if you are not sure.

A fourth ending — no downside at all — means the report has been cleaned. Go back.

## Output Format

Produce this structure, one block per decision:

```markdown
### <Title: the choice, phrased as "X over Y" or "X instead of Y">

**Decision.** <One sentence. Active voice. What was done.>

**Alternative, at its strongest.** <What you passed on, and what it is genuinely better at.>

**Cost.** <The specific thing given up. Not a risk. A price.>

**Outcome.** <What happened, including the part that cut against you.>
```

Title the decision as a contrast — `"Ranked candidates over a single confident answer"`, `"Evangelism instead of enforcement"` — so the tradeoff is visible before the reader has read anything else.

## Reviewing Someone Else's Decision

Output a markdown table. One row per issue.

| Before | After | Why |
| --- | --- | --- |
| "We chose X because it's cleaner" | "We chose X over Y; Y was better at Z; X cost us W" | No alternative and no cost — a preference |
| "The alternative would have been too slow" | "The alternative gave total control of the foundation" | Strawman: names only the downside |
| "There was a risk users wouldn't find it" | "Users did not find it. That's a documentation failure and it's mine" | A risk is not a cost; report what landed |
| "The result was a complete success" | "It cut both ways, as designed: <upside>, and <downside>" | An outcome with no cost is incomplete |

## Quick Checklist

- [ ] The decision is an action someone could have refused to take
- [ ] The alternative is stated with what it is genuinely better at
- [ ] A competent person could have chosen the alternative
- [ ] The cost is a price paid, not a risk mitigated
- [ ] The cost is specific enough to be checked
- [ ] The outcome contains something you would rather delete
- [ ] The title names the contrast, not the feature
