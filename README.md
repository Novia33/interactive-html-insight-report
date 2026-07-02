# Interactive HTML Insight Report

A Codex skill for turning messy analysis, datasets, research notes, or business reviews into polished single-file interactive HTML reports.

This is not a chart template. It is a reporting workflow that helps an AI agent infer useful dimensions, separate evidence from interpretation, add adversarial review, and produce a lightweight report that people can actually read.

## What It Creates

The skill guides Codex to create a self-contained `index.html` report with:

- Sticky navigation and sectioned analysis.
- KPI cards, compact tables, data bars, matrices, or timelines.
- Secondary controls for comparing segments, personas, products, channels, regions, or other inferred dimensions.
- First-principles interpretation of the underlying decision or problem.
- Opportunity, risk, and action sections.
- Evidence notes that preserve source limits, dates, sample sizes, and uncertainty.

The generated report uses plain HTML, CSS, and vanilla JavaScript by default. It does not require a server, framework, CDN, or BI platform.

## Why This Exists

Many data reports fail because they are either too static, too long, too raw, or too heavy:

- Spreadsheets show data but hide the story.
- Slide decks look clean but flatten the exploration.
- BI dashboards are powerful but often too much work for one-off insight sharing.
- Long documents explain everything but are hard to scan.

This skill aims for a middle path: a single interactive report that is readable, evidence-aware, and action-oriented.

## Good Use Cases

- Executive summaries from spreadsheets or CSV files.
- Customer research and interview synthesis.
- Market or competitor analysis.
- Campaign, funnel, or channel reviews.
- Product feedback reports.
- Operational retrospectives.
- Strategy memos that need visual evidence and clear next steps.

## Not For

- Real-time dashboards with live data pipelines.
- Production analytics applications.
- Highly customized charting systems.
- Reports that require confidential data to be published without review.

## Installation

Copy this folder into your Codex skills directory:

```bash
~/.codex/skills/interactive-html-insight-report
```

Then invoke it in Codex:

```text
Use $interactive-html-insight-report to turn this dataset into an interactive executive report.
```

## Example Prompt

```text
Use $interactive-html-insight-report to turn these campaign notes into a single-page HTML report.
Infer the most useful sections, include opportunities and risks, and keep the output shareable.
```

## Design Philosophy

The skill follows four principles:

1. **Insight over decoration.** Every visual should clarify a decision.
2. **Useful structure over user micromanagement.** The agent should infer the right dimensions when the user does not know what to ask for.
3. **Evidence before confidence.** Strong claims need visible support; weak signals should be labeled as hypotheses.
4. **Simple files over heavy systems.** A single HTML file is often enough to communicate the point.

## Privacy Note

When preparing a public or shareable report, anonymize private brands, people, internal URLs, customer data, and exact proprietary figures by default. Keep sensitive business logic in a private fork or private skill variant.

## Repository Structure

```text
interactive-html-insight-report/
  SKILL.md
  agents/
    openai.yaml
  examples/
    sample-input.md
    sample-report.html
  LICENSE
```

## License

MIT
