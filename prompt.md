# The Prompt

Copy everything inside the code block below, fill in the **Client Inputs**, and paste it into your AI agent.

> Tip: fill the inputs using [`templates/client-inputs.md`](templates/client-inputs.md), or see a worked example in [`examples/example-inputs.md`](examples/example-inputs.md).

```text
You are a senior SEO, AEO and GEO consultant. Do a complete SEO audit and strategy for the business below, then deliver everything in ONE Excel workbook (.xlsx).

==================================================
1. CLIENT INPUTS (fill in before running)
==================================================
Business name (exact, full):       [--------------]
Brand name to use in content:      [--------------]
Website:                           [--------------]
Business location (city, state):   [--------------]
Target service area:               [--------------]
Country / search database:         [--------------]
Customer types:                    [--------------]
Primary audience:                  [--------------]
Typical budget / job size:         [--------------]
Primary service (priority 1):      [--------------]
Secondary service (priority 2):    [--------------]
Other services:                    [--------------]
Services NOT offered:              [--------------]
Known competitors:                 [--------------]
Brand-name collisions to watch:    [--------------]
Existing assets:                   [--------------]
Connected tools to use:            [--------------]

If an input is missing, check the website, uploaded files and connected tools first. Ask me only for what you truly can't find.

==================================================
2. RULES
==================================================
- Use live data. Crawl the site with an audit tool, read real pages, and pull keyword, competitor and SERP data from the connected SEO tool. Run SERP checks at city level (the business's city), not just country level.
- Never invent numbers. If something can't be measured (quota limit, no access), mark it "Check" and give the manual step.
- Cite the source and date for every data table (tool name, database, audit ID, date).
- Keep the client's priorities: primary service first, secondary second, primary audience first.
- Flag any content that promotes services the client doesn't offer.
- Write in the client's local English (e.g. Australian English).

==================================================
3. WORK TO DO
==================================================

A. BUSINESS PROFILE
Capture from the site and inputs: name, ABN/registration, phone, email, hours, address, service area, years in business, USPs, guarantees, brands/systems used, sectors, testimonials, projects, process steps. Mark which facts came from the client and which from the site.

B. TECHNICAL AUDIT – run every test below; status = Pass / Warning / Fail / Check
1. Redirection (www / non-www, http → https, single hop)
2. HTTPS (certificate, mixed content, HTTP URLs in sitemap)
3. Amount of content (word count per page; flag pages under 600 words)
4. Title tags (missing, duplicate, over 65 chars, broken or truncated)
5. Meta descriptions (missing, duplicate, over 158 chars)
6. Favicon
7. Robots.txt (valid, sitemap listed, AI crawlers allowed)
8. Schema (type, NAP, geo, areaServed, sameAs, aggregateRating, Service, FAQ, Article, Breadcrumb)
9. Twitter Card tags
10. Open Graph tags
11. Sitemap.xml (all URLs 200, canonical, indexable)
12. Responsive / mobile (viewport, lang)
13. Images (alt text, WebP, lazy loading, oversized files)
14. Header tags (one H1 per page, keyword in H1, H2 structure)
15. Nofollow tags (internal and external)
16. Social links on site and in schema sameAs
17. Google Search Console (verification, indexed pages, sitemap submitted)
18. Google Analytics / GTM installed, conversion events
19. Site loading speed (TTFB, load time)
20. Custom 404 page (real 404 status, branded, noindex)
21. SEO-friendly URLs
22. AI optimisation readiness (see sections H–J)
23. LLMs.txt (/llms.txt and /llms-full.txt)
24. Website speed – PageSpeed Insights mobile and desktop, Core Web Vitals (LCP, INP, CLS)
Also check: broken internal links (4xx), internal links to redirects, broken external links, canonical issues, orphan pages, indexation count, JS counters or content that renders as "0" in the raw HTML, and navigation links that break on sub-pages.

C. PAGE-BY-PAGE ON-PAGE AUDIT
For EVERY URL in the sitemap: URL, page type, title, title length, meta description, description length, H1, H1 length, word count, primary keyword it targets, and the issue and fix. Flag keyword cannibalisation (two pages targeting the same keyword) and off-strategy pages.

D. SERVICE AREA ACCURACY CHECK
Scan every page and the schema for place names. Flag:
- areas described wrongly (e.g. a separate city called a suburb or called "metro")
- suburbs listed in two regions, or in the wrong region
- council names used as suburb names
- interstate or out-of-area mentions that suggest the business serves there
- generic "[country] homes" content with no local angle
- important suburbs or regions that are missing
Give the correct wording for each.

E. OFF-PAGE AUDIT
Backlink profile (referring domains, authority, anchors, toxic links); Google Business Profile (category, reviews, rating, photos, posts, NAP match); citations and directories (local trade directories, review sites, hipages/Supertrades/ProductReview-style sites, Yellow Pages, Houzz); NAP consistency; review count compared with competitors; brand mentions; link-building opportunities and quick wins.

F. COMPETITOR AUDIT
Find the top 8–10 competitors from the city-level SERP for the main money keyword, plus the known competitors and any businesses named in AI answers. For each: domain, rating, review count, ranking keywords, top-10 keywords, positions 11–20, estimated traffic, traffic value, rank for the main keyword, number of service and location pages, blog yes/no, schema, llms.txt, AI citations, strengths, weaknesses and gaps. Then list each competitor's top 5–10 target keywords (keyword, position, volume, difficulty, ranking URL) and flag the ones the client can realistically win.

G. KEYWORD RESEARCH MAPPED TO URLS
Build a keyword map that assigns every keyword to ONE target URL (home, each service page, each area page, blogs, and new pages to create). Columns: page, URL, role (Primary/Secondary), keyword, volume, difficulty, CPC, intent, current position, difficulty band. Include service + city, service + suburb, cost, comparison, "near me" and question keywords. Mark gaps where a new page is needed.

H. AEO (Answer Engine Optimisation)
- Find the questions people ask (People Also Ask, question keywords, forums).
- Check whether each key page opens with a 40–60 word direct answer.
- Check FAQ blocks and FAQPage schema.
- Check for tables, lists, steps and real numbers (prices, timeframes, specs).
- Find featured snippet opportunities and say which page should win each one.
- List the FAQs to add, page by page.

I. GEO (Generative Engine Optimisation)
- Entity consistency: same name, NAP and description everywhere.
- Schema sameAs links to GBP and social profiles.
- llms.txt present and accurate.
- AI crawlers (GPTBot, ClaudeBot, PerplexityBot, Google-Extended) allowed in robots.txt.
- Brand-collision risk with similarly named businesses.
- E-E-A-T signals: author, real job stories, photos, licences, years in business.
- Presence on the sources AI tools cite (directories, review sites, "best of" lists, industry bodies).
- Citable content: original data, local specifics, clear definitions.

J. AI VISIBILITY CHECK
- Use the SEO tool's AI search data (e.g. SE Ranking AI Search Overview, prompts by target or brand) for AI Overviews, AI Mode, ChatGPT, Perplexity and Gemini.
- Report: brand presence, link presence, number of prompts citing the domain, average position, and competitor comparison (AI share of voice).
- List 20–30 realistic prompts the audience would type into AI tools (best [service] in [city], cost, comparisons, problems). For each, record who is mentioned or cited now, whether the client appears, and which page should win it.
- If I uploaded screenshots of AI answers, extract the businesses, ratings and sources shown.
- Note which third-party sources the AI answers rely on, and how the client can get listed there.

K. ISSUES, FIXES AND ACTION PLAN
Combine all findings into one prioritised list (High / Medium / Low / Info) with the exact fix. Then write a 90-day action plan: quick wins (week 1–2), month 1, month 2, month 3, each with an owner (dev / content / client) and the expected impact.

==================================================
4. EXCEL OUTPUT (one .xlsx file)
==================================================
Tabs, in this order:
1. Summary – key numbers, client inputs, health score, checklist counts (formulas), top 5 fixes
2. Business Profile – field, detail, source (client inputs highlighted)
3. Audit Checklist – #, test, status, finding, fix; Pass/Warning/Fail/Check colour-coded; count and score formulas
4. Page Meta Audit – all pages; length columns as LEN() formulas; red when title > 65, description > 158, H1 missing, words < 600
5. Area Check – where, what the site says, status (Correct/Wrong/Check/Gap), fix
6. On-Page Issues – page-level fixes
7. Off-Page – backlinks, GBP, citations, reviews, link opportunities
8. Competitor Audit – metrics table + averages (formulas) + client as % of average
9. Competitor Keywords – with an "Opportunity?" formula (competitor in top 10 AND difficulty ≤ 20)
10. Keyword Map – keywords by URL, difficulty band formula, totals by cluster
11. AEO – question, target page, current answer status, FAQ to add, snippet opportunity
12. GEO – check, status, finding, fix
13. AI Visibility – metrics by engine + prompt table (prompt, intent, who appears now, client visible Y/N, target page, action) + visibility score formula
14. Issues & Fixes – prioritised
15. 90-Day Action Plan
16. Open Questions – things the client must confirm

Formatting: Arial font, header row filled, frozen header, filters, wrapped text, sensible column widths, alternating row shading. Use formulas for counts, lengths, averages and scores (no hardcoded totals). Recalculate and check for zero formula errors before delivering. Put the data source and date under each tab title.

==================================================
5. FINAL REPLY
==================================================
After the file, give me a short summary: health score, the 5 biggest problems, the 3 quickest wins, where the client stands against competitors and in AI answers, and anything you couldn't check (with the manual step).
```
