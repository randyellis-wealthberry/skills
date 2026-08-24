# Skills for Product Design Decisions

Agent skills for people who have to defend their design work.

Agents are good at producing design rationale that sounds right. They are much worse at producing rationale that is *true* — that names the option you passed on, admits what your choice cost, and reports the result that cut against you. Left alone, an agent will write you a case study where every decision was correct, every number is yours, and nothing was traded away.

That is the gap these skills close. They encode a working method built across social platforms, logistics, fintech, AI products, a design system, and design leadership at enterprise scale: **a decision you can't defend isn't a decision, it's a preference — and a claim you can't support isn't a result, it's a story.**

Based on [work.randyellis.design](https://work.randyellis.design).

## Install

```bash
npx skills@latest add randyellis-wealthberry/skills
```

Or copy any `skills/<name>/` directory into your project's `.claude/skills/`.

## Skills

- **[randy-design-eng](./skills/randy-design-eng/SKILL.md)** — The main skill. Decision defensibility, evidence standards, claim discipline, AI product surfaces, design-system API design, and leading design without authority. Worked examples from real projects live in [DECISIONS.md](./skills/randy-design-eng/DECISIONS.md).
- **[defend-decision](./skills/defend-decision/SKILL.md)** — Take a design decision and harden it until it survives interrogation: the alternative at its strongest, the price you actually paid, and the outcome you would rather delete.
- **[write-case-study](./skills/write-case-study/SKILL.md)** — Write or audit a case study with strict claim discipline. Separates what you decided from what was handed to you, and what you validated from what shipped after you left.

## What they enforce

**Every decision names its alternative and its cost.** Not "I chose X because it's better" — "I chose X; Y was genuinely better at Z; here's what X cost me."

**Claim only what you did.** Post-engagement growth is the product's, not yours. Organization size is not team size. Prototype approval is not adoption. Client revenue is theirs to disclose.

**Report the outcome that cut against you.** Every real decision has a cost. An outcome section with no downside in it is either a decision that was never real or a report that has been cleaned.

**Adoption is the hard part, not construction.** A familiar API beats a better one. A fork beats a clean sheet when the foundation is adequate. Persuasion beats a mandate you can't enforce.

**Trust is a design material.** In any product that asserts something to a user, the interface either builds trust or spends it. Confidence you haven't earned is the fastest way to spend it.

**The number you care about most is rarely the biggest one.** Lead with the metric that maps to the intent. Put the large number second.

## Why this exists

The skills are a side-effect of domain expertise, not a replacement for it. They encode judgment developed by making these calls and living with what they cost — which is why the examples throughout are real projects with real tradeoffs, including the ones where the predicted cost landed.

Use them to get to a defensible decision faster. Then go develop the expertise yourself; it is the part that compounds.

## Prior art

The structure of this collection is modeled on [emilkowalski/skills](https://github.com/emilkowalski/skills), which does the same thing for animation and UI craft. Different domain, same premise: agents don't have taste, so give them yours.

## License

MIT
