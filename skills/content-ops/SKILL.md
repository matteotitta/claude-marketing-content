---
name: content-ops
description: 'Turns a content strategy into a system a team can run: recurring series, a cross-channel calendar, content briefs,
  a production pipeline with owners, and review steps before anything ships. Triggers: "content operations", "content calendar",
  "content pipeline", "content briefs", "editorial workflow", "operationalise the strategy", "turn this into a calendar".
  Reads the output of /content-strategy. Not for writing the pieces themselves.'
version: '1.0.0'
license: MIT
---

# Content ops

A strategy says what to publish. This skill decides who makes it, when, from what brief, and who checks it before it goes out. The output is a calendar, a brief template, a pipeline and a review checklist sized to the team you actually have.

## When to use it

Use it once a strategy exists and the team is ready to produce, when output is erratic, or when pieces keep stalling in review.

Don't use it to build the strategy (run `/content-strategy` first), to write the pieces, or to audit what already exists (`/content-audit`).

## Inputs

Read these if they exist. Agency users: swap `context/` for `clients/<client>/context/`.

- `outputs/content/*-content-strategy.md`: clusters, funnel mix, channels, volume targets. Required.
- `context/brand/`: voice rules, which become review criteria.
- `context/messaging/`: approved claims and proof points, which reviewers check against.

Ask the user for:

- Team: who is involved and hours per week each.
- Tools: where the calendar and pipeline will live (Notion, Airtable, a spreadsheet, a project tool).
- Who has final sign-off, and anything that needs legal or compliance review.

If there's no strategy file, stop and suggest `/content-strategy`. If you only have clusters and channels, carry on and flag what's missing.

## Steps

1. **Design the series.** Give each cluster one to three recurring series with a clear arc: a problem series, a how-it-works series, a case series, an opinion series. Each instalment should build on the last. Produces: a series list with cluster, funnel stage, cadence and the first four titles.
2. **Plan the cascade.** For the anchor format, map which smaller pieces come out of it, on which channel, in which order. A typical pattern: anchor piece on day 1, two LinkedIn posts that week, a newsletter mention the next. Produces: a cascade map.
3. **Build the calendar.** Lay out 8-12 weeks across channels. Keep a two-week buffer of finished pieces and one open slot a week for timely topics. Produces: a calendar table with date, channel, series, title, funnel stage, owner and status.
4. **Write the brief template.** Every piece starts from a brief: the ICP problem it answers, the one point the reader should take away, the funnel stage, the proof or example to use, the call to action, the format and length, the owner and the due date. Produces: a template plus filled briefs for the first two weeks.
5. **Set the pipeline.** Stages: idea, briefed, drafting, review, approved, scheduled, published, reviewed for results. Each stage has an owner and a clear exit rule (for example, "review" ends when the reviewer signs off against the checklist). Produces: a stage table.
6. **Fit roles to the team.** Solo: one person writes and reviews, with a waiting period before publishing and design done with templates or AI help. Small team: split writer and reviewer. Larger team: add an editor and a designer. Produces: a roles table with hours per week.
7. **Write the review checklist.** What every piece is checked against before it ships (see below). Produces: a checklist the reviewer runs on every piece.
8. **Set the results review.** A monthly look at what performed by series and format, with rules: a series that clearly beats the channel average gets more slots; one that trails for two months gets cut or changed. Produces: the review agenda and those rules.

## The review checklist

- Answers the ICP problem named in the brief.
- Makes one point, stated early.
- Every claim, number and customer reference has a source. Missing ones are marked `[source needed]` and the piece doesn't ship until they're filled.
- Matches the voice rules in `context/brand/` and the approved claims in `context/messaging/`.
- Has one call to action that fits the funnel stage.
- Reads like a person wrote it: contractions, plain words, no filler openers or buzzwords.
- Compliance or legal sign-off where required.

## What good looks like

- The calendar is realistic for the stated hours, with buffer.
- Every calendar entry traces to a series and a cluster from the strategy.
- Briefs are short enough to fill in five minutes and specific enough that two writers would produce similar pieces.
- Nothing ships without passing the checklist.

## Mistakes to avoid

- Calendars with no buffer. One sick week and the whole thing slips.
- Review by gut feel. Use the checklist so feedback is consistent.
- Too many stages for a solo operator. Collapse them.
- Treating the calendar as fixed. The monthly review exists to change it.

## Output

Write to `outputs/content/MMYY-content-ops.md`: series plan, cascade map, calendar, brief template with the first briefs filled, pipeline stages, roles, review checklist, results-review rules.

Next step: write the pieces with `/thought-leadership` for long-form and `/newsletter` for the newsletter.
