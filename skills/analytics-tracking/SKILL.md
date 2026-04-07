# Analytics Tracking

## When to Use This Skill
Use this skill when you want to set up, audit, or improve analytics 
tracking for StorX — including website events, signup tracking, trial 
activations, and campaign performance measurement.

Always read `skills/storx-marketing-context/SKILL.md` first before 
running this skill.

---

## Step 1 — The StorX Metrics That Actually Matter

Not all metrics are equal. These are the ones StorX should track 
obsessively:

### Primary Metrics (Revenue-Connected)
| Metric | Why It Matters |
|---|---|
| Trial signups | Top of funnel health |
| Trial to paid conversion rate | Product-market fit signal |
| Signup source / channel | Where to invest more budget |
| Time to first file upload | Activation speed — faster = better retention |
| Churn rate | Retention health |

### Secondary Metrics (Awareness and Engagement)
| Metric | Why It Matters |
|---|---|
| Organic search traffic | SEO compounding effect |
| Blog to signup conversion | Content ROI |
| Ad click-through rate | Creative effectiveness |
| Email open and click rate | Audience engagement |
| Community mentions | Brand awareness in Web3 / DevOps circles |

### Vanity Metrics to Deprioritize
- Page views without conversion context
- Social media followers
- Email list size without engagement data

---

## Step 2 — Events to Track on the StorX Website

Set up tracking for these specific user actions:

**Acquisition Events**
- `page_view` — every page on storx.network
- `cta_click` — every "Start Free Trial" or "Get Started" button
- `pricing_page_view` — intent signal
- `docs_page_view` — high-intent technical evaluation signal

**Activation Events**
- `signup_started` — user begins registration
- `signup_completed` — user completes registration
- `first_login` — user logs in for the first time
- `first_file_uploaded` — THE most important activation event
- `api_key_generated` — signals technical integration intent

**Retention Events**
- `storage_limit_reached` — upgrade opportunity trigger
- `subscription_started` — paid conversion
- `subscription_cancelled` — churn trigger

---

## Step 3 — UTM Parameters for Campaign Tracking

Every link StorX shares externally must have UTM parameters so you know 
exactly where signups are coming from.

**UTM Format:**
https://storx.io/?utm_source=X&utm_medium=Y&utm_campaign=Z

**StorX UTM Naming Convention:**

| Parameter | Options | Example |
|---|---|---|
| utm_source | twitter, linkedin, reddit, newsletter, google, producthunt | twitter |
| utm_medium | social, email, paid, organic, referral | social |
| utm_campaign | campaign name in lowercase with hyphens | web3-founders-jan |

**Example links:**
- Twitter post: `?utm_source=twitter&utm_medium=social&utm_campaign=web3-launch`
- Newsletter: `?utm_source=newsletter&utm_medium=email&utm_campaign=monthly-jan`
- Google Ad: `?utm_source=google&utm_medium=paid&utm_campaign=s3-alternative`

**Rule: Never share a link without UTM parameters. Ever.**

---

## Step 4 — Recommended Analytics Stack for StorX

| Tool | Purpose | Priority |
|---|---|---|
| Google Analytics 4 (GA4) | Website traffic and event tracking | 🔴 Must have |
| Google Search Console | Organic search performance | 🔴 Must have |
| Hotjar or Microsoft Clarity | Heatmaps and session recordings | 🟡 High value |
| Mixpanel or Amplitude | Product analytics (in-app events) | 🟡 High value |
| UTM.io or Notion | UTM link management and naming | 🟢 Nice to have |

Start with GA4 and Google Search Console. Add the others as you grow.

---

## Step 5 — Monthly Analytics Review Checklist

Run this review every month:

- [ ] Which channel drove the most signups this month?
- [ ] What is the current trial-to-paid conversion rate?
- [ ] Which blog posts are driving the most organic signups?
- [ ] Where are users dropping off in the signup flow?
- [ ] What is the average time from signup to first file upload?
- [ ] Which ad campaigns have the lowest cost per signup?
- [ ] Are there any sudden traffic drops that need investigating?

---

## Step 6 — StorX-Specific Tracking Priorities

Based on StorX's current marketing goals, set these up first:

1. **Signup conversion tracking** — know exactly how many visitors 
   become trial users
2. **Channel attribution** — know which content, ads, and communities 
   are driving signups
3. **Activation tracking** — know how many trial users upload their 
   first file within 24 hours
4. **Search Console setup** — track which keywords are bringing 
   technical buyers to StorX content

---

## Related Skills
- `skills/storx-marketing-context/SKILL.md` — read first
- `skills/ab-test-setup/SKILL.md` — always set up tracking before 
  running any A/B test
- `skills/seo-audit/SKILL.md` — uses Search Console data
- `skills/content-strategy/SKILL.md` — uses organic traffic data
