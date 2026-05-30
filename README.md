<div align="center">

# BetterScholar

**轻量级 Google Scholar 检索增强用户脚本**  
*Lightweight Google Scholar userscript for result sorting, source tagging, and page-level filtering.*

![Type](https://img.shields.io/badge/type-Tampermonkey%20Userscript-blue?style=flat-square)
![Domain](https://img.shields.io/badge/domain-literature%20search-green?style=flat-square)
![Architecture](https://img.shields.io/badge/architecture-page--native-purple?style=flat-square)
![License](https://img.shields.io/badge/license-MIT-yellow?style=flat-square)

Part of **ResearchFlow Lab** — a local-first research productivity ecosystem for literature, manuscripts, data, and scientific visualization.

</div>

---

## 01. Overview

**BetterScholar** is a lightweight Tampermonkey userscript that improves the Google Scholar result page without replacing its native interface. It adds page-level sorting, publication-year extraction, source tagging, and publisher/database filtering.

**BetterScholar** 是一个轻量级 Google Scholar 增强脚本，适合在当前检索结果页快速做“微观筛选”：按引用量、年份和来源初步判断文献价值。

---

## 02. Why this project exists

Google Scholar is powerful, but its result page is intentionally minimal. Researchers often need quick local filtering by year, citation count, publisher, database, or source type. BetterScholar adds these controls directly to the existing Google Scholar page while keeping the original reading experience intact.

核心目标：

- Keep the Google Scholar interface lightweight and familiar.
- Add useful local sorting and filtering without external services.
- Help researchers screen papers faster on the current result page.
- Serve as a minimal userscript counterpart to PaperPilot Pro.

---

## 03. Key features

| Module | What it does | 中文说明 |
|---|---|---|
| Citation Sorting | Sorts currently loaded results by citation count | 按当前页引用量排序 |
| Year Sorting | Sorts currently loaded results by publication year | 按当前页发表年份排序 |
| Source Tagging | Extracts and displays publisher/database labels | 自动提取并显示出版商或数据库标签 |
| Sidebar Filtering | Filters visible results by publisher or database | 通过侧边栏按来源筛选结果 |
| Native UI Style | Uses Google Scholar-like visual language | 尽量保持 Google Scholar 原生视觉风格 |
| Reset Control | Restores default result order | 一键恢复默认排序 |

---

## 04. Product philosophy

BetterScholar follows four design principles:

1. **Minimal intervention** — enhance the page without visually overwhelming it.
2. **Current-page scope** — keep behavior transparent and limited to loaded results.
3. **No server dependency** — run entirely in the browser userscript context.
4. **Fast screening** — help users decide what to open, save, or ignore.

---

## 05. Architecture

```text
Google Scholar Page
    ↓
BetterScholar Userscript
├── result parser
├── citation and year extractor
├── publisher/source tagger
├── sorting controls
├── sidebar filter controls
└── native-style UI injection
```

---

## 06. Quick start

1. Install a userscript manager such as **Tampermonkey**.
2. Install the BetterScholar userscript from the release/source script.
3. Open Google Scholar and perform a search.
4. Use the injected sorting and filtering controls on the result page.

Manual installation:

```bash
git clone https://github.com/groele/BetterScholar.git
```

Then copy the userscript content into Tampermonkey.

---

## 07. Recommended workflow

```text
Search topic on Google Scholar → Sort by citations / year
                               → Filter by source
                               → Open promising results
                               → Save important papers to PaperPilot / ResearchFlow / Zotero
```

Typical use cases:

- Quickly screen the first page of Google Scholar results.
- Identify high-citation papers on the loaded page.
- Remove irrelevant databases or source types.
- Use as a lightweight alternative when a full extension is unnecessary.

---

## 08. Limitations

BetterScholar only processes the **currently loaded Google Scholar result page**. It does not perform global ranking across all search results because Google Scholar does not provide an official full-result sorting API.

For more advanced literature workflows, use **PaperPilot Pro** or **ResearchFlow Companion**.

---

## 09. Roadmap

- [ ] Improve source detection across more Scholar domains
- [ ] Add configurable source groups
- [ ] Add export of visible result metadata
- [ ] Add integration notes for PaperPilot Pro
- [ ] Add safer handling for Google Scholar layout changes

---

## 10. Privacy and data ownership

BetterScholar runs locally in the browser userscript context. It does not require a backend server. Result parsing happens on the visible Google Scholar page.

---

## 11. Related projects

- **PaperPilot Pro** — full academic search and publisher-page enhancement
- **ResearchFlow Companion** — research workflow operating system
- **ClipNote** — browser-native quick notes and Markdown capture
- **ManuGuide** — Microsoft Word manuscript formatting and style checker

---

## 12. License

MIT License.

Developed by **Shikun Hou / groele**.
