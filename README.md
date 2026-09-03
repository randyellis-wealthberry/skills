# Skills for Product Design Decisions

Agent skills for people who have to defend their design work.

For twenty years a design portfolio worked as proof by being expensive — producing a polished case study cost real hours, so the artifact itself was evidence. That cost is now zero. Anyone can generate six clean sections and a metrics band in an afternoon, and no reader can tell the difference by looking.

So evaluation moved to the only question that still carries information: **walk me through why you didn't just do the simpler thing.**

These skills exist to make an agent useful for answering that. Agents are good at producing design rationale that sounds right. They are much worse at producing rationale that is *true* — that names the option you passed on, admits what your choice cost, and reports the result that cut against you. Left alone, an agent will write you a case study where every decision was correct, every number is yours, and nothing was traded away.

That is the gap these skills close. They encode a working method built across social platforms, logistics, fintech, AI products, a design system, and design leadership at enterprise scale: **a decision you can't defend isn't a decision, it's a preference — and a claim you can't support isn't a result, it's a story.**

Based on [work.randyellis.design](https://work.randyellis.design).

## Install

```bash
npx skills@latest add randyellis-wealthberry/skills
```

Or copy any `skills/<name>/` directory into your project's `.claude/skills/`.

## Skills

- **[randy-ellis](./skills/randy-ellis/SKILL.md)** — The whole method as one file. The six rules, the decision framework, evidence standards, interface assertion, AI product surfaces, design systems, leading without authority, and the review format, consolidated from the four skills below. Served canonically at [work.randyellis.design/skill.md](https://work.randyellis.design/skill.md); the paid modules and the engagement are at [work.randyellis.design/skill](https://work.randyellis.design/skill).
- **[randy-design-eng](./skills/randy-design-eng/SKILL.md)** — The main skill. Decision defensibility, evidence standards, claim discipline, AI product surfaces, design-system API design, and leading design without authority. Worked examples from real projects live in [DECISIONS.md](./skills/randy-design-eng/DECISIONS.md).
- **[ui-craft](./skills/ui-craft/SKILL.md)** — The interface lens. How much a surface should assert: progressive disclosure over modes, ranked candidates over single confident answers, graceful scope degradation over empty states, composition over configuration, and designing the seam between two roles.
- **[defend-decision](./skills/defend-decision/SKILL.md)** — Take a design decision and harden it until it survives interrogation: the alternative at its strongest, the price you actually paid, and the outcome you would rather delete.
- **[write-case-study](./skills/write-case-study/SKILL.md)** — Write or audit a case study with strict claim discipline. Separates what you decided from what was handed to you, and what you validated from what shipped after you left.

## What they enforce

**Every decision names its alternative and its cost.** Not "I chose X because it's better" — "I chose X; Y was genuinely better at Z; here's what X cost me."

**Claim only what you did.** Post-engagement growth is the product's, not yours. Organization size is not team size. Prototype approval is not adoption. Client revenue is theirs to disclose.

**Report the outcome that cut against you.** Every real decision has a cost. An outcome section with no downside in it is either a decision that was never real or a report that has been cleaned.

**Adoption is the hard part, not construction.** A familiar API beats a better one. A fork beats a clean sheet when the foundation is adequate. Persuasion beats a mandate you can't enforce.

**Trust is a design material.** In any product that asserts something to a user, the interface either builds trust or spends it. Confidence you haven't earned is the fastest way to spend it.

**The number you care about most is rarely the biggest one.** Lead with the metric that maps to the intent. Put the large number second.

## What that looks like in practice

The skills and worked examples are held to the standard they enforce, which means several of them argue against their own author:

> It cut both ways, as designed. Novices stopped bouncing off the first run; experienced gardeners said plainly that features they knew existed were buried. Same call again, but the complaint was real and there was no good answer for it.

> **The risk landed.** Developers largely did not find the primitives on their own; they hit the edge of a default and asked rather than dropping down a layer. That is a documentation failure, not an architecture one, and it is mine to fix.

> The scale number that gets quoted — 18,000+ people across 36 countries — is the organization, not my team. I had direct authority over 15 designers and influence over everyone else, which is the honest shape of design leadership at this size.

> The client's commercial results are theirs to disclose. What is claimed here is the design work.

An agent running these skills will hold your work to that standard, including when the honest version is smaller than the one you wanted to write.

## Why this exists

The skills are a side-effect of domain expertise, not a replacement for it. They encode judgment developed by making these calls and living with what they cost — which is why the examples throughout are real projects with real tradeoffs, including the ones where the predicted cost landed.

The engagements are described by what they were rather than by name — a social gardening platform, a payroll fraud-detection system, a design system — so the skills read as method rather than as a client list. The decisions, the costs and the outcomes that cut against the author are unchanged; only the labels are off. Named versions of several of them are public case studies at [work.randyellis.design](https://work.randyellis.design).

Use them to get to a defensible decision faster. Then go develop the expertise yourself; it is the part that compounds.

## Prior art

The structure of this collection is modeled on [emilkowalski/skills](https://github.com/emilkowalski/skills). Same premise — agents don't have taste, so give them yours — aimed at a different layer.

The two are complements, not alternatives. His lens is how an interface *feels to move*: springs, interruptibility, velocity handoff, gesture. The lens here is how much an interface should *assert*: what it shows, how certain it looks, what it refuses to do. If you want the motion half, install his directly — it is not reproduced here, and none of the content in this repo is derived from it.

## License

MIT
