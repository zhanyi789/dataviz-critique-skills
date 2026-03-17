# Data Visualization Critique Prompt

> A prompt toolkit for critiquing data visualization charts — works with Claude, ChatGPT, Gemini, and any LLM with vision capability.

---

## What is this?

A structured prompt that turns any LLM into a professional data visualization judge. Paste a chart image and get a critique covering design quality, readability, and storytelling — with scores and actionable suggestions.

**Two language versions available:**
- [`prompts/dataviz-critique-zh.md`](prompts/dataviz-critique-zh.md) — Chinese prompt, outputs in Chinese by default
- [`prompts/dataviz-critique-en.md`](prompts/dataviz-critique-en.md) — English prompt, outputs in English by default

Both versions follow the same response language rule: **reply in the user's language; fall back to the prompt's default if unspecified.**

---

## Features

- **Two modes**: single chart or batch PDF report (with cross-chart narrative analysis)
- **Three scoring dimensions**: Visual Design / Readability / Storytelling (1–10 each)
- **Scoring anchors**: defined rubric to prevent score inflation
- **Bias-free scoring**: chart source (NYT, The Economist, etc.) does not affect the score
- **Forced chart type review**: always evaluates whether the chart type fits the data
- **Context-first**: reads any caption or report text before analyzing

---

## Quick Start

**Step 1** — Copy the prompt content

Open [`prompts/dataviz-critique-en.md`](prompts/dataviz-critique-en.md) (or the Chinese version).
- **Claude Code users**: the file works as a Claude skill directly.
- **ChatGPT / Gemini / other LLMs**: copy everything starting from the `# Data Visualization Critique` heading and paste it as a system prompt or at the start of a conversation.

**Step 2** — Paste the prompt into your LLM

**Step 3** — Upload a chart image and start critiquing

---

## Output Format

Each critique follows this structure:

```
[Chart Interpretation]   — What data is shown? What is the key message?
[Design Analysis]        — Chart type, visual design, readability, storytelling
[Score]                  — Visual Design: X/10 / Readability: X/10 / Storytelling: X/10
[Things to Learn]        — 1–2 design techniques worth borrowing
[Suggestions]            — 1–3 specific, actionable improvements
```

For batch mode (PDF with multiple charts), each chart is critiqued in sequence, followed by a **Report Narrative Analysis** covering:
- Narrative coherence diagnosis (Strong / Partial / Weak — with diagnosis if weak)
- Narrative arc (Hook → Development → Conclusion, or breakdown analysis if incoherent)
- Visual consistency across charts (color semantics, axis alignment, annotation strategy)
- One-liner narrative summary
- Ghost data (what's missing that would change the story)

---

## Examples

See the [`examples/`](examples/) directory for real input/output samples.
- [`examples/en/`](examples/en/) — outputs from the English prompt
- [`examples/zh/`](examples/zh/) — outputs from the Chinese prompt

---

## License

MIT — free to use, modify, and share. See [LICENSE](LICENSE).

---
---

# 資料視覺化圖表賞析 Prompt 工具庫

> 跨 LLM 通用的圖表賞析 prompt，支援 Claude、ChatGPT、Gemini 及任何具備視覺辨識能力的 LLM。

---

## 這是什麼？

一個結構化 prompt，讓任何 LLM 化身為資料視覺化競賽評審。貼上圖表圖片，即可獲得涵蓋設計品質、易讀性與故事性的完整賞析——附評分與具體改善建議。

**提供兩個語言版本：**
- [`prompts/dataviz-critique-zh.md`](prompts/dataviz-critique-zh.md) — 中文版，預設輸出中文
- [`prompts/dataviz-critique-en.md`](prompts/dataviz-critique-en.md) — 英文版，預設輸出英文

兩個版本均遵循相同的輸出語言規則：**以使用者輸入的語言回覆；若未指定，使用該版本的預設語言。**

---

## 功能特色

- **兩種模式**：單張圖表 / 批次 PDF 報告（含跨圖敘事評析）
- **三維度評分**：視覺設計 / 易讀性 / 故事性（各 1–10 分）
- **評分錨點**：有明確定義防止評分膨脹
- **評分無偏見**：不因圖表來源（NYT、《經濟學人》等）而調整分數
- **強制圖表類型評論**：每次賞析都評估圖表類型是否適合該資料
- **上下文優先**：有說明文字或報告文字時，先讀再分析

---

## 快速開始

**第一步** — 複製 prompt 內容

開啟 [`prompts/dataviz-critique-zh.md`](prompts/dataviz-critique-zh.md)（或英文版）。
- **Claude Code 使用者**：此文件可直接作為 Claude skill 使用。
- **ChatGPT / Gemini / 其他 LLM**：從 `# 資料視覺化圖表賞析` 標題開始複製，貼入 system prompt 或對話開頭。

**第二步** — 將 prompt 貼入你的 LLM

**第三步** — 上傳圖表圖片，開始賞析

---

## 輸出格式

每份賞析包含以下區塊：

```
【圖表解讀】   — 呈現什麼數據？核心訊息是什麼？
【設計分析】   — 圖表類型、視覺設計、易讀性、故事性
【評分】       — 視覺設計 X/10 / 易讀性 X/10 / 故事性 X/10
【可以學習的地方】 — 1–2 個值得借鑒的設計手法
【改善建議】   — 1–3 個具體可執行的改善方向
```

批次模式（含多張圖的 PDF）會依序賞析每張圖，最後輸出**報告敘事評析**，包含：
- 敘事連貫性診斷（強／部分／薄弱，薄弱時說明缺失原因）
- 敘事弧線（Hook → Development → Conclusion，或不連貫時的斷點分析）
- 視覺一致性（色彩語意、時間軸縮放、標注策略）
- 一句話敘事摘要
- 缺席的數據（Ghost Data）

---

## 範例

參見 [`examples/`](examples/) 目錄，包含真實的輸入圖表與 AI 輸出範例。
- [`examples/zh/`](examples/zh/) — 中文版 prompt 的輸出
- [`examples/en/`](examples/en/) — 英文版 prompt 的輸出

---

## 授權

MIT 授權 — 可自由使用、修改與分享。詳見 [LICENSE](LICENSE)。
