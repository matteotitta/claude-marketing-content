---
name: newsletter
description: 'Writes one B2B newsletter issue built on a single idea: picks the idea from your expert point of view and recent
  work, structures it as hook, idea, proof, one takeaway and one call to action, then adds subject line options and a short
  LinkedIn promo post. Triggers: "write our newsletter", "next newsletter issue", "newsletter draft", "write this week''s
  newsletter", "newsletter subject lines". Not for long-form articles (use /thought-leadership).'
version: '1.0.0'
license: MIT
---

# Newsletter

Write one newsletter issue that a busy buyer reads to the end. One idea per issue, made concrete with a real example, ending on one takeaway and one ask. Then give the issue its best chance of being opened (subject lines) and seen (a LinkedIn post).

## When to use it

Use it for a weekly or fortnightly B2B newsletter, or to turn a recent piece of work into an issue.

Don't use it for long-form essays (use `/thought-leadership`), product announcements that need launch planning, or a link digest with no point of view.

## Inputs

Read these if they exist. Agency users: swap `context/` for `clients/<client>/context/`.

- `context/expert-pov/`: opinions, stories and lessons worth sharing. The main source of ideas.
- `context/icp/`: who reads it and what they're stuck on.
- `context/brand/`: voice rules.
- `outputs/content/`: recent strategy, articles and audits. Recent work is often the best raw material.
- `outputs/content/*-content-strategy.md`: the clusters, so the issue fits the plan.

Ask the user for: what they've worked on, learned or argued about in the last two weeks, the newsletter's usual length, and what the call to action should point to (a reply, a resource, a call, an event).

If `context/expert-pov/` is missing, ask the user three questions: what surprised you lately, what do you disagree with in your field, and what did a customer or colleague get wrong that you see often?

## Steps

1. **Pick one idea.** List three candidates from `context/expert-pov/`, recent work and the user's answers. Pick the one that is specific, useful to the ICP, and grounded in something that actually happened. Produces: the idea in one sentence, plus why this reader should care now.
2. **Find the proof.** One concrete example: a project, a before-and-after, a mistake, a number from real work. If it involves a customer, generalise it ("a Series B fintech") unless the user confirms they can be named. Produces: the example with its source.
3. **Write the issue** in this order:
   - **Hook** (2-3 sentences): the tension or surprise, aimed at the reader's problem. No "welcome back" or "this week I want to talk about".
   - **The idea** (one short section): state it plainly, then explain why it's true.
   - **Proof or example** (the longest section): what happened, what was done, what changed.
   - **One takeaway**: what the reader can do or think differently on Monday, in a sentence or two.
   - **One call to action**: a single ask that fits the takeaway.
4. **Subject lines.** Write five options under 50 characters: one plain statement of the idea, one question, one with a number, one naming the reader's problem, one curiosity line that the issue actually pays off. Recommend one. Add a preview text line.
5. **LinkedIn promo post.** 150-300 words that stand on their own: the hook rewritten for the feed, the idea in brief, one line from the example, then an invite to read or subscribe. Plain text, no emojis, no hashtag lists.
6. **Check.** Run the checklist below and fix anything that fails.

Length: 500-1,200 words for the issue unless the user's newsletter runs differently. Match what they already send.

## What good looks like

- One idea. A reader can repeat it in a sentence.
- The example is real and specific. Invented numbers or customers are never used; a missing fact is marked `[check]` for the user.
- The hook is about the reader, not the writer or the newsletter.
- Exactly one takeaway and one call to action.
- Subject lines are honest: the issue delivers what the line promises.
- It reads like a person wrote it: contractions, short sentences, plain words.

## Mistakes to avoid

- Three ideas in one issue. Save two for later issues.
- A summary of links with no opinion.
- Burying the idea under a long personal preamble.
- Clickbait subject lines that the issue doesn't pay off.
- A promo post that only says "new issue is out".
- Several calls to action competing with each other.

## Output

Write to `outputs/content/MMYY-newsletter-<topic-slug>.md`:

1. Recommended subject line, four alternatives, preview text.
2. The issue.
3. The LinkedIn promo post.
4. Sources and any `[check]` flags for the user.

Your email platform (Substack, beehiiv, Kit or another) is where you paste and send; this skill only drafts. Next step: if the idea deserves more room, expand it with `/thought-leadership`.
