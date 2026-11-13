---
name: content-opportunities
description: Find the questions and topics where AI answers leave a brand out, and turn them into content briefs, using Heralded. Use when someone asks what to write, which pages to create or update, content ideas for AI visibility, or how to show up for a question or topic.
---

# Content opportunities

The person's own instructions take precedence over this skill.

Find where the brand is absent from answers buyers get, and say what content would put it there.

## Find the gaps

1. Pick the brand: its domain from the person, or `list_brands`.
2. `get_topics` with `with_trend=true`, sorted by `demand`. Topics in the `Invisible` and `Under-visible` bands with real demand come first. `view=suggested` adds topics the brand doesn't track yet.
3. For a topic worth taking, `list_prompts` with `topic` and `you=not_named`: the questions where AI leaves the brand out.
4. For two or three of those questions, `list_answers` with `prompt`, then `get_answer` on one: who is named instead, and which pages are cited.
5. `get_page` lists the brand's own pages and how AI cites them. An existing page to improve beats a new one.
6. `list_actions` with `subject=topic:<id>`: Heralded may already have a content action with a draft. Point to it rather than writing a second brief.

## Write

For each opportunity, a brief:

- **The question** buyers ask and what AI answers today, in one line.
- **Who wins it** and the pages that earn it.
- **The page to write or update**, its angle, and what it must cover to be the better source. Base it on what the cited pages cover and miss.
- **Facts to use** from `get_brand_profile`. Never invent claims about the brand.

For a page to update, `preview_content_language` with its `page_url` gives the language to write it in.

Rank the briefs by demand and by how far the brand is behind.
