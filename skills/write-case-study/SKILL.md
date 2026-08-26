---
name: write-case-study
description: Write or audit a portfolio case study with strict claim discipline — separating what you decided from what was handed to you, and what you validated from what shipped after you left. Use when writing up a project, drafting portfolio or resume copy, preparing an interview walkthrough, or checking whether a claim is actually supported by the work. For hardening a single decision use defend-decision.
---

# Writing a Case Study

A construction skill. It does ONE thing: turn a project into a written case study whose every claim is supported by work you actually did. It does not harden individual decisions (that's `defend-decision`) or teach the philosophy behind the standards (that's `randy-design-eng`).

The bar: **a skeptical reader who knows the project cannot point at a single sentence and say "that wasn't yours."**

## Why Claim Discipline Wins Work

The instinct is that hedging makes work look smaller. The opposite happens. A case study that states its own limits reads as written by someone who knows the difference between validation and adoption — and every unhedged number in it becomes believable.

The reader is not comparing you to a perfect candidate. They are comparing you to five other case studies that all claim total credit for everything, and yours is the only one they can calibrate.

## Structure

Constraints before decisions, so decisions are read inside the box they were made in.

### 1. Role narrative

Open with your actual scope. Three things, in this order:

1. **Your role and team size.** "Lead product designer, one of eight." "Product design director on a three-person team over ten working days."
2. **What was in your lane.** Concretely: research, flows, interaction design, prototyping, the API surface, the go-to-market.
3. **What was not yours to decide.** Sequencing set by the client. A partnership already in place. A stack you inherited. A timeline handed down.

That third item is the one people skip, and it is the one that makes the rest credible.

> "Two things that shape this case study were not mine to decide: the client and PM set the three-phase sequencing, and the horticultural content partnership was already in place when I arrived. What follows are the calls I actually made, inside those constraints."

When the title oversells the scope, correct it in the same paragraph:

> "The scale number that gets quoted — 18,000+ people across 36 countries — is the organization, not my team. I had direct authority over 15 designers and influence over everyone else, which is the honest shape of design leadership at this size."

### 2. Background

The problem, with the market or operational facts that made it worth solving. Specific numbers, not adjectives. "10 hours of manual audit per pay cycle" beats "a slow, painful process."

### 3. Decisions

Two to five entries. Use the format from `defend-decision`:

```markdown
### <X over Y>
**Decision.** <action>
**Alternative, at its strongest.** <what it's genuinely better at>
**Cost.** <the price paid>
**Outcome.** <what happened, including what cut against you>
```

Fewer, well-defended decisions beat a long list of shallow ones. If you cannot name a cost for an entry, it is not a decision — move it into the process section as a task.

### 4. Process

Approach and methodology, specific enough to be checked. Method, sample size, duration, setting.

- ✗ "Conducted extensive user research."
- ✓ "n=127 unmoderated in Maze plus n=15 moderated in-person, over ten working days."
- ✓ "15 high school students on iOS and Android, in school libraries and hallways."

If research happened somewhere unusual, say where and why — the setting is often the finding.

### 5. Outcome

Sort every result into one of three buckets and never blend them:

| Bucket | Claim as | Example |
| --- | --- | --- |
| **Validation** | A tested result, labeled as one | "94% prototype approval; the engagement ended at validation" |
| **Shipped, mine** | Yours | "Errors dropped 78% over six months" |
| **Shipped, after me** | The product's, or omit | "The post-launch numbers came after my engagement and are not mine to claim" |

**Lead with the metric that maps to the intent, not the biggest one.** Put the large number second.

> "The platform reached over 240,000 active users... The number I care about most is that 87% of novices reported better gardening outcomes, because that was the actual point."

If the client's commercial results are confidential, say so and describe the design work instead. That sentence costs nothing and buys the reader's trust in everything around it.

### 6. Reflection

What you would do again, and what you still do not have a good answer for. One honest open problem is worth more than three lessons learned.

## Voice

- **First person singular** for what you did. **First person plural** for what the team did. Never blur them to inflate scope.
- Plain sentences. Cut "leveraged", "seamlessly", "revolutionized", "utilized", "spearheaded", "passionate about".
- Prefer the concrete noun: "3.4M photo ratings against 350K uploads" over "significant engagement."
- Write it so it would survive being read aloud to the engineer who built it.

## Auditing an Existing Case Study

Output a markdown table. One row per issue.

| Before | After | Why |
| --- | --- | --- |
| "Impacted 18,000+ employees" | "Directly led 15 designers in an 18,000-person organization" | Organization size is not team size |
| "The app now has 15,000 weekly actives" | "Testing established the workflow; post-launch numbers came after my engagement" | Post-engagement results are the product's |
| "Achieved 94% approval and drove adoption" | "94% prototype approval; the engagement ended at validation" | Prototype numbers are not product numbers |
| "Increased client revenue by 30%" | "<describe the design work>" | Client commercial results are theirs to disclose |
| "Led the redesign" | "Led the redesign; the three-phase sequencing was set by the client" | Constraints you were handed belong in the role narrative |
| "Conducted extensive user research" | "n=15 moderated sessions in school libraries and hallways" | Unfalsifiable — give method, size, setting |
| "The project was a complete success" | "<result>, and <the cost that landed>" | An outcome with no cost has been cleaned |
| "Leveraged design thinking to seamlessly..." | "<plain verbs>" | Filler |

## Checklist

- [ ] Role narrative states team size and what was *not* yours to decide
- [ ] Every decision names an alternative and a cost
- [ ] Every number is labeled: validation, shipped-mine, or shipped-after-me
- [ ] The lead metric maps to the project's intent, not to size
- [ ] Research claims carry method, sample size and setting
- [ ] Confidential client results are declined explicitly, not implied
- [ ] At least one sentence reports something that cut against you
- [ ] Singular and plural first person are used accurately throughout
