---
name: run-snapshot
description: Run a Heralded Snapshot of a website and report its result. Use when someone asks to run a Snapshot, or to measure a site's AI visibility, such as a prospect's, a client's or a competitor's, and agrees to spend a Snapshot on it.
---

# Run a Snapshot

The person's own instructions take precedence over this skill.

A Snapshot measures how AI answers treat one website. It uses the person's free Snapshot or one of their workspace's Snapshot credits, and it needs Full access.

1. Unless the person asked for a Snapshot in so many words, ask first: say it measures the site in AI answers and uses a Snapshot. Don't start one to answer a general question about a brand.
2. `get_free_snapshot`: say whether this run is free or uses a credit.
3. `start_snapshot` with the `domain`. Nothing is spent yet, but until it runs, or lapses unrun after 24 hours, it holds a place against the person's free Snapshot and credits. It returns a drafted profile: brand, what it does, category, buyer, market and the competitors found so far. A null profile is still drafting, so read it again with `get_scan`.
4. Show the profile and ask the person to confirm it. `edit_snapshot` can correct the brand name, the description and the market. Category, buyer and competitors can't be changed: the Snapshot ranks the competitors its AI answers name. Skip the check only when they said to run without checking.
5. `run_snapshot` once they agree. Give them the returned link for live progress. It takes about 6 to 10 minutes.
6. Check on it with `get_scan` and the `scan_id`. While it runs, report progress as answers read of answers total. When it completes, report the Heralded Score with its range and give the report link.

After it completes, `get_shared_snapshot` with the `share_id` from `get_scan` gives the detail: which competitors win, how each engine answers, the sources cited and the market's demand. Offer the person a short read of it.

If a Snapshot tool is refused for lack of access, the connection is Read only. Tell the person to reconnect Heralded with Full access to run Snapshots.
