<h1 align="center">Uwais Jawed</h1>

<p align="center">
  <b>Founding Engineer at The Dev Group LLC</b><br/>
  Multi-tenant SaaS, production AI agents and the integrations nobody else wants.<br/>
  Kolkata, India · working remotely with US teams
</p>

<p align="center">
  <a href="https://uwais.dev"><img src="https://img.shields.io/badge/uwais.dev-0d1117?style=for-the-badge&logo=googlechrome&logoColor=white" alt="uwais.dev"/></a>
  <a href="https://www.linkedin.com/in/uwais-jawed/"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"/></a>
  <a href="mailto:uwaisjawed8081@gmail.com"><img src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Email"/></a>
  <a href="https://x.com/uwais_jawed"><img src="https://img.shields.io/badge/@uwais__jawed-000000?style=for-the-badge&logo=x&logoColor=white" alt="X"/></a>
</p>

---

I take products from an empty repo to paying customers: schema, API, frontend, infra, CI/CD and the AI layer. Most of my work is private client and company code, so this page is the map.

## What I'm building

### [Complied](https://compliednyc.com/) · NYC building compliance · lead engineer
The compliance operating system for NYC lead-paint inspection and abatement firms.
- Ingests 15 NYC open-data feeds (HPD, DOB, ECB/OATH, 311, DOF) into one record per building, with nightly deltas, resumable backfills and a quarantine for rows that match no building.
- The citywide violations map runs on its own DuckDB service over nightly Parquet snapshots, off the transactional database.
- Tenants isolated by Postgres row-level security; edge functions generate HPD filings, lab reports, affidavits, invoices and e-signed proposals behind a white-label client portal.

`React` `TypeScript` `Supabase` `PostgreSQL` `DuckDB` `AWS EC2` · [docs](https://docs.compliednyc.com/)

### [Riskflow](https://vodazok.com/) · HIPAA compliance for MSPs · sole architect
Risk assessments, policies, staff training and e-signed vendor agreements for healthcare orgs and the MSPs that run their IT.
- Three-level tenancy (MSP → org → vendor) scoped in every query, bitfield RBAC, 404-over-403 so nothing leaks across tenants, decisions written down as ADRs.
- GRC engine: HIPAA controls mapped to requirements, with a nightly test runner that checks Google Workspace through the Admin SDK and flips controls to passing or failing.
- Audit log with CSV export, Redis rate limiting, CI with migration-drift checks and daily backups.

`NestJS` `Prisma` `PostgreSQL` `Redis` `Turborepo` `Google Admin SDK`

### [SlashPost](https://slashpost.ai/) · AI local SEO · 25+ paying businesses
Puts a local business's Google Business Profile on autopilot: scheduled posts, review replies, listing scans and profile fixes.
- A Claude agent audits each profile with read-only tools; a deterministic validator, not the prompt, decides what survives, and nothing is written to Google without the owner's approval.
- A LangGraph website-SEO agent, stabilised by moving to Anthropic native structured output after forced tool calls broke six production runs in a row.
- 39 Trigger.dev background jobs, Stripe + Razorpay billing with webhooks as source of truth and a nightly drift-repair sweep.

`Next.js` `LangGraph` `Claude` `OpenAI` `Trigger.dev` `Prisma` `Stripe`

## Client work
- **Fire dispatch print gateway** for a US fire department: Active911 webhooks to printed run tickets in seconds, deduped against alert bursts, printed silently on Windows or ESC/POS on a Raspberry Pi.
- **Clinic operations platform** for a US behavioral-health clinic: real-time call intake, a Chrome extension that fills the EHR, granular permissions with audit logging, and an AI insights chat limited to aggregate data.
- **PeopleSoft PunchOut gateway**: cXML bridge between PeopleSoft eProcurement and a print supplier's storefront.

## Public
- [**stormflag**](https://github.com/Martial-Geek/stormflag): feature-flag service in Java on a hand-written Raft (elections, heartbeats, failover).
- [**seo-os**](https://github.com/Martial-Geek/seo-os): LangGraph agent that turns Search Console and GA4 data into typed SEO actions behind a human approval gate.

## Experience
| Role | Company | When |
|---|---|---|
| Founding Engineer | The Dev Group LLC | Jan 2025 – present |
| Full Stack Developer | Segritude Games | Mar 2025 – Jun 2025 |
| Web Development Intern | Zidio Development | Aug 2024 – Oct 2024 |

B.E. Computer Science, Future Institute of Engineering and Management, Kolkata (2021 – 2025, CGPA 8.21)

## Stack
- **Languages:** TypeScript · JavaScript · Python · Java · SQL
- **Backend:** Node.js · NestJS · Express · Prisma · Drizzle · BullMQ · Trigger.dev · Supabase
- **AI:** LangGraph · Anthropic Claude · OpenAI · structured output · embeddings · human-in-the-loop agents
- **Data & infra:** PostgreSQL · Redis · DuckDB · MongoDB · Docker · AWS · GCP · Cloudflare · Vercel · GitHub Actions

---

<p align="center"><sub>Open to founding and early engineer roles · <a href="https://uwais.dev">uwais.dev</a></sub></p>
