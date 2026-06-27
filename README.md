# 🤝 Sales Manager — AI Sales Team for Claude Code

> **Your full AI sales team, running inside Claude Code.**  
> Research prospects, qualify leads, find decision-makers, write outreach, prep for meetings, handle objections, and close more deals — all from a single command.

---

## What is this?

Sales Manager is a collection of **14 specialized AI skills** that turn Claude Code into a complete B2B sales intelligence system. Each skill is a focused agent that does one thing exceptionally well. Together they cover the entire sales cycle — from first research to signed proposal.

Built for: **founders doing their own sales**, **sales teams without a research budget**, **agency owners**, and **solopreneurs** who need to move fast and win deals.

---

## Installation

```bash
npx skills add alexgenovese/sales-manager
```

Then invoke any skill from inside Claude Code:

```
/sales prospect https://acme.com
```

---

## The 14 Skills

### 🔍 `/sales prospect <url>`
**Full prospect audit — everything you need before the first call.**

Runs all research phases in parallel and produces a single consolidated report covering company overview, tech stack, recent news, growth signals, hiring patterns, and likely pain points.

```
/sales prospect https://linear.app
```
> *"Give me a complete picture of Linear before my demo call tomorrow."*

---

### 🔬 `/sales research <url>`
**Deep company intelligence across 8 research dimensions.**

Goes beyond a Google search. Analyzes firmographics, funding history, leadership team, product evolution, market position, recent press, customer sentiment, and strategic direction.

```
/sales research https://vercel.com
```
> *"I'm going into a meeting with Vercel's Head of Partnerships — give me everything."*

---

### ✅ `/sales qualify <url>`
**BANT + MEDDIC qualification scorecard.**

Evaluates a prospect against both frameworks and produces an honest score: Is this worth pursuing? Who has budget? Who is the economic buyer? What's the likely timeline? Where are the red flags?

```
/sales qualify https://startupxyz.com
```
> *"Is this lead worth two hours of my time, or should I deprioritize it?"*

---

### 👥 `/sales contacts <url>`
**Decision-maker map and personalized outreach strategy.**

Identifies the full buying committee — economic buyer, champion, technical evaluator, legal/procurement — with LinkedIn search queries, likely email patterns, and a tailored opening line for each stakeholder.

```
/sales contacts https://shopify.com
```
> *"Who exactly should I be talking to at Shopify, and what do I say to each of them?"*

---

### 📧 `/sales outreach <prospect>`
**Complete cold email sequences, ready to send.**

Generates a multi-touch sequence (email + LinkedIn) personalized to the prospect's business, role, and likely pain points. Every message is word-for-word ready — not a template, not a framework.

```
/sales outreach https://notion.so — targeting their Head of Revenue
```
> *"Write me a 5-step cold outreach sequence for the VP of Sales at Notion."*

---

### 🔁 `/sales followup`
**Follow-up sequences for every post-meeting scenario.**

Whether the prospect went quiet after a demo, asked for time to think, or said "check back in 3 months" — this skill generates the exact follow-up to send, when to send it, and what subject line to use.

```
/sales followup — demo was 5 days ago, no response
```
> *"They loved the demo but went dark. What do I send now?"*

---

### 📋 `/sales prep <url>`
**Meeting preparation brief — walk in confident.**

Generates a complete pre-call brief: company snapshot, key stakeholders, their likely agenda, recommended discovery questions, potential objections to expect, and a suggested conversation flow.

```
/sales prep https://stripe.com — 30-minute discovery call
```
> *"I have a call with Stripe's CTO in 2 hours. What do I need to know?"*

---

### 📄 `/sales proposal`
**Professional, client-ready sales proposals.**

Produces a persuasive proposal document tailored to the prospect's specific situation, goals, and objections. Includes executive summary, proposed solution, pricing presentation, ROI case, and next steps.

```
/sales proposal — based on PROSPECT-ANALYSIS.md
```
> *"Turn my research and call notes into a proposal I can send today."*

---

### 🛡️ `/sales objections`
**Word-for-word objection response scripts.**

Covers every common objection — price, timing, incumbent vendor, internal priority, "send me more info" delays — with ready-to-use scripts for calls, meetings, and email replies.

```
/sales objections — prospect said "we already have a solution for this"
```
> *"They said they're happy with their current vendor. What exactly do I say?"*

---

### 🏆 `/sales competitors <url>`
**Battle cards for every competitor your prospect currently uses.**

Detects the tools and vendors the prospect already uses (via job postings, tech stack signals, case studies, review sites), then builds a full competitive battle card for each: strengths, weaknesses, switching costs, landmine questions, and positioning statements.

```
/sales competitors https://hubspot.com
```
> *"What tools is HubSpot using, and how do I position against each of them?"*

---

### 🎯 `/sales icp <description>`
**Define and score your Ideal Customer Profile.**

Takes your product description and builds a detailed ICP: firmographic criteria, behavioral signals, technographic fit, buying triggers, and a scoring model you can apply to any prospect.

```
/sales icp — B2B SaaS, helps engineering teams manage on-call rotations
```
> *"Who is my ideal customer, and how do I know when I've found one?"*

---

### 📊 `/sales report`
**Sales pipeline report from your prospect files.**

Scans all prospect analysis files in your working directory and generates a consolidated pipeline report: deal status, key risks, recommended next actions, and a summary view of your entire book of business.

```
/sales report
```
> *"Give me a summary of where all my active deals stand right now."*

---

### 📑 `/sales report-pdf`
**Export your pipeline report as a professional PDF.**

Takes the output of `/sales report` and produces a formatted, client-presentable PDF version — useful for weekly reviews, investor updates, or sharing with your team.

```
/sales report-pdf
```
> *"I need to share the pipeline status with my co-founder — make it look professional."*

---

## How the Skills Work Together

The real power is in chaining skills across a deal:

```bash
# Day 1 — qualify and research a new inbound lead
/sales qualify https://prospect.com
/sales research https://prospect.com

# Day 2 — find the right person and write the outreach
/sales contacts https://prospect.com
/sales outreach https://prospect.com

# Day 5 — prep for the discovery call
/sales prep https://prospect.com

# Day 10 — handle objections and send a proposal
/sales objections
/sales proposal

# Weekly — review your pipeline
/sales report
```

Each skill reads files produced by previous skills (e.g., `PROSPECT-ANALYSIS.md`, `LEAD-QUALIFICATION.md`) so the intelligence compounds as you work a deal.

---

## Typical Outputs

| Skill | Output file |
|---|---|
| `/sales prospect` | `PROSPECT-ANALYSIS.md` |
| `/sales research` | `COMPANY-RESEARCH.md` |
| `/sales qualify` | `LEAD-QUALIFICATION.md` |
| `/sales contacts` | `CONTACT-STRATEGY.md` |
| `/sales outreach` | `OUTREACH-SEQUENCE.md` |
| `/sales followup` | `FOLLOWUP-SEQUENCE.md` |
| `/sales prep` | `MEETING-PREP.md` |
| `/sales proposal` | `PROPOSAL.md` |
| `/sales objections` | `OBJECTION-PLAYBOOK.md` |
| `/sales competitors` | `COMPETITIVE-INTEL.md` |
| `/sales report` | `SALES-REPORT.md` |

---

## Requirements

- [Claude Code](https://claude.ai/code) with `skills.sh` / Agent Skills support
- Internet access for live research (WebFetch, WebSearch)
- A product or service to sell

---

## License

MIT — use freely, adapt for your own sales stack.
