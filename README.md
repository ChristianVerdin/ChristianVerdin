# Hi there, I'm Christian Verdin

**Senior Data Scientist & AI/ML Engineer** with 7+ years of experience designing, developing, and deploying end-to-end ML/AI systems — from data pipelines and production models to complete applications that drive real business impact.

I build production-grade systems that integrate LLMs, real-time data pipelines, and modern web frameworks to solve complex analytical problems.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/christian-verdin/)
[![Portfolio](https://img.shields.io/badge/Portfolio-dailylocks.ai-4285F4?style=for-the-badge&logo=google-chrome&logoColor=white)](https://dailylocks.ai)
[![Medium](https://img.shields.io/badge/Medium-Articles-000000?style=for-the-badge&logo=medium&logoColor=white)](https://medium.com/@cver123/about)

---

## Projects at a Glance

| Project | What it does | Status | Stack |
|---------|--------------|--------|-------|
| **LakeshoreIQ** | Real estate intelligence platform — 12 data sources, ZIP-level appreciation analytics, 3-pathway valuation methodology | Live · Open Beta | Next.js · FastAPI · Supabase |
| **312Deals** | Chicago food & drink deals — 12,000+ venues, 15,000+ deals, multi-channel agent surface (REST · MCP · WebMCP · ChatGPT) | Live | Next.js · FastAPI · SQLite · MCP |
| **Daily Locks AI** | Multi-domain AI agent for sports intelligence — Claude-powered chat, intent routing, multi-sport prediction surface | Live · Open Beta | Next.js · FastAPI · Claude · Stripe |
| **NFL Analytics** | Pure R analytics engine — 285 games, 21 custom playoff visualizations, 116+ matchup reports | 2025-26 Complete | R · ggplot2 · SQLite |
| **MLB 2026** | Active production modeling pipeline — 16-step daily run, validated alpha-pattern detection, automated deploy | Live (in-season) | R · Python · Supabase |

---

## Featured Projects

### LakeshoreIQ — Illinois Real Estate Intelligence
**Property search, valuation, and market analysis platform**

A production SaaS aggregating 12 real-time data sources to deliver property search, automated valuations, and neighborhood intelligence across 150+ Illinois cities and 50+ Chicago neighborhoods. Integrates census demographics, ISBE school ratings (5,112 schools, 94% geocoded), FEMA flood zones, FBI crime data, FRED economic indicators, and 14,176 transit stops across CTA, Metra, and Pace into a unified property analysis experience. Three-pathway valuation methodology, ZIP-level appreciation analytics across 1,076 IL ZIPs, and automated weekly buyer reports.

**Live:** [lakeshoreiq.com](https://lakeshoreiq.com)

<p align="center">
  <img src="./images/illinois_real_estate/desktop-home-fresh.png" width="800" alt="LakeshoreIQ — homepage with 12 data sources and Illinois market intelligence">
</p>

**Built with:** `Next.js 15` · `React 19` · `TypeScript` · `FastAPI` · `Python` · `Supabase` · `PostgreSQL` · `Redis` · `Stripe` · `Tailwind CSS`

[View Repository →](https://github.com/ChristianVerdin/illinois-real-estate)

---

### 312Deals — Chicago Food & Drink Deals
**AI-powered restaurant deal intelligence platform**

A production platform aggregating 12,000+ active venues and 15,000+ active deals across 128 Chicagoland neighborhoods (52 city + 76 suburban). Multi-channel agent surface: 26 REST endpoints, 11-tool FastMCP server, 10 in-browser WebMCP tools, and a ChatGPT custom GPT — all backed by a single SQLite database. Automated multi-source deal collection pipeline using Claude API for extraction, Firecrawl for web scraping, Apify for social media ingestion, and AgentMail for newsletter parsing. Content hashing reduces API costs 60–80%; adaptive scheduling handles 5,810 tracked sources.

**Live:** [312deals.com](https://312deals.com)

<p align="center">
  <img src="./images/312deals/desktop-home-fresh.png" width="800" alt="312Deals — Chicago food and drink deals homepage">
</p>

**Built with:** `Next.js 14` · `TypeScript` · `FastAPI` · `Python` · `SQLite` · `Claude API` · `FastMCP` · `Firecrawl` · `Apify` · `AgentMail` · `Vercel` · `Railway`

[View Repository →](https://github.com/ChristianVerdin/chideals)

---

### Daily Locks AI — Multi-Domain AI Agent for Sports Intelligence
**Consumer-facing AI agent unifying multi-sport prediction backends**

A production AI agent surfacing multi-sport prediction outputs (NCAAB, MLB, NFL) through a Next.js consumer product and a Claude-powered conversational interface. Multi-step intent routing translates natural-language questions into structured queries against tier-based confidence models, with calibrated tiering (VERY_HIGH · STRONG_BET · LEAN) exposing the highest-conviction picks. Real-time ESPN scoreboard integration, automated Telegram alert delivery, and Stripe-based subscription billing. Closed the 2025-26 NCAAB season with full tier-based accuracy tracking across 1,835 graded predictions and 730 teams.

**Live:** [dailylocks.ai](https://dailylocks.ai)

<p align="center">
  <img src="./images/dailylocks/desktop-ai-chat.png" width="800" alt="Daily Locks AI — Claude-powered chat interface routing multi-sport questions">
</p>

**Built with:** `Next.js 15` · `React 19` · `TypeScript` · `FastAPI` · `Python` · `Claude API` · `Supabase` · `Stripe` · `ESPN API`

---

### NFL Analytics — Pure R Engine for Playoff & Matchup Analysis
**Statistical visualization toolkit with 21 custom charts and 116+ matchup reports**

A pure R analytics engine that processed 285 NFL games, 14,900+ player-quarter records, 22,700+ snap counts, and 1,455 TD events from the 2025-26 season (closed at Super Bowl LX). Twenty-one custom playoff visualizations spanning EPA comparisons, efficiency matrices, quarter-scoring heatmaps, third-down and red-zone breakdowns, explosive-play and turnover analytics, and skill-position matchup charts. 116+ scripted matchup reports generated through ggplot2 and SQLite pipelines.

<p align="center">
  <img src="./images/nfl_analytics/1_playoff_epa_comparison.png" width="800" alt="NFL Analytics — playoff EPA comparison visualization">
</p>

**Built with:** `R 4.5` · `tidyverse` · `ggplot2` · `dplyr` · `SQLite` · `RSQLite` · `DBI`

---

### MLB 2026 — Active Production Modeling Pipeline
**16-step daily pipeline ingesting play-by-play, lineups, and authoritative odds**

An active production modeling pipeline running on a 3x-daily cadence (8 AM · 11 AM · 2 PM CT) throughout the 2026 MLB season. The 16-step orchestrator ingests play-by-play, lineup, weather, and odds data; applies validated alpha-pattern detection across career history, geographic context, and situational matchups; and auto-deploys generated picks to dailylocks.ai via scheduled launchd jobs. Anti-hallucination odds verification fails loudly when authoritative sources are missing, preventing silent fall-throughs.

**Built with:** `R` · `Python` · `Supabase` · `Odds API` · `RotoWire` · `ESPN API` · `launchd`

---


## Technical Skills

<table>
<tr>
<td valign="top" width="33%">

### Languages
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-007ACC?style=flat-square&logo=typescript&logoColor=white)
![R](https://img.shields.io/badge/R-276DC3?style=flat-square&logo=r&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=flat-square&logo=postgresql&logoColor=white)

</td>
<td valign="top" width="33%">

### AI & ML
![Claude](https://img.shields.io/badge/Claude_API-191919?style=flat-square&logo=anthropic&logoColor=white)
![MCP](https://img.shields.io/badge/MCP%2FFastMCP-191919?style=flat-square&logo=anthropic&logoColor=white)
![LangChain](https://img.shields.io/badge/LangChain-121212?style=flat-square&logo=chainlink&logoColor=white)
![OpenAI](https://img.shields.io/badge/OpenAI-412991?style=flat-square&logo=openai&logoColor=white)

</td>
<td valign="top" width="33%">

### Frontend
![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=next.js&logoColor=white)
![React](https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black)
![Tailwind](https://img.shields.io/badge/Tailwind-38B2AC?style=flat-square&logo=tailwind-css&logoColor=white)

</td>
</tr>
<tr>
<td valign="top" width="33%">

### Backend & Data
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![Supabase](https://img.shields.io/badge/Supabase-3ECF8E?style=flat-square&logo=supabase&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white)
![SQLite](https://img.shields.io/badge/SQLite-003B57?style=flat-square&logo=sqlite&logoColor=white)

</td>
<td valign="top" width="33%">

### Cloud & ML Platforms
![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat-square&logo=amazon-aws&logoColor=white)
![Databricks](https://img.shields.io/badge/Databricks-FF3621?style=flat-square&logo=databricks&logoColor=white)
![Vercel](https://img.shields.io/badge/Vercel-000000?style=flat-square&logo=vercel&logoColor=white)
![Railway](https://img.shields.io/badge/Railway-0B0D0E?style=flat-square&logo=railway&logoColor=white)

</td>
<td valign="top" width="33%">

### Tools
![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Playwright](https://img.shields.io/badge/Playwright-2EAD33?style=flat-square&logo=playwright&logoColor=white)
![Stripe](https://img.shields.io/badge/Stripe-008CDD?style=flat-square&logo=stripe&logoColor=white)

</td>
</tr>
</table>

---

## Let's Connect

Open to senior IC and beginner-manager roles in AI/ML, applied ML, data platform, and AI-product engineering — particularly where production scale and modern AI tooling intersect.

<p align="center">
  <a href="https://www.linkedin.com/in/christian-verdin/"><img src='https://img.icons8.com/color/2x/linkedin.png' alt='linkedin' height='40'></a>
  <a href="https://github.com/ChristianVerdin"><img src='https://img.icons8.com/material-outlined/24/000000/github.png' alt='github' height='40'></a>
  <a href="https://medium.com/@cver123/about"><img src='https://img.icons8.com/color/2x/medium-logo.png' alt='Medium' height='40'></a>
</p>

<p align="center">
  <a href="https://www.linkedin.com/in/christian-verdin/">Reach me on LinkedIn</a>
</p>

---
