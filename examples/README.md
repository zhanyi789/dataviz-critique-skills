# Examples

Real input/output samples showing what this prompt produces.

## Directory Structure

```
examples/
├── zh/          — outputs from the Chinese prompt (dataviz-critique-zh.md)
│   └── single-chart/
│       └── 01-<chart-type>/
│           ├── input.png    ← the chart image used as input
│           └── output.md   ← the AI's critique output
└── en/          — outputs from the English prompt (dataviz-critique-en.md)
    └── single-chart/
        └── 01-<chart-type>/
            ├── input.png
            └── output.md
```

## Naming Convention

- Folders: `01-bar-chart`, `02-line-chart`, `03-scatter-plot`, etc.
- `input.png` — screenshot of the chart you submitted
- `output.md` — paste the full AI response here

## output.md Format

Each `output.md` should start with a metadata header:

```markdown
---
chart_type: bar chart
llm: Claude Sonnet 4.6
prompt_version: 1.1.0
date: YYYY-MM-DD
source: [chart source or "original"]
---

[paste AI output below]
```

## Contributing

Contributions welcome! If you've run this prompt on an interesting chart, feel free to open a PR with your example (both `input.png` and `output.md`).
