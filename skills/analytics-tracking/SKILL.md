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
