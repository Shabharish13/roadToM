You are running a deep competitive analysis for Shab on a specific idea or market. The goal is not just to list competitors — it is to identify **where the market is weak**, what the real entry wedge is, and whether this is worth building given who's already there.

The idea to analyse is provided as an argument. If a corresponding file exists in `/Users/Personal/SaaS-Ideas/ideas/`, read it first. If no argument is given, ask the user to state the problem in Who/What/When format.

---

## Step 1 — Load context

Read these files in parallel:
- `/Users/Personal/SaaS-Ideas/shab-capabilities.md` — to filter which competitive positions are realistic for Shab
- The relevant idea file in `/Users/Personal/SaaS-Ideas/ideas/` if it exists (e.g. `ideas/freelancer-milestone-payments-india.md`)

Extract: the stated problem, existing competitors already identified, and any Shab Fit notes.

---

## Step 2 — Map the competitive landscape

Run all searches in parallel using WebSearch. For each search, fetch the top 2–3 results.

**Direct competitors** (tools that solve the exact same problem):
1. `"[product category]" India pricing OR subscription 2024 OR 2025`
2. `site:producthunt.com "[product category or problem keywords]"`
3. `site:g2.com "[product category]" reviews`
4. `"[product category]" alternatives`
5. `"[problem keywords]" app OR software OR tool site:reddit.com`

**Adjacent competitors** (tools people use as workarounds or that solve 80% of the problem):
6. `"[problem keywords]" "we use" OR "I use" OR "we switched to" site:reddit.com`
7. `"[problem keywords]" "instead of" OR "alternative to" OR "vs"`
8. `"[problem keywords]" site:news.ycombinator.com`

**India-specific landscape** (if India-relevant):
9. `"[product category]" India startup OR "made for India" OR "India-first"`
10. `"[product category]" India review OR users site:g2.com OR site:capterra.com`

For each competitor found, extract:
- Product name + URL
- Pricing (exact if available, estimated range if not)
- User/review count (signals market validation and incumbent strength)
- Target customer (who they're built for)
- Top complaints or gaps from reviews/threads (your potential wedge)
- Funding status if visible (signals how entrenched they are)

---

## Step 3 — Analyse each competitor

For each significant competitor (direct or adjacent), run one targeted search:

`site:g2.com "[product name]" reviews` OR `site:reddit.com "[product name]" complaints OR problems OR alternatives`

Extract the **top 3 recurring complaints** about each product. These are potential entry wedges.

---

## Step 4 — Identify entry wedges

Based on the competitive map, identify 2–4 potential entry angles. For each:

- **Wedge:** What's the specific gap or underserved segment?
- **Evidence:** What complaints, signals, or gaps support this?
- **Realistic for Shab?** Does it play to his strengths (translation, 0-to-1, India context) or run into his risk zones (enterprise sales, ops grind, elite technical depth)?

Use Shab's constraints from Step 1 to filter out wedges that are theoretically good but practically wrong for him.

---

## Step 5 — Score the competitive threat

Rate the overall competitive threat level:

| Dimension | Score (1–5) | Notes |
|---|---|---|
| Number of direct competitors | | |
| Strength of incumbents (funding + distribution) | | |
| Speed of market movement | | |
| India-specific gap (if relevant) | | |
| Wedge availability for Shab | | |

**Overall threat level:** Low / Medium / High / Critical

Rubric:
- **Low** — 0–1 funded competitors, clear gap, India underserved
- **Medium** — 2–3 competitors but weak on specific wedge; India underserved
- **High** — 3+ competitors, some funded, market moving fast; entry requires precise positioning
- **Critical** — 5+ competitors including well-funded players with strong distribution; not worth entering without a structural moat

---

## Step 6 — Output the report

Write a structured report to the console (do NOT write a file unless the user asks):

---

```
## Competitive Analysis: [Idea Title]
**Date:** [today]
**Analysed by:** /competitive-analysis

---

### Competitive Landscape

| Competitor | Type | Pricing | Users/Reviews | Key Gap |
|---|---|---|---|---|
| [name] | Direct / Adjacent | [price] | [count] | [top complaint] |

---

### Top Recurring Complaints (Entry Wedges)

1. **[Wedge 1]:** [what users hate + product it applies to]
2. **[Wedge 2]:** [what users hate + product it applies to]
3. **[Wedge 3]:** [what users hate + product it applies to]

---

### Entry Wedge Recommendations for Shab

| Wedge | Evidence | Realistic for Shab? |
|---|---|---|
| [wedge] | [signal] | Yes / No / With caveats |

**Best wedge:** [one line — the specific positioning Shab should consider]

---

### Competitive Threat Score

| Dimension | Score (1–5) | Notes |
|---|---|---|
| Number of direct competitors | | |
| Incumbent strength | | |
| Market velocity | | |
| India-specific gap | | |
| Wedge availability for Shab | | |

**Overall:** [Low / Medium / High / Critical]

---

### Recommendation

[2–3 sentences: should Shab proceed given this competitive landscape? If yes, what is the exact positioning? If no, why not?]

### Suggested Next Step

[One concrete action: e.g. "Sign up for [Competitor X]'s free tier and map the 3 flows where India freelancers hit a wall — that's your PRD starting point."]
```

---

After printing the report, ask: "Want me to save this as a file in `ideas/competitive/`?"
