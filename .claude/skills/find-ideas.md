You are helping Shab find startup ideas worth validating today. Follow these steps precisely.

## Step 1 — Load context

Read both files in parallel:
- `/Users/Personal/SaaS-Ideas/sources.md` — to get the free source URLs
- `/Users/Personal/SaaS-Ideas/shab-capabilities.md` — to load the capability filter

## Step 2 — Fetch each free source

Fetch ALL of the following URLs in parallel. For each, extract: problem statements, pain points, unmet needs, or idea themes that appear on the page.

Free sources (from sources.md):
- https://razorpay.com/m/fix-my-itch
- https://www.ycombinator.com/rfs
- https://www.indiehackers.com/ideas
- https://www.findstartupideas.com
- https://needgap.com
- https://www.opinionx.co/99-problems

Fetch prompt for each: "Extract all problem statements, pain points, unmet needs, and startup opportunity themes visible on this page. Include any scores, votes, or signals of demand if present."

## Step 3 — Filter against Shab's profile

Apply this filter to every problem/idea collected. Keep only those that:

**KEEP if:**
- Requires bridging tech and business (translation gap, not pure engineering)
- 0-to-1 opportunity — no obvious solution exists yet
- Can be validated with a landing page, conversation, or lightweight prototype
- Fits AI, SaaS, or automation applied to a real recurring pain
- India-relevant OR globally applicable with India as a wedge

**DISCARD if:**
- Requires elite technical depth (ML research, niche infrastructure, compiler work)
- Moat is pure operational grind (logistics, high-touch support, manual fulfilment)
- Hard part is enterprise sales or large-org behavior change
- Already has 3+ well-funded competitors with strong distribution

## Step 4 — Output

Present results as a clean shortlist. For each idea, use this exact format — the problem statement is structured to feed directly into `/validator`:

```
### [Problem title — 5 words max]
**Source:** [site name]
**Who:** [specific person feeling the pain]
**What:** [exact friction or failure they experience]
**When:** [trigger or context it happens in]
**Why Shab:** One sentence — why this fits his profile

→ `/validator [Who] [What] [When]` — paste this to validate
```

Aim for 5–10 ideas. If a source yields nothing after filtering, note it briefly and move on. Do not pad — quality over quantity.
