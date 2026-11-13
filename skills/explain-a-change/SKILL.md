---
name: explain-a-change
description: Find out why a brand's AI visibility moved, using Heralded's answers, competitors and sources. Use when someone asks why their Heralded Score, Mentioned or Recommended went up or down, why they dropped on an engine or topic, or what caused a change in their weekly report.
---

# Explain a change

The person's own instructions take precedence over this skill.

Trace a move in a figure to the answers behind it, then say what caused it and whether it needs action.

## Find the move

1. Pick the brand: its domain from the person, or `list_brands`.
2. `list_changes`: the measured changes, newest first, with their supporting evidence. Match the one the person means. If they name none, take the largest recent move.
3. `get_scores` with `group_by=engine`, then `group_by=topic`, with `with_trend=true`. Find where the move is concentrated. A move on one engine or one topic has a narrower cause than a move everywhere.

## Find the cause

Work from the narrowest slice the scores showed.

- **Questions.** `list_prompts` filtered to that engine or topic, sorted by `change`. These are the questions where the brand gained or lost.
- **Answers.** For the two or three questions that moved most, `list_answers` with `prompt` and `period=4w`, then `get_answer` on a recent answer and an older one. Compare who each names and what each cites.
- **Competitors.** `list_competitors` with `with_details=true` for the same slice. A competitor that gained where the brand lost is the likeliest cause.
- **Sources.** When the answers changed what they cite, `get_source` on the domain that appeared or disappeared.
- **Heralded's own read.** `list_evidence` with `subject` set to the prompt, topic or figure.

## Write

1. The move in one sentence: which figure, how much, where.
2. The cause, with the evidence: quote the answer lines or name the cited pages that show it. Say how sure you are. One answer is an anecdote, a pattern across questions is a cause.
3. What to do about it. Check `list_actions` with `subject` first, and say when Heralded already has an action for it.

Never call a move up or down unless its state says so. A figure marked `not_comparable` or `first_report` has no change to explain.
