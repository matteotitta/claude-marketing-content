---
name: content-audit
description: 'Audits a B2B company''s existing content across blog, newsletter, LinkedIn, YouTube and events to set a baseline
  before planning. Produces a channel inventory, cadence and topic counts, funnel-stage mix, 1-5 scores per dimension, gaps
  and a ranked list of fixes. Triggers: "content audit", "audit our content", "content gaps", "what content do we have",
  "assess our content", "review our blog and LinkedIn". Diagnostic only: it does not write new content. Feeds /content-strategy.'
version: '1.0.0'
license: MIT
---

# Content audit

Take stock of what a company already publishes, channel by channel, so the next plan builds on real numbers instead of guesses. The output is a diagnosis: what exists, how often, on what topics, at which funnel stage, what works and what's missing.

## When to use it

Use it before writing a content strategy, when taking over a content programme, or when someone asks "what are we actually publishing and is it working?".

Don't use it to write posts or articles, to build the strategy itself (that's `/content-strategy`, which reads this audit), or for a one-channel quick look you can answer in a paragraph.

## Inputs

Read these first if they exist. Agency users: swap `context/` for `clients/<client>/context/`.

- `context/icp/`: who the content is for and the problems they have. Needed to judge relevance.
- `context/positioning/` and `context/messaging/`: what the company wants to be known for.
- `context/goals/`: what content is meant to deliver (pipeline, awareness, hiring).
- `context/competitors/`: optional, for a light benchmark.

Ask the user for:

- Company name and website URL (required).
- At least one content channel URL: blog or newsletter, LinkedIn company page or founder profile. Optional: YouTube, events page.
- Time range. Default to the last 6 months.

If a context file is missing, run anyway and say in the output which judgements are weaker because of it (for example, "relevance scored without an ICP file").

## Tools

If you have Firecrawl or Exa, use them to list and read pages. Otherwise use web search with `site:` queries, or ask the user to paste URLs or exports. List pages first, keep only the ones in scope, then read those. Don't crawl a whole domain to count blog posts.

## Steps

1. **Find the channels.** Check the site footer and navigation, then search `site:domain.com blog OR newsletter OR resources` and the company name on LinkedIn, YouTube and event platforms. Produces: a channel list with URL, active or inactive, and last-published date.
2. **Audit the blog or newsletter.** Sample the 10-15 most recent pieces. Record cadence (posts per month), topic, format, funnel stage, and quality signals: headline specificity, depth, a clear call to action, any lead magnet. Produces: a per-piece table plus a cadence figure.
3. **Audit LinkedIn.** Pull the last 20-30 posts. Record cadence, format (text, carousel, video, image, poll), topic, and visible engagement. Read 5-10 for voice and hook patterns. Produces: the same table for LinkedIn plus voice notes.
4. **Audit YouTube and events, if they exist.** Cadence, content types, recent view counts, production quality; for events, type, virtual or in-person, and community signals. Produces: one short section each.
5. **Map topics to the ICP.** Group everything into topic clusters and check each against the problems in `context/icp/`. Produces: a cluster table showing which ICP problems are covered, thin or missing.
6. **Check the funnel mix.** Tag each piece top (problem awareness), middle (how to solve it) or bottom (why this product). Produces: the mix as percentages per channel and overall.
7. **Score.** Rate 1-5 on volume, consistency, quality, ICP relevance, funnel balance and cross-channel alignment, then an overall health score. Each score gets one line of evidence.
8. **Find what works.** Name the 3-5 pieces or formats that clearly outperform the rest and say what they have in common.
9. **Write the recommendations.** Split into quick wins (this week), strategic fixes (next 30 days) and longer bets (next quarter). Each one names the gap it closes.

## What good looks like

- Every channel listed with its URL, status and last-active date.
- Numbers, not adjectives: "3.2 posts a month, mostly Tuesdays", not "posts regularly".
- Every key finding links to the specific post or page it came from.
- No invented engagement figures or guessed intent. Where data isn't visible, write "not available" and say how to get it.
- Gaps are stated in ICP terms: "nothing on [problem the ICP names]", not "needs more educational content".
- Recommendations are specific enough that someone could start one tomorrow.

## Mistakes to avoid

- Judging quality by taste. Tie every score to evidence or to the ICP's problems.
- Counting only the blog. LinkedIn and the founder's profile are often where the real output is.
- Reading likes as results. Engagement shows reach, not pipeline; say which you're looking at.
- Padding the recommendations. Five that matter beat fifteen that don't.

## Output

Write to `outputs/content/MMYY-content-audit.md` with this shape:

1. Header: company, website, audit period, channels audited, date.
2. Summary: three to five sentences on overall health and the biggest gap.
3. Scorecard: the six dimensions plus overall, 1-5, one line of evidence each.
4. Channel sections: inventory table, cadence, topics, formats, notes.
5. Topic and funnel analysis: cluster table against ICP problems, funnel mix.
6. What works: the outperformers and the pattern behind them.
7. Recommendations: quick wins, strategic, longer bets.
8. Input for the strategy: current baseline, gaps to close, voice patterns worth keeping.
9. Data gaps: what you couldn't see and how to get it.

Next step: run `/content-strategy`, which reads this file as its baseline.
