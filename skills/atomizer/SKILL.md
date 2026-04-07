# StorX Atomizer

## When to Use This Skill
Use this skill when you want to repurpose any content into 
platform-ready marketing material for StorX — including blog posts, 
YouTube videos, competitor articles, industry news, customer 
interviews, or any text source.

Always read `skills/storx-marketing-context/SKILL.md` first before 
running this skill.

---

## What the Atomizer Is

The StorX Atomizer is an internal content intelligence tool that 
takes any source content and breaks it into 8-12 reusable content 
atoms — each one reframed through StorX's DePIN challenger brand 
voice. From each atom it generates ready-to-publish content for 
7 platforms simultaneously.

**Live URL:** https://atomizer.storx.io
**Stack:** Cloudflare Worker · Claude AI · YouTube Data API v3

---

## What It Takes As Input

The Atomizer accepts three types of input:

| Input Type | How to Use |
|---|---|
| YouTube URL | Paste any YouTube URL — captions fetched automatically |
| Web / Article URL | Paste any article URL — content fetched server-side |
| Paste Text | Paste any text directly — transcripts, tweets, competitor copy, customer quotes |

---

## What It Outputs

From each atom the tool generates content for 7 platforms:

| Platform | Format |
|---|---|
| Twitter/X | 4-tweet thread |
| LinkedIn | 150-200 word post |
| Instagram | 6-slide carousel |
| Newsletter | 200-250 word section |
| SEO Blog Article | 700-900 words, fully structured |
| Medium Article | 600-800 words, story-driven |
| Reddit Post | Authentic voice + suggested subreddits |

Everything is generated in StorX's brand voice automatically — 
no manual editing of tone or positioning needed.

---

## Step 1 — How to Use the Atomizer

### Using It
1. Go to https://atomizer.storx.io
2. Choose your input method — YouTube URL, Article URL, or Paste Text
3. Paste your source content
4. Click **Atomize**
5. Wait 30-60 seconds — Claude extracts 8-12 atoms from your source
6. Click any atom to expand it
7. Click any platform tab to see the generated content for that platform
8. Copy the output directly — it is ready to publish

### Saving Your Work
- Every generated output saves automatically to your browser library
- Click the **Library** drawer in the nav to access all previous sessions
- Download individual sessions or your full library as a Word doc

---

## Step 2 — What a Content Atom Is

An atom is a single reusable insight extracted from your source. 
Each atom has:

- **Type** — insight / framework / datapoint / story
- **Title** — max 7 words summarising the atom
- **Hook** — one punchy opening sentence tied to this atom's angle
- **Content** — 2-3 sentences with StorX context baked in
- **Quote** — direct quote from the source if relevant
- **SEO Keywords** — 3-5 keywords specific to this atom's topic

The tool leads every piece of generated content with the atom's 
hook — not a generic StorX pitch. StorX appears as the solution 
to the problem the atom raises.

---

## Step 3 — Best Source Content to Atomize

Not all source content is equal. Prioritise these in order:

### Highest Value Sources
**1. Customer Interview Recordings or Transcripts**
- Produces the most authentic, conversion-focused content
- Customer language becomes Twitter threads, LinkedIn posts, 
  and newsletter sections
- Connect with `skills/customer-research/SKILL.md` — 
  atomize every customer interview immediately after it happens

**2. Competitor Articles and Blog Posts**
- Turn competitor content into StorX-positioned responses
- Identify gaps in their arguments and fill them with StorX angles
- Use data from `skills/competitor-intelligence/SKILL.md` — 
  atomize the top competitor articles flagged each Monday

**3. Industry News and Reports**
- Cloud storage market reports, data breach news, outage stories
- Reactive content opportunity — atomize within 24 hours of 
  a major cloud event

**4. StorX Blog Posts**
- Atomize every blog post after publishing to get a full 
  week of social content from it
- Connect with `skills/content-strategy/SKILL.md` — 
  every published piece should be atomized immediately

**5. YouTube Videos**
- Competitor product demos, conference talks, industry 
  expert interviews
- Paste the YouTube URL — captions are fetched automatically

---

## Step 4 — Platform-by-Platform Usage Guide

### Twitter/X Thread
- Use immediately — threads can be posted same day
- Best atoms for threads: datapoints and frameworks
- Connect with `skills/social-content/SKILL.md` for 
  posting schedule and engagement rules

### LinkedIn Post
- Review before posting — ensure tone matches LinkedIn audience
- Best atoms for LinkedIn: insights and datapoints with numbers
- Target audience: CTOs and DevOps Leads
- Connect with `skills/social-content/SKILL.md`

### Instagram Carousel
- Review all 6 slides for visual flow before posting
- Best atoms for carousels: frameworks and step-by-step insights
- Add StorX brand visuals before publishing

### Newsletter Section
- Drop directly into your newsletter draft
- Best atoms: stories and insights with emotional hooks
- Review for length — trim if needed for your newsletter format

### SEO Blog Article (700-900 words)
- Do not publish directly — review and expand first
- Add internal links to storx.io pages
- Add the target keyword in the title, H1, and first paragraph
- Connect with `skills/seo-audit/SKILL.md` before publishing

### Medium Article (600-800 words)
- Review for story flow before publishing
- Best atoms: stories and customer journey narratives
- Add StorX CTA at the bottom pointing to https://storx.io

### Reddit Post
- Always review suggested subreddits before posting
- Never make it sound promotional — Reddit punishes this
- Connect with `skills/social-content/SKILL.md` for 
  Reddit community rules

---

## Step 5 — Weekly Atomizer Workflow

Follow this routine to get maximum output from minimum effort:
Monday:

Open competitor-intelligence dashboard at intel.storx.io
Note top 2-3 competitor articles flagged in the Articles tab
Paste each into atomizer.storx.io and atomize
Pick the best Twitter thread from each — schedule for the week

After Every Blog Post Published:
5. Paste the blog post URL into atomizer.storx.io
6. Atomize it — pick outputs for each platform
7. Schedule social posts across the week
After Every Customer Interview:
8. Paste the transcript into atomizer.storx.io
9. Atomize it — customer language atoms are your best social content
10. Pick the best LinkedIn post and Twitter thread immediately
When Industry News Breaks:
11. Paste the news article URL into atomizer.storx.io
12. Atomize within 2 hours
13. Post the Twitter thread and LinkedIn post as reactive content

---

## Step 6 — Brand Voice Rules Baked Into the Tool

The Atomizer has StorX's brand voice hardcoded — you do not need 
to prompt it manually. Every output automatically:

- Opens with the centralised storage pain point
- Positions StorX as the logical alternative
- Anchors claims with real StorX numbers:
  - 2,500+ nodes across 50+ countries
  - 50-85% cost savings vs AWS/Azure/GCP
  - 70+ integrations
  - Client-side encryption, S3-compatible API
  - No egress fees, no vendor lock-in
- Always links to https://storx.io — never any other domain
- Never mentions competitors by name in the output

---

## Step 7 — Content Library Management

Every session is automatically saved to your browser library.

**Accessing saved content:**
1. Click the **Library** drawer in the nav at atomizer.storx.io
2. Browse previous sessions by date
3. Click any session to reload all atoms and outputs
4. Download as Word doc for sharing with the team

**Important limitation:**
The library currently saves to your browser only — it is not 
shared across devices or team members. If you clear your browser 
data, library content will be lost. Download important sessions 
as Word docs and save to the StorX shared Google Drive.

---

## Step 8 — What to Atomize and When

| Trigger | What to Atomize | Priority |
|---|---|---|
| Monday morning | Top competitor articles from intel.storx.io | 🔴 Weekly |
| Blog post published | The new blog post URL | 🔴 Every time |
| Customer interview done | Full interview transcript | 🔴 Every time |
| Cloud outage or breach in news | The news article | 🟡 Within 2 hours |
| Competitor publishes new content | Their new page or post | 🟡 Within 24 hours |
| Industry report released | The report or summary | 🟢 Within the week |

---

## Connecting This Tool to Other Skills

| Skill | How They Connect |
|---|---|
| `competitor-intelligence/SKILL.md` | Atomize competitor articles flagged every Monday |
| `content-strategy/SKILL.md` | Atomize every blog post after publishing |
| `social-content/SKILL.md` | Use Atomizer outputs as ready-to-post social content |
| `customer-research/SKILL.md` | Atomize every customer interview transcript |
| `seo-audit/SKILL.md` | Review SEO blog outputs before publishing |
| `programmatic-seo/SKILL.md` | Use Atomizer article outputs as programmatic page drafts |

---

## Known Limitations

| Limitation | Workaround |
|---|---|
| YouTube audio not available | Paste transcript manually from YouTube captions |
| YouTube occasionally rate-limited | Tool automatically falls back to video metadata |
| Library is browser-only | Download Word doc and save to shared Google Drive |
| Twitter/X URLs cannot be fetched | Paste tweet text directly into Paste Text tab |

---

## Related Skills
- `skills/storx-marketing-context/SKILL.md` — read first
- `skills/social-content/SKILL.md` — post Atomizer outputs 
  across platforms
- `skills/content-strategy/SKILL.md` — atomize every 
  published blog post
- `skills/customer-research/SKILL.md` — atomize every 
  customer interview
- `skills/competitor-intelligence/SKILL.md` — atomize 
  top competitor articles weekly
- `skills/seo-audit/SKILL.md` — review SEO blog outputs 
  before publishing
