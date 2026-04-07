# SEO Audit

## When to Use This Skill
Use this skill when you want to audit, review, or diagnose SEO issues 
on the StorX website — including technical SEO, on-page SEO, content 
gaps, and backlink health.

Always read `skills/storx-marketing-context/SKILL.md` first before 
running this skill.

---

## Step 1 — StorX SEO Audit Checklist

Run through this checklist in full before making any SEO 
recommendations. Check each item and note its current status.

---

### Section 1 — Technical SEO

These are the foundation. If technical SEO is broken, nothing 
else matters.

**Indexing and Crawlability**
- [ ] Is storx.io verified in Google Search Console?
- [ ] Is the sitemap submitted to Google Search Console?
- [ ] Are there any crawl errors showing in Search Console?
- [ ] Are any important pages accidentally blocked in robots.txt?
- [ ] Are all important pages indexed by Google? 
      (Search: site:storx.io in Google)
- [ ] Are there any redirect chains longer than 1 hop?
- [ ] Are all redirects 301 (permanent) not 302 (temporary)?

**Page Speed and Core Web Vitals**
- [ ] Does the homepage load in under 3 seconds on mobile?
- [ ] What is the Largest Contentful Paint (LCP) score?
      Target: under 2.5 seconds
- [ ] What is the Cumulative Layout Shift (CLS) score?
      Target: under 0.1
- [ ] What is the First Input Delay (FID) or INP score?
      Target: under 200ms
- [ ] Are images compressed and served in WebP format?
- [ ] Is caching enabled on the server?

**Mobile and HTTPS**
- [ ] Is storx.io fully mobile responsive?
- [ ] Does the site load correctly on mobile devices?
- [ ] Is HTTPS enabled across all pages?
- [ ] Are there any mixed content warnings (HTTP assets on 
      HTTPS pages)?

**URL Structure**
- [ ] Are URLs clean, readable, and keyword-rich?
      Good: blogs.storx.io/aws-s3-alternative
      Bad: blogs.storx.io/post?id=1234
- [ ] Are URLs lowercase with hyphens (not underscores)?
- [ ] Are there any duplicate URLs for the same content?

---

### Section 2 — On-Page SEO

Check every important page on storx.io:

**Title Tags**
- [ ] Does every page have a unique title tag?
- [ ] Are all title tags between 50-60 characters?
- [ ] Does every title tag include the primary keyword for that page?
- [ ] Does the homepage title tag include "StorX" and 
      "decentralized cloud storage"?

**Meta Descriptions**
- [ ] Does every page have a unique meta description?
- [ ] Are all meta descriptions between 150-160 characters?
- [ ] Does every meta description include a clear benefit or CTA?

**Headings**
- [ ] Does every page have exactly one H1 tag?
- [ ] Does the H1 match the primary keyword intent of that page?
- [ ] Are H2 and H3 tags used to structure content logically?

**Content Quality**
- [ ] Is every page at least 300 words? 
      (Blog posts should be 1000-2500 words)
- [ ] Does each page target one primary keyword?
- [ ] Is the primary keyword used naturally in the first 100 words?
- [ ] Are there internal links from each page to related pages?
- [ ] Are external links opening in a new tab?

**Images**
- [ ] Do all images have descriptive alt text?
- [ ] Are image file names descriptive 
      (storx-decentralized-storage.webp not image001.jpg)?

---

### Section 3 — Keyword Coverage Audit

Check whether StorX is currently targeting the right keywords.

**Priority Keywords StorX Should Rank For:**

| Keyword | Monthly Searches | Current StorX Ranking |
|---|---|---|
| decentralized cloud storage | High | Check Search Console |
| s3 compatible storage | Medium | Check Search Console |
| aws s3 alternative | High | Check Search Console |
| storj alternative | Medium | Check Search Console |
| censorship resistant storage | Low | Check Search Console |
| encrypted cloud storage | Medium | Check Search Console |
| cloud storage no egress fees | Low | Check Search Console |
| decentralized storage for web3 | Low | Check Search Console |
| filecoin alternative | Low | Check Search Console |
| backblaze alternative | Low | Check Search Console |

**How to check current rankings:**
Open Google Search Console → Performance → Search Results → 
Filter by query → Search each keyword above.

**What to do with the results:**
- Ranking 1-3: Maintain and protect — build internal links to 
  these pages
- Ranking 4-10: Optimize — improve content, add internal links, 
  build backlinks
- Ranking 11-30: Low-hanging fruit — these pages need content 
  improvement and link building
- Not ranking: Gap — create new content targeting this keyword

---

### Section 4 — Content Gap Analysis

These are content types StorX likely needs but may not have yet:

**High Priority Content Gaps:**
- [ ] Does StorX have a dedicated page explaining erasure coding 
      in plain language?
- [ ] Does StorX have a dedicated page explaining client-side 
      encryption?
- [ ] Does StorX have a "StorX vs AWS S3" comparison page?
- [ ] Does StorX have a "StorX vs Storj" comparison page?
- [ ] Does StorX have a migration guide for coming from AWS S3?
- [ ] Does StorX have a pricing comparison page vs competitors?
- [ ] Does StorX have published customer case studies?
- [ ] Does StorX have a live network stats page?

**Secondary Content Gaps:**
- [ ] Blog posts targeting each primary vertical 
      (SaaS, Web3, Media)
- [ ] Technical tutorials for common developer workflows
- [ ] FAQ page covering all major objections
- [ ] Glossary page for decentralized storage terms 
      (good for long-tail SEO)

---

### Section 5 — Backlink Health

Backlinks are votes of trust from other websites. More quality 
backlinks = higher rankings.

**How to check backlinks:**
Use Google Search Console → Links section, or a free tool 
like Ahrefs Webmaster Tools or Moz Link Explorer.

**What to audit:**
- [ ] How many total backlinks does storx.io have?
- [ ] How many unique domains are linking to StorX?
- [ ] Are any backlinks coming from spammy or irrelevant sites?
- [ ] Which StorX pages have the most backlinks?
- [ ] Which competitor has the most backlinks? 
      (This shows the gap to close)

**Backlink building priorities for StorX:**
1. Get listed in decentralized storage directories and roundups
2. Contribute guest posts to Web3 and DevOps publications
3. Get coverage when a major cloud provider has an outage
4. Build free tools — they attract natural backlinks
5. Submit to Product Hunt, Hacker News, and startup directories

---

## Step 2 — Priority Fixes After the Audit

After completing the checklist, organize findings by impact:

### Fix Immediately (Blocking Issues)
- Crawl errors and indexing problems
- Pages not indexed that should be
- Broken redirects
- Missing title tags or H1s
- Core Web Vitals failures

### Fix This Month (High Impact)
- Missing meta descriptions
- Thin content pages under 300 words
- Missing alt text on images
- Pages targeting no clear keyword
- Internal linking gaps between related pages

### Fix This Quarter (Growth Opportunities)
- Create missing high-priority content
- Build competitor alternative pages
- Improve rankings for keywords in position 4-30
- Start backlink building campaign

---

## Step 3 — Ongoing SEO Monitoring

Run these checks every month:

- [ ] Review Search Console for new crawl errors
- [ ] Check Core Web Vitals report for any regressions
- [ ] Review top performing queries — are rankings improving?
- [ ] Check which pages lost ranking — investigate why
- [ ] Review new backlinks acquired this month
- [ ] Check competitor rankings for priority keywords

**Tools needed for ongoing monitoring:**
- Google Search Console — free, essential
- Google Analytics 4 — free, essential
- Ahrefs Webmaster Tools — free tier available
- PageSpeed Insights — free, use monthly

---

## Related Skills
- `skills/storx-marketing-context/SKILL.md` — read first
- `skills/content-strategy/SKILL.md` — fix content gaps found 
  in the audit
- `skills/programmatic-seo/SKILL.md` — scale content after 
  fixing technical issues
- `skills/competitor-alternatives/SKILL.md` — build comparison 
  pages identified as gaps
- `skills/analytics-tracking/SKILL.md` — set up proper tracking 
  before auditing
- `skills/free-tool-strategy/SKILL.md` — build tools to generate 
  backlinks
- `skills/competitor-intelligence/SKILL.md` — use SEO scores 
  and keyword gap data to prioritise audit fixes
