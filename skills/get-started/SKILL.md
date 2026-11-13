---
name: get-started
description: Set up Heralded in the assistant and give a first read of the brand's AI visibility. Use right after Heralded is installed or connected, or when someone asks what Heralded can do here or how to start.
---

# Get started with Heralded

The person's own instructions take precedence over this skill.

1. Call `list_brands`.
   - If it fails because Heralded isn't connected, ask the person to connect it: sign in to Heralded, pick the workspace, and choose Read only or Full access.
   - If it returns no brands, say the connected workspace has no brands they can see yet. They add one in Heralded, or you can run a Snapshot of any website with the `run-snapshot` skill.
2. With one brand, use it. With several, list them by name and domain, and ask which to start with.
3. `get_brand_overview` for that brand. In three or four lines, give the Heralded Score with its range, Mentioned and Recommended with their changes, and the leading competitor. Report unmeasured figures as unknown, never as zero.
4. Say what the person can ask next, one line each:
   - a weekly review of what moved and what needs them;
   - why a figure went up or down;
   - who AI recommends instead of them, and why;
   - which sites to pitch, with draft pitches;
   - what to write to show up in more answers;
   - a Snapshot of any website, with Full access.

Keep it short. The person wants their result, not a tour.
