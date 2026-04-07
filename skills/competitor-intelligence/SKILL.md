# Competitor Intelligence Agent

## When to Use This Skill
Use this skill when you want to monitor competitors, identify SEO gaps, 
track competitor content activity, generate action items from competitor 
data, or audit whether StorX has implemented previous recommendations.

Always read `skills/storx-marketing-context/SKILL.md` first before 
running this skill.

---

## What This Tool Is

The StorX Competitor Intelligence Agent is an automated monitoring 
system that crawls competitor websites, checks keyword rankings, 
monitors social media, and uses Claude AI to generate prioritised 
action items for the StorX marketing team.

**Dashboard URL:** http://localhost:5000 (local)  
**Production URL:** https://intel.storx.io (coming soon — pending deployment)  
**Current Status:** 🔄 Running locally — live server deployment in progress
**Runs automatically:** Every Monday at 06:00 UTC
**Competitors tracked:** 18 across decentralised storage, privacy 
cloud, enterprise storage, and cloud backup categories

---

## Step 1 — Accessing the Dashboard

Open your browser and go to:
https://intel.storx.io

The dashboard has 7 tabs:

| Tab | What It Shows |
|---|---|
| Report | Executive summary + Top 10 prioritised action items |
| Articles | 5 AI-generated content briefs with H2 outlines |
| Keyword Gaps | Keywords competitors rank for that StorX does not |
| SEO Scores | AI-rated SEO quality 1-10 per competitor |
| Alerts | New competitor pages, trend spikes, SEO changes |
| StorX Audit | Self-audit — checks if action items were implemented |
| History | Log of every previous run |

---

## Step 2 — Running the Agent

### Option A — Automatic Weekly Run
The agent runs every Monday at 06:00 UTC automatically.
No action needed — just check the dashboard Monday morning.

### Option B — Manual Full Run
1. Go to https://intel.storx.io
2. Click **▶ Run Now**
3. Select which competitors to crawl from the modal
4. Click **Start Run**
5. Wait 10-15 minutes for results to appear

### Option C — Quick Test Run
1. Click **Test Run** on the dashboard
2. Crawls Storj and Filecoin only
3. Takes 2-3 minutes
4. Use this to verify the tool is working correctly

### Option D — StorX Self-Audit
1. Click **🔍 Run StorX Audit**
2. Agent crawls storx.io and compares against last action plan
3. Returns a checklist showing what has and has not been implemented
4. Use this every 2 weeks to track marketing execution progress

---

## Step 3 — Reading the Report Tab

The Report tab is your most important weekly output.

**Executive Summary** — Claude's overall assessment of the 
competitive landscape this week. Read this first.

**Top 10 Action Items** — Prioritised list of what StorX should 
do based on what competitors are doing. Each item is colour coded:

- 🔴 **High Impact** — do this week
- 🟡 **Medium Impact** — do this month  
- 🟢 **Low Impact** — backlog

**How to use action items:**
- Copy the top 3 into your weekly marketing task list
- Share the full list with your team in your Monday standup
- Run the StorX Audit in 2 weeks to check completion status

---

## Step 4 — Reading the Articles Tab

The Articles tab gives you 5 ready-to-brief content pieces 
generated from competitor gap analysis.

Each article brief includes:
- Suggested title and target keyword
- Why this topic is a gap or opportunity right now
- Full H2 outline — the structure is already done
- Recommended word count and content type

**How to use article briefs:**
- Pick the most relevant brief each week
- Use `skills/content-strategy/SKILL.md` to plan distribution
- Pass the brief to a writer or use it as a Claude prompt directly:
Read skills/storx-marketing-context/SKILL.md — then write
a full blog post based on this brief: [paste brief here]

---

## Step 5 — Reading the Keyword Gaps Tab

Shows keywords that competitor websites rank for in Google 
that storx.io does not currently rank for.

**How to use keyword gap data:**
- Add high-volume gaps to your `keywords` tab in the Google Sheet
- Use gaps to brief new blog posts or programmatic SEO pages
- Reference `skills/programmatic-seo/SKILL.md` for scaling 
  gap coverage at volume
- Reference `skills/seo-audit/SKILL.md` for fixing on-page 
  issues that may be blocking rankings

**Priority filter:**
Focus on keywords where:
- A competitor ranks in position 1-5
- StorX is not ranking at all
- The keyword matches one of StorX's three buyer personas 
  (CTO, DevOps Lead, Web3 Founder)

---

## Step 6 — Reading the Alerts Tab

Alerts are automatically generated when the agent detects:

- A competitor has published a new page
- A competitor's SEO score has changed significantly
- A competitor has had a spike in social media engagement
- A keyword ranking has shifted dramatically

**How to use alerts:**
- Check alerts every Monday after the weekly run
- Reactive content opportunity: if a competitor publishes 
  something new, publish a StorX response within 48 hours
- Use `skills/social-content/SKILL.md` for reactive posts
- Use `skills/competitor-alternatives/SKILL.md` if a new 
  competitor page targets StorX's keywords directly

---

## Step 7 — Running the StorX Self-Audit

The self-audit is one of the most valuable features. 
Run it every two weeks.

**What it checks:**
1. Crawls storx.io — homepage, blog, pricing, docs, sitemap
2. Loads the last AI-generated action plan
3. Asks Claude: "Has this been implemented?"
4. Returns a checklist with four statuses:

| Status | Meaning |
|---|---|
| ✅ Completed | Evidence found on storx.io |
| 🔄 Partial | Some progress, not fully done |
| ❌ Pending | No evidence of implementation |
| ❓ Cannot Verify | Internal task — not checkable from HTML |

**How to use audit results:**
- Any ❌ Pending item older than 2 weeks needs to be 
  escalated or deprioritised
- Any 🔄 Partial item needs an owner assigned
- Use the completion percentage as a weekly team metric

---

## Step 8 — Downloading the Word Report

After any run, click **⬇ Download Report** in the navbar.

The Word document includes:
- Run summary (date, competitors, pages, gaps)
- Executive summary
- Top 10 action items with colour coding
- 5 article briefs with full H2 outlines
- Keyword gap table
- SEO scores table
- Trend alerts

**File name format:** `StorX_Intelligence_Report_YYYY-MM-DD.docx`

**Share this report:**
- With the StorX founder and leadership team weekly
- In the marketing team Slack channel every Monday
- Archive in the shared Google Drive marketing folder

---

## Step 9 — Managing Competitors in the Google Sheet

The Google Sheet is the control panel for the agent. 
Access it via your Google Drive.

**To add a new competitor:**
1. Open the Google Sheet
2. Go to the `competitors` tab
3. Add a new row with these details:

| Column | What to Fill In |
|---|---|
| Competitor Name | e.g. Cloudflare R2 |
| Website URL | e.g. https://cloudflare.com/r2 |
| Blog / News Path | e.g. https://blog.cloudflare.com |
| Twitter / X Handle | e.g. @cloudflare |
| Active? (Y/N) | Y |
| Priority | High / Medium / Low |
| Pricing URL | e.g. https://cloudflare.com/r2/pricing |

No code changes needed — the agent picks up new rows 
automatically on the next run.

**To pause a competitor:**
Change their `Active? (Y/N)` column to `N`.
They will be skipped on the next run.

**Current competitors tracked:**

High Priority: Storj, Filecoin, Sia Network, Proton Drive, 
Internxt, MEGA, Backblaze, Impossible Cloud Network, Aethir

Medium Priority: Arweave, Akash Network, Tresorit, Sync.com, 
Icedrive, Pure Storage, Rubrik

Low Priority: Carbonite

---

## Step 10 — Weekly Workflow Using This Tool

Follow this routine every Monday:
Monday Morning:

Open https://intel.storx.io
Read the Report tab — executive summary first
Copy top 3 action items into this week's task list
Check Alerts tab — any reactive content opportunities?
Check Keyword Gaps — any new gaps to add to content plan?
Pick one Article Brief to brief or write this week
Share the downloaded Word report with the team

Every Two Weeks:
8. Run the StorX Self-Audit
9. Review completion percentage — escalate any stuck items
10. Update the Google Sheet competitors tab if needed

---

## Connecting This Tool to Other Skills

| Skill | How They Connect |
|---|---|
| `competitor-alternatives/SKILL.md` | Use keyword gap data and new competitor pages to brief comparison pages |
| `seo-audit/SKILL.md` | Use SEO scores and keyword gaps to prioritise audit fixes |
| `content-strategy/SKILL.md` | Use article briefs and gap data to feed the content calendar |
| `social-content/SKILL.md` | Use alerts for reactive social posts when competitors make moves |
| `programmatic-seo/SKILL.md` | Use keyword gap data to scale programmatic page coverage |
| `analytics-tracking/SKILL.md` | Track whether content created from briefs drives signups |
| `ab-test-setup/SKILL.md` | Use competitor SEO scores to identify what to test on storx.io |

---

## Troubleshooting Quick Reference

| Problem | Fix |
|---|---|
| Dashboard shows no data | Check the reports tab — run may still be processing |
| Test run fails | Check your .env API keys are correct |
| Competitor not being crawled | Check Active? column is set to Y in Google Sheet |
| Google Sheet not updating | Check sheet is shared with service account email |
| Twitter data missing | Check Twitter API credentials in .env |

---

## Related Skills
- `skills/storx-marketing-context/SKILL.md` — read first
- `skills/competitor-alternatives/SKILL.md` — act on competitor data
- `skills/seo-audit/SKILL.md` — act on SEO gap data
- `skills/content-strategy/SKILL.md` — act on article briefs
- `skills/social-content/SKILL.md` — act on alerts reactively
- `skills/programmatic-seo/SKILL.md` — scale keyword gap coverage
