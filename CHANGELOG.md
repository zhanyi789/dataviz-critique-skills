# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/).

---

## [1.1.0] - 2026-03-16

### Added
- Batch mode: prompt now asks the user to confirm the total chart count before scanning, then cross-checks to prevent missed charts
- English version of the prompt (`dataviz-critique-en.md`)
- [Things to Learn] section in output format (1–2 design techniques worth borrowing)
- Version number annotation at the top of each prompt file
- Output language rule: reply in user's language; fall back to prompt default if unspecified

### Changed
- Batch mode flow upgraded from "AI self-counts" to "user confirms count → AI scans → cross-check"

---

## [1.0.0] - 2026-02-01

### Added
- Initial release: single-chart critique mode
- Three scoring dimensions: Visual Design / Readability / Storytelling (1–10 each)
- Scoring anchors to prevent score inflation
- Bias-free scoring principle (chart source does not affect score)
- Mandatory chart type review in every critique
- Context-first principle (reads captions/report text before analyzing)
- Cross-LLM compatibility: prompt works with Claude, ChatGPT, Gemini, and other LLMs
