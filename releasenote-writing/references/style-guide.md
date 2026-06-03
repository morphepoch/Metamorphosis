# Release Note Style Guide

Source basis:

- NotebookLM X account: https://x.com/NotebookLM. X pages may be sparse in crawled HTML, so this guide relies on accessible indexed post snippets and observed account pattern.
- Claude release notes: https://support.claude.com/zh-CN/articles/12138966-发布说明.
- Manus updates/blog: https://manus.im/zh-cn/updates and related public product update pages such as https://manus.im/zh-cn/blog/manus-projects-self-updating and https://manus.im/zh-cn/blog/manus-max-release.

## NotebookLM Style

Best for: social posts, short launch blurbs, compact community updates, newsletter openers, and "what can I try now?" announcements.

Content character:

- Conversational, upbeat, concise.
- Speaks directly to users with "you can now..." and short questions.
- Frames the release as an invitation to try, not a formal changelog.
- Uses temporal hooks like "Starting today" or "Now available" when true.
- Often bundles features as a compact list after a short setup.
- Length should track the user's source material. For longer inputs, keep all major feature groups and examples, but make each sentence more direct and social-friendly.
- When the source has multiple feature sections, preserve that section logic. Write one lightweight NotebookLM-style block per heading, feature group, or logical block instead of compressing everything into a single umbrella list. Do not force a fixed number of sections; mirror the input's natural structure.

Structure:

```markdown
[One-line announcement or hook]

[Brief context sentence: what changed and why it matters.]

Starting today, you can now:
— [Action-oriented capability 1]
— [Action-oriented capability 2]
— [Action-oriented capability 3]

[Short CTA or question]
```

Formatting:

- Prefer 1-3 short paragraphs.
- For longer launch material, use one short paragraph plus compact bullets for each major feature group; do not collapse multiple major features into one generic bullet.
- Use em-dash style bullets (`—`) for social copy, or simple hyphen bullets if the destination does not support em dashes.
- Keep each bullet under one line when possible.
- Use product mentions naturally; avoid long headings.
- Optional emojis may be used only if the user's brand voice permits them.

Voice moves:

- "Have you tried...?"
- "What do you think?"
- "Now you can..."
- "We’re taking [existing workflow] to the next level" when there is a genuine continuation of a prior feature.

Avoid:

- Long explanation, nested bullets, technical implementation detail.
- Formal date/month archive structure.
- Unsupported hype such as "revolutionary" or "game-changing."
- Turning a multi-part source into a one-part summary when the user expects comparable coverage.

Multi-section template:

```markdown
[One-line umbrella hook.]

[Feature group A is now available / ready / easier.]

Starting today, you can:
— [Capability]
— [Capability]
— [Capability]

[Short example or try-it prompt.]

[Feature group B is coming / now available.]

You can:
— [Capability]
— [Capability]
— [Capability]

[Short example or try-it prompt.]

[Feature group C improves the ongoing workflow.]

Now you can:
— [Capability]
— [Capability]
— [Capability]

[Closing CTA.]
```

## Claude Style

Best for: help center release notes, changelog pages, product documentation updates, multi-feature monthly summaries, and factual update archives.

Content character:

- Neutral, direct, highly scannable.
- Leads with date and feature title.
- Explains the change in one paragraph, then links to documentation or blog posts.
- Uses bullet lists for subfeatures or related articles.
- Prioritizes what shipped, who can use it, and where to learn more.

Structure:

```markdown
## [YYYY年M月]

### [YYYY年M月D日]

[Feature title]

[One paragraph describing the release, availability, and user value. Include "有关更多信息，请参阅..." / "Learn more..." links when available.]

[Second feature title, if same date]

[One paragraph.]

  * [Related article or subfeature]
  * [Related article or subfeature]

* * *
```

Formatting:

- Month as `##`.
- Date as `###`.
- Feature titles are plain text lines below the date, not necessarily headings.
- Use short paragraphs of 1-3 sentences.
- Use indented asterisk bullets for related links or grouped subfeatures.
- Use horizontal rules between month sections when building a long archive.

Voice moves:

- "现已..."
- "我们推出了..."
- "我们改进了..."
- "有关更多信息，请参阅..."
- "此功能适用于..."

Avoid:

- Marketing flourish and broad narrative setup.
- Rhetorical questions.
- Long "why this matters" sections unless the source material requires it.
- Mixing multiple unrelated changes into one paragraph.

## Manus Style

Best for: product blog launches, strategic updates, major feature announcements, product education, and announcements that need to turn a capability into a user workflow.

Content character:

- Narrative and explanatory.
- Starts with a product/category label and publication date when available.
- Uses a strong H1, then a short lead that states the new capability and value.
- Frames the problem before the solution.
- Uses clear sections such as "该功能的作用", "主要能力", "为什么这很重要", "如何使用", "可用性", and "常见问题 / FAQ".
- Often uses bullet lists with the `•` marker and short bolded capability labels.

Structure:

```markdown
产品·[日期]

# [Launch title]

[Lead: what is new and the user-level promise.]

[Problem/context paragraph.]

[Solution paragraph beginning with "现在..." when appropriate.]

## 该功能的作用

[Explain the feature in concrete workflow terms.]

## 主要能力

•[Capability label]: [What users can do and why it helps.]

•[Capability label]: [What users can do and why it helps.]

## 为什么这很重要

•[Outcome 1.]

•[Outcome 2.]

## 如何使用

1.[Step 1.]
2.[Step 2.]
3.[Step 3.]

## 可用性

[Plans, platforms, rollout, limits.]

## 常见问题 / FAQ

问:[Question?]

答:[Answer.]

## [Closing]

[Short closing that returns to the product vision or user workflow.]
```

Formatting:

- H1 for the announcement title.
- H2 for conceptual sections.
- H3 for feature pillars inside major launch posts when needed.
- Use `•` bullets for capabilities and reasons.
- Use numbered steps for usage.
- Use simple markdown tables for examples, scenarios, or comparisons when they clarify repeated patterns.
- Keep paragraphs short but allow more context than Claude style.

Voice moves:

- "在此之前..."
- "现在，Manus 可以..."
- "这意味着..."
- "为什么这很重要"
- "从...到..."
- "更少的重复说明 / 更高的连续性 / 从最新上下文开始" style outcome phrasing.

Avoid:

- Thin changelog entries with no user workflow.
- Overly casual social CTA.
- Dense technical lists without narrative or use cases.

## Auto-Match Heuristics

Use these signals when the user does not specify a style:

| Input signal | Best style |
| --- | --- |
| One feature, social channel, "发 X/微博/朋友圈/社区", short launch copy | NotebookLM |
| Many dated changes, docs/help center, version history, release archive | Claude |
| Major product capability, blog post, launch article, needs "why/how/FAQ" | Manus |
| Internal engineering changelog but external users need to understand changes | Claude, unless strategic positioning is requested |
| Product marketing launch with use cases and workflow examples | Manus |
| Mobile/app store update notes under strict length | NotebookLM or Claude depending on formality |

## Drafting Transformations

- Convert implementation notes into outcomes:
  - "Added API endpoint" -> "Admins can now access..."
  - "Refactored upload flow" -> "Uploads are more reliable and easier to recover..."
  - "Supports connector X" -> "You can now connect X to..."
- Preserve constraints:
  - plan tiers, platform, geography, beta/preview status, rollout windows, admin controls, data/privacy notes.
- Replace internal verbs:
  - "fixed" -> "improved", "resolved", or "now handles..."
  - "launched backend support" -> "now supports..."
  - "edge case" -> describe the user-visible situation.
- Make bullets parallel:
  - Start with verbs for capabilities: "创建", "连接", "查看", "管理".
  - Start with nouns for benefits: "更高的...", "更少的...", "更清晰的...".

## Quick Templates

NotebookLM:

```markdown
[Feature] is now available for [audience/platform].

Starting today, you can now:
— [Do X]
— [Do Y]
— [Do Z]

[CTA/question]
```

Claude:

```markdown
## [Month]

### [Date]

[Feature title]

[Product] 现已支持 [capability]. [Audience/availability]. 有关更多信息，请参阅 [link/placeholder].
```

Manus:

```markdown
# [Launch title]

[Product] 现在可以 [new capability]，让 [audience] 能够 [primary outcome].

在此之前，[problem/context]. 现在，[solution].

## 主要能力

•[Capability]: [Benefit].

## 如何使用

1.[Step].
2.[Step].
3.[Step].
```
