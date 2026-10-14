---
name: content-strategy
description: 'Builds a B2B content strategy from your context files: topic clusters tied to real ICP problems, funnel mapping,
  a channel mix, cadence and volume targets, and a 90-day plan. Triggers: "content strategy", "content pillars", "content
  plan", "90-day content plan", "what should we publish", "content roadmap", "LinkedIn content strategy", "newsletter strategy".
  Not for writing individual pieces. Hands off to /content-ops to turn the plan into a calendar and pipeline.'
version: '1.0.0'
license: MIT
---

# Content strategy

Turn what you know about your buyers, your positioning and your current content into a plan a small team can run: what to write about, for which buyer problem, on which channels, how often, and what the next 90 days look like.

## When to use it

Use it when starting or resetting a content programme, when a team publishes a lot but can't say why, or when someone asks "what should we be publishing?".

Don't use it to write posts or articles, to build messaging from scratch (do that first, then come back), or to plan a single launch.

## Inputs

Read these if they exist. Agency users: swap `context/` for `clients/<client>/context/`.

- `context/icp/`: segments, roles and the problems they name. This drives everything; it's the one input you really need.
- `context/positioning/` and `context/messaging/`: what the company wants to be known for and its proof points.
- `context/competitors/`: what rivals already cover, so you can find the open ground.
- `context/expert-pov/`: the founder's or experts' strong opinions; these become the most distinctive content.
- `context/goals/`: what content must deliver and by when.
- `context/brand/`: voice rules.
- `outputs/content/*-content-audit.md`: the baseline from `/content-audit`, if it has run.

Ask the user for team size and hours per week for content, plus any channels that are fixed.

If there's no ICP file, ask the user to describe their buyer and the top three problems in their words before going further. If other files are missing, proceed and list the assumptions you made.

## Steps

1. **Set goals.** Pick two to four content goals in priority order (pipeline, awareness, hiring, customer retention), each with a measure. Produces: a goals table.
2. **List the ICP problems.** Pull 5-10 specific problems from `context/icp/`, in the buyer's words. Produces: a problem list. This is the spine of the strategy.
3. **Build topic clusters.** Group the problems into four or five clusters. Each cluster is a topic the company can credibly own, named for the buyer problem it answers, not a generic bucket like "educational" or "thought leadership". Give each a share of output (for example 30/25/20/15/10). The company's core theme from positioning runs through every cluster rather than being its own. Produces: a cluster table with the problem, the angle and the share.
4. **Map the funnel.** For each cluster, name content at the top (the problem exists and costs money), middle (how to solve it) and bottom (why this company). A typical split is 40/35/25. Produces: a cluster by funnel grid with a named example in every cell.
5. **Choose channels.** Start with LinkedIn plus a blog or newsletter. Add video, podcast or events only if the team has capacity and the ICP is there. Pick one anchor format, the highest-effort piece, and show how it breaks into 5-10 smaller pieces. Produces: a channel table with format, frequency, main cluster and the metric to watch.
6. **Set volume and cadence.** Work out monthly totals per channel and per cluster that fit the stated team capacity. Produces: volume targets and a weekly rhythm.
7. **Plan 90 days.** Month 1 establishes the clusters and the anchor format. Month 2 goes deeper on the problems that got traction. Month 3 shifts toward proof: case stories, comparisons, bottom-of-funnel pieces. Name the recurring series. Produces: a month-by-month plan and one sample week.
8. **Set measures and review rules.** Primary and secondary metric per channel, a monthly review, and what triggers a change (cut a cluster, double a format). Produces: a measurement table.
9. **List gaps and assumptions.** What you didn't know and what research would close it.

## What good looks like

- Every cluster traces to a named ICP problem. If you can't point to the problem, cut the cluster.
- Clusters are specific enough that a competitor couldn't copy the list unchanged.
- Both mixes (cluster and funnel) add up to 100%, with monthly counts.
- Volume fits the team. Two people can't sustain 40 pieces a month.
- The 90 days build on each other rather than repeating month 1 three times.
- Every channel has one metric that matters, tied to a goal.

## Mistakes to avoid

- Generic pillars (educational, personal, promotional). They describe format, not what you'll be known for.
- Channel sprawl. Two channels done well beat five done thinly.
- Planning without capacity. Ask for hours before setting volume.
- All top-of-funnel. Awareness content with no path to the product doesn't create pipeline.
- Inventing data: no made-up benchmarks or audience sizes. Mark estimates as estimates.

## Output

Write to `outputs/content/MMYY-content-strategy.md`:

1. Summary: the goals, the clusters and the channels in five lines.
2. Goals and measures.
3. ICP problems and topic clusters, with shares.
4. Cluster by funnel grid with example pieces.
5. Channel plan, anchor format and how it breaks down.
6. Volume, cadence and a sample week.
7. 90-day plan and recurring series.
8. Measurement and review rules.
9. Assumptions and open questions.

Next step: `/content-ops` turns this into a calendar, briefs and a review process. `/thought-leadership` and `/newsletter` write the pieces.
