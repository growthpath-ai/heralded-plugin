---
name: source-outreach
description: Find the third-party sites AI cites where a brand is missing, and draft outreach to get on them, using Heralded. Use when someone asks which sites or publications to pitch, where to get mentioned, for PR or link targets, for review sites to be on, or to draft an outreach email for AI visibility.
---

# Source outreach

The person's own instructions take precedence over this skill.

Find the sites AI trusts in the brand's market that don't name the brand yet, and help the person get on them.

## Find the targets

1. Pick the brand: its domain from the person, or `list_brands`.
2. `list_sources` with `owner=third_party`, `names_you=false` and `sort=priority`. Add `opening=true` to keep sites with an opening the brand could pitch. Filter by `source_type`, such as `review`, `media` or `community`, when the person wants one kind.
3. For the top five, `get_source` with its `domain` and `actions_limit=5`: the cited pages, the questions they are cited for, and Heralded's related actions.
4. `list_cited_pages` with `domain` shows which pages on a site AI cites and how they describe the brand and its competitors.
5. `list_actions` with `subject=source:<domain>`: Heralded may already propose outreach for that site, with a draft. Use its draft rather than writing a second one.

## Write

A short table of targets: site, kind, how often AI cites it, which competitors it names, and the opening.

Then, for the targets the person picks, a pitch:

- To the right person or page on that site: the editor, the list owner, the review profile.
- Built on what the site already publishes: the cited page, and the gap where the brand belongs on it.
- With a reason to include the brand that the site's readers would care about. Use the facts from `get_brand_profile`, never invented claims.
- Short. A subject line and under 150 words.

Never send anything. The person sends the pitch.
