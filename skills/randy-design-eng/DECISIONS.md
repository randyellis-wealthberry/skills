# Worked Decisions

Reference examples for the four-part decision framework in [SKILL.md](SKILL.md). Every entry is a real decision from a real engagement, including the ones whose predicted cost landed.

Read these when you need to see the shape of a finished decision before writing one. The pattern to copy is not the subject matter — it is that each entry names the alternative at its strongest, names what the choice cost, and reports the outcome including the part that cut against it.

---

## Social gardening platform
**Role:** Lead Product Designer, one of eight. Design end to end: feature vision, evaluative research, flows, interaction design, hi-fi prototyping.
**Not mine to decide:** the client and PM set the three-phase sequencing; the horticultural content partnership was already in place.

### One interface for novices and experts, not two

**Decision.** A single interface with progressive disclosure — advanced controls surfacing as users demonstrated competence — instead of splitting the app into beginner and expert modes.

**Alternative, at its strongest.** Two distinct modes is the cleaner UX answer. Each mode gets tuned to its audience with no compromise between them.

**Cost.** It doubles design and build surface, and it forces a self-identification choice on first run that novices routinely get wrong. Progressive disclosure kept one path through the product at the cost of burying expert features behind demonstrated behavior — experienced gardeners had to earn their way to depth they already knew they wanted.

**Outcome.** It cut both ways, as designed. Novices stopped bouncing off the first run; experienced gardeners said plainly that features they knew existed were buried. Same call again, but the complaint was real and there was no good answer for it.

### Ranked candidates over a single confident answer

**Decision.** Plant recognition showed top candidates and required the user to confirm one, rather than presenting a single identification as fact.

**Alternative, at its strongest.** A single auto-answer is the better demo and the better first-run moment.

**Cost.** One extra tap on every identification, and a less magical first impression. But a wrong identification in a plant-care app does not just embarrass the product — it sends someone down an incorrect watering and light schedule for a living thing.

**Outcome.** The confirmation step built trust rather than merely preventing error. People believed an identification more once they had chosen it themselves than when the app simply asserted one. It also made community verification mean something downstream.

### A rating mechanic designed for volume, not depth

**Decision.** Photo rating stayed a single low-effort tap — no writing, almost no thought.

**Alternative, at its strongest.** A richer review (stars, tags, commentary) produces far better data per interaction.

**Cost.** Shallower signal per interaction, accepted deliberately to get contribution from the majority of users who would never write a review at all.

**Outcome.** 3.4M photo ratings against 350K uploads — roughly ten ratings per photo contributed. The ratio is the mechanic working as intended, not an accident of traffic.

### Widening the radius instead of shipping an empty feed

**Decision.** Location-scoped discovery expanded its radius automatically when local density was too low to fill a feed.

**Alternative, at its strongest.** Strict location scoping keeps every piece of content climate-relevant, which is the entire point in gardening.

**Cost.** Relevance degrades as the radius stretches. Strict scoping punishes exactly the users who need the app most — the ones with no gardening community nearby — so scope was allowed to degrade gracefully instead.

**Outcome.** Users in sparse regions got a populated feed instead of a blank screen, and it cost exactly what was expected: the people getting the most content were getting the least applicable content.

### Treating winter as planning season, not dead season

**Decision.** Designed off-season content — planning, indoor plants — rather than absorbing the seasonal engagement trough.

**Alternative, at its strongest.** A gardening app is seasonal; accept the winter drop and re-acquire in spring.

**Cost.** Content work in the months with the least obvious payoff.

**Outcome.** The winter drop-off got shallower than pure seasonality predicts. It did not eliminate the trough, but the app stopped going quiet for a full quarter.

**Results.** 240,000+ active users across 25,000+ cities. 3.4M photo ratings, 350K uploads — the largest user-generated gardening database in the U.S. Expert-validated content for 15,000+ plant varieties at 94% identification accuracy. *The number that mattered:* 87% of novices reported better gardening outcomes, because reaching novices was the actual point.

---

## Sports video editing for student athletes
**Role:** UX Researcher & Designer, one of six. Owned user research and the design that came out of it.
**Claim boundary:** the app shipped, but post-launch store rating, retention and total reels created came from the product's life after this engagement. They are not results of this work and are not claimed here.

### Testing both editing models instead of arguing about them

**Decision.** Built and tested both editing models with real students rather than settling the question in a design review.

**Alternative, at its strongest.** Pick one on judgment and spend the time building it properly.

**Cost.** Prototype effort spent on a model that was going to be thrown away.

**Outcome.** The sessions settled a design argument that opinion would have run indefinitely. Students chose speed and simplicity every time they were offered control instead.

### Testing in schools instead of a lab

**Decision.** Ran testing with 15 high school students on iOS and Android in libraries and hallways — the places they actually use their phones.

**Alternative, at its strongest.** A seated lab session is cleaner, better instrumented, easier to schedule and easier to compare across participants.

**Cost.** Noisier data, harder logistics, less control.

**Outcome.** The real setting surfaced problems the lab version never would have: noise, bad lighting, one-handed use, patchy connectivity, and genuine time pressure between periods. Those constraints shaped the interface more than anything from the seated sessions.

**Results (validation only).** 93% of students successfully created a highlight reel during testing. Editing time down 67% against existing solutions. 87% said they would recommend it to teammates.

---

## AI payroll fraud detection
**Role:** AI Product Lead & Technical Architect.

### Fixing false positives with context, not thresholds

**Decision.** Taught the system payroll context — one-time payments, seasonal patterns, role-specific variation — rather than raising the anomaly threshold.

**Alternative, at its strongest.** Moving the threshold is a one-line change that immediately stops the complaints.

**Cost.** Substantially more feature engineering, and a longer period of visible false positives while the context work landed.

**Outcome.** Detection reached 92% on known anomalies with 90%+ precision. Threshold-tuning would have hidden the same errors and taught the system nothing.

### Limiting what the system was allowed to see

**Decision.** Scoped the model's data access to the minimum the detection task required.

**Alternative, at its strongest.** More data is more signal; broader access would likely have improved raw accuracy.

**Cost.** Some detection ceiling, traded for a smaller blast radius and a system employees could be told the shape of.

**Outcome.** The result worth leading with was not the money. Employee payroll satisfaction rose 15% and payroll-related HR inquiries dropped sharply — the system was built to protect people's trust, not only the company's money.

**Results.** Errors down 78%. Audit time from 10 hours to 3–4 per cycle (65% saving). $180,000 saved in year one, ROI inside 6 months, $50,000 in prevented fraud losses, no compliance penalties post-implementation.

---

## AI career intelligence platform
**Role:** Product Design Director, two-week case-study sprint for Alight, three-person team.
**Claim boundary:** everything here is prototype-stage. The engagement ended at validation, not at a shipped product.

### Cut tracking depth to protect the network feature

**Decision.** Thinned out application-tracking depth to keep the referral-network feature within a ten-working-day scope.

**Alternative, at its strongest.** Tracking is the feature users arrive expecting, and the one incumbents are judged on.

**Cost.** The weakest part of the prototype in testing was, predictably, the thinned-out tracking.

**Outcome.** Exactly the tradeoff chosen going in. The referral-discovery concept — the actual bet — held up with real job seekers.

### Consent and transparency over the magic moment

**Decision.** When the prototype surfaced a referral path through second- and third-degree connections, it showed how that connection was found and gave the user control over it.

**Alternative, at its strongest.** Presenting the result as if by magic is a dramatically better demo moment.

**Cost.** A less impressive reveal, and extra interface surface explaining the derivation.

**Outcome.** The consent-first framing did not scare people off, which was the open question.

**Results (validation only).** 94% prototype approval, 91.7% task completion, 4.8/5 mobile usability, 89.2% feature discovery. n=127 unmoderated (Maze) plus n=15 moderated.

---

## Trucking and logistics platform
**Role:** UX Researcher & Product Designer, with Echo Global Logistics and Eight Bit Studios.
**Claim boundary:** the client's commercial results are theirs to disclose. What is claimed here is the design work.

### Designing the handoff, not two separate apps

**Decision.** Designed the driver/dispatch handoff first, then designed each side against that shared shipment state.

**Alternative, at its strongest.** Build each app well for its own user, then integrate — the normal, parallelizable way to run two platforms.

**Cost.** Slower start; neither app could be designed independently.

**Outcome.** Drivers and dispatch got a shared view of a shipment for the first time. Integrating two separately-optimized apps would have produced two internally consistent products with a seam between them.

### Going to the drivers before designing for them

**Decision.** On-site interviews with drivers and dispatch officers before design started.

**Alternative, at its strongest.** Domain expertise plus stakeholder interviews is faster and much easier to schedule.

**Cost.** Weeks of field time in an industry with low technology penetration and no interest in being researched.

**Outcome.** The driver app was built for the conditions drivers actually work in, which is the difference between adoption and a compliance tool nobody opens. The product went alpha → beta → launch and met the ELD Mandate.

---

## Design leadership at scale
**Role:** Head of Design, March–October 2022.
**Scope, stated plainly:** direct authority over 15 designers; influence, not authority, over the wider organization. The 18,000+ figure across 36 countries is the organization, not the team. Nearly every decision below is therefore about persuasion rather than control.

### Aiming past the compliance floor

**Decision.** Wrote the Digital Accessibility Strategy 2023 to target genuinely usable design rather than the WCAG conformance bar.

**Alternative, at its strongest.** Conformance is measurable, defensible, easy to fund, and the only part anyone can audit.

**Cost.** Committing to a goal that cannot be proven with a score, inside an IT consultancy where unmeasurable goals are the first ones cut. It cost the simpler story and a cleaner metric to report against. The compliance floor stayed in as the minimum, never the target.

**Outcome.** Positioned the firm ahead of requirements rather than at them, and opened healthcare and government work that required real inclusive-design capability.

### Evangelism instead of enforcement

**Decision.** Positioned design as a business driver and invested in advocacy, content and mentoring rather than mandating standards through process.

**Alternative, at its strongest.** A policy attached to a delivery gate is measurable, has a completion date, and shows progress cleanly.

**Cost.** Persuasion is slower, has no completion date, and is much harder to report on. But a mandate that cannot be enforced across teams that do not report to you produces compliance theatre and quiet resentment.

**Outcome.** Adoption up threefold. Junior designer retention up 40% through the mentor-coaching program. Content strategy reached 10K+ subscribers and generated 100+ qualified leads — which is what made the design function legible to the business.

---

## Design system
**Role:** Lead design-system architect, team of four. Ongoing, not finished. Started as a fork of Chakra UI, not a clean sheet.

### Forking Chakra UI instead of starting from a clean sheet

**Decision.** Built as a fork, inheriting Chakra's component API rather than designing a new one.

**Alternative, at its strongest.** A clean sheet gives total control of the foundation with no inherited mistakes.

**Cost.** Control of the foundation. Chakra's design decisions came wholesale — the good ones and the awkward ones — and the awkward ones are now mine to carry.

**Outcome.** A clean win on speed. Forking produced something real and usable in a fraction of the time, and the familiar API meant early users needed almost no onboarding. Adoption is the hard part of a design system, not construction.

### Opinionated defaults with an escape hatch underneath

**Decision.** Made the common case a single obvious call, with composable primitives underneath for anyone who needed to go further.

**Alternative, at its strongest.** Pick a pole. Fully composable is maximally powerful; fully opinionated is maximally teachable. Either is one API to document.

**Cost.** A two-layer API — twice the surface to document, and a real risk people never discover the lower layer exists.

**Outcome.** **The risk landed.** Developers largely did not find the primitives on their own; they hit the edge of a default and asked rather than dropping down a layer. That is a documentation failure, not an architecture one, and it is mine to fix.

**Method note.** The API surface was cut from usage data, not taste: instrumenting Chakra showed 80% of developers used only 20% of component props.

---

## AI interview scorecard generator
**Role:** Whole product lifecycle — research, strategy, UX, full-stack build, go-to-market. Live production SaaS.

### Generative UI over plain text streaming

**Decision.** Stream scorecards as interactive React components rather than plain text.

**Alternative, at its strongest.** Stream text, parse, hydrate the DOM — vastly cheaper in tokens and the standard approach.

**Cost.** More tokens per generation, and a harder streaming architecture.

**Outcome.** Scorecards feel like a product rather than a chatbot. The text-then-hydrate path would have flashed unstyled content and broken mid-stream.

### Claude over GPT-4 for scorecard generation

**Decision.** Anthropic Claude as the primary model.

**Alternative, at its strongest.** GPT-4 generated faster and cost ~15% less per scorecard.

**Cost.** ~15% higher token cost per scorecard.

**Outcome.** Tested both across 20 job descriptions with identical prompts: GPT-4 needed 3 rounds of refinement to avoid biased language; Claude hit the bias-reducing standard on the first pass 90% of the time. Zero customer complaints about biased questions after 3 months in production. The token delta is negligible against one lawsuit-inducing question.

### Chat interface over form-based input

**Decision.** Conversational input rather than a structured form.

**Alternative, at its strongest.** A form produces cleaner structured input, is far easier to validate, and reads as more professional.

**Cost.** Less "professional" surface, and no guaranteed input structure.

**Outcome.** Hiring managers think in problems and constraints, not form fields; the form made them pre-structure their thinking and produced worse scorecards. Recruiters preferred chat 11:1 (n=12). Chat-generated scorecards average 6.2 competencies vs 4.1 from the form flow, and sessions complete 40% faster.

### Multi-tenant from day one instead of single-user MVP

**Decision.** Shipped organization and team features in v1.

**Alternative, at its strongest.** Single-user ships three weeks sooner and is the textbook MVP.

**Cost.** Three weeks of launch timeline, and genuine over-engineering risk.

**Outcome.** Every customer interview described the same workflow: build it, then share it with the hiring panel. First paid customer was a 12-person recruiting team, not an individual. No retrofit of sharing features post-launch.

**Reflection.** The hard part of an AI product is not the LLM integration, it is the wrapper that makes it useful in a real workflow — PDF export, team sharing, the template library. And hiring managers did not want control over the AI: v1 let users edit the system prompt and nobody used it. Removing that and hardening the bias-reducing prompts increased conversions 23%. Sometimes the best UX decision is to give users less choice, not more.
