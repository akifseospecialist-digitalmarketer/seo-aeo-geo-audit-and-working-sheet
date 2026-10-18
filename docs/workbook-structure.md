# Workbook Structure

Every tab the prompt asks for, with its columns, formulas and formatting rules.

**Applies to all tabs**

- Row 1: tab title. Row 2: data source and date (tool name, database, audit ID, date).
- Header row filled, frozen, with filters on.
- Arial font, wrapped text, sensible column widths, alternating row shading.
- Counts, lengths, averages and scores are formulas — never hardcoded.
- Workbook is recalculated and checked for zero formula errors before delivery.

---

## 1. Summary

| Section | Contents |
|---------|----------|
| Client inputs | All fields from the inputs block |
| Key numbers | Pages crawled, indexed pages, referring domains, domain authority, ranking keywords, GBP rating and reviews |
| Health score | Formula pulled from the Audit Checklist score |
| Checklist counts | `COUNTIF` of Pass / Warning / Fail / Check from the Audit Checklist |
| Top 5 fixes | Highest-priority items from Issues & Fixes |

## 2. Business Profile

| Column | Notes |
|--------|-------|
| Field | Name, ABN/registration, phone, email, hours, address, service area, years in business, USPs, guarantees, brands/systems, sectors, testimonials, projects, process steps |
| Detail | The value found |
| Source | `Client` or `Site` (client-supplied rows highlighted) |

## 3. Audit Checklist

| Column | Notes |
|--------|-------|
| # | 1–24, plus extra checks (broken links, canonicals, orphans, etc.) |
| Test | Name of the check |
| Status | Pass / Warning / Fail / Check — conditional colour |
| Finding | What was found, with numbers |
| Fix | Exact action |

**Formulas:** counts per status, and a score, e.g. `(Pass + 0.5 × Warning) / (Total − Check)`.

The 24 tests: redirection, HTTPS, amount of content, title tags, meta descriptions, favicon, robots.txt, schema, Twitter Card, Open Graph, sitemap.xml, responsive/mobile, images, header tags, nofollow, social links, Google Search Console, GA/GTM, loading speed, custom 404, SEO-friendly URLs, AI optimisation readiness, llms.txt, PageSpeed/Core Web Vitals.

## 4. Page Meta Audit

| Column | Notes |
|--------|-------|
| URL | Every URL in the sitemap |
| Page type | Home, service, area, blog, contact, etc. |
| Title | |
| Title length | `=LEN(C3)` — red if > 65 |
| Meta description | |
| Description length | `=LEN(E3)` — red if > 158 |
| H1 | Red if missing |
| H1 length | `=LEN(G3)` |
| Word count | Red if < 600 |
| Primary keyword | The keyword the page targets |
| Issue / Fix | Including cannibalisation and off-strategy flags |

## 5. Area Check

| Column | Notes |
|--------|-------|
| Where | Page URL or schema property |
| What the site says | Exact wording |
| Status | Correct / Wrong / Check / Gap |
| Fix | Correct wording |

## 6. On-Page Issues

Page-level fixes: page, issue, priority, fix, owner.

## 7. Off-Page

Sections for backlink profile (referring domains, authority, anchors, toxic links), Google Business Profile (category, reviews, rating, photos, posts, NAP match), citations and directories, NAP consistency, review comparison, brand mentions, and link opportunities / quick wins.

## 8. Competitor Audit

| Column | Notes |
|--------|-------|
| Domain | Client row first, then 8–10 competitors |
| Rating / Reviews | GBP |
| Ranking keywords / Top-10 / Positions 11–20 | |
| Est. traffic / Traffic value | |
| Rank for main keyword | City-level SERP |
| Service pages / Location pages | |
| Blog / Schema / llms.txt / AI citations | Yes/No or count |
| Strengths / Weaknesses / Gaps | |

**Formulas:** `AVERAGE` row for competitors, and a "client as % of average" row.

## 9. Competitor Keywords

| Column | Notes |
|--------|-------|
| Competitor | |
| Keyword | Top 5–10 per competitor |
| Position / Volume / Difficulty | |
| Ranking URL | |
| Opportunity? | `=IF(AND(C3<=10, E3<=20), "Yes", "No")` |

## 10. Keyword Map

| Column | Notes |
|--------|-------|
| Page / URL | Existing page or "NEW – [proposed page]" |
| Role | Primary / Secondary |
| Keyword | Each keyword appears once |
| Volume / Difficulty / CPC | |
| Intent | Informational / Commercial / Transactional / Navigational |
| Current position | |
| Difficulty band | `=IF(F3<=20,"Easy",IF(F3<=40,"Medium","Hard"))` |

**Totals by cluster** with `SUMIF` / `COUNTIF`.

## 11. AEO

Question, target page, current answer status (direct 40–60 word answer yes/no), FAQ to add, snippet opportunity.

## 12. GEO

Check, status, finding, fix — entity consistency, `sameAs`, llms.txt, AI crawler access, brand collision, E-E-A-T, presence on cited sources, citable content.

## 13. AI Visibility

**Metrics by engine:** AI Overviews, AI Mode, ChatGPT, Perplexity, Gemini — brand presence, link presence, prompts citing domain, average position, share of voice.

**Prompt table:** prompt, intent, who appears now, client visible (Y/N), target page, action.

**Formula:** visibility score = `COUNTIF(visible,"Y") / COUNTA(prompts)`.

## 14. Issues & Fixes

Every finding combined: #, area, issue, priority (High / Medium / Low / Info), fix, owner, effort.

## 15. 90-Day Action Plan

Phase (Week 1–2 quick wins / Month 1 / Month 2 / Month 3), task, owner (dev / content / client), expected impact.

## 16. Open Questions

Question, why it matters, who answers it, status.
