---
name: releasenote-writing
description: "Release note and product update announcement writing for user-facing launches. Use when the user provides feature notes, changelog items, PRDs, launch docs, screenshots, drafts, or rough bullet points and wants them rewritten, polished, localized, or structured as a release note in one of three styles: NotebookLM social-update style, Claude Help Center release-note style, or Manus product-announcement style. Also use when the user asks to auto-match a release-note style, compare announcement tones, or turn internal updates into external product marketing copy."
---

# Releasenote Writing

## Workflow

1. Read the user's source material and identify the audience, product surface, launch size, availability, and intended channel.
2. Choose a style:
   - Use the user's explicit choice when provided: `notebooklm`, `claude`, or `manus`.
   - Auto-match when no style is provided using the decision rules below.
3. Read [references/style-guide.md](references/style-guide.md) before drafting. Load only the chosen style section unless comparing styles.
4. Convert internal notes into user-facing benefits. Preserve factual constraints, eligibility, dates, regions, pricing, model/version names, and links.
5. Draft in the chosen structure and level of detail. Keep the output close to the source material's information density unless the user asks for a shorter or longer version.
6. Add a short "Assumptions / needs confirmation" note only if a publish-critical fact is missing or inferred.

## Style Selection

- Choose **NotebookLM style** for short social announcements, launch posts, community updates, or when the goal is excitement and quick comprehension.
- Choose **Claude style** for changelogs, help-center release notes, monthly grouped updates, docs-style announcements, or when accuracy and scanability matter more than persuasion.
- Choose **Manus style** for major launches, product blogs, narrative announcements, feature education, or when the update needs positioning, use cases, and "why it matters."

When several styles fit, prefer the smallest style that can carry the content:
NotebookLM for one feature or a small bundle; Claude for many discrete changes; Manus for strategic or high-context launches.

## Output Rules

- Write in the user's language unless they ask otherwise.
- Keep claims grounded in the provided material. Do not invent metrics, rollout dates, platform availability, pricing, or customer outcomes.
- Translate capability into user value, but keep concrete feature names intact.
- Match heading depth, bullet shape, and paragraph length to the chosen style guide.
- For external announcements, include availability and next action when known.
- For drafts based on messy inputs, silently consolidate duplicates and group related changes.
- Do not over-compress long source material just because a compact style is selected. A short-channel style should simplify wording and structure while retaining the main feature groups, user benefits, and examples.
- For NotebookLM-style drafts, preserve the user's source information architecture. If the input has explicit headings, feature groups, or logical blocks, produce matching lightweight announcement blocks with the same short, direct sentence style rather than one compressed summary. Do not force a fixed number of sections.

## Quality Checklist

Before finalizing, verify:

- The style choice is explicit or clearly implied.
- The opening explains what changed without burying the feature.
- Bullets are parallel and concrete.
- Limitations, plan/region eligibility, and rollout timing are visible.
- The draft has no internal-only language such as "ticket," "Jira," "backend refactor," or "we fixed a bug" unless the audience expects it.
- Links or placeholders are present for "learn more," documentation, blog posts, or update pages when appropriate.
