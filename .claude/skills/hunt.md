You are running a full idea hunt for Shab — finding problems from sources, validating each one, and saving results to the ideas folder. This combines /find-ideas and /validator into one pipeline.

## Step 1 — Load context

Read these files in parallel:
- `/Users/Personal/SaaS-Ideas/sources.md` — free source URLs
- `/Users/Personal/SaaS-Ideas/shab-capabilities.md` — capability filter

## Step 2 — Fetch all free sources

Fetch ALL of the following in parallel and extract problem statements, pain points, and opportunity themes:

- https://razorpay.com/m/fix-my-itch
- https://www.ycombinator.com/rfs
- https://www.indiehackers.com/ideas
- https://www.findstartupideas.com
- https://needgap.com
- https://www.opinionx.co/99-problems

Fetch prompt for each: "Extract all problem statements, pain points, unmet needs, and startup opportunity themes visible on this page. Include any scores, votes, or signals of demand if present."

## Step 3 — Filter against Shab's profile

Keep only problems that pass ALL of:

**KEEP if:**
- Requires bridging tech and business (translation gap, not pure engineering)
- 0-to-1 opportunity — no obvious solution exists yet
- Can be validated with a landing page, conversation, or lightweight prototype
- Fits AI, SaaS, or automation applied to a real recurring pain
- India-relevant OR globally applicable with India as a wedge

**DISCARD if:**
- Requires elite technical depth (ML research, niche infrastructure, compiler work)
- Moat is pure operational grind (logistics, high-touch support, manual fulfilment)
- Hard part is enterprise sales or large-org behaviour change
- Already has 3+ well-funded competitors with strong distribution

Target 5–8 ideas to carry forward. Do not pad.

## Step 4 — Validate each idea

For each idea that passes the filter, run validation in parallel where possible.

**Pain signal searches** (run in parallel per idea):
1. `site:reddit.com "[problem keywords]"` — complaints, rants, workarounds
2. `site:reddit.com "[problem keywords]" solution OR tool OR software`
3. `"[problem keywords]" site:x.com OR site:twitter.com`
4. `"[problem keywords]" site:g2.com OR site:capterra.com`
5. `"[problem keywords]" site:news.ycombinator.com`

**Buying signal searches** (run in parallel per idea):
1. `"[problem keywords]" pricing OR "per month" OR subscription`
2. `site:producthunt.com "[problem keywords]"`
3. `"[problem keywords]" alternatives OR competitor`
4. `site:g2.com "[problem keywords]" reviews`

For each search fetch the top 2 results and extract quotes, product names, prices, and review counts.

## Step 5 — Write one MD file per idea

For each validated idea, write a file to `/Users/Personal/SaaS-Ideas/ideas/`.

Filename: slugified problem title, e.g. `gst-reconciliation-for-indian-smes.md`

Use this exact template for every file:

---

```markdown
# [Problem Title]

**Date:** [today's date]
**Source:** [site name + URL where the problem was found]
**Status:** Needs validation / Signal but no money / Validated / Saturated

---

## Problem Statement

- **Who:** [specific person feeling the pain]
- **What:** [exact friction or failure they experience]
- **When:** [trigger or context it happens in]

---

## Pain Signal

| Source | Quote or Evidence | Intensity |
|---|---|---|
| Reddit | [quote or summary + link] | Low / Medium / High |
| X/Twitter | [quote or summary + link] | Low / Medium / High |
| G2/Capterra | [quote or summary + link] | Low / Medium / High |
| HN | [quote or summary + link] | Low / Medium / High |

**Workarounds people use today:**
- [workaround 1]
- [workaround 2]

---

## Buying Signal

| Product | Price | Reviews/Users | Gap |
|---|---|---|---|
| [name + URL] | [price] | [count] | [what users complain about] |

---

## Shab Fit

**Verdict:** Good fit / Weak fit / Hard pass

- [One line on why it fits or doesn't, referencing his strengths/constraints]

---

## Recommended Next Step

[One concrete action — e.g. "Post in r/IndiaStartups with a poll asking if X is a weekly problem for founders"]
```

---

After writing all files, print a summary:

```
## Hunt complete

| Idea | File | Status | Shab Fit |
|---|---|---|---|
| [title] | ideas/[filename].md | [status] | [fit] |
```
