You are validating whether a startup problem is real and worth building for Shab specifically.

The problem to validate is provided as an argument (ideally from `/find-ideas` output), or if none given, ask the user to state it using Who/What/When.

## Step 1 — Load context + confirm the problem statement

Read `/Users/Personal/SaaS-Ideas/shab-capabilities.md` — you will use this in Step 4 to check fit.

Restate the problem clearly in this format before proceeding:
- **Who:** the specific person feeling the pain
- **What:** the exact friction or failure they experience
- **When:** the trigger or context it happens in

If the argument is vague, sharpen it before searching. Do not proceed with a fuzzy problem statement.

## Step 2 — Search for people talking about it

Run these searches in parallel using WebSearch:

1. `site:reddit.com "[problem keywords]"` — look for complaints, questions, rants, workarounds
2. `site:reddit.com "[problem keywords]" solution OR tool OR software` — look for people seeking or recommending fixes
3. `"[problem keywords]" site:x.com OR site:twitter.com` — look for public complaints or threads
4. `"[problem keywords]" site:g2.com OR site:capterra.com` — look for reviews mentioning the pain in existing tools
5. `"[problem keywords]" site:news.ycombinator.com` — look for HN discussions
6. `"[problem keywords]" forum OR community OR group` — find niche communities where this surfaces

For each search, fetch the top 2–3 results and extract:
- Direct quotes from real people describing the pain
- How frequently the complaint appears
- Any workarounds or hacks people use today (strong validation signal)
- Emotional intensity — is it a mild annoyance or a blocker?

## Step 3 — Check if people already pay to solve it

Run these searches in parallel:

1. `"[problem keywords]" pricing OR "per month" OR "per user" OR subscription` — find paid tools in this space
2. `site:producthunt.com "[problem keywords]"` — find launched products and their upvotes/comments
3. `site:g2.com "[problem keywords]" reviews` — find paid software with real user reviews
4. `"[problem keywords]" alternatives OR "vs " OR competitor` — find comparison pages (signals an active market)
5. `"[problem keywords]" "how much" OR "cost" OR "pricing"` — find people asking about or discussing cost

Fetch results and extract:
- Names of existing paid products solving this (or adjacent to it)
- Price points if visible
- Number of reviews / users (signals market size)
- Gaps or complaints IN those existing solutions (your wedge)

## Step 4 — Score and output

Present a structured validation report:

---

### Problem
[Restated: Who / What / When]

### Signal: Are people talking about it?

| Source | Evidence | Intensity |
|---|---|---|
| Reddit | [quote or summary] | Low / Medium / High |
| X/Twitter | [quote or summary] | Low / Medium / High |
| G2/Capterra | [quote or summary] | Low / Medium / High |
| HN | [quote or summary] | Low / Medium / High |

**Workarounds found:** [List any DIY hacks people use — each one is a validation signal]

### Signal: Are people already paying?

| Product | Price | Users/Reviews | Gap in their solution |
|---|---|---|---|
| [name] | [price] | [count] | [what they complain about] |

### Verdict

One of:
- **VALIDATED** — real pain, people are paying, there's a gap to exploit
- **SIGNAL BUT NO MONEY** — real pain, no one paying yet (early market or wrong audience)
- **WEAK SIGNAL** — few people talking, no payment evidence (de-prioritise)
- **SATURATED** — real pain, but existing solutions are strong and well-distributed (hard to enter)

### Shab Fit Check

Using `shab-capabilities.md`, flag any mismatches:
- Does solving this require elite narrow technical depth? (red flag)
- Is the moat operational grind or high-touch fulfilment? (red flag)
- Is the hard part enterprise sales or large-org behaviour change? (red flag)
- Does it play to his strengths — bridging tech/business, 0-to-1 product thinking, AI/SaaS? (green)

One line: **Good fit / Weak fit / Hard pass** + reason

### Recommended next step

One concrete action based on verdict + fit (e.g. "DM 5 Reddit users who complained about X and ask if they'd pay $Y/month for Z")
