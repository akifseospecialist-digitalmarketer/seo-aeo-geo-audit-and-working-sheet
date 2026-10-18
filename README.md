# SEO-AEO-GEO Audit and Working Sheet

**One prompt → a full SEO, AEO and GEO audit → one Excel working sheet.**

A single, copy-paste prompt that turns an AI agent (Claude, ChatGPT, or any agent with tool access) into a senior SEO consultant. It runs a full **SEO, AEO (Answer Engine Optimisation) and GEO (Generative Engine Optimisation)** audit and strategy for a local service business, and delivers everything in **one formatted Excel workbook with 16 tabs**.

Built for agencies and freelancers who audit local businesses and want consistent, data-backed deliverables every time.

---

## What you get

One `.xlsx` file with these tabs:

| # | Tab | What's in it |
|---|-----|--------------|
| 1 | Summary | Key numbers, client inputs, health score, checklist counts, top 5 fixes |
| 2 | Business Profile | NAP, ABN, hours, USPs, guarantees, sectors — with source per field |
| 3 | Audit Checklist | 24 technical tests, Pass / Warning / Fail / Check, score formulas |
| 4 | Page Meta Audit | Every sitemap URL — titles, descriptions, H1s, word counts, `LEN()` formulas |
| 5 | Area Check | Service-area accuracy: wrong suburbs, regions, out-of-area mentions |
| 6 | On-Page Issues | Page-level fixes |
| 7 | Off-Page | Backlinks, Google Business Profile, citations, reviews, link opportunities |
| 8 | Competitor Audit | 8–10 competitors from the city-level SERP, averages, client vs average |
| 9 | Competitor Keywords | Competitor targets with an "Opportunity?" formula |
| 10 | Keyword Map | Every keyword mapped to one URL, difficulty bands, cluster totals |
| 11 | AEO | Questions, direct-answer status, FAQs to add, snippet opportunities |
| 12 | GEO | Entity consistency, schema `sameAs`, llms.txt, AI crawlers, E-E-A-T |
| 13 | AI Visibility | Presence in AI Overviews, AI Mode, ChatGPT, Perplexity, Gemini + 20–30 prompts |
| 14 | Issues & Fixes | Everything combined and prioritised (High / Medium / Low / Info) |
| 15 | 90-Day Action Plan | Quick wins, month 1–3, owner and expected impact |
| 16 | Open Questions | Things the client must confirm |

Full column-by-column breakdown: [`docs/workbook-structure.md`](docs/workbook-structure.md)

---

## Quick start

1. Open [`prompt.md`](prompt.md) and copy the prompt (use the copy button on the code block).
2. Fill in the **Client Inputs** block. A blank template is in [`templates/client-inputs.md`](templates/client-inputs.md) and a filled-in example is in [`examples/example-inputs.md`](examples/example-inputs.md).
3. Paste it into an AI agent that has the tools listed below connected.
4. Upload any extras you have (screenshots of AI answers, GBP exports, past reports).
5. Get back the workbook plus a short summary: health score, top 5 problems, 3 quickest wins, competitive position and anything that couldn't be checked.

Missing inputs are fine — the prompt tells the agent to check the website, uploaded files and connected tools first, and only ask you for what it truly can't find.

---

## Requirements

The prompt is built around **live data, not guesses**. For best results the agent needs:

| Need | Examples |
|------|----------|
| Site crawler / audit tool | SE Ranking Website Audit, Screaming Frog, Sitebulb |
| Keyword, competitor and SERP data | SE Ranking, Semrush, Ahrefs, DataForSEO |
| AI search visibility data | SE Ranking AI Search / AI Results Tracker, or manual checks |
| Web fetch | To read real pages, robots.txt, sitemap.xml, llms.txt |
| Spreadsheet generation | Code execution with `openpyxl` (or equivalent) to build the `.xlsx` |
| Optional | Google Search Console, GA4, PageSpeed Insights, GBP access |

If a tool isn't available, the agent marks that item **"Check"** and gives you the manual step — it never invents numbers.

Tested with Claude (with an SEO MCP connector and code execution). Should work with any capable agent that has equivalent tools.

---

## Key rules baked into the prompt

- **Live data only.** Crawl the site, read real pages, pull real keyword and SERP data.
- **City-level SERPs**, not just country level — critical for local businesses.
- **No invented numbers.** Unmeasurable items are marked "Check" with a manual step.
- **Every table cites its source and date** (tool, database, audit ID, date).
- **Client priorities first** — primary service, then secondary, primary audience first.
- **Flags content for services the client doesn't offer.**
- **Writes in the client's local English** (e.g. Australian English).
- **Formulas, not hardcoded totals**, and zero formula errors before delivery.

---

## Customising

- **Different country:** change *Country / search database* and the local English rule. Swap the directory examples in section E (hipages, Supertrades, ProductReview) for local equivalents (e.g. Checkatrade/Trustpilot in the UK, Angi/Yelp in the US, JustDial/Sulekha in India).
- **Non-local business:** drop section D (Service Area Accuracy) and the city-level SERP rule.
- **Lighter audit:** remove tabs you don't need from section 4 — but keep section 3 K (Issues & Action Plan), which pulls everything together.
- **Different thresholds:** adjust title (65 chars), description (158 chars) and thin content (600 words) in sections B and 4.

---

## Repo structure

```
.
├── README.md                  ← you are here
├── prompt.md                  ← the full prompt (copy this)
├── templates/
│   └── client-inputs.md       ← blank inputs block
├── examples/
│   └── example-inputs.md      ← filled-in example (fictional business)
├── docs/
│   └── workbook-structure.md  ← every tab and column explained
├── .github/
│   └── ISSUE_TEMPLATE/
│       └── improvement.md     ← issue template
├── .gitignore                 ← keeps client .xlsx/.csv files out of the repo
├── CHANGELOG.md
├── CONTRIBUTING.md
└── LICENSE
```

---

## Contributing

Improvements welcome — new checks, better thresholds, country-specific directory lists, or results from other AI agents. See [`CONTRIBUTING.md`](CONTRIBUTING.md).

## License

[MIT](LICENSE) — free to use, modify and share, including for client work.
