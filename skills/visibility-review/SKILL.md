---
name: visibility-review
description: Review a brand's AI visibility with Heralded, what changed and what needs the person now. Use when someone asks how their brand is doing in AI answers, for a weekly or monthly review, a status update, a report for their boss or client, or "what should I look at in Heralded".
---

# AI visibility review

The person's own instructions take precedence over this skill.

Give the person their standing, what moved, and what needs them, in that order.

## Gather

1. Pick the brand. If the person named one, pass its domain as `brand`. Otherwise call `list_brands`; with several brands, ask which, or call `list_portfolio` when they want all of them.
2. `get_brand_overview` with `side=all` and `with_diagnosis=true`. This is the standing: the Heralded Score, Mentioned, Recommended, Understood and Praised, the leading competitors and the open actions.
3. `get_weekly_brief` with `with_today=true`: the decisions Heralded issued and what is live today.
4. `get_week_timeline`: what changed this week, results linked to work, and competitor moves.
5. `list_actions` with `assignee=mine_or_open`: what waits on the person's team, and how long each has waited (`waiting_since`).

For a longer period, pass `period=4w` or `12w` to the overview, and read `get_reports` for the reports already issued in that window.

## Write

- **Standing.** The Heralded Score with its range, and the four figures, each with its change. One line on where the brand ranks among its competitors.
- **What moved.** The two or three changes that matter most, each with its cause when Heralded gives one. Leave out moves Heralded marks steady.
- **Needs you.** Each waiting action in one line: what it is and the decision it needs.
- **Next.** One recommendation, drawn from the diagnosis or the actions.

Keep it to what a busy marketer reads in a minute. Offer to go deeper on any line: the `explain-a-change`, `competitor-gaps`, `source-outreach` and `content-opportunities` skills do that.

## Read figures as Heralded states them

- Figures are points from 0 to 100 with a 95% range. Quote the range when two figures are close.
- `pending`, `not_measured`, `not_scored` and `too_few_answers` are unknown, never zero.
- Call a figure up or down only when its state says `up` or `down`. Respect `first_report` and `not_comparable`.
