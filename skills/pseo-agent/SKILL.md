# StorX Programmatic SEO Agent (pSEO)

## When to Use This Skill
Use this skill when you want to generate programmatic SEO pages 
for storx.io at scale — including competitor comparisons, 
integration pages, migration guides, industry pages, glossary 
pages, file type pages, and pricing alternative pages.

Always read `skills/storx-marketing-context/SKILL.md` first 
before running this skill.

---

## What This Tool Is

The StorX pSEO Agent is a local AI content factory that generates 
190 publication-ready SEO pages for storx.io. It runs a 5-stage 
pipeline for every page and produces output in Word, HTML, JSON, 
or plain text format.

**Local URL:** http://localhost:3000 (current)  
**Production URL:** https://pseo.storx.io (coming soon — pending deployment)  
**Current Status:** 🔄 Running locally — live server deployment in progress
**Total pages it can generate:** 190 across 9 templates

---

## The 190 Pages It Generates

| Template | Pages | URL Pattern | Funnel Stage |
|---|---|---|---|
| Competitor comparisons | 17 | `/compare/storx-vs-[competitor]` | Bottom |
| Integration pages | 46 | `/integrations/[tool]` | Bottom |
| Migration guides | 46 | `/migrate/[tool]-to-storx` | Bottom |
| Use case comparisons | 12 | `/compare/[use-case]` | Mid |
| Glossary and education | 15 | `/learn/[concept]` | Top |
| Industry pages | 10 | `/for/[industry]` | Mid |
| File type pages | 10 | `/store/[filetype]` | Mid |
| Pricing alternatives | 17 | `/pricing/[slug]-alternative` | Bottom |
| Alternatives list | 17 | `/alternatives/[slug]` | Mid-Bottom |

---

## Step 1 — Starting the Agent

Open your terminal
Navigate to the storx-v2 folder
Run: node server.js
Open your browser and go to: http://localhost:3000


The dashboard will load with all 9 templates in the left sidebar.

---

## Step 2 — Generating Pages

1. Click any template from the left sidebar
2. Tick the items you want to generate
3. Click **GENERATE**
4. Watch the 5-stage pipeline run in the logs panel
5. Click **PREVIEW** to see the rendered content
6. Click **↓ DOWNLOAD** to export

**Download formats available:**
- **Word (.doc)** — opens in Microsoft Word and LibreOffice
- **HTML** — clean standalone page ready for CMS
- **JSON** — structured data for developer handoff
- **Plain text** — for copy-pasting into any CMS

---

## Step 3 — The 5-Stage Pipeline Explained

Every page runs through these 5 stages automatically:

**Stage 1 — Keywords**
Builds keyword intelligence for that specific page:
primary keyword, secondary keywords, competitor gaps, 
trending terms, FAQ questions, and content angle.
No API call needed — uses built-in keyword database.

**Stage 2 — Research**
For competitor pages: fetches live pricing from the 
competitor's pricing page.
For all other templates: loads data from the built-in 
database.

**Stage 3 — Generate**
Calls Claude AI with a structured prompt.
Returns a complete page as a JSON object.
Auto-retries if rate limited.

**Stage 4 — Humanise**
Scans 50+ AI writing patterns 
(words like "delve", "seamlessly", "game-changer" etc.)
Rewrites any flagged sections automatically.
This ensures content does not read like AI output.

**Stage 5 — Quality Gate**
Runs a 14-18 point checklist specific to each template.
Checks: title length, word counts, pricing accuracy, 
CTA links, banned words, and required sections.
Returns: PASS / PARTIAL / FAIL with specific details.

Only PASS pages should be published. 
PARTIAL pages need a human review before publishing.
FAIL pages need to be regenerated.

---

## Step 4 — Which Templates to Generate First

Build pages in this priority order — highest buyer intent first:

### Priority 1 — Bottom Funnel (Generate First)
These pages capture buyers who are actively ready to switch.

**Competitor Comparisons (17 pages)**
Generates one page per competitor.
URL pattern: `/compare/storx-vs-[competitor]`
These are your highest-converting pages.
Competitors covered: AWS S3, Google Cloud, Azure, Backblaze, 
Storj, Filecoin, MEGA, Internxt, Proton Drive, Tresorit, 
Sync.com, Icedrive, Sia, Filebase, Pure Storage, Rubrik, 
Carbonite.

**Migration Guides (46 pages)**
One guide per integration showing how to migrate to StorX.
URL pattern: `/migrate/[tool]-to-storx`
Directly addresses the "migration sounds painful" objection.
These pages are your DevOps Lead conversion asset.

**Pricing Alternatives (17 pages)**
URL pattern: `/pricing/[slug]-alternative`
Captures cost-focused buyers searching for cheaper options.

### Priority 2 — Mid Funnel (Generate Second)
These pages build awareness and educate buyers.

**Integration Pages (46 pages)**
URL pattern: `/integrations/[tool]`
Shows StorX works with tools buyers already use.
S3 compatibility proof in action.

**Industry Pages (10 pages)**
URL pattern: `/for/[industry]`
Industries: SaaS, Web3, Media, Healthcare, 
Financial Services, and more.

**Use Case Comparisons (12 pages)**
URL pattern: `/compare/[use-case]`
Mid-funnel buyers evaluating options.

**Alternatives List (17 pages)**
URL pattern: `/alternatives/[slug]`

### Priority 3 — Top Funnel (Generate Last)
These pages build organic traffic over time.

**Glossary and Education (15 pages)**
URL pattern: `/learn/[concept]`
Topics: erasure coding, decentralized storage, 
client-side encryption, S3 compatibility, etc.
Long-tail keywords with low competition.

**File Type Pages (10 pages)**
URL pattern: `/store/[filetype]`

---

## Step 5 — StorX Pricing Used in All Content

The agent uses these verified StorX prices in every page.
Do not change these without updating the agent database:

| Plan | Price | Storage |
|---|---|---|
| Free | $0/month | 2 GB |
| Welcome | $9.99/month | 500 GB |
| Professional | $16.99/month | 1 TB |

Egress is included in all plans — this is a key differentiator 
to highlight in every comparison page.

---

## Step 6 — Quality Gate Rules

Before publishing any generated page, check the quality score:

| Decision | What It Means | Action |
|---|---|---|
| ✅ PASS | All checks passed | Publish directly |
| 🟡 PARTIAL | Minor issues found | Human review required |
| ❌ FAIL | Major issues found | Regenerate the page |

**Common failure reasons and fixes:**

| Failure | Fix |
|---|---|
| Title too long or short | Regenerate — model will vary output |
| Pricing incorrect | Check competitors database is up to date |
| AI writing patterns found | Humanise stage should catch this — regenerate if it didn't |
| CTA link wrong | Check button_url is https://storx.io |
| Word count too low | Regenerate with a note to expand |

---

## Step 7 — Publishing Workflow

After generating and downloading pages:

**For HTML output:**
1. Review the page in a browser before publishing
2. Check all internal links point to storx.io pages
3. Verify pricing figures are current
4. Add to the CMS or hand to the developer for upload
5. Submit new URLs to Google Search Console after publishing

**For Word doc output:**
1. Open in Microsoft Word or Google Docs
2. Review for any formatting issues
3. Send to the content team for final review
4. Hand to developer for CMS upload

**After publishing:**
- Add new URLs to the storx.io sitemap
- Submit to Google Search Console
- Add internal links from existing pages to new pages
- Track rankings in `skills/seo-audit/SKILL.md`

---

## Step 8 — Batch Generation Strategy

Generating all 190 pages takes several hours due to API 
rate limits. Use this batching strategy:

**Week 1:** Generate all 17 competitor comparison pages
**Week 2:** Generate all 17 pricing alternative pages
**Week 3:** Generate top 20 migration guides
**Week 4:** Generate remaining migration guides (26)
**Week 5:** Generate all 46 integration pages
**Week 6:** Generate industry, use case, and glossary pages
**Week 7:** Generate file type and alternatives pages

This spreads API costs and gives time to review and publish 
each batch before generating the next.

---

## Step 9 — Keeping Content Fresh

Generated pages need to be refreshed when:
- StorX pricing changes — regenerate all comparison pages
- A competitor changes their pricing — regenerate that page
- A new integration is added to integrations.storx.io — 
  generate the new integration and migration pages
- A new competitor enters the market — add to competitors 
  database and generate their pages

**Recommended refresh schedule:**
- Competitor comparison pages: Every 3 months
- Pricing alternative pages: Every 3 months
- Integration and migration pages: When new integrations launch
- Glossary and education pages: Annually

---

## Connecting This Tool to Other Skills

| Skill | How They Connect |
|---|---|
| `competitor-intelligence/SKILL.md` | Use crawl data to keep competitor pricing accurate in the agent database |
| `seo-audit/SKILL.md` | Audit published pSEO pages monthly — track rankings in Search Console |
| `competitor-alternatives/SKILL.md` | pSEO agent generates the competitor pages at scale — this skill guides their strategy |
| `analytics-tracking/SKILL.md` | Track which pSEO pages drive signups — use UTM parameters on all CTAs |
| `atomizer/SKILL.md` | Atomize high-performing pSEO pages into social content after publishing |
| `content-strategy/SKILL.md` | pSEO pages are part of the broader content plan — coordinate timing |

---

## Troubleshooting

| Problem | Fix |
|---|---|
| Server won't start | Check Node.js version is 18+ — run: `node --version` |
| API key error | Check .env file has ANTHROPIC_API_KEY with no spaces |
| Rate limit errors (429) | Agent retries automatically — wait 60 seconds |
| Generation stuck | Check terminal for error messages — restart with `node server.js` |
| Quality gate failing repeatedly | Check competitors.js database has correct pricing data |
| Download not working | Check the /output folder exists in the storx-v2 directory |

---

## Known Limitations

- Generating all 190 pages takes several hours due to API 
  rate limits — plan batch sessions accordingly
- Keyword volumes are approximate — integrate DataForSEO 
  credentials for exact monthly search volumes
- Content is generated in English only
- Rate limit: 30,000 tokens per minute on Anthropic Starter 
  tier — agent adds automatic delays between calls

---

## Related Skills
- `skills/storx-marketing-context/SKILL.md` — read first
- `skills/programmatic-seo/SKILL.md` — strategy behind 
  what pages to build and why
- `skills/competitor-alternatives/SKILL.md` — strategy 
  for competitor comparison pages
- `skills/seo-audit/SKILL.md` — audit and track published 
  pages after they go live
- `skills/analytics-tracking/SKILL.md` — track which 
  pages drive signups
- `skills/competitor-intelligence/SKILL.md` — keep 
  competitor data accurate in the agent
- `skills/atomizer/SKILL.md` — repurpose published pages 
  into social content
