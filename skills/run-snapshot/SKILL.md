---
name: run-snapshot
description: Run a Heralded Snapshot of any website and report its result. Use when someone asks to check a site's AI visibility, to measure a prospect, client or competitor, or to run a Snapshot.
---

# Run a Snapshot

The person's own instructions take precedence over this skill.

A Snapshot measures how AI answers treat one website. It needs Full access, and it spends the person's free Snapshot or a Snapshot credit.

1. `get_free_snapshot`: say whether this run is free or uses a credit, before starting.
2. `start_snapshot` with the `domain`. Nothing is spent yet. It returns a drafted profile: brand, what it does, category, buyer, market and competitors found. A null profile is still drafting, so read it again with `get_scan`.
3. Show the profile and ask the person to confirm it. Correct it with `edit_snapshot`. Skip this only when they said to run without checking.
4. `run_snapshot` once they agree. Give them the returned link for live progress. It takes about 6 to 10 minutes.
5. Check on it with `get_scan` and the `scan_id`. While it runs, report progress as answers read of answers total. When it completes, report the Heralded Score with its range and give the report link.

After it completes, `get_shared_snapshot` with the `share_id` from `get_scan` gives the detail: which competitors win, how each engine answers, the sources cited and the market's demand. Offer the person a short read of it.
