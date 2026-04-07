# StorX Marketing Skills

A library of AI agent skills built specifically for StorX Network — 
covering SEO, content strategy, competitor positioning, social media, 
analytics, A/B testing, and more.

Built for use with Claude, Claude Code, and any AI agent that supports 
markdown-based skill files.

---

## How It Works

Each skill is a markdown file that gives an AI agent specialized 
knowledge for a specific marketing task. Every skill reads the 
`storx-marketing-context` file first — so every output is tailored 
to StorX's product, audience, and positioning automatically.

---

## Skills in This Library

| Skill | What It Does |
|---|---|
| `storx-marketing-context` | Foundation file — read by all other skills first |
| `ab-test-setup` | Plan and run A/B tests on any StorX marketing asset |
| `analytics-tracking` | Set up and audit analytics and conversion tracking |
| `competitor-alternatives` | Build StorX vs competitor comparison pages |
| `content-strategy` | Plan what content to create and why |
| `customer-research` | Conduct and synthesize customer research and VOC |
| `free-tool-strategy` | Plan and build free tools for lead generation and SEO |
| `marketing-psychology` | Apply behavioral science to StorX marketing |
| `programmatic-seo` | Create SEO-driven pages at scale |
| `seo-audit` | Audit and fix SEO issues on the StorX website |
| `social-content` | Create and plan content for LinkedIn, Twitter/X, and Reddit |

---

## How to Use

Simply reference any skill file in your AI agent prompt:
Read skills/storx-marketing-context/SKILL.md and then
skills/social-content/SKILL.md — help me write 5 Twitter posts
about StorX's flat pricing.

The agent will read the context first, then apply the skill 
framework to produce StorX-specific output.

---

## Built For

StorX Network — decentralized, S3-compatible cloud storage.
Learn more at [StorxNetwork](https://storx.io)
