---
name: thought-leadership
description: 'Writes long-form thought leadership (articles, essays, whitepapers, guest posts) built on one contrarian, specific
  governing thought, with every claim sourced. Works in three approved stages: argument outline, prose draft, polish. Triggers:
  "thought leadership article", "long-form piece", "write a whitepaper", "write an article about", "turn this insight into an
  essay", "guest post". Not for short social posts or website copy.'
version: '1.0.0'
license: MIT
---

# Thought leadership

Write a long-form piece that changes what the reader believes. The method: find one governing thought the reader doesn't hold yet, build the argument for it, then write and polish, with the user approving each stage. Every claim is sourced or flagged.

## When to use it

Use it for articles, essays, whitepapers and guest posts where there's a real point of view to argue.

Don't use it for social posts, newsletter copy (use `/newsletter`), website copy, or a topic where the user has no opinion yet. If there's no angle, help find one first or stop.

## Inputs

Read these if they exist. Agency users: swap `context/` for `clients/<client>/context/`.

- `context/expert-pov/`: the founder's or experts' opinions, stories and arguments. The best source of angles.
- `context/icp/`: who's reading, what they believe now and what they're stuck on.
- `context/positioning/` and `context/messaging/`: what the company wants to be known for, and proof points.
- `context/competitors/`: what rivals already say, so the piece doesn't repeat it.
- `context/brand/`: voice rules.
- `outputs/content/*-content-strategy.md`: which cluster this piece belongs to.

Ask the user for: the topic, the audience, the core argument if they have one, any source material (interviews, data, notes), the publication and the target length (LinkedIn article 800-1,500 words, blog 1,500-2,500, guest post 2,000-3,500).

If `context/expert-pov/` is missing, interview the user for five minutes: what do they believe that most people in their field don't, and what happened that made them believe it?

## Stage 1: the argument (then stop)

1. **Find the governing thought.** Ask: "What's the one thing you want the reader to believe after this that they didn't believe before?" It has to be contrarian (a smart reader could disagree) and specific (it names who, what and why). "AI will change marketing" fails. "Most B2B teams should cut their blog output in half and spend the time on sales calls" passes.
2. **Find the reader's starting point.** What they believe now, the gap to the governing thought, and the three objections they'll raise.
3. **Build the pyramid.** The governing thought on top, two to four key arguments under it, evidence under each argument. This is the Pyramid Principle (Barbara Minto).
4. **Test it.** The key arguments don't overlap and together fully support the governing thought. Ask "so what?" of every level.
5. **Source check.** List every claim and its source. Anything without one gets `[source needed]` or comes out.

Show the outline, objections and source list. Wait for the user to approve before writing prose.

## Stage 2: the draft (then stop)

1. **Opening:** a hook that names a tension the reader feels, short context, then the governing thought stated plainly. No slow throat-clearing.
2. **Sections:** one per key argument. Each opens with its claim, gives the evidence, answers the relevant objection, then hands off to the next.
3. **Closing:** restate the governing thought in new words, say what the reader should do differently, and end with one call to action.
4. **Titles:** offer three options.

Show the full draft. Wait for approval before polishing.

## Stage 3: the polish (then stop)

1. **Voice:** apply `context/brand/`. Plain words, contractions, sentence-case headings, specific over superlative.
2. **Reader check:** would the ICP care, is it pitched at their level, would they forward it to a colleague?
3. **Evidence check:** no invented customers, numbers or quotes. Unverified examples are marked `[example, verify before publishing]`. External facts carry a link and the date accessed.
4. **Read it aloud.** Cut anything you wouldn't say to a peer.

Deliver the final piece with a short report: sources used, flags still open, and anything that needs the user's sign-off.

## What good looks like

- The governing thought fits in one sentence and someone could argue against it.
- The key arguments are distinct and each is backed by evidence the reader can check.
- Every claim is sourced or visibly flagged. Nothing invented.
- One or two persuasion moves that are true for this reader (a specific example, a named result, a credible source), not a pile of them.
- Concrete details over abstraction: a real situation, a number, a named step.

## Mistakes to avoid

- A safe thesis. If nobody would disagree, it isn't thought leadership.
- Skipping the stops. Writing prose on a weak argument wastes the user's review time.
- "Studies show" without the study.
- Buzzwords and filler: "game-changer", "cutting-edge", "in today's fast-paced world".
- Ending on a summary instead of what the reader should do next.

## Output

Write to `outputs/content/MMYY-<topic-slug>.md`: final piece, three title options, source list, open flags.

Next step: turn the piece into a newsletter issue with `/newsletter`, or slot it into the calendar from `/content-ops`.
