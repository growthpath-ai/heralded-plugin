---
name: competitor-gaps
description: Show where competitors beat a brand in AI answers and why, using Heralded. Use when someone asks who AI recommends instead of them, how they compare with a named competitor, where a rival wins, or what a competitor does that they don't.
---

# Competitor gaps

The person's own instructions take precedence over this skill.

Show who wins the answers the brand should win, where, and what they have that the brand lacks.

## Rank the field

1. Pick the brand: its domain from the person, or `list_brands`.
2. `list_competitors` with `with_details=true` and `with_trend=true`. Read the ranking by Heralded Score, share of voice, and each competitor's moves and AI description.
3. If the person named a competitor, use its key. Otherwise take the one or two that rank above the brand or gained most.

## Find the gaps

For each competitor:

- `get_competitor` with its `key` and `section=lost`: the questions where AI names the competitor and not the brand. `section=won` gives the reverse.
- `get_competitor` with `section=pages`: the competitor pages AI cites. These are what earns them the answers.
- `list_sources` with `names_you=false`, sorted by `citations`: sites AI cites that name rivals and not the brand.
- For a question that matters, `list_answers` with `prompt` and `names` set to the competitor, then `get_answer` on one, to quote how AI frames them.

## Write

- **Who wins.** The ranking in a short table: competitor, Heralded Score, trend, share of voice.
- **Where they win.** For each competitor that matters, the questions or topics they take, grouped by theme.
- **Why.** What the answers say about them and what they cite: their pages, the third-party sites that mention them. Quote the answer when it shows the reason.
- **What to do.** Two or three moves that would close the gap. Check `list_actions` first and point to Heralded's actions where they cover it.

Figures are points from 0 to 100 with a range. Treat unmeasured figures as unknown, never zero.
