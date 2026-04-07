# StorX Marketing Skills

A library of AI agent skills and tool operating manuals built 
specifically for StorX Network — covering SEO, content strategy, 
competitor intelligence, social media, analytics, A/B testing, 
programmatic SEO, and more.

Built for use with Claude, Claude Code, and any AI agent that 
supports markdown-based skill files.

---

## How It Works

Each skill is a markdown file that gives an AI agent specialised 
knowledge for a specific marketing task. Every skill reads the 
`storx-marketing-context` file first — so every output is 
tailored to StorX's product, audience, and positioning 
automatically.

---

## Skills in This Library

### Foundation
| Skill | What It Does |
|---|---|
| `storx-marketing-context` | Read by all other skills first — contains StorX product, audience, personas, voice, and competitive context |

### Marketing Skills
| Skill | What It Does |
|---|---|
| `ab-test-setup` | Plan and run A/B tests on any StorX marketing asset |
| `analytics-tracking` | Set up and audit analytics and conversion tracking |
| `competitor-alternatives` | Build StorX vs competitor comparison pages |
| `content-strategy` | Plan what content to create and why |
| `customer-research` | Conduct and synthesise customer research and voice of customer |
| `free-tool-strategy` | Plan and build free tools for lead generation and SEO |
| `marketing-psychology` | Apply behavioural science to StorX marketing |
| `programmatic-seo` | Strategy for creating SEO-driven pages at scale |
| `seo-audit` | Audit and fix SEO issues on storx.io |
| `social-content` | Create and plan content for LinkedIn, Twitter/X, and Reddit |

### Tool Skills
| Skill | What It Does |
|---|---|
| `competitor-intelligence` | Operate the StorX competitor crawl intelligence agent |
| `atomizer` | Turn any content into platform-ready output for 7 channels simultaneously |
| `pseo-agent` | Operate the programmatic SEO agent to generate 190 pages at scale |

---

## Tool Status

| Tool | Local URL | Production URL | Status |
|---|---|---|---|
| Competitor Intelligence | http://localhost:5000 | https://intel.storx.io | 🔄 Deployment in progress |
| Atomizer | — | https://atomizer.storx.io | ✅ Live |
| pSEO Agent | http://localhost:3000 | https://pseo.storx.io | 🔄 Deployment in progress |

---

## How to Use

Reference any skill file in your Claude prompt:
Read skills/storx-marketing-context/SKILL.md and then
skills/social-content/SKILL.md — help me write 5 Twitter
posts about StorX's flat pricing.

For tool skills:
Read skills/storx-marketing-context/SKILL.md and then
skills/atomizer/SKILL.md — I have a YouTube video URL,
help me atomize it into social content.

The agent reads the context first, then applies the skill 
framework to produce StorX-specific output every time.

---

## How Skills Connect

All skills are interconnected. Here is how they work together:
storx-marketing-context (read first by everything)
│
├── competitor-intelligence → feeds → competitor-alternatives
│                          → feeds → content-strategy
│                          → feeds → seo-audit
│
├── pseo-agent → feeds → programmatic-seo
│             → feeds → competitor-alternatives
│             → feeds → seo-audit
│
├── atomizer → feeds → social-content
│           → feeds → content-strategy
│           → feeds → customer-research
│
├── customer-research → feeds → copywriting
│                    → feeds → social-content
│
└── analytics-tracking → feeds → ab-test-setup
→ feeds → seo-audit
→ feeds → content-strategy

---

## Weekly Workflow Using This Library
Monday Morning:

Check competitor-intelligence dashboard — intel.storx.io
Pick top 3 action items from the report
Atomize top competitor articles via atomizer.storx.io
Schedule social content from Atomizer outputs

During the Week:
5. Write or brief content using content-strategy skill
6. Generate pSEO pages using pseo-agent skill
7. Post social content using social-content skill
Every Two Weeks:
8. Run StorX self-audit on competitor-intelligence dashboard
9. Run seo-audit skill to check storx.io health
Monthly:
10. Review analytics-tracking metrics
11. Run ab-test-setup for highest priority test
12. Update customer-research with new interview findings

---

## Built For

StorX Network — decentralised, S3-compatible cloud storage.

- **Website:** https://storx.io
- **Blog:** https://blogs.storx.io
- **Integrations:** https://integrations.storx.io
- **Tools:** https://tools.storx.io
