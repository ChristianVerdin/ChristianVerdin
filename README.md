# Hi there, I'm Christian Verdin

**Data Scientist & Full-Stack Engineer** with 7+ years of experience designing, developing, and delivering end-to-end data science, ML, and AI solutions that drive real business impact.

I build production-grade applications that integrate LLMs, real-time data pipelines, and modern web frameworks to solve complex analytical problems.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/christian-verdin/)
[![Email](https://img.shields.io/badge/Email-Contact-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:christiandverdin@gmail.com)
[![Portfolio](https://img.shields.io/badge/Portfolio-dailylocks.ai-4285F4?style=for-the-badge&logo=google-chrome&logoColor=white)](https://dailylocks.ai)
[![Medium](https://img.shields.io/badge/Medium-Articles-000000?style=for-the-badge&logo=medium&logoColor=white)](https://medium.com/@cver123/about)

---

## Featured Project

### NFL Analytics Engine
**Sports Betting Analytics & Visualization Platform**

A comprehensive analytics system for NFL betting intelligence, processing **282+ games**, **14,800+ player-quarter records**, and **1,446 TD events** for the 2025 season. Features automated matchup reports, real-time visualization generation, and multi-tier betting edge detection through the Conference Championship round.

<p align="center">
  <img src="./assets/nfl_analytics/20_skill_position_matchups.png" width="800" alt="NFL Analytics - Skill Position Matchups Dashboard">
</p>

<details>
<summary><b>View More Screenshots</b></summary>
<br>
<p align="center">
  <img src="./assets/nfl_analytics/2_efficiency_matrix.png" width="800" alt="NFL Analytics - Team Efficiency Matrix">
</p>
<p align="center">
  <img src="./assets/nfl_analytics/1_playoff_epa_comparison.png" width="800" alt="NFL Analytics - EPA Comparison Analysis">
</p>
<p align="center">
  <img src="./assets/nfl_analytics/3_quarter_scoring_heatmap.png" width="800" alt="NFL Analytics - Quarter Scoring Heatmap">
</p>
<p align="center">
  <img src="./assets/nfl_analytics/6_red_zone_breakdown.png" width="800" alt="NFL Analytics - Red Zone Efficiency Analysis">
</p>
</details>

**Key Capabilities:**
- **Matchup Intelligence System** — Generates 14-page reports per game with player trends, red zone efficiency, and situational analysis across 116 matchup reports
- **Quarter-by-Quarter Tracking** — 1,446 TD events and 14,847 player stat records with Q1-Q4 breakdowns for live betting insights
- **Visualization Engine** — 21 custom playoff visualizations including skill position dashboards, TD probability gauges, and clutch performer analysis
- **Playoff Scenario Simulator** — Win/loss impact modeling for seeding scenarios with elimination risk detection
- **Injury Context Analysis** — Distinguishes "injury beneficiaries" from "organic risers" for sustainable prop betting

**Sample Outputs:**
- [Skill Position Matchups Dashboard](./assets/nfl_analytics/20_skill_position_matchups.png) — 6-panel analysis: TD leaders, quarter scoring patterns, RB comparisons, clutch performers, receiving threats, and scoring consistency
- [Conference Championship Visualizations](https://github.com/ChristianVerdin/nfl_analytics/tree/main/outputs/reports/conference_championship_2025) — 21 betting-focused graphics for AFC/NFC title games
- [Weekly Matchup Reports](https://github.com/ChristianVerdin/nfl_analytics/tree/main/outputs/reports/matchups) — 8 weeks of detailed game intelligence (Wild Card through Conference Championship)

**Technical Highlights:**
- **Data Pipeline:** R-based ETL processing 500+ metrics per game via nflreadr API with SQLite persistence
- **Statistical Modeling:** EPA calculations, efficiency matrices, player trend detection (20%+ usage changes)
- **Visualization:** ggplot2 with custom `theme_nfl_playoff()`, multi-panel dashboards via gridExtra
- **Database:** 9 core tables + 5 quarter-level tracking tables with parameterized query wrappers
- **Automation:** Batch game analysis processing 14 games in parallel with `analyze_week_matchups.sh`

**Built With:**

`R` `tidyverse` `ggplot2` `SQLite` `nflreadr` `gridExtra` `Cairo`

[View Repository →](https://github.com/ChristianVerdin/nfl_analytics)

---

### NCAAB Analytics
**College Basketball Prediction System** | *76.3% prediction accuracy*

A production-grade analytics pipeline for NCAA Men's Basketball that combines possession-based efficiency metrics with real-time betting market data to generate daily game predictions and value opportunities.

<p align="center">
  <img src="https://img.shields.io/badge/Accuracy-76.3%25-brightgreen?style=for-the-badge" alt="Model Accuracy"/>
  <img src="https://img.shields.io/badge/Games%20Analyzed-5,900+-blue?style=for-the-badge" alt="Games Analyzed"/>
  <img src="https://img.shields.io/badge/Teams-728-purple?style=for-the-badge" alt="Teams"/>
</p>

<p align="center">
  <img src="https://raw.githubusercontent.com/ChristianVerdin/ChristianVerdin/master/images/ncaab_architecture.svg" width="800" alt="NCAAB Analytics Architecture"/>
</p>

<details>
<summary><b>View Sample Output</b></summary>
<br>

```
══════════════════════════════════════════════════════════════════════
 STRONG BET PICKS (70%+ Confidence)
══════════════════════════════════════════════════════════════════════

  1. Louisiana Ragin' Cajuns @ App State Mountaineers
     Pick: App State Mountaineers (95% confidence)
     Bet Type: MONEYLINE → TAKE_MONEYLINE

  2. Niagara Purple Eagles @ Fairfield Stags
     Pick: Fairfield Stags (95% confidence)
     Vegas: Spread -10.5 | ML: -800/490
     Bet Type: MONEYLINE_JUICED → SMALL_ML_BET

══════════════════════════════════════════════════════════════════════
 UNDERDOG VALUE PLAYS
══════════════════════════════════════════════════════════════════════

  → South Alabama Jaguars (77%)
    vs James Madison Dukes
    Vegas: +4.5 spread | ML +160
```

</details>

**Key Capabilities:**
- Possession-based efficiency metrics (KenPom-style) normalized per 100 possessions
- Iterative strength of schedule using Colley-like algorithm (10 iterations)
- Volatility detection identifying high-variance matchups for live betting
- Confidence calibration achieving 0.1801 Brier score (excellent)
- Real-time Vegas odds integration with spread value detection

**Technical Highlights:**
- **Data Pipeline:** R-based ETL processing 728 teams and 5,900+ games with incremental updates
- **Statistical Modeling:** Four-factor analysis, adaptive recency weighting (14-day half-life)
- **Prediction Engine:** Win probability calibration validated against historical performance
- **Database:** SQLite with optimized schema for analytical queries
- **Agent Integration:** Python interface syncing daily predictions to conversational AI

**Performance Metrics:**

| Metric | Result |
|--------|--------|
| Overall Accuracy | 76.3% (971/1,273 games) |
| STRONG_BET Picks | 80.8% accuracy |
| VERY_HIGH Tier | 82.4% accuracy |

**Built With:**

`R` `Python` `SQLite` `Pandas` `Statistical Modeling` `The Odds API`

---

### AI Real Estate System
**Multi-Platform Property Aggregation & Analysis**

A full-stack application that aggregates real estate listings from 5 major platforms (Zillow, Redfin, Trulia, Realtor.com, Homes.com), applying AI-powered extraction to deliver unified property data with interactive mapping and investment analytics.

<p align="center">
  <img src="./assets/ai_real_estate/search_interface.png" width="800" alt="AI Real Estate - Search Interface">
</p>

<details>
<summary><b>View More Screenshots</b></summary>
<br>
<p align="center">
  <img src="./assets/ai_real_estate/property_results.png" width="800" alt="AI Real Estate - Property Results">
</p>
<p align="center">
  <img src="./assets/ai_real_estate/map_view.png" width="800" alt="AI Real Estate - Interactive Map">
</p>
<p align="center">
  <img src="./assets/ai_real_estate/analytics_dashboard.png" width="800" alt="AI Real Estate - Analytics Dashboard">
</p>
</details>

**Key Features:**
- Multi-platform data aggregation from 5 real estate websites
- AI-powered property extraction using Firecrawl + OpenAI GPT
- Three-tier caching system (Memory -> Redis -> SQLite)
- Interactive mapping with geocoded property locations
- Investment analytics with ROI and cap rate calculations

**Technical Highlights:**
- **Frontend:** Streamlit with custom components, Plotly visualizations
- **Backend:** Python with async HTTP clients, circuit breaker pattern
- **AI/ML:** OpenAI GPT for intelligent data extraction and normalization
- **Caching:** Multi-tier LRU cache with 65-70% hit rate optimization
- **Data:** Pydantic schemas, pandas processing, multi-format exports

**Built With:**

`Python` `Streamlit` `OpenAI API` `Firecrawl` `Redis` `SQLite` `Pandas` `Folium` `Plotly`

---

### Daily Locks AI
**Production SaaS Platform with LLM-Powered Analytics**

A full-stack application featuring agentic AI that processes natural language queries against 15,000+ historical records, delivering structured insights with confidence scoring and real-time streaming responses.

**Live:** [dailylocks.ai](https://dailylocks.ai)

<p align="center">
  <img src="./assets/dailylocks/chat_interface.png" width="800" alt="Daily Locks AI - Chat Interface">
</p>

<details>
<summary><b>View More Screenshots</b></summary>
<br>
<p align="center">
  <img src="./assets/dailylocks/ai_response.png" width="800" alt="Daily Locks AI - Analysis Response">
</p>
<p align="center">
  <img src="./assets/dailylocks/games_dashboard.png" width="800" alt="Daily Locks AI - Games Dashboard">
</p>
<p align="center">
  <img src="./assets/dailylocks/settings_page.png" width="800" alt="Daily Locks AI - Settings & Billing">
</p>
</details>

**Key Features:**
- Natural language interface with context-aware prompt engineering
- Multi-model LLM routing (Claude Haiku/Sonnet/Opus) based on user tier
- Real-time streaming responses with Server-Sent Events
- Subscription management with Stripe Checkout & Customer Portal
- Persistent conversation history with full-text search

**Architecture & Technical Highlights:**
- **Frontend:** Next.js 15 App Router, React 19, TypeScript, Zustand state management
- **Backend:** FastAPI with async endpoints, intelligent agent routing system
- **AI/ML:** Anthropic Claude API, dynamic prompt construction, context windowing
- **Database:** Supabase (PostgreSQL) with Row-Level Security, real-time subscriptions
- **Auth:** JWT-based authentication with protected API routes
- **Payments:** Stripe integration (checkout sessions, webhooks, customer portal)
- **Data Pipeline:** Automated ETL processing 500+ records weekly via Playwright
- **Testing:** 116 automated tests with pytest

**Built With:**

`Next.js 15` `React 19` `TypeScript` `FastAPI` `Python` `Claude API` `Supabase` `Stripe` `Tailwind CSS` `Zustand` `Playwright`

---

## Technical Skills

<table>
<tr>
<td valign="top" width="33%">

### Languages
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-007ACC?style=flat-square&logo=typescript&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![R](https://img.shields.io/badge/R-276DC3?style=flat-square&logo=r&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=flat-square&logo=postgresql&logoColor=white)

</td>
<td valign="top" width="33%">

### Frontend
![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=next.js&logoColor=white)
![React](https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black)
![Tailwind](https://img.shields.io/badge/Tailwind-38B2AC?style=flat-square&logo=tailwind-css&logoColor=white)
![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?style=flat-square&logo=streamlit&logoColor=white)

</td>
<td valign="top" width="33%">

### Backend & Data
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![Supabase](https://img.shields.io/badge/Supabase-3ECF8E?style=flat-square&logo=supabase&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat-square&logo=pandas&logoColor=white)

</td>
</tr>
<tr>
<td valign="top" width="33%">

### AI & ML
![Claude](https://img.shields.io/badge/Claude_API-191919?style=flat-square&logo=anthropic&logoColor=white)
![OpenAI](https://img.shields.io/badge/OpenAI-412991?style=flat-square&logo=openai&logoColor=white)
![LangChain](https://img.shields.io/badge/LangChain-121212?style=flat-square&logo=chainlink&logoColor=white)

</td>
<td valign="top" width="33%">

### Infrastructure
![Vercel](https://img.shields.io/badge/Vercel-000000?style=flat-square&logo=vercel&logoColor=white)
![Railway](https://img.shields.io/badge/Railway-0B0D0E?style=flat-square&logo=railway&logoColor=white)
![Stripe](https://img.shields.io/badge/Stripe-008CDD?style=flat-square&logo=stripe&logoColor=white)

</td>
<td valign="top" width="33%">

### Tools
![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Playwright](https://img.shields.io/badge/Playwright-2EAD33?style=flat-square&logo=playwright&logoColor=white)

</td>
</tr>
</table>

---

## Let's Connect

I'm always open to collaborating on projects together so feel free to reach out!

<p align="center">
  <a href="https://www.linkedin.com/in/christian-verdin/"><img src='https://img.icons8.com/color/2x/linkedin.png' alt='linkedin' height='40'></a>
  <a href="https://github.com/ChristianVerdin"><img src='https://img.icons8.com/material-outlined/24/000000/github.png' alt='github' height='40'></a>
  <a href="https://medium.com/@cver123/about"><img src='https://img.icons8.com/color/2x/medium-logo.png' alt='Medium' height='40'></a>
</p>

<p align="center">
  <i>Open to opportunities in AI/ML engineering, full-stack development, and data-intensive applications.</i>
</p>

<p align="center">
  <a href="mailto:christiandverdin@gmail.com">christiandverdin@gmail.com</a>
</p>

---
