---
name: interactive-html-insight-report
description: Create self-contained interactive HTML insight reports from datasets, analysis notes, research findings, or business reviews. Use when the user wants a polished single-page report, dashboard-style briefing, decision memo with tabs or filters, or a visual analysis artifact that combines metrics, interpretation, opportunities, risks, and action recommendations.
---

# Interactive HTML Insight Report

## Purpose

Turn messy analytical material into a self-contained interactive HTML report that helps people understand the situation, compare dimensions, and decide what to do next.

Use this skill when the user provides data, notes, research findings, meeting context, or a business question and wants a report that is easier to scan than a long document, more interactive than a slide deck, and lighter than a full BI dashboard.

## Default Output

Create a single `index.html` file with:

- HTML, CSS, and vanilla JavaScript only.
- No external libraries, CDNs, icon fonts, trackers, or remote assets unless the user explicitly asks.
- A professional report layout with sticky top navigation, responsive sections, compact visuals, and clear action recommendations.
- Local data embedded in the file unless the user asks for dynamic data loading.

## Core Principles

- **Insight over decoration.** Visuals must explain meaning, tradeoffs, priorities, or next actions.
- **Infer useful dimensions.** The user may not know the right cuts in advance. Infer dimensions from the material, such as segment, persona, product, market, region, time, funnel stage, sentiment, competitor, use case, opportunity, or risk.
- **Respect evidence limits.** Preserve dates, sample sizes, data sources, assumptions, and uncertainty.
- **Use first-principles reasoning.** Identify the underlying decision, user need, constraint, economic driver, or operational bottleneck behind the data.
- **Add adversarial review.** Include what could be wrong, what is overclaimed, what needs validation, and what evidence would change the conclusion.
- **Keep it usable.** This is a report, not a full application. Prefer simple interactions that make reading easier.

## Workflow

1. **Clarify only when blocked.** If the topic, source material, and intended audience are clear enough, proceed.
2. **Read the source material.** Use available files, tables, notes, documents, or user-provided context. Do not invent facts.
3. **Derive the architecture.**
   - Choose 5-8 top-level sections for the navigation.
   - Add secondary controls only where comparison improves understanding.
   - Group content by decision-relevant dimensions, not by the order of raw input.
4. **Analyze the material.**
   - Separate facts, interpretations, implications, and recommendations.
   - Convert observations into user needs, business implications, opportunities, risks, and next actions.
   - Mark weak signals and validation needs clearly.
5. **Design the report.**
   - Use compact KPI cards, insight cards, data bars, matrices, timelines, tables, or ranked lists.
   - Keep dense information scannable on desktop and readable on mobile.
6. **Build the HTML.**
   - Use semantic HTML, scoped CSS, and small JavaScript render functions.
   - Keep state simple: tabs, segmented controls, filters, or expandable details.
   - Avoid overengineering.
7. **Verify before delivery.**
   - Check navigation, filters, and secondary switches.
   - Check responsive behavior on mobile and desktop.
   - Check that labels, tables, and buttons do not overflow or overlap.
   - Check that every strong recommendation is supported by visible evidence or marked as a hypothesis.

## Recommended Sections

Pick the subset that fits the task:

- Executive Summary
- Key Metrics
- First-Principles Interpretation
- Segment or Persona View
- Product or Offer View
- Channel or Funnel View
- Competitive or Market View
- Opportunity Map
- Risk and Rebuttal
- Action Roadmap
- Appendix and Data Notes

## Content Pattern

For each important dimension, include as much of this pattern as the evidence supports:

- Core conclusion
- Supporting data
- Interpretation
- Opportunity
- Risk or uncertainty
- Recommended action
- Validation question

Do not force weak data into a confident conclusion. If a dimension has limited evidence, present it as a hypothesis or validation item.

## Visual Style

Use a restrained, professional data-report style:

- Light background with clear hierarchy and readable contrast.
- Cards and controls with border radius of 8px or less.
- Stable dimensions for cards, buttons, bars, tables, and tab panels.
- Concise headings and labels.
- Tables that remain readable on narrow screens.
- Palettes that use contrast and meaning, not decoration.

Avoid:

- Decorative blobs, bokeh, gradient orbs, or oversized hero sections.
- One-note purple, blue, beige, or dark-slate palettes.
- Visible instructional copy explaining how the interface works.
- Text overflow, overlapping content, or buttons that change layout on interaction.
- Charts or visuals that look impressive but do not clarify the decision.

## Interaction Patterns

Prefer simple JavaScript patterns:

- `data-tab` buttons for top-level sections.
- Segmented controls for secondary dimensions.
- Keyed data objects for report content.
- Render functions that update text, tables, bars, and action lists.
- Expandable details for appendices or evidence notes.

Keep interactions predictable. A reader should understand the report without learning a new interface.

## Evidence and Privacy Rules

- Include a data-source note with date range, source names, sample size, and known limitations when available.
- Do not expose private business names, customer data, internal URLs, credentials, or proprietary numbers unless the user explicitly wants them included.
- When preparing a public or shareable report, anonymize brands, people, accounts, and exact figures by default.
- Do not imply statistical confidence when the source is anecdotal, partial, or directional.

## Delivery

Return the path to the generated `index.html`. If the user asks for a shareable link and a publishing workflow is available, publish the static HTML report. If a document companion is requested, create a short document that links to the interactive report instead of trying to embed complex JavaScript in the document.

## Example Prompts

- "Use $interactive-html-insight-report to turn this spreadsheet into an interactive executive report."
- "Create a one-page HTML insight report from these customer interview notes."
- "Turn this market research into a dashboard-style briefing with opportunities, risks, and next actions."
- "Build a shareable HTML report from this campaign review. Infer the sections yourself."
