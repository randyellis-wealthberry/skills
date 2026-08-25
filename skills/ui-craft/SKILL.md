---
name: ui-craft
description: How much an interface should assert — progressive disclosure over modes, ranked candidates over single confident answers, graceful scope degradation over empty states, composition over configuration, and designing the seam between two roles. Use when deciding what a screen shows, how sure a system should look, how a surface behaves when it has nothing or too much, what a component's API should refuse to do, or how an interface holds up in the conditions people actually use it in. For the decision framework and evidence standards see randy-design-eng; to harden one interface decision use defend-decision.
---

# Interface Craft

Every interface is continuously deciding three things: **how much to show, how sure to look, and how much rope to give.** Most bad interfaces are bad because those three were never decided — they were inherited from the data model, the component library, or the happy path.

This is the surface-level lens. The decision-level lens is in `randy-design-eng`.

## Initial Response

When this skill is invoked without a specific interface question, respond only with:

> Interface craft: disclosure, confidence, degradation, and API surface. Show me the screen, the component, or the decision you're weighing — what does it currently show, and what is it hiding? More at [work.randyellis.design](https://work.randyellis.design).

Then stop. Do not review anything until there is something concrete to review.

## Core Principles

### Confidence is a design decision, not an output format

When a system asserts something to a person — an identification, a match, a risk score, a recommendation — the interface chooses how certain to appear. That choice is yours, and it is usually made carelessly by defaulting to a single answer because that's what the function returns.

A single confident answer is the highest-cost option available: it is right or it is wrong, and when it is wrong it spends trust that took months to build.

> Ranked candidates with a confirmation step, rather than one asserted match. The confirmation built trust rather than merely preventing error — people believed an identification more once they had chosen it themselves than when the app simply asserted one.

The second-order effect matters more than the first: user confirmation made downstream community verification mean something. **Showing uncertainty did not weaken the product; it created a signal the product did not previously have.**

### One surface disclosed progressively beats two modes

Splitting an app into beginner and expert modes is the cleaner answer on a whiteboard. It is also a permanent tax: two surfaces to design, two to maintain, a mode switch to explain, and a moment where a person has to self-classify before they've used anything.

> A single interface with progressive disclosure — advanced controls surfaced as users demonstrated competence — instead of splitting the app into beginner and expert modes.

Be honest about the cost, because it is real and it lands: experienced users will say plainly that features they knew existed were buried. That is the price of the call, not evidence the call was wrong. Make it anyway when the alternative is asking people to declare their skill level before they have any.

### Degrade the scope, don't ship the empty state

An empty state is a design failure dressed as a design pattern. Before building one, ask what constraint could relax instead.

> Location-scoped discovery expanded its radius automatically when local density was too low to fill a feed. Rather than choose between relevance and a populated feed, scope degrades gracefully: tight where there was density, wider where there wasn't.

The cost is exact and predictable, and you should state it up front: **the people getting the most content are getting the least applicable content.** That is a better failure than a blank screen, but it is still a failure — say so.

### Composition over configuration

The two things a component library is pulled between are intuition and flexibility. Most systems pick one and suffer for it.

Settle it with usage data instead of taste. Instrumenting the original Chakra UI showed **80% of developers used only 20% of component props** — which is what justified a streamlined surface with advanced cases reachable through composition rather than configuration.

The API question is not "what can this component do." It is **what should this component refuse to do, and how much rope does the developer get.** A component that does everything has no opinion, and a system with no opinion is just a folder.

### Show the work being built, not that work is happening

A spinner communicates one bit: *not yet*. If the system is actually producing structured output, the interface can show it assembling.

> Streaming actual UI components rather than text — each competency card builds live with its own state. Early users consistently called out the live-building UI as "magical" compared to competitors that just show loading spinners.

The alternative path — stream text, then hydrate into components — flashes unstyled content and breaks mid-stream. **Structure the output as the interface from the start** rather than as text you convert later.

### Match the input to how people think

Form fields impose the data model's shape on the person filling them. Sometimes that is correct — it is correct whenever the person already thinks in those fields. Often it is not.

> Hiring managers think in problems and constraints, not form fields. The form made them pre-structure their thinking and produced worse output.

The tell is measurable: if the freeform path produces *richer* results than the structured one, the form was doing damage, not scaffolding.

### Design the seam before either side

In any product with two roles, the interface people actually experience is the handoff — not either screen.

> Nothing in logistics is done by one role alone: a status a driver sets is only worth setting if it lands usefully on a dispatcher's screen, and a request a dispatcher sends is only worth sending if it is answerable from a truck.

Building two separately-optimized apps produces two internally consistent products with a seam between them. **Design the shared object first** — the shipment, the document, the case — then design each role's view onto it.

### The conditions are part of the interface

An interface designed at a desk is designed for a desk. Field conditions are not edge cases; they are the operating environment.

> Noise, bad lighting, one-handed use, patchy connectivity, and genuine time pressure. Those constraints shaped the interface more than anything from the seated sessions.

Every one of those has a direct interface consequence: contrast and target size, offline behavior and optimistic state, how much a person can accomplish in one thumb-reachable gesture. Get them from observation, not imagination.

### Calm is a property you can measure

For a product used under stress, cognitive load is the design problem — not the feature set.

> Applied cognitive load theory to stress-reducing interface patterns: **4.8/5 usability in high-pressure prototype testing**, and a 43% reduction in decision fatigue against feature-heavy comparisons.

*(Prototype-stage validation, not shipped results — see `write-case-study` for why that distinction has to survive into the write-up.)*

The counterintuitive part: patterns that *lowered* cognitive load tested better than added functionality. Sometimes the best interface decision is to give people less to choose from, not more.

### Accessibility constrains architecture upward

Treating accessibility as a compliance floor produces components that pass an audit and stay awkward. Treating it as an architectural constraint produces better components for everyone — building for users with disabilities forces clearer state, better focus handling, and more honest semantics.

Conformance is not usability. Passing WCAG AA tells you nothing about whether the thing is good.

## Review Format (Required)

When reviewing an interface, output a table. One row per change. No exceptions.

| Before | After | Why |
| --- | --- | --- |
| Single asserted match | Top 3 ranked, user confirms | Confirmation builds trust and creates a downstream signal |
| Empty state illustration | Widen radius, label the tradeoff | Degrade scope before showing nothing |
| Spinner during generation | Stream components as they build | Shows the work, not that work is happening |
| 14 props on one component | 4 props + composition slot | 80% of use needs 20% of surface |
| Beginner / Expert toggle | One surface, disclose on competence | No self-classification before first use |

Do **not** write prose paragraphs describing what could be improved. Do **not** write "consider adding…" or "it might be worth…". Every row names a concrete current state, a concrete replacement, and the principle it serves.

If the interface is genuinely fine, say so in one line and stop. A table padded with marginal rows is worse than no table.

## When to Break These

- **Two modes are right** when the audiences are legally or operationally distinct — a clinician view and a patient view are not a disclosure problem.
- **A single confident answer is right** when the cost of a wrong assertion is trivial and the friction of confirmation is not (autocomplete, spell-check).
- **A spinner is right** when the output has no structure to reveal, or arrives fast enough that a build-up animation is theater.
- **Configuration beats composition** when the consumers are not developers, or when the composition API would require understanding internals to use safely.

Naming the condition under which a principle inverts is what separates a principle from a preference.

## Review Checklist

| Check | Fail condition |
| --- | --- |
| Confidence | System asserts one answer where it holds a ranked set |
| Confirmation | User has no cheap way to correct an assertion |
| Disclosure | Surface split into modes before anyone has used it |
| Disclosure cost | Progressive disclosure shipped without acknowledging what got buried |
| Empty states | Blank screen shipped where a constraint could have relaxed |
| Degradation cost | Scope widened silently, with no label for reduced relevance |
| Loading | Spinner covering structured output that could stream |
| Streaming | Text streamed then hydrated, flashing unstyled content |
| API surface | Component takes props nobody uses; no escape hatch for the ones who need it |
| API refusal | No stated position on what the component won't do |
| Input shape | Form imposes the data model on someone who doesn't think in it |
| Multi-role | Two role views designed before the object they share |
| Handoff | State one role sets doesn't land usefully on the other's screen |
| Conditions | Designed seated, shipped to a truck cab, warehouse, or street |
| Offline | No optimistic state or recovery on patchy connectivity |
| Cognitive load | Functionality added to a surface used under stress |
| Accessibility | Treated as an audit to pass rather than an architectural constraint |
| Focus | Keyboard path undefined or invisible |
| Claim discipline | Prototype-stage usability numbers reported as shipped results |
